---
course: [PROG1]
semester: "115-1"
chapter: ["2"]
tags: [programming, lecture]
source:
  - "Computer_Programming_Deck2_AI_PBL_English.pptx.pdf（Deck 2 投影片）"
  - "Computer_Programming_Deck2_ClassNotes_ZH.pdf（Deck 2 中文補充講義）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W4：Deck 2 How Can a Program Represent the Real World? 投影片（English）與中文補充講義融合，依 inquiry ladder（Q1–Q6）排列。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答；其餘內容都來自投影片與講義。輸出一律收在 `[!solution]-` 裡：先預測，再展開。
> 兩份期中考古題與解答在 [[PROG1 Midterm 考古題]]。
> 上一個：[[PROG1 Deck 1 整理]]｜下一個：[[PROG1 Deck 3 整理]]

## Deck 2：程式如何表示真實世界

對應投影片：Deck 2｜1–4。

> [!question] Driving question
> How can a program represent the real world?
>
> Values, types, variables, expressions — and specifications that AI can follow.

**Bridge from Deck 1**：Today we keep the same project and make its data model explicit.

```python
km = float(input("Distance in km: "))
miles = km * 0.621371
print("Distance in miles:", miles)
```

What changes today? A route label. A duration. Clear units. A readable report. We will explain every input, conversion, assignment, and calculation. Keep `main.py`; build `trip_summary.py` in the existing `student-utility-toolkit` repository.

**Driving problem：The user does not ask for "variables". The user asks for an answer.**

> "My route is 12.5 km and takes 45 minutes. Show its name, distance in miles, and average speed in km/h."

| Input | Expected report |
| --- | --- |
| Route: Campus to station | Campus to station |
| Distance: 12.5 km | Distance: 7.77 miles |
| Duration: 45 min | Average speed: 16.67 km/h |

A correct-looking number is not enough. Its meaning and unit must also be correct.

Inquiry ladder：Q1 What information does the problem need? Q2 Why do values need types? Q3 How do names refer to data? Q4 How do input and conversion work? Q5 How do we turn relationships into expressions? Q6 How can AI help us implement and verify our model? Along the way: bits → bytes → fixed-width integers → two's complement.

講義的閱讀方法：先預測，再執行，最後解釋差異。標示「片段」的程式必須放進所說明的上下文；標示「故意錯誤」的範例不是可直接採用的解答。

## D2-Q1 問題需要哪些資訊

對應投影片：Deck 2｜1–9。

單獨看見 12.5，我們不知道它是公里、英里、分鐘還是價格；45 分鐘和 45 小時雖然使用同一個數字，代表的行程完全不同。程式不會因為變數叫做 `time`，就自動知道它的單位；**單位必須由規格與公式共同維持**。A number without a role or unit is ambiguous. Our first deliverable is a data contract, not a Python file.

版本 0.2 的 data contract（Assumptions for version 0.2 — validation code comes in Deck 3）：

| 資料 | Python 名稱與型態 | 版本 0.2 的約定 |
| --- | --- | --- |
| 路線標籤 | `route_name: str` | 非空文字；原樣保留（keep the label unchanged）。 |
| 距離 | `distance_km: float` | 有限且非負的公里數；可以有小數。 |
| 經過時間 | `duration_min: int` | 正整數分鐘（positive whole number of elapsed minutes）。 |
| 報告 | `miles`, `speed_kmh` | 顯示到小數點後兩位，並標示單位。 |

Course conversion rule：miles = kilometers × 0.621371（an approximation，課程採用的近似換算係數，不是聲稱精確到所有位數的物理常數）。

> [!definition] 定義：約定（contract）
> 使用者提供什麼，程式承諾產生什麼，以及承諾成立的條件。Deck 2 假設輸入符合約定，尚未寫出拒絕錯誤資料的判斷；這不是宣稱程式已經能處理所有輸入，Deck 3 才會把部分假設變成會執行的檢查。

> [!note] 核心觀念
> 「規格寫著時間必須大於零」和「程式真的檢查時間是否大於零」是兩件事。先清楚記錄限制，比把尚未實作的能力寫成已完成更重要。

**先手算一個答案，再寫程式**（An expected answer must not come only from the program under test）：

$$
\begin{aligned}
\text{miles} &= 12.5 \times 0.621371 = 7.7671375 \\
\text{hours} &= 45 / 60 = 0.75 \\
\text{speed} &= 12.5 / 0.75 = 16.666\ldots\ \text{km/h}
\end{aligned}
$$

預期顯示值是 **7.77 miles** 和 **16.67 km/h**。程式還不存在，我們已經知道一個應該得到的答案。

> [!definition] 定義：Test oracle（測試的判定依據）
> 獨立答案稱為 test oracle：它來自需求與手算，而不是把待測程式的輸出抄回「正確答案」欄。先寫下預期值，再執行程式；不一致時才有真正需要調查的證據。

> [!question] Quick challenge：is the specification complete?
> A vague request：「The distance is 3 and the time is 30. Calculate the speed.」Your repair：add the units, state the allowed duration, give one expected output. Now use 3 km in 30 min. What should the speed be, in km/h?

> [!solution]- 答案
> 缺單位。補成 3 公里、30 分鐘、要求 km/h 後，答案是 **6 km/h**，而不是 0.1 km/h。

**AI 也需要同一份規格**：先要求 AI 列出輸入名稱、型態、單位、允許值、公式和兩個手算測試，而不是立即產生程式。

> [!example] 提示範本：Specify before generating（live output will vary）
> ```text
> Do not write code yet.
> Plan a console trip-summary tool.
> Inputs: route label, distance in km,
>       duration in positive whole minutes.
> Outputs: miles and average speed in km/h.
> Use 0.621371 miles per km; display 2 decimals.
> List names, types, units, assumptions,
> formulas, and two independently worked tests.
> ```
> Human review：Are the units right? Is zero time allowed? Is anything invented?

學生仍須確認：AI 是否改了單位？是否把整數分鐘改成任意小數？是否自行加入選單或功能？方便的功能不等於這一次需要的功能。Agree on the contract before generating candidate code.

## D2-Q2 為什麼資料需要型態

對應投影片：Deck 2｜10–14。

Representation determines which operations make sense. A Python value has a type. The type affects valid operations.

| `int` | `float` | `str` |
| --- | --- | --- |
| A whole-number value | A floating-point value（有限精度） | A text value |
| `45`：duration in whole minutes | `12.5`：distance in kilometers | `"Campus to station"`：a route label |

`bool` will support decisions in Deck 3. **Python 沒有另外一個 char 型態**；單一字元 `"A"` 也是字串。

同一個 `+`，不同運算（表見 [[PROG1 Deck 1 整理#D1-Q3 電腦如何表示資訊|D1-Q3 電腦如何表示資訊]]）：`65 + 1` → `66`；`65.0 + 1` → `66.0`；`"65" + "1"` → `"651"`；`"65" + 1` → `TypeError`（No implicit number-to-text conversion here）。第三列不是算錯，Python 正確執行了字串串接；第四列是不支援這組型態的加法。若目標是算術，寫 `int("65") + 1`；若目標是文字串接，寫 `"65" + str(1)`。**先決定資料的意思，再決定如何轉型。**

> [!example] 範例：Printing a value can hide its type
> ```python
> a = 65
> b = "65"
> print(a)
> print(b)
> print(type(a))
> print(type(b))
> ```

> [!solution]- 輸出
> ```text
> 65
> 65
> <class 'int'>
> <class 'str'>
> ```
> `print()` 顯示文字時，通常不把字串外面的引號印出來，所以兩個 65 不能證明型態相同。`type()` 是檢查目前資料型態的工具；除錯時不只問「值是多少」，還要問「這個值是哪一種型態」。Identical-looking output does not prove identical data types.

> [!example] 範例：Digits do not always mean "a quantity"
> ```python
> route_id = "007"
> print(route_id)
> print(int(route_id))
> ```

> [!solution]- 輸出
> ```text
> 007
> 7
> ```
> 路線編號 007 的前導零可能是名稱的一部分。轉成整數雖然成功，卻遺失這個拼寫。這是**資料模型錯誤**，不是語法錯誤：程式合法、轉型成功，仍然可能不符合需求。A route identifier is a label, not something we add or average. 相對地，距離要做除法與換算，使用數值型態才符合它的角色。

> [!note] 核心觀念
> 型態的選擇取決於資料要表示什麼，而不只是輸入看起來像什麼。這裡也沒有聲稱 Python 的 `65`、`65.0` 和 `"65"` 具有相同的記憶體位元。

## D2-Q3 變數名稱如何指向資料

對應投影片：Deck 2｜15–20。

> [!definition] 定義：名稱綁定到物件
> A variable name is bound to an object. The object has a type and a value. A name gives us a readable way to refer to it.
> 可以先把變數名稱想成貼在資料旁的標籤。這個比喻是理解程式語意，不是在規定物件必須放在哪個實體記憶體位址；For this lesson, focus on names and values — not memory addresses.

**Assignment：evaluate the right, then bind the left.** 指派是動作，不是永久成立的等式。

```python
distance_km = 10 + 2.5
```

Python 先計算右邊 `10 + 2.5`，得到浮點數 `12.5`，再讓左邊的名稱 `distance_km` 指向這個結果。這行是 assignment statement（指派敘述），**不是一個會回傳 None 的運算式**。

> [!example] 範例：`x = x + 1` is an update, not an equation
> ```python
> x = 4
> x = x + 1
> print(x)
> ```

> [!solution]- 輸出
> ```text
> 5
> ```
> 在數學等式中，`x = x + 1` 不成立；在 Python 中，它的意思是「讀取舊的 x（4）、加 1（5）、把名稱 x 綁定到新結果」。A program describes actions that happen in time. 若 x 之前完全沒有被綁定，右邊讀取 x 就會產生 `NameError`。

`=` assigns. `==` asks about equality; we study Boolean decisions in Deck 3.

> [!example] 範例：Rebinding one name does not update another
> ```python
> a = 10
> b = a
> a = 20
> print(a, b)
> ```

> [!solution]- 輸出
> ```text
> 20 10
> ```
> | 執行後 | a 指向 | b 指向 |
> | --- | --- | --- |
> | `a = 10` | 10 | 尚未綁定 |
> | `b = a` | 10 | 10 |
> | `a = 20` | 20 | 10 |
>
> `b = a` 使用的是當時 a 指向的物件，不是建立「b 永遠追蹤 a」的連線（not a live link; an arrow means "refers to", not a spreadsheet formula）。也不要把這解釋成「每次指派一定複製一個物件」；名稱綁定和物件複製是不同的概念。

> [!question] Trace challenge：predict the stale result
> Write a value table before you run this program. Does `miles` change when `distance_km` changes? Which line must run again?
> ```python
> distance_km = 10
> miles = distance_km * 0.621371
> distance_km = 20
> print(distance_km)
> print(miles)
> ```

> [!solution]- 輸出
> ```text
> 20
> 6.21371
> ```
> `miles` 保存的是第一次計算得到的值，不是會自動重新計算的公式。要得到 20 公里對應的英里數，必須在更新距離後再執行一次 `miles = distance_km * 0.621371`，補算後為 `12.42742`。Assignment stores a computed result; it does not keep recalculating the expression.

**Names should carry meaning and units**：

| Less clear | More clear | Why it helps |
| --- | --- | --- |
| `d` | `distance_km` | Quantity and unit are visible. |
| `t` | `duration_min` | Elapsed time; minutes rather than hours. |
| `0.621371` | `MILES_PER_KM` | The conversion rule has a name. |
| `60` | `MINUTES_PER_HOUR` | The unit conversion is explicit. |

- 名稱區分大小寫（case-sensitive）。大寫常數是命名慣例，不代表 Python 禁止重新指派（not enforced immutability）。
- 本課使用小寫加底線的 snake_case 名稱。名稱不可有空格、不可用數字開頭，也不要使用保留字。
- 避免把 `input`、`float` 或 `str` 當作自己的變數名稱，否則可能蓋掉稍後需要呼叫的內建名稱。

## D2-Q4 輸入與轉型如何運作

對應投影片：Deck 2｜21–26。

Typing 45 does not automatically create an int. `input()` reads a line and returns a string. We decide how that text should be interpreted：**Read → convert → bind → use.**

> [!example] 範例：Why does "3 + 5" become "35"?（依序輸入 3 與 5）
> ```python
> a = input("First number: ")
> b = input("Second number: ")
> print(a + b)
> ```

> [!solution]- 輸出
> ```text
> 35
> ```
> 按下 Enter 只是結束這次輸入；`input()` 回傳的是**不含最後換行符號的字串**。輸入 3 與 5 後，a 與 b 分別指向 `"3"`、`"5"`，加號執行的是串接。這不是 input 壞了，而是我們還沒把文字解讀成數字。Diagnose before editing.

Conversion is an operation with rules — some inputs convert cleanly; others fail or lose information：

| 轉型 | 結果 | 要記住的事 |
| --- | --- | --- |
| `int("45")` | `45` | 整數文字可以解析成 int。 |
| `float("12.5")` | `12.5` | 距離可以保留小數。 |
| `str(12.5)` | `"12.5"` | 產生文字表示。 |
| `int(12.9)` | `12` | Float → int **向零截斷**，不是四捨五入。 |
| `int("12.5")` | `ValueError` | 這段文字不是 int() 能解析的整數格式。 |

最後兩列不同：`int(12.9)` 收到一個已存在的浮點數；`int("12.5")` 收到文字。不要為了讓後者不報錯，隨意改成 `int(float(text))`。如果規格要求整數分鐘，把 45.5 默默改成 45，等於改變資料，而不是單純修復語法。

> [!example] 範例：Build the input stage one field at a time（輸入 Campus to station、12.5、45）
> ```python
> route_name = input("Route label: ")
> distance_km = float(input("Distance in km: "))
> duration_min = int(input("Duration in minutes: "))
>
> print(type(route_name))
> print(type(distance_km))
> print(type(duration_min))
> ```

> [!solution]- 輸出
> ```text
> <class 'str'>
> <class 'float'>
> <class 'int'>
> ```
> 讀 `float(input(...))` 時由內往外想：input 先讀到 `"12.5"`，float 再解析成 `12.5`，最後指派給 `distance_km`。`print(type(...))` 是診斷用的輸出，正式報告不需要保留這三行。Name, type, and unit should match the written contract.

**Conversion is not validation**（A successfully parsed number may still violate the problem specification）：

| Text → numeric value | Value → valid input? |
| --- | --- |
| `int("0")` succeeds. | Zero duration is not allowed. |
| `float("-3.5")` succeeds. | Negative distance is not allowed. |

> [!note] 核心觀念
> 轉型問的是「能否成為指定型態？」；驗證問的是「這個值是否符合問題規則？」`int("0")` 可以成功，但零分鐘仍違反本版的輸入約定。Version 0.2 assumes valid input and documents that limitation; Deck 3 will add decisions that reject invalid values.

> [!question] Mini-lab：make the inputs visible（6 minutes）
> Use the project folder from Deck 1. No new repository.
> 1. Create `trip_summary.py` alongside `main.py`.
> 2. Read the route label, distance in km, and whole minutes.
> 3. Print each value and its type. Save and run the file.
> 4. Try a decimal distance. Predict what happens with duration `"45.5"`.
>
> Use Run Python File in Terminal, or `python trip_summary.py` from the project folder（依環境可能改用 `python3` 或 `py`）。不要把 shell 指令打進 `>>>`。

> [!solution]- 執行結果（Claude 執行）：duration 輸入 45.5
> ```text
> ValueError: invalid literal for int() with base 10: '45.5'
> ```
> 小數距離沒問題（`float`），但 `int("45.5")` 解析失敗，程式在第三個 input 就停下。

## D2-Q5 如何把數量關係寫成運算式

對應投影片：Deck 2｜27–35。

Average speed = distance ÷ duration. Distance arrives in kilometers; duration arrives in minutes; the report asks for kilometers per hour. **The unit conversion is part of the algorithm, not just an output label.**

$$
\text{duration (h)} = \frac{\text{duration (min)}}{60}, \qquad \text{speed (km/h)} = \frac{\text{distance (km)}}{\text{duration (h)}}
$$

Use the operators the problem actually needs（a compact toolkit, not a memorization exercise）：

| Purpose | Python expression | Result |
| --- | --- | --- |
| Combine quantities | `10 + 2.5` | `12.5` |
| Convert km → miles | `12.5 * 0.621371` | ≈ `7.7671375` |
| Convert min → hours | `45 / 60` | `0.75` |
| Square a value | `3 ** 2` | `9` |
| Whole units / remainder | `83 // 60`、`83 % 60` | 1 hour / 23 minutes |

> [!failure] 故意錯誤的範例：This program runs — and still answers the wrong question
> Prepared teaching bug: the printed unit does not match the calculation. Expected: 60.0 km/h.
> ```python
> distance_km = 60
> duration_min = 60
> speed = distance_km / duration_min
> print(speed, "km/h")
> ```

> [!solution]- 輸出與分析
> ```text
> 1.0 km/h
> ```
> 它實際算的是公里／分鐘，也就是 1 km/min。後面印出 km/h 並不會改變已經算出的數字：`distance_km / duration_min` has units km/min. A label cannot change those units. 用 60 公里花一小時這個容易手算的例子，就能發現答案應為 60 km/h。修正方式是先把分鐘換成小時，再做除法。

> [!example] 片段：Translate the model into named steps（distance_km 與 duration_min 已取得）
> ```python
> MILES_PER_KM = 0.621371
> MINUTES_PER_HOUR = 60
>
> miles = distance_km * MILES_PER_KM
> duration_h = duration_min / MINUTES_PER_HOUR
> speed_kmh = distance_km / duration_h
> ```

同一個速度公式也可寫成 `distance_km / (duration_min / 60)`。括號表示整個分鐘轉小時的結果才是除數。**不要寫成 `distance_km / duration_min / 60`**：那是先除以分鐘，再除以 60，方向相反。中間名稱通常比讓讀者猜括號更容易維護。

**除法、整除、餘數與次方**（"/" and "//" answer different questions）：

> [!example] 範例
> ```python
> print(45 / 60)
> print(45 // 60)
> print(83 // 60)
> print(83 % 60)
> print(3 ** 2)
> ```

> [!solution]- 輸出
> ```text
> 0.75
> 0
> 1
> 23
> 9
> ```
> `/` 保留比例；`//` 做 floor division。對這裡的非負整數而言，`83 // 60` 是完整的 1 小時，`83 % 60` 是剩下的 23 分鐘。但 45 分鐘換成小時要用 `45 / 60`；若用 `//`，結果變成零，後面的速度除法就可能除以零。Use division for proportions; use floor division for whole groups.

Python 用 `**` 表示次方，**不是 `^`**。對本課的一般算術，乘除優先於加減；有疑慮就使用括號。更細的次方結合方向與負數整除規則在 [[#D2 選讀：容易混淆的精確規則]]，不要用「所有運算子都由左到右」取代真正的語法規則。

> [!warning] Claude 提醒：`^` 在 Python 是 XOR
> 考古題 A3 有 `a^10`、`a|b`，B3 有 `a<<10`、`a^b`：這些是位元運算，`1^10` 得 11，不是 1 的 10 次方。新講義只在 [[PROG1 Deck 3 整理#D3-Q2 多個條件如何一起工作|D3-Q2 多個條件如何一起工作]] 提到 `&`、`|`、`~` 是位元運算，`^`、`<<` 整理在 [[PROG1 Midterm 考古題#新講義沒教的舊考點|新講義沒教的舊考點]]。

**顯示格式和計算值要分開**：f-string 開頭的 `f` 表示大括號中的運算式要被求值。

> [!example] 範例：Format the report for a human reader
> ```python
> miles = 12.5 * 0.621371
> print(f"Distance: {miles:.2f} miles")
> print(miles)
> ```

> [!solution]- 輸出
> ```text
> Distance: 7.77 miles
> 7.7671375000000005
> ```
> `{miles:.2f}` 把數值格式化成固定小數點、兩位小數的文字（`f` = formatted string，`{miles}` = value to insert，`:.2f` = 2 decimal places）。這不會把 `miles` 本身改成 7.77；後續計算仍使用原本的數值。Formatting changes the displayed text; it does not rebind or round the stored value. 報告需要兩位小數，不代表每一步中間結果都應先被四捨五入。

> [!example] 範例：Why can a float display an unexpected decimal?
> ```python
> total = 0.1 + 0.2
> print(total)
> print(f"{total:.2f}")
> ```

> [!solution]- 輸出
> ```text
> 0.30000000000000004
> 0.30
> ```
> 許多十進位小數只能以二進位浮點數近似表示，因此可能看見額外的尾數。並非每個小數都如此，例如 0.5 可以精確表示。Keep intermediate values; format only when producing the report. 格式化是讓報告符合顯示約定，不是把浮點數變成任意精度的十進位算術。

> [!example] 範例：完整的 Trip Summary v0.2（`trip_summary.py`，VALID INPUTS ASSUMED）
> ```python
> # Assumption: all inputs satisfy the Deck 2 contract.
> MILES_PER_KM = 0.621371
> MINUTES_PER_HOUR = 60
>
> route_name = input("Route label: ")
> distance_km = float(input("Distance in km: "))
> duration_min = int(input("Duration in minutes: "))
>
> miles = distance_km * MILES_PER_KM
> duration_h = duration_min / MINUTES_PER_HOUR
> speed_kmh = distance_km / duration_h
>
> print(f"Route: {route_name}")
> print(f"Distance: {miles:.2f} miles")
> print(f"Average speed: {speed_kmh:.2f} km/h")
> ```

> [!solution]- 執行結果（Claude 執行）
> ```text
> Route label: Campus to station
> Distance in km: 12.5
> Duration in minutes: 45
> Route: Campus to station
> Distance: 7.77 miles
> Average speed: 16.67 km/h
> ```

先看三段責任：**取得資料、計算衍生值、顯示報告**。程式沒有迴圈、函式定義或錯誤處理；在本版的有效輸入假設下，它已是一個完整的小工具。零時間與無法解析的文字屬於限制，不應把它們寫成「已通過驗證」。

**Guided lab：change one input, predict one consequence**（Do not ask AI for the prediction. Work from the quantities）：

| 公里／分鐘 | 英里顯示值 | 速度顯示值 | 關係 |
| --- | --- | --- | --- |
| 12.5 / 45 | 7.77 | 16.67 | 原始案例 |
| 12.5 / 90 | 7.77 | 8.33 | 時間加倍，速度減半。 |
| 25 / 90 | 15.53 | 16.67 | 距離再加倍，速度再加倍。 |

這些是成對的關係測試：只改一個輸入，預測什麼會改、什麼不會改。顯示值經過捨入，不必要求兩個已格式化的字串仍符合精確的倍數關係；關係是針對計算模型的未格式化數值。A useful test checks relationships between cases, not only one plausible-looking output.

## D2 電腦基礎：位元如何表示整數

對應投影片：Deck 2｜36–40、58。

一個 bit 有兩種狀態；**一個 byte 包含 8 bits**。以 8 位元無號整數為例，從左到右的權重為 128、64、32、16、8、4、2、1；位元是 1 就加入該位置的權重，是 0 就不加入。

```text
Weights: 128 64 32 16  8  4  2  1
Bits:      0  0  0  0  1  1  0  1

00001101 = 8 + 4 + 1 = 13
```

這是位置權重示意，不是 Python int 的完整記憶體內容。反過來，要把 13 編成二進位：先選不超過 13 的最大權重 8，剩下 5；再選 4，剩下 1；最後選 1。To decode: add the selected place values.

**有幾種圖樣，和最大值是多少，不一樣**（Fixed width means a limited number of patterns）：

$$
n \text{ bits} \implies 2^{n} \text{ patterns}; \qquad 0 \le x \le 2^{n} - 1 \ \ (\text{unsigned})
$$

| 寬度 | 圖樣數 | 無號範圍 |
| --- | --- | --- |
| 8 bits = 1 byte | $2^{8} = 256$ | 0 to 255 |
| 16 bits = 2 bytes | $2^{16} = 65{,}536$ | 0 to 65,535 |
| n bits | $2^{n}$ | 0 to $2^{n} - 1$ |

8 位元有 256 種圖樣，但因為第一個值是零，最大值是 255；16 位元有 65,536 種圖樣，65,535 才是最大無號值。若某種檔案或硬體欄位要求固定寬度，超出範圍要如何處理必須另外指定，不能猜測一定會怎麼溢位。

**二補數（two's complement）：同一組位元的有號解讀。** How do 8 bits encode −5? Invert the fixed-width representation of +5, then add 1：

| Step | 8-bit pattern | Interpretation |
| --- | --- | --- |
| Start with +5 | `00000101` | 4 + 1 |
| Invert each bit | `11111010` | Still working with exactly 8 bits |
| Add 1 | `11111011` | The 8-bit two's-complement encoding of −5 |

Signed check：$-128 + 64 + 32 + 16 + 8 + 2 + 1 = -5$。

二補數不是單純把最左邊當成獨立的正負號。以 8 位元來看，**最高位的權重是 −128**，其餘位仍是 64 到 1。因此 `11111011` 可解成 −5；若改用無號規則解讀，它卻是 251。

$$
-2^{n-1} \le x \le 2^{n-1} - 1 \quad (\text{two's complement})
$$

| `11111011` 用哪種規則讀 | 結果 | 範圍 |
| --- | --- | --- |
| 8-bit unsigned | 251 | 0 to 255 |
| 8-bit two's complement | −5 | −128 to 127 |
| Python int | `127 + 1` gives `128` | 不是固定 8 位元欄位 |

Python 的一般 int 具有受資源限制的任意精度（arbitrary precision, limited by resources）；不能把固定欄位的範圍直接套成 Python 整數的最大值，do not assume 8-bit wraparound。**Always name the width and the encoding.**

> [!question] Foundation checkpoint：decode, encode, distinguish
> Two minutes without Python or AI; explain your answer.
> 1. Write decimal 31 as an 8-bit unsigned binary pattern.
> 2. Interpret `10000000` as unsigned, then as 8-bit two's complement.
> 3. What does Python print for `127 + 1`? Why is that a different question?

> [!solution]- Appendix D：worked answers
> | Question | Answer | Reason |
> | --- | --- | --- |
> | Encode 13, unsigned 8-bit | `00001101` | 8 + 4 + 1 |
> | Encode −5, signed 8-bit | `11111011` | Invert `00000101`; add 1. |
> | Encode 31, unsigned 8-bit | `00011111` | 16 + 8 + 4 + 2 + 1 |
> | `10000000` | 128 or −128 | Unsigned or two's complement |
> | Python: `127 + 1` | 128 | Python int is not fixed 8-bit storage. |

> [!warning] Claude 提醒：考古題的 byte 與位元是非題
> 考古題 A 1(k)「A one byte data means that it is stored using 8 bits」是 T；A 1(l)「Any number stored in a computer can be represented using 8 bits without information loss」與 B 1(j)「Any number stored in a computer uses 8 bits」都是 F：8 bits 只有 256 種圖樣，而且 Python int 不是固定寬度。

## D2-Q6 如何用 AI 實作並驗證資料模型

對應投影片：Deck 2｜41–51。

Human decisions first; candidate code second. We now have a contract and an expected answer. Ask AI to implement that model, then check whether its code preserves the names, units, allowed inputs, and required outputs. A plausible implementation is a candidate — not evidence of correctness.

這一階段可以請 AI 產生候選程式，但限制在已學過的 `input`、`int`、`float`、`print`、指派、算術與 f-string。不要讓一個小工具突然變成需要套件、網站伺服器、選單或多個函式的專案；可以執行不代表學生已經能理解。

> [!example] 提示範本：Contract → candidate（不是一段真實 AI 對話紀錄）
> ```text
> Implement the approved trip-summary contract.
> Use the names, units, and constants from the spec.
> Use input(), int(), float(), print(), arithmetic,
> assignments, and f-strings only.
> One console script; no loops, user-defined functions,
> packages, file I/O, network calls, or validation yet.
> State the valid-input assumptions as comments.
> Explain the unit of each intermediate quantity.
> ```
> Review scope creep. Extra menus, exception handlers, and packages are not today's deliverable.

> [!failure] 故意錯誤的範例：three contract violations, the script can still run
> Prepared faulty teaching example — not a recorded AI response. Inspect fractional distance, conversion direction, and preservation of the route label.
> ```python
> route_name = input("Route label: ")
> distance_km = int(float(input("Distance in km: ")))
> duration_min = int(input("Duration in minutes: "))
>
> miles = distance_km / 0.621371
> speed_kmh = distance_km / (duration_min / 60)
> print(f"Distance: {miles:.2f} miles")
> print(f"Average speed: {speed_kmh:.2f} km/h")
> ```

> [!solution]- 講義的分析：輸入標籤 007、距離 3.5、時間 30
> ```text
> Distance: 4.83 miles
> Average speed: 6.00 km/h
> ```
> 1. 3.5 被截成 3，速度變成 6.00 而不是 7.00。
> 2. 公里轉英里應乘上係數，這裡卻做除法，得到錯誤的 4.83（應為 2.17）。
> 3. 讀了 `route_name` 卻從未印出，遺漏了需求。
>
> | Violation | Minimal repair | Evidence to recheck |
> | --- | --- | --- |
> | Fraction discarded | `float(input(...))` | 3.5 km remains 3.5, not 3. |
> | Conversion reversed | `distance_km * MILES_PER_KM` | 3.5 km displays 2.17 miles. |
> | Label omitted | `print(f"Route: {route_name}")` | Route label 007 still displays 007. |
>
> 每改一項就重跑相關測試，才能知道是哪個改動解決了哪個問題。A diff is more informative than an unexplained replacement script. **不要為了讓錯誤程式通過，把預期速度改成 6.00。**

**Use independent tests, not "it seems reasonable"**（Compute expected values from the contract before running either implementation）：

| 案例 | 輸入 km / min | 預期 miles / km/h | 檢查重點 |
| --- | --- | --- | --- |
| Campus / typical | 12.5 / 45 | 7.77 / 16.67 | 一般案例與時間單位。 |
| Stationary / zero distance | 0 / 30 | 0.00 / 0.00 | 零距離有效。 |
| One hour / easy oracle | 60 / 60 | 37.28 / 60.00 | 容易手算的速度。 |
| 007 / fractional distance | 3.5 / 30 | 2.17 / 7.00 | 保留小數與標籤零。 |

每個案例都應記錄預期結果、實際結果與判斷理由（pass/fail，不是只寫 "tested"），並檢查標籤是否原樣保留。通過四個測試代表這四個案例已有證據，不代表證明所有可能輸入都正確；無法解析的文字和零時間，另列為目前未支援的輸入。

**A controlled workflow, not a giant "write my project" prompt**：Specify → Predict → Generate → Inspect → Run tests → Revise。

| Human decisions | AI assistance |
| --- | --- |
| Meaning, units, input domain, expected outputs, and whether the implementation satisfies them. | Candidate code, explanations, test suggestions, and a small, reviewable patch. |

Keep a short sanitized AI-use note: what you asked, what you accepted, and what you verified.

> [!question] Build task：build your next toolkit version（12 minutes）
> 1. Finish `trip_summary.py` under the written valid-input contract.
> 2. Pass the four report tests; record expected and actual outputs.
> 3. Add one field: distance in meters OR duration in hours.
> 4. Write your expected value before running the new feature.

> [!solution]- 新欄位的預期值
> 12.5 km / 45 min：**12,500.00 m** 或 **0.75 h**。先寫下新預期值，再新增運算與輸出；不要順便重寫整個程式。

Can you defend the result?

1. Meaning：Can you name each input's type, unit, and permitted values?
2. Execution：Can you explain why `duration_min / 60` is needed before the speed calculation?
3. Verification：Can you show expected and actual output for a fractional and a zero-distance case?
4. Ownership：Can you explain one change you made and how you checked it?

**Push a tested change, not a second repository**（繼續使用 Deck 1 的 GitHub Desktop workflow）：

1. Keep `main.py`; add `trip_summary.py` and the Deck 2 evidence files（規格、測試、AI 使用簡記與執行方式）.
2. Run the saved script. In Desktop, inspect the Changes／diff view.
3. Commit：`Add tested trip summary with explicit units`.
4. Push origin. View on GitHub and verify the latest commit and files.

Never upload tokens, private data, or unreviewed AI transcripts. AI 使用簡記可以只包含：問了什麼、採用哪些部分、自己改了什麼、如何測試。如果出現同步問題，**不要把 force push 當成預設修法**。Save、commit、push 分別保存檔案、版本與遠端分享的版本；成功 push 不會替你證明計算正確。

A project begins with a quantity worth computing — choose a small problem you actually care about：

| Printing-cost estimator | Study-time planner | Energy-use estimator |
| --- | --- | --- |
| Inputs: page count, cost per page. | Inputs: pages, minutes per page. | Inputs: watts, hours of use. |
| Model: total = pages × unit price. | Model: hours = pages × rate / 60. | Model: kWh = watts × hours / 1000. |
| Check: 10 × 2.5 = 25. | Check: 20 × 3 / 60 = 1 h. | Check: 100 × 2 / 1000 = 0.2. |

Start with one computation, explicit units, and one hand-worked test. Add features later.

Representing the world means preserving meaning throughout the program：

1. Q1 Specify inputs, outputs, assumptions, and units.
2. Q2 Choose types that preserve the data's meaning.
3. Q3 Bind meaningful names; trace changes over time.
4. Q4 Parse input text deliberately, without silently losing information.
5. Q5 Implement relationships and unit conversions as expressions.
6. Q6 Use AI for candidate work; keep independent verification.

Human responsibility today: define the data model and verify that the code preserves it. Next: what should happen when an input is invalid? Our contract says "Duration must be positive." What should the program do with 0 minutes? → Deck 3（comparisons → Boolean conditions → `if`／`elif`／`else` → boundary tests）。

## D2 Exit Ticket 與複習練習

對應投影片：Deck 2｜9、19、35、40、47、52–54、58。

> [!question] 先自行作答（explain without running the code）
> 1. 為什麼路線 ID `"007"` 應保留為 str？請說明「轉型成功」仍可能有什麼問題。
> 2. 執行 `a = 5; b = a; a = 8` 後，b 是多少？這和試算表公式有何不同？
> 3. 若輸入 12.5 km、45 min，為何 `distance_km / duration_min` 不能標示為 km/h？
> 4. 分別預測 `45 / 60`、`45 // 60`、`83 % 60`。哪一個可用於計算平均速度所需的時間？
> 5. 距離保持 12.5 km，時間從 45 min 改為 90 min。英里與速度各有什麼變化？
> 6. 把 13、31 編成 8 位元無號圖樣；把 −5 編成 8 位元二補數；解讀 `10000000`。
> 7. `int("0")` 成功，能否因此宣稱本版工具支援零時間？
> 8. 想做讀書時間估算器：20 頁、每頁 3 分鐘。請寫出輸入單位、公式及小時數的獨立預期值。

> [!solution]- 解答與理由
> 1. 因為它是識別名稱，不是要加總的量。int 會把 007 變成 7，遺失名稱需要的前導零。
> 2. b 仍指向 5。指派使用當下的物件，不會讓 b 自動追蹤 a 之後的重新綁定。
> 3. 該商的單位是 km/min。應先算 45/60 = 0.75 小時，再算 12.5/0.75；顯示為 16.67 km/h。
> 4. 依序是 0.75、0、23。速度公式需要 `/` 保留不足一小時的部分；餘數可用來另做「幾小時幾分鐘」的表示。
> 5. 英里仍為 7.77，速度顯示為 8.33。未格式化的速度減半；報告只顯示兩位小數。
> 6. 13：`00001101`；31：`00011111`；−5：`11111011`。`10000000` 是無號 128 或二補數 −128。Python 的 `127 + 1` 則是 128，不適用 8 位元上限。
> 7. 不行。轉型只決定型態能否建立；零時間仍違反正分鐘的模型，後續也可能除以零。
> 8. 頁數 × 分鐘／頁 = 分鐘；再除以 60 得小時。20 × 3 / 60 = 1 小時。這是課程中的假設案例，不是對實際讀書速度的保證。

## D2 選讀：容易混淆的精確規則

對應投影片：Deck 2｜55–57、59–60。

**Truncation, floor, ceiling, and round** — these operations express different policies. Pick the policy before the function.

| 運算式 | 結果 | 規則 |
| --- | --- | --- |
| `int(-1.7)` | `-1` | 向零截斷（truncate toward zero）。 |
| `math.floor(-1.7)` | `-2` | 不大於原值的最大整數。 |
| `math.ceil(-1.7)` | `-1` | 不小於原值的最小整數。 |
| `round(2.5), round(3.5)` | `2, 4` | 精確中間值採靠偶數的捨入（tie to even）。 |

使用 `floor`、`ceil` 前需 `import math`。`int("1.7")` is not the same as `int(1.7)`。floor 與截斷對負數不一樣，例如 `-7 // 3` 是 `-3`，而 `int(-7 / 3)` 是 `-2`：這是「往下」和「往零」的差異。

> [!example] 範例：precedence and updating a numeric variable
> ```python
> print(2 ** 3 ** 2)
> print(-3 ** 2)
> print((-3) ** 2)
>
> distance_km = 10.0
> distance_km += 2.5
> print(distance_km)
> ```

> [!solution]- 輸出
> ```text
> 512
> -9
> 9
> 12.5
> ```
> 第一行分組為 `2 ** (3 ** 2)`，不是 `(2 ** 3) ** 2`：`**` associates right-to-left。第二行是對 3 的平方取負，第三行才是把 −3 當作底數平方。寫出括號比背誦「由左到右」可靠。For these numbers, `x += y` updates x using `x + y`.

> [!example] 範例：display, result, and statement are different
> ```python
> result = print("Hello")
> print(result)
> value = 12.345
> label = f"{value:.2f}"
> print(label)
> print(type(label))
> ```

> [!solution]- 輸出
> ```text
> Hello
> None
> 12.35
> <class 'str'>
> ```
> 第一個 Hello 是 print 的顯示效果；`result` 收到的是該函式呼叫的回傳值 `None`。`print()` returns `None`. An assignment statement has no expression result; it does not "return None." f-string 的結果是字串，所以 `label` 不是已經被四捨五入的數值變數。

> [!warning] Claude 提醒：`print()` 回傳 None 是考古題必考
> 考古題 A2 `print(print(a*b,end=""),end = ".")` 與 B2 `print(print(a+b,end=""),end = ".")` 都在考這一點：內層 `print` 先印出內容，回傳 `None`，外層再把 `None` 印出來。答案分別是 `33333None.` 與 `35None.`；`end=` 的用法見 [[PROG1 Midterm 考古題#新講義沒教的舊考點|新講義沒教的舊考點]]。

投影片所列的延伸閱讀：Python tutorial: an informal introduction；Python: built-in functions；Python: assignments and simple statements；Python: floating-point arithmetic；MIT OCW 6.004: information encoding。Corrections carried forward（Appendix E）：names bind to objects; value ≠ raw bits; no separate char type; assignment does not return None; correct integer ranges; exponentiation is right-associative.
