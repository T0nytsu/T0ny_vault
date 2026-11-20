---
course: [PROG1]
semester: "115-1"
tags: [programming, lecture]
source:
  - "Functions_Complete_Classroom_104slides.pdf（W10 Functions 投影片，104 頁）"
created: 2026-11-18
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W10：Functions（函式）投影片 104 頁（封面署名 Guan-Ju Peng @ AM, NCHU），依投影片的單元 01–08 排列；每個單元把一般概念頁、淺藍統整頁、淺黃應用頁（實作單元、黑板數學填空）放在一起。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答（投影片的「動手練習」沒有附答案，答案都是 Claude 執行後寫的）；其餘內容都來自投影片。輸出一律收在 `[!solution]-` 裡：先預測，再展開。所有程式都用 Python 3.13 跑過。
> 心智圖：[[PROG1 Week 10 心智圖.excalidraw|PROG1 Week 10 心智圖]]
> 上一個：[[PROG1 Deck 5 整理]]

## W10：函式 Functions

對應投影片：W10｜1–2。

> [!abstract] 這一章要學什麼？
> 將已經寫過的程式整理成可以**重用、理解與檢查**的函式。先看 Function 如何包裝一項工作，接著理解參數、回傳值與不同作用域；本章從函式語法，逐步走到作用域、程式整合與遞迴，中間加入數學填空、函式分工及程式測試。
>
> 學會函式，不只要知道怎麼寫，也要能說明**資料如何進出函式**。

本章學習地圖：從一個函式，到可驗證的小程式。先讀概念與短例子，再做數學填空；接著把相同觀念用在行程紀錄程式。

| 01 理解函式 | 02 追蹤資料 | 03 組合程式 | 04 檢查結果 |
| --- | --- | --- | --- |
| 名稱、參數與回傳值 | 作用域與呼叫返回 | 驗證、格式化與主流程 | 手算、邊界與整合測試 |

本章的三種頁面：

| 頁面 | 怎麼讀 |
| --- | --- |
| 一般概念頁 | 先讀左側範例（老師的原投影片），再用右側中文導讀確認理解。 |
| 淺藍統整頁 | 整理剛學過的規則，辨認容易混淆的觀念。 |
| 淺黃應用頁 | 看程式如何拆解；填空、預測輸出，再核對解答。 |

應用頁的程式分成三種：「可獨立執行」的可以直接跑；標為「片段」的要和指定的函式一起執行；完整程式見課程練習包。

> [!tip] Claude 補充：這份投影片接在 Deck 5 後面
> Deck 5 最後預告下一份是「How do we organize a growing program into understandable components?（functions, parameters, return values, interfaces, and AI-assisted integration）」。這份投影片的貫穿案例就是 Deck 4–5 的行程紀錄程式（`Campus East,12.5,45`），只是把 [[PROG1 Deck 5 整理#D5-Q6 如何讓 AI 修改介面而不偷改規則|D5-Q6]] 的 `trip_text.py` 拆成一個個函式。投影片本身說「不需要預先看過其他教材」，所以沒讀 Deck 5 也看得懂。
>
> T0ny 把這份投影片標為 W10；[[PROG1 Index]] 的課程進度表 W10 目前寫的是 Class & Object。

## W10-01 Function 的基本觀念

對應投影片：W10｜3–12。

**甚麼是 Function？** 可以想成一種特殊的 operator，用以執行一些較複雜的運算。Function 把具有特定目的的工作**命名**，方便在不同地方再次使用。

**Why Functions?**

- Reuse Code
    - Easy updating and testing
    - Only need to test and update the function, rather than every place that we use it.
- Easy Understanding

重複的工作若分散在各處，修改時容易漏掉；抽成函式後，修改與檢查的範圍會更明確。不是所有工作都必須拆函式，重點是**責任是否清楚**：函式也能因責任清楚而值得獨立，不一定要被呼叫很多次。Function 的價值在於重用與可理解性，不只是減少程式行數。

**把 Function 想成運算單位。** 如果把 Function 考慮成 Operators，那麼它應該要有運算元、值、運算方法，還有「名稱」。以內建的型別轉換 `int(X)` 為例：

| Operator 的要素 | 對應到 Function | `int(X)` |
| --- | --- | --- |
| 運算元 | 呼叫函式時提供的資料 | 1 個運算元 X |
| 運算方法 | 函式本體 | 將 X 值轉換為整數 |
| 值 | 呼叫產生的結果 | X 相對應的整數值 |
| 名稱 | 用來呼叫 | `int` |

函式是有名稱的工作單位，但不能假設每個函式都會回傳可計算的值：函式可以產生回傳值，也可能只執行顯示等動作。之後要特別區分 **return** 和 **print**。

> [!example] 範例：Built-in Function `print()`（先分清楚「顯示的文字」與「呼叫產生的值」）
> ```python
> x = print(3)
> print(x)
> ```

> [!solution]- 輸出
> ```text
> 3
> None
> ```
> `print(X)` 取得 X，將它寫入輸出；螢幕上有文字，並不等於呼叫結果是那段文字。`x = print(3)` 會顯示 3，但 x 是 `None`：**print 的回傳值是 None**。顯示文字與回傳資料是兩種不同效果。
> 投影片導讀更正：前述範例（老師原投影片）寫的「null」應修正為 Python 使用的 `None`。

> [!warning] Claude 提醒：期中考古題的「print 裡的 print」就是這條規則
> [[PROG1 Midterm 考古題#A2 print 裡的 print（5 分）|A2]] 與 [[PROG1 Midterm 考古題#B2 print 裡的 print（5 分）|B2]]：內層 `print` 先印出內容並回傳 `None`，外層 `print` 再把 `None` 印出來。期末考的函式題很可能再考「看得到輸出 ≠ 有回傳值」。

**內建函式 `int()`**：Built-in Functions 是內建於 Python 內的常用 Functions。把 `int(X)` 視為「傳入資料、產生轉型結果」的例子：傳入可以轉換的數值或文字，呼叫者取得一個整數結果，再決定如何使用。`int("3")` 得到 3，但不是任何文字都能成功轉成整數（例如 [[PROG1 Deck 2 整理#D2-Q4 輸入與轉型如何運作|D2-Q4]] 的 `int("12.5")` → `ValueError`）。比較 `int()` 與 `print()` 的回傳值：相同的函式呼叫語法，可能代表**計算結果**或**顯示效果**。

> [!example] 範例：標準函式庫 `math.floor()`（math.floor 位於 math 模組；先 import math，再呼叫）
> ```python
> import math
>
> print(math.floor(2.7))   # 2
> print(math.floor(-2.7))  # -3
> ```

> [!solution]- 輸出
> ```text
> 2
> -3
> ```
> `math.floor(x)` 取得**不大於 x 的最大整數**（向下取整）；`math.ceil(x)` 才是向上取整的 ceiling，例如 floor(2.7) = 2、ceil(2.7) = 3。利用數學內建函式說明：名稱與實際操作要一致。
> 投影片導讀更正：前述範例將 floor 說成 ceiling，且名稱寫成 int。floor 是向下取整；不能只依例子的名稱判斷它做了什麼。

> [!tip] Claude 補充：floor、ceil 與 int 對負數不一樣
> Claude 執行 `print(math.ceil(2.7), math.ceil(-2.7), int(-2.7))` 得到 `3 -2 -2`。`int()` 是**向零截斷**，所以 `int(-2.7)` 是 −2，`math.floor(-2.7)` 卻是 −3。同一個規則在 [[PROG1 Deck 2 整理#D2 選讀：容易混淆的精確規則|D2 選讀]] 出現過。

**重複利用是第一個理由**：相同工作若寫在多個地方，會增加修改與維護負擔。先辨識真正重複的運算，再讓不同的輸入共用同一套處理步驟。由重複程式思考共同規則，再進入自訂 Function（下一節用階乘示範）。

> [!note] 單元 01 統整：Function 是有名稱、可重用的工作
> 從 `print()`、`int()`、`math.floor()` 出發，先觀察函式如何接受資料、完成工作，再思考為什麼需要將工作命名。名稱／Input → 執行工作 → 回傳值或效果。
> - **函式的角色**：每個函式都負責一項明確的工作；不只為了少寫幾行程式。
> - **不同的結果**：`print()` 主要產生輸出效果；`int()` 會交回可使用的整數。
> - **讀懂介面**：閱讀函式時，先問它接收什麼、會做什麼、交回什麼。

> [!question] 想一想
> 觀察 `print(3)` 和 `int("3")`，它們都能呼叫，但交回的結果相同嗎？

> [!solution]- 答案（Claude）
> 不同。`print(3)` 在螢幕上顯示 3，交回 `None`；`int("3")` 不顯示任何東西，交回整數 3。只有後者能接著做 `+ 1`。

### 貫穿案例：行程紀錄與統計小程式

這只是本章用來練習函式分工的例子；不需要預先看過其他教材。依序輸入四行（名稱、公里、分鐘）：

```text
Campus East,12.5,45
Broken,1
Station,3.5,30
DONE
```

一筆資料的意思：`Campus East` 是路線名稱，12.5 是公里，45 是分鐘。`Broken,1` 少一個欄位，不能列入統計。

程式要完成什麼？辨識結束、檢查資料、計算速度，再產生報告與有效資料的統計。手算最後結果：有效 **2 筆**，共 **16 公里、75 分鐘**；整體速度 16 ÷ (75 ÷ 60) = **12.80**。

本章要練習的能力不是背誦專題名稱，而是**決定每個函式應負責哪項工作**。同一個問題逐步展開：先學會小函式，再完成整體分工。

### 實作單元 01：函式與工作分解

**一支程式，原來同時做了很多事。** 先觀察一筆「有效行程」的簡化程式，再辨認哪些工作值得獨立成函式。

> [!example] 範例：教學縮小版：單筆有效資料（不是完整輸入驗證器）
> ```python
> raw = "Campus,3.5,30"
> label, km_text, min_text = raw.split(",")
> km = float(km_text)
> minutes = int(min_text)
> speed = km / (minutes / 60)
> if minutes <= 30:
>     band = "Short"
> elif minutes <= 60:
>     band = "Medium"
> else:
>     band = "Long"
> print(f"{label}: {speed:.2f} km/h")
> print(f"Trip band: {band}")
> ```

> [!solution]- 輸出
> ```text
> Campus: 7.00 km/h
> Trip band: Short
> ```
> 閱讀重點：1. 解析資料：`split()`、`float()`、`int()`。2. 計算規則：公里 ÷ 小時。3. 分類規則：30／60 分鐘的邊界。4. 顯示結果：印成可閱讀的報告。

> [!question] 動手練習
> 圈出哪幾行負責「讀取／解析」、「計算」、「分類」、「輸出」。若只想測試 30 分鐘分類，為什麼不該每次都執行整支程式？

> [!solution]- 答案（Claude）
> 第 1–4 行讀取／解析（`raw`、`split`、`float`、`int`）；第 5 行計算速度；第 6–11 行分類；最後兩行輸出。分類規則混在整支程式裡，想測 30 分鐘就得改 `raw`、跑完解析與計算、再用眼睛讀報告；把分類獨立成函式後，直接呼叫 `duration_band(30)` 就能檢查它交回的值（下一個範例）。

**把「分類規則」獨立成 `duration_band()`。** Function 的價值不只是減少重複，更是讓單一規則可以直接被檢查。

> [!example] 範例：可獨立執行：單一工作、輸入明確、直接回傳結果
> ```python
> def duration_band(duration_min):
>     if duration_min <= 30:
>         return "Short"
>     if duration_min <= 60:
>         return "Medium"
>     return "Long"
>
> print(duration_band(1))
> print(duration_band(30))
> print(duration_band(31))
> print(duration_band(61))
> ```

> [!solution]- 輸出
> ```text
> Short
> Short
> Medium
> Long
> ```
> 閱讀重點：1. 函式只需要 minutes，不需要 `input()`。2. 回傳的是字串，不是直接 print。3. 可直接測試分類的臨界值。

> [!question] 動手練習
> 先預測 `duration_band(60)` 的結果，再測試 29、30、31、60、61；說明第二個 `if` 為何不必使用 `elif`。

> [!solution]- 答案（Claude 執行）
> ```text
> 60 Medium
> 29 Short
> 30 Short
> 31 Medium
> 60 Medium
> 61 Long
> ```
> 第一個 `if` 成立時，`return "Short"` 已經結束整個函式，不會再往下執行；能走到第二個 `if` 的一定是 `duration_min > 30`，效果和 `elif` 相同。

## W10-02 自訂函式與重複利用

對應投影片：W10｜13–25。

**從重複階乘找出共同步驟。** Reuse Code，考慮下面的例子（左邊是原本的寫法，右邊把差異改成 x，黃色標出兩段完全相同的程式）：

> [!example] 範例：compute 3! 與 5!
> 原本：
> ```python
> # compute 3!
> res = 1
> for i in range(1, 4):
>     res *= i
> print(res)
>
> # compute 5!
> res = 1
> for i in range(1, 6):
>     res *= i
> print(res)
> ```
> 把不同的部分改成 x：
> ```python
> # compute 3!
> x = 3
> res = 1
> for i in range(1, x+1):
>     res *= i
> print(res)
>
> # compute 5!
> x = 5
> res = 1
> for i in range(1, x+1):
>     res *= i
> print(res)
> ```

> [!solution]- 輸出（兩個版本相同）
> ```text
> 6
> 120
> ```
> 共同部分是初始化 res、執行 for 迴圈與累乘；差異只在輸入的 n 與迴圈終點。下一步會把不同的 n 改由參數傳入。抽取函式前，先把**不變的演算法**與**變動的輸入**分開。導讀也提醒：乘法變數要用小寫 `i`，Python 大小寫有別。

**如何定義自訂函式？** 自訂函式：輸入 → 運算 → 回傳。`def` 建立函式；**呼叫才執行函式本體**。

> [!example] 範例：def、參數、縮排的函式本體與 return
> ```python
> def f(x, y):
>     z = x + y
>     return z
>
> print(f(3, 5))  # 8
> ```

> [!solution]- 輸出
> ```text
> 8
> ```
> `def F(X, Y):` 建立有名稱的函式；呼叫後執行縮排的 Blocks，最後可透過 `return` 交回結果。參數是函式內接收資料的名稱。`return` 後沒有資料，或執行至結尾未回傳時，結果是 `None`（不是 null）。def 定義工作；真正的運算發生在函式被呼叫時。

> [!failure] 辨識示例：階乘算對，介面卻不對
> 這裡故意保留 print 與 return 的差別，請預測結果。
> ```python
> def fac(x):
>     res = 1
>     for i in range(1, x + 1):
>         res *= i
>     print(res)
>
> print(fac(3))  # 先印 6，再印 None
> ```

> [!solution]- 輸出與分析
> ```text
> 6
> None
> ```
> `fac(x)` 依輸入值 x 執行相同的累乘過程，但函式內只 `print(res)`，沒有 return，所以外層 `print(fac(3))` 還會顯示 `None`。要讓外部取得階乘值、讓結果繼續參與運算，把 `print(res)` 改成 `return res`。「看到 6」與「得到可再計算的 6」不同：要重複使用計算結果，通常應由函式回傳，而不是只印在螢幕上。

**函式可以組合其他函式**：也可以在別的 function 之中呼叫別的 function。

> [!example] 範例：兩數中取大 → 三數中取大
> ```python
> def max(a, b):
>     if a > b:
>         return a
>     else:
>         return b
> # 三數中取大
> # 可重複使用之前的 fun
> def max3(a, b, c):
>     return max(max(a, b), c)
> ```

> [!solution]- Claude 執行：加上一次呼叫
> ```python
> print(max3(3, 9, 5))
> ```
> ```text
> 9
> ```
> 先計算 `max(a, b)`，再將第一個結果與 c 比較，得到三個數中的最大值。內層函式先回傳，外層才能完成：函式的結果可以成為另一個函式的輸入。

> [!warning] Claude 提醒：自己定義 `max` 會遮蔽內建的 `max`
> 導讀指出本例重新定義 `max`，會遮蔽同名的 Python 內建 max。Claude 在同一個檔案接著執行 `print(max(3, 4, 5))`，得到 `TypeError: max() takes 2 positional arguments but 3 were given`：之後呼叫的都是兩個參數的自訂版本。自己的函式不要取 `max`、`sum`、`input`、`list` 這類內建名稱（[[PROG1 Deck 2 整理#D2-Q3 變數名稱如何指向資料|D2-Q3]] 也提醒過不要拿 `input`、`float`、`str` 當變數名）。

**不固定數量的引數 `*args`。**

> [!example] 範例：不定數量的引數 `*values`（`maximum(3, 5, 5)` → 5；`maximum(3, 4, 5, 6, 9)` → 9）
> ```python
> def maximum(*values):
>     result = values[0]
>     for value in values[1:]:
>         if value > result:
>             result = value
>     return result
>
> print(maximum(3, 5, 5))
> print(maximum(3, 4, 5, 6, 9))
> ```

> [!solution]- 輸出
> ```text
> 5
> 9
> ```
> `def max(*a)` 將多個位置引數收成 **tuple**，再利用迴圈逐個比較，更新暫存的最大值。`a[0]` 代表第一個元素，`a[1:]` 代表其餘元素；`values[0]` 是第一個**值**，不是個數。本範例至少需要一個值；若完全沒有輸入，`a[0]` 會出錯。`*args` 讓輸入數量有彈性，但函式仍需說清楚有效輸入條件。

> [!note] 單元 02 統整：同一算法可以處理不同輸入
> 階乘程式、`max3()` 與 `*args`，連起來就是一條從重複程式到函式組合的路。找共同流程 → 定義與呼叫 → 組合與重用。
> - **抽取共同演算法**：將計算 3!、5! 中共用的流程寫成 `fac(x)`，改由參數決定輸入。
> - **函式可以組合**：`max3()` 先呼叫 `max(a, b)`，再把結果與 c 比較。
> - **引數數量可以變**：`*args` 將多個位置引數收為 tuple，但仍需注意至少提供一個有效值。

> [!question] 想一想
> 只把 `print(res)` 放進 `fac()`，外層為何可能取得 None？

> [!solution]- 答案（Claude）
> 函式本體裡沒有 `return`，執行到結尾就自動回傳 `None`。`print(res)` 只把 6 顯示在螢幕上，沒有把 6 交給呼叫者。

### 數學填空 1：平方

> [!question] 數學填空 1｜平方：顯示答案，還是交回答案？
> 數學目標 f(x) = x²；使用函式的結果計算 f(3) + 1。請只填空白；不要先執行程式。
> ```python
> def square(x):
>     ____________________ # ①
>
> y = square(3)
> print(y + 1)
> ```
> 已知條件：x 是整數。`square(x)` 應回傳一個可計算的數字。
> 先寫在黑板上：① 要填什麼？最後會印出：＿＿＿＿。
> 想一想：若①改成 `print(x * x)`，y 到底接到了什麼？
> 學生任務：圈出「把值交回去」的一行，並說明 y 的值從哪裡來。

> [!solution]- 參考解答 1｜用 return 交回平方值
> 填空答案：① `return x * x`
> ```python
> def square(x):
>     return x * x
>
> y = square(3)
> print(y + 1)
> ```
> ```text
> 10
> ```
> 手算追蹤：沿著資料的流向追蹤一次呼叫，每個箭頭都要問：交出去的是哪個值？誰接住這個值？
>
> | 01 提供引數 | 02 計算並回傳 | 03 接收結果 | 04 繼續計算 |
> | --- | --- | --- | --- |
> | `square(3)`：把 3 交給 x。 | x * x = 9；return 9。 | 呼叫運算式的值是 9；y = 9。 | y + 1 = 10；print 顯示 10。 |
>
> 數學上的函數值與程式中的回傳值：我們要的是 f(3) = 9，讓外面的程式繼續用這個 9。顯示在螢幕上的文字，不會自動變成指定給 y 的資料。函式呼叫可以放進運算式，是因為它有回傳結果。
> 檢查你的理解：`square(4) + square(2)` = 20，兩次呼叫各自回傳數值，再相加（Claude 執行確認：20）。**print 給人看；return 把資料交給呼叫者繼續使用。**

> [!failure] 常見錯誤：印出了 9，為什麼還不能加 1？
> 以下是故意出錯的版本。先判斷錯誤發生在哪一行。
> ```python
> def square(x):
>     print(x * x)
>
> y = square(3)
> print(y + 1)
> ```

> [!solution]- 預期輸出與分析
> ```text
> 9
> TypeError: unsupported operand type(s) for +: 'NoneType' and 'int'
> ```
> （Claude 執行；traceback 前幾行省略，投影片只寫 `TypeError`。）第一行 9 是函式內 print 的效果。函式沒有 return 數字，所以 **y 是 None**；最後一行試圖計算 `None + 1`。看到正確輸出，不等於函式回傳了正確資料。

### 實作單元 02：重用與函式組合

**把重複的速度公式寫成 `average_speed()`**：同一個計算規則，只需要一個函式；不同資料透過參數傳入。

> [!example] 範例：重複公式 → 一個可重用的數值函式
> ```python
> # 原本：相同公式寫了兩次
> s1 = 3.5 / (30 / 60)
> s2 = 5.0 / (45 / 60)
>
> def average_speed(distance_km, duration_min):
>     duration_h = duration_min / 60
>     return distance_km / duration_h
>
> print(average_speed(3.5, 30))
> print(average_speed(5.0, 45))
> ```

> [!solution]- 輸出
> ```text
> 7.0
> 6.666666666666667
> ```
> 閱讀重點：1. 改變資料時不必再複製公式。2. 函式回傳未捨入的數字。3. 輸入時間是分鐘；計算時須轉小時。**計算與顯示分開：return 完整數字，報告時才格式化。**

> [!question] 動手練習
> 把時間改成 60 分鐘，先手算 `average_speed(3.5, 60)`；如果把 60 分鐘當成 60 小時計算會有什麼錯？

> [!solution]- 答案（Claude 執行）
> 60 分鐘 = 1 小時，所以 `average_speed(3.5, 60)` = 3.5 ÷ 1 = `3.5`。若忘了除以 60、把 60 當成 60 小時，會算出 3.5 ÷ 60 = `0.058333333333333334`，小了 60 倍；程式不會報錯，是 logic error。

**一個 Function 可以組合其他 Functions。** `format_trip()` 不重新計算速度或分類，而是呼叫已經存在的 helper。

> [!example] 片段：先定義 `duration_band()` 與 `average_speed()`（需先定義輔助函式）
> ```python
> MILES_PER_KM = 0.621371
>
> def format_trip(label, km, minutes):
>     miles = km * MILES_PER_KM
>     speed = average_speed(km, minutes)
>     band = duration_band(minutes)
>     return (
>         f"Route: {label}\n"
>         f"Distance: {miles:.2f} miles\n"
>         f"Average speed: {speed:.2f} km/h\n"
>         f"Trip band: {band}"
>     )
>
> print(format_trip("Campus", 3.5, 30))
> ```

> [!solution]- 輸出
> ```text
> Route: Campus
> Distance: 2.17 miles
> Average speed: 7.00 km/h
> Trip band: Short
> ```
> 資料／控制流程：`format_trip()` → `average_speed()`；`format_trip()` → `duration_band()`；回傳整份文字 → `print()`。每個函式負責一件事；較大的函式負責組合結果。

> [!question] 動手練習
> 若把 minutes 改成 45，哪兩個計算結果會改變？哪一個 helper 決定 Short／Medium？

> [!solution]- 答案（Claude 執行）
> ```text
> Route: Campus
> Distance: 2.17 miles
> Average speed: 4.67 km/h
> Trip band: Medium
> ```
> 速度（7.00 → 4.67 km/h）和分類（Short → Medium）會改變；英里只跟 km 有關，不變。Short／Medium 由 `duration_band()` 決定。

**當引數數量不固定：`*args`**：延續 `max()` 的例子；`*values` 將不固定數量的引數收集成 tuple。投影片這頁的程式和輸出與上一節的 `maximum(*values)` 範例相同（獨立練習：可變數量引數，至少提供一個值）。閱讀重點：1. `*values` 將傳入的多個值組成 tuple。2. `values[0]` 是第一個元素，不是個數。3. 若不傳入任何值，會違反本例的前提。

> [!question] 動手練習
> 預測 `maximum(-2, -5, -1)`；若呼叫 `maximum()`，哪一行會出錯？如何在函式開始就明確拒絕空輸入？

> [!solution]- 答案（Claude 執行）
> `maximum(-2, -5, -1)` → `-1`。`maximum()` 在 `result = values[0]` 出錯：`IndexError: tuple index out of range`（空 tuple 沒有第 0 個元素）。在函式開頭先檢查：
> ```python
> def maximum(*values):
>     if len(values) == 0:
>         raise ValueError("maximum() needs at least one value")
>     result = values[0]
>     for value in values[1:]:
>         if value > result:
>             result = value
>     return result
>
> try:
>     maximum()
> except ValueError as error:
>     print(error)
> ```
> ```text
> maximum() needs at least one value
> ```
> `raise ValueError` 的用法在 [[#實作單元 07：多函式整合與測試]]。

## W10-03 參數、回傳與常見呼叫錯誤

對應投影片：W10｜26–37。

**最基本的 def 與 return**：用 f(x) = x² 的小例子，建立函式呼叫的基本流程。

> [!example] 範例：基本的自定義 Functions 型式
> ```python
> def f(x):
>     x=x*x
>     return x
> ```
> 此例中：運算元：(X)；運算方法：執行 Blocks 內的程式（x = x*x）；值：x。呼叫 f 的例子：`f(3)` 的值為 9。

> [!solution]- Claude 執行：`print(f(3))` 與 `y = f(3)`
> ```text
> 9
> 9
> ```
> 呼叫 `f(3)` 後，局部 x 先取得 3；`x = x*x` 得到 9，再由 return 交回呼叫者。回傳後，函式的這次執行結束。可以把結果存成 `y = f(3)`，而不是只能 print。函式執行的基本單位是「**輸入 → 處理 → 回傳**」。

**預設參數如何運作？** default argument 可以讓呼叫者省略部分引數。

> [!example] 範例：有標準初始值的自定義 Function
> ```python
> def f(x,y = 10):
>     x=x*y
>     return x
> ```
> 此例中：`y = 10` 將 y 的標準初始值設定為 10；若沒有傳入 y，y 的值為 10；若有傳入 y，則 y 的值設為傳入值。呼叫 f 的例子：`f(3)` 的值為 30；`f(3,7)` 的值為 21。

> [!solution]- Claude 執行：`print(f(3))`、`print(f(3, 7))`
> ```text
> 30
> 21
> ```
> `f(3)` 沒有給 y，因此使用預設值 y = 10；`f(3,7)` 提供 y = 7，改用呼叫者給的值。參數的預設值與呼叫時提供的值有不同的來源。**預設值是函式介面的一部分**，不能在重構時任意改掉。

**必要引數不能省略**：分辨有預設值的 y 與沒有預設值的 x、z。

> [!example] 範例：必須的傳入參數
> ```python
> def f(x, z ,y = 10):
>     x=x*y
>     return x
> ```
> 此例中：
> - 若沒有傳入 y，y 的值為 10 → 依舊可以執行！
> - 若沒有傳入 z，z 雖然沒有被用到但也沒有初始值 → 會出現錯誤！
> - 若沒有傳入 x，x 有被用到又沒有標準初始值 → 會出現錯誤！

> [!solution]- Claude 執行：`f(3, 0)`、`f(3)`、`f()`
> ```text
> 30
> TypeError: f() missing 1 required positional argument: 'z'
> TypeError: f() missing 2 required positional arguments: 'x' and 'z'
> ```
> `f(x, z, y=10)` 的 x 和 z 都必須由呼叫者提供；即使 z 暫時沒有用在運算中，呼叫時仍必須提供。省略必要參數會出現 `TypeError`。**輸入介面取決於函式簽名**，不取決於程式是否真的使用到每個變數。必要參數是呼叫時必須滿足的約定。

**函式定義與呼叫的錯誤**（常見的錯誤）：

> [!example] 範例：參數順序錯誤
> ```python
> def f(x, y = 10,z):
>     x=x*y
>     return x
> ```
> 此例中：有初始值的變數要放再沒有初始值的變數之後否則會出現錯誤。

> [!solution]- Claude 執行
> ```text
> SyntaxError: parameter without a default follows parameter with a default
> ```
> 一般位置參數中，無預設值的參數不能排在有預設值參數之後；`def f(x,y=10,z):` 造成 `SyntaxError`。

> [!example] 範例：Function 必須先定義才能夠呼叫
> ```python
> f(3)
> def f(x):
>     return x
> ```
> 此例中：出現錯誤，因為 `f(3)` 呼叫時 f 沒有定義。

> [!solution]- Claude 執行
> ```text
> NameError: name 'f' is not defined
> ```
> 呼叫執行時，函式名稱必須已被定義並綁定；在定義前執行 `f(3)`，通常會發生 `NameError`。請分清楚**定義時的語法錯誤**與**呼叫時的名稱錯誤**。

> [!tip] Claude 補充：SyntaxError 一行都不會跑，NameError 跑到那一行才停
> [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式|D1-Q5]]：有 syntax error 時整個 script 不會開始；`def f(x, y = 10, z)` 就算寫在檔案最後面，前面的 print 也不會印。`NameError` 是 runtime error，前面的程式會正常執行，直到 `f(3)` 那一行才失敗。

> [!note] 單元 03 統整：函式簽名決定如何呼叫
> 從 `f(x)` 到 `f(x, y=10)`，認識必要引數、預設值，以及呼叫時會發生的錯誤。def 介面 → 提供 argument → 取得 return。
> - **必要與預設參數**：有預設值的參數可以省略；沒有預設值的參數仍需提供。
> - **語法與執行不同**：`def f(x,y=10,z)` 是語法錯誤；尚未定義就呼叫是名稱問題。
> - **介面應穩定**：改變參數名稱、順序或預設值，可能改變原本的呼叫方式。

> [!question] 想一想
> `f(x, z, y=10)` 中，z 即使沒有用到，呼叫時可以省略嗎？

> [!solution]- 答案（Claude 執行）
> 不行。`f(3)` → `TypeError: f() missing 1 required positional argument: 'z'`。Python 只看簽名，不看函式本體有沒有用到 z。

### 數學填空 2：絕對值

> [!question] 數學填空 2｜絕對值：每一條路徑都有回傳嗎？
> 數學目標：x < 0 時回傳 −x；x ≥ 0 時回傳 x。不要使用 `abs()`。請只填空白；不要先執行程式。
> ```python
> def abs_value(x):
>     if x < 0:
>         return ________ # ①
>     __________________ # ②
>
> print(abs_value(-3))
> print(abs_value(0))
> print(abs_value(3))
> ```
> 已知條件：x 是整數。負數、零、正數都應有數值結果。
> 請預測三行輸出：−3 → ＿＿＿＿；0 → ＿＿＿＿；3 → ＿＿＿＿。
> 想一想：若刪掉②，零與正數會自動回傳 x 嗎？
> 學生任務：先分成負數、零、正數三種情況，再填①與②。

> [!solution]- 參考解答 2｜讓負數、零、正數都有答案
> 填空答案：① `-x`　② `return x`
> ```python
> def abs_value(x):
>     if x < 0:
>         return -x
>     return x
>
> print(abs_value(-3))
> print(abs_value(0))
> print(abs_value(3))
> ```
> ```text
> 3
> 0
> 3
> ```
> 手算追蹤：把分段定義對應到執行路徑。不要只用一個負數測試；零與正數走的是另一條路徑。
>
> | 輸入 x | x < 0？ | 執行的 return | 結果 |
> | --- | --- | --- | --- |
> | -3 | True | `return -x` | 3 |
> | 0 | False | `return x` | 0 |
> | 3 | False | `return x` | 3 |
>
> 為什麼第二個 return 不一定需要 else？負數已在第一個 return 結束；能繼續往下的，就是零或正數。把每條可能的路徑走一次，才能檢查是否漏了結果。最小測試集合：本題至少檢查**負數、零、正數**。先看數學上的分類，再檢查程式的每條回傳路徑。

> [!failure] 常見錯誤：負數正確，零與正數卻得到 None
> 以下函式只有一條回傳路徑；觀察沒有進入 if 時會發生什麼。
> ```python
> def abs_value(x):
>     if x < 0:
>         return -x
>
> print(abs_value(-3))
> print(abs_value(0))
> print(abs_value(3))
> ```

> [!solution]- 預期輸出與分析
> ```text
> 3
> None
> None
> ```
> 不是自動回傳 x：零與正數跳過 if，然後走到函式結尾；沒有明確回傳值時，結果就是 `None`。單一輸入成功，不代表其他分支也符合函式承諾。

### 實作單元 03：參數、回傳與介面

**Parameter、Argument 與 Default Value**：先分清楚定義時的名稱、呼叫時的值，以及可省略的預設引數。

> [!example] 範例：兩種呼叫方式與一個預設值
> ```python
> def minutes_to_hours(minutes):
>     return minutes / 60
>
> def label_with_prefix(label, prefix="Route"):
>     return f"{prefix}: {label}"
>
> print(minutes_to_hours(45))
> print(minutes_to_hours(minutes=30))
> print(label_with_prefix("Campus"))
> print(label_with_prefix("Campus", prefix="Trip"))
> ```

> [!solution]- 輸出
> ```text
> 0.75
> 0.5
> Route: Campus
> Trip: Campus
> ```
> 閱讀重點：1. `minutes` 是 **parameter**；45 是 **argument**。2. `minutes=30` 是 **keyword argument**。3. `prefix` 有預設值；`label` 仍是必填。

| 名詞 | 在哪裡 | 例子 |
| --- | --- | --- |
| parameter（參數） | 定義時，函式內接收資料的名稱 | `def minutes_to_hours(minutes):` 的 `minutes` |
| argument（引數） | 呼叫時提供的值 | `minutes_to_hours(45)` 的 45 |
| keyword argument | 呼叫時用名稱指定 | `minutes_to_hours(minutes=30)` |
| default value | 定義時給的預設值，可省略 | `prefix="Route"` |

> [!question] 動手練習
> 預測 `label_with_prefix("Station", "Stop")`；若省略 `minutes_to_hours()` 的必要引數，會出現哪種錯誤？

> [!solution]- 答案（Claude 執行）
> ```text
> Stop: Station
> TypeError: minutes_to_hours() missing 1 required positional argument: 'minutes'
> ```
> 第二個位置引數 `"Stop"` 依位置對到 `prefix`，取代預設的 `"Route"`。

**看得到輸出，不代表函式有回傳值**：`print()` 只把文字顯示出來；`return` 才能把資料交給呼叫者繼續計算。

> [!example] 範例：可獨立執行：相同計算、不同介面
> ```python
> def show_hours(minutes):
>     print(minutes / 60)
>
> def hours(minutes):
>     return minutes / 60
>
> x = show_hours(30)
> y = hours(30)
> print("x =", x)
> print("y =", y)
> ```

> [!solution]- 輸出
> ```text
> 0.5
> x = None
> y = 0.5
> ```
> 閱讀重點：1. `show_hours()` 印出 0.5，卻回傳 None。2. `hours()` 回傳 0.5，由呼叫者決定用途。3. 因此函式的測試不能只看螢幕。螢幕上的結果與函式真正回傳的值，是兩件不同的事。

> [!question] 動手練習
> 把 `show_hours()` 改成能回傳數字的函式；再嘗試 `x * 2`，修正前後會有什麼差別？

> [!solution]- 答案（Claude 執行）
> 修正前 `x` 是 None：先印出 0.5，再 `TypeError: unsupported operand type(s) for *: 'NoneType' and 'int'`。把 `print(minutes / 60)` 改成 `return minutes / 60` 後，`print(x * 2)` 印出 `1.0`。

**Function Contract：先講清楚函式的承諾**：不只要算對，還要決定輸入單位、合法範圍與輸出型態。

> [!example] 範例：有效資料才交給計算 helper；不要提早捨入
> ```python
> def average_speed(distance_km, duration_min):
>     # 前提：km 有限且 >= 0；minutes > 0
>     return distance_km / (duration_min / 60)
>
> speed = average_speed(5, 45)
> print(f"Display: {speed:.2f}")
> print(f"Twice: {2 * speed:.2f}")
> ```

> [!solution]- 輸出
> ```text
> Display: 6.67
> Twice: 13.33
> ```
> 閱讀重點：1. 輸入：距離 km、時間 minutes。2. 前提：非負且有限距離、正分鐘。3. 輸出：未捨入的數值 km/h。4. 驗證責任：由 parser 先拒絕非法資料。**Contract 是函式對呼叫者的承諾，不只是參數名稱。**

> [!question] 動手練習
> 請解釋為何 Twice 顯示 13.33 而不是 13.34；如果 `duration_min=0`，這個 helper 的前提被怎樣違反？

> [!solution]- 答案（Claude 執行）
> `speed` 存的是未捨入的 6.666666666666667，`2 * speed` 是 13.333333333333334，格式化成 13.33。如果先捨入成 6.67 再乘 2，才會得到 13.34：提早捨入的誤差被放大了。`duration_min=0` 違反「minutes > 0」的前提，執行會得到 `ZeroDivisionError: float division by zero`；照契約，這種資料應該在 parser 就被拒絕，不該交給 helper。

## W10-04 Docstring 與函式說明

對應投影片：W10｜38–44。

**如何使用 Docstring？** Docstring 是函式的第一個字串敘述：讓使用者知道函式做什麼，而不是逐行翻譯實作。它讓函式具備可由 `help()` 查閱的說明文字。

> [!example] 範例：Docstring
> ```python
> def f(x):
>     """Return the square of x."""
>     return x * x
>
> help(f)
> ```

> [!solution]- 輸出（Claude 執行）
> ```text
> Help on function f in module __main__:
>
> f(x)
>     Return the square of x.
>
> ```
> 將描述函式的字串放在函式本體最前面，`help(f)` 就能顯示函式的文件資訊。概念釐清：不要求位於第一個實體文字行；重點是**函式本體的第一個敘述**。Python 可使用三個單引號或三個雙引號包住多行 docstring。好的說明應描述函式做什麼與回傳什麼。Docstring 是函式給使用者看的介面說明。

**甚麼是好的註解？～一些原則**

- Describes what a function does.
- Does not describe how a function works.
- Makes the purpose of every parameter clear and refers to the parameter by name.
- Be clear if a function returns a value, and if so, what.
- Make sure to explicitly state any assumptions the function has.
- Be concise and grammatically correct.
- Use commands rather than descriptions.

區分函式的用途與函式內每一行的實作細節：說明參數代表什麼、有哪些前提；說明回傳結果的含義與使用者應注意的限制。避免只是把程式碼逐行翻譯成文字；寫給呼叫函式的人閱讀，讓他不用先理解完整實作。說明重點是 **what 與 contract**，不是逐行描述 how。

**差的註解**

- ''A sunset module Changes into a sunset.''
- These are terrible docstrings.
    - They are vague and ambiguous. The don't tell us what the function expects or what it does.
- How can we make it better?

閱讀這段描述後，仍不知道要傳入什麼，也不知道呼叫後會得到什麼結果。思考：使用者要如何判斷輸入是否合法？好的文件必須讓別人能正確呼叫與檢查結果。

**何者是好的註解？描述清楚回傳值與其間的關係**

- Make sure to explicitly state any assumptions the function has.
- Def decrease_red(pic,percent)
- '''Decreases the amount of red per pixel in picture pic by int percent. percent must be between 0 and 100.'''

透過 `decrease_red(pic, percent)` 說明參數意義與有效範圍：pic 表示要修改的影像；percent 代表紅色減少比例，教材指定為 0 到 100。這頁主要展示函式契約的文字表達，未提供完整實作。對閱讀者而言，這些輸入限制比單純敘述運算步驟更重要。Docstring 應能回答：「我可以傳什麼？結果代表什麼？」

> [!note] 單元 04 統整：寫文件是為了讓別人正確使用函式
> `help()`、好壞註解對照與影像範例，都在回答：呼叫者不用看完整程式碼，也能否知道函式的約定？用途 → 輸入前提 → 結果與限制。
> - **說目的**：說明函式做什麼，不必逐行重述每一步。
> - **說輸入與前提**：描述參數代表什麼、單位與有效範圍。
> - **說結果**：讓呼叫者知道得到的值與錯誤代表什麼。

> [!question] 想一想
> 一段只說 "process the image" 的註解，缺少哪些重要資訊？

> [!solution]- 答案（Claude）
> 缺少：參數是什麼（哪張圖、什麼型態、其他參數的意義）；做了哪一種處理；輸入的前提與有效範圍（例如 percent 要在 0–100）；結果是什麼（回傳一張新圖，還是直接修改原圖並回傳 None）。

### 實作單元 04：文件說明與測試依據

**Docstring：描述函式「保證做什麼」**：文件應說明輸入、單位、回傳結果與前提，而不是逐行翻譯程式。

> [!example] 範例：可獨立執行：第一個字串常值是 docstring
> ```python
> def average_speed(distance_km, duration_min):
>     """Return numeric km/h for a valid trip.
>
>     distance_km: finite, non-negative km.
>     duration_min: positive minutes.
>     Do not round or print the result.
>     """
>     return distance_km / (duration_min / 60)
>
> print(average_speed(3.5, 30))
> ```

> [!solution]- 輸出
> ```text
> 7.0
> ```
> 閱讀重點：1. 做什麼：回傳數值速度（km/h）。2. 需要什麼：已驗證的 km 和 minutes。3. 不做什麼：不印出、不提前捨入。好的 Docstring 是介面說明，不是程式內部流程的逐行解說。

> [!question] 動手練習
> 執行 `help(average_speed)`。如果把 `duration_min` 改成「小時」，這個 docstring 和公式應如何一起改？

> [!solution]- 答案（Claude 執行）
> ```text
> Help on function average_speed in module __main__:
>
> average_speed(distance_km, duration_min)
>     Return numeric km/h for a valid trip.
>
>     distance_km: finite, non-negative km.
>     duration_min: positive minutes.
>     Do not round or print the result.
>
> ```
> 改成小時時，參數名稱、docstring、公式要一起改：例如參數改名 `duration_h`，docstring 寫 `duration_h: positive hours.`，公式改成 `distance_km / duration_h`（不再除以 60）。只改其中一處，文件和程式就會互相矛盾；而且這是介面改變，所有呼叫者傳入的值也要改成小時。

**把文字承諾，轉成可執行的邊界測試**：不只測一般數值，也要檢查 30、31、60、61 等臨界值。Docstring → 流程規則 → assert。

> [!example] 範例：邊界測試
> ```python
> def duration_band(minutes):
>     """Return a band for positive whole minutes."""
>     if minutes <= 30:
>         return "Short"
>     if minutes <= 60:
>         return "Medium"
>     return "Long"
>
> assert duration_band(30) == "Short"
> assert duration_band(31) == "Medium"
> assert duration_band(60) == "Medium"
> assert duration_band(61) == "Long"
> print("Boundary tests passed")
> ```

> [!solution]- 輸出
> ```text
> Boundary tests passed
> ```
> 閱讀重點：1. 每個 `assert` 表達一個可檢查的預期值。2. 邊界值能揭露 `<=` 或 `<` 的錯誤。3. 不應直接把函式輸出抄作標準答案。**規格先決定答案；測試只是檢查程式是否符合規格。**

> [!question] 動手練習
> 新增 `duration_band(1)` 的測試。如果把第一個 `<= 30` 改成 `< 30`，哪個測試會失敗？

> [!solution]- 答案（Claude 執行）
> 新增 `assert duration_band(1) == "Short"`。把 `<= 30` 改成 `< 30` 後，`assert duration_band(30) == "Short"` 失敗（`AssertionError`）：30 會落到 Medium。`duration_band(1)` 的測試仍然通過，所以只測一般數值抓不到邊界錯誤。

> [!tip] Claude 補充：assert 是什麼
> `assert 條件` 在條件為 True 時什麼都不做；為 False 時立刻停下並產生 `AssertionError`。所以「全部 assert 都通過」才會走到最後的 `print`。這就是把 [[PROG1 Deck 1 整理#D1-Q6 如果 AI 可以寫 code，為什麼還要學 Programming|D1-Q6]] 的 test case（input＋獨立算出的 expected）寫成程式。

## W10-05 Variable Scope 與 Call Stack

對應投影片：W10｜45–60。

這一頁是老師投影片「遞迴」章節的封面（原標題保留），但後面會先說明變數作用域：先理解 Global／Local Variable，再理解 Call Stack 與函式間如何傳遞結果，最後進入 Recursion。先掌握每次呼叫的局部狀態，才容易理解遞迴的多層呼叫。

**Variable Scope：變數可用範圍。** Scope 說的是名稱能在哪裡查找。

> [!example] 範例：a 的可用範圍？（兩個看似相似的程式）
> ```python
> # a 的可用範圍 ?
> def f():
>     print(a)
> a = 1
> f()
> # a : global
> ```
> ```python
> # a 的可用範圍 ?
> def f():
>     a = 1
> f()
> print(a)
> # NameError: name 'a' is not defined
> # a: local
> ```

> [!solution]- 輸出（Claude 執行）
> 第一個程式：
> ```text
> 1
> ```
> 第二個程式：
> ```text
> NameError: name 'a' is not defined
> ```
> 函式可讀取模組層已有的 a（在沒有局部同名綁定時）；函式內建立的局部 a，不會自動出現在函式外。局部名稱與全域名稱不會因為字相同就變成同一個綁定。

**Global & Local Variable**：同時有 global & local variable 且同名的情況。

> [!example] 範例：同名的 Local 與 Global
> ```python
> # 同時有
> def f():
>     a = 1
>     print(a)
> a = 0
> f()
> print(a)
> #1
> #0
> #Why?
> ```

> [!solution]- 輸出
> ```text
> 1
> 0
> ```
> 全域 a = 0；`f()` 裡把局部 a 設為 1，印出 1；回到外面印出 0。請分別標示兩個 a 所在的作用域；不要把函式內的 `a = 1` 誤認為修改外面的 `a = 0`。**名字相同不代表變數綁定相同。**

**用呼叫框架（call frame）觀察局部狀態**：投影片 48–52 用同一段程式，一步一步追蹤「本次 f() 的局部 a」和「模組層的 a」。

| 投影片 | 目前執行到 | 本次 f() 的局部 a | 模組層的 a | 概念釐清 |
| --- | --- | --- | --- | --- |
| 49 | `a = 0`（模組層） | 尚未呼叫 f()；無本次局部值 | 0 | 此時尚未進入 f()；呼叫前的全域狀態不會因為函式已定義就先被更動。 |
| 50 | 進入 f()，執行 `a = 1` | 1 | 0 | 函式內 a = 1，不會改綁模組層的 a；每次呼叫都可能有自己的局部名稱綁定。 |
| 51 | f() 內的 `print(a)` | 1 | 0 | 印出 1；不是沿著呼叫堆疊搜尋變數。函式中的同名局部變數，會使全域同名變數被遮蔽。 |
| 52 | f() 結束，回到模組層的 `print(a)` | f() 已結束；不再執行此框架 | 0 | 印出 0。這表示執行位置改變，不是局部變數被複製到全域。 |

將「目前執行位置」和「變數在哪裡」分開觀察。投影片的 Function_1 與 Global 方框可以幫助追蹤執行中的狀態，但這個圖**不代表 Python 會沿呼叫堆疊查找所有名稱**：舊圖的「往回找變數」只是示意，不應當作 Python 通用的動態查找規則。Call Frame 協助理解函式執行；變數查找仍遵守作用域規則。**返回位置與變數的作用域是兩個不同概念。**

> [!note] 單元 05 統整：呼叫順序與名稱查找是兩個問題
> 藉由局部 a = 1 和全域 a = 0 的追蹤，觀察執行期間每個名稱的值。呼叫位置 → 局部狀態 → 回到呼叫者。
> - **局部改綁定**：在函式內對局部 a 賦值，不會因此改變外面的 a。
> - **呼叫框架**：Call Stack 說明執行中的函式，以及完成後要返回的位置。
> - **作用域**：Scope 決定名稱在哪裡查找；不能把它當成沿呼叫者堆疊搜尋。

> [!question] 想一想
> `f()` 裡印 1，外面印 0，這足以證明 Python 沿 Call Stack 查找變數嗎？

> [!solution]- 答案（Claude）
> 不能。這個例子只要用「f() 裡有自己的局部 a」就能解釋，兩種說法都會預測出 1、0。要分辨兩者，需要像實作單元 05 的 `read_label()` 那樣：被呼叫的函式讀不到呼叫者的局部變數，證明查找依照的是定義位置（lexical scope），不是呼叫堆疊。

### 數學填空 3：加一

> [!question] 數學填空 3｜加一：函式內外的 x 是同一個嗎？
> 數學目標 f(x) = x + 1。先預測 A，再利用函式讓外層 x 增加 1。請只填空白；不要先執行程式。
> ```python
> x = 10
>
> def add_one(x):
>     x = x + 1
>     return x
>
> y = add_one(3)
> print(y, x)          # A
>
> x = __________________ # ①
> print(x)             # B
> ```
> 先追蹤第一次呼叫：呼叫的引數是 3，不是外層的 10。
> 請填入輸出：A：＿＿＿＿；B：＿＿＿＿。
> 想一想：若最後只有 `add_one(x)`，沒有 `x =`，外層 x 會變嗎？
> 學生任務：替「外層 x」和「函式參數 x」畫兩個不同的框。

> [!solution]- 參考解答 3｜用指定敘述更新外層 x
> 填空答案：① `add_one(x)`
> ```python
> x = 10
>
> def add_one(x):
>     x = x + 1
>     return x
>
> y = add_one(3)
> print(y, x)
>
> x = add_one(x)
> print(x)
> ```
> ```text
> 4 10
> 11
> ```
> 手算追蹤：同一個名字，不同的綁定。第一次呼叫 `add_one(3)` 時，外層 x 並沒有被重新指定。
>
> | 執行位置 | 函式內的 x | 外層 x | 外層 y |
> | --- | --- | --- | --- |
> | 開始呼叫前 | 尚未建立 | 10 | 尚未指定 |
> | `add_one(3)` 開始 | 3 | 10 | 尚未指定 |
> | `x = x + 1` | 4 | 10 | 尚未指定 |
> | `return x` 後 | 本次呼叫結束 | 10 | 4 |
>
> 接著 `x = add_one(x)`：先用外層 10 計算出 11，再把 11 指定給外層 x。資料如何走？外層 10 → 局部計算 11 → return 11 → 外層 x = 11。局部 x 改綁定，不會自動改掉外層的同名變數。**要改變外層變數，明確接收結果，不依賴隱藏的全域修改。**

> [!failure] 常見錯誤：算出了新值，卻沒有接住它
> 這段程式沒有執行錯誤，但外層 x 不是學生可能猜測的 11。
> ```python
> x = 10
>
> def add_one(x):
>     x = x + 1
>     return x
>
> add_one(x)
> print(x)
> ```

> [!solution]- 預期輸出與分析
> ```text
> 10
> ```
> 呼叫做了什麼？函式用 10 計算出 11，並把 11 回傳。少了哪一步？呼叫者沒有使用指定敘述，所以沒有把 11 存回 x。函式回傳結果，與呼叫者是否保存結果，是兩個步驟。

### 實作單元 05：Scope 與函式呼叫

**Local Rebinding：同名不代表同一個變數**：函式中的參數是局部名稱；重新指派不會修改呼叫者的外層名稱。

> [!example] 範例：可獨立執行：追蹤 45 → 90 與外部 45
> ```python
> def double_minutes(minutes):
>     minutes = minutes * 2
>     return minutes
>
> minutes = 45
> result = double_minutes(minutes)
> print(result)
> print(minutes)
> ```

> [!solution]- 輸出
> ```text
> 90
> 45
> ```
> 資料／控制流程：外層 minutes = 45 → 函式內 minutes = 90 → return 90；外層仍為 45。重新綁定局部名稱，不等於修改呼叫者的外部名稱。

> [!question] 動手練習
> 如果把 `minutes = minutes * 2` 改成 `minutes += 10`，兩行輸出分別會是多少？

> [!solution]- 答案（Claude 執行）
> ```text
> 55
> 45
> ```
> `minutes += 10` 一樣只改綁函式內的局部 minutes。

**Lexical Scope：變數不是沿著呼叫堆疊尋找**：Call Stack 決定「誰在等誰」；名稱查找依函式的定義位置與作用域。

> [!example] 範例：可獨立執行：兩個函式都在模組層定義
> ```python
> label = "module"
>
> def read_label():
>     return label
>
> def caller():
>     label = "caller local"
>     return read_label()
>
> print(caller())
> ```

> [!solution]- 輸出
> ```text
> module
> ```
> 閱讀重點：1. `caller()` 雖然呼叫 `read_label()`；2. 但 caller 的局部 label 不在 read_label 的外圍作用域；3. read_label 讀到模組層的 label。**Scope 是名稱解析規則；Stack 是函式執行與返回的紀錄。**

> [!question] 動手練習
> 若在 `print(caller())` 前加上 `label = "changed"`，預期輸出是什麼？為什麼？

> [!solution]- 答案（Claude 執行）
> 印出 `changed`。`read_label()` 讀的是模組層的 label，而且是在**呼叫當下**才去讀；呼叫前模組層的 label 已改綁成 "changed"。caller 的局部 label 仍然讀不到。

**Call Stack：Function 完成後回到哪裡？** 以已經完成的 helper 組合，追蹤 main → format_trip → 小函式 → main。

> [!example] 片段：使用前面定義的 `format_trip()` 等函式（需先定義輔助函式）
> ```python
> # 使用先前定義的 average_speed()、
> # duration_band() 與 format_trip()
>
> def main():
>     report = format_trip("Campus", 3.5, 30)
>     print(report)
>
> main()
> ```

> [!solution]- 輸出
> ```text
> Route: Campus
> Distance: 2.17 miles
> Average speed: 7.00 km/h
> Trip band: Short
> ```
> 資料／控制流程：main → format_trip（等待文字）；format_trip → average_speed／band；各函式 return → 組成報告 → main。

> [!question] 動手練習
> 請畫出執行順序：main 開始，哪個函式取得 km=3.5？哪個函式產生 "Short"？最後由誰 print？

> [!solution]- 答案（Claude）
> 1. `main()` 呼叫 `format_trip("Campus", 3.5, 30)`，main 暫停等待。
> 2. `format_trip` 的參數 km 取得 3.5，算出 miles，再呼叫 `average_speed(km, minutes)`：average_speed 的 distance_km 也取得 3.5，回傳 7.0 後回到 format_trip。
> 3. `format_trip` 呼叫 `duration_band(30)`，由 duration_band 產生 "Short"，回到 format_trip。
> 4. `format_trip` 組好整份文字並 return 給 main；最後由 main 的 `print(report)` 印出。

## W10-06 UnboundLocalError 與作用域陷阱

對應投影片：W10｜61–70。

投影片 61–67 用同一段程式，一頁一頁追蹤錯誤怎麼發生，並修正前述範例「全域變數受到保護」的說法。

> [!example] 範例：局部名稱陷阱：先預測哪裡出錯
> ```python
> def f():
>     print(a)
>     if False:
>         a = 0
>
> a = 1
> f()
> ```

> [!solution]- 輸出（Claude 執行）
> ```text
> UnboundLocalError: cannot access local variable 'a' where it is not associated with a value
> ```
> 不是全域變數被保護；錯誤已在 `print(a)` 發生，程式不會繼續走到 if。

| 投影片 | 這一步 | 重點 |
| --- | --- | --- |
| 61 | 名稱判定：函式內有 a 的賦值 | 函式裡即使在 `if False` 中寫了 `a = 0`，a 仍被視為局部名稱；錯誤是 `UnboundLocalError`，並不是 Python 禁止函式改動 global。賦值會影響局部名稱判定，即使該賦值路徑不執行。 |
| 62 | 錯誤發生前：外面有 a = 1 | 先在模組層建立 a = 1，再呼叫 f()。全域 a = 1 存在，不代表函式中的同名局部 a 已經有值。 |
| 63 | 進入 f()：局部 a 尚未取得值 | Python 依函式本體的賦值決定 a 是局部名稱；執行尚未到任何對 a 的有效賦值。建立呼叫框架，不等於建立值：作用域判定與實際是否已賦值必須分開。 |
| 64 | 讀取局部 a：在 `print(a)` 發生錯誤 | 讀取該局部名稱時，不能因為尚未賦值就自動改讀全域 a。所以不是「先沿 Call Stack 找到外層變數」；用 lexical scope 理解比堆疊搜尋更精確。 |
| 65 | 全域的 a = 1 仍然存在 | 右側的全域 a = 1 並未消失，但 f() 的 `print(a)` 仍指向尚未綁定的局部 a。避免把「全域有值」誤判成「局部一定可讀」。 |
| 66 | 錯誤不在 if False 執行 | `if False: a = 0` 不會真的執行，但函式內有此賦值語法，已決定 a 是局部名稱；在 `print(a)` 讀取尚未綁定的局部 a，才產生錯誤。從程式結構和執行路徑兩側理解。 |
| 67 | 作用域陷阱的正確總結 | 局部名稱 a 被編譯期判定為 local；`print(a)` 前無有效的局部賦值，因此產生 UnboundLocalError。若要明確操作模組層的 a，可以使用 `global`，但要了解其副作用；程式應用建議多利用參數與回傳值表達資料關係。 |

**不是「Global 不可修改」，而是「未綁定局部名稱不可先讀取」。**

> [!note] 單元 06 統整：函式中的賦值會影響局部名稱判定
> `if False: a=0` 即使不執行，仍會使 a 被判定為局部名稱；錯誤發生在嘗試讀取尚未賦值的 a。函式內有賦值 → 判定為 local → 讀取前未綁定。
> - **錯誤位置**：`print(a)` 讀取未綁定的局部名稱，產生 UnboundLocalError。
> - **不是保護機制**：Python 不是一般性禁止修改全域變數；`global` 能明確改綁模組名稱。
> - **更好的理解方式**：分開觀察詞彙作用域、名稱是否已綁定，以及控制流程是否到達賦值。

> [!question] 想一想
> `if False` 永遠不執行，為什麼仍會影響函式內 `print(a)`？

> [!solution]- 答案（Claude）
> 「a 是不是局部名稱」是 Python 在執行前看整個函式本體決定的（只要本體裡任何地方有對 a 的賦值），跟那行會不會執行無關。執行時才檢查「這個局部 a 有沒有值」：`print(a)` 時還沒有，所以出錯。

### 實作單元 06：Scope 陷阱與可靠介面

**UnboundLocalError：沒有執行的賦值也會影響名稱**：這不是「全域變數受到保護」；是函式內已將名稱判定為局部名稱。

> [!example] 範例：故意出錯的示例：請單獨執行（預期產生錯誤）
> ```python
> count = 3
>
> def inspect_count():
>     print(count)
>     if False:
>         count = 0
>
> inspect_count()
> ```

> [!solution]- 輸出
> ```text
> UnboundLocalError: cannot access local variable 'count' where it is not associated with a value
> ```
> 投影片寫的執行結果是「UnboundLocalError at print(count)」。閱讀重點：1. 函式內存在對 count 的賦值。2. 因此 count 在此函式被視為局部。3. print 時局部 count 尚未綁定，便產生錯誤。**先判定 Scope，再執行讀取；不是呼叫時沿 Stack 向上尋找。**

> [!question] 動手練習
> 把函式改成 `def inspect_count(count): return count`，呼叫 `inspect_count(3)`，是否還需要 global？

> [!solution]- 答案（Claude 執行）
> 不需要。`inspect_count(3)` 回傳 `3`：資料從參數進來，函式根本不必碰模組層的 count。

**隱藏的全域依賴，會讓 Function 算錯**：函式接收 minutes，卻偷偷使用模組層的 duration_min。

> [!failure] 故意錯誤 → 修正參數使用（錯誤分析練習）
> ```python
> duration_min = 45  # 隱藏的全域值
>
> def bad_speed(km, minutes):
>     return km / (duration_min / 60)
>
> def average_speed(km, minutes):
>     return km / (minutes / 60)
>
> print(f"bad: {bad_speed(3.5,30):.2f}")
> print(f"good: {average_speed(3.5,30):.2f}")
> ```

> [!solution]- 輸出與分析
> ```text
> bad: 4.67
> good: 7.00
> ```
> 閱讀重點：1. 呼叫者明明提供 30 分鐘。2. bad_speed 卻使用全域的 45 分鐘。3. 相同距離、不同時間測試可抓到錯誤。避免讓函式對呼叫者隱藏依賴：**要用到的資料盡量從參數傳入。**

> [!question] 動手練習
> 呼叫 `bad_speed(3.5, 45)` 會顯示正確值嗎？為什麼只有這一組測試不足以發現錯誤？

> [!solution]- 答案（Claude 執行）
> 會：`bad_speed(3.5, 45)` 和 `average_speed(3.5, 45)` 都是 4.67。傳入的 45 剛好等於隱藏的全域 45，錯誤被巧合蓋住。要換一個不是 45 的時間（例如 30）才看得出差別。

## W10-07 Global State、Return 與資料傳遞

對應投影片：W10｜71–85。

**global 允許改綁全域名稱（Fetch Global Variable）**：要怎麼在 function 中修改 global variable 呢？使用 `global var` 來接取 global variable。

> [!example] 範例：global a
> ```python
> # 這裡也只有一個 global variable
> # function 中的 global a 會接到外面的
> # global variable a 不會自己一個
> def f():
>     global a
>     a = 1
>     print(a)
> a = 0
> f()
> print(a)
> ```

> [!solution]- 輸出
> ```text
> 1
> 1
> ```
> 在 f() 中宣告 `global a`，接著 `a = 1` 更改的是外部同名名稱的綁定，所以函式裡外印出的 a 都是 1。對照前面的局部 a 範例，外部狀態這次真的被改變了：原本全域 a = 0，f() 執行 `global a` 與 `a = 1`，返回後全域 a 變為 1，函式以外的其他程式也會看到新的全域值。
> 概念釐清：`global` 指定名稱所屬的模組作用域，不是沿呼叫堆疊往回搜尋。這是語言允許的操作；是否採用則是程式設計的選擇。global 改變名稱綁定的作用域，不是一般情況下的最佳設計；**改全域狀態會影響後續程式，必須知道誰負責更新它。**

**用 global 傳遞階乘結果（Declare Global Variable）**

> [!example] 範例：可以執行、但存在隱藏輸出依賴的階乘設計
> ```python
> # 在 function 內宣告位使用過的 global var
> def factorial(n):
>     global f  #沒有在 function 外宣告過
>     res = 1
>     for i in range(2, n + 1):
>         res *= i
>     f = res
> n = int(input())
> factorial(n)
> print(f)
> # doing other stuff with variable f
> ```

> [!solution]- Claude 執行：輸入 5
> ```text
> 120
> ```
> `factorial(n)` 計算階乘，將結果寫入全域 f；呼叫者之後透過 `print(f)` 取回結果。這裡的輸出不是由 return 明確交回；依賴全域 f，會增加測試、重用與追蹤資料的負擔。計算結果若只寫進 global f，呼叫者較難看出函式的輸出。

**global 宣告，不等於已經產生結果**：本次呼叫內仍有局部名稱 n、res、i，並非「沒有變數」。

> [!example] 範例：全域結果的隱藏依賴
> ```python
> def factorial(n):
>     global f
>     res = 1
>     for i in range(2, n + 1):
>         res *= i
>     f = res
>
> factorial(4)
> print(f)  # 24
> ```

> [!solution]- 輸出
> ```text
> 24
> ```
> 概念釐清：`global f` 指定綁定位置；直到 `f = res`，模組層 f 才取得計算結果。`factorial(n)` 必須執行成功，global f 才有預期結果；其他位置使用 f，依賴先前是否呼叫過 factorial（投影片圖中的 f=1 是示意，實際值會依 n 改變）。讓函式依賴呼叫順序與全域狀態，會降低可重用性。
> Claude 執行：同一段定義、但沒先呼叫 `factorial` 就 `print(f)`，得到 `NameError: name 'f' is not defined`。

**為什麼這種 global 寫法不好？（Reuse?）** 可以再次呼叫，但共享全域結果，較難獨立重用與測試：函式會改動與自己程式外部共用的名稱；當要連續計算不同 n 時，結果可能彼此覆寫；函式本身沒有清楚的回傳結果，測試也更不直接。能跑的函式，不一定具有清楚的輸入輸出介面。

**用 return 取代隱藏全域輸出**：同樣的功能，但右邊的寫法可達成再利用的效果（左邊就是上面的 global f 版本）。

> [!example] 範例：右邊的寫法
> ```python
> def factorial(n):
>     res = 1
>     for i in range(2, n + 1):
>         res *= i
>     return res
> n = int(input())
> f = factorial(n)
> print(f)
> # doing other stuff with variable f
> ```

> [!solution]- Claude 執行：輸入 5
> ```text
> 120
> ```
> 左側 `factorial(n)` 將答案存進 global f；右側 `factorial(n)` 回傳 res，呼叫者用 `f = factorial(n)` 接收。右側能直接測試 `factorial(5) == 120`（Claude 加上 `assert factorial(5) == 120`，通過）；外部仍可決定要存在哪個名稱，而不由 helper 偷偷指定。**return 讓計算結果成為清楚、可重用的函式介面。**

**一次回傳多個資料（Multi-Return）**：function 可以同時回傳多個變數：`return [a, b]`、`n, m = f(a, b)`。

> [!example] 範例：同時回傳
> ```python
> # 同時回傳 !&+
> def f(n):
>     a = 1
>     b = 1
>     for i in range(2, n + 1):
>         a *= i
>         b += i
>     return [a,b]
> n,m = f(100)
> ```

> [!solution]- Claude 執行：看看回傳了什麼
> ```python
> print(f(4))
> print(m)
> ```
> ```text
> [24, 10]
> 5050
> ```
> a 是 n!（累乘），b 是 1 + 2 + ⋯ + n（累加）；`f(100)` 的 n 是 100!（158 位數），m 是 5050。`return [a,b]` 回傳一個含兩個元素的 **list**；`n,m = f(100)` 會依序 unpack 成兩個名稱。程式應用使用 tuple 做相同概念的示範。**元素個數與順序屬於介面的一部分**：多筆資料可以一起回傳，再在呼叫位置解包使用。

> [!note] 單元 07 統整：讓資料傳遞從隱藏變為明確
> 使用 global 可以修改外部名稱，但以 return 明確交回資料通常更容易測試、組合和重複利用。提供輸入 → 回傳結果 → 呼叫者管理狀態。
> - **Global 的效果**：函式可以使用 global 修改模組層的名稱，但這讓呼叫有可見的副作用。
> - **Return 的優點**：`factorial(n)` 回傳 res，呼叫者自己決定結果存在哪裡。
> - **多筆回傳**：`return [a,b]` 與 tuple 都能包裝資料；解包時需遵守個數與順序。

> [!question] 想一想
> 為什麼 `f = factorial(n)` 比 `factorial(n)` 偷偷修改 global f 更容易測試？

> [!solution]- 答案（Claude）
> return 版本可以直接寫 `assert factorial(5) == 120`：一次呼叫、一個結果，不需要先準備或事後讀取外部狀態。global 版本要先呼叫、再去讀全域 f，而且 f 的值取決於「最後一次」呼叫是誰，兩個測試會互相覆寫。

### 數學填空 4：總和與平方和

> [!question] 數學填空 4｜總和與平方和：何時才算完成？
> 計算 S(n) = 1 + ⋯ + n，Q(n) = 1² + ⋯ + n²；n 是非負整數，n = 0 時兩者皆為 0。請只填空白；不要先執行程式。
> ```python
> def two_sums(n):
>     s, q = 0, 0
>     for k in range(1, n + 1):
>         s += k
>         q += ________          # ①
>     return ________, ________ # ②③
>
> a, b = two_sums(3)
> print(a, b)
> print(two_sums(0))
> ```
> 回傳順序已約定：先回傳總和，再回傳平方和。
> 先手算：S(3) = ＿＿＿＿；Q(3) = ＿＿＿＿。
> 檢查縮排：return 應在 for 裡面，還是等 for 結束之後？
> 學生任務：填①②③；再預測 `two_sums(0)` 回傳什麼。

> [!solution]- 參考解答 4｜算完再回傳，依順序接收
> 填空答案：① `k * k`　② `s`　③ `q`
> ```python
> def two_sums(n):
>     s, q = 0, 0
>     for k in range(1, n + 1):
>         s += k
>         q += k * k
>     return s, q
>
> a, b = two_sums(3)
> print(a, b)
> print(two_sums(0))
> ```
> ```text
> 6 14
> (0, 0)
> ```
> 手算追蹤：每次迴圈各加進一項。
>
> | 完成的階段 | s：目前總和 | q：目前平方和 |
> | --- | --- | --- |
> | 尚未開始 | 0 | 0 |
> | k = 1 | 0 + 1 = 1 | 0 + 1² = 1 |
> | k = 2 | 1 + 2 = 3 | 1 + 2² = 5 |
> | k = 3 | 3 + 3 = 6 | 5 + 3² = 14 |
>
> n = 0 時，迴圈一次也不執行；保留初值，所以最後回傳 (0, 0)。完成全部累加後，才把 s、q 打包成一個 tuple 回傳。`return s, q` 產生一個 tuple；a, b 依照位置拆開它（a 接總和，b 接平方和；接收變數的名稱不會自動改變對應順序）。**回傳的個數、順序與回傳時機，都是函式介面的一部分。**

> [!failure] 常見錯誤：return 縮排到迴圈裡面
> 以下會在第一項加完後，就結束整次函式呼叫。
> ```python
> def two_sums(n):
>     s, q = 0, 0
>     for k in range(1, n + 1):
>         s += k
>         q += k * k
>         return s, q
>
> print(two_sums(3))
> print(two_sums(0))
> ```

> [!solution]- 預期輸出與分析
> ```text
> (1, 1)
> None
> ```
> n = 3：k = 1 後就 return，不會繼續執行 k = 2、3。n = 0：迴圈不執行，return 也沒執行；走到函式結尾回傳 None。**return 離開函式；break 才是只離開最內層迴圈。**

> [!warning] Claude 提醒：return 縮排是追蹤題的經典陷阱
> 期中考古題都是迴圈追蹤（[[PROG1 Midterm 考古題#A4 for 迴圈與同時指派（10 分）|A4]]、[[PROG1 Midterm 考古題#A7 Fibonacci 找 index（12 分）|A7]]）；包進函式以後，多一個要盯的地方：`return` 在迴圈裡面還是外面。在迴圈裡的 return 只跑一輪；迴圈一次都沒跑時，函式可能根本沒碰到 return，得到 None。

### 實作單元 07：多函式整合與測試

**Global vs Return：誰應該保存計算結果？** 同樣是計算階乘，使用 return 能讓結果由呼叫者管理，避免不必要的全域狀態。

> [!example] 範例：兩種版本：相同結果、不同的責任分工
> ```python
> result = 0
>
> def factorial_global(n):
>     global result
>     result = 1
>     for i in range(2, n + 1):
>         result *= i
>
> def factorial(n):
>     value = 1
>     for i in range(2, n + 1):
>         value *= i
>     return value
>
> factorial_global(4)
> print(result)
> print(factorial(4))
> ```

> [!solution]- 輸出
> ```text
> 24
> 24
> ```
> 閱讀重點：1. global 版本會改動外部 result。2. return 版本把計算結果交給呼叫者。3. 明確回傳值更容易重用與單獨測試。

> [!question] 動手練習
> 如果依序呼叫 `factorial(3)` 與 `factorial(5)`，要怎麼同時保存 6 和 120？改成使用全域 result 會有何限制？

> [!solution]- 答案（Claude 執行）
> return 版本：`a = factorial(3)`、`b = factorial(5)`，印出 `6 120`，兩個結果各自有名字。global 版本只有一個 result：`factorial_global(5)` 會把 6 覆寫成 120，所以每次呼叫完都得趕快把 result 複製到別的名稱（`r3 = result`），漏一次就弄丟。

**Multiple Return：一次傳回一筆資料**：一筆行程有名稱、公里、分鐘三個欄位；使用 tuple 依順序交回呼叫者。

> [!example] 範例：教學縮小版：只示範拆欄位；尚未做完整驗證（已知格式正確）
> ```python
> def trip_fields(raw_line):
>     label, km_text, min_text = raw_line.split(",")
>     return label.strip(), float(km_text), int(min_text)
>
> trip = trip_fields("Campus,3.5,30")
> print(trip)
> label, km, minutes = trip
> print(label, km, minutes)
> ```

> [!solution]- 輸出
> ```text
> ('Campus', 3.5, 30)
> Campus 3.5 30
> ```
> 閱讀重點：1. 函式實際上回傳一個三元素 tuple。2. 左邊三個名稱依照位置 unpack。3. 順序與欄位數都是介面的一部分。`parse_trip()` 在完整版還需要檢查輸入、拋出 ValueError。

> [!question] 動手練習
> 把輸入改成 `"Station,1.2,45"`。如果輸入變成 `"Broken,1"`，簡化版會發生什麼事？

> [!solution]- 答案（Claude 執行）
> `trip_fields("Station,1.2,45")` → `('Station', 1.2, 45)`。`trip_fields("Broken,1")` 在第一行解包時失敗：`ValueError: not enough values to unpack (expected 3, got 2)`。split 只切出兩段，裝不進三個名稱；這個錯誤訊息對使用者沒有意義，所以完整版要先檢查欄位數。

**Validation 與 Exception：把錯誤交回控制器**：helper 不必決定使用者介面；它可以用 `ValueError` 明確報告失敗。

> [!example] 範例：可獨立執行：先練習局部資料驗證
> ```python
> def require_label(text):
>     label = text.strip()
>     if label == "":
>         raise ValueError("Error: empty label.")
>     return label
>
> for raw in ["Campus", " "]:
>     try:
>         print(require_label(raw))
>     except ValueError as error:
>         print(error)
> ```

> [!solution]- 輸出
> ```text
> Campus
> Error: empty label.
> ```
> 閱讀重點：1. 成功時 return 已處理過的值。2. 失敗時 `raise ValueError`，停止正常回傳。3. 呼叫者用 `except` 決定是否顯示、繼續或停止。完整 `parse_trip()` 還需檢查欄位數、數值轉型與合法範圍。

> [!question] 動手練習
> 如果把空白標籤交給 `require_label()`，為什麼不應讓它回傳 `""` 當成成功資料？在 main 裡應該何時更新統計？

> [!solution]- 答案（Claude）
> 回傳 `""` 時呼叫者分不出「成功」和「失敗」，空標籤會被當成有效行程算進筆數與總和；raise 讓失敗走另一條路，呼叫者不可能不小心拿到它。main 應該在 parse 沒有拋出例外、報告也印出以後，才更新筆數與總和（見下一節的主流程）。

> [!tip] Claude 補充：try／except 在這一章的角色
> Deck 3–5 的 try／except 是用來接 `int()`、`float()` 的轉型錯誤（[[PROG1 Deck 5 整理#D5-Q4 如何把一行文字解析成有效欄位|D5-Q4]]）。這裡多了 `raise`：函式自己發現資料不合規格時，主動丟出 `ValueError`，把「要不要印、要不要繼續」交給呼叫者決定。

## W10 整合實作：行程紀錄程式

對應投影片：W10｜86–93。

**完整資料解析 `parse_trip()`**：先確認這一行的結構（把欄位數與空標籤處理好，才進行數值轉換），再轉成數值、檢查範圍。投影片分兩頁，第二頁的程式行都仍在函式內；這裡合成一段。

> [!example] 範例：`parse_trip()`（投影片 86–87）
> ```python
> import math
>
> def parse_trip(raw_line):
>     line = raw_line.strip()
>     if line == "":
>         raise ValueError("Error: empty record.")
>     if '"' in line:
>         raise ValueError("Error: double quotes are not supported.")
>     fields = line.split(",")
>     if len(fields) != 3:
>         raise ValueError("Error: expected route, km, minutes.")
>     label = fields[0].strip()
>     km_text = fields[1].strip()
>     min_text = fields[2].strip()
>     if label == "":
>         raise ValueError("Error: route label must not be empty.")
>     try:
>         km = float(km_text)
>         minutes = int(min_text)
>     except ValueError:
>         raise ValueError("Error: distance must be numeric "
>                          "and minutes an integer.") from None
>     if not math.isfinite(km):
>         raise ValueError("Error: distance must be finite.")
>     if km < 0:
>         raise ValueError("Error: distance must be non-negative.")
>     if minutes <= 0:
>         raise ValueError("Error: duration must be positive.")
>     return label, km, minutes
> ```

> [!solution]- Claude 執行：把投影片提到的輸入都丟進去
> ```text
> 'Broken,1' -> Error: expected route, km, minutes.
> 'Campus,1,30.9' -> Error: distance must be numeric and minutes an integer.
> 'Campus,-1,0' -> Error: distance must be non-negative.
> '' -> Error: empty record.
> '"Campus, East",1,45' -> Error: double quotes are not supported.
> '  ,1,30' -> Error: route label must not be empty.
> 'Campus,nan,30' -> Error: distance must be finite.
> 'Campus,1,0' -> Error: duration must be positive.
> 'Station,3.5,30' -> ('Station', 3.5, 30)
> ```
> 先看順序（1/2）：空行 → 不支援的雙引號 → 欄位數 → 空標籤。手動追蹤：`"Broken,1"` 只有兩欄，在數值轉換前就被拒絕。誰處理 DONE？主流程先檢查結束命令；parse_trip 只處理候選資料。同一筆有多個問題時，**先回報哪個錯誤也是規格的一部分**。
> 三類檢查別混在一起（2/2）：轉型失敗、非有限數值、負距離或非正時間。比較兩筆輸入：`"Campus,1,30.9"` 整數轉型失敗；`"Campus,-1,0"` 先回報負距離。成功才回傳：只有資料通過全部檢查，才回傳 (label, km, minutes)。**失敗用 raise；成功用 return。呼叫者不會拿到半套資料。**

> [!tip] Claude 補充：`from None` 是什麼
> 在 `except ValueError:` 裡再 `raise` 一個新的 ValueError 時，Python 預設會把原本 `float()`／`int()` 的錯誤也一起附上（"During handling of the above exception, another exception occurred"）。`from None` 把舊的錯誤藏起來，呼叫者只看到自己寫的那一句訊息。這份規則表和 [[PROG1 Deck 5 整理#D5-Q4 如何把一行文字解析成有效欄位|D5-Q4]] 的拒絕階段一致，只是改成函式。

**最後摘要 `format_summary()`**：總和由呼叫者提供，函式只組成文字；先處理零筆資料，再計算平均時間與整體速度。

> [!example] 範例：`format_summary()`（投影片 88）
> ```python
> def format_summary(count, total_km, total_min):
>     if count == 0:
>         return "Accepted trips: 0\nNo valid trips to summarize."
>     mean_duration = total_min / count
>     overall_speed = average_speed(total_km, total_min)
>     return (
>         f"Accepted trips: {count}\n"
>         f"Total distance: {total_km:.2f} km\n"
>         f"Total duration: {total_min} min\n"
>         f"Mean duration: {mean_duration:.2f} min\n"
>         f"Overall speed: {overall_speed:.2f} km/h"
>     )
> ```
> 前提：count、total_km、total_min 都來自相同批有效資料。為什麼先檢查零筆？避免計算 total_min / 0，也避免把沒有資料誤當平均為 0。誰負責累加？這個函式只 return 字串；不讀鍵盤、不偷偷改總和。「維持統計狀態」和「把統計顯示出來」分成不同責任。

**主流程 `main()`**：每筆資料先分成停止、拒絕、接受；六個 helper 都準備好以後，main() 負責安排順序與保存統計。投影片分兩頁，第二頁接續上一頁的 while 迴圈；這裡合成一段。

> [!example] 範例：`is_done()` 與 `main()`（投影片 89–90）
> ```python
> def is_done(raw_line):
>     return raw_line.strip().upper() == "DONE"
>
> def main():
>     count = 0
>     total_km = 0.0
>     total_min = 0
>     while True:
>         raw = input("Trip (route, km, minutes; DONE to finish): ")
>         if is_done(raw):
>             break
>         try:
>             label, km, minutes = parse_trip(raw)
>         except ValueError as error:
>             print(error)
>             continue
>         print(format_trip(label, km, minutes))
>         count += 1
>         total_km += km
>         total_min += minutes
>     print(format_summary(count, total_km, total_min))
>
> if __name__ == "__main__":
>     main()
> ```

| 路徑 | 什麼時候 | 做什麼 |
| --- | --- | --- |
| STOP：結束命令 | 整行 DONE（`is_done` 成立） | `break`，離開迴圈 |
| REJECT：無效資料 | `parse_trip` 拋出 ValueError | 印一次錯誤後 `continue` |
| ACCEPT：有效資料 | 沒有例外 | 先輸出這一筆報告，再更新筆數、總公里、總分鐘 |

拒絕資料的路徑不會走到統計更新；這是流程設計，不是巧合。觀察縮排：`count += 1` 在 while 內；最終 print 在 while 外，離開迴圈以後只輸出**一次**最終摘要，全部資料無效也要能處理。**main 管流程與狀態；helper 接資料、做工作、交回結果。**

**完整執行追蹤：把四行輸入走一遍**（每次只看一行資料，記錄 count、total_km、total_min 是否改變）：

| 輸入 | 走哪條路徑？ | count | 總 km | 總 min |
| --- | --- | --- | --- | --- |
| Campus East,12.5,45 | 接受；報告並更新 | 1 | 12.5 | 45 |
| Broken,1 | 拒絕；統計不動 | 1 | 12.5 | 45 |
| Station,3.5,30 | 接受；報告並更新 | 2 | 16.0 | 75 |
| DONE | 停止；輸出摘要 | 2 | 16.0 | 75 |

獨立手算：平均時間 75 ÷ 2 = 37.50 分鐘；整體速度 16 ÷ (75 ÷ 60) = 12.80 km/h。既要測每個函式，也要測主流程；各部分正確不代表連接一定正確。

> [!solution]- Claude 執行：完整程式跑一次
> 把 `duration_band()`、`average_speed()`、`format_trip()`、`parse_trip()`、`format_summary()`、`is_done()`、`main()` 放進同一個檔案，用管線送入上面四行（所以畫面上看不到輸入的那一行，提示後面直接接程式的輸出）：
> ```text
> Trip (route, km, minutes; DONE to finish): Route: Campus East
> Distance: 7.77 miles
> Average speed: 16.67 km/h
> Trip band: Medium
> Trip (route, km, minutes; DONE to finish): Error: expected route, km, minutes.
> Trip (route, km, minutes; DONE to finish): Route: Station
> Distance: 2.17 miles
> Average speed: 7.00 km/h
> Trip band: Short
> Trip (route, km, minutes; DONE to finish): Accepted trips: 2
> Total distance: 16.00 km
> Total duration: 75 min
> Mean duration: 37.50 min
> Overall speed: 12.80 km/h
> ```
> 和手算一致。第一行就輸入 DONE 時，輸出 `Accepted trips: 0` 與 `No valid trips to summarize.`，沒有除以零。

**Module：把計算與互動放在不同 Python 檔案**：`trip_core.py` 放 helper；`trip_app.py` 放 main 與輸出，兩個檔案放同一資料夾。

> [!example] 範例：分別建立兩個檔案，從 trip_app.py 執行（兩個 .py 檔）
> ```python
> # 檔案 A：trip_core.py
> def average_speed(km, minutes):
>     return km / (minutes / 60)
>
> # 檔案 B：trip_app.py
> from trip_core import average_speed
>
> def main():
>     speed = average_speed(3.5, 30)
>     print(f"Speed: {speed:.2f} km/h")
>
> if __name__ == "__main__":
>     main()
> ```

> [!solution]- 輸出
> ```console
> $ python trip_app.py
> Speed: 7.00 km/h
> ```
> 資料／控制流程：執行 `python trip_app.py` → `main()` → 匯入的 `average_speed()` → return 7.0 → `main()` 再 `print()`。**被 import 時不應自動呼叫 main() 問使用者輸入。**

> [!tip] Claude 補充：`if __name__ == "__main__":` 為什麼有用
> 直接執行一個檔案時，它的 `__name__` 是 `"__main__"`；被別的檔案 import 時，`__name__` 是模組名稱（例如 `"trip_app"`）。Claude 執行 `import trip_app`：沒有出現 Speed 那一行，main() 沒被呼叫。所以測試檔可以放心 import，不會卡在 `input()`。

> [!question] 動手練習
> 實際建立兩個 .py 檔並執行；再把 `duration_band()` 放入 `trip_core.py`，供後續測試。

> [!solution]- 答案（Claude 執行）
> 兩個檔案放在同一個資料夾，`python trip_app.py` 印出 `Speed: 7.00 km/h`。把 [[#實作單元 01：函式與工作分解]] 的 `duration_band()` 加到 `trip_core.py` 之後，下面的 `test_trip_core.py` 就能 import 它。

**Testing：拆成功了嗎？不只要看一次輸出**：個別 helper、完整 session 與修改前後的行為，要分別建立證據。

> [!example] 範例：`test_trip_core.py`：先將 `duration_band()` 加入 `trip_core.py`（測試環境正常執行）
> ```python
> import math
> from trip_core import average_speed, duration_band
>
> assert duration_band(30) == "Short"
> assert duration_band(31) == "Medium"
> assert type(average_speed(3.5, 30)) is float
> assert math.isclose(average_speed(5, 45), 20/3,
>                     rel_tol=1e-12)
> print("Helper checks passed.")
> ```

> [!solution]- 輸出
> ```text
> Helper checks passed.
> ```
> 閱讀重點：1. **Helper**：函式回傳值、型態、邊界。2. **Session**：DONE、拒絕資料、有效統計。3. **Regression**：原有輸入的結果不可偷偷改變。AI 修改後也要重新執行測試，而不是只相信「看起來乾淨」。

> [!question] 動手練習
> 若把 `duration_band()` 的 return 改成 print，哪個 assert 會失敗？再用前面的四行輸入，核對總公里與總分鐘。

> [!solution]- 答案（Claude 執行）
> 第一個 `assert duration_band(30) == "Short"` 就失敗（`AssertionError`）：函式印出文字，但回傳 None，`None == "Short"` 是 False，後面的 assert 不會再執行。四行輸入的總公里是 16.00 km、總分鐘是 75 min，和上面的完整執行一致。

> [!tip] Claude 補充：浮點數為什麼用 `math.isclose`
> `average_speed(5, 45)` 是 6.666666666666667，`20/3` 也是無限小數的近似值。浮點數比較用 `==` 可能因為最後一位不同而失敗（[[PROG1 Deck 2 整理#D2-Q5 如何把數量關係寫成運算式|D2-Q5]] 的 `0.1 + 0.2`），所以用「相對誤差小於 1e-12」來判斷。

## W10-08 Recursion、Loop 與執行成本

對應投影片：W10｜94–103。

**Recursion：函式呼叫自己。** Function 可以呼叫別的 function；Function 可以呼叫自己嗎？可以，這種做法稱為 recursion。

> [!example] 範例：遞迴階乘
> ```python
> def factorial(n):
>     if n == 0:
>         return 1
>     else:
>         return n * factorial(n - 1)
> ```

> [!solution]- Claude 執行：`print(factorial(4), factorial(0))`
> ```text
> 24 1
> ```
> 遞迴把原本的問題，轉為規模更小的同類問題：`factorial(n)` 若 n == 0 就 return 1；否則回傳 `n * factorial(n - 1)`。每次呼叫都等待下一層返回結果。**Base Case 是使呼叫能停止的條件**；遞迴必須有終止條件，也必須逐步接近它。

**遞迴為什麼容易出錯？**

- Recursion 很簡潔
- 但是容易出錯，一定要仔細驗證
- 例子：無窮 recursion

> [!example] 範例：無窮 recursion
> ```python
> def f():
>     return f()
> ```

> [!solution]- Claude 執行：呼叫 `f()`
> ```text
> RecursionError: maximum recursion depth exceeded
> ```
> 完全不停止的 f() → f() 無法得到回傳結果；若遞迴參數不往基本情況靠近，也無法正常完成。在 Python 中通常會遇到 `RecursionError`。

無窮 recursion 成因：

- Incorrect stopping condition. For example, if in the factorial-calculating program we forget to put the check if n == 0, then factorial(0) will call factorial(-1), that will call factorial(-2), etc.
- Recursive call with incorrect parameters. For example, if the function factorial(n) calls the function factorial(n), we will also obtain an infinite chain of calls.

不要只看程式短不短，必須驗證每條路徑會走向終點：**Base Case 與進展方向缺一不可。**

**同一問題可用 Loop 或 Recursion。** 重要觀念：迴圈跟 Recursion 可以互換：能用迴圈寫的可以換成 recursion，Recursion 也可以換成迴圈。

> [!example] 範例：階乘的迴圈版與遞迴版
> ```python
> def factorial(n):
>     res = 1
>     for i in range(2, n + 1):
>         res *= i
>     return res
> ```
> ```python
> def factorial(n):
>     if n == 0:
>         return 1
>     else:
>         return n * factorial(n - 1)
> ```

> [!solution]- Claude 執行：兩個版本都算 `factorial(4)`
> ```text
> 24
> 24
> ```
> Loop 反覆更新 res；Recursion 將部分計算交給下一層呼叫。用 n = 4 追蹤兩邊最後都得到 24，但它們的執行方式和需要保存的狀態不同。選擇 Loop 或 Recursion，應看可理解性與執行限制。

**遞迴與效率：看呼叫成本。** 迴圈與遞迴：同一個階乘，不同的執行方式。

| 迴圈 `factorial_loop(n)` | 遞迴 `factorial(n)` |
| --- | --- |
| 同一個呼叫內反覆更新 | 多個呼叫等待返回 |
| Loop 在同一次函式呼叫中反覆執行 | Recursion 為每一層建立新的呼叫狀態 |

Python 的階乘遞迴通常有額外呼叫成本與深度限制。概念釐清：本例可討論遞迴呼叫與深度成本；不能只憑程式行數判定所有程式的效率，也不能將這一個例子推廣為所有語言和演算法的速度定律。**能否遞迴和適不適合遞迴，是兩個不同問題。**

> [!tip] Claude 補充：Python 的深度限制
> Claude 執行 `sys.getrecursionlimit()` 得到 1000：預設大約一千層呼叫就會 `RecursionError`。所以遞迴版的 `factorial(5000)` 會失敗，迴圈版不會。`factorial(-1)` 也會 `RecursionError`：−1、−2、⋯ 永遠不會碰到 n == 0，這就是投影片說的「負數不會朝 0 前進」。

> [!note] 單元 08 統整：遞迴是另一種組織重複計算的方法
> `factorial(n)` 用 n × factorial(n−1) 表達問題的遞迴結構；這個寫法必須有基本情況，也要逐步接近終點。遞迴呼叫 → Base case → 逐層返回。
> - **停止條件**：n == 0 時回傳 1，避免繼續向下呼叫。
> - **遞迴進展**：factorial(n−1) 每次讓問題規模變小。
> - **Loop 對照**：兩者可以得到相同結果，但 Python 的遞迴多了呼叫成本與深度限制。

> [!question] 想一想
> `factorial(4)` 如何在遇到 n == 0 後，一層一層回傳 24？

> [!solution]- 答案（Claude）
> factorial(0) 直接回傳 1 → factorial(1) 算 1 × 1 = 1 → factorial(2) 算 2 × 1 = 2 → factorial(3) 算 3 × 2 = 6 → factorial(4) 算 4 × 6 = 24。每一層都在等內層的結果，拿到之後才完成自己的乘法。

### 數學填空 5：階乘

> [!question] 數學填空 5｜階乘：有終點，就一定到得了嗎？
> 數學目標：0! = 1；n! = n × (n − 1)!。n 是小的非負整數。請只填空白；不要先執行程式。
> ```python
> def factorial(n):
>     if n == 0:
>         return ________ # ①
>     return ________ * factorial(________)
>         # ②                     # ③
>
> print(factorial(4))
> print(factorial(0))
> ```
> 基本情況：什麼輸入不需要再呼叫自己？這個情況要回傳多少？
> 遞迴步驟：每次呼叫的參數，是否比上一次更接近 0？
> 請預測輸出：factorial(4)：＿＿＿＿；factorial(0)：＿＿＿＿。
> 學生任務：填①②③；再畫出 `factorial(2)` 的呼叫與回傳順序。

> [!solution]- 參考解答 5｜每次減 1，直到基本情況
> 填空答案：① `1`　② `n`　③ `n - 1`
> ```python
> def factorial(n):
>     if n == 0:
>         return 1
>     return n * factorial(n - 1)
>
> print(factorial(4))
> print(factorial(0))
> ```
> ```text
> 24
> 1
> ```
> 手算追蹤：向下呼叫與向上回傳是不同階段（用 factorial(3) 觀察每一層在等待什麼結果）。
>
> | 向下呼叫：逐步接近 0 | 向上回傳：把等待的乘法算完 |
> | --- | --- |
> | factorial(3) 等待 3 × factorial(2) | factorial(0) = 1 |
> | factorial(2) 等待 2 × factorial(1) | factorial(1) = 1 × 1 = 1 |
> | factorial(1) 等待 1 × factorial(0) | factorial(2) = 2 × 1 = 2 |
> | factorial(0) 直接回傳 1 | factorial(3) = 3 × 2 = 6 |
>
> 每一層呼叫有自己的 n；內層完成後，外層才繼續運算。學生任務的 factorial(2)：向下 factorial(2) → factorial(1) → factorial(0)；向上 1 → 1 × 1 = 1 → 2 × 1 = 2。
> 前提不是裝飾：本例只討論小的非負整數；負數不會朝 0 前進。**基本情況給答案，遞迴步驟把問題縮小。**

> [!failure] 常見錯誤：每次都呼叫 factorial(n)
> 停止條件雖然存在，但這條呼叫路徑永遠到不了 n == 0。
> ```python
> def factorial(n):
>     if n == 0:
>         return 1
>     return n * factorial(n)
>
> print(factorial(4))
> ```

> [!solution]- 預期輸出與分析
> ```text
> RecursionError: maximum recursion depth exceeded
> ```
> 參數沒有改變：factorial(4) → factorial(4) → factorial(4) → …。要檢查兩件事：有沒有**終止條件**？有沒有**朝終點前進**？遞迴的下一次輸入必須推進問題，不能只重複原問題。

### 實作單元 08：遞迴與呼叫堆疊

**Recursion：函式也能呼叫自己**：用階乘觀察 Base Case、遞迴呼叫，以及每一層如何等待結果返回。

> [!example] 範例：兩種算法：相同結果、不同的執行流程
> ```python
> def factorial_loop(n):
>     value = 1
>     for i in range(2, n + 1):
>         value *= i
>     return value
>
> def factorial(n):
>     if n == 0:
>         return 1
>     return n * factorial(n - 1)
>
> print(factorial_loop(4))
> print(factorial(4))
> ```

> [!solution]- 輸出
> ```text
> 24
> 24
> ```
> 資料／控制流程：向下呼叫 4 → 3 → 2 → 1 → 0；基本情況 factorial(0) = 1；逐層回傳 1 → 2 → 6 → 24。必須有 Base Case，且每次呼叫都要逐步接近終點。

> [!question] 動手練習
> 先畫出 `factorial(3)` 的呼叫與返回順序。若刪除 `n == 0` 的停止條件，會出現什麼問題？

> [!solution]- 答案（Claude 執行）
> 呼叫：factorial(3) → factorial(2) → factorial(1) → factorial(0)；返回：1 → 1 → 2 → 6。刪除停止條件後，factorial(0) 會繼續呼叫 factorial(−1)、factorial(−2)⋯，Claude 執行得到 `RecursionError: maximum recursion depth exceeded`。

## W10 課後自我檢查與複習練習

對應投影片：W10｜104。

課後自我檢查：我能解釋，而不只是執行成功嗎？用五個數學問題，檢查本章最容易混淆的地方。

| 看到這種寫法… | 我應該能回答… |
| --- | --- |
| `y = square(3)` | 顯示與回傳的差別是什麼？ |
| `if x < 0: return -x` | 沒有進入 if 時，函式會交回什麼？ |
| `add_one(x)` | 外層 x 是否被重新指定？ |
| `for … / return s, q` | 在何時回傳？以什麼順序回傳？ |
| `factorial(n - 1)` | 有終點嗎？每次都有朝終點前進嗎？ |

學習檢核：每次都問：**輸入是什麼？結果交給誰？在哪一行結束？**

> [!question] 練習
> 1. `square()` 裡寫 `print(x * x)` 而不是 `return x * x`，`y = square(3)` 之後 y 是什麼？
> 2. `abs_value()` 只有 `if x < 0: return -x`，`abs_value(0)` 回傳什麼？
> 3. `x = 10` 之後只寫 `add_one(x)`，外層 x 是多少？
> 4. `two_sums()` 的 return 縮排到 for 裡面，`two_sums(3)` 與 `two_sums(0)` 各回傳什麼？
> 5. `factorial()` 的遞迴步驟寫成 `factorial(n)`，會發生什麼？
> 6. `def f(x, y=10, z):` 與「先呼叫再定義」分別是哪一種錯誤？
> 7. 函式內有 `if False: a = 0`，前面先 `print(a)`，為什麼是 UnboundLocalError？
> 8. 為什麼 `parse_trip()` 失敗時用 raise，而不是回傳空字串或 None？

> [!solution]- 解答與理由
> 1. None：print 只顯示 9，函式走到結尾回傳 None；接著 `y + 1` 會 TypeError。
> 2. None：0 不進 if，走到函式結尾沒有 return。
> 3. 10：回傳的 11 沒有被指定給 x；要寫 `x = add_one(x)`。
> 4. `(1, 1)` 與 `None`：第一輪就 return；n = 0 時迴圈不跑、也碰不到 return。
> 5. 參數不變，永遠到不了 n == 0，得到 RecursionError。
> 6. 前者是 SyntaxError（無預設值的參數排在有預設值的參數之後，整個檔案不會執行）；後者是 NameError（執行到 `f(3)` 時 f 還沒定義）。
> 7. 函式內只要有對 a 的賦值，a 就被判定為局部名稱；`print(a)` 時局部 a 尚未綁定，也不會退回讀全域 a。
> 8. 回傳空值時呼叫者可能把它當成有效資料算進統計；raise 讓失敗走 except 那條路，呼叫者不會拿到半套資料。

> [!tip] Claude 補充：本章出現的錯誤類型
> | 錯誤 | 本章的例子 |
> | --- | --- |
> | `TypeError` | `None + 1`（函式只 print 沒 return）；少給必要引數 `f(3)`；自訂 `max(a, b)` 遮蔽內建 max 後呼叫 `max(3, 4, 5)` |
> | `SyntaxError` | `def f(x, y = 10, z):` |
> | `NameError` | 先呼叫再定義 `f(3)`；在函式外讀函式內的局部 a；還沒呼叫 factorial 就讀 global f |
> | `UnboundLocalError` | 函式內有 `if False: a = 0`，前面先 `print(a)` |
> | `IndexError` | `maximum()` 沒有傳任何值，`values[0]` 失敗 |
> | `ValueError` | `"Broken,1"` 解包成三個名稱；`parse_trip()` 主動 raise |
> | `ZeroDivisionError` | `average_speed(5, 0)` |
> | `RecursionError` | 沒有 base case，或參數沒有朝 base case 前進 |
> | `AssertionError` | 邊界測試沒過，例如 `<= 30` 改成 `< 30` |
>
> 沒有錯誤訊息、結果卻錯的 logic error 也有：`bad_speed()` 偷用全域的 45 分鐘、`add_one(x)` 沒接住回傳值、return 縮排在迴圈裡。
