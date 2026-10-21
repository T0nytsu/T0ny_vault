1.開啟 power shell
2.
```
cd E:\breeze-asr
```

3.啟用虛擬環境
```
.\.venv\Scripts\Activate.ps1
```

4.
```
python transcribe.py "錄音檔路徑"
```


python transcribe.py "錄音檔路徑"

```powershell
python transcribe.py "E:\錄音\微積分 第3週.m4a"
```

```powershell
python transcribe.py "E:\錄音\10_21"
```





---
# Install
## Breeze-ASR-25 本機轉錄教學（Windows + RTX 3060）

Oct 14, 2026 · @T0ny

### 開始前

做完這 6 步，你的 RTX 3060（12 GB）就能用不量化的 float16 滿血版模型，離線把 2–3 小時的中文錄音轉成逐字稿（.txt）和字幕（.srt）。第一次安裝約 30 分鐘，大部分時間在下載；裝好之後不需要網路。

這裡用社群轉好的 CTranslate2 版模型搭配 faster-whisper 執行，比官方範例的 Transformers 寫法快，也比較省顯示卡記憶體。[官方模型](https://huggingface.co/MediaTek-Research/Breeze-ASR-25)是聯發創新基地以 Whisper-large-v2 微調、針對台灣華語與中英夾雜的版本，授權 Apache 2.0；官方評測中，長篇課程錄音 ML-lecture-2021-long 的錯誤率是 4.98%（原版 Whisper-large-v2 為 6.13%），另一組課程資料 Formosa-Course 則和原版差不多（9.94% 對 9.50%）。

|                            |              |          |
| -------------------------- | ------------ | -------- |
| 要裝的東西                      | 用途           | 下載量      |
| NVIDIA 顯示卡驅動               | 讓程式使用 GPU    | 通常已裝好    |
| Python 3.13                | 執行環境         | 約 30 MB  |
| faster-whisper + PyAV 18   | 推論引擎與音訊解碼    | 約 90 MB  |
| cuBLAS（CUDA 12）+ cuDNN 9   | GPU 運算函式庫    | 約 1.4 GB |
| Breeze-ASR-25（float16 滿血版） | 模型本體         | 2.9 GB   |
| `transcribe.py`            | 轉錄腳本，隨這份教學附上 | —        |

E 槽請預留約 6 GB（虛擬環境約 2.3 GB、模型 2.9 GB）。工作資料夾放在 `E:\breeze-asr`，不要放在 OneDrive 會同步的資料夾裡。

Python 本體（約 100 MB）和 pip 的下載快取（約 1.4 GB）預設在 C 槽；C 槽吃緊的話，步驟 3 的 pip 指令加上 `--no-cache-dir`，或裝完執行 `pip cache purge`。完成後的資料夾會長這樣：

```text
E:\breeze-asr\

├─ .venv\              Python 虛擬環境（步驟 2、3）

├─ models\float16\     模型（步驟 4）

└─ transcribe.py       轉錄腳本（步驟 5）
```

### 步驟 1：確認顯示卡驅動

只要 `nvidia-smi` 看得到 RTX 3060、右上角 CUDA Version 是 12 以上，就不用另外安裝好幾 GB 的 CUDA Toolkit。

1. 按 `Win + X`，選「終端機」（或 Windows PowerShell）。
2. 輸入下面這行後按 Enter：

```powershell
nvidia-smi
```

3. 確認三件事：表格裡的顯示卡名稱含 `RTX 3060`；右上角 `CUDA Version` 是 12.x 或更高（這是驅動支援的上限，不是已安裝的版本）；記憶體欄的總量應該是 12288MiB（工作管理員的「GPU 記憶體」會把共用的系統記憶體算進去，要以 nvidia-smi 為準）。

4. 找不到這個指令，或版本低於 12：用 NVIDIA App（或 GeForce Experience）更新驅動，或到 [NVIDIA 驅動程式下載頁](https://www.nvidia.com/Download/index.aspx)下載，裝完重開機。

### 步驟 2：安裝 Python 並建立虛擬環境

Python 3.12、3.13、3.14 都可以，這裡以 3.13 為例；所有套件都裝在 `E:\breeze-asr\.venv` 裡，不會影響電腦上其他 Python 專案。

1. 已經有 3.12–3.14 可以跳過這步（不確定就執行 `py --list` 看看）。沒有的話安裝 3.13，裝完**關掉終端機再重開**：

```powershell
winget install -e --id Python.Python.3.13
```

2. 建立工作資料夾與虛擬環境，再啟用它（用的是 3.12 就把 `-3.13` 改成 `-3.12`）：

```powershell
mkdir E:\breeze-asr

cd E:\breeze-asr

py -3.13 -m venv .venv

.\.venv\Scripts\Activate.ps1
```

3. 提示字元最前面出現 `(.venv)` 就成功了。之後每次開新視窗，都要先 `cd E:\breeze-asr`，再執行 `.\.venv\Scripts\Activate.ps1` 啟用。

出現「因為這個系統上已停用指令碼執行」時，先執行下面這行（只需一次），再重新啟用：

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

### 步驟 3：安裝 faster-whisper 與 CUDA 函式庫

在已出現 `(.venv)` 的視窗依序執行這三行；第三行約 1.4 GB，會下載比較久。

```powershell
python -m pip install --upgrade pip

pip install faster-whisper "av<19"

pip install nvidia-cublas-cu12 "nvidia-cudnn-cu12==9.*"
```

- `"av<19"` 不能省：2026/9/29 釋出的 PyAV 19 拿掉了 faster-whisper 1.2.1 讀音檔時會傳的參數，裝到 19 會出現 `open() got an unexpected keyword argument 'metadata_errors'`。這個錯誤已在測試環境實際重現，鎖在 18.1 就正常。

- faster-whisper 目前搭配的 CTranslate2 4.8 需要 CUDA 12 的 cuBLAS 與 cuDNN 9。官方 README 把 pip 裝法標成 Linux 專用，是因為 Windows 不會自動找到這些 DLL；附的 `transcribe.py` 啟動時會自己把它們的資料夾加入搜尋路徑，不必修改系統 PATH。

確認安裝成功，最後一個數字是 `1` 代表抓到 GPU（版本號日後可能更新）：

```powershell
python -c "import faster_whisper, ctranslate2; print(faster_whisper.__version__, ctranslate2.__version__, ctranslate2.get_cuda_device_count())"
```

寫這份教學時的組合是 faster-whisper 1.2.1、CTranslate2 4.8.3、PyAV 18.1.0、cuBLAS 12.9、cuDNN 9.27。

### 步驟 4：下載 Breeze-ASR-25 模型


下載 float16 版（約 2.9 GB），也就是不量化的滿血版，12 GB 顯示卡跑起來很寬裕。`hf` 指令是跟著 faster-whisper 一起裝好的。

```powershell
hf download shdennlin/breeze-asr-25-ct2 --include "float16/*" --local-dir models
```

完成後 `E:\breeze-asr\models\float16\` 裡會有 12 個檔案，其中 `model.bin` 約 2.9 GB（3,086,913,037 bytes）。下載中斷就再執行同一行，會接著下載。

|                |        |                               |
| -------------- | ------ | ----------------------------- |
| 版本             | 大小     | 適合                            |
| `float16`      | 2.9 GB | 不量化的滿血版，本教學採用（12 GB 顯示卡）      |
| `int8_float16` | 1.5 GB | 權重壓成 8-bit 的省記憶體版，適合 6 GB 顯示卡 |
| `int8`         | 1.5 GB | 純 CPU 執行                      |

這是社群使用者把[官方權重](https://huggingface.co/MediaTek-Research/Breeze-ASR-25)用 `ct2-transformers-converter`（CTranslate2 4.7.1）轉成的[CTranslate2 版](https://huggingface.co/shdennlin/breeze-asr-25-ct2)，授權同樣是 Apache 2.0；`model.bin` 是純權重檔，不含可執行的程式碼。官方原檔是 16-bit 的 BF16 權重，float16 版轉成同樣 16-bit 的 FP16，所以 `model.bin` 和官方 `model.safetensors`（3,086,761,032 bytes）幾乎一樣大。想從官方原檔自己轉，見附錄。

### 步驟 5：放上轉錄腳本並檢查 GPU

把對話裡附的 `transcribe.py`（v1.2）存到 `E:\breeze-asr\`，執行下面這行；最後一行出現 `[OK] 推論測試通過（裝置：cuda…）`，就代表 cuBLAS、cuDNN 和模型都正常。

```powershell
python transcribe.py --check
```

正常的輸出大致如下：

```text
Breeze-ASR-25 轉錄腳本 v1.2

Python 3.13.x｜faster-whisper 1.2.1｜ctranslate2 4.8.3

偵測到的 NVIDIA GPU 數量：1

已加入的 CUDA DLL 資料夾：

  E:\breeze-asr\.venv\Lib\site-packages\nvidia\cublas\bin

  E:\breeze-asr\.venv\Lib\site-packages\nvidia\cuda_nvrtc\bin

  E:\breeze-asr\.venv\Lib\site-packages\nvidia\cudnn\bin

載入模型：E:\breeze-asr\models\float16（cuda / float16）…

模型載入完成（… 秒）

執行 3 秒靜音的推論測試（會實際用到 cuBLAS 與 cuDNN）…

[OK] 推論測試通過（裝置：cuda，… 秒）。可以開始轉錄了。
```

載入模型那行顯示（cuda / float16），就代表用的是滿血版。腳本會自動找到 pip 裝的 CUDA DLL、解碼常見的音檔與影片（m4a、mp3、wav、mp4…）、用 VAD 跳過靜音，邊轉邊寫入檔案，轉錄期間也會讓電腦暫時不進入睡眠。出現錯誤，或程式沒有任何訊息就結束，請看「疑難排解」。

### 步驟 6：轉錄 2–3 小時的錄音

先用 `--minutes 2` 試跑 2 分鐘確認品質，再轉整個檔案；3 小時錄音用預設的批次模式，推估約 5–10 分鐘。

1. 試跑前 2 分鐘。路徑有空格要加引號，也可以把檔案直接拖進終端機視窗貼上路徑：

```powershell
python transcribe.py "E:\錄音\微積分 第3週.m4a" --minutes 2
```

2. 打開音檔旁邊的 `微積分 第3週.前2分鐘.txt` 看看品質，沒問題就轉整個檔案：

```powershell
python transcribe.py "E:\錄音\微積分 第3週.m4a"
```

3. 也可以整個資料夾一次轉，模型只會載入一次：

```powershell
python transcribe.py "E:\錄音"
```

轉錄時每一段都會即時顯示進度，例如 `[01:23:45 / 02:45:10  51%｜剩約 4 分 30 秒] 那這個 eigenvalue…`。中途按 `Ctrl + C` 可以中斷，已轉好的部分會留在檔案裡。

|   |   |   |
|---|---|---|
|輸出檔|內容|用途|
|`檔名.txt`|每段一行，開頭是時間戳，如 `[00:12:34] 那這個 eigenvalue 我們…`|閱讀、交給 AI 整理|
|`檔名.srt`|標準字幕檔|用 PotPlayer、VLC 邊聽邊對照，或用 Subtitle Edit 校對|

**預估時間怎麼來的**：faster-whisper 官方在 RTX 3070 Ti 上用同架構的 large-v2 轉 13 分鐘音檔，fp16 逐段模式 63 秒、batch 8 批次模式 17 秒，顯示卡記憶體約用 4.5 GB 與 6.1 GB。桌機版 RTX 3060 的運算力約是 3070 Ti 的六成，換算 3 小時錄音約是批次模式 5–10 分鐘、逐段模式 20–30 分鐘，實際以你的機器為準。12 GB 跑 batch 8 綽綽有餘，想更快可以試 `--batch 16`，記憶體不夠時腳本會自動減半重跑。

從官方範例看，Breeze-ASR-25 的輸出是用空格斷句、沒有標點；要變成好讀的文字，請看「後處理」。

以後每次使用只要三行（或用附錄的 `轉錄.bat` 直接拖曳）：

```powershell
cd E:\breeze-asr

.\.venv\Scripts\Activate.ps1

python transcribe.py "錄音檔路徑"
```

### 參數速查

參數可以混著用，例如 `python transcribe.py 檔案.m4a --hotwords "特徵值 eigenvalue" --outdir E:\逐字稿`。

|   |   |   |
|---|---|---|
|參數|預設|什麼時候用|
|`--minutes N`|整個檔案|只轉前 N 分鐘，試跑用|
|`--hotwords "詞 詞"`|無|課程專有名詞、老師名字一直被聽錯時，用空格分隔|
|`--prompt "文字"`|無|給一句情境，例如 `"線性代數課，談特徵值與對角化"`|
|`--batch N`|8|12 GB 可以試 16；記憶體不足會自動減半；`0` 改用逐段模式，可以拿來比較品質|
|`--beam N`|5|改成 1 會更快，但可能稍微不準|
|`--outdir 資料夾`|和音檔同一處|想把輸出集中放在一個資料夾|
|`--device cpu`|cuda|GPU 不能用時的備案，3 小時錄音可能要好幾個小時|
|`--model 路徑`|`models\float16`|改用 int8_float16 省記憶體版，或自己轉的模型|
|`--compute 類型`|float16|依模型自動選：float16 版用 float16，int8 版用 int8_float16，一般不用改|
|`--language 代碼`|zh|中英夾雜也維持 zh|
|`--check`|—|只檢查環境，不轉錄|
## 後處理：補標點、整理成筆記

把 `.txt` 交給 Claude 或 Gemini 補標點和分段最省事。3 小時課程以每分鐘 200–250 字估算約 3.5–4.5 萬字，建議每 30–40 分鐘切一段處理，避免輸出被截斷。

可以直接用這段提示詞：

```text
以下是一堂課的語音辨識逐字稿，每行開頭是時間戳。請：

1. 補上全形標點並依主題分段，每段開頭保留該段第一行的時間戳

2. 只修正明顯的同音錯字，不要改寫、刪減或摘要

3. 不確定的詞保留原文，後面加〔?〕

4. 專有名詞參考：（填入課程關鍵字，例如 特徵值、對角化、eigenvalue）
```

整理好的逐字稿也可以放進 Gemini Notebook（原 NotebookLM）當來源問答，或貼回對話請 Claude 整理成 Obsidian 筆記。

## 疑難排解

多數問題出在 CUDA 函式庫沒被找到；先跑 `python transcribe.py --check`，它會列出抓到的 GPU 數量與 DLL 資料夾。

| 狀況                                                            | 原因                             |
| ------------------------------------------------------------- | ------------------------------ |
| 啟用時出現「因為這個系統上已停用指令碼執行」                                        | PowerShell 預設擋腳本               |
| `py`、`hf` 或 `python` 不是可辨識的指令                                 | Python 裝完沒重開視窗，或沒啟用 `(.venv)`  |
| `Library cublas64_12.dll is not found or cannot be loaded`    | cuBLAS 沒裝在這個虛擬環境               |
| `Could not locate cudnn_ops64_9.dll`，或跑到一半沒有任何訊息就結束           | cuDNN 找不到或版本不對                 |
| `偵測不到 NVIDIA GPU`                                             | 驅動沒裝好                          |
| `[顯示卡記憶體不足]` 自動重跑，或 `out of memory`                           | 顯示卡記憶體被其他程式占用                  |
| `open() got an unexpected keyword argument 'metadata_errors'` | 裝到 PyAV 19                     |
| 同一句話重複很多次，或靜音處冒出「請不吝點讚 訂閱 轉發」這類句子                             | Whisper 系模型在長靜音、雜音時的幻覺         |
| 速度只有一、兩倍速                                                     | 加了 --device cpu，或遊戲等程式同時在用 GPU |
| 專有名詞一直錯                                                       | 模型沒看過這個詞                       |
| 偶爾出現簡體字                                                       | 模型偶發                           |
| `hf download` 很慢或中斷                                           | 網路不穩                           |

### 附錄

  

### 拖曳就轉錄的 .bat

把附的 `轉錄.bat` 放在 `E:\breeze-asr\`，之後把音檔或資料夾拖到它的圖示上就會開始轉錄，不用每次開終端機啟用環境。它的內容如下，會直接呼叫虛擬環境裡的 Python：

```bat
@echo off

chcp 65001 >nul

if "%~1"=="" (

  echo 把音檔或資料夾拖到這個檔案的圖示上，就會開始轉錄。

  pause

  exit /b

)

"%~dp0.venv\Scripts\python.exe" "%~dp0transcribe.py" %*

pause
```

#### pip 版 CUDA 函式庫無效時：手動放 DLL

faster-whisper 官方 README 列的 Windows 備案，是 Purfview 整理的 DLL 包。到 [whisper-standalone-win 的 libs 頁面](https://github.com/Purfview/whisper-standalone-win/releases/tag/libs)下載 CUDA12 的 Windows 版（CUDA12\_v3 為 cuBLAS 12.8.4.1 + cuDNN 9.8.0.87），解壓縮後把所有 `.dll` 放進 `E:\breeze-asr\cuda_dlls\`，打不開壓縮檔就用 7-Zip。`transcribe.py` 會自動把這個資料夾加入搜尋路徑，放好後再跑一次 `python transcribe.py --check` 確認。

#### 從官方原檔自己轉換模型

想完全從聯發科的官方權重開始，可以照 faster-whisper README 的方法自己轉。這會多裝 PyTorch 與 Transformers，並下載約 3.1 GB 的官方 `model.safetensors`：

```powershell
pip install "transformers[torch]>=4.23"

ct2-transformers-converter --model MediaTek-Research/Breeze-ASR-25 --output_dir models\breeze-float16 --copy_files tokenizer.json preprocessor_config.json --quantization float16

python transcribe.py --check --model models\breeze-float16
```

官方 repo 裡另有 3.6 GB 的訓練用 `optimizer.bin`，轉換用不到，所以不要用 `hf download` 整包抓。這段轉換沒有經過實測，出錯的話把錯誤訊息貼給 Claude。
### 參考資料

- [MediaTek-Research/Breeze-ASR-25 模型卡](https://huggingface.co/MediaTek-Research/Breeze-ASR-25)：架構、授權、評測數據、官方用法
- [shdennlin/breeze-asr-25-ct2](https://huggingface.co/shdennlin/breeze-asr-25-ct2)：CTranslate2 轉換版與各量化版本、轉換來源
- [SYSTRAN/faster-whisper](https://github.com/SYSTRAN/faster-whisper)：GPU 需求、效能數據、批次模式與 VAD
- [Purfview/whisper-standalone-win libs](https://github.com/Purfview/whisper-standalone-win/releases/tag/libs)：Windows 用的 cuBLAS / cuDNN DLL 包
- PyPI 上的 [av](https://pypi.org/project/av/)、[nvidia-cublas-cu12](https://pypi.org/project/nvidia-cublas-cu12/)、[nvidia-cudnn-cu12](https://pypi.org/project/nvidia-cudnn-cu12/)、[ctranslate2](https://pypi.org/project/ctranslate2/)：版本與 Windows 安裝檔，2026/10/14 查證

