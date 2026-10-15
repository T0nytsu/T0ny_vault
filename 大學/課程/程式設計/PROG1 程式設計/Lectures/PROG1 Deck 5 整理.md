---
course: [PROG1]
semester: "115-1"
chapter: ["5"]
tags: [programming, lecture]
source:
  - "Computer_Programming_Deck5_AI_PBL_English.pptx.pdf（Deck 5 投影片）"
  - "Computer_Programming_Deck5_ClassNotes_ZH.pdf（Deck 5 中文補充講義）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> W8：Deck 5 How Can a Program Process and Interpret Text? 投影片（English）與中文補充講義融合，依 inquiry ladder（Q1–Q6）排列。
>
> 標示方式：`[!tip] Claude 補充` 是 Claude 加的解釋，`[!warning] Claude 提醒` 是考試陷阱與考古題提醒，標題有「Claude」的 `[!solution]` 是 Claude 跑程式得到的結果或解答；其餘內容都來自投影片與講義。輸出一律收在 `[!solution]-` 裡：先預測，再展開。
> 兩份期中考古題與解答在 [[PROG1 Midterm 考古題]]。
> 上一個：[[PROG1 Deck 4 整理]]

## Deck 5：程式如何處理並解讀文字

對應投影片：Deck 5｜1–4。

> [!question] Driving question
> How can a program process and interpret text?
>
> Strings, explicit formats, and careful changes to an AI-assisted project.

**Bridge from Deck 4**：Our loop works. The input interface is still awkward. Keep Deck 4's calculations and totals; change how one record enters the program.

| Version 0.4 | Version 0.5 |
| --- | --- |
| Route label: Campus East／Distance in km: 12.5／Duration in minutes: 45 | One line per trip: `Campus East,12.5,45`. Then another line — or DONE. |

A text-processing change should not silently change the numerical model.

**Driving problem**：separate fields, clean only their edges, and preserve their meaning（The request is "accept this whole line"）。

```text
  Campus East , 12.5 , 45
Broken,1
Station,3.5,30
  done
```

Expected summary：Accepted trips: 2；Total distance: 16.00 km；Total duration: 75 min；Overall speed: 12.80 km/h。**Whitespace tolerance is useful. Losing parts of a label is not.**

Inquiry ladder：01 What is text, and what does our format promise? 02 How do we access and extract parts of text? 03 How do we inspect and transform text without damaging it? 04 How do we turn one line into validated fields? 05 How do characters become bytes and persistent files? 06 How can AI help us modify the tool without changing its rules? — Build: Trip Text v0.5 | AI skill: controlled modification | Foundations: encoding + storage。

## D5-Q1 文字的意義從哪裡來

對應投影片：Deck 5｜1–9。

Deck 4 已能反覆讀行程、略過無效資料、累加有效結果。現在要改的是輸入介面：不用每筆分三次回答路線、距離、時間，而是輸入一整行 `Campus East,12.5,45`。數學公式與統計不變，新的問題是「如何把一行文字解讀成正確的欄位」。

How does the program know which part is a name, a distance, or a duration? 這不是一般自然語言理解。程式知道第一段是名稱、第二段是公里、第三段是分鐘，是因為我們**約定了格式**，而不是因為逗號本身理解這些角色。The meaning comes from an agreed format, not from the string alone. 先決定格式，再選擇分割、清理與驗證工具。

版本 0.5 的約定（classroom design decisions, not universal rules for cleaning text）：

| 項目 | 新約定 |
| --- | --- |
| 一筆資料 | 恰好三個逗號分隔欄位：route, km, minutes。 |
| 空白 | 去除各欄位兩端空白；保留標籤內部空白與大小寫。 |
| 結束命令 | 整行去除兩端空白後，忽略大小寫等於 DONE（only the entire trimmed line）。 |
| 格式限制 | 拒絕雙引號、過多或過少欄位；不是完整 CSV。 |
| 數值模型 | 保留有限非負距離、正整數分鐘、30／60 分類和有效資料總和（keep value checks, reports, bands, and accepted-only totals）。 |

這裡**改變了 Deck 4 的精確 DONE 政策**：小寫或兩端有空白的 done 現在也可以結束；標籤兩端的空白也會被去除。但這不授權程式移除名稱中間的空白、改寫大小寫或把 007 改成 7。保留舊 `trip_log.py`，另外建立 `trip_text.py`，讓版本差異可被檢查。New behavior needs new tests. A "cleanup" must not invent a different policy.

> [!note] 核心觀念
> 「讓輸入更寬容」不是一個完整規格。哪些差異可以忽略、哪些文字必須保留，都需要明確決定並測試。

> [!example] 範例：A string is data, not a calculation
> ```python
> print(type("007"))
> print(len("007"))
> print("3" + "5")
> print(3 + 5)
> print("Trip " * 2)
> ```

> [!solution]- 輸出
> ```text
> <class 'str'>
> 3
> 35
> 8
> Trip Trip 
> ```
> Python uses `str` for text, including a single character. str 可以包含英文字、數字、空白、標點與其他文字；Python 不會因為字串裡有數字就把它當數量。`len("007")` 是三個碼位；`int("007")` 才是另外一次明確的數值解析，而解析後會失去前導零的拼寫。Choose operations from the meaning of the data, not just its appearance.

> [!tip] Claude 補充：字串 × 整數＝重複
> `"Trip " * 2` 是把字串重複兩次，結果其實是 `"Trip Trip "`（最後有一個看不見的空白）。考古題 A2 的 `a = "3"`、`b = 5`、`a*b` 就是這個規則：得到 `"33333"`，不是 15。

> [!example] 範例：Some characters are easier to see with repr()
> ```python
> text = "A\tB\nC"
> print(text)
> print(repr(text))
> print(len(text))
> ```

> [!solution]- 輸出
> ```text
> A	B
> C
> 'A\tB\nC'
> 5
> ```
> 值裡有 A、tab、B、換行、C，共五個碼位（`\t` → tab，`\n` → newline）。print 會呈現 tab 與換行的顯示效果；`repr` 則把跳脫表示顯示出來，方便檢查兩端空白或隱藏字元。在原始碼中，引號通常是文字常值的界線（Quotes in source code delimit a literal; they are not usually part of its value）；在 input 提示中真的輸入引號，引號就會成為資料本身。Do not confuse how a value is written in Python with what the user types.

> [!example] 範例：Names can change; string objects do not
> ```python
> s = "Campus"
> t = s
> s = "Station"
> print(s)
> print(t)
> ```

> [!solution]- 輸出
> ```text
> Station
> Campus
> ```
> `t = s` 讓兩個名稱參考當時同一個字串，不要求複製一份。後來 s 改指向 Station，不會改變 t 指向的 Campus。**immutable（不可變）描述的是字串物件**，而不是「這個變數以後不能被重新指派」。Assignment binds names. It does not mean "always allocate and copy the string."

## D5-Q2 如何取出文字的一部分

對應投影片：Deck 5｜10–16。

A label contains several characters. How do we request one character — or a whole region — without retyping it? **Indexing selects one item. Slicing describes a region.**

> [!example] 範例：Give every character a position
> ```python
> s = "Campus"
> print(s[0])
> print(s[-1])
> print(len(s))
> ```

> [!solution]- 輸出
> ```text
> C
> s
> 6
> ```

| 字元 | C | a | m | p | u | s |
| --- | --- | --- | --- | --- | --- | --- |
| 非負索引 | 0 | 1 | 2 | 3 | 4 | 5 |
| 負索引 | −6 | −5 | −4 | −3 | −2 | −1 |

最後一個非負索引是 `len(s) - 1`，不是 `len(s)`。負索引 −1 從最後一個項目開始。取出的單一項目也是 str，不是不同的 char 型態；索引不會把該字元從原字串移除。這裡先用 ASCII 單字，讓每個可見字母與碼位位置一致（For this ASCII example, one visible letter is one code point）。

> [!example] 範例：An index must refer to an existing item（先確認不是空字串，再取第一個項目）
> ```python
> label = input("Label: ")
> if label != "":
>     print(label[0])
> else:
>     print("No first character")
> ```
> Isolated error examples：`"Campus"[6]` → `IndexError`；`""[0]` → `IndexError`。

`"Campus"[6]` 與 `""[0]` 都會產生 `IndexError`，而不是自動回傳空字串。空字串根本沒有第一個字元，所以需要先檢查索引的前提（Check the precondition before asking for a first or last character）。Empty text and one-past-the-end are ordinary cases to think about. 錯誤範例應分開執行，以免第一個例外中止後面的示範。

**切片選一個區域：含起點，不含終點**（`s[start:stop]` returns a string; stop is a boundary, not a selected character）：

| 運算式，`s = "Campus"` | 選到的位置 | 結果 |
| --- | --- | --- |
| `s[1:4]` | 1, 2, 3 | `"amp"` |
| `s[:3]` | 0, 1, 2 | `"Cam"` |
| `s[3:]` | 3, 4, 5 | `"pus"` |
| `s[3:3]` | 沒有項目 | `""` |
| `s[1:100]` | 1–5 | `"ampus"` |

Think "up to, but not including stop." 切片遇到超過字串範圍的邊界，會依字串長度限制區域；不會像單一索引 `s[100]` 那樣產生 `IndexError`。這是兩種不同的操作，不是前後矛盾。

> [!example] 範例：Negative indices and steps describe useful regions
> ```python
> s = "Campus"
> print(s[-3:])
> print(s[::2])
> print(s[::-1])
> print(s[:])
> print(s)
> ```

> [!solution]- 輸出
> ```text
> pus
> Cmu
> supmaC
> Campus
> Campus
> ```
> 第三個位置是 step：每隔幾個項目取一次。負的 step 可反向取值，所以 `s[::-1]` 在本例反轉單字；原本的 s 不變。對 Unicode 文字而言，這是**碼位反轉**，不一定是人眼所見字元的正確反轉（not a universal text-layout operation）；見 [[#D5-Q5 字元如何變成位元組並被保存]]。

> [!example] 範例：Find a boundary before you slice around it（小型抽取例題，不是最終三欄位解析器）
> ```python
> line = input("Text: ")
> pos = line.find(",")
> if pos == -1:
>     print("No comma")
> else:
>     print(line[:pos])
> ```
> Try two inputs：`Campus,12.5,45` → `Campus`；`Campus` → `No comma`。

輸入 `Campus,12.5,45`，逗號位置為 6，所以 `line[:6]` 是 Campus。若沒有逗號，`find` 回傳 −1。未檢查就做 `line[:-1]`，會默默丟掉最後一個字元；例如 Campus 變成 Campu。這種錯誤不一定報例外，更需要明確判斷。A missing delimiter is not a valid boundary at the end of the label.

> [!question] Lab A：extract a useful label without losing information
> Six minutes: predict, run, then explain the empty-input case. `tag = "TRIP-007"`
> 1. Get the first character, final character, prefix（前四字元）, and numeric-looking suffix（最後三字元）.
> 2. Keep the suffix as text. What would `int()` change?
> 3. Handle an empty tag without an index error.
> 4. Explain `tag[4:4]`, `tag[:100]`, and `tag[len(tag)]`.

> [!solution]- 答案（講義＋Claude 執行）
> 長度 8；`tag[0]` 是 `"T"`，`tag[-1]` 是 `"7"`；前四字元 `"TRIP"`；最後三字元 `tag[-3:]` 是 `"007"`。後綴是標籤拼寫，轉成 int 會變成 7 而失去前導零（Keep 007 as text when its spelling is part of the identifier）。`tag[4:4]` 是空字串 `""`；`tag[:100]` 是整個 `"TRIP-007"`；`tag[len(tag)]` 即 `tag[8]`，產生 `IndexError`。空 tag 要先用 `if tag != "":` 檢查再索引。

## D5-Q3 如何檢查與修改文字而不破壞意義

對應投影片：Deck 5｜17–23。

"Make the input more forgiving." Which differences may we ignore — and which differences are real data? **A useful transformation follows a policy; it is not arbitrary deletion.**

> [!example] 範例：走訪字串，問每個字元一個問題（the loop already knows how to visit text）
> ```python
> label = "Route 007"
> digit_count = 0
> for ch in label:
>     if ch in "0123456789":
>         digit_count += 1
> print(digit_count)
> print("aaaa".count("aa"))
> ```

> [!solution]- 輸出
> ```text
> 3
> 2
> ```
> 第一個迴圈只數 ASCII 數字字元，所以得到三個；它不是完整數值解析器，無法單靠這個計數判斷 `-3.5` 等文字是否有效（A character test is not a number parser）。`"aaaa".count("aa")` 的結果是二，因為 **count 計算不重疊的匹配**。要先說清楚數的是什麼（State exactly what is being counted），再選方法。

**相等、包含與位置是不同的問題**（Choose the search that matches your question）：

| 運算式，`label = "Campus East"` | 結果 | 它問什麼 |
| --- | --- | --- |
| `label == "Campus"` | `False` | 整個值相同嗎？ |
| `"Campus" in label` | `True` | 這段文字出現嗎？ |
| `label.find("Campus")` | `0` | 首次出現的位置？ |
| `label.startswith("Campus")` | `True` | 是否位於開頭？ |
| `label.find("West")` | `-1` | 沒有出現。 |

**不要用 `if label.find("Campus"):` 判斷存在**：找到開頭時回傳零，零為假；找不到時回傳 −1，−1 卻為真。問存在就用 `in`；問位置才用 `find`，並明確處理 −1。這也是型態與回傳值角色很重要的例子。

> [!example] 範例：Trim the edges; keep the name（只修規格允許修的部分）
> ```python
> raw_label = " Campus East "
> label = raw_label.strip()
> print(repr(raw_label))
> print(repr(label))
> print("campus" in label.lower())
> print(label)
> ```

> [!solution]- 輸出
> ```text
> ' Campus East '
> 'Campus East'
> True
> Campus East
> ```
> `strip` 去掉兩端空白，不移除中間空白；`raw_label` 也沒有被改掉。搜尋時使用 `label.lower()` 的比較值，不必把保存的名稱改成小寫。**把比較鍵與顯示資料分開**，就能同時寬容地比較、忠實地顯示。This version explicitly changes edge whitespace; it does not change internal whitespace.

`replace(" ", "")` 會把 Campus East 變成 CampusEast，違反本版規則（strip() is not the same operation as removing every space）。若標籤中有兩個內部空白，例如 `West  Gate`，也必須保留兩個。這不是美觀問題，而是資料是否被擅自改寫。

> [!example] 片段：Normalize a command comparison, not the whole record（只正規化命令的比較，不改寫整筆資料）
> ```python
> # Fragment inside the existing input loop.
> line = raw_line.strip()
> if line.upper() == "DONE":
>     break
> # Otherwise, parse the original-case line as a record.
> ```

| 整行輸入 | 是否停止？ | 原因 |
| --- | --- | --- |
| `DONE` | Yes | 整行命令。 |
| `dOnE` | Yes | 去除兩端空白並忽略大小寫後相等。 |
| `Donegal,1,30` | No | 名稱中出現字樣，不是命令（record）。 |
| `DONE,1,30` | No | 完整三欄位資料，標籤可為 DONE（record）。 |

A command is determined by its whole-line role, not by a word appearing inside data.

> [!example] 範例：A text method returns a result; use the result
> ```python
> s = "Campus East"
> t = s
> s.replace("East", "West")
> print(s)
> s = s.replace("East", "West")
> print(s)
> print(t)
> ```

> [!solution]- 輸出
> ```text
> Campus East
> Campus West
> Campus East
> ```
> 第一次 `replace` 產生替換後的結果，但被忽略，所以 s 不變。第二次把結果重新綁定給 s；t 仍指向原字串（`s = s.replace(...)` rebinds s. It does not mutate the object still referenced by t）。`s[0] = "c"` 則會產生 `TypeError`，因為那是要求原地改動字串物件，不是重新綁定名稱。Creating another value is different from modifying the existing string.

> [!question] Lab B：tolerant comparison, faithful display
> Seven minutes: clean a name and search a comparison copy. `raw_label = " Campus East "`
> 1. Trim only the edges; keep `raw_label` for comparison.
> 2. Find campus without case sensitivity; keep display case unchanged.
> 3. Count ASCII digits in `Route 007` with a loop.
> 4. Check DONE, padded done, `Donegal,1,30`, and `DONE,1,30`.
>
> Explain which transformations affect the stored label and which affect only a comparison.

## D5-Q4 如何把一行文字解析成有效欄位

對應投影片：Deck 5｜24–33。

`"Campus East,12.5,45"`：Where should we split? What must be checked before we can calculate? **Separate format, numeric conversion, and value validation.**

> [!example] 範例：split(",") separates fields, not their meanings
> ```python
> line = "Campus East, 12.5, 45"
> fields = line.split(",")
> print(fields)
> print(len(fields))
> print(fields[0])
> print(repr(fields[1]))
> ```

> [!solution]- 輸出
> ```text
> ['Campus East', ' 12.5', ' 45']
> 3
> Campus East
> ' 12.5'
> ```
> split 的結果是一個有順序的 **list**，裡面每一項仍是字串。Three items — with whitespace still present in the numeric fields. Splitting does not convert `"12.5"` into `12.5`; it only identifies pieces of text.

A small list bridge：count items, then select an item（Only `len()` and indexing are needed for this lesson's list result）：

| Expression | Value / role |
| --- | --- |
| `len(fields)` | 3 items（欄位數，不是整行字元數） |
| `fields[0]` | `"Campus East"` — the label |
| `fields[1]` | `" 12.5"` — distance text |
| `fields[2]` | `" 45"` — duration text |
| `fields[1].strip()` | `"12.5"` — still text |

`fields[0]` selects a field. `line[0]` selects a character. Keep the two levels separate. 數值欄位前面的空白仍在，直到稍後刻意 strip。`split()` 不帶參數是依空白分割，會把 Campus East 拆開，不符合本題的逗號格式。也不要丟掉空欄位：`Campus,,45` 的空距離需要保留，驗證器才知道哪裡缺資料。

> [!example] 片段：Check the shape before indexing the fields（三個欄位都存在後，才能安全取得它們）
> ```python
> # Fragment inside while, after command/empty/quote checks.
> fields = line.split(",")
> if len(fields) != 3:
>     print("Error: expected route, km, minutes.")
>     continue
> route_name = fields[0].strip()
> distance_text = fields[1].strip()
> duration_text = fields[2].strip()
> ```

如果只有兩個欄位就直接讀 `fields[2]`，會得到 `IndexError`；形狀檢查先排除這條路徑。多的欄位不能隨便忽略，缺的欄位不能自動補零；兩者都會讓錯誤資料被誤當成完整行程。Do not discard an extra field or invent a missing value to make the input fit.

**把拒絕流程分成明確階段**（One invalid line should fail at one clear stage; apply the agreed first-error order; update no totals before acceptance）：

| 順位 | 檢查 | 通過後才可以做什麼 |
| --- | --- | --- |
| 1 | 整行命令（whole-line stop command） | 不是命令才當資料解析。 |
| 2–4 | 空行、雙引號、欄位數（exactly three fields） | 安全取出三個欄位。 |
| 5 | 去除邊緣空白後的空標籤 | 允許進行數值轉換。 |
| 6 | 先 float 距離，再 int 分鐘 | 得到所需數值型態。 |
| 7–9 | 非有限距離、負距離、非正時間 | 報告並更新總和一次。 |

每筆錯誤只在第一個失敗階段被拒絕。`Campus,-1,abc` 先出現數值解析錯誤，因為負值檢查尚未開始；`Campus,-1,0` 則先報負距離錯誤。這不是任意排序，而是規格讓多重問題的輸出可預測。Parsing asks "can this text become the required type?" Validation asks "is the value allowed?"

> [!example] 片段：Malformed numeric text needs a narrow recovery path（PROVIDED FRAGMENT · INSIDE while, AFTER LABEL CHECK）
> ```python
> try:
>     distance_km = float(distance_text)
>     duration_min = int(duration_text)
> except ValueError:
>     print("Error: distance must be numeric "
>           "and minutes an integer.")
>     continue
> ```
> This small guard is supplied scaffolding; text processing remains today's focus.

`try` 先執行轉換；`ValueError` 被捕捉後，印一次錯誤並改讀下一行。不要把所有程式都包進無差別的 `except`，否則真正的程式缺陷也可能被掩蓋。解析成功後，仍需 `isfinite` 和範圍檢查。`int("30.0")` 與 `int("30.9")` 都會產生 `ValueError`；若改成 `int(float("30.9"))`，會得到 30，違反「整數分鐘文字」的約定——這不是修好資料，而是擅自改掉資料。Do not "repair" malformed data by silently rounding or truncating it.

**A simple delimiter is not a complete CSV grammar**（Our core format deliberately rejects double quotes and extra fields）：

| 輸入 | What it means under v0.5（第一個結果） |
| --- | --- |
| `Campus,,45` | 三欄位，但空距離無法轉成 float → conversion error。 |
| `Campus,1,45,` | 四欄位 → shape error。 |
| `"Campus, East",1,45` | 含雙引號 → unsupported-format error（依本版規則拒絕）。 |
| `Campus East,1,45` | 正常三欄位 → ordinary valid record。 |

真正 CSV 可把引號內的逗號視為資料，但單純 `split(",")` 不理解那套規則。本版刻意拒絕雙引號，而不是假裝支援後把資料切壞（A limitation stated and tested is safer than accidental support that corrupts records）。未來要支援 CSV，必須明確更改文法與測試。**不要用 `eval` 去執行使用者輸入的文字。**

New text handling must preserve old numerical decisions（The same parsed values must receive the same report and classification）：

| Existing rule | Still required |
| --- | --- |
| Distance must be finite | Reject nan and inf after conversion. |
| Zero distance is allowed | 0 km / 30 min is valid. |
| Time bands | 30 → Short; 60 → Medium; 61 → Long. |
| Session state | Only accepted trips change the count and totals. |
| Empty summary | No division when there are no accepted trips. |

The front end changes; the accepted-only invariant and formulas do not. 單行輸入只是新的前端，不是重新定義所有行程規則。

Test what a text cleanup is allowed to change（Use specific labels that reveal accidental transformations）：

| Input line | Expected label / action |
| --- | --- |
| `  Campus East , 12.5 , 45` | `Campus East` |
| `  West  Gate ,1,30` | `West  Gate`（keep two internal spaces） |
| `007,0,30` | `007`（not 7） |
| `Donegal,1,30` | Donegal — accept, do not stop |
| `DONE,1,30` | DONE — accept, do not stop |

"Looks cleaner" is not evidence that the data still means the same thing.

> [!question] Lab C：predict the first rejection stage
> Five minutes: use the contract, not the current candidate's output. An input can violate several rules. The specification decides which error appears first.
>
> | Input | Your first outcome |
> | --- | --- |
> | `Campus,1` | ? |
> | `Campus,,30` | ? |
> | `   ,1,30` | ? |
> | `Campus,-1,0` | ? |
> | `Campus,1,30.0` | ? |
> | `   done` | ? |

> [!solution]- 答案（Claude 用 `trip_text.py` 執行確認）
> | Input | 第一個失敗階段 | 印出 |
> | --- | --- | --- |
> | `Campus,1` | 欄位數（兩欄） | `Error: expected route, km, minutes.` |
> | `Campus,,30` | 數值解析（空距離） | `Error: distance must be numeric and minutes an integer.` |
> | `   ,1,30` | 去空白後標籤為空 | `Error: route label must not be empty.` |
> | `Campus,-1,0` | 負距離（解析成功後） | `Error: distance must be non-negative.` |
> | `Campus,1,30.0` | 數值解析（`int("30.0")` 失敗） | `Error: distance must be numeric and minutes an integer.` |
> | `   done` | 整行命令 | 停止，進入摘要 |

## D5-Q5 字元如何變成位元組並被保存

對應投影片：Deck 5｜34–40。

A string can contain more than English letters. How does that text travel to a file — and what remains after the program ends? **Separate text, encoding, program state, and persistent storage.**

電腦可以用數字識別字元。**ASCII** 定義 128 個代碼；Python 的 `ord` 回傳單一字元的 Unicode code point，`chr` 做反向對應；Unicode 的前 128 個碼位與 ASCII 對齊。Selected entries are enough to explain the mapping; no full-table memorization.

| Character | Decimal code | Python expression |
| --- | --- | --- |
| space | 32 | `ord(" ")` |
| `"0"` | 48 | `ord("0")` |
| `"A"` | 65 | `ord("A")` |
| `"a"` | 97 | `ord("a")` |

`chr(65)` → `"A"`；`ord("A")` → `65`。

> [!example] 範例：ASCII 與 Unicode code point
> ```python
> print(ord(" "))
> print(ord("0"))
> print(ord("A"))
> print(ord("a"))
> print(chr(65))
> ```

> [!solution]- 輸出
> ```text
> 32
> 48
> 65
> 97
> A
> ```
> 數值 0、字元 `"0"`、字元碼 48 是三個不同角色（The character "0" has code 48; it is not the numeric value 0）。也要區分整數 65、兩字元字串 `"65"`、一字元字串 `"A"`。ord／chr 展示對應關係，不是聲稱這些 Python 物件的整個記憶體配置相同。

**Unicode identifies characters; UTF-8 encodes them.** A code point and a byte are different units.

> [!example] 範例：A 加上「中」（U+4E2D）的編碼示例
> ```python
> text = "A中"
> payload = text.encode("utf-8")
> print(len(text))
> print(len(payload))
> print(payload)
> print(payload.decode("utf-8") == text)
> ```

> [!solution]- 輸出
> ```text
> 2
> 4
> b'A\xe4\xb8\xad'
> True
> ```
> 這個文字值是「A中」，共兩個 Unicode 碼位；以 UTF-8 編碼後，十六進位位元組是 `41 E4 B8 AD`，共四個 bytes。`encode` 的結果是 bytes，`decode` 的結果是 str。`len(text)` counts code points. `len(text.encode("utf-8"))` counts encoded bytes. 文字長度、編碼後長度與整個 Python 物件的 RAM 大小，是三件不同的事。

| 文字 | 碼位數 | UTF-8 位元組數 |
| --- | --- | --- |
| A | 1 | 1 |
| 中（U+4E2D） | 1 | 3 |
| A中 | 2 | 4 |

UTF-8 對 Unicode scalar value 使用一到四個位元組；ASCII 字元使用一個。不能因為英文常常是一字一 byte，就推論所有文字都如此。

> [!example] 範例：Visible symbols, code points, and bytes can differ
> ```python
> a = "é"       # precomposed e-acute
> b = "é"       # e + combining acute
> print(len(a), len(b))
> print(len(a.encode("utf-8")))
> print(len(b.encode("utf-8")))
> print(a == b)
> ```

> [!solution]- 輸出
> ```text
> 1 2
> 2
> 3
> False
> ```
> 兩者可能都顯示成 é；第一種是一個預先組合好的碼位，第二種是 e 加上組合重音，因此碼位數與位元組數都不同，原始字串比較也不相等。這就是 `len` 不保證等於人眼看到的字數，以及直接反轉碼位可能破壞顯示的原因。Do not use a byte count or code-point count as a universal count of visible characters.

**顯示在螢幕，不代表已經保存到檔案**（Printed text is not automatically a saved data file）：

| During the run（working program state） | Across runs（persisted file contents） |
| --- | --- |
| `raw_line` and `fields` | A saved UTF-8 sample file |
| Parsed numeric values | Saved Python source |
| Accepted count and totals | Committed test evidence |

`raw_line`、`fields` 與累計值是執行中的狀態；程式結束後，不會自動變成行程資料庫。用編輯器儲存的 UTF-8 測試檔則可以跨次執行保留。`print` 只是輸出，不會自行寫出那個測試檔；commit 保存追蹤中的檔案版本，不保存任意現場變數或終端畫面。Program state lives during execution; a saved file has an explicit persistence mechanism.

HDD, SSD, and optical media store data differently（Different physical mechanisms; the text still needs an agreed encoding）：

| 儲存媒體 | 基本機制 | Key distinction |
| --- | --- | --- |
| HDD | 旋轉磁碟上的磁性記錄（magnetic recording on rotating disks）。 | Mechanical movement；可保存檔案，不是工作中的 RAM。 |
| SSD | 非揮發固態記憶體（nonvolatile solid-state memory），通常是 flash。 | No moving read head；仍需正確編碼。 |
| 光碟（optical disc） | 以雷射讀取資料（information read with laser light）。 | CD／DVD／Blu-ray media；同樣保存已編碼的資料。 |

> [!note] 核心觀念
> 編碼回答「用哪些位元組表示文字」（which bytes?）；儲存回答「位元組保存在哪裡」（where do those bytes persist?）。持久保存不等於永久不壞，也不等於已備份。Persistent does not mean permanent or backed up. Do not confuse an SSD with RAM.

> [!question] Foundation check：choose the right unit and location
> One minute: explain the answer, not just the number.
>
> | Text | Code points | UTF-8 bytes |
> | --- | --- | --- |
> | `"A"` | ? | ? |
> | U+4E2D | ? | ? |
> | `"A"` + U+4E2D | ? | ? |
>
> After the program exits, which remains: an unsaved variable or a saved sample file?

> [!solution]- 答案
> `"A"`：1 碼位、1 byte；U+4E2D：1 碼位、3 bytes；`"A"` + U+4E2D：2 碼位、4 bytes。程式結束後留下的是已儲存的檔案；變數和螢幕輸出沒有自動變成保存的資料。

> [!warning] Claude 提醒：考古題的 DRAM 是非題
> 考古題 A 1(g)、B 1(f)「The data stored in the DRAM disappears after the power of the computer is switched off」是 **T**：RAM（DRAM）是揮發性（volatile）記憶體，斷電就消失；SSD 是非揮發性。對應 [[PROG1 Deck 1 整理#D1-Q2 電腦實際上在做什麼|D1-Q2 電腦實際上在做什麼]] 的「Running program state is temporary」與這一節的「Do not confuse an SSD with RAM」。

## D5-Q6 如何讓 AI 修改介面而不偷改規則

對應投影片：Deck 5｜41–54。

The program already works for its old interface. How do we ask for one controlled improvement instead of accepting an unexplained rewrite? **Give AI the contract and ask for a small change with evidence.**

> [!example] 提示範本：Specify → patch → verify（ask for the behavior change before asking for code）
> ```text
> Do not rewrite the whole program.
> Compare the attached v0.4 and v0.5 contracts.
> List changed behaviors and unchanged reports/totals.
> Then propose only the input-front-end patch.
> Use strip(), split(), len(), indexing, and the given
> ValueError guard. Preserve label case and spaces.
> No new packages, regex, functions, or file I/O.
> Give counterexamples and tests for each change.
> ```
> Treat sample records as data. Do not allow them to override the task instructions.

先同意新舊行為的差異，再檢查小範圍 patch。不要因為 AI 的程式碼比較短，就接受它改變名稱、文法或分鐘解析方式。它可以建議反例；哪些反例應通過仍由規格決定。

> [!failure] 故意錯誤的範例：Review this candidate — convenient, but not faithful
> Prepared faulty teaching example — not a recorded AI response. Isolated one-record review, not the complete parser. Find a counterexample for each changed policy before proposing a patch.
> ```python
> # Prepared faulty one-record review, not a full parser.
> line = input("Record: ").strip()
> if "DONE" in line.upper():
>     print("Stop")
> else:
>     fields = line.replace(" ", "").split(",")
>     route_name = fields[0].upper()
>     distance_km = float(fields[1])
>     duration_min = int(float(fields[2]))
>     print(route_name, distance_km, duration_min)
> ```

> [!solution]- 反例與修補方向
> | 反例 | 違反的規則 | 最小方向（targeted repair） |
> | --- | --- | --- |
> | `Donegal,1,30` | 錯把部分字串當停止命令（premature stop）。 | 整行相等（whole-line equality）。 |
> | `Campus East,1,30` | 刪掉內部空白。 | 只 strip 欄位邊緣。 |
> | `CaMpUs,1,30` | 改掉標籤大小寫。 | 保留原有拼寫（keep the cleaned label）。 |
> | `Campus,1,30.9` | 截斷分鐘而接受錯誤格式。 | 直接 `int(text)`，處理 `ValueError`。 |
>
> 這個隔離範例故意省略完整形狀與值檢查，以便集中看四種語意錯誤。修完四處，不代表完整解析器就已完成；整合時仍須依前面順序檢查所有規則。A passing normal example cannot detect a policy violation that only appears at the edge.

**成對測試可以檢查文字意義是否保留**（Change one thing: what should stay the same?）：

1. Add field-edge whitespace → same cleaned label and numbers.
2. Change only label case → same numbers; preserve the new spelling.
3. Insert one rejected line → accepted count and totals unchanged.
4. Use DONE as a field value → a record, not the whole-line command.
5. End immediately → zero accepted trips and no unsafe averages.

這些關係來自規格，不需要把程式自己的結果當標準答案。AI can suggest useful transformations. The contract decides which invariants are valid.

**Write the session oracle before executing the patch**：混合 session 的測試輸入（每行送入一次）就是本 Deck 開頭的四行。

$$
\text{count} = 2, \quad \text{total km} = 12.5 + 3.5 = 16, \quad \text{total min} = 45 + 30 = 75
$$

$$
\text{mean duration} = 75/2 = 37.5, \qquad \text{overall speed} = 16/(75/60) = 12.8
$$

| Quantity | Derivation | Expected display |
| --- | --- | --- |
| Accepted trips | Campus East + Station | 2 |
| Total distance | 12.5 + 3.5 | 16.00 km |
| Total duration | 45 + 30 | 75 min |
| Mean duration | 75 / 2 | 37.50 min |
| Overall speed | 16 / (75 / 60) | 12.80 km/h |

`Broken,1` 只有兩欄位，拒絕後不改任何總和。除此之外還要檢查 Campus East 的大小寫與空白保留，不能只看最後的四個數字正確就結束測試（Check both the numerical output and the preservation of each accepted label）。

**Integrate a text front end with the loop you already trust**：01 Read a raw line and recognize the whole-line command. 02 Check the format; split and trim three fields. 03 Convert numeric text, then apply the previous value checks. 04 On acceptance: preserve the report and update totals once. 05 After DONE: produce the same guarded summary. One line is accepted, rejected, or a stop command. No partial record enters the totals.

下面的可執行示例是講義依投影片規則整理的教學整合示例（不包含檔案輸入或一般 CSV）。**投影片未提供空白整行及雙引號拒絕訊息的逐字原始碼，因此講義分別定為 `Error: empty record.` 與 `Error: double quotes are not supported.`**；這兩句是明確標示的補定文字，不是聲稱取自 classroom pack。其餘第一錯誤順序、數值規則與報告依本課來源保留。

> [!example] 範例：`trip_text.py`（v0.5，講義整合示例）
> ```python
> # Companion v0.5 example; finite classroom-sized sessions.
> import math
> MILES_PER_KM = 0.621371
> accepted_count = 0
> total_km = 0.0
> total_min = 0
>
> while True:
>     raw_line = input("Trip (route, km, minutes; DONE to finish): ")
>     line = raw_line.strip()
>     if line.upper() == "DONE":
>         break
>     if line == "":
>         print("Error: empty record.")
>         continue
>     if '"' in line:
>         print("Error: double quotes are not supported.")
>         continue
>     fields = line.split(",")
>     if len(fields) != 3:
>         print("Error: expected route, km, minutes.")
>         continue
>     route_name = fields[0].strip()
>     distance_text = fields[1].strip()
>     duration_text = fields[2].strip()
>     if route_name == "":
>         print("Error: route label must not be empty.")
>         continue
>     try:
>         distance_km = float(distance_text)
>         duration_min = int(duration_text)
>     except ValueError:
>         print("Error: distance must be numeric "
>               "and minutes an integer.")
>         continue
>
>     error = ""
>     if not math.isfinite(distance_km):
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
> ```text
> Trip (route, km, minutes; DONE to finish):   Campus East , 12.5 , 45
> Route: Campus East
> Distance: 7.77 miles
> Average speed: 16.67 km/h
> Trip band: Medium
> Trip (route, km, minutes; DONE to finish): Broken,1
> Error: expected route, km, minutes.
> Trip (route, km, minutes; DONE to finish): Station,3.5,30
> Route: Station
> Distance: 2.17 miles
> Average speed: 7.00 km/h
> Trip band: Short
> Trip (route, km, minutes; DONE to finish):   done
> Accepted trips: 2
> Total distance: 16.00 km
> Total duration: 75 min
> Mean duration: 37.50 min
> Overall speed: 12.80 km/h
> ```
> 保留測試也跑過：`  West  Gate ,1,30` 印 `Route: West  Gate`、`007,0,30` 印 `Route: 007`、`Donegal,1,30` 與 `DONE,1,30` 都被當成資料接受。

請先把程式分成 **STOP、REJECT、ACCEPT** 三條路徑，再逐段看程式碼。`continue` 之前的任何失敗都不會跑到更新點；`break` 則離開迴圈，進入一次性的摘要。numeric helper 尚未被抽成函式，因為這是 Deck 6 的下一個問題。

> [!question] Lab D：finish the line-based trip tool（12 minutes）
> 1. Add `trip_text.py` in the existing repository; keep `trip_log.py`.
> 2. Complete TODO A–C: shape checks, fields, and clean label.
> 3. Reuse the supplied parsing guard and the old report/summary.
> 4. Run immediate DONE, the mixed session, and label-preservation cases.
> 5. Explain one slice, one field guard, and one preserved invariant.
>
> Success means tested behavior you can explain, not just a script that starts.

Push a reviewed text-handling change with its evidence：save and run `trip_text.py` from the existing project folder；record `spec_deck5.md`、`tests_deck5.md`、`ai_use_deck5.md`；inspect the diff: were labels or formulas changed unintentionally?；commit, Push origin, and verify the latest files online；exclude private route histories, secrets, and unreviewed AI transcripts。Commit message idea：`Add tested one-line trip input with preserved labels`。至少記錄八個有理由的測試：缺欄、額外欄位、空欄位、錯誤數值文字、標籤保留、DONE 子字串、非有限距離，以及舊的時間邊界或空 session。

A small text tool can solve a real nuisance（Choose one repeated task, a precise format, and a result worth checking）：

| Study-session log | Reading-log cleaner | Your own utility |
| --- | --- | --- |
| topic, minutes。Keep topic spelling. Reject missing minutes. Summarize accepted work. | title, pages。A title may contain commas. Choose a grammar, then choose a parser. | What is one line? What may be normalized? What must be preserved? Which input should fail? |

不要先選 split 再假裝所有輸入都符合它；應先選問題與格式，再選工具。Start with a narrow format you can explain. Expand it when a real requirement appears.

Interpreting text requires a representation, a policy, and evidence：01 Treat text as an immutable sequence of code points. 02 Use positions and slices to extract a needed part. 03 Inspect and transform text according to an explicit policy. 04 Parse fields only after checking the record's shape. 05 Distinguish text, encoded bytes, and persistent storage. 06 Ask AI for small changes; verify the old and new contracts. Human responsibility today: preserve meaning while changing representation and behavior.

Next：Now it works. How do we keep it manageable? → Deck 6 · How do we organize a growing program into understandable components?（functions, parameters, return values, interfaces, and AI-assisted integration）。

## D5 Exit Ticket 與複習練習

對應投影片：Deck 5｜16、23、31、40、52–54。

> [!question] 練習
> 1. `s="Campus"; t=s; s="Station"` 後，t 是什麼？為何這不代表每次指派都複製字串？
> 2. `TRIP-007` 的長度、前四字元、最後三字元各是什麼？為何後者不轉成 int？
> 3. `find` 回傳 −1 時，為什麼不能直接當作切片終點？
> 4. `Campus,,45` 分割後有幾欄？第一個失敗階段是什麼？
> 5. `DONE,1,30` 與兩端空白的 done，分別是資料還是命令？
> 6. `Campus,-1,abc` 與 `Campus,-1,0`，先出現哪一個錯誤？
> 7. A中有幾個碼位與 UTF-8 bytes？這能否當作 Python 物件完整大小？
> 8. 程式結束後，未儲存的 `total_km` 和編輯器儲存的測試檔，哪個有明確的持久保存機制？
>
> 投影片 exit ticket 另有：Why compare an uppercase copy but keep the original label case?

> [!solution]- 解答與理由
> 1. t 仍指向 Campus。`t=s` 只是增加綁定；後來改綁 s，不會原地修改舊字串。
> 2. 長度 8、TRIP、007。後綴是標籤拼寫，轉成 int 會變成 7 而失去前導零。
> 3. −1 在切片中表示最後一個位置之前，因此找不到逗號可能被誤解成「去掉最後一個字元」。先處理不存在的情況。
> 4. 三欄，中間欄位是空字串；欄位數檢查通過，但 float 空字串會造成解析錯誤。
> 5. `DONE,1,30` 是標籤為 DONE 的有效候選資料；整行清理後等於 DONE 的 done 是命令。
> 6. 前者先數值解析錯誤；後者解析成功後，先負距離錯誤，再也不進到時間錯誤。
> 7. 兩個碼位、四個 UTF-8 bytes；只描述文字長度與編碼 payload，不是物件 RAM 大小。
> 8. 已儲存的檔案。變數和螢幕輸出沒有自動變成保存的資料；Git 也只版本控制指定的檔案。

## D5 選讀：CSV、Unicode 比較與檔案輸入

對應投影片：Deck 5｜55–60。

> [!example] 範例：use a CSV parser when the grammar needs one（不同文法的選讀示例，不直接取代核心格式）
> ```python
> import csv
> line = '"Campus, East",12.5,45'
> fields = next(csv.reader([line]))
> print(fields)
> ```

> [!solution]- 輸出
> ```text
> ['Campus, East', '12.5', '45']
> ```
> The comma inside the quoted label is data, not a field boundary. 這個 parser 能辨識引號內的逗號，但仍不會替你驗證型態、單位、範圍或 DONE 政策。此例中的 list、next 與 CSV 只作延伸參考；要納入專題，必須更新規格和測試（A grammar change requires a new contract and tests for quotes, delimiters, and line breaks）。

> [!example] 範例：Unicode-aware comparison is a policy choice
> ```python
> import unicodedata
> a = "é"
> b = "é"
> print(a == b)
> print(unicodedata.normalize("NFC", a) ==
>       unicodedata.normalize("NFC", b))
> ```

> [!solution]- 輸出
> ```text
> False
> True
> ```
> NFC 可讓本例兩種標準等價拼寫在比較前成為一致的序列。`casefold` 也可用於某些更完整的 Unicode 大小寫比較。但這些不是通用身分辨識或語系排序規則；不應未經需求允許就改寫任意 ID。Keep a display value separate from a comparison key when the application needs both.

> [!example] 選讀唯讀示例：read saved UTF-8 text with an explicit encoding（從本例資料夾執行）
> ```python
> with open("samples/mixed_session.txt", "r",
>           encoding="utf-8") as source:
>     for raw_line in source:
>         line = raw_line.strip()
>         if line.upper() == "DONE":
>             break
>         print(repr(line))
> ```

範例套件附有這個合成測試檔。`with` 結束時會關閉檔案；不存在的路徑或解碼錯誤沒有被默默忽略。這段只讀與顯示，並沒有整合完整行程解析；若日後要做檔案版工具，還需要指定沒有 DONE、直接到 EOF 時的政策。A new input adapter can supply lines to the same text-processing pipeline. Saving a sample in the editor persists it. The core console tool does not automatically do that.

Reference：select the operation that answers the question（Do not memorize an API catalogue; connect each operation to its purpose）：

| Need | Operation / reminder |
| --- | --- |
| One position / a region | `s[i]` / `s[start:stop:step]` |
| Presence / prefix / suffix | `part in s` / `s.startswith(p)` / `s.endswith(p)` |
| First / last position | `s.find(part)` / `s.rfind(part)`; missing → −1 |
| Count occurrences | `s.count(part)`; non-overlapping matches |
| Edge trim / case comparison | `s.strip()` / `s.lower()` / `s.upper()` |
| Replace / split / join | `s.replace(a,b)` / `s.split(",")` / `",".join(fields)` |

Remember the result type: Boolean, index, string, or list of strings. 查詢方法時記得它們的結果型態：`in`、`startswith`、`endswith` 回答布林問題；`find`／`rfind` 回傳位置或 −1；`replace`／`strip` 回傳字串；`split` 回傳字串串列；`join` 以分隔符號組合字串。`strip("km")` 的引數是**一組可去除的邊界字元**，不是「移除整個 km 字尾」。

投影片所列的延伸閱讀：Python: text, indexing, and slicing；Python: string methods；Python: Unicode HOWTO；Python: csv module；Python: reading and writing files；Seagate: hard drives and SSDs。Corrected: immutability is not "assignment always makes a copy." The core tool is a small line parser — not general CSV, natural-language understanding, or a database.
