---
course: [PROG1]
semester: "115-1"
chapter: ["4"]
tags: [programming, lecture]
source:
  - "Computer_Programming_Deck4_AI_PBL_English.pptx.pdf（Deck 4 投影片）"
  - "Computer_Programming_Deck4_ClassNotes_ZH.pdf（Deck 4 中文補充講義）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W7：Deck 4 How Can a Program Repeat Work Without Repeating Code? 投影片（English）與中文補充講義融合，依 inquiry ladder（Q1–Q6）排列。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答；其餘內容都來自投影片與講義。輸出一律收在 `[!solution]-` 裡：先預測，再展開。
> 兩份期中考古題與解答在 [[PROG1 Midterm 考古題]]。
> 上一個：[[PROG1 Deck 3 整理]]｜下一個：[[PROG1 Deck 5 整理]]

## Deck 4：程式如何重複工作而不重複撰寫程式

對應投影片：Deck 4｜1–4。

> [!question] Driving question
> How can a program repeat work without repeating code?
>
> Loops, state, stopping rules — and evidence that the process is correct.

**Bridge from Deck 3**：Our tool can judge one trip. What about the next? Preserve Deck 3: the validation rules and the four-line report already work.

| Version 0.3 | Version 0.4 |
| --- | --- |
| Read one trip. | Read another trip. |
| Validate it. | Keep useful totals. |
| Print one report or one error. | Stop when the user is finished. |

New problem: repeat the same policy without copying the whole script.

**Driving problem**：enter several trips, skip invalid records, and finish with a useful summary（The request is "keep going, then summarize"）。

| Input session | Expected summary |
| --- | --- |
| Campus / 12.5 km / 45 min | Accepted trips: 2 |
| Bad / −1 km / 30 min | Total distance: 16.00 km |
| Station / 3.5 km / 30 min | Total duration: 75 min |
| DONE | Overall speed: 12.80 km/h |

The rejected record and the stop command must not enter the totals.

Inquiry ladder：01 What is the unit of work we need to repeat? 02 How can we visit each item with a for loop? 03 What must the program remember across iterations? 04 How do we repeat until a condition or command says stop? 05 How do we stop, skip, and keep making progress? 06 How can we verify a loop with AI as an assistant? — Build: Trip Log v0.4 | AI skill: trace and debug | Foundations: loops + memory locality。

## D4-Q1 我們究竟要重複哪一件事

對應投影片：Deck 4｜1–8。

Deck 3 能處理一筆行程：讀取資料、檢查規則，再印出報告或第一個錯誤。現在使用者希望輸入第二筆、第三筆，最後看總距離與平均速度。這是新的「整個工作階段」（session）需求，不是把原本程式複製多次就能妥善解決的問題。"Let me enter another trip." Which steps should run again — and which should run only once?

| Copy and paste | Describe the rule once |
| --- | --- |
| Read → validate → report／Read → validate → report／Read → validate → report。What if there is a fourth trip? | While there is more input: read one record, validate it, report and update if valid. |

複製三份程式，只能預先處理三次；需要第四次時又得修改。A fixed number of copies hard-codes the number of trips. 迴圈讓我們把「一次工作的規則」寫一次，再用控制條件決定是否再做一次：**A loop repeats a block; its control rule decides whether there is another iteration.** 本版保留 `trip_decisions.py`，另建 `trip_log.py`，繼續使用相同的資料規則與四行行程報告。

Draw the process before choosing syntax：Initialize state → Read next record → Validate → Report + update → Repeat。One iteration handles one candidate record, not the whole session.

| 位置 | 責任 | 例子 |
| --- | --- | --- |
| 迴圈之前（once before） | 建立整段 session 的初始狀態。 | 筆數 0；距離總和 0.0。 |
| 每次迴圈 | 讀取一筆候選資料；停止、拒絕或接受。 | 接受後印報告並累加一次。 |
| 迴圈之後（once after） | 對已接受資料印一次摘要。 | 總距離、總時間、整段平均速度。 |

> [!definition] 定義：Iteration（迭代）
> 一次 iteration 不是整個 session，而是處理下一個輸入的機會。被拒絕的資料也使用了一次迭代，但不能因此變成一筆「接受的行程」；這個區別決定計數器應放在哪裡更新。

版本 0.4 的輸入協定（adds an input protocol; it does not silently change the earlier data rules）：

| 情況 | 必須發生的事 |
| --- | --- |
| 路線標籤剛好是 `DONE` | 立即停止迴圈；不再詢問距離與時間；不計入總和。 |
| 完整一筆資料無效 | 印第一個錯誤；總和不變；重新詢問下一筆路線。 |
| 完整一筆資料有效 | 保留行程報告（Deck 3 report），筆數與兩個總和各更新一次。 |
| 結束時沒有有效資料 | 明確說沒有可摘要的行程；不算平均（do not divide by zero）。 |
| Other scope limits | Numeric conversion succeeds; values/totals are classroom-sized. |

> [!note] 核心觀念
> 本版只保留「完全相等的、大寫 `DONE`」作為路線欄位的結束命令；`done`、` DONE ` 不會自動被正規化。零距離仍是有效資料，不能拿 0 偷代替結束命令。DONE is a command, not an empty or numeric record.

核心版本仍假設數值轉換成功、數值與累加結果在一般課堂大小的範圍內，而且使用者最後會輸入 DONE。非命令的輸入仍先讀完三個欄位，再執行原本的第一錯誤檢查；這不是逐欄位重試，也不是一般文字解析器。

## D4-Q2 for 如何逐項處理資料

對應投影片：Deck 4｜9–14。

One letter at a time. One numbered attempt at a time. How can one block work for every item? **A for loop requests items from an iterable and runs its body for each one.**

> [!example] 範例：One item is assigned on each iteration
> ```python
> for character in "loop":
>     print(character)
> ```

> [!solution]- 輸出
> ```text
> l
> o
> o
> p
> ```
> 第一次讓 `character` 指向 l，做一次 print；第二次指向 o，再做 print，直到沒有下一個字元。兩個 o 是兩個位置的資料，都會被處理；**for 不會自動去除重複值**。

只針對上例的展開追蹤（equivalent trace for this example），不是 Python 內部實作：

```python
character = "l"
print(character)
character = "o"
print(character)
character = "o"
print(character)
character = "p"
print(character)
```

> [!definition] 定義：Iterable（可迭代物件）
> 能依序提供下一個項目的物件。本課用有限字串和 range 示範，但一般 iterable 不一定可以索引，也不一定預先知道長度。「已知次數用 for」是方便的例子，不是 for 的完整定義。

> [!example] 範例：Indentation tells us what repeats
> How many trips? How many "Finished" lines? Move the last line inward. What changes?
> ```python
> for attempt in range(1, 4):
>     print("Trip", attempt)
> print("Finished")
> ```

> [!solution]- 輸出
> ```text
> Trip 1
> Trip 2
> Trip 3
> Finished
> ```
> 迴圈只重複縮排進去的區塊，`Finished` 在外面，所以只印一次。把最後一行向內縮排，輸出就變成每一筆 Trip 後都印 Finished。兩種寫法都符合語法，但意思不同。The loop body is the indented block — not everything written below `for`.

**range describes an integer sequence**：start is included; stop is excluded; step determines the direction.

| 表示式 | 依序提供的值 | 重點 |
| --- | --- | --- |
| `range(4)` | 0, 1, 2, 3 | 預設從零開始，步長為 1。 |
| `range(1, 4)` | 1, 2, 3 | 含起點，不含終點（stop 4 is excluded）。 |
| `range(6, 0, -2)` | 6, 4, 2 | 負步長向下走。 |
| `range(8, 3)` | 沒有值 | 正步長方向不合；合法的空序列。 |
| `range(0, 5, 0)` | `ValueError` | 步長不能是零。 |

range 儲存起點、終點與步長等緊湊描述，不需要先建立每個整數的 list（A range stores a compact description; it does not build a list of all its integers）。請特別注意「stop 不包含」；這正是 `range(1, 4)` 只有三個值的原因。

> [!question] Quick check：predict the values and body count
> Three minutes: write the sequences first, then test your predictions.
>
> | Expression | Your sequence | Body executions |
> | --- | --- | --- |
> | `range(1, 4)` | ? | ? |
> | `range(4)` | ? | ? |
> | `range(5, 1, -2)` | ? | ? |
> | `range(2, 2)` | ? | ? |

> [!solution]- 答案
> `range(1, 4)`：1, 2, 3，三次；`range(4)`：0, 1, 2, 3，四次；`range(5, 1, -2)`：5, 3，兩次；`range(2, 2)`：空序列，零次。Zero iterations is normal behavior, not necessarily a bug.

> [!example] 範例：A known number of attempts fits range（固定三次嘗試；假設文字皆可轉成整數）
> ```python
> for attempt in range(1, 4):
>     duration_min = int(input("Minutes: "))
>     if duration_min > 0:
>         print("Accepted", duration_min)
>     else:
>         print("Rejected")
> ```

> [!solution]- 執行結果（Claude 執行）：輸入 0、20、30
> ```text
> Minutes: 0
> Rejected
> Minutes: 20
> Accepted 20
> Minutes: 30
> Accepted 30
> ```
> 這個 for 仍只詢問三次，但只接受兩次：**迭代次數和成功次數不是同一個概念**。Three iterations means three attempts — not necessarily three accepted records. 另外，固定三次也不代表程式一定很快結束，因為 input 可能等待使用者。

> [!warning] Claude 提醒：考古題的 for 迴圈
> 考古題 A4（`range(5)`）、B4（`range(10)`）都是固定次數的 for，每次用 `a,b = ...` 同時更新兩個變數，最後只印一次。迴圈只跑「range 給的次數」、`print` 在迴圈外只執行一次，是這兩題的關鍵；同時指派見 [[PROG1 Midterm 考古題#新講義沒教的舊考點|新講義沒教的舊考點]]。

## D4-Q3 如何記住前面處理過的資料

對應投影片：Deck 4｜15–21。

The next trip arrives. How do we remember how many were accepted and how far they traveled altogether? **Loop state carries information from earlier iterations into the next one.**

> [!definition] 定義：Counter 與 Accumulator
> **counter（計數器）** 回答「有幾筆」（how many?）；**accumulator（累加器）** 回答「加起來多少」（how much altogether?）。它們在迴圈之前初始化一次，之後只在對應事件（接受一筆行程）發生時更新。A skipped record must leave all three variables unchanged.

| 名稱 | 初始值 | 接受一筆後 |
| --- | --- | --- |
| `accepted_count` | `0` | `accepted_count += 1` |
| `total_km` | `0.0` | `total_km += distance_km` |
| `total_min` | `0` | `total_min += duration_min` |

對這些純數值變數而言，`total_km += distance_km` 可以理解成用舊總和加上新距離，再更新名稱的綁定；它不是每次重新從零開始。可變物件的 `+=` 細節不同，這裡先限於本課的數值。

> [!example] 範例：A small sum makes the state visible（contract: n is a non-negative integer; compute 1 + 2 + … + n）
> ```python
> n = 4
> total = 0
> for i in range(1, n + 1):
>     total += i
> print(total)
> ```

> [!solution]- 輸出與追蹤
> ```text
> 10
> ```
> | i | 加之前的 total | 加之後的 total |
> | --- | --- | --- |
> | 1 | 0 | 1 |
> | 2 | 1 | 3 |
> | 3 | 3 | 6 |
> | 4 | 6 | 10 |

> [!definition] 定義：Loop invariant（迴圈不變量）
> A loop invariant is a statement that remains true as the loop progresses. 上例的不變量：**每次迭代結束後，total 等於已處理數字的總和**。n = 0 時 `range(1, 1)` 為空，total 仍保持初始值零：初始狀態即使在一次也沒執行的情況下，也必須合理。

1 到 n 的和也可用 $n(n+1)/2$ 手算，提供獨立預期值；這個例子是練習追蹤，不是在宣稱加總一定得使用迴圈。Trace before trusting.

> [!failure] 故意錯誤的範例：把初始化放錯位置
> Prepared faulty teaching example — not a recorded AI response. Predict both results before pressing Run.
> ```python
> # Prepared fault: resetting the sum in every iteration.
> for i in range(1, 5):
>     total = 0
>     total += i
> print(total)
> ```

> [!solution]- 輸出與修補
> ```text
> 4
> ```
> 每次先清零，就會忘記之前的數字；最後只剩當次的 4。正確修補不是在最後多加一個常數，而是把 `total = 0` 移到迴圈外，恢復「記住已處理前綴」的不變量（repaired version prints 10）：
> ```python
> total = 0
> for i in range(1, 5):
>     total += i
> print(total)
> ```
> Totals live across the session. Per-record fields are refreshed each iteration.

**Trace the accepted prefix, not every attempt**（每列是處理完成後的狀態）：

| 剛處理的輸入 | 動作 | 筆數 | 總 km | 總 min |
| --- | --- | --- | --- | --- |
| 尚未輸入 | – | 0 | 0.0 | 0 |
| Campus / 12.5 / 45 | 接受 | 1 | 12.5 | 45 |
| Bad / −1 / 30 | 拒絕（skip） | 1 | 12.5 | 45 |
| Station / 3.5 / 30 | 接受 | 2 | 16.0 | 75 |
| DONE | 停止 | 2 | 16.0 | 75 |

Bad 不有效，所以三個值都不變；DONE 不是資料，也都不變。After each record, the count and sums describe exactly the accepted records so far. 這個不變量比「程式裡有加法」更有力，因為它限制了加法應該在哪些路徑出現。浮點數仍有一般數值精度限制，不是精確實數加總的保證。

**「平均」必須先說清楚平均什麼**（Which average actually answers the question?）：

$$
\text{mean duration} = \frac{75}{2} = 37.5\ \text{min per trip}
$$

$$
\text{overall speed} = \frac{12.5 + 3.5}{(45 + 30)/60} = \frac{16}{1.25} = 12.8\ \text{km/h}
$$

第一趟速度約 16.6667 km/h，第二趟是 7 km/h。把兩個速度直接相加除以二，約為 11.8333，並不是整段行程的 12.8：兩趟用的時間不同，因此本題要的是**總距離除以總經過時間**，不是每筆速度的等權平均。Do not average the two speed numbers: (16.67 + 7.00) / 2 answers a different question. 也不要先把每筆速度格式化到兩位小數再累加；保留原始的距離和時間總和，在最後依定義計算，再格式化顯示。

> [!question] Lab A：read three durations and report their mean
> Seven minutes · first assume all three inputs are positive whole minutes.
> 1. Initialize a total once.
> 2. Read and add three values with one for loop.
> 3. Print the mean after the loop.
> 4. Predict 10, 20, 30; then run your program.
>
> Extension question: if one attempt is rejected, is dividing by 3 still justified?

> [!solution]- 答案（延伸題由 Claude 回答）
> 平均應是 20 分鐘（用 `/` 會印 `20.0`，Claude 執行）。若改成會拒絕無效輸入，分母就不能固定寫 3，而要用「實際接受的筆數」——這正是下面 `accepted_count` 的用途。

## D4-Q4 不知道次數時，如何決定何時停止

對應投影片：Deck 4｜22–27。

We do not know the number of trips in advance. What should decide whether the next iteration happens? **A while loop repeats while its condition remains true.**

> [!example] 範例：while checks its condition before every iteration
> ```python
> remaining = 3
> while remaining > 0:
>     print(remaining)
>     remaining -= 1
> print("Go")
> ```

> [!solution]- 輸出
> ```text
> 3
> 2
> 1
> Go
> ```
> 先問 `remaining > 0` 嗎？若成立，就印出目前值並減一，再回去重問；到零時條件為假，離開迴圈。**若一開始就是零，區塊一次也不執行**（The condition can be false before the body has run even once）。這裡每次重新求值的是比較式，不是會自動更新的「已儲存條件」。Ask: what can change before the next condition check?

同一個有限過程的 for 版本（item-driven vs condition-driven），輸出相同：

```python
for remaining in range(3, 0, -1):
    print(remaining)
print("Go")
```

兩段輸出相同，但重複的來源不同：for 由 iterable 提供下一項；while 由程式重新判斷條件。選擇能讓「下一次從哪裡來、什麼時候結束」最清楚的寫法，而不是認為兩者只能解固定兩種題目。"Known count → for" is a useful example, not a complete definition of for.

> [!definition] 定義：Sentinel（結束命令）
> 用一個明確的保留值結束輸入。Read the route label first. A stop command must not be parsed as a trip.
> ```python
> while True:
>     route_name = input("Route label (DONE to finish): ")
>     if route_name == "DONE":
>         break
>
>     distance_km = float(input("Distance in km: "))
>     duration_min = int(input("Duration in minutes: "))
>     # Validate, report, and update one record here.
> ```
> `while True` 的條件一直成立，但程式可以在明確的位置用 `break` 離開。先讀 route，再檢查 DONE，才能避免使用者明明要結束，程式卻還要他填距離與時間。這裡的命令是一個保留標籤，而不是一筆零行程。DONE is checked before numeric input. A valid zero-distance trip is still data.

Choose a loop from the problem, not from habit — identify where the next item or stopping condition comes from：

| Task | Natural expression | Control source |
| --- | --- | --- |
| Visit each character in a word | `for character in text` | Next item from the iterable |
| Make exactly n attempts | `for attempt in range(n)` | A finite integer sequence |
| Read until DONE | `while True` + `break` | An explicit user command |
| Collect n accepted records | `while accepted_count < n` | A state condition |

The best loop makes "what comes next?" and "when do we stop?" explicit.

> [!example] 範例：Three attempts is not three accepted values（隔離例題：直到接受三個正時間；不是最終行程協定）
> Trace this input：0、20、30、40。How many attempts?
> ```python
> accepted_count = 0
> while accepted_count < 3:
>     duration_min = int(input("Minutes: "))
>     if duration_min > 0:
>         accepted_count += 1
> print("Accepted:", accepted_count)
> ```

> [!solution]- 答案（Claude 執行）
> ```text
> Minutes: 0
> Minutes: 20
> Minutes: 30
> Minutes: 40
> Accepted: 3
> ```
> 嘗試四次，才接受三次（Claude 執行）。Only successful records should advance an accepted-count target. 這個小例題沒有取消命令，所以它假設後來會出現足夠的正數；不要把這個假設說成「while 一定會停」。A condition-controlled loop stops only if the required progress actually occurs. 最終行程工具採用的是使用者輸入 DONE 的另一套停止協定。

> [!warning] Claude 提醒：考古題的 while True ＋ break
> 考古題 A5／B5（質因數分解：`while True:` 裡能整除就計數，不能就 `break`）、A6／B6（一直乘 2，直到 `i*2 > Num` 才印出並 `break`）、A7（Fibonacci 找 index）全部是 `while True` 搭配 `break`。追蹤時把每一輪的變數值寫成表，就像上面的 accepted prefix 表。

## D4-Q5 停止、略過與繼續前進有何不同

對應投影片：Deck 4｜28–36。

An invalid record should not end the session. DONE should. How do we express those different actions? **break leaves the loop; continue skips the rest of the current iteration.**

| 控制敘述 | 作用 | 本版用途 |
| --- | --- | --- |
| `break` | 離開最內層的迴圈，繼續執行迴圈後面的程式（Stop this loop; continue with the first statement after the loop）。 | DONE 結束 session。 |
| `continue` | 略過這一次剩下的區塊，進入下一個迴圈週期（Skip the rest of this body; start the next cycle of the same loop）。 | 無效完整資料不計入，改讀下一筆。 |

在 while 中，`continue` 回到條件檢查；在 for 中，則取得下一個項目。兩者都不等於必然結束整個應用程式。For our tool: DONE → `break`. Invalid complete trip → `continue`.

> [!example] 片段：Reuse the first-error policy; then skip the record（保留 Deck 3 的第一錯誤順序）
> ```python
> # Fragment inside while, after numeric conversion.
> error = ""
> if route_name == "":
>     error = "Error: route label must not be empty."
> elif not math.isfinite(distance_km):
>     error = "Error: distance must be finite."
> elif distance_km < 0:
>     error = "Error: distance must be non-negative."
> elif duration_min <= 0:
>     error = "Error: duration must be positive."
>
> if error != "":
>     print(error)
>     continue
> # Only accepted records reach the report and totals.
> ```

`error` 是每筆資料的暫時狀態，所以每次都先清空；總和是跨筆資料的 session 狀態，不能跟著每次清空。忘記重設 error，可能讓前一筆的錯誤污染下一筆有效資料；重設總和，則會忘記前面接受的資料。Reset error for each record. Keep accepted totals outside this reset.

> [!example] 片段：Only accepted records reach the update point（all rejection paths have already continued）
> ```python
> # Fragment: all rejection paths have already continued.
> miles = distance_km * MILES_PER_KM
> speed_kmh = distance_km / (duration_min / 60)
>
> # Keep the existing band calculation and report.
>
> accepted_count += 1
> total_km += distance_km
> total_min += duration_min
> ```
> Invariant check: did this accepted record enter each total exactly once?

> [!example] 片段：The final summary belongs after the loop（摘要之前先防護空資料）
> ```python
> # Fragment after the while loop.
> print(f"Accepted trips: {accepted_count}")
> if accepted_count == 0:
>     print("No valid trips to summarize.")
> else:
>     mean_duration = total_min / accepted_count
>     overall_speed = total_km / (total_min / 60)
>     # Display the totals and averages with units.
> ```
> Zero accepted records is a normal outcome of the input protocol.

沒有資料不等於「測量出的平均為零」（No data is not the same as a measured zero）。若筆數為零，平均沒有這個樣本基礎，因此印出明確訊息而不做除法。若至少接受一筆，每筆時間都已驗證為正，所以在課堂數值範圍內，總時間也為正；零公里則仍可產生零速度。Do not divide before checking the count.

> [!failure] 故意錯誤的範例：continue can skip the update that makes progress
> 只做紙上追蹤，不直接啟動無界執行（READ ONLY: deliberately nonterminating example）。
> ```python
> # READ ONLY: deliberately nonterminating example.
> i = 1
> while i <= 3:
>     if i == 2:
>         continue
>     print(i)
>     i += 1
> ```

> [!solution]- 有界追蹤（bounded trace）
> | 步驟 | i | 下一個動作 |
> | --- | --- | --- |
> | 1 | 1 | 印 1，更新為 2。 |
> | 2 | 2 | continue，跳過 `i += 1`。 |
> | 3 | 2 | 再次 continue，狀態仍相同。 |
> | 4 … | 2 | 同樣狀態不斷重複。 |
>
> 這個程式不是在等待輸入，而是在反覆執行不變的狀態。可修成 skip 路徑也更新 i，或用 `for` over `range(1, 4)` 讓迭代器前進。把 `continue` 換成 `break` 會少印 3，因此不是保留原意的修補。A continue path is still a path. Check what it does to the next condition check.

> [!example] 範例：for 版本讓迭代器自己前進
> ```python
> for i in range(1, 4):
>     if i == 2:
>         continue
>     print(i)
> ```

> [!solution]- 輸出
> ```text
> 1
> 3
> ```

**Explain progress on every path**（Passing a few tests does not prove that every possible interaction will terminate）：

| Loop | What progresses? | What must be true? |
| --- | --- | --- |
| for over a finite range | The iterator advances | The body completes each time |
| Countdown while | remaining decreases | The update is not skipped |
| Trip Log until DONE | Each record returns to a new prompt | The user eventually enters DONE |

Waiting for input ≠ spinning through unchanged state. Describe the stop assumption; do not promise unconditional termination for interactive input. 有限幾次測試不能證明所有使用者互動必然結束。

> [!example] 範例：Nested loops restart the inner work
> ```python
> for i in range(1, 3):
>     for j in range(1, 4):
>         print(i, j)
> ```

> [!solution]- 輸出
> ```text
> 1 1
> 1 2
> 1 3
> 2 1
> 2 2
> 2 3
> ```
> 外層每取得新的 i，內層就重新走一遍 j。若把內層 body 換成：
> ```python
> if j == 2:
>     break
> print(i, j)
> ```
> 只會印 `1 1`、`2 1`：**break 離開的是內層，不會取消外層下一次迭代**（A break belongs to the innermost enclosing loop, not to every loop）。先用這個 2×3 小表追蹤，通常比直接看大型巢狀程式清楚。

> [!question] Lab B：choose the correct stop and skip
> Six minutes · a miniature duration-only exercise; not the final route interface（這個練習把命令放在分鐘欄，與正式工具的路線欄不同）。INCOMPLETE EXERCISE · FILL BEFORE RUNNING.
> ```python
> accepted_count = 0
> while True:
>     raw_minutes = input("Minutes (DONE to finish): ")
>     if raw_minutes == "DONE":
>         # BLANK 1
>     duration_min = int(raw_minutes)
>     if duration_min <= 0:
>         print("Skip")
>         # BLANK 2
>     accepted_count += 1
> print(accepted_count)
> ```
> Predict 0, 20, −5, 30, DONE. Then also check DONE as the very first input.

> [!solution]- 答案
> 讀到 DONE 時 `break`（BLANK 1），讀到非正整數時印 Skip 並 `continue`（BLANK 2），其餘才增加計數。輸入 0、20、−5、30、DONE 應接受兩次（印 Skip 兩次，最後印 `2`）；一開始就 DONE 則為 `0`（Claude 執行確認）。

## D4 電腦基礎：向後跳躍與記憶體區域性

對應投影片：Deck 4｜37–41。

**A loop is a branch back to earlier work.** 教學指令集（toy assembly），不是 Python 的實際編譯結果：

```text
      LOAD R0, 0
loop: CMP R0, 3
      JGE done
      OUT R0
      ADD R0, 1
      JMP loop
done: HALT
```

`JGE` 在 R0 大於或等於 3 時跳到 done；`ADD` 讓 R0 增加；`JMP loop` 回到檢查。同一個區塊不需要被複製（the body need not be copied），因為「下一個指令」可以回到先前的位置；狀態更新則讓下一次比較的結果不同。The backward branch repeats instructions; the state update changes the next decision.

| 比較時的 R0 | 是否跳到 done？ | 輸出 | 下一個狀態 |
| --- | --- | --- | --- |
| 0 | No | 0 | 1 |
| 1 | No | 1 | 2 |
| 2 | No | 2 | 3 |
| 3 | Yes | – | HALT |

刪掉 `ADD`，R0 永遠是零，會持續輸出零（which state repeats → the loop no longer stops）；刪掉 `JMP`，則只輸出一次零就走到 HALT。這是一個明確標示的教學機器，不是對真實 CPU 週期數或 Python 執行效能的測量。

**重複工作也會重複存取資料**（Repeated work also means repeated memory access）：CPU execution → CPU caches（small, nearby）→ RAM（larger working memory）。CPU caches help service some accesses without going all the way to RAM.

| Cache / RAM | SSD / other storage |
| --- | --- |
| Keep working data available while the program runs. | Keeps saved files persistently. Accessed through the storage system. |

CPU cache 保存部分指令或資料的快取列（cache line），讓某些存取不必走到較遠的 RAM。RAM 是較大的工作記憶體，SSD 等持久儲存則保存已儲存的檔案。**cache hit** 表示所需資料已在該層；**miss** 表示需要到更下層找。這不是說每一行 Python 都對應一次固定的 cache 存取。Saving a file to an SSD and fetching a cache line are different operations.

| 概念 | 抽象位址順序 | 直覺 |
| --- | --- | --- |
| 時間區域性（temporal locality） | 100 → 100 → 100 | 很快又使用同一個位置。 |
| 空間區域性（spatial locality） | 100 → 104 → 108 | 接近的時間內使用鄰近位置。 |

Locality is about memory access patterns — not just how many lines of Python we write. These are abstract memory addresses, not a claim about Python object layout. 補充比喻：剛用過的資料先留在手邊，是時間區域性；拿一頁資料時，把旁邊幾筆一起帶來，可能幫到空間區域性。這只是記憶體存取的比喻，不代表 Python 名稱或物件一定在連續位址，也不代表快取一定使每段程式更快。

> [!question] Cache quick check：follow the addresses
> Toy read cache: initially empty; one line holds addresses 0–3; no eviction.
>
> | Read address | Hit or miss? | Why? |
> | --- | --- | --- |
> | 0 | ? | ? |
> | 1 | ? | ? |
> | 2 | ? | ? |
> | 0 again | ? | ? |

> [!solution]- 答案
> Miss、Hit、Hit、Hit。第一次讀零 miss 並載入整列（0–3），後三次都 hit：讀鄰近的 1、2 展示空間區域性，重讀 0 展示時間區域性。

> [!note] 核心觀念
> 這個四位址快取列是教學假設，不是真實硬體規格。不要用一個極短 Python 迴圈的時間差，宣稱已單獨測出 CPU cache 的效果；直譯器與物件管理等工作也混在其中。Explain the memory behavior. Do not use a tiny Python timing test as proof of cache effects.

> [!warning] Claude 提醒：考古題的 L1／L2 cache
> 考古題 A 1(c)(d)、B 1(c) 問 L1 和 L2 cache 誰比較小、比較快；新講義只講到「cache 小而近、RAM 大」。答案：L1 比 L2 小、比 L2 快（A 1(c)(d) 都是 T，B 1(c)「L1 比 L2 大」是 F），整理在 [[PROG1 Midterm 考古題#新講義沒教的舊考點|新講義沒教的舊考點]]。

## D4-Q6 如何驗證整個迴圈與 session

對應投影片：Deck 4｜42–52。

One valid trip works. What evidence tells us that empty input, rejected records, and stopping also work? Test ordered sessions, inspect state, and challenge every exit and skip path.

**A loop needs sequence tests, not only isolated inputs** — each session has a meaningful order and an explicit ending：

| session | 預期 | 能抓到什麼（likely bug exposed） |
| --- | --- | --- |
| 一開始 DONE | 零筆；不問數值，不算平均。 | 命令檢查太晚（sentinel checked too late）。 |
| 一筆有效，DONE | 報告一次，摘要一次。 | 縮排或摘要位置錯誤（body or summary in wrong block）。 |
| 有效、無效、有效、DONE | 只把兩筆有效資料相加。 | 錯誤狀態殘留、把嘗試當成功（counting attempts; stale error）。 |
| 有效、無效、DONE | 保留第一筆總和。 | 最後一筆把累加器清零（resetting totals inside the loop）。 |
| 全部無效，DONE | 0 筆；沒有行程報告；不除以零。 | 使用未定義的最後一筆有效資料；unsafe final division。 |
| 零距離、重複、邊界 | 零距離有效（speed 0.00）；重複各計一次；保留分類。 | 擅自改規格；using 0 as a stop command。 |

只測一筆有效行程無法顯示 session 狀態錯誤；特別是「有效後再無效然後結束」，容易抓到總和被重設的問題。每個案例應包含明確的 DONE，並記錄不該出現的額外詢問或錯誤報告（Also check what must NOT happen: extra prompts, rejected-record reports, or corrupted totals）。Also retain the earlier 30/60-minute boundary and finite-distance regression tests.

**Work out the reference answer independently**（Use the specification and ordinary arithmetic, not the program's own output）：

| Quantity | Independent derivation | Expected display |
| --- | --- | --- |
| Accepted trips | Campus + Station only | 2 |
| Total distance | 12.5 + 3.5 | 16.00 km |
| Total duration | 45 + 30 | 75 min |
| Mean duration | 75 / 2 | 37.50 min |
| Overall speed | 16 / (75 / 60) | 12.80 km/h |

Write the expected answer before running either the original or the repaired program.

> [!example] 提示範本：Trace → diagnose → patch（ask AI for a bounded trace before asking for a rewrite）
> ```text
> Use this contract and code. Do not rewrite it yet.
> Trace at most six iterations or complete records.
> Show the branch and state before/after each step.
> Which path reads new input, skips, or stops?
> If a state repeats, explain why progress may fail.
> Do not execute a potentially unbounded loop.
> Then suggest one minimal patch and tests to rerun.
> ```
> AI can propose a trace. You must check that it follows the code and the agreed contract.

AI 的追蹤也需要檢查：它有沒有真的遵守縮排？是否把 `continue` 後面的更新算進去了？是否把無效資料偷偷加入總和？先核對具體狀態，再接受修補，會比要求「幫我改好整個程式」更容易掌握。

> [!failure] 故意錯誤的範例：Find two violations in a loop that still finishes
> Prepared faulty teaching example — not an actual AI response. Isolated task: three finite distance attempts. For 12.5, −1, 3.5: expected count = 2, total = 16.0. What does this code actually print?
> ```python
> # Prepared fault: three finite numeric distances.
> count = 0
> total_km = 0.0
> for attempt in range(3):
>     distance_km = float(input("km: "))
>     count += 1
>     total_km = 0.0
>     if distance_km < 0:
>         continue
>     total_km += distance_km
> print(count, total_km)
> ```

> [!solution]- 輸出與分析：輸入 12.5、−1、3.5
> ```text
> 3 3.5
> ```
> `count` 在拒絕前增加，所以數的是三次嘗試；`total_km` 每次清零，所以只剩最後 3.5。修補是把計數移到負數防護後，以及刪除迴圈內的清零（move the counter behind validation; remove the repeated initialization）。預期仍然是 2、16.0，不能因為程式已經會結束，就接受錯誤總和。
> ```python
> count = 0
> total_km = 0.0
> for attempt in range(3):
>     distance_km = float(input("km: "))
>     if distance_km < 0:
>         continue
>     count += 1
>     total_km += distance_km
> print(count, total_km)
> ```
> ```text
> 2 16.0
> ```
> A good repair restores the stated invariant and survives the relevant regression tests.

**Assemble one loop with three visible paths**（Do not hide control flow inside unexplained new abstractions）：

| Path | Action inside the loop |
| --- | --- |
| STOP: route is DONE | `break` before numeric prompts → final summary |
| SKIP: invalid complete record | print the first error; `continue` → next route |
| ACCEPT: valid complete record | report and update once → next route |

| Before the loop | After the loop |
| --- | --- |
| `accepted_count = 0`；`total_km = 0.0`；`total_min = 0` | One summary. No averages when count is zero. Totals contain accepted records only. |

整合示例的五個區域：初始化、輸入與停止、驗證與略過、接受報告與更新、最後摘要。以下是講義依投影片規則整理的示例，不是未附 classroom pack 的原始檔複本；摘要的英文欄位文字在此示例中明確列出，方便後續測試。

> [!example] 範例：`trip_log.py`（v0.4，講義整合示例）
> ```python
> # Core: numeric parsing succeeds; eventual exact DONE.
> import math
> MILES_PER_KM = 0.621371
>
> accepted_count = 0
> total_km = 0.0
> total_min = 0
>
> while True:
>     route_name = input("Route label (DONE to finish): ")
>     if route_name == "DONE":
>         break
>     distance_km = float(input("Distance in km: "))
>     duration_min = int(input("Duration in minutes: "))
>
>     error = ""
>     if route_name == "":
>         error = "Error: route label must not be empty."
>     elif not math.isfinite(distance_km):
>         error = "Error: distance must be finite."
>     elif distance_km < 0:
>         error = "Error: distance must be non-negative."
>     elif duration_min <= 0:
>         error = "Error: duration must be positive."
>     if error != "":
>         print(error)
>         continue
>
>     miles = distance_km * MILES_PER_KM
>     speed_kmh = distance_km / (duration_min / 60)
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
>     accepted_count += 1
>     total_km += distance_km
>     total_min += duration_min
>
> print(f"Accepted trips: {accepted_count}")
> if accepted_count == 0:
>     print("No valid trips to summarize.")
> else:
>     mean_duration = total_min / accepted_count
>     overall_speed = total_km / (total_min / 60)
>     print(f"Total distance: {total_km:.2f} km")
>     print(f"Total duration: {total_min} min")
>     print(f"Mean duration: {mean_duration:.2f} min")
>     print(f"Overall speed: {overall_speed:.2f} km/h")
> ```

> [!solution]- 執行結果（Claude 執行）：混合 session
> 混合 session 使用 Campus/12.5/45、Bad/−1/30、Station/3.5/30、DONE。講義的預期：第一筆 Medium、第二筆只印負距離錯誤、第三筆 Short；最後是 2 筆、16.00 km、75 min、37.50 min 平均時間、12.80 km/h 整段速度。實際執行：
> ```text
> Route label (DONE to finish): Campus
> Distance in km: 12.5
> Duration in minutes: 45
> Route: Campus
> Distance: 7.77 miles
> Average speed: 16.67 km/h
> Trip band: Medium
> Route label (DONE to finish): Bad
> Distance in km: -1
> Duration in minutes: 30
> Error: distance must be non-negative.
> Route label (DONE to finish): Station
> Distance in km: 3.5
> Duration in minutes: 30
> Route: Station
> Distance: 2.17 miles
> Average speed: 7.00 km/h
> Trip band: Short
> Route label (DONE to finish): DONE
> Accepted trips: 2
> Total distance: 16.00 km
> Total duration: 75 min
> Mean duration: 37.50 min
> Overall speed: 12.80 km/h
> ```
> 一開始就 DONE：
> ```text
> Route label (DONE to finish): DONE
> Accepted trips: 0
> No valid trips to summarize.
> ```

> [!question] Lab C：finish the repeated-input tool（12 minutes）
> 1. Add `trip_log.py`; preserve the earlier files.
> 2. Recognize DONE before numeric input; skip rejected records.
> 3. Keep each accepted report and update totals once.
> 4. Print the guarded summary after the loop.
> 5. Run: immediate DONE, one valid trip, and the mixed session.
>
> Explain one state update, one continue path, and the condition that makes summary division safe.

Push a tested behavior change and its evidence：save and run `trip_log.py` from the existing project folder；record `spec_deck4.md`、`tests_deck4.md`、`ai_use_deck4.md`（至少六個有順序的 session 測試，並保留先前 30／60 邊界與非有限距離案例）；review selected changes and commit；push origin and verify online。Commit idea：`Add repeated trip input and accepted-only summaries`。不需要新 repository，也不需要把整個工具改成函式、GUI 或資料庫。

Use the same patterns for a problem you care about（Choose the question first. Then reuse the process, not somebody else's unexplained code）：

| Score analyzer | Study-session log | Your own utility |
| --- | --- | --- |
| Read scores until DONE. Reject values outside a stated range. Count passes; report a mean. A score of 0 is still data. | Read elapsed study minutes. Skip invalid records. Report total and mean duration. Define empty-data behavior. | What is one record? What ends the session? What should be skipped? What summary is useful? Write two session tests. |

可以重用「先驗證、再累加」的流程，但不能不思考就照搬每個數值限制。A useful loop has a clear repeated unit, meaningful state, and justified stopping behavior：01 Identify the unit of work and what should happen once. 02 Use for to visit items; use while to express a condition. 03 Maintain counters and totals with a clear invariant. 04 Specify stop and skip paths, including empty data. 05 Trace, test, repair, and keep evidence of the final behavior.

Next：can the tool understand less tidy text? 一個新需求：「Accept this whole line: `Campus, 12.5, 45`」。How do we find and clean each part? → Deck 5（strings, indexing, slicing, and text methods）。

## D4 Exit Ticket 與複習練習

對應投影片：Deck 4｜13、21、36、41、53–54、58。

> [!question] 練習
> 1. `range(1,4)`、`range(5,1,-2)`、`range(2,2)` 的區塊各執行幾次？
> 2. 為何 `total_km` 在迴圈外初始化，`error` 卻在迴圈內初始化？
> 3. 輸入有效 A/5/30，再輸入無效 B/−1/30，最後 DONE。摘要應該保留什麼？
> 4. 一開始就 DONE 時，哪些提示與計算絕對不能出現？
> 5. 把無效資料的 `continue` 改成 `break`，對 session 有什麼影響？
> 6. 12.5 km/45 min 與 3.5 km/30 min 的整段平均速度，為什麼不是兩筆速度的算術平均？
> 7. 教學 cache 讀取 0、1、2、0，初始空、每列含 0–3、沒有淘汰，結果如何？
> 8. 看起來程式「停住」，如何區分在等 input 和陷入不前進的迴圈？

> [!solution]- 解答與理由
> 1. 分別是 3、2、0 次；值依序為 1,2,3；5,3；沒有值。
> 2. `total_km` 必須記住跨筆總和，`error` 只描述當前這筆。兩者的生命週期與責任不同。
> 3. 一筆、5.00 km、30 min、平均時間 30.00 min、整段速度 10.00 km/h。無效最後一筆不能清掉 A。
> 4. 不問距離與時間，不算平均；只顯示零筆及沒有有效行程可摘要的訊息。
> 5. 第一筆無效資料會提前結束，之後可能有效的資料都不會讀取，違反「略過後繼續」的協定。
> 6. 時間不同，整段速度應以總距離 16 除以總小時 1.25，得到 12.80。等權平均回答的是另一個問題。
> 7. Miss、Hit、Hit、Hit。第一次帶入鄰近資料，後來重用同一列。
> 8. input 會等待外部資料；不前進的迴圈會持續執行相同狀態。用有界追蹤檢查下一次條件前是否有狀態改變，不直接啟動疑似無界範例。

## D4 選讀：loop-else、解析恢復與最長行程

對應投影片：Deck 4｜55–57、59–60。

> [!example] 範例：迴圈正常完成才執行的 else（a loop can have an else clause）
> ```python
> target = 7
> for candidate in range(5):
>     if candidate == target:
>         print("Found")
>         break
> else:
>     print("Not found")
> ```

> [!solution]- 輸出
> ```text
> Not found
> ```
> `else` 對齊 `for`，不是對齊 `if`。`target = 3` 時找到後 `break`，略過 loop-else；`target = 7` 時 range 正常用盡，才執行 else。空 iterable 也會正常用盡。只說「沒 break 就一定 else」仍不夠精確，因為例外或 `return` 離開迴圈也不會執行這個 else。

> [!example] 選讀片段：Recover from malformed numeric text（不等於核心版本原本已有此能力）
> ```python
> # Optional fragment inside while, after the DONE check.
> raw_distance = input("Distance in km: ")
> raw_duration = input("Duration in minutes: ")
> try:
>     distance_km = float(raw_distance)
>     duration_min = int(raw_duration)
> except ValueError:
>     print("Error: enter distance as a number and minutes as an integer.")
>     continue
> # Apply the same value checks after successful conversion.
> ```

這個延伸先讀兩個原始文字欄位，再做轉型；失敗時略過整筆，回去讀新路線。成功後仍需原本的有限數與正負範圍檢查。Parsing failure is different from rejecting a successfully parsed value; the core version does not claim to recover from parse errors — this extension makes a new promise. 不要用包住整支程式的廣泛 `except` 隱藏其他程式錯誤。

> [!example] 兩個放置位置不同的片段：remember the longest accepted trip
> ```python
> # Before the loop:
> longest_min = 0
> longest_route = ""
>
> # Accepted path, before accepted_count += 1:
> if accepted_count == 0 or duration_min > longest_min:
>     longest_min = duration_min
>     longest_route = route_name
> ```

Choose the empty-data and tie policies before implementing the feature. 第一筆有效資料建立候選；之後只有更長才替換，因此**同時間時保留第一筆**（tie policy: the first accepted trip wins）。空 session 不印最長行程。要測第一筆、更長、較短、同時間與空資料；不要用一個任意初始零就假裝真的觀察到零分鐘行程。

投影片所列的延伸閱讀：Python tutorial: control flow；Python: for and while statements；Python: range objects；Python: break and continue；Cornell CS 3410: caches。Legacy wording is selectively adapted and technically checked, not copied as authority.
