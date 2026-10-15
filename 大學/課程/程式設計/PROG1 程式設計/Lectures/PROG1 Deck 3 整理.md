---
course: [PROG1]
semester: "115-1"
chapter: ["3"]
tags: [programming, lecture]
source:
  - "Computer_Programming_Deck3_AI_PBL_English.pptx.pdf（Deck 3 投影片）"
  - "Computer_Programming_Deck3_ClassNotes_ZH.pdf（Deck 3 中文補充講義）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W6：Deck 3 How Can a Program Make Decisions? 投影片（English）與中文補充講義融合，依 inquiry ladder（Q1–Q6）排列。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答；其餘內容都來自投影片與講義。輸出一律收在 `[!solution]-` 裡：先預測，再展開。
> 兩份期中考古題與解答在 [[PROG1 Midterm 考古題]]。
> 上一個：[[PROG1 Deck 2 整理]]｜下一個：[[PROG1 Deck 4 整理]]

## Deck 3：程式如何做決策

對應投影片：Deck 3｜1–4。

> [!question] Driving question
> How can a program make decisions?
>
> Conditions, branches, and tests that challenge AI-generated code.

**Bridge from Deck 2**：Deck 2 assumed valid inputs. Today the program checks the rules.

```python
distance_km = 12.5
duration_min = 0
duration_h = duration_min / 60
speed_kmh = distance_km / duration_h
```

What happens with zero minutes? The missing choice：calculate a report, or explain why not. **A written assumption is not the same as a check that runs.**

Driving problem：accept valid trip data; reject invalid data before calculating.

| 12.5 km / 45 min | 12.5 km / 0 min |
| --- | --- |
| Route: Campus | Error: duration must be positive. |
| Distance: 7.77 miles | No speed. No report. |
| Average speed: 16.67 km/h | No division by zero. |
| Trip band: Medium | |

Today's added policy：Short ≤ 30 min；Medium ≤ 60 min；Long > 60 min。

Inquiry ladder：01 How can a computer answer a yes/no question? 02 How can several conditions work together? 03 How does a condition choose what runs? 04 What if there are more than two possible outcomes? 05 Why does the order of conditions matter? 06 How can we test decisions, with AI as an assistant? — Build: Trip Summary v0.3 | AI skill: test-case design | Foundations: compare + branch。

## D3-Q1 如何把規則變成是非問題

對應投影片：Deck 3｜1–10。

Deck 2 的工具假設資料有效；如果時間是零，原本的公式就無法完成計算。Deck 3 的新任務不是換一個公式，而是**在計算前做選擇**：資料有效就產生報告，資料無效就說明原因。前一版的限制不等於前一版在自己的規格內失敗；現在增加驗證，是擴充能力。保留 `trip_summary.py`，另外建立 `trip_decisions.py`，這樣就能看見新能力從哪裡加入。Extend the existing contract. Do not silently change the meaning of the inputs.

| 資料／結果 | 版本 0.3 的規則 |
| --- | --- |
| `route_name: str` | 拒絕剛好為空的字串 `""`；其他標籤原樣保留。 |
| `distance_km: float` | 拒絕非有限數（non-finite）與負數；零距離有效。 |
| `duration_min: int` | 必須是已解析成功的正整數分鐘；reject 0 and negative minutes. |
| 無效資料 | 只印出第一個驗證錯誤，不計算、不印行程報告。 |
| 有效資料 | 保留 Deck 2 的三行報告，再加入一個時間分類（duration band）。 |

> [!note] 核心觀念
> 核心版本先假設 float／int 轉換成功，再驗證數值範圍。`"abc"` 之類文字的解析錯誤，與「成功讀到 0，但 0 不被允許」不同；一般解析錯誤的處理放在選讀（optional extension）。

> [!definition] 定義：Condition 與比較運算
> A condition is an expression whose truth value guides a choice. 「時間必須為正」可以寫成 `duration_min > 0`：45 分鐘得到 `True`，0 或 −5 分鐘得到 `False`。對本課使用的內建數字與字串，比較結果是 `bool`；這個值可以被儲存、印出，或交給後面的 `if` 決定要走哪條路。

| 符號 | 問題 | 範例與結果 |
| --- | --- | --- |
| `>` | 是否大於？ | `45 > 0` → `True` |
| `>=` | 是否至少？ | `0 >= 0` → `True` |
| `<` | 是否小於？ | `30 < 30` → `False` |
| `<=` | 是否至多？ | `30 <= 30` → `True` |
| `==` | 值是否相等？ | `45 == 45` → `True` |
| `!=` | 值是否不同？ | `"" != ""` → `False` |

只差一條橫線，規則就不同：時間用 `> 0`，因為零不合法；距離用 `>= 0`，因為零距離合法。不要只背符號，應把每個條件讀成一句完整的規則，再檢查邊界是否包含。

> [!example] 範例：「=」stores a binding；「==」asks a question
> ```python
> duration_min = 45
> time_ok = duration_min > 0
> print(time_ok)
> duration_min = 0
> print(time_ok)
> print(duration_min > 0)
> ```

> [!solution]- 輸出
> ```text
> True
> True
> False
> ```
> 這和 Deck 2 的舊 `miles` 結果一樣。`time_ok` 在指派時已經求值為 `True`；後來 `duration_min` 改成零，不會自動執行之前的比較。若需要目前的判斷，必須重新求值。A saved condition does not automatically update when its input variable changes.

> [!question] Quick challenge：a number or a piece of text?
> Pair check, 2 minutes. Predict each line separately. Which lines return a bool? Which raises an error? Why do types matter?
> ```python
> print(30 <= 30)
> print(0 > 0)
> print("30" == 30)
> print("9" > "30")
> print("30" > 0)
> ```

> [!solution]- 答案
> | 運算式 | 結果 | 原因 |
> | --- | --- | --- |
> | `30 <= 30` | `True` | 包含相等邊界。 |
> | `0 > 0` | `False` | 零不是正數。 |
> | `"30" == 30` | `False` | 文字與整數不是相同的值。 |
> | `"9" > "30"` | `True` | 比較文字順序，不是數量大小。 |
> | `"30" > 0` | `TypeError` | 這組字串與整數不支援此大小比較。 |
>
> `"9" > "30"` 先比較開頭字元，因此不能拿它當作數字 9 和 30 的大小關係。數值規則必須在需要時先做數值解析。Type conversion and domain validation answer different questions.

但成功轉成 float 也還不夠，因為 float 能表示無窮大和 NaN：

> [!example] 範例：A number can be non-finite
> ```python
> import math
> print(math.isfinite(12.5))
> print(math.isfinite(0.0))
> print(math.isfinite(float("inf")))
> print(math.isfinite(float("nan")))
> ```

> [!solution]- 輸出
> ```text
> True
> True
> False
> False
> ```
> `math.isfinite()` 讓「距離必須有限」變成可以執行的檢查；只檢查負數不能完整排除非有限數。Conversion success does not guarantee a meaningful distance. 這個工具仍以一般課堂大小的輸入為範圍，不是保證所有極端有限數的後續算術都不會發生問題。

## D3-Q2 多個條件如何一起工作

對應投影片：Deck 3｜11–18。

A valid trip needs more than valid time: the label, distance, and duration must all satisfy the contract. Build small named conditions, then combine them.

> [!example] 範例：所有條件通過，用 and
> ```python
> import math
> route_name = "Campus"
> distance_km = 12.5
> duration_min = 45
>
> label_ok = route_name != ""
> distance_ok = math.isfinite(distance_km) and distance_km >= 0
> time_ok = duration_min > 0
> valid = label_ok and distance_ok and time_ok
> print(valid)
> ```

> [!solution]- 輸出
> ```text
> True
> ```
> `valid` 不代表「有一項資料看起來可以」，而是三個條件全部成立。把規則拆成有意義的名稱，方便逐項檢查，也方便向同學解釋哪一個條件失敗。All requirements satisfied → `and`. One valid input is not enough.

| A | B | A and B | A or B |
| --- | --- | --- | --- |
| True | True | True | True |
| True | False | False | True |
| False | True | False | True |
| False | False | False | False |

**任一條件失敗就拒絕，用 or**（片段：此小例子先假設距離有限）：

```python
bad_numbers = (distance_km < 0) or (duration_min <= 0)
```

| Distance | Minutes | Must reject? |
| --- | --- | --- |
| −1 | 30 | Yes: distance fails |
| 5 | 0 | Yes: duration fails |
| −1 | 0 | Yes: both fail |
| 0 | 30 | No: both satisfy these rules |

負距離配上正常時間，仍然必須拒絕；正常距離配上零時間，也必須拒絕。若把 `or` 換成 `and`，就變成「兩項同時壞掉才拒絕」。同時輸入 −1 km、0 min 會讓這個錯誤版本也拒絕，反而看不出錯；**測試單一欄位失敗才容易抓到它**。Do not confuse "all checks must pass" with "all checks must fail."

**not 是邏輯否定，不是位元反轉**：

```python
time_ok = duration_min > 0
print(not time_ok)

valid = distance_ok and time_ok
invalid = not valid
```

`not time_ok` 會把 `True` 變成 `False`，把 `False` 變成 `True`。Python 的條件組合使用 `and`、`or`、`not`；`&`、`|`、`~` 是另一組**位元運算**符號（integer bit operations），不應把 `~` 當成一般條件的邏輯否定。For Boolean negation, write `not`. Do not replace it with `~`. 對一般有限數，「不是全部有效」可以對應到「至少一項失敗」；但包含 NaN 時，比較的否定容易和直覺不同，所以完整距離驗證仍保留獨立的 `isfinite` 檢查。

**括號與短路求值都會影響結果**（For Boolean combinations: not before and before or. Parentheses remove doubt）：

> [!example] 範例：Do these require the same thing?
> ```python
> valid = False
> duration_min = 60
> print(valid and duration_min <= 30 or duration_min == 60)
> print(valid and (duration_min <= 30 or duration_min == 60))
> ```

> [!solution]- 輸出
> ```text
> True
> False
> ```
> `and` 的優先序高於 `or`，所以第一行的最後一項可以繞過 `valid`；第二行要求 `valid` 成立後，括號裡的任何選項才有用。寫出括號並把句子讀出來（Read a complex condition aloud），確認它真的符合需求。

同一個範圍的兩種寫法：

```python
0 < duration_min <= 30
(duration_min > 0) and (duration_min <= 30)
```

> [!example] 範例：Short-circuit evaluation can protect an operation
> ```python
> distance_km = 12.5
> duration_min = 0
> can_compute = (duration_min > 0) and (
>     distance_km / (duration_min / 60) >= 0
> )
> print(can_compute)
> ```

> [!solution]- 輸出
> ```text
> False
> ```
> `and` 左邊已經是 `False`，就不必再算右邊；因此本例沒有做除法（no division occurs）。若把除法放到左邊，保護就失效了。`or` 則是在左邊已為真時略過右邊。Python may not evaluate the second operand; the order is observable. Put a guard before the risky operation. 最後的工具仍應先完整驗證，再進行計算。

> [!failure] 故意錯誤的範例：every option needs its own comparison
> Prepared misconception example — this condition is not what it looks like.
> ```python
> duration_min = 45
> print(duration_min == 30 or 60)
> print((duration_min == 30) or (duration_min == 60))
> ```

> [!solution]- 輸出與分析
> ```text
> 60
> False
> ```
> 第一行不是「時間等於 30 或等於 60」的縮寫，而是把比較結果與數字 60 做 `or`。比較為假時，運算式得到 `60`；60 在 `if` 中被視為真（The number 60 is truthy; it is not an abbreviation for `duration_min == 60`）。因此它放在 `if` 裡會總是選到真分支，但不能不精確地說它「永遠回傳布林值 True」。

> [!question] Lab 1：express validity without "if"
> Six-minute pair task. We are still computing Boolean values, not selecting a branch.
> 1. Define `label_ok`, `distance_ok`, `time_ok`, and `valid`.
> 2. Include both finite and non-negative checks for distance.
> 3. Predict the results below, then run the expressions（講義版本多加一個零距離案例）.
>
> | Route | km | min | Your prediction |
> | --- | --- | --- | --- |
> | Campus | 12.5 | 45 | ? |
> | Campus | 12.5 | 0 | ? |
> | `""` | 1 | 30 | ? |
> | Campus | inf | 30 | ? |
> | Campus | 0 | 30 | ? |

> [!solution]- 預期 valid
> 依序為 `True`、`False`、`False`、`False`、`True`（Claude 執行確認）。最後一項零距離配正時間，應該有效。Save a Boolean expression you can explain, not just an answer copied from AI.

## D3-Q3 條件如何選擇要執行的程式

對應投影片：Deck 3｜19–25。

Printing `False` does not prevent a division. 印出 `False` 並不會阻止下一行除法；要讓某段程式只在條件成立時執行，需要 **if statement**。A comparison produces a value; `if` uses a truth value to choose a path.

> [!definition] 定義：if statement 與縮排區塊
> 冒號開始區塊，縮排指出哪些敘述屬於它（The colon begins the block; indentation shows which statements belong to it）。The indented lines run only when the condition is true. The dedented line is outside the block. 本課使用四個空格作為一致風格；重點是結構與一致性，而不是宣稱 Python 只允許四個空格。
> ```python
> if duration_min > 0:
>     duration_h = duration_min / 60
>     speed_kmh = distance_km / duration_h
>     print(f"Average speed: {speed_kmh:.2f} km/h")
>
> print("End of this run")
> ```

> [!example] 範例：if / else expresses two alternative paths
> ```python
> distance_km = 15
> duration_min = 30
> if duration_min > 0:
>     speed_kmh = distance_km / (duration_min / 60)
>     print(f"Average speed: {speed_kmh:.2f} km/h")
> else:
>     print("Error: duration must be positive.")
> print("End of this run")
> ```

> [!solution]- 輸出
> ```text
> Average speed: 30.00 km/h
> End of this run
> ```
> 30 分鐘會選到 if 區塊；把 `duration_min` 改成 0，會選到 else，只印錯誤與最後的 `End of this run`。最後一行退回外層縮排，所以兩條正常執行路徑都會到達它（Continue after the selection）。**Exactly one of these two blocks runs**, assuming the condition evaluates normally. An error message is one branch, not an automatic command to stop the entire program.

Trace the same code with two inputs — follow the selected path; do not execute both blocks in your head：

| `distance_km` | `duration_min` | Selected block | Division? |
| --- | --- | --- | --- |
| 15 | 30 | if | Yes |
| 15 | 0 | else | No |

What proves the zero case is safe? The calculation is inside the valid-input branch.

> [!failure] 故意錯誤的範例：A warning alone does not guard the calculation
> 合法縮排，錯誤的執行結構（Prepared faulty example: duration_min is zero）：
> ```python
> # Prepared faulty example: duration_min is zero.
> duration_min = 0
> if duration_min <= 0:
>     print("Error")
> speed = 60 / duration_min
> ```

> [!solution]- 輸出與分析
> ```text
> Error
> ZeroDivisionError: division by zero
> ```
> 講義把第二行寫成「ZeroDivisionError (the final division is still reached)」：最後的除法仍然被執行到。印出 `Error` 不等於停止程式。除法在 if 區塊外面，所以照樣會執行。把除法放入 else 才能讓錯誤與計算互斥：
> ```python
> if duration_min <= 0:
>     print("Error")
> else:
>     speed = 60 / duration_min
> ```
> Both snippets are syntactically valid; only one protects the division. 這段程式語法合法，問題是邏輯結構，最後也造成執行時的除零錯誤。**Indentation can be legal Python and still express the wrong algorithm**；不是每種縮排錯誤都會被 Python 以 `IndentationError` 抓到。

Three different failures need different repairs — read the error or observed behavior before changing the code：

| 觀察到的問題 | 小例子 | 應檢查什麼 |
| --- | --- | --- |
| 語法錯誤（Syntax） | `if duration_min > 0` | 缺冒號或區塊結構不合法。 |
| 執行時錯誤（Runtime） | `"30" > 0` | 操作數型態；是否尚未解析？ |
| 邏輯錯誤（Logic） | `duration_min >= 0` | 允許零時間，違反本題規格。 |

錯誤的邏輯可以造成執行時例外，因此分類不是在說每個缺陷永遠只能有一個標籤。除錯時要分開看「觀察到什麼」和「根本原因是什麼」。A program that runs without an exception can still violate its specification.

> [!question] Lab 2：reject before dividing
> Six-minute guided task. Use a single if / else.
> 1. Read `distance_km` and `duration_min` using the Deck 2 types.
> 2. If time is not positive, print an explanatory error.
> 3. Otherwise calculate speed in km/h and print it.
> 4. Before running, predict the cases：(15, 30)、(15, 0)、(15, −1). 請指出除法在哪個區塊中。

> [!solution]- 答案
> 第一個案例顯示 `Average speed: 30.00 km/h`，後兩個只能顯示時間錯誤（Claude 執行確認）。除法必須在 else（有效資料）區塊中。Success: valid data produce a report; invalid time produces only an error.

## D3-Q4 超過兩種結果時，如何分類

對應投影片：Deck 3｜26–31。

Valid trips still need different labels. First define the categories. Then choose a control-flow structure. Short、Medium、Long 是課堂自行設定的標籤，不是交通、體能或安全標準；先驗證時間是正整數，再依下表分類，**無效時間不屬於任何一類**。

| 分類 | 有效分鐘區間 | 邊界案例 |
| --- | --- | --- |
| Short | `0 < duration_min <= 30` | 1、30 are Short |
| Medium | `30 < duration_min <= 60` | 31、60 are Medium |
| Long | `duration_min > 60` | 61 is Long |

> [!example] 範例：elif adds an alternative, not another independent test
> ```python
> # Precondition: duration_min is a positive integer.
> duration_min = 45
> if duration_min <= 30:
>     trip_band = "Short"
> elif duration_min <= 60:
>     trip_band = "Medium"
> else:
>     trip_band = "Long"
> print(f"Trip band: {trip_band}")
> ```

> [!solution]- 輸出
> ```text
> Trip band: Medium
> ```
> `elif` 是同一串替代選項的一部分。Python 從上往下測試，**第一個為真的區塊執行後，就略過後面的替代區塊**（The first true branch in the chain wins）。45 分鐘先不符合 `<=30`，再符合 `<=60`，因此得到 Medium。Within the valid domain, one chain produces exactly one `trip_band`.

> [!example] 範例：Separate "if" statements may all run
> ```python
> duration_min = 20
> if duration_min <= 30:
>     print("Short")
> if duration_min <= 60:
>     print("Medium")
> ```

> [!solution]- 輸出
> ```text
> Short
> Medium
> ```
> 兩個 if 都各自被檢查，所以會印兩個標籤。若把第二個 `if` 換成 `elif`，20 分鐘就只會印 Short。獨立 if 不是天生錯誤；當一個行程可以同時得到多種標記時，它可能正是需求。現在規格要求的是一個互斥分類，因此應用同一串選擇。Use a chain for one exclusive label; use separate if statements for independent actions.

> [!example] 範例：驗證與分類是不同問題（nested selection）
> ```python
> duration_min = 0
> if duration_min <= 0:
>     print("Error: duration must be positive.")
> else:
>     if duration_min <= 30:
>         trip_band = "Short"
>     elif duration_min <= 60:
>         trip_band = "Medium"
>     else:
>         trip_band = "Long"
>     print(f"Trip band: {trip_band}")
> ```

> [!solution]- 輸出
> ```text
> Error: duration must be positive.
> ```
> 外層先回答「可不可以產生報告」，內層才回答「報告應該用哪個標籤」。`0 <= 30` 在數學上為真，卻不代表零時間應被分類為 Short；它根本不該進入內層的有效資料區域。Do not classify invalid data and then try to explain the label afterward.

> [!question] Lab 3：turn the category table into code
> Five-minute task. Classify positive integer minutes without loops or functions.
> 1. Read one positive integer duration.
> 2. Assign exactly one `trip_band` using if / elif / else.
> 3. Try 1, 29, 30, 31, 60, and 61 minutes.
> 4. Explain why the second branch can use only `<= 60`.
>
> 分類用原始整數分鐘，不使用四捨五入後的速度，也不使用格式化後的字串。

> [!solution]- 答案（Claude 執行確認）
> 1、29、30 → Short；31、60 → Medium；61 → Long。第二個分支只寫 `<= 60` 就夠，因為能走到 `elif` 的路徑，前一個測試 `<= 30` 已經失敗，代表 `t > 30`（見下一節的 path reasoning）。

> [!warning] Claude 提醒：考古題的 if／elif／else 都包在 while 迴圈裡
> 考古題 A7、B7 是「Fibonacci 找 index」：`while True:` 裡面 `if b == Num:`、`elif b> Num:`、`else:` 三選一，前兩條路徑用 `break` 離開。這一節的「第一個為真的分支勝出」加上 [[PROG1 Deck 4 整理#D4-Q5 停止、略過與繼續前進有何不同|D4-Q5 停止、略過與繼續前進有何不同]] 的 `break`，就是整題的結構。

## D3-Q5 為什麼條件順序也是規格

對應投影片：Deck 3｜32–37。

True does not mean "the best matching branch." **Python selects the first true branch.** The programmer must choose a suitable order; the order of a chain is part of its meaning.

> [!failure] 故意錯誤的範例：A broad condition can hide a narrower one
> Prepared logic bug（duration is already positive）. Trace the code for a 20-minute trip.
> ```python
> # Prepared faulty order; duration is already positive.
> duration_min = 20
> if duration_min <= 60:
>     trip_band = "Medium"
> elif duration_min <= 30:
>     trip_band = "Short"
> else:
>     trip_band = "Long"
> print(trip_band)
> ```

> [!solution]- 輸出與分析
> ```text
> Medium
> ```
> 20 本來應是 Short，但先遇到 `<=60`，已經選走 Medium。更嚴重的是：所有可能符合 `<=30` 的正數，也一定先符合 `<=60`，所以 **Short 永遠到不了**（unreachable category）。這不是「Python 會挑最適合的條件」；它只挑第一個成立的條件。

Read each later condition under the earlier failures — the second branch inherits information from the path used to reach it：

| 到達的位置 | 路徑已知資訊 | 實際覆蓋範圍 |
| --- | --- | --- |
| `if t <= 30` | 已驗證 `t > 0`。 | `0 < t <= 30` |
| `elif t <= 60` | 先前 `<=30` 為假，因此 `t > 30`。 | `30 < t <= 60` |
| `else` | 前兩個測試均為假。 | `t > 60` |

所以正確的第二個分支不必再寫 `>30`：執行到那裡的路徑已提供這項資訊。也可以用另一套正確的遞減順序，例如先判 `>60`，再判 `>30`；重點不是背唯一排列，而是**每條可達路徑要符合預定區間**。Order is correct when the reachable paths match the intended categories.

**多個欄位錯誤時，誰優先？**「只回報第一個錯誤」需要明確定義第一個是什麼。版本 0.3 在數值解析成功後，按照下列順序處理；這是產品／課堂規格，不是 Python 自帶的驗證順序。

| 順位 | 失敗條件 | 完整訊息 |
| --- | --- | --- |
| 1 | `route_name == ""` | `Error: route label must not be empty.` |
| 2 | `not math.isfinite(distance_km)` | `Error: distance must be finite.` |
| 3 | `distance_km < 0` | `Error: distance must be non-negative.` |
| 4 | `duration_min <= 0` | `Error: duration must be positive.` |

空標籤、負距離、零時間同時出現，仍只印標籤錯誤；非有限距離與零時間同時出現，印有限距離錯誤。每個拒絕案例都不應再出現 Route、Distance、Average speed 或 Trip band 報告——這些「不該發生的事」也是測試的一部分。"Report the first error" and "report all errors" are different product requirements.

> [!note] 核心觀念
> 錯誤訊息的順序、是否繼續計算，以及會不會印出多餘報告，都屬於可觀察行為。只檢查程式「沒有當掉」是不夠的。

Make the outcomes complete and non-overlapping（Parsed data › Validity check › One allowed outcome）：

| Domain | Required output |
| --- | --- |
| Any validation rule fails | One error; no report |
| Valid + duration <= 30 | Report + Short |
| Valid + 30 < duration <= 60 | Report + Medium |
| Valid + duration > 60 | Report + Long |

A single output is not enough: it must be the correct output for that input. 本版的空字串規則是精確比對 `""`，不是自動去掉空白：只含空白的標籤仍是非空文字，會被保留；Deck 5 才明確改變這個政策。請不要把自行加入的 `strip` 說成只是修正同一份規格。

> [!question] Checkpoint：defend the chosen path
> Three-minute trace. No execution yet. For each case, name the condition that chooses the path and one statement that must not run.
> - Case A：`route_name = ""`，`distance_km = -1`，`duration_min = 0`。Which error appears first?
> - Case B：`route_name = "Rest"`，`distance_km = 0`，`duration_min = 60`。Error, or a valid report?

> [!solution]- 答案
> - Case A：只印空標籤錯誤 `Error: route label must not be empty.`，不能報告。
> - Case B：有效。距離與速度均顯示 0.00，時間分類是 Medium（60 屬於 Medium）。

## D3 電腦基礎：比較與跳躍

對應投影片：Deck 3｜38–40。

高階的 if／else 可以用「比較後選擇下一個指令位置」來理解：Compare values › Choose next instruction › Continue execution。

| Python level | Lower-level idea |
| --- | --- |
| `if score >= 60: print("pass")` / `else: print("fail")` | Compare the score with 60. Jump to one output path. Skip the other output path. |

The next instruction need not be the next line in the written program. 下面是一套為教學發明的指令（toy instruction set），不是 x86、ARM 或 CPython bytecode，也不是 Python 編譯器真的輸出的組合語言；目的是追蹤控制流程。

```text
      LOAD R0, score
      CMP R0, 60
      JLT fail
      OUT "pass"
      JMP done
fail: OUT "fail"
done: HALT
```

`LOAD` 把分數放進 R0；`CMP` 比較 R0 和 60；`JLT` 在「小於」時跳到 fail；`OUT` 印出文字；`JMP` 無條件跳到指定位置；`HALT` 結束。`fail`、`done` 是位置的名稱（labels identify destinations），不是另外執行的一個動作。A branch changes which instruction executes next.

| 階段 | score = 59 | score = 60 |
| --- | --- | --- |
| 比較 | 59 < 60 | 60 is not < 60 |
| `JLT fail` | 跳到 fail（jump taken） | 不跳躍 |
| 輸出 | fail | pass |
| 結束 | HALT | `JMP done` → HALT |

60 分的路徑印完 pass，必須跳過 fail 區塊。若刪掉 `JMP done`，它會繼續往下，連 fail 也印出來（依序印 pass 和 fail）。這和高階語言中把互斥 elif 誤寫成兩個獨立 if 的問題相似：兩個輸出不再互斥。The boundary changes the path, not the instruction set.

## D3-Q6 如何測試決策並審查 AI 程式

對應投影片：Deck 3｜41–51。

A program can run and still choose the wrong branch. Our job is to find inputs that challenge the rules, not just inputs that make the demonstration look good. AI suggests cases; the specification determines what should happen.

**Choose tests from the specification**（Do not derive the expected answer by copying the program's output）。測試至少要挑三種問題：

| Boundaries | Invalid fields | Interactions |
| --- | --- | --- |
| 29, 30, 31 minutes；59, 60, 61 minutes；just below, at, and above | Empty label；negative distance；zero or negative time；NaN／infinity | Two failures at once；zero distance + valid time；check priority and over-rejection |

只測 45 分鐘，很可能抓不到 `<` 和 `<=` 的差異。A useful test explains which rule or likely mistake it is designed to challenge.

講義測試表與投影片 Appendix 測試表合併（all numeric inputs parse successfully; use the stated first-error priority）：

| 輸入 route / km / min | 預期結果 | 主要目的 |
| --- | --- | --- |
| Campus / 12.5 / 45 | 7.77 miles；16.67 km/h；Medium | 正常報告。 |
| Rest / 0 / 30 | 0.00、0.00、Short | 不過度拒絕零距離。 |
| Campus / 1 / 29 | Short | before 30 |
| Campus / 1 / 30 | Short | 包含 30。 |
| Campus / 1 / 31 | Medium | 越過第一個邊界。 |
| Campus / 1 / 59 | Medium | before 60 |
| Campus / 1 / 60 | Medium | 包含 60。 |
| Campus / 1 / 61 | Long | 越過第二個邊界。 |
| Campus / −1 / 30 | 距離錯誤；不產生報告。 | 單一失敗。 |
| Campus / 1 / 0 | 時間錯誤；不產生報告。 | 計算前防護。 |
| Campus / −1 / 0 | 距離錯誤先出現 | 兩個失敗（distance error first）。 |
| `""` / −1 / 0 | 空標籤錯誤優先。 | 錯誤優先序。 |
| Campus / nan / 30 | 距離必須有限的錯誤。 | 解析成功不等於有效。 |

每列的預期值應在執行前寫好。錯誤列還要檢查「沒有行程報告」，而不是只確認錯誤文字出現。Test case = input + expected result + actual result + a reasoned pass/fail judgment. 通過這組測試能提供有用證據，仍不能當成所有可能輸入的完整證明。

> [!example] 提示範本：Test first（ask AI to challenge the rules before writing more code）
> ```text
> Do not write code yet. Use the attached v0.3 contract.
> Propose 10 tests: valid cases, 30/60-minute boundaries,
> zero and negative inputs, non-finite distance,
> and simultaneous failures.
> For each: input, expected outcome, rule challenged.
> Respect the stated first-error priority.
> Mark cases outside the core parsing scope.
> Explain expected outcomes from the rules, not code.
> ```
> Human review：Is each expectation justified? Did AI omit a boundary or invent a requirement?

AI 可以提出候選測試，但不能以自己的程式輸出作為唯一判準，也不能自行發明門檻。學生仍要獨立驗算至少一個正常案例與邊界案例，說明測試到底在挑戰哪一項規則。

> [!failure] 故意錯誤的範例：Find a counterexample to this candidate
> Prepared faulty teaching example — not a recorded AI response. 片段：兩個故意植入的規則錯誤；不是完整驗證器（isolated exercise: finite numbers; parsing already succeeded）。Which inputs expose the wrong guard? Which input exposes the wrong category boundary?
> ```python
> # Isolated prepared fault: numeric values are finite.
> if distance_km < 0 and duration_min <= 0:
>     print("Error: invalid trip data.")
> else:
>     speed_kmh = distance_km / (duration_min / 60)
>     if duration_min < 30:
>         trip_band = "Short"
>     elif duration_min <= 60:
>         trip_band = "Medium"
>     else:
>         trip_band = "Long"
>     print(f"Average speed: {speed_kmh:.2f} km/h")
>     print(f"Trip band: {trip_band}")
> ```

> [!solution]- 反例與最小修補
> | Counterexample | Failure observed | Minimal repair |
> | --- | --- | --- |
> | 1 km / 0 min | Division is reached（`and` 防護太弱，只有時間錯就被放行，造成除零） | Guard: `and` → `or` |
> | −1 km / 30 min | Invalid distance is reported（負距離被接受） | Same guard repair |
> | 5 km / 30 min | Medium instead of Short（分類邊界錯誤） | Boundary: `< 30` → `<= 30` |
>
> 完整工具仍需要標籤與有限數檢查，不能把這個隔離例題當完整解答。Do not change a correct expected answer just to make the candidate pass. A small patch is easier to review than an unexplained replacement script.

**整合：先驗證，再計算與分類**（`trip_decisions.py`；依投影片 47–48 與既有報告規則組合）：

> [!example] 範例：`trip_decisions.py`（v0.3）
> ```python
> # Core scope: numeric conversions succeed; classroom-sized data.
> import math
> MILES_PER_KM = 0.621371
>
> route_name = input("Route label: ")
> distance_km = float(input("Distance in km: "))
> duration_min = int(input("Duration in minutes: "))
>
> if route_name == "":
>     print("Error: route label must not be empty.")
> elif not math.isfinite(distance_km):
>     print("Error: distance must be finite.")
> elif distance_km < 0:
>     print("Error: distance must be non-negative.")
> elif duration_min <= 0:
>     print("Error: duration must be positive.")
> else:
>     miles = distance_km * MILES_PER_KM
>     duration_h = duration_min / 60
>     speed_kmh = distance_km / duration_h
>     if duration_min <= 30:
>         trip_band = "Short"
>     elif duration_min <= 60:
>         trip_band = "Medium"
>     else:
>         trip_band = "Long"
>     print(f"Route: {route_name}")
>     print(f"Distance: {miles:.2f} miles")
>     print(f"Average speed: {speed_kmh:.2f} km/h")
>     print(f"Trip band: {trip_band}")
> ```

> [!solution]- 執行結果（Claude 執行）：一筆有效、一筆錯誤
> ```text
> Route label: Campus
> Distance in km: 12.5
> Duration in minutes: 45
> Route: Campus
> Distance: 7.77 miles
> Average speed: 16.67 km/h
> Trip band: Medium
> ```
> ```text
> Route label: 
> Distance in km: -1
> Duration in minutes: 0
> Error: route label must not be empty.
> ```

請找出外層的有效資料 else，確認三個計算、內層分類和四個 print 都在其中——這就是「無效資料不會計算、不會報告」的結構性理由。No calculation occurs in the validation chain; keep the three Deck 2 report prints inside this else, before the final Trip band line. 測試失敗時先指出哪條路徑違反規格，再提出修改，而不是盲目要求 AI 整份重寫。

> [!question] Build task：build, challenge, explain（12 minutes）
> 1. Complete `trip_decisions.py` in the existing repository.
> 2. Preserve the Deck 2 report for valid inputs; add one band.
> 3. Reject invalid inputs in the stated priority, with no report.
> 4. Record at least six tests, including 30, 60, 0, and two failures.
> 5. Explain one condition, one execution path, and one repair.
>
> No loops, menus, external packages, or user-defined functions yet. Finish one understandable tool.

Push the tested change and its evidence：keep `main.py` and `trip_summary.py`；add `trip_decisions.py`；record `spec_deck3.md`、`tests_deck3.md`、`ai_use_deck3.md`；run the saved script and inspect the selected Changes／diff；commit `Add trip validation and boundary-tested bands`；push origin and verify online. A pushed code file is not the whole deliverable: include expected/actual results and a short explanation. 不要只提交「AI 給我的程式」，而要能解釋一個條件、一條路徑和一次修補。

A project starts with a rule you can defend：

| Study-time planner | Printing estimator | Your own utility |
| --- | --- | --- |
| Compare estimated work with available minutes. Can the plan fit? | Reject negative page counts. Apply a stated price rule. What happens at the threshold? | One input rule. One useful choice. Two boundary tests. Explain your policy. |

Do not ask AI to invent the goal. Choose the decision, define its rule, then ask for help. 每個新題目的門檻和有效值都要重新指定，不能直接把行程的 30／60 分鐘規則照搬。

Decisions become trustworthy when their rules and execution paths can be explained：01 Compare values to ask a precise yes/no question. 02 Combine requirements with and, or, and not. 03 Use if / else to control whether a block runs. 04 Use elif to select one of several outcomes. 05 Order conditions to match categories and error priority. 06 Challenge the logic with independent expected outcomes. Next：can the program handle more than one trip? Do not copy the whole script ten times → Deck 4。

## D3 Exit Ticket 與複習練習

對應投影片：Deck 3｜18、25、31、37、40、53–54、58。

> [!question] 先預測，再看答案
> 1. `=` 與 `==` 各做什麼？`time_ok` 為何不會隨時間變數自動改變？
> 2. 寫出「距離為負，或時間不為正，就拒絕」的條件。提供一個可抓到錯用 `and` 的案例。
> 3. 為何 `duration_min == 30 or 60` 不是正確比較？當時間為 45 時，它得到什麼值？
> 4. 已驗證正時間後，為何先判 `<=60` 再判 `<=30` 會讓 Short 永遠不可達？
> 5. 給出 29、30、31、59、60、61 分鐘的預期分類。
> 6. 空標籤、−1 km、0 min 同時出現，應印什麼？Rest、0 km、60 min 又如何？
> 7. 在教學組合語言中刪去 `JMP done`，score = 60 會印什麼？
> 8. 本版自行對標籤加上 `strip`，是修 bug 還是改規格？為什麼？

> [!solution]- 解答與理由
> 1. `=` 求值後綁定名稱，`==` 比較值。`time_ok` 保存先前比較的結果；需要新的判斷就重新求值。
> 2. `(distance_km < 0) or (duration_min <= 0)`。例如 1 km、0 min：只有時間失敗，正確版本仍須拒絕。
> 3. 它把比較結果與數字 60 做 `or`；時間為 45 時得到 `60`。應寫兩次完整比較；60 是 truthy，不是另一個隱含比較。
> 4. 所有 `<=30` 的有效值也都 `<=60`，已在第一個分支被選走。20 分鐘就是清楚的反例。
> 5. Short、Short、Medium、Medium、Medium、Long。30 與 60 分別屬於較低的那個區間。
> 6. 第一個只印空標籤錯誤，不能報告。第二個有效：距離與速度均顯示 0.00，時間分類是 Medium。
> 7. 依序印 pass 和 fail，因為通過路徑沒有跳過失敗區塊。
> 8. 是規格變更。原本要求精確空字串檢查且標籤原樣保留；去除空白會改變顯示值，也改變空白標籤是否被接受。

## D3 選讀：truthiness、解析失敗與範圍限制

對應投影片：Deck 3｜55–57、59–60。

> [!example] 範例：truth values are broader than bool objects
> ```python
> print(bool(0))
> print(bool("0"))
> print(bool("False"))
> print(0 or 7)
> print("ok" and 5)
> print(not "")
> ```

> [!solution]- 輸出
> ```text
> False
> True
> True
> 7
> 5
> True
> ```
> 空字串和數值零為 falsy，非空字串則為 truthy，即使內容寫著 False。一般 Python 的 `and`／`or` **回傳其中一個操作數**，不一定回傳 bool；`not` 才一定產生布林結果。A truthy value need not be the object `True`. 本課主線使用清楚的比較，避免過早用這些簡寫掩蓋規則。比較數字與字串的值使用 `==`，不要用代表身分相同的 `is` 取代它。

> [!example] 選讀延伸：parsing can fail before validation begins（單次解析與驗證，沒有自動重試）
> ```python
> raw_minutes = input("Minutes: ")
> try:
>     duration_min = int(raw_minutes)
> except ValueError:
>     print("Error: enter minutes as an integer.")
> else:
>     if duration_min <= 0:
>         print("Error: duration must be positive.")
>     else:
>         print("Valid duration")
> ```

這裡的 `except` 處理文字無法成為整數；`else` 只在轉換沒有拋出 `ValueError` 時檢查正負。Parsing: can this text become the required type? Validation: is that value allowed? `try`／`except` 不是 `if` 的替代品，也不會自動重複輸入。`int("45.0")` 仍會失敗；不要偷偷把它改成先 float 再 int，因為那會改變整數文字的約定。

Do not quietly widen or narrow the contract — record a change of requirement separately from a repair of the existing code：

| Input / issue | Current handling | Possible later change |
| --- | --- | --- |
| `""` route | Rejected | Already required |
| `" "` route | Accepted as nonempty | Reject whitespace-only labels after agreement |
| `"abc"` numeric text | Core: parse error | try / except extension |
| nan / inf distance | Rejected by isfinite | Already required |
| Extreme numeric sizes | Outside classroom scope | Define bounds / numerical error policy |

A new policy needs new tests. It should not be smuggled into an AI-generated "fix." 核心課程不宣稱處理中斷輸入、所有巨大數值或每一種外部資料格式。Original definitions are not copied blindly: the legacy `~` / `not` error is corrected, not propagated（Appendix · Sources and adaptation）。

投影片所列的延伸閱讀：Python: truth values, Boolean operations, comparisons；Python: if statements；Python: expression precedence；Python: math.isfinite；Python: errors and exceptions。
