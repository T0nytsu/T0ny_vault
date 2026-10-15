---
course: [PROG1]
semester: "115-1"
chapter: ["1"]
tags: [programming, lecture]
source:
  - "Computer_Programming_Deck1_AI_PBL_English_v3.pptx.pdf（Deck 1 投影片）"
  - "Computer_Programming_Deck1_ClassNotes_ZH.pdf（Deck 1 中文補充講義）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W1：Deck 1 How Can We Make a Computer Solve a Problem? 投影片（English）與中文補充講義融合，依 inquiry ladder（Q1–Q7）排列。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答；其餘內容都來自投影片與講義。輸出一律收在 `[!solution]-` 裡：先預測，再展開。
> 兩份期中考古題與解答在 [[PROG1 Midterm 考古題]]。
> 下一個：[[PROG1 Deck 2 整理]]

> [!tip] Claude 補充：五個 Deck 是同一個專案的五個版本
> 每個 Deck 都在同一個 `student-utility-toolkit` repository 新增一個檔案，舊檔保留；投影片一再強調「不要開第二個 repository」。
>
> | Deck | 檔案 | 版本 | 新增能力 | 新語法 |
> | --- | --- | --- | --- | --- |
> | 1 | `main.py` | v0.1 | km → miles | `input()`、`float()`、`print()` |
> | 2 | `trip_summary.py` | v0.2 | 路線、英里、平均速度（假設輸入有效） | 型態、指派、算術、f-string |
> | 3 | `trip_decisions.py` | v0.3 | 先驗證再計算；Short／Medium／Long | 比較、`and`／`or`／`not`、`if`／`elif`／`else` |
> | 4 | `trip_log.py` | v0.4 | 多筆行程、`DONE` 結束、只累加有效資料 | `for`、`range`、`while`、`break`、`continue` |
> | 5 | `trip_text.py` | v0.5 | 一行輸入 `Campus East,12.5,45` | 索引、切片、`strip`、`split`、`try`／`except` |
>
> 每個 Deck 都重複同一套流程：先寫規格（contract）→ 手算預期答案 → 寫或請 AI 產生程式 → 用獨立測試檢查 → commit、push、上網確認。

## Deck 1：電腦如何解決問題

對應投影片：Deck 1｜1–5（Q1–Q7 各節另標）。

> [!question] Driving question
> How can we make a computer solve a problem?
>
> Problem → Representation → Code → Execution → Verification
>
> Today is about building a mental model: how a human problem becomes an executable and verifiable program.

> [!note] 核心觀念
> 程式設計不是「把語法打進電腦」。程式設計是把一個人的問題，變成電腦可以精確執行、我們可以檢查，而且可以持續修改與分享的解法。

**This is not a syntax-first Python course.** Programming in the AI era starts from problems, not commands.

| Old default | New goal |
| --- | --- |
| Today we teach variables, operators, loops, and functions. | Use programming and AI to turn real problems into executable, testable solutions. |

- Each class begins with a driving question.
- Every concept is introduced because it helps answer that question.
- AI can generate code, but students must define, inspect, test, and revise it.
- The final target is project capability, not memorized syntax.

課程節奏：Question → Concept → Example → Live code → AI workflow → Project。

| What students do | What AI does |
| --- | --- |
| Predict outputs, run code, inspect errors, design tests, and make small modifications. | Generate a candidate solution, explain errors, suggest tests, and help refactor code. |

Human responsibility: problem formulation, execution reasoning, and verification.

Inquiry ladder（每個問題都帶出一個概念、一個 demo、一個小練習）：

1. Q1 What kind of problems can a computer solve?
2. Q2 What does a computer actually do?
3. Q3 How does a computer represent information?
4. Q4 What is a program?
5. Q5 How does Python execute our code?
6. Q6 If AI can write code, why learn programming?
7. Q7 How do we save and push the first code to GitHub?

閱讀方法：先回答問題，再理解概念，再看程式，最後用執行結果或測試驗證自己的理解。

## D1-Q1 什麼樣的問題可以交給電腦解

對應投影片：Deck 1｜6–9。

> [!definition] 定義：Input → Process → Output
> 初學者最實用的第一個模型不是「先學 variable」，而是先問三件事：
> 1. **Input**：程式拿到什麼資料？（Data given to the program）
> 2. **Process**：程式要做什麼計算或判斷？（Computation or decision）
> 3. **Output**：最後要得到或顯示什麼結果？（Result shown or saved）
>
> Programming begins before code: specify what goes in, what happens, and what comes out.

整堂課的主線例子：Celsius → Fahrenheit。

$$
F = C \times \frac{9}{5} + 32
$$

| Input | Process | Output |
| --- | --- | --- |
| Celsius temperature $C$ | $C \times 9/5 + 32$ | Fahrenheit temperature $F$ |

如果輸入 $C = 0$，不寫任何程式就能算出預期答案 $F = 32$。**在程式碼之前，我們已經知道問題的規格與至少一個可以檢查的答案。**

| Problem statement | Before code | After code |
| --- | --- | --- |
| Input a Celsius temperature and output the corresponding Fahrenheit temperature. | What data goes in? What computation happens? What result comes out? | Run it. Test it. Fix it. Push it. |

> [!question] Quick Challenge 1：decompose first, code later
> 兩分鐘自己想，再和旁邊同學討論一分鐘。Do not use AI yet. Practice human problem formulation first.
>
> | Problem | Input | Process | Output |
> | --- | --- | --- | --- |
> | Birth year → age | ? | ? | ? |
> | Score → pass/fail | ? | ? | ? |
> | Several numbers → average | ? | ? | ? |

> [!solution]- 講義的討論：為什麼要先定義問題，而不是先問 AI
> - 「輸入出生年，算年齡」不夠完整。只知道出生年，通常只能算「某參考年份減出生年份」的近似年齡；要精確年齡，還必須知道生日與參考日期。
> - 「score → pass/fail」需要先定義及格門檻。
> - 「several numbers → average」需要先定義資料集合，也要思考空集合怎麼處理。

> [!note] 核心觀念
> AI 可以很快寫出程式，但 AI 無法替你消除一個沒有被定義清楚的需求。模糊問題通常只會得到一個看似合理、但規格可能錯誤的程式。

## D1-Q2 電腦實際上在做什麼

對應投影片：Deck 1｜10–15。

> [!definition] 定義：Hardware 與 Software
> **Hardware** 是實體裝置，例如 CPU、memory、storage、keyboard、display、network interface。
> **Software** 是告訴硬體要做什麼的程式，例如作業系統、Python、VS Code 與你自己寫的 `main.py`。

Original idea retained: a computer is input + storage + computing + output.

| 功能 | 說明 |
| --- | --- |
| Input | 鍵盤、滑鼠、檔案、感測器、網路請求等資料來源。 |
| Storage | 把檔案與程式保留下來，程式結束或電腦關機後仍可存在。 |
| Computing | CPU 執行低階 machine instructions，逐步改變計算狀態。 |
| Output | 文字、影像、檔案、聲音或網路回應。 |

```python
name = input("Name: ")
print("Hello", name)
```

`input()` 收集資料，`print()` 產生輸出，而中間的執行工作最終由 CPU 完成；Python executes the statements in order.

**按下 Run 之後發生什麼事？** 簡化但有用的模型：

source file on storage → running process in RAM → Python runtime → CPU executes machine instructions → output

- 你的 `main.py` 平常是保存在 SSD／HDD（secondary storage）上的檔案。
- 執行時，作業系統建立 Python process；程式執行所需的 code 與 data 出現在 memory 中。
- CPU 執行 Python runtime 所需要的 machine instructions，runtime 再依照你的 Python source 執行工作。
- 這是概念模型，不是說資料永遠以一條單向輸送帶「storage → RAM → CPU」移動。真實系統還有 cache、virtual memory、I/O controller、DMA 等機制。

More computer foundations will return in Decks 2–6, when the programming problem needs them.

**CPU、RAM、Storage 有什麼不同？**（A common beginner confusion）

| 元件 | 主要角色 | 程式設計直覺 |
| --- | --- | --- |
| Storage | 長期保存檔案；Keeps files after the program stops | `main.py`、README、資料檔平常放在這裡 |
| RAM／Memory | 暫時保存執行中的程式狀態與資料 | 執行期間使用的資料與物件（variables）存在這裡，要能被 processor 快速存取 |
| CPU | 執行 machine instructions | 真正進行 load、store、arithmetic、branch 等低階步驟的處理器 |

好記的比喻：**storage 是倉庫，RAM 是工作桌，CPU 是工作的人。**

> [!note] Key idea
> Running program state is temporary. To keep a result after the process ends, save the data explicitly.

**為什麼常說 CPU「直接存取 RAM」，而不是直接把 SSD 當成 memory？** CPU 的一般 machine instruction 可以使用 memory address，例如概念上的：

```text
LOAD register, [memory address]
STORE [memory address], register
```

- RAM 就是為這種低延遲、可定址的工作負載設計。
- SSD／HDD 是 block-oriented I/O device，主要追求容量、持久性與每 GB 成本。要讀 storage，通常由 OS／driver 對 storage controller 發出 I/O request，把需要的 block 搬到 RAM，之後 CPU 再使用它。
- 所以「CPU 不能存取 SSD」不完全精確。更精確地說：CPU 可以控制 storage I/O，但 storage 通常不是 CPU 一般 load／store 所使用的主記憶體位址空間。
- 這也解釋為什麼開啟大型程式時會先有「loading」：程式與資料需要從 persistent storage 進入執行中 process 可以使用的 memory。

> [!definition] 定義：Fetch → Decode → Execute
> CPU 的第一個模型，先用三個動詞理解：
> 1. **Fetch**：取得下一個 machine instruction。
> 2. **Decode**：判斷 instruction 要做什麼、使用哪些 operands。
> 3. **Execute**：執行 operation，更新 register、memory 或控制流程（update the machine state）。
>
> 然後 Next instruction → Fetch again。

> [!question] 先想一想
> 一行 Python，例如 `print(3 + 5)`，是不是等於一個 CPU instruction？

> [!solution]- 答案
> 不是。一個 Python operation 通常需要 Python runtime 執行許多底層 machine instructions。之後學 assembly 時會更清楚看到這個層次差異。

> [!warning] Claude 提醒：考古題考過電腦硬體的是非題
> 兩份考古題的第 1 題都有硬體概念：instruction set、RISC／CISC、L1／L2 cache、時脈與效能、DRAM 斷電後資料消失、system software。新講義只教到這一節與 [[PROG1 Deck 4 整理#D4 電腦基礎：向後跳躍與記憶體區域性|D4 電腦基礎：向後跳躍與記憶體區域性]]、[[PROG1 Deck 5 整理#D5-Q5 字元如何變成位元組並被保存|D5-Q5 字元如何變成位元組並被保存]]，其餘整理在 [[PROG1 Midterm 考古題#新講義沒教的舊考點|新講義沒教的舊考點]]。

## D1-Q3 電腦如何表示資訊

對應投影片：Deck 1｜16–19。

在低階儲存層次，資料最後由 bits（0 與 1）表示；在 Python 程式中，我們通常不直接操作 bits，而是操作 value 與 type。

> [!definition] 定義：Data = value + type
> data = value + type + operations that make sense for that type
> - **Value**：The stored information: `65`, `65.0`, `"65"`.
> - **Type**：How Python interprets the value: `int`, `float`, `str`.
> - **Operation**：What you can do with it: add numbers, concatenate strings.
>
> `65`、`65.0`、`"65"` 看起來都和「65」有關，但分別是 int、float、str，因此可做的運算不同。

**同一組 bits 可以有不同 interpretation。** 只看一個 8-bit pattern `01000001`：

- 用 unsigned integer 的規則解讀，它代表 decimal 65。
- 把 65 當成 ASCII code，對應字元 `A`。

重點：bits 本身需要 interpretation rule 才有程式層次的意義。技術上要注意：Python 的 `int(65)` 與字串 `"A"` 並不是「記憶體裡完全相同的 bits 只換一個 type label」；Python objects 有自己的 runtime representation。這張 8-bit 圖是在解釋「底層 bit pattern 的意義取決於 encoding／type interpretation」。

```python
print(chr(65))      # A
print(ord('A'))     # 65
```

用 `chr` 與 `ord` 看 code point 與 character 的對應。

**Type 也決定 operator 的行為**（Predict before running）：

> [!example] 範例：它們看起來都是 65
> ```python
> print(65 + 1)
> print(65.0 + 1)
> print("65" + "1")
> print("65" + 1)
> ```

> [!solution]- 結果
> | Expression | 結果 | 為什麼 |
> | --- | --- | --- |
> | `65 + 1` | `66` | int + int：numeric addition |
> | `65.0 + 1` | `66.0` | float 與 int 進行數值運算，結果為 float |
> | `"65" + "1"` | `"651"` | str + str：string concatenation |
> | `"65" + 1` | `TypeError` | Python 不替你猜「要數值加法還是字串串接」 |

因此 `+` 並不是永遠代表同一個實作；operand 的 type 會影響 operation 的意義。

```python
print(int("65") + 1)   # 66
print("65" + str(1))   # 651
```

想做數值運算就先 `int(...)`，想做字串串接就先 `str(...)`。

> [!note] 核心觀念
> 初學 Python 時，不要只看畫面上「長得像什麼」。要問：這個 value 的 type 是什麼？這個 operator 對這些 types 定義了什麼行為？
>
> A type mismatch can appear in human-written or AI-assisted code. Always check what the input means.

Bits matter, but type is the programming lesson：

| Computer storage | Programming view | Why this matters |
| --- | --- | --- |
| At a low level, data is represented using 0s and 1s. | At the Python level, we work with values and types. | Type determines whether `+` means numeric addition or string concatenation. |

```python
3 + 5          # numeric addition
"3" + "5"      # string concatenation
```

> [!warning] Claude 提醒：考古題的資料表示是非題
> 考古題 A 1(j)(m)(n)、B 1(i)(k)(l) 都考這一節：「所有資料都以 0／1 儲存」是 T；「只給一個 byte 就能解讀它的意義」是 F（要知道 encoding／type）；「數字和字元是 0／1，圖片和音樂不是」是 F。

## D1-Q4 什麼是 Program

對應投影片：Deck 1｜20–22。

> [!definition] 定義：Algorithm 與 Source code
> **Algorithm** 是一系列清楚、有限、可執行的步驟，用來完成指定問題（A sequence of well-defined steps that solve the problem）。
> **Source code** 是把 algorithm 用某個 programming language 精確表達出來（The algorithm expressed precisely in a programming language）。

Human problem → Algorithm → Source code → Execution → Result。A program is a precise, executable solution — not mysterious syntax, not magic. Programming is the process of turning the problem into exact instructions that the computer can execute and that we can verify.

**Pseudocode first**：先解決「解法結構」，再處理 programming language 的 syntax。

```text
1. Read Celsius value C
2. Compute F = C * 9 / 5 + 32
3. Display F
```

```python
c = float(input("Celsius: "))
f = c * 9 / 5 + 32
print(f)
```

> [!question] Mini activity
> Write 3-line pseudocode for a BMI calculator before writing any Python.

**精確性比「大概知道」更重要。** 人與人說話可以靠常識補足細節，電腦不會。BMI calculator 至少要先知道輸入的身高單位與體重單位、公式如何定義，以及輸出只要 BMI 數值還是還要分類。

> [!note] 核心觀念
> 好的程式不是「很多 code」，而是需求、algorithm、source code 與 tests 彼此一致。

## D1-Q5 Python 如何執行我們的程式

對應投影片：Deck 1｜23–35。

**High-level language、Assembly、Machine language**：用同一件事「把 65 加 1」看三個層次。

```python
x = 65
x = x + 1
```

```text
MOV EAX, 65
ADD EAX, 1
```

上面是 assembly-like representation（示意）。Machine language 則是 CPU architecture 定義的 binary instruction encoding；不同 CPU architecture（x86、ARM、RISC-V）有不同 instruction set 與 machine code。

| 層次 | 意思 |
| --- | --- |
| High-level language | 接近人的問題描述，隱藏大量 processor-level 細節，例如 Python、C、Java。Readable code closer to human problem solving. |
| Assembly language | 用 mnemonic 表達低階 instruction，例如 `MOV`、`ADD`；仍與特定 architecture 密切相關。 |
| Machine language | CPU 真正解碼與執行的 instruction bit patterns。 |

> [!note] 核心觀念
> High-level language 主要讓我們描述「要做什麼」；assembly 更接近描述 processor「一步一步怎麼做」；machine code 是 CPU 實際執行的編碼。
> Python is high-level: it lets us describe computations without manually managing CPU-level instructions.

**Compiler：translate first, run later.** Source code → Compiler → Machine code → Run executable。

- A compiler translates a high-level program into another program, often machine code.
- After translation, the compiled program can be executed repeatedly.
- Typical teaching examples: C and C++.
- For Week 1, remember the direction: source code → compiler → executable program.

> [!definition] 定義：Compilation 與 Interpretation
> **Compilation** 是把一種 program representation 轉換成另一種 representation；target 可能是 machine code，也可能是 bytecode。
> **Interpretation** 是由另一個 program／runtime（or virtual machine）來執行某種 representation；compilation may happen first.
>
> 常見 C／C++ 教學模型：source code → compiler → native executable → run。這是一個常見 ahead-of-time workflow，但不能推論「一種語言永遠只能 compiler 或 interpreter 二選一」。C/C++ and Python are examples, not a rule that every language uses only one strategy.

**CPython 的實用工作模型**（class demo 用的 implementation）：

Python source → parse／compile → bytecode → Python runtime executes it

- Python bytecode 不是 CPU native machine code。最終 CPU 執行的是 Python runtime 與相關 library 的 machine instructions。
- 對這門課最重要的不是背 bytecode，而是知道：你寫的是 source code；Python runtime 讀取、檢查並執行它；CPU 在更低層真正執行 machine instructions。
- **Syntax error**：A syntax error in `main.py` prevents that script from starting.
- **Runtime error**：A valid script may start, then fail while executing an operation.

In this course: edit Python source → run it with Python → inspect the result.

> [!warning] Claude 提醒：考古題的 interpreter 是非題和新講義說法不一樣
> 考古題 A 1(o)、B 1(m) 都是「A python interpreter translates the high-level language to the machine language before the program can be executed.」2021 手寫參考答案給 **T**；但這一節明講 CPython 先編譯成 bytecode，而「Python bytecode 不是 CPU native machine code」，照新講義應判 **F**。W2 補課影片（Interpreter and Compiler）看的時候留意老師用哪一種說法；今年若出這題，最好考前問老師或助教以哪個為準。詳見 [[PROG1 Midterm 考古題#考古題 A：Midterm I（年份不明）|考古題 A：Midterm I（年份不明）]]。

**Interactive mode 與 Script mode**（The same Python language, two ways to submit code）：

```pycon
>>> 3 + 5
8
```

在 REPL（`>>>` prompt）輸入一個 expression，Python 會顯示它的結果。Script mode 把 code 存在 `main.py` 再執行：

```python
3 + 5
```

只把上面一行存進 `main.py` 後執行，通常不會自動顯示 8；要顯示結果需要 `print(3 + 5)`。

> [!note] 不要把兩種環境混在一起
> `>>>` 是 Python interactive prompt；`python main.py` 是 shell／terminal command。Type Python code at `>>>`. Type `python main.py` in the terminal shell, not at `>>>`.

**From a local folder to a running `main.py`**（Suggested class setup: VS Code + Python 3）：

1. Desktop → File → New repository: name it `student-utility-toolkit`.
2. Choose a parent folder; select README and the Python `.gitignore` template.
3. VS Code → Open Folder: open the project folder Desktop created.
4. Select a Python 3 interpreter. Create a file named `main.py`, not `main.py.txt`.

```text
student-utility-toolkit/
    main.py
    README.md
```

```python
print("Hello, world!")
```

Install Python 3, VS Code + its Python extension, and Desktop before class.

**開發迴圈：Edit → Save → Run → Inspect（Read evidence）→ Revise**。第一次寫 Python 最重要的習慣不是一次寫完，而是建立短迴圈：

1. 在 editor 修改 `main.py`。
2. Save。
3. Run：editor 裡選 Run Python File in Terminal，或在 terminal shell（含 `main.py` 的資料夾）打 `python main.py`；依安裝可能要用 `python3` 或 `py`。
4. 看 actual output 或 error message。
5. 根據 evidence 修改，再執行一次。

At `>>>`? Run `exit()` first. Command not found? Check the Python installation. 這個 loop 之後會自然擴充成 test、debug、commit 與 push。

> [!example] Live Demo 1：your first Python program
> Predict first, run second, explain last. What will each line output? How are line 3 and line 4 different?
> ```python
> print("Hello, world!")
> print("I am learning programming.")
>
> print(3 + 5)
> print("3 + 5")
> ```

> [!solution]- 執行結果（Claude 執行）
> ```text
> Hello, world!
> I am learning programming.
> 8
> 3 + 5
> ```
> 第 3 行的 `3 + 5` 是 expression，先算成 8 再印；第 4 行是字串，原樣印出。

Learning rule：Prediction builds a mental model. Execution gives evidence. Explanation turns output into understanding.

**Syntax、Expression、Statement**（Valid code has a structure; execution gives that structure meaning）：

> [!definition] 定義：Syntax
> **Syntax** 是 Python 的文法規則：一段程式是否符合 language grammar。
> ```python
> if x > 5:
>     print("Large")
> ```
> 少了冒號就是 syntax error：
> ```python
> if x > 5
>     print("Large")
> ```

> [!definition] 定義：Expression
> **Expression** 是 evaluate 之後會得到一個 value 的程式片段：
> ```python
> 3 + 5
> 10 > 3
> "Hello" + " World"
> ```
> 分別得到 `8`、`True`、`"Hello World"`。

> [!definition] 定義：Statement
> **Statement** 是 Python grammar 中可執行的完整敘述（an executable unit）：
> ```python
> result = 3 + 5
> ```
> 這是 assignment statement，其中 `3 + 5` 是 expression。再看：
> ```python
> if y > 12:
>     print(y)
> ```
> `y > 12` 是 expression，整個 if structure 是 statement。

技術細節：`print(result)` 是 function-call expression；當它單獨出現在一行時，形成 expression statement。第一週不必記 grammar 名稱，重點是分辨「產生 value」與「控制／執行程式」的角色。A `#` starts a comment.

```python
print("Hello")                 # valid
print("Hello"                  # invalid
```

**Variable：替資料取一個有意義的名字**（This is only a preview; Deck 2 will develop it formally）：

> [!example] 範例：variable
> ```python
> name = "Amy"
> age = 20
> print(name)
> print(age + 1)
> ```

> [!solution]- 執行結果（Claude 執行）
> ```text
> Amy
> 21
> ```

- A variable name helps code read like a human solution.
- 初學時可以把 variable 想成「程式目前用來指稱某份資料的名字」。
- 不要把 Python variable 直接當成數學中的未知數；assignment 可以讓一個名稱在程式執行過程中指向新的 value。

**為什麼 `input()` 是第一個 type 陷阱？** `input()` always returns a string first：

> [!example] 範例：輸入 3 與 5
> ```python
> x = input("x = ")
> y = input("y = ")
> print(x + y)
> ```

> [!solution]- 結果
> ```text
> 35
> ```
> 實際上做的是 `"3" + "5"` → `"35"`。The program runs, but the result does not match our intended computation.

修正：convert input text into numbers。Type conversion aligns the operation with the problem.

```python
x = float(input("x = "))
y = float(input("y = "))
print(x + y)
```

這裡的 type conversion 不是形式動作，而是讓 program operation 與問題真正需要的 computation 對齊。Vocabulary：`input()`、`print()`、`int()`、`float()`、`str()`。

> [!tip] Claude 補充：修正後的輸出是 8.0，不是 8
> 同樣輸入 3 與 5，修正版印出 `8.0`（Claude 執行）：`float()` 產生 float，float + float 還是 float。想得到 `8` 要用 `int()`，但那就只能輸入整數。

> [!question] Mini challenge
> Turn this pattern into a Celsius → Fahrenheit converter.

## D1-Q6 如果 AI 可以寫 code，為什麼還要學 Programming

對應投影片：Deck 1｜36–45。

**AI use in this course**：Use AI in today's practice. Keep ownership of the reasoning and the evidence.

| Allowed and encouraged | Your responsibility |
| --- | --- |
| Ask for concept explanations. | Explain the submitted code. |
| Request candidate code or a plan. | Run it yourself. |
| Ask for the smallest bug fix. | Check expected versus actual output. |
| Generate test ideas. | Describe AI help and your revisions. |
| Compare possible approaches. | Keep secrets and private data out. |

Keep a short, sanitized AI-use record. Explain what you changed and how you tested it. Assessment-specific instructions determine whether AI is allowed in each exam or assignment.

> [!definition] 定義：AI-generated code 是 candidate solution，不是答案證明
> AI 可以生成程式、解釋錯誤、提出測試案例，但它不知道你的程式是否真的滿足規格，除非你提供足夠清楚的需求，而且你仍然需要獨立驗證。
> 工作流：**Ask → Inspect → Run → Test → Revise**。

> [!failure] 故意錯誤的範例：AI-generated code is a candidate solution
> Teaching example with a deliberately inserted bug — not a recorded AI response. Live prompt：Write a Python script that converts Celsius to Fahrenheit. Assume numeric input. State the formula and suggest two test inputs.
> ```python
> c = input("Celsius: ")
> f = c * 9 / 5 + 32
> print(f)
> ```
> 1. Predict: what type does `input()` produce?
> 2. Run: read the actual error before changing anything.
> 3. Revise one line; then run the independent test cases.

> [!solution]- 講義的分析
> 先不要急著改。先問：`input()` 的 type 是什麼？答案是 `str`。因此這段程式在 numeric computation 上會失敗。最小的 intended correction 是：
> ```python
> c = float(input("Celsius: "))
> ```
> 但「程式現在能跑」仍不等於「程式一定正確」，還要測試。If the live AI response is correct, inspect and test it; do not pretend it failed.

> [!tip] Claude 補充：錯誤其實發生在 `/ 5`
> 輸入 `0` 時 `c` 是 `"0"`，`c * 9` 不會出錯，而是字串重複得到 `"000000000"`；接著 `/ 5` 才拋出 `TypeError: unsupported operand type(s) for /: 'str' and 'int'`（Claude 執行，Python 3.13）。字串可以乘整數這件事，在 [[PROG1 Deck 5 整理#D5-Q1 文字的意義從哪裡來|D5-Q1 文字的意義從哪裡來]] 的 `"Trip " * 2` 和考古題 A2 都會用到。

Today's rule：Whenever AI generates code, include at least two test cases（$C = 0 \to F = 32$，$C = 100 \to F = 212$）。Use tests as evidence for specified cases. Passing two examples does not prove correctness for every input.

> [!definition] 定義：Test case
> **Test case = specified input + independently justified expected result.**
> Expected value 應先從需求或公式獨立算出，再去比較程式 actual output。

| Input C | Expected F | Actual F | Verdict |
| --- | --- | --- | --- |
| 0 | 32 | Run to find out | Compare |
| 100 | 212 | Run to find out | Compare |
| −40 | −40 | Run to find out | Compare |

Before you run: compute the expected result from $F = C \times 9/5 + 32$. After you run: record the actual result. A disagreement needs investigation.

如果只是再問另一個 AI「這個答案對不對」，那並不是很強的 independent oracle；兩個模型可能共享同一個錯誤假設。An AI agreeing with another AI is not an independent test oracle.

> [!note] 核心觀念
> Passing two or three examples is evidence, not mathematical proof of correctness for every possible input. 但對初學程式而言，先養成「預期結果 ↔ 實際結果」的驗證習慣非常重要。

**Program development cycle（AI-native version）**：Understand → Design → Generate／Write → Run → Debug → Verify。

- If you do not understand the problem, AI can quickly generate the wrong program.
- If you do not understand the program, you cannot know whether AI wrote it correctly.
- If you cannot debug, you are only copying errors repeatedly.

**三種常見錯誤**（Run these examples separately. Read the evidence, then choose the smallest fix）：

> [!definition] 定義：Syntax error
> 程式寫法不符合語法；Python cannot parse the current script，因此回報 `SyntaxError`。
> ```python
> print("Hello"
> ```

> [!definition] 定義：Runtime error
> 語法正確，但執行某個 operation 時失敗。除以零產生 `ZeroDivisionError`；`"65" + 1` 產生 `TypeError`。
> ```python
> print(3 / 0)
> ```
> ```python
> print("65" + 1)
> ```

> [!definition] 定義：Logic error
> 程式跑完了，但違反需求（The program runs, but violates the requirement）。
> ```python
> f = 0 * 9 / 5 + 30
> print(f)
> ```
> 程式正常輸出、沒有 exception；但 Celsius 0 應該得到 Fahrenheit 32。錯誤在公式中的 `+30`，應該是 `+32`。

> [!warning] Claude 提醒：實際印出的是 30.0
> 講義與投影片寫「輸出 30」，Python 實際印 `30.0`（Claude 執行）：`/` 一律產生 float，所以 `0 * 9 / 5` 是 `0.0`，加 30 得 `30.0`。寫「螢幕輸出」的題目時，`/` 帶來的 `.0` 很容易漏掉。

| 錯誤類型 | 發生方式 | Python 通常會不會直接報錯 |
| --- | --- | --- |
| Syntax error | 目前 script 無法被正確 parse | 會 |
| Runtime error | script 開始執行後某個 operation 失敗 | 會 |
| Logic error | 程式可以執行，但結果不符合 specification | 通常不會 |

這就是為什麼「程式沒有 error message」不能當成 correctness 的證明。

> [!definition] 定義：Debugging 的基本順序
> 遇到 bug 時不要隨機改 code：**Read the error → Locate the line → Form a hypothesis → Test one fix.**
> 例如 `print(hello)`：如果 `hello` 沒有定義，會得到 `NameError`。真正的修正取決於你的意圖：想印文字，可能是 `print("hello")`；想印 variable，就應先定義它。不要看到 error 就隨便把某個 token 換掉。

> [!question] Bug Hunt：classify and fix
> 三分鐘分組討論。
> - A：`print("Hello"`
> - B：`print(hello)`
> - C：`print(3 / 0)`

> [!solution]- 依講義的分類
> - A：Syntax error（`SyntaxError`），補上右括號。
> - B：Runtime error（`NameError`），依意圖改成 `print("hello")` 或先定義 `hello`。
> - C：Runtime error（`ZeroDivisionError`），除數不能是零。

Good AI debugging prompt：Here is my code. Here is the error message. Explain what happened and suggest the smallest fix.

> [!warning] Claude 提醒：考古題的錯誤題
> - 考古題 A 1(q)、B 1(o)「Most of the logic errors can be directly identified by the python IDE」是 **F**：logic error 通常不會報錯。
> - 考古題 B7「找出三個 syntax errors」裡，`while true:` 在 Python 3 其實是執行時的 `NameError`，不是 `SyntaxError`；考題把它算成 syntax error，作答時照樣改成 `True`。見 [[PROG1 Midterm 考古題#B7 改正三個語法錯誤（10 分）|B7 改正三個語法錯誤（10 分）]]。

## D1 Practice：把問題變成可測試的程式

對應投影片：Deck 1｜42–43。

> [!example] Worked example：Gross Pay
> Problem：Input hours worked and hourly pay; output gross pay.
> ```text
> 1. Read hours
> 2. Read hourly pay
> 3. gross = hours * pay
> 4. Display gross
> ```
> ```python
> hours = float(input("Hours: "))
> pay = float(input("Hourly pay: "))
> gross = hours * pay
> print("Gross pay:", gross)
> ```
> 這個例子同時包含 Input、type conversion、variable、expression、statement 與 Output。Notice: variable names make the code explain the problem.

> [!question] Practice 1：km → miles converter
> 10 minutes: write pseudocode first, then Python. 公式：miles = km × 0.621371。至少包含：
> - at least one `input()`、one `float()`、one variable、one `print()`
> - at least two test cases（自己先算好）
>
> You may use AI, but you must identify Input / Process / Output and design your own tests.

> [!solution]- 講義的 possible implementation
> ```python
> km = float(input("Distance in km: "))
> miles = km * 0.621371
> print("Distance in miles:", miles)
> ```
> 請不要把「AI 給的兩個 tests」直接當成獨立驗證。至少其中一個 expected output 自己根據公式計算。

## D1-Q7 Git 與 GitHub 在程式設計中做什麼

對應投影片：Deck 1｜46–52、56。

**為什麼程式需要 version control？** 沒有 Git 時，很多人會得到：

```text
main.py
main_new.py
main_final.py
main_final2.py
main_really_final.py
```

這其實是人在手動做版本管理。Git 的目的，是把版本歷史變成系統化、可追蹤的紀錄。

> [!definition] 定義：Git 與 GitHub
> **Git** 是 version-control system，主要管理 local repository 的 change history。
> **GitHub** 是 hosting service，用來保存 remote repository，方便分享、合作與建立 portfolio。
>
> $$
> \text{Git} \neq \text{GitHub}
> $$
>
> Git 管版本；GitHub 放 remote copy、分享與協作。

> [!definition] 定義：Repository
> Repository（repo）可以先理解成：一個由 Git 管理的 project folder，加上它的 version history。Git 在 repository 中維護 metadata／history（通常在隱藏的 `.git` directory），初學者不需要手動修改 `.git`。
> ```text
> student-utility-toolkit/
>     main.py
>     README.md
>     tests.md
> ```

> [!definition] 定義：Save、Commit、Push
> - **Save**：把 editor 中目前的檔案內容寫回本機檔案。Ctrl/Cmd+S 屬於這一層。
> - **Commit**：在 local Git history 建立一個有 message 的 checkpoint。
> - **Push**：把 local commits 傳到 remote repository，例如 GitHub。
>
> Edit + Save → Review + Commit → Push → Verify online。Ctrl/Cmd+S saves a file. Commit saves a version. Push shares that version.

這三個動作不能混為一談：可以 save 但還沒 commit；可以 commit 很多次但都還沒 push；push 之後才會讓 remote copy 更新。

Why GitHub belongs in the first class — programming is not only writing code; it is managing code：

| Save history | Share work | Build projects |
| --- | --- | --- |
| A repository records how your code changes over time. | Teachers, TAs, teammates, and future you can inspect the same project. | Every small exercise becomes part of a growing portfolio. |

Minimum Week 1 target: create a GitHub account, create one repository, and push your first Python file.

**GitHub Desktop 的 Week 1 workflow**（One local project, one remote repository. Do not create a second repository online）：

1. 建立／登入 GitHub account，完成 email verification。
2. GitHub Desktop 用瀏覽器授權登入，選擇 Q5 已經建立好的 local `student-utility-toolkit` repository；確認 `main.py` 能在這個位置執行。
3. 在 VS Code 編輯與執行 `main.py`，把 output 和記錄的 tests 比對。
4. 回到 Desktop 的 Changes，先看自己要 commit 的檔案與 diff。
5. 輸入有意義的 commit message，例如 `Add tested km converter`，commit to the current branch。
6. 第一次用 Publish repository 建立 remote（今天的練習 keep the repository private）；後續使用 Push origin。
7. View on GitHub：確認 code 與 latest commit 真的存在。
8. 再做一次小修改、save、test、commit、push、verify，確定自己真正走過完整循環。

Already created a README? Keep the README created locally in Desktop. Do not initialize another repository on GitHub.com.

**為什麼一定要 verify online？**「我有按 Push」不是 evidence。真正 evidence 是：

- GitHub 網頁看得到正確的 `main.py`。
- 看得到最新 commit。
- 第二次小修改也真的出現在 remote。
- 你保留了測試記錄。

Success = code visible online + latest change visible + tests recorded, not just a clicked button. 這和程式測試是一樣的思維：按了一個 button 不是結果；觀察到期望的 state 才是證據。

**Before publishing: inspect what leaves your computer.** A private repository is not a substitute for keeping secrets out of Git.

| Do not commit or upload | Today's reviewed project files |
| --- | --- |
| Passwords, API keys, tokens | `main.py` |
| Personal or confidential data | `README.md` with run instructions |
| Other students' answers | `tests.md` with expected/actual output |
| Unreviewed AI transcripts | A sanitized AI-use note |
| Large generated or unrelated files | Python `.gitignore` |

- Read the Changes／diff view before every commit.
- `.gitignore` 可以幫助排除某些「未被追蹤」的檔案，但它不是「已經 commit 的秘密資料自動消失」的工具。若 credential 已經進入 Git history，應把 credential revoke／rotate，並尋求適當的 repository-history remediation。
- Do not paste unknown terminal commands from AI without understanding their effects.

> [!example] Appendix：CLI alternative — do not mix workflows
> Only for students not using Desktop. Start from one local project and one empty remote. Before these commands: install Git, set your Git name/email, and configure GitHub authentication. Create an EMPTY remote repository: no README, license, or `.gitignore`.
> ```bash
> git init -b main
> git add main.py README.md .gitignore
> git commit -m "Add first tested Python program"
> git remote add origin <YOUR-REPOSITORY-URL>
> git push -u origin main
> ```
> Run inside the project folder; stage only files you created. Replace the URL placeholder. Use browser/credential-manager or SSH authentication, not an account password.

**Project seed：Student Utility Toolkit v0.1**（One working tool today; add capability only when we learn the concept）：

```python
km = float(input("Distance in km: "))
miles = km * 0.621371
print("Distance in miles:", miles)
```

| Deck | What the existing project gains |
| --- | --- |
| 2 | Clear data types, units, expressions, and formatting |
| 3–4 | Decisions, repeated input, and accumulated results |
| 5–6 | Text processing, functions, independent tests, and integration |

## D1 總結、詞彙表與 Exit Ticket

對應投影片：Deck 1｜53–55。

How can we make a computer solve a problem?

1. 把問題定義成 Input → Process → Output。
2. 建立 hardware／software execution model：storage、RAM、CPU 的角色不同。
3. 用 values 與 types 表示資訊，理解 operations 依 type 而變。
4. 把問題寫成 algorithm／pseudocode，再變成 Python source code。
5. 用 Python runtime 執行，閱讀 output 與 errors。
6. 用 independent expected results 進行 tests，debug 並 revise。
7. AI 可以協助 generate／explain／test ideas，但人必須控制 requirement 與 verification。
8. 用 Git 保存 version history，用 GitHub 分享 remote repository，並 verify remote state。

> [!note] 核心觀念
> Programming = turning problems into executable, verifiable, and shareable solutions.

| Term | 本課使用的意思 |
| --- | --- |
| Input | 提供給 program 的資料。 |
| Process | 對 input 做的計算、轉換或決策。 |
| Output | program 顯示、儲存或傳出的結果。 |
| CPU | 執行 machine instructions 的 processor。 |
| RAM／memory | 執行中 process 使用的主要 working memory。 |
| Storage | 持久保存程式與檔案的裝置，例如 SSD／HDD。 |
| Bit | 0 或 1 的 binary digit。 |
| Value | 程式處理的資料值，例如 `65`、`65.0`、`"65"`。 |
| Type | 決定 value 如何被 interpretation 以及支援哪些 operations 的分類。 |
| Algorithm | 解決問題的一系列明確步驟。 |
| Source code | 用 programming language 表達的程式文字。 |
| High-level language | 比 machine instructions 更接近人類問題描述的語言。 |
| Assembly | 與 processor instruction set 高度對應的低階 mnemonic representation。 |
| Machine language | CPU 真正解碼執行的 instruction encoding。 |
| Compiler | 把一種 program representation 轉成另一種 representation 的工具。 |
| Interpreter／runtime | 執行某種 program representation 的程式環境。 |
| Syntax | 程式語言的文法規則。 |
| Expression | evaluate 後得到 value 的程式片段。 |
| Statement | Python grammar 中可執行的完整敘述。 |
| Runtime error | 執行過程中某 operation 失敗。 |
| Logic error | 程式跑完但不符合 specification。 |
| Test case | specified input + independently justified expected result。 |
| Git | distributed version-control system。 |
| Repository | project files 與 Git history 的管理單位。 |
| Commit | local history 中的一個 checkpoint。 |
| Push | 把 local commits 傳到 remote repository。 |
| GitHub | hosting Git repositories 的網路服務。 |

> [!question] Exit Ticket：離開前應該能回答
> 1. Input／Process／Output 分別是什麼？
> 2. Storage、RAM、CPU 的角色有何不同？
> 3. 為什麼 `65`、`65.0`、`"65"` 不是同一份資料？
> 4. High-level language、assembly、machine language 的層次差在哪裡？
> 5. Syntax、expression、statement 怎麼區分？
> 6. Syntax error、runtime error、logic error 怎麼區分？
> 7. 為什麼 code 能執行並不代表 code 正確？
> 8. AI-generated code 為什麼只能先當 candidate solution？
> 9. Git 與 GitHub 有什麼不同？
> 10. Save、commit、push 又有什麼不同？

> [!tip] Claude 補充：Exit Ticket 的答案在哪
> 講義沒有附 Deck 1 的參考解答，答案都在上面各節：1 → [[#D1-Q1 什麼樣的問題可以交給電腦解]]；2 → [[#D1-Q2 電腦實際上在做什麼]]；3 → [[#D1-Q3 電腦如何表示資訊]]；4、5 → [[#D1-Q5 Python 如何執行我們的程式]]；6、7、8 → [[#D1-Q6 如果 AI 可以寫 code，為什麼還要學 Programming]]；9、10 → [[#D1-Q7 Git 與 GitHub 在程式設計中做什麼]]。

**After class：complete and verify your first push**（do not submit an untested code dump）：

1. Run the saved `main.py` again from your local repository folder.
2. Record at least two test inputs, expected outputs, actual outputs, and pass/fail.
3. Write a README: what the tool does, its input assumptions, and how to run it.
4. Commit and publish; make one small change, commit it, and push again.
5. Record how AI helped and what you changed or verified; remove private content.
6. Keep the repository URL; arrange teacher/TA access if the submission is private.

Bring one small real-world problem that could become your next program. Next class：How Can a Program Represent the Real World?
