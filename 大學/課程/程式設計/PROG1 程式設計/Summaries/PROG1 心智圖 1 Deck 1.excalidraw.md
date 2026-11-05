---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Deck 1 整理]]"
  - "Midterm_Practice_Student.pdf（老師的 140 題例題，T001–T100、Q001–Q040）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
電腦如何解決問題
Deck 1・W1 ^4kCYzNT3

課程定位 ^XWTRZnJY

Not syntax-first：從問題出發，不是從指令 ^sDPeLM4B

AI 可以寫 code，但人要 define、inspect、test、
revise ^DP73xn83

學生做：預測輸出、跑程式、看錯誤、設計測試、小
修改 ^hWyK9pcR

AI 做：candidate solution、解釋錯誤、建議測試、
refactor ^dTijhYGT

人的責任：problem formulation、execution
reasoning、verification ^7MKzgeRx

Q1 什麼問題可以交給電腦解 ^vJ9LxXp6

Input → Process → Output ^M9vehhg9

例：Celsius C → C × 9/5 + 32 → Fahrenheit F ^tZRvESe4

寫 code 前先算：C = 0 → F = 32 ^GKtW9pgT

先定義問題，再問 AI ^nLjtbsAX

出生年 → 年齡：還要生日與參考日期 ^szfMavJY

score → pass/fail：要及格門檻 ^YZByFhRd

several numbers → average：資料集合＋空集合怎麼辦 ^UrBJW9PE

核心：AI 無法替你消除沒定義清楚的需求 ^gydKYmyn

Q2 電腦實際上在做什麼 ^fHZykYwu

Hardware（實體裝置）vs Software（告訴硬體做什
麼的程式） ^XnSbmGi5

四功能：Input／Storage／Computing／Output ^JbreVTMe

例：name = input("Name: ")、print("Hello", name) ^bHR6w8SC

按下 Run ^gMtGVkKt

file on storage → process in RAM → Python
runtime → CPU 執行 machine instructions →
output ^u7UdmsEL

概念模型；真實還有 cache、virtual memory、I/O
controller、DMA ^ghiYbYTV

Storage／RAM／CPU ^X2GCYc3P

Storage＝倉庫：長期保存 main.py ^GKxgmAyY

RAM＝工作桌：執行中的狀態與變數 ^Nv5Dif6s

CPU＝工作的人：load、store、arithmetic、branch ^EjFFQFZP

Key idea：執行狀態是暫時的，要保存就明確存檔 ^j6w6WtpC

為什麼 CPU 直接用 RAM ^Dgb5kBuJ

LOAD register, [address]、STORE [address],
register ^mGSxG8ZU

SSD／HDD 是 block I/O：OS／driver → controller
→ 搬進 RAM ^zpzwE4Yh

Fetch → Decode → Execute ^EvSpEcL7

⚠ 一行 Python ≠ 一個 CPU instruction ^2iSKx64h

★ 硬體是非題（cache、RISC／CISC、時脈、
DRAM）→ 見心智圖 6 ^vbJP6QAr

Q3 電腦如何表示資訊 ^ZUTdyYQH

data = value + type + operations ^TTbZ5GMZ

65／65.0／"65" → int／float／str ^9qEi6F7Q

同一組 bits，不同解讀 ^i3RwnWsJ

01000001 → unsigned 65 → ASCII 'A' ^syFJyPNV

chr(65) → A；ord('A') → 65 ^h86gKbEC

type 決定 + 的意思 ^tYhc6Jtu

65 + 1 → 66 ^pzvcFXnz

65.0 + 1 → 66.0 ^qh668EW7

"65" + "1" → "651" ^fqdwUMiW

⚠ "65" + 1 → TypeError ^8HNXpJcd

修：int("65") + 1 → 66；"65" + str(1) → 651 ^3qrVRS5i

★ 所有資料都是 0／1（T）；只看 byte 不知道意
義（F）；圖片音樂也是 0／1 ^Ppk7kwVG

Q4 什麼是 Program ^hgLNBcGb

Algorithm：清楚、有限、可執行的步驟 ^eqUNtPfE

Source code：algorithm 用程式語言的精確表達 ^6X77gK7V

Pseudocode first：Read C → Compute F →
Display F ^C8LQzCK5

精確性：BMI 要先定單位、公式、輸出 ^RAUb8eK4

好程式＝需求、algorithm、code、tests 彼此一致 ^MKuxURh5

Q5 Python 如何執行 ^ajnLi6PH

三個層次 ^qBpRqFiB

High-level：x = x + 1（描述要做什麼） ^fUJhsvz5

Assembly：MOV EAX, 65、ADD EAX, 1（一步一步怎
麼做） ^hxnspvpu

Machine language：CPU 解碼的 bit patterns；x86、
ARM、RISC-V 各不同 ^LJNExhuf

Compiler：source → compiler → machine code →
run（C／C++；翻一次跑多次） ^rVQrMPvq

Compilation vs Interpretation：不是互斥標籤 ^jZtA4sJt

CPython：source → parse／compile → bytecode
→ runtime 執行 ^iz3nVnkW

⚠ bytecode ≠ CPU machine code ^4dZ8NY6H

★⚠ 是非題「interpreter 翻成 machine language」：
2021 答 T，新講義判 F → 問老師 ^w6wvqH4J

Syntax error：整個 script 不會開始；Runtime
error：跑到一半失敗 ^Phhb4nkN

Interactive vs Script mode ^EyiBbVYM

>>> 3 + 5 顯示 8 ^Hdq5buP6

script 裡只寫 3 + 5 不顯示 → 要 print(3 + 5) ^eu8tijQn

⚠ >>> 打 Python；terminal 打 python main.py ^qeWg7bSF

開發迴圈：Edit → Save → Run → Inspect →
Revise ^MixTYRSU

Syntax／Expression／Statement ^kP8zmp3P

Syntax：文法；少冒號 → SyntaxError ^m2dCYBWy

Expression 產生值：3 + 5 → 8；10 > 3 → True ^La2eeukf

Statement 可執行：result = 3 + 5；整個 if 結構 ^kDj7swPd

print(result)＝expression statement；# 開始註解 ^3ZGVWeUQ

Variable：名字指向資料，不是數學未知數 ^pAPvCfmS

⚠ input() 一律回傳 str ^HsSMF77X

輸入 3、5：x + y → 35 ^SkQDeszb

修：float(input()) → 8.0〔C〕 ^h8BWik6A

Q6 AI 會寫 code，為什麼還要
學 ^yK4UYjW4

AI code＝candidate solution，不是答案證明 ^FPNCBegi

Ask → Inspect → Run → Test → Revise ^DnfPFmnA

故意錯誤 Celsius：c = input(...) → TypeError ^XcnamR3G

修：c = float(input("Celsius: ")) ^696sXF52

〔C〕錯在 / 5："0" * 9 是字串重複，不會錯 ^dQ9xW9DL

Test case＝specified input＋independently
justified expected result ^M6HyR3uL

0 → 32、100 → 212、−40 → −40 ^EV9LXmCW

AI 同意 AI ≠ independent oracle ^JCEqN5NY

通過測試是證據，不是證明 ^DX3bJSqx

開發循環：Understand → Design → Generate →
Run → Debug → Verify ^p3AjVQpu

三種錯誤 ^yXtvzSBC

Syntax：print("Hello" → 無法 parse ^2i2LhSru

Runtime：3 / 0 → ZeroDivisionError；"65" + 1 →
TypeError；print(hello) → NameError ^yeLyHTMp

Logic：0 * 9 / 5 + 30 → 能跑但錯（應 +32） ^sgDWGz7h

〔C〕實際印 30.0，不是 30 ^ib7P4kwk

★ 「多數 logic error IDE 直接抓得到」→ F ^m2tWN87Y

Debugging：Read error → Locate line →
Hypothesis → Test one fix ^ByYupu8T

AI 使用規範：可問解釋、candidate、最小修補、
測試；要自己跑、比對、記錄、保密 ^2hckAhT6

Practice ^wzNrx5Wy

Gross pay：gross = hours * pay ^8ptsvM2K

km → miles：miles = km * 0.621371；至少兩個自
己算的 test ^Rfk52uBz

Q7 Git 與 GitHub ^FsMZMj6A

version control：取代 main_final2.py 式手動版本 ^GWfbnSsx

Git（版本控制系統）≠ GitHub（遠端 hosting） ^QrPxG6MB

Repository＝project folder＋version history
（.git） ^WJ67fx4p

Save／Commit／Push ^LjzDamdj

Save：寫回本機檔案（Ctrl+S） ^A35MjH8t

Commit：local checkpoint＋message ^xUTMKWRp

Push：傳到 remote ^XncGssgp

流程：Edit + Save → Review + Commit → Push →
Verify online ^tkJbs3ba

commit 之後再改、再存，要重新 commit 才會被 push ^4QHKH66v

GitHub Desktop：第一次 Publish repository，之
後 Push origin ^RqBuL4rC

Verify online：看得到 main.py、最新 commit、第二
次修改 ^U3qgUd2v

不能 commit：密碼、API key、token、私人資料、
別人答案、未檢查的 AI transcript ^rc78fJU2

.gitignore 只擋未追蹤的檔；已 commit 的 secret →
revoke／rotate ^9pukLtAt

CLI：git init -b main → git add → git commit
-m → git remote add origin → git push -u origin
main ^WCY2YtMd

Q001 ^JcU95eeE

Q002 ^sMcPZkne

T002 ^bNHKk7Pa

T001 ^uVKq9viP

Q001 ^WjFKCGkn

T007 ^xEJjgTtr

T013 ^LSVrg2ja

T010 ^aVBwDQXQ

T086 ^3QMfaVkx

Q005 ^zsUhqKGS

Q003 ^qr84Fa63

T008 ^pvAkkRnM

T009 ^2ttnxixi

Q004 ^ASQkmGV7

T087 ^a2TguZv3

Q035 ^JSzGBQm4

PROG1 期中心智圖 1｜Deck 1：電腦如何解決問題（W1） ^BLUsN9kk

來源：PROG1 Deck 1 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的練
習題。 ^wPjss35v

★ 考古題考過 ^5ZsdNB3X

⚠ 易錯陷阱 ^JpdU3wEr

〔C〕Claude 補充（投影片與講義沒有） ^zAstH6Me

例題考到、原本心智圖沒有的觀念 ^H6F4uy3f

T001 Q001 ^GATYKYkx

老師例題題號 ^NrJ6ptZ4

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "XykXwLLL",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 1019.83,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1323457338,
			"version": 2,
			"versionNonce": 620815464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75,
					0
				],
				[
					75,
					-1019.83
				],
				[
					150,
					-1019.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "A6Pap8Rc",
			"type": "arrow",
			"x": 472.5,
			"y": -1019.83,
			"width": 76,
			"height": 148.37,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 869581924,
			"version": 2,
			"versionNonce": 1396438552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-148.37
				],
				[
					76,
					-148.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jbNgSCVi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "4qRZc36k",
			"type": "arrow",
			"x": 472.5,
			"y": -1019.83,
			"width": 76,
			"height": 82.62,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1158394392,
			"version": 2,
			"versionNonce": 121116520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-82.62
				],
				[
					76,
					-82.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ykBcj9gQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "ZVeeYZ2L",
			"type": "arrow",
			"x": 472.5,
			"y": -1019.83,
			"width": 76,
			"height": 5.62,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1822578913,
			"version": 2,
			"versionNonce": 965047064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-5.62
				],
				[
					76,
					-5.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LEpNcdzD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "Xi3jSYvJ",
			"type": "arrow",
			"x": 472.5,
			"y": -1019.83,
			"width": 76,
			"height": 71.38,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1130108666,
			"version": 2,
			"versionNonce": 571533928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					71.38
				],
				[
					76,
					71.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KPzGbYU2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "QR7WLzRC",
			"type": "arrow",
			"x": 472.5,
			"y": -1019.83,
			"width": 76,
			"height": 148.38,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1378035094,
			"version": 2,
			"versionNonce": 1939296280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					148.38
				],
				[
					76,
					148.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NnQdbZXZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "s7g8bq3h",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "4MA43Ccx",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 645.33,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 60903956,
			"version": 2,
			"versionNonce": 811031912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75,
					0
				],
				[
					75,
					-645.33
				],
				[
					150,
					-645.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Gb4Fs55x",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "4geMWNQE",
			"type": "arrow",
			"x": 685.5,
			"y": -645.33,
			"width": 76,
			"height": 109.62,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 40146806,
			"version": 2,
			"versionNonce": 694521112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-109.62
				],
				[
					76,
					-109.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Gb4Fs55x",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "viJme3p4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "pnTmBcZA",
			"type": "arrow",
			"x": 685.5,
			"y": -645.33,
			"width": 76,
			"height": 10.38,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2143205541,
			"version": 2,
			"versionNonce": 861368424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					10.38
				],
				[
					76,
					10.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Gb4Fs55x",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zYM3KGGk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "dZK3LKWL",
			"type": "arrow",
			"x": 685.5,
			"y": -645.33,
			"width": 76,
			"height": 109.63,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 887748119,
			"version": 2,
			"versionNonce": 1684285976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					109.63
				],
				[
					76,
					109.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Gb4Fs55x",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aESgGfRm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "JF8Yd5RT",
			"type": "arrow",
			"x": 1045.5,
			"y": -754.95,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 463677077,
			"version": 2,
			"versionNonce": 584917864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-24
				],
				[
					60,
					-24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "viJme3p4",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XZTUEjiQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "s4dusaUj",
			"type": "arrow",
			"x": 1045.5,
			"y": -754.95,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 532755814,
			"version": 2,
			"versionNonce": 1602692888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					24
				],
				[
					60,
					24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "viJme3p4",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "suCYFbkD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "P3bcz6WY",
			"type": "arrow",
			"x": 970.5,
			"y": -634.95,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1190996440,
			"version": 2,
			"versionNonce": 489977448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-48
				],
				[
					60,
					-48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYM3KGGk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ahR9VLEv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "qmeH9Luf",
			"type": "arrow",
			"x": 970.5,
			"y": -634.95,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 480327671,
			"version": 2,
			"versionNonce": 1463976984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYM3KGGk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EmBuQkqb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "9Ej9ZFuE",
			"type": "arrow",
			"x": 970.5,
			"y": -634.95,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1245354496,
			"version": 2,
			"versionNonce": 388589928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					48
				],
				[
					60,
					48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYM3KGGk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "n7D6pyZF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "6HX4RaA3",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 89.4,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1886369203,
			"version": 2,
			"versionNonce": 1502232856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75,
					0
				],
				[
					75,
					-89.4
				],
				[
					150,
					-89.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "sgYSpkf7",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 350.55,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2091795066,
			"version": 2,
			"versionNonce": 201849960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-350.55
				],
				[
					76,
					-350.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GV6K5uNB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "w2c9BLCJ",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 284.8,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1726517681,
			"version": 2,
			"versionNonce": 366108184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-284.8
				],
				[
					76,
					-284.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7g2ZwM3Q",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "5TCyeLp7",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 174.55,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1761938646,
			"version": 2,
			"versionNonce": 765210472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-174.55
				],
				[
					76,
					-174.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pMJT3nnN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "zVXSKcZT",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 3.85,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2135023602,
			"version": 2,
			"versionNonce": 755948312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					3.85
				],
				[
					76,
					3.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7U3EBELq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "7AyUhcwB",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 177.25,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1059578934,
			"version": 2,
			"versionNonce": 338821736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					177.25
				],
				[
					76,
					177.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WGETEJAC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "vLpYktAG",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 284.8,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1443437301,
			"version": 2,
			"versionNonce": 28555288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					284.8
				],
				[
					76,
					284.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7kWSbijP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "rjJmwxUB",
			"type": "arrow",
			"x": 642.5,
			"y": -89.4,
			"width": 76,
			"height": 350.55,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1277757444,
			"version": 2,
			"versionNonce": 1855288680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					350.55
				],
				[
					76,
					350.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eMvPfcSi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rp2vVJtD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "cfEh5nQy",
			"type": "arrow",
			"x": 1154.5,
			"y": -374.2,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1662172764,
			"version": 2,
			"versionNonce": 129299736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7g2ZwM3Q",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4fp6PERP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "9wfcZWTr",
			"type": "arrow",
			"x": 827.5,
			"y": -263.95,
			"width": 60,
			"height": 39,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 428721953,
			"version": 2,
			"versionNonce": 840075368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-39
				],
				[
					60,
					-39
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pMJT3nnN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "B5L3PuUi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "DfBmfJ6h",
			"type": "arrow",
			"x": 827.5,
			"y": -263.95,
			"width": 60,
			"height": 39,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1559383140,
			"version": 2,
			"versionNonce": 344363544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					39
				],
				[
					60,
					39
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pMJT3nnN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WBep3NGY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "MUavRDp9",
			"type": "arrow",
			"x": 935.5,
			"y": -85.55,
			"width": 60,
			"height": 81.4,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 8890278,
			"version": 2,
			"versionNonce": 1249196904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-81.4
				],
				[
					60,
					-81.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7U3EBELq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qKsaEMUm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "4VsDxaS2",
			"type": "arrow",
			"x": 935.5,
			"y": -85.55,
			"width": 60,
			"height": 33.4,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1349273942,
			"version": 2,
			"versionNonce": 790400792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-33.4
				],
				[
					60,
					-33.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7U3EBELq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "deeigukr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "9kM6Ckrk",
			"type": "arrow",
			"x": 935.5,
			"y": -85.55,
			"width": 60,
			"height": 14.6,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2013062075,
			"version": 2,
			"versionNonce": 1242140264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					14.6
				],
				[
					60,
					14.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7U3EBELq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ZQHdRmEV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "9NRVymvt",
			"type": "arrow",
			"x": 935.5,
			"y": -85.55,
			"width": 60,
			"height": 81.4,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 940016194,
			"version": 2,
			"versionNonce": 1609231384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					81.4
				],
				[
					60,
					81.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7U3EBELq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9nhrtuCh",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "kCune5dT",
			"type": "arrow",
			"x": 961.5,
			"y": 87.85,
			"width": 60,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 989393638,
			"version": 2,
			"versionNonce": 429621608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-34
				],
				[
					60,
					-34
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "WGETEJAC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "M9V8XmX3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "bSGecR5N",
			"type": "arrow",
			"x": 961.5,
			"y": 87.85,
			"width": 60,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 814521231,
			"version": 2,
			"versionNonce": 15051032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					34
				],
				[
					60,
					34
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "WGETEJAC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tXSfhm38",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "VpP46cdH",
			"type": "arrow",
			"x": 1007.5,
			"y": 195.4,
			"width": 60,
			"height": 3.25,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 755757856,
			"version": 2,
			"versionNonce": 678892648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					3.25
				],
				[
					60,
					3.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7kWSbijP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eyRfmTRt",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "DyxfnSwA",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 585.02,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 343563419,
			"version": 2,
			"versionNonce": 226543128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75,
					0
				],
				[
					75,
					585.02
				],
				[
					150,
					585.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "yQDyydAL",
			"type": "arrow",
			"x": 615.5,
			"y": 585.02,
			"width": 76,
			"height": 228.12,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2100823516,
			"version": 2,
			"versionNonce": 476596072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-228.12
				],
				[
					76,
					-228.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wajLgwUy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "uZSMyaqb",
			"type": "arrow",
			"x": 615.5,
			"y": 585.02,
			"width": 76,
			"height": 173.62,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 294821802,
			"version": 2,
			"versionNonce": 1924154136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-173.62
				],
				[
					76,
					-173.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YszYzcAn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "H7CV7JF6",
			"type": "arrow",
			"x": 615.5,
			"y": 585.02,
			"width": 76,
			"height": 98.37,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 521506422,
			"version": 2,
			"versionNonce": 29039208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-98.37
				],
				[
					76,
					-98.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YqZGSDX6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "qyp726g8",
			"type": "arrow",
			"x": 615.5,
			"y": 585.02,
			"width": 76,
			"height": 69.63,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 181218071,
			"version": 2,
			"versionNonce": 1592270872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					69.63
				],
				[
					76,
					69.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "WeLBZ9yB",
			"type": "arrow",
			"x": 615.5,
			"y": 585.02,
			"width": 76,
			"height": 228.13,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 491681826,
			"version": 2,
			"versionNonce": 2067500392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					228.13
				],
				[
					76,
					228.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ypZCrq87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BmzN3NYE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "KLJ3hqHz",
			"type": "arrow",
			"x": 912.5,
			"y": 486.65,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1822229339,
			"version": 2,
			"versionNonce": 303848728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-24
				],
				[
					60,
					-24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YqZGSDX6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "udUKCg2V",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "7BirrV88",
			"type": "arrow",
			"x": 912.5,
			"y": 486.65,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1193180082,
			"version": 2,
			"versionNonce": 1916117096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					24
				],
				[
					60,
					24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YqZGSDX6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MyrpaamM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "nWZFjcwu",
			"type": "arrow",
			"x": 887.5,
			"y": 654.65,
			"width": 60,
			"height": 96,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1013624294,
			"version": 2,
			"versionNonce": 767621656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-96
				],
				[
					60,
					-96
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gtKh5ai8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "sM3tC8dB",
			"type": "arrow",
			"x": 887.5,
			"y": 654.65,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1100037128,
			"version": 2,
			"versionNonce": 1182094184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					-48
				],
				[
					60,
					-48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "k3bB7tDB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "a54dMaCt",
			"type": "arrow",
			"x": 887.5,
			"y": 654.65,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 845369681,
			"version": 2,
			"versionNonce": 80344856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "W2wFMzxz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "KhhvuM9B",
			"type": "arrow",
			"x": 887.5,
			"y": 654.65,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 291809514,
			"version": 2,
			"versionNonce": 2118559336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					48
				],
				[
					60,
					48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "AHN7Xrw5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "nyLskJMw",
			"type": "arrow",
			"x": 887.5,
			"y": 654.65,
			"width": 60,
			"height": 96,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 221000227,
			"version": 2,
			"versionNonce": 1806390296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					30,
					0
				],
				[
					30,
					96
				],
				[
					60,
					96
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eLVSwH22",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6Vcg4hfE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "H3RdLPXR",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 1038.55,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 767899914,
			"version": 2,
			"versionNonce": 1987418472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					75,
					0
				],
				[
					75,
					1038.55
				],
				[
					150,
					1038.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "trEmvfbN",
			"type": "arrow",
			"x": 597.5,
			"y": 1038.55,
			"width": 76,
			"height": 129.65,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2090873109,
			"version": 2,
			"versionNonce": 140054808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-129.65
				],
				[
					76,
					-129.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "G2cfXRXX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "vTnZngFQ",
			"type": "arrow",
			"x": 597.5,
			"y": 1038.55,
			"width": 76,
			"height": 75.15,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1813495507,
			"version": 2,
			"versionNonce": 307113064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					-75.15
				],
				[
					76,
					-75.15
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Vz5FHX7C",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "HAt6Hzef",
			"type": "arrow",
			"x": 597.5,
			"y": 1038.55,
			"width": 76,
			"height": 9.4,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1467839190,
			"version": 2,
			"versionNonce": 575090200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					9.4
				],
				[
					76,
					9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WwsiVBPz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "t6PBMwKY",
			"type": "arrow",
			"x": 597.5,
			"y": 1038.55,
			"width": 76,
			"height": 75.15,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 132330419,
			"version": 2,
			"versionNonce": 1805410152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					75.15
				],
				[
					76,
					75.15
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3pMeEhUA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "RaKdW22a",
			"type": "arrow",
			"x": 597.5,
			"y": 1038.55,
			"width": 76,
			"height": 129.65,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1542464609,
			"version": 2,
			"versionNonce": 1919527704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					38,
					0
				],
				[
					38,
					129.65
				],
				[
					76,
					129.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bi7mVPx7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YN4MzDdV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "w7HusntV",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 941.3,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1595720288,
			"version": 2,
			"versionNonce": 44839528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-75,
					0
				],
				[
					-75,
					-941.3
				],
				[
					-150,
					-941.3
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "e6uUafqW",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 468.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 844344038,
			"version": 2,
			"versionNonce": 1932822552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-468.5
				],
				[
					-76,
					-468.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KZxM2vHn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "YNdR7TwS",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 333,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 337737532,
			"version": 2,
			"versionNonce": 1850320232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-333
				],
				[
					-76,
					-333
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5QmZZ2zd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "GhMCeLpN",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 267.25,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 339728898,
			"version": 2,
			"versionNonce": 815514904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-267.25
				],
				[
					-76,
					-267.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "J4vSLtdb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "wjPk3zcX",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 182.7,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1081888648,
			"version": 2,
			"versionNonce": 197179496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-182.7
				],
				[
					-76,
					-182.7
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "L39dXeYq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "MmPDykwY",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 85.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 516340473,
			"version": 2,
			"versionNonce": 403923480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-85.5
				],
				[
					-76,
					-85.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gzdUDis2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "ipndTquz",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 25,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 34385488,
			"version": 2,
			"versionNonce": 786262888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					25
				],
				[
					-76,
					25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "M4gYkEET",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "vcphvwxF",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 135.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2056835563,
			"version": 2,
			"versionNonce": 1217355544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					135.5
				],
				[
					-76,
					135.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PcPCmgS5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "RfzVFMvd",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 270,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 961577057,
			"version": 2,
			"versionNonce": 1374404200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					270
				],
				[
					-76,
					270
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "T3fS7hUk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "fMH7bhxk",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 393.25,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2098741112,
			"version": 2,
			"versionNonce": 1652800536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					393.25
				],
				[
					-76,
					393.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MkVZ6LAm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "ufbLg7yX",
			"type": "arrow",
			"x": -612.5,
			"y": -941.3,
			"width": 76,
			"height": 468.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 328100326,
			"version": 2,
			"versionNonce": 1169666408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					468.5
				],
				[
					-76,
					468.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eV5WWD9i",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8MkLvUmp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "YtscKUgS",
			"type": "arrow",
			"x": -793.5,
			"y": -1409.8,
			"width": 60,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1382560889,
			"version": 2,
			"versionNonce": 1474591000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-63
				],
				[
					-60,
					-63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KZxM2vHn",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sZ7KeEp2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "2V2y3iLB",
			"type": "arrow",
			"x": -793.5,
			"y": -1409.8,
			"width": 60,
			"height": 5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1258226653,
			"version": 2,
			"versionNonce": 1636648040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-5
				],
				[
					-60,
					-5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KZxM2vHn",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ppgXTqP3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "85nvnt5P",
			"type": "arrow",
			"x": -793.5,
			"y": -1409.8,
			"width": 60,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 60048641,
			"version": 2,
			"versionNonce": 1009096216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					63
				],
				[
					-60,
					63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KZxM2vHn",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9aV8sumK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "6pVGWq3n",
			"type": "arrow",
			"x": -1148.5,
			"y": -1124,
			"width": 60,
			"height": 33.3,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 574721489,
			"version": 2,
			"versionNonce": 859338600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-33.3
				],
				[
					-60,
					-33.3
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "L39dXeYq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NUcUckYW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "fGYE77su",
			"type": "arrow",
			"x": -1148.5,
			"y": -1124,
			"width": 60,
			"height": 24.7,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1279629814,
			"version": 2,
			"versionNonce": 339415832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					24.7
				],
				[
					-60,
					24.7
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "L39dXeYq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VuhYmUYz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "SKbiAQaZ",
			"type": "arrow",
			"x": -960.5,
			"y": -916.3,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1730092686,
			"version": 2,
			"versionNonce": 788875880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-48
				],
				[
					-60,
					-48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "M4gYkEET",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LYN7qgth",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "6V8geGgR",
			"type": "arrow",
			"x": -960.5,
			"y": -916.3,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1186143743,
			"version": 2,
			"versionNonce": 647557144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "M4gYkEET",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eMkdaZGE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "VUrMv32N",
			"type": "arrow",
			"x": -960.5,
			"y": -916.3,
			"width": 60,
			"height": 48,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1756655950,
			"version": 2,
			"versionNonce": 1606401384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					48
				],
				[
					-60,
					48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "M4gYkEET",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TjWaFXNy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "WH9S4uA4",
			"type": "arrow",
			"x": -1010.5,
			"y": -671.3,
			"width": 60,
			"height": 72,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1364106456,
			"version": 2,
			"versionNonce": 1261645080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-72
				],
				[
					-60,
					-72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "T3fS7hUk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JDVabgEY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "T7cgfWZB",
			"type": "arrow",
			"x": -1010.5,
			"y": -671.3,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 921308906,
			"version": 2,
			"versionNonce": 380883048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-24
				],
				[
					-60,
					-24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "T3fS7hUk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5vtfX88Y",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0A"
		},
		{
			"id": "cEZNxNKv",
			"type": "arrow",
			"x": -1010.5,
			"y": -671.3,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1743653606,
			"version": 2,
			"versionNonce": 998099480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					24
				],
				[
					-60,
					24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "T3fS7hUk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VHRkAvwa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0B"
		},
		{
			"id": "rfTjq2ka",
			"type": "arrow",
			"x": -1010.5,
			"y": -671.3,
			"width": 60,
			"height": 72,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1673196947,
			"version": 2,
			"versionNonce": 464356200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					72
				],
				[
					-60,
					72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "T3fS7hUk",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wXGedvi8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0C"
		},
		{
			"id": "25nYTFwy",
			"type": "arrow",
			"x": -922.5,
			"y": -472.8,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 338551150,
			"version": 2,
			"versionNonce": 1651296024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-24
				],
				[
					-60,
					-24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8MkLvUmp",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ztSyAuDp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0D"
		},
		{
			"id": "wKTSS3CF",
			"type": "arrow",
			"x": -922.5,
			"y": -472.8,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1274093248,
			"version": 2,
			"versionNonce": 1559811688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					24
				],
				[
					-60,
					24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8MkLvUmp",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xveF7gex",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0E"
		},
		{
			"id": "dab5y9dW",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 23.78,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2103104847,
			"version": 2,
			"versionNonce": 745808920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-75,
					0
				],
				[
					-75,
					23.78
				],
				[
					-150,
					23.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0F"
		},
		{
			"id": "L96FGfxm",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 391.33,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 22923170,
			"version": 2,
			"versionNonce": 526502248,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-391.33
				],
				[
					-76,
					-391.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "36QqdkxA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0G"
		},
		{
			"id": "42GGQYJ2",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 336.83,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 770712349,
			"version": 2,
			"versionNonce": 1468522776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-336.83
				],
				[
					-76,
					-336.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bXGrSrey",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0H"
		},
		{
			"id": "qhMxKqm4",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 261.58,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1580471658,
			"version": 2,
			"versionNonce": 775183464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-261.58
				],
				[
					-76,
					-261.58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sSJDx3rS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0I"
		},
		{
			"id": "ibFYjWie",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 122.78,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1190115329,
			"version": 2,
			"versionNonce": 1125907992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-122.78
				],
				[
					-76,
					-122.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dGtWMPnG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0J"
		},
		{
			"id": "NHFkcdry",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 6.52,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2140173546,
			"version": 2,
			"versionNonce": 188518248,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					6.52
				],
				[
					-76,
					6.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7KZ2PY4v",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0K"
		},
		{
			"id": "YXbufHSR",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 160.42,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1917359766,
			"version": 2,
			"versionNonce": 1076132632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					160.42
				],
				[
					-76,
					160.42
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2VvKCidz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0L"
		},
		{
			"id": "6VP2Dx3C",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 314.32,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1482035696,
			"version": 2,
			"versionNonce": 516317800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					314.32
				],
				[
					-76,
					314.32
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "k95qc93B",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0M"
		},
		{
			"id": "uFg6D5DF",
			"type": "arrow",
			"x": -721.5,
			"y": 23.78,
			"width": 76,
			"height": 391.32,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 772183081,
			"version": 2,
			"versionNonce": 1628788760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					391.32
				],
				[
					-76,
					391.32
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Q3BPgEV6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7Z3cae74",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0N"
		},
		{
			"id": "V45R6Snf",
			"type": "arrow",
			"x": -1223.5,
			"y": -237.8,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 633029542,
			"version": 2,
			"versionNonce": 1738397032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-24
				],
				[
					-60,
					-24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sSJDx3rS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "t9hhJ3de",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0O"
		},
		{
			"id": "9VPz9EAA",
			"type": "arrow",
			"x": -1223.5,
			"y": -237.8,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 650291333,
			"version": 2,
			"versionNonce": 1239586072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					24
				],
				[
					-60,
					24
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sSJDx3rS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qaniQwDL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0P"
		},
		{
			"id": "YTEarLvi",
			"type": "arrow",
			"x": -1208.5,
			"y": -99,
			"width": 60,
			"height": 66.8,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 986923351,
			"version": 2,
			"versionNonce": 722397288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-66.8
				],
				[
					-60,
					-66.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dGtWMPnG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SsR55Axy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Q"
		},
		{
			"id": "mzRADRzq",
			"type": "arrow",
			"x": -1208.5,
			"y": -99,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1356178327,
			"version": 2,
			"versionNonce": 12824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dGtWMPnG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zbsWP2Kv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0R"
		},
		{
			"id": "VYiE5Hhh",
			"type": "arrow",
			"x": -1208.5,
			"y": -99,
			"width": 60,
			"height": 66.8,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1643577183,
			"version": 2,
			"versionNonce": 619027304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					66.8
				],
				[
					-60,
					66.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dGtWMPnG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HtnKfsti",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0S"
		},
		{
			"id": "yf75aEP2",
			"type": "arrow",
			"x": -902.5,
			"y": 184.2,
			"width": 60,
			"height": 91.4,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 692085065,
			"version": 2,
			"versionNonce": 979513112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-91.4
				],
				[
					-60,
					-91.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "2VvKCidz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "53jydubM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0T"
		},
		{
			"id": "BnENnCRW",
			"type": "arrow",
			"x": -902.5,
			"y": 184.2,
			"width": 60,
			"height": 33.4,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1511663367,
			"version": 2,
			"versionNonce": 929951336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-33.4
				],
				[
					-60,
					-33.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "2VvKCidz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8qfYyzUy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0U"
		},
		{
			"id": "ADePJMJc",
			"type": "arrow",
			"x": -902.5,
			"y": 184.2,
			"width": 60,
			"height": 24.6,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1401711603,
			"version": 2,
			"versionNonce": 830245912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					24.6
				],
				[
					-60,
					24.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "2VvKCidz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "H92xwVXa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0V"
		},
		{
			"id": "Us8dUaGA",
			"type": "arrow",
			"x": -902.5,
			"y": 184.2,
			"width": 60,
			"height": 91.4,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 360653239,
			"version": 2,
			"versionNonce": 460579176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					91.4
				],
				[
					-60,
					91.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "2VvKCidz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9xUAN7W4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0W"
		},
		{
			"id": "rFyKbhjt",
			"type": "arrow",
			"x": -1346.5,
			"y": 208.8,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1930924182,
			"version": 2,
			"versionNonce": 1866680600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "H92xwVXa",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EQc8nfZW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0X"
		},
		{
			"id": "3Hpf9Hem",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 543.73,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2047361826,
			"version": 2,
			"versionNonce": 272856168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-75,
					0
				],
				[
					-75,
					543.73
				],
				[
					-150,
					543.73
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4EkgSF7R",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Y"
		},
		{
			"id": "Y7VRynyy",
			"type": "arrow",
			"x": -472.5,
			"y": 543.73,
			"width": 76,
			"height": 32.88,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 535095278,
			"version": 2,
			"versionNonce": 522872344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-32.88
				],
				[
					-76,
					-32.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4EkgSF7R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "hU7BiJ48",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Z"
		},
		{
			"id": "uvRL4nCi",
			"type": "arrow",
			"x": -472.5,
			"y": 543.73,
			"width": 76,
			"height": 32.87,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1236663754,
			"version": 2,
			"versionNonce": 195602280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					32.87
				],
				[
					-76,
					32.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4EkgSF7R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2CNBgvnv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0a"
		},
		{
			"id": "8RSSvEzH",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 1059.7,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 3,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1151180103,
			"version": 2,
			"versionNonce": 1579541272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-75,
					0
				],
				[
					-75,
					1059.7
				],
				[
					-150,
					1059.7
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4d22n9fM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0b"
		},
		{
			"id": "Q7watCAn",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 387.35,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2046972098,
			"version": 2,
			"versionNonce": 1777302120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-387.35
				],
				[
					-76,
					-387.35
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qwC2XFd2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0c"
		},
		{
			"id": "GnbaQCfz",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 332.85,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 221099788,
			"version": 2,
			"versionNonce": 178896920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-332.85
				],
				[
					-76,
					-332.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "v5kmFtPP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0d"
		},
		{
			"id": "bS4LcSNQ",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 267.1,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1780733263,
			"version": 2,
			"versionNonce": 501476712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-267.1
				],
				[
					-76,
					-267.1
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ZQ55Ex4Z",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0e"
		},
		{
			"id": "8hkZivUE",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 70.4,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 265147179,
			"version": 2,
			"versionNonce": 346684696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					-70.4
				],
				[
					-76,
					-70.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0f"
		},
		{
			"id": "7gwfDddQ",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 126.3,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 988239489,
			"version": 2,
			"versionNonce": 1624375400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					126.3
				],
				[
					-76,
					126.3
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NZxhhgD6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0g"
		},
		{
			"id": "Zttx9Xr2",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 222.1,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1778877207,
			"version": 2,
			"versionNonce": 1301977624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					222.1
				],
				[
					-76,
					222.1
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "D29sHNTm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0h"
		},
		{
			"id": "625nSLpm",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 299.1,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 579772181,
			"version": 2,
			"versionNonce": 1652929384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					299.1
				],
				[
					-76,
					299.1
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JeTAY4FC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0i"
		},
		{
			"id": "3ZmP6jti",
			"type": "arrow",
			"x": -580.5,
			"y": 1059.7,
			"width": 76,
			"height": 387.35,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 759490429,
			"version": 2,
			"versionNonce": 946837272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-38,
					0
				],
				[
					-38,
					387.35
				],
				[
					-76,
					387.35
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "fTacMbVR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JNT3xBRn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0j"
		},
		{
			"id": "E4A8WdMJ",
			"type": "arrow",
			"x": -871.5,
			"y": 989.3,
			"width": 60,
			"height": 134.2,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1263579848,
			"version": 2,
			"versionNonce": 2034959976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-134.2
				],
				[
					-60,
					-134.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8Y4fkQTj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0k"
		},
		{
			"id": "efN33tme",
			"type": "arrow",
			"x": -871.5,
			"y": 989.3,
			"width": 60,
			"height": 67.4,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 67598306,
			"version": 2,
			"versionNonce": 1503458328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-67.4
				],
				[
					-60,
					-67.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HsWXd9ch",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0l"
		},
		{
			"id": "PnVt6d6y",
			"type": "arrow",
			"x": -871.5,
			"y": 989.3,
			"width": 60,
			"height": 0.6,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 580120438,
			"version": 2,
			"versionNonce": 1374550376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					-0.6
				],
				[
					-60,
					-0.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xC9NrDtg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0m"
		},
		{
			"id": "dhZSaF74",
			"type": "arrow",
			"x": -871.5,
			"y": 989.3,
			"width": 60,
			"height": 57.4,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1104178511,
			"version": 2,
			"versionNonce": 118927640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					57.4
				],
				[
					-60,
					57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vEBmcvzL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0n"
		},
		{
			"id": "VTsxDA4w",
			"type": "arrow",
			"x": -871.5,
			"y": 989.3,
			"width": 60,
			"height": 134.2,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1911147843,
			"version": 2,
			"versionNonce": 532319336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-30,
					0
				],
				[
					-30,
					134.2
				],
				[
					-60,
					134.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CeecciQr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yRsJ3Xv4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0o"
		},
		{
			"id": "iwes5587",
			"type": "arrow",
			"x": -1118.5,
			"y": 1358.8,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2103575353,
			"version": 2,
			"versionNonce": 944819736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-60,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JeTAY4FC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jFWBDia4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0p"
		},
		{
			"id": "4d22n9fM",
			"type": "rectangle",
			"x": -181.5,
			"y": -67,
			"width": 363,
			"height": 134,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#343a40",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1938087759,
			"version": 2,
			"versionNonce": 1283243880,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4kCYzNT3"
				},
				{
					"type": "arrow",
					"id": "XykXwLLL"
				},
				{
					"type": "arrow",
					"id": "4MA43Ccx"
				},
				{
					"type": "arrow",
					"id": "6HX4RaA3"
				},
				{
					"type": "arrow",
					"id": "DyxfnSwA"
				},
				{
					"type": "arrow",
					"id": "H3RdLPXR"
				},
				{
					"type": "arrow",
					"id": "w7HusntV"
				},
				{
					"type": "arrow",
					"id": "dab5y9dW"
				},
				{
					"type": "arrow",
					"id": "3Hpf9Hem"
				},
				{
					"type": "arrow",
					"id": "8RSSvEzH"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b0q"
		},
		{
			"id": "4kCYzNT3",
			"type": "text",
			"x": -149.5,
			"y": -45,
			"width": 299,
			"height": 90,
			"angle": 0,
			"strokeColor": "#ffffff",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 860979153,
			"version": 2,
			"versionNonce": 1446988568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "電腦如何解決問題\nDeck 1・W1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4d22n9fM",
			"originalText": "電腦如何解決問題\nDeck 1・W1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0r"
		},
		{
			"id": "NnQdbZXZ",
			"type": "rectangle",
			"x": 331.5,
			"y": -1046.83,
			"width": 141,
			"height": 54,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1980350259,
			"version": 2,
			"versionNonce": 679514728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XWTRZnJY"
				},
				{
					"type": "arrow",
					"id": "XykXwLLL"
				},
				{
					"type": "arrow",
					"id": "A6Pap8Rc"
				},
				{
					"type": "arrow",
					"id": "4qRZc36k"
				},
				{
					"type": "arrow",
					"id": "ZVeeYZ2L"
				},
				{
					"type": "arrow",
					"id": "Xi3jSYvJ"
				},
				{
					"type": "arrow",
					"id": "QR7WLzRC"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b0s"
		},
		{
			"id": "XWTRZnJY",
			"type": "text",
			"x": 351.5,
			"y": -1034.83,
			"width": 101,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1922061974,
			"version": 2,
			"versionNonce": 190195736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "課程定位",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NnQdbZXZ",
			"originalText": "課程定位",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0t"
		},
		{
			"id": "jbNgSCVi",
			"type": "rectangle",
			"x": 548.5,
			"y": -1188.45,
			"width": 404,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 214012859,
			"version": 2,
			"versionNonce": 445777256,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sDPeLM4B"
				},
				{
					"type": "arrow",
					"id": "A6Pap8Rc"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b0u"
		},
		{
			"id": "sDPeLM4B",
			"type": "text",
			"x": 562.5,
			"y": -1179.45,
			"width": 376,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 191702479,
			"version": 2,
			"versionNonce": 327771416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Not syntax-first：從問題出發，不是從指令",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jbNgSCVi",
			"originalText": "Not syntax-first：從問題出發，不是從指令",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0v"
		},
		{
			"id": "ykBcj9gQ",
			"type": "rectangle",
			"x": 548.5,
			"y": -1133.95,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 453744708,
			"version": 2,
			"versionNonce": 1341986920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DP73xn83"
				},
				{
					"type": "arrow",
					"id": "4qRZc36k"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b0w"
		},
		{
			"id": "DP73xn83",
			"type": "text",
			"x": 562.5,
			"y": -1124.95,
			"width": 433,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1808747346,
			"version": 2,
			"versionNonce": 206373400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI 可以寫 code，但人要 define、inspect、test、\nrevise",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ykBcj9gQ",
			"originalText": "AI 可以寫 code，但人要 define、inspect、test、\nrevise",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0x"
		},
		{
			"id": "LEpNcdzD",
			"type": "rectangle",
			"x": 548.5,
			"y": -1056.95,
			"width": 457,
			"height": 63,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 391329588,
			"version": 2,
			"versionNonce": 1821231976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hWyK9pcR"
				},
				{
					"type": "arrow",
					"id": "ZVeeYZ2L"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b0y"
		},
		{
			"id": "hWyK9pcR",
			"type": "text",
			"x": 562.5,
			"y": -1047.95,
			"width": 429,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 191576248,
			"version": 2,
			"versionNonce": 1150615320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "學生做：預測輸出、跑程式、看錯誤、設計測試、小\n修改",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LEpNcdzD",
			"originalText": "學生做：預測輸出、跑程式、看錯誤、設計測試、小\n修改",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0z"
		},
		{
			"id": "KPzGbYU2",
			"type": "rectangle",
			"x": 548.5,
			"y": -979.95,
			"width": 468,
			"height": 63,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1807111521,
			"version": 2,
			"versionNonce": 982523496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dTijhYGT"
				},
				{
					"type": "arrow",
					"id": "Xi3jSYvJ"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b10"
		},
		{
			"id": "dTijhYGT",
			"type": "text",
			"x": 562.5,
			"y": -970.95,
			"width": 440,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1763393085,
			"version": 2,
			"versionNonce": 215309336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI 做：candidate solution、解釋錯誤、建議測試、\nrefactor",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KPzGbYU2",
			"originalText": "AI 做：candidate solution、解釋錯誤、建議測試、\nrefactor",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b11"
		},
		{
			"id": "s7g8bq3h",
			"type": "rectangle",
			"x": 548.5,
			"y": -902.95,
			"width": 402,
			"height": 63,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1041977393,
			"version": 2,
			"versionNonce": 1523585384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7MKzgeRx"
				},
				{
					"type": "arrow",
					"id": "QR7WLzRC"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b12"
		},
		{
			"id": "7MKzgeRx",
			"type": "text",
			"x": 562.5,
			"y": -893.95,
			"width": 374,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1135105393,
			"version": 2,
			"versionNonce": 117578008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "人的責任：problem formulation、execution\nreasoning、verification",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "s7g8bq3h",
			"originalText": "人的責任：problem formulation、execution\nreasoning、verification",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b13"
		},
		{
			"id": "Gb4Fs55x",
			"type": "rectangle",
			"x": 331.5,
			"y": -672.33,
			"width": 354,
			"height": 54,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#b2f2bb",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1051277575,
			"version": 2,
			"versionNonce": 1956226152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vJ9LxXp6"
				},
				{
					"type": "arrow",
					"id": "4MA43Ccx"
				},
				{
					"type": "arrow",
					"id": "4geMWNQE"
				},
				{
					"type": "arrow",
					"id": "pnTmBcZA"
				},
				{
					"type": "arrow",
					"id": "dZK3LKWL"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b14"
		},
		{
			"id": "vJ9LxXp6",
			"type": "text",
			"x": 351.5,
			"y": -660.33,
			"width": 314,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 212583737,
			"version": 2,
			"versionNonce": 1989096984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q1 什麼問題可以交給電腦解",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Gb4Fs55x",
			"originalText": "Q1 什麼問題可以交給電腦解",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b15"
		},
		{
			"id": "viJme3p4",
			"type": "rectangle",
			"x": 761.5,
			"y": -775.2,
			"width": 284,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"YrUenJFB"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2041053472,
			"version": 2,
			"versionNonce": 1706612584,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "M9vehhg9"
				},
				{
					"type": "arrow",
					"id": "4geMWNQE"
				},
				{
					"type": "arrow",
					"id": "JF8Yd5RT"
				},
				{
					"type": "arrow",
					"id": "s4dusaUj"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b16"
		},
		{
			"id": "M9vehhg9",
			"type": "text",
			"x": 775.5,
			"y": -766.2,
			"width": 256,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YrUenJFB"
			],
			"frameId": null,
			"roundness": null,
			"seed": 182416997,
			"version": 2,
			"versionNonce": 275821336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Input → Process → Output",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "viJme3p4",
			"originalText": "Input → Process → Output",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b17"
		},
		{
			"id": "XZTUEjiQ",
			"type": "rectangle",
			"x": 1105.5,
			"y": -795.95,
			"width": 398,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 134868298,
			"version": 2,
			"versionNonce": 1920576104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tZRvESe4"
				},
				{
					"type": "arrow",
					"id": "JF8Yd5RT"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b18"
		},
		{
			"id": "tZRvESe4",
			"type": "text",
			"x": 1117.5,
			"y": -788.95,
			"width": 374,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1039409854,
			"version": 2,
			"versionNonce": 1260032024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例：Celsius C → C × 9/5 + 32 → Fahrenheit F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XZTUEjiQ",
			"originalText": "例：Celsius C → C × 9/5 + 32 → Fahrenheit F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b19"
		},
		{
			"id": "suCYFbkD",
			"type": "rectangle",
			"x": 1105.5,
			"y": -747.95,
			"width": 287,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2065618641,
			"version": 2,
			"versionNonce": 1973951848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GKtW9pgT"
				},
				{
					"type": "arrow",
					"id": "s4dusaUj"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1A"
		},
		{
			"id": "GKtW9pgT",
			"type": "text",
			"x": 1117.5,
			"y": -740.95,
			"width": 263,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1106379725,
			"version": 2,
			"versionNonce": 780193048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "寫 code 前先算：C = 0 → F = 32",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "suCYFbkD",
			"originalText": "寫 code 前先算：C = 0 → F = 32",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1B"
		},
		{
			"id": "zYM3KGGk",
			"type": "rectangle",
			"x": 761.5,
			"y": -655.2,
			"width": 209,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1103725844,
			"version": 2,
			"versionNonce": 277885032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nLjtbsAX"
				},
				{
					"type": "arrow",
					"id": "pnTmBcZA"
				},
				{
					"type": "arrow",
					"id": "P3bcz6WY"
				},
				{
					"type": "arrow",
					"id": "qmeH9Luf"
				},
				{
					"type": "arrow",
					"id": "9Ej9ZFuE"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1C"
		},
		{
			"id": "nLjtbsAX",
			"type": "text",
			"x": 775.5,
			"y": -646.2,
			"width": 181,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1814919724,
			"version": 2,
			"versionNonce": 605514264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "先定義問題，再問 AI",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zYM3KGGk",
			"originalText": "先定義問題，再問 AI",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1D"
		},
		{
			"id": "ahR9VLEv",
			"type": "rectangle",
			"x": 1030.5,
			"y": -699.95,
			"width": 303,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1976768833,
			"version": 2,
			"versionNonce": 1526588264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "szfMavJY"
				},
				{
					"type": "arrow",
					"id": "P3bcz6WY"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "szfMavJY",
			"type": "text",
			"x": 1042.5,
			"y": -692.95,
			"width": 279,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1526219578,
			"version": 2,
			"versionNonce": 1188194072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "出生年 → 年齡：還要生日與參考日期",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ahR9VLEv",
			"originalText": "出生年 → 年齡：還要生日與參考日期",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "EmBuQkqb",
			"type": "rectangle",
			"x": 1030.5,
			"y": -651.95,
			"width": 268,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1138911848,
			"version": 2,
			"versionNonce": 322778728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YZByFhRd"
				},
				{
					"type": "arrow",
					"id": "qmeH9Luf"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "YZByFhRd",
			"type": "text",
			"x": 1042.5,
			"y": -644.95,
			"width": 244,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1332902137,
			"version": 2,
			"versionNonce": 858113048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "score → pass/fail：要及格門檻",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EmBuQkqb",
			"originalText": "score → pass/fail：要及格門檻",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "n7D6pyZF",
			"type": "rectangle",
			"x": 1030.5,
			"y": -603.95,
			"width": 438,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 256647828,
			"version": 2,
			"versionNonce": 1310337384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UrBJW9PE"
				},
				{
					"type": "arrow",
					"id": "9Ej9ZFuE"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "UrBJW9PE",
			"type": "text",
			"x": 1042.5,
			"y": -596.95,
			"width": 414,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1810082934,
			"version": 2,
			"versionNonce": 1459978520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "several numbers → average：資料集合＋空集合怎麼辦",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "n7D6pyZF",
			"originalText": "several numbers → average：資料集合＋空集合怎麼辦",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "aESgGfRm",
			"type": "rectangle",
			"x": 761.5,
			"y": -555.95,
			"width": 376,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 99515919,
			"version": 2,
			"versionNonce": 652262504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gydKYmyn"
				},
				{
					"type": "arrow",
					"id": "dZK3LKWL"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "gydKYmyn",
			"type": "text",
			"x": 775.5,
			"y": -546.95,
			"width": 348,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1326796633,
			"version": 2,
			"versionNonce": 1105567256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "核心：AI 無法替你消除沒定義清楚的需求",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aESgGfRm",
			"originalText": "核心：AI 無法替你消除沒定義清楚的需求",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "eMvPfcSi",
			"type": "rectangle",
			"x": 331.5,
			"y": -116.4,
			"width": 311,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffd8a8",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 390692063,
			"version": 2,
			"versionNonce": 1868361576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fHZykYwu"
				},
				{
					"type": "arrow",
					"id": "6HX4RaA3"
				},
				{
					"type": "arrow",
					"id": "sgYSpkf7"
				},
				{
					"type": "arrow",
					"id": "w2c9BLCJ"
				},
				{
					"type": "arrow",
					"id": "5TCyeLp7"
				},
				{
					"type": "arrow",
					"id": "zVXSKcZT"
				},
				{
					"type": "arrow",
					"id": "7AyUhcwB"
				},
				{
					"type": "arrow",
					"id": "vLpYktAG"
				},
				{
					"type": "arrow",
					"id": "rjJmwxUB"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "fHZykYwu",
			"type": "text",
			"x": 351.5,
			"y": -104.4,
			"width": 271,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1297991151,
			"version": 2,
			"versionNonce": 1958353688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q2 電腦實際上在做什麼",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eMvPfcSi",
			"originalText": "Q2 電腦實際上在做什麼",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "GV6K5uNB",
			"type": "rectangle",
			"x": 718.5,
			"y": -471.45,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 825748794,
			"version": 2,
			"versionNonce": 1608172136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XnSbmGi5"
				},
				{
					"type": "arrow",
					"id": "sgYSpkf7"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "XnSbmGi5",
			"type": "text",
			"x": 732.5,
			"y": -462.45,
			"width": 433,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1078522233,
			"version": 2,
			"versionNonce": 838268952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Hardware（實體裝置）vs Software（告訴硬體做什\n麼的程式）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GV6K5uNB",
			"originalText": "Hardware（實體裝置）vs Software（告訴硬體做什\n麼的程式）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "7g2ZwM3Q",
			"type": "rectangle",
			"x": 718.5,
			"y": -394.45,
			"width": 436,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1387722357,
			"version": 2,
			"versionNonce": 1193686376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JbreVTMe"
				},
				{
					"type": "arrow",
					"id": "w2c9BLCJ"
				},
				{
					"type": "arrow",
					"id": "cfEh5nQy"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "JbreVTMe",
			"type": "text",
			"x": 732.5,
			"y": -385.45,
			"width": 408,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 727137746,
			"version": 2,
			"versionNonce": 1301296408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "四功能：Input／Storage／Computing／Output",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7g2ZwM3Q",
			"originalText": "四功能：Input／Storage／Computing／Output",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "4fp6PERP",
			"type": "rectangle",
			"x": 1214.5,
			"y": -391.2,
			"width": 399,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1260289298,
			"version": 2,
			"versionNonce": 982206568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bHR6w8SC"
				},
				{
					"type": "arrow",
					"id": "cfEh5nQy"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "bHR6w8SC",
			"type": "text",
			"x": 1226.5,
			"y": -384.2,
			"width": 375,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1942205391,
			"version": 2,
			"versionNonce": 2096747032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例：name = input(\"Name: \")、print(\"Hello\", name)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4fp6PERP",
			"originalText": "例：name = input(\"Name: \")、print(\"Hello\", name)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "pMJT3nnN",
			"type": "rectangle",
			"x": 718.5,
			"y": -284.2,
			"width": 109,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 955337783,
			"version": 2,
			"versionNonce": 1171651432,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gMtGVkKt"
				},
				{
					"type": "arrow",
					"id": "5TCyeLp7"
				},
				{
					"type": "arrow",
					"id": "9wfcZWTr"
				},
				{
					"type": "arrow",
					"id": "DfBmfJ6h"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "gMtGVkKt",
			"type": "text",
			"x": 732.5,
			"y": -275.2,
			"width": 81,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 349677569,
			"version": 2,
			"versionNonce": 656920344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "按下 Run",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pMJT3nnN",
			"originalText": "按下 Run",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "B5L3PuUi",
			"type": "rectangle",
			"x": 887.5,
			"y": -339.95,
			"width": 384,
			"height": 74,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 757604088,
			"version": 2,
			"versionNonce": 458378856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "u7UdmsEL"
				},
				{
					"type": "arrow",
					"id": "9wfcZWTr"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "u7UdmsEL",
			"type": "text",
			"x": 899.5,
			"y": -332.95,
			"width": 360,
			"height": 60,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 10133401,
			"version": 2,
			"versionNonce": 881732632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "file on storage → process in RAM → Python\nruntime → CPU 執行 machine instructions →\noutput",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "B5L3PuUi",
			"originalText": "file on storage → process in RAM → Python\nruntime → CPU 執行 machine instructions →\noutput",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "WBep3NGY",
			"type": "rectangle",
			"x": 887.5,
			"y": -251.95,
			"width": 404,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1000699244,
			"version": 2,
			"versionNonce": 1137459560,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ghiYbYTV"
				},
				{
					"type": "arrow",
					"id": "DfBmfJ6h"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "ghiYbYTV",
			"type": "text",
			"x": 899.5,
			"y": -244.95,
			"width": 380,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1362353061,
			"version": 2,
			"versionNonce": 1595992344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "概念模型；真實還有 cache、virtual memory、I/O\ncontroller、DMA",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WBep3NGY",
			"originalText": "概念模型；真實還有 cache、virtual memory、I/O\ncontroller、DMA",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "7U3EBELq",
			"type": "rectangle",
			"x": 718.5,
			"y": -105.8,
			"width": 217,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"CGCMHuqA"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1348415436,
			"version": 2,
			"versionNonce": 1318048872,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "X2GCYc3P"
				},
				{
					"type": "arrow",
					"id": "zVXSKcZT"
				},
				{
					"type": "arrow",
					"id": "MUavRDp9"
				},
				{
					"type": "arrow",
					"id": "4VsDxaS2"
				},
				{
					"type": "arrow",
					"id": "9kM6Ckrk"
				},
				{
					"type": "arrow",
					"id": "9NRVymvt"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "X2GCYc3P",
			"type": "text",
			"x": 732.5,
			"y": -96.8,
			"width": 189,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"CGCMHuqA"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2050671409,
			"version": 2,
			"versionNonce": 39061016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Storage／RAM／CPU",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7U3EBELq",
			"originalText": "Storage／RAM／CPU",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "qKsaEMUm",
			"type": "rectangle",
			"x": 995.5,
			"y": -183.95,
			"width": 283,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1730736503,
			"version": 2,
			"versionNonce": 23660392,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GKxgmAyY"
				},
				{
					"type": "arrow",
					"id": "MUavRDp9"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "GKxgmAyY",
			"type": "text",
			"x": 1007.5,
			"y": -176.95,
			"width": 259,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1186638391,
			"version": 2,
			"versionNonce": 1796965144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Storage＝倉庫：長期保存 main.py",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qKsaEMUm",
			"originalText": "Storage＝倉庫：長期保存 main.py",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "deeigukr",
			"type": "rectangle",
			"x": 995.5,
			"y": -135.95,
			"width": 293,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 63357920,
			"version": 2,
			"versionNonce": 144956008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Nv5Dif6s"
				},
				{
					"type": "arrow",
					"id": "4VsDxaS2"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "Nv5Dif6s",
			"type": "text",
			"x": 1007.5,
			"y": -128.95,
			"width": 269,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 751316399,
			"version": 2,
			"versionNonce": 669736984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "RAM＝工作桌：執行中的狀態與變數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "deeigukr",
			"originalText": "RAM＝工作桌：執行中的狀態與變數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "ZQHdRmEV",
			"type": "rectangle",
			"x": 995.5,
			"y": -87.95,
			"width": 416,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1748449577,
			"version": 2,
			"versionNonce": 655117672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EjFFQFZP"
				},
				{
					"type": "arrow",
					"id": "9kM6Ckrk"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "EjFFQFZP",
			"type": "text",
			"x": 1007.5,
			"y": -80.95,
			"width": 392,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 305148988,
			"version": 2,
			"versionNonce": 1488428312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "CPU＝工作的人：load、store、arithmetic、branch",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZQHdRmEV",
			"originalText": "CPU＝工作的人：load、store、arithmetic、branch",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "9nhrtuCh",
			"type": "rectangle",
			"x": 995.5,
			"y": -21.15,
			"width": 389,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"Q4MeYS7H"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 208344251,
			"version": 2,
			"versionNonce": 1710121064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "j6w6WtpC"
				},
				{
					"type": "arrow",
					"id": "9NRVymvt"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "j6w6WtpC",
			"type": "text",
			"x": 1007.5,
			"y": -14.15,
			"width": 365,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Q4MeYS7H"
			],
			"frameId": null,
			"roundness": null,
			"seed": 238412047,
			"version": 2,
			"versionNonce": 2129934872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Key idea：執行狀態是暫時的，要保存就明確存檔",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9nhrtuCh",
			"originalText": "Key idea：執行狀態是暫時的，要保存就明確存檔",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "WGETEJAC",
			"type": "rectangle",
			"x": 718.5,
			"y": 67.6,
			"width": 243,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1782964439,
			"version": 2,
			"versionNonce": 1159074664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Dgb5kBuJ"
				},
				{
					"type": "arrow",
					"id": "7AyUhcwB"
				},
				{
					"type": "arrow",
					"id": "kCune5dT"
				},
				{
					"type": "arrow",
					"id": "bSGecR5N"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "Dgb5kBuJ",
			"type": "text",
			"x": 732.5,
			"y": 76.6,
			"width": 215,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 141432866,
			"version": 2,
			"versionNonce": 1301624600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "為什麼 CPU 直接用 RAM",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WGETEJAC",
			"originalText": "為什麼 CPU 直接用 RAM",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "M9V8XmX3",
			"type": "rectangle",
			"x": 1021.5,
			"y": 26.85,
			"width": 396,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1183298070,
			"version": 2,
			"versionNonce": 1791977064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mGSxG8ZU"
				},
				{
					"type": "arrow",
					"id": "kCune5dT"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "mGSxG8ZU",
			"type": "text",
			"x": 1033.5,
			"y": 33.85,
			"width": 372,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 642645707,
			"version": 2,
			"versionNonce": 2030998552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "LOAD register, [address]、STORE [address],\nregister",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M9V8XmX3",
			"originalText": "LOAD register, [address]、STORE [address],\nregister",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "tXSfhm38",
			"type": "rectangle",
			"x": 1021.5,
			"y": 94.85,
			"width": 425,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 425439094,
			"version": 2,
			"versionNonce": 1407605096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zpzwE4Yh"
				},
				{
					"type": "arrow",
					"id": "bSGecR5N"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "zpzwE4Yh",
			"type": "text",
			"x": 1033.5,
			"y": 101.85,
			"width": 401,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1831557396,
			"version": 2,
			"versionNonce": 122966296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "SSD／HDD 是 block I/O：OS／driver → controller\n→ 搬進 RAM",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tXSfhm38",
			"originalText": "SSD／HDD 是 block I/O：OS／driver → controller\n→ 搬進 RAM",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "7kWSbijP",
			"type": "rectangle",
			"x": 718.5,
			"y": 175.15,
			"width": 289,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1916391548,
			"version": 2,
			"versionNonce": 61271144,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EvSpEcL7"
				},
				{
					"type": "arrow",
					"id": "vLpYktAG"
				},
				{
					"type": "arrow",
					"id": "VpP46cdH"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "EvSpEcL7",
			"type": "text",
			"x": 732.5,
			"y": 184.15,
			"width": 261,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2105241057,
			"version": 2,
			"versionNonce": 534408728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Fetch → Decode → Execute",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7kWSbijP",
			"originalText": "Fetch → Decode → Execute",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "eyRfmTRt",
			"type": "rectangle",
			"x": 1067.5,
			"y": 181.65,
			"width": 336,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"Gfs8BXKR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1788255364,
			"version": 2,
			"versionNonce": 870129512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2iSKx64h"
				},
				{
					"type": "arrow",
					"id": "VpP46cdH"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "2iSKx64h",
			"type": "text",
			"x": 1079.5,
			"y": 188.65,
			"width": 312,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Gfs8BXKR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1730197424,
			"version": 2,
			"versionNonce": 1536486168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 一行 Python ≠ 一個 CPU instruction",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eyRfmTRt",
			"originalText": "⚠ 一行 Python ≠ 一個 CPU instruction",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "rp2vVJtD",
			"type": "rectangle",
			"x": 718.5,
			"y": 229.65,
			"width": 422,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff3bf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 157535144,
			"version": 2,
			"versionNonce": 81064552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vbJP6QAr"
				},
				{
					"type": "arrow",
					"id": "rjJmwxUB"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "vbJP6QAr",
			"type": "text",
			"x": 732.5,
			"y": 238.65,
			"width": 394,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1332727155,
			"version": 2,
			"versionNonce": 351782936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ 硬體是非題（cache、RISC／CISC、時脈、\nDRAM）→ 見心智圖 6",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rp2vVJtD",
			"originalText": "★ 硬體是非題（cache、RISC／CISC、時脈、\nDRAM）→ 見心智圖 6",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "ypZCrq87",
			"type": "rectangle",
			"x": 331.5,
			"y": 558.02,
			"width": 284,
			"height": 54,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#d0bfff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1402114298,
			"version": 2,
			"versionNonce": 760898920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZUTdyYQH"
				},
				{
					"type": "arrow",
					"id": "DyxfnSwA"
				},
				{
					"type": "arrow",
					"id": "yQDyydAL"
				},
				{
					"type": "arrow",
					"id": "uZSMyaqb"
				},
				{
					"type": "arrow",
					"id": "H7CV7JF6"
				},
				{
					"type": "arrow",
					"id": "qyp726g8"
				},
				{
					"type": "arrow",
					"id": "WeLBZ9yB"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "ZUTdyYQH",
			"type": "text",
			"x": 351.5,
			"y": 570.02,
			"width": 244,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 705177996,
			"version": 2,
			"versionNonce": 938935576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q3 電腦如何表示資訊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ypZCrq87",
			"originalText": "Q3 電腦如何表示資訊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "wajLgwUy",
			"type": "rectangle",
			"x": 691.5,
			"y": 336.65,
			"width": 327,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1136179927,
			"version": 2,
			"versionNonce": 716798056,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TTbZ5GMZ"
				},
				{
					"type": "arrow",
					"id": "yQDyydAL"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "TTbZ5GMZ",
			"type": "text",
			"x": 705.5,
			"y": 345.65,
			"width": 299,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1274341223,
			"version": 2,
			"versionNonce": 302424600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "data = value + type + operations",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wajLgwUy",
			"originalText": "data = value + type + operations",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "YszYzcAn",
			"type": "rectangle",
			"x": 691.5,
			"y": 391.15,
			"width": 336,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 312888267,
			"version": 2,
			"versionNonce": 1891511144,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9qEi6F7Q"
				},
				{
					"type": "arrow",
					"id": "uZSMyaqb"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "9qEi6F7Q",
			"type": "text",
			"x": 705.5,
			"y": 400.15,
			"width": 308,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 900136707,
			"version": 2,
			"versionNonce": 572170008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "65／65.0／\"65\" → int／float／str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YszYzcAn",
			"originalText": "65／65.0／\"65\" → int／float／str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "YqZGSDX6",
			"type": "rectangle",
			"x": 691.5,
			"y": 466.4,
			"width": 221,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 393533562,
			"version": 2,
			"versionNonce": 431259240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "i3RwnWsJ"
				},
				{
					"type": "arrow",
					"id": "H7CV7JF6"
				},
				{
					"type": "arrow",
					"id": "KLJ3hqHz"
				},
				{
					"type": "arrow",
					"id": "7BirrV88"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "i3RwnWsJ",
			"type": "text",
			"x": 705.5,
			"y": 475.4,
			"width": 193,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1827301052,
			"version": 2,
			"versionNonce": 1755773976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "同一組 bits，不同解讀",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YqZGSDX6",
			"originalText": "同一組 bits，不同解讀",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "udUKCg2V",
			"type": "rectangle",
			"x": 972.5,
			"y": 445.65,
			"width": 333,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1896034026,
			"version": 2,
			"versionNonce": 375943528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "syFJyPNV"
				},
				{
					"type": "arrow",
					"id": "KLJ3hqHz"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "syFJyPNV",
			"type": "text",
			"x": 984.5,
			"y": 452.65,
			"width": 309,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 477647260,
			"version": 2,
			"versionNonce": 933214488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "01000001 → unsigned 65 → ASCII 'A'",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "udUKCg2V",
			"originalText": "01000001 → unsigned 65 → ASCII 'A'",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "MyrpaamM",
			"type": "rectangle",
			"x": 972.5,
			"y": 493.65,
			"width": 249,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 513701982,
			"version": 2,
			"versionNonce": 1579549800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "h86gKbEC"
				},
				{
					"type": "arrow",
					"id": "7BirrV88"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "h86gKbEC",
			"type": "text",
			"x": 984.5,
			"y": 500.65,
			"width": 225,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 965509037,
			"version": 2,
			"versionNonce": 41473560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "chr(65) → A；ord('A') → 65",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MyrpaamM",
			"originalText": "chr(65) → A；ord('A') → 65",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "eLVSwH22",
			"type": "rectangle",
			"x": 691.5,
			"y": 634.4,
			"width": 196,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1803834049,
			"version": 2,
			"versionNonce": 515454824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tYhc6Jtu"
				},
				{
					"type": "arrow",
					"id": "qyp726g8"
				},
				{
					"type": "arrow",
					"id": "nWZFjcwu"
				},
				{
					"type": "arrow",
					"id": "sM3tC8dB"
				},
				{
					"type": "arrow",
					"id": "a54dMaCt"
				},
				{
					"type": "arrow",
					"id": "KhhvuM9B"
				},
				{
					"type": "arrow",
					"id": "nyLskJMw"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "tYhc6Jtu",
			"type": "text",
			"x": 705.5,
			"y": 643.4,
			"width": 168,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1429138154,
			"version": 2,
			"versionNonce": 774263576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "type 決定 + 的意思",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eLVSwH22",
			"originalText": "type 決定 + 的意思",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "gtKh5ai8",
			"type": "rectangle",
			"x": 947.5,
			"y": 541.65,
			"width": 127,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2002726580,
			"version": 2,
			"versionNonce": 1819150952,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pzvcFXnz"
				},
				{
					"type": "arrow",
					"id": "nWZFjcwu"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "pzvcFXnz",
			"type": "text",
			"x": 959.5,
			"y": 548.65,
			"width": 103,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1064228543,
			"version": 2,
			"versionNonce": 1629237272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "65 + 1 → 66",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gtKh5ai8",
			"originalText": "65 + 1 → 66",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "k3bB7tDB",
			"type": "rectangle",
			"x": 947.5,
			"y": 589.65,
			"width": 158,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1890885919,
			"version": 2,
			"versionNonce": 1913683304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qh668EW7"
				},
				{
					"type": "arrow",
					"id": "sM3tC8dB"
				}
			],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "qh668EW7",
			"type": "text",
			"x": 959.5,
			"y": 596.65,
			"width": 134,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1576094584,
			"version": 2,
			"versionNonce": 1397648664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132594,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "65.0 + 1 → 66.0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "k3bB7tDB",
			"originalText": "65.0 + 1 → 66.0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "W2wFMzxz",
			"type": "rectangle",
			"x": 947.5,
			"y": 637.65,
			"width": 169,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1157345914,
			"version": 2,
			"versionNonce": 552374376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fqdwUMiW"
				},
				{
					"type": "arrow",
					"id": "a54dMaCt"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "fqdwUMiW",
			"type": "text",
			"x": 959.5,
			"y": 644.65,
			"width": 145,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 825676709,
			"version": 2,
			"versionNonce": 506530328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"65\" + \"1\" → \"651\"",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "W2wFMzxz",
			"originalText": "\"65\" + \"1\" → \"651\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "AHN7Xrw5",
			"type": "rectangle",
			"x": 947.5,
			"y": 685.65,
			"width": 223,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1109004750,
			"version": 2,
			"versionNonce": 1624130408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8HNXpJcd"
				},
				{
					"type": "arrow",
					"id": "KhhvuM9B"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "8HNXpJcd",
			"type": "text",
			"x": 959.5,
			"y": 692.65,
			"width": 199,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1111776027,
			"version": 2,
			"versionNonce": 213387032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ \"65\" + 1 → TypeError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AHN7Xrw5",
			"originalText": "⚠ \"65\" + 1 → TypeError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "6Vcg4hfE",
			"type": "rectangle",
			"x": 947.5,
			"y": 733.65,
			"width": 382,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1993526095,
			"version": 2,
			"versionNonce": 1073845864,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3qrVRS5i"
				},
				{
					"type": "arrow",
					"id": "nyLskJMw"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "3qrVRS5i",
			"type": "text",
			"x": 959.5,
			"y": 740.65,
			"width": 358,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1277109763,
			"version": 2,
			"versionNonce": 1800889368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "修：int(\"65\") + 1 → 66；\"65\" + str(1) → 651",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6Vcg4hfE",
			"originalText": "修：int(\"65\") + 1 → 66；\"65\" + str(1) → 651",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "BmzN3NYE",
			"type": "rectangle",
			"x": 691.5,
			"y": 781.65,
			"width": 453,
			"height": 63,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#fff3bf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 772116197,
			"version": 2,
			"versionNonce": 592611688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Ppk7kwVG"
				},
				{
					"type": "arrow",
					"id": "WeLBZ9yB"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "Ppk7kwVG",
			"type": "text",
			"x": 705.5,
			"y": 790.65,
			"width": 425,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2096323628,
			"version": 2,
			"versionNonce": 1476600088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ 所有資料都是 0／1（T）；只看 byte 不知道意\n義（F）；圖片音樂也是 0／1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BmzN3NYE",
			"originalText": "★ 所有資料都是 0／1（T）；只看 byte 不知道意\n義（F）；圖片音樂也是 0／1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "bi7mVPx7",
			"type": "rectangle",
			"x": 331.5,
			"y": 1011.55,
			"width": 266,
			"height": 54,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#99e9f2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1509759611,
			"version": 2,
			"versionNonce": 1980570728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hgLNBcGb"
				},
				{
					"type": "arrow",
					"id": "H3RdLPXR"
				},
				{
					"type": "arrow",
					"id": "trEmvfbN"
				},
				{
					"type": "arrow",
					"id": "vTnZngFQ"
				},
				{
					"type": "arrow",
					"id": "HAt6Hzef"
				},
				{
					"type": "arrow",
					"id": "t6PBMwKY"
				},
				{
					"type": "arrow",
					"id": "RaKdW22a"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "hgLNBcGb",
			"type": "text",
			"x": 351.5,
			"y": 1023.55,
			"width": 226,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 128848189,
			"version": 2,
			"versionNonce": 305085976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q4 什麼是 Program",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bi7mVPx7",
			"originalText": "Q4 什麼是 Program",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "G2cfXRXX",
			"type": "rectangle",
			"x": 673.5,
			"y": 888.65,
			"width": 355,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 981156568,
			"version": 2,
			"versionNonce": 1509773160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eqUNtPfE"
				},
				{
					"type": "arrow",
					"id": "trEmvfbN"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "eqUNtPfE",
			"type": "text",
			"x": 687.5,
			"y": 897.65,
			"width": 327,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 131357831,
			"version": 2,
			"versionNonce": 1255127832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Algorithm：清楚、有限、可執行的步驟",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G2cfXRXX",
			"originalText": "Algorithm：清楚、有限、可執行的步驟",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "Vz5FHX7C",
			"type": "rectangle",
			"x": 673.5,
			"y": 943.15,
			"width": 433,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 993795049,
			"version": 2,
			"versionNonce": 1466901096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6X77gK7V"
				},
				{
					"type": "arrow",
					"id": "vTnZngFQ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "6X77gK7V",
			"type": "text",
			"x": 687.5,
			"y": 952.15,
			"width": 405,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 253433495,
			"version": 2,
			"versionNonce": 1951963160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Source code：algorithm 用程式語言的精確表達",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Vz5FHX7C",
			"originalText": "Source code：algorithm 用程式語言的精確表達",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "WwsiVBPz",
			"type": "rectangle",
			"x": 673.5,
			"y": 1016.45,
			"width": 424,
			"height": 63,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"de7ntvWW"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 779344393,
			"version": 2,
			"versionNonce": 221156712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "C8LQzCK5"
				},
				{
					"type": "arrow",
					"id": "HAt6Hzef"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "C8LQzCK5",
			"type": "text",
			"x": 687.5,
			"y": 1025.45,
			"width": 396,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"de7ntvWW"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1015442299,
			"version": 2,
			"versionNonce": 314430744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Pseudocode first：Read C → Compute F →\nDisplay F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WwsiVBPz",
			"originalText": "Pseudocode first：Read C → Compute F →\nDisplay F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "3pMeEhUA",
			"type": "rectangle",
			"x": 673.5,
			"y": 1093.45,
			"width": 354,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2067563966,
			"version": 2,
			"versionNonce": 1619503208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RAUb8eK4"
				},
				{
					"type": "arrow",
					"id": "t6PBMwKY"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "RAUb8eK4",
			"type": "text",
			"x": 687.5,
			"y": 1102.45,
			"width": 326,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 985305416,
			"version": 2,
			"versionNonce": 192115224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "精確性：BMI 要先定單位、公式、輸出",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3pMeEhUA",
			"originalText": "精確性：BMI 要先定單位、公式、輸出",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "YN4MzDdV",
			"type": "rectangle",
			"x": 673.5,
			"y": 1147.95,
			"width": 453,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1519344303,
			"version": 2,
			"versionNonce": 759585640,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MKuxURh5"
				},
				{
					"type": "arrow",
					"id": "RaKdW22a"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2W"
		},
		{
			"id": "MKuxURh5",
			"type": "text",
			"x": 687.5,
			"y": 1156.95,
			"width": 425,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1776420484,
			"version": 2,
			"versionNonce": 1970106136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "好程式＝需求、algorithm、code、tests 彼此一致",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YN4MzDdV",
			"originalText": "好程式＝需求、algorithm、code、tests 彼此一致",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "eV5WWD9i",
			"type": "rectangle",
			"x": -612.5,
			"y": -968.3,
			"width": 281,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fcc2d7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1605043300,
			"version": 2,
			"versionNonce": 1974906472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ajnLi6PH"
				},
				{
					"type": "arrow",
					"id": "w7HusntV"
				},
				{
					"type": "arrow",
					"id": "e6uUafqW"
				},
				{
					"type": "arrow",
					"id": "YNdR7TwS"
				},
				{
					"type": "arrow",
					"id": "GhMCeLpN"
				},
				{
					"type": "arrow",
					"id": "wjPk3zcX"
				},
				{
					"type": "arrow",
					"id": "MmPDykwY"
				},
				{
					"type": "arrow",
					"id": "ipndTquz"
				},
				{
					"type": "arrow",
					"id": "vcphvwxF"
				},
				{
					"type": "arrow",
					"id": "RfzVFMvd"
				},
				{
					"type": "arrow",
					"id": "fMH7bhxk"
				},
				{
					"type": "arrow",
					"id": "ufbLg7yX"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "ajnLi6PH",
			"type": "text",
			"x": -592.5,
			"y": -956.3,
			"width": 241,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1283155549,
			"version": 2,
			"versionNonce": 1763691544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q5 Python 如何執行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eV5WWD9i",
			"originalText": "Q5 Python 如何執行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "KZxM2vHn",
			"type": "rectangle",
			"x": -793.5,
			"y": -1430.05,
			"width": 105,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 306649441,
			"version": 2,
			"versionNonce": 312779112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qBpRqFiB"
				},
				{
					"type": "arrow",
					"id": "e6uUafqW"
				},
				{
					"type": "arrow",
					"id": "YtscKUgS"
				},
				{
					"type": "arrow",
					"id": "2V2y3iLB"
				},
				{
					"type": "arrow",
					"id": "85nvnt5P"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "qBpRqFiB",
			"type": "text",
			"x": -779.5,
			"y": -1421.05,
			"width": 77,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 354481647,
			"version": 2,
			"versionNonce": 1350469912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "三個層次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KZxM2vHn",
			"originalText": "三個層次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
		},
		{
			"id": "sZ7KeEp2",
			"type": "rectangle",
			"x": -1171.5,
			"y": -1489.8,
			"width": 318,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1659648472,
			"version": 2,
			"versionNonce": 1666987112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fUJhsvz5"
				},
				{
					"type": "arrow",
					"id": "YtscKUgS"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2c"
		},
		{
			"id": "fUJhsvz5",
			"type": "text",
			"x": -1159.5,
			"y": -1482.8,
			"width": 294,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1178120827,
			"version": 2,
			"versionNonce": 922592792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "High-level：x = x + 1（描述要做什麼）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sZ7KeEp2",
			"originalText": "High-level：x = x + 1（描述要做什麼）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2d"
		},
		{
			"id": "ppgXTqP3",
			"type": "rectangle",
			"x": -1281.5,
			"y": -1441.8,
			"width": 428,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 546503922,
			"version": 2,
			"versionNonce": 2108254056,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hxnspvpu"
				},
				{
					"type": "arrow",
					"id": "2V2y3iLB"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2e"
		},
		{
			"id": "hxnspvpu",
			"type": "text",
			"x": -1269.5,
			"y": -1434.8,
			"width": 404,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 935652429,
			"version": 2,
			"versionNonce": 428942104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Assembly：MOV EAX, 65、ADD EAX, 1（一步一步怎\n麼做）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ppgXTqP3",
			"originalText": "Assembly：MOV EAX, 65、ADD EAX, 1（一步一步怎\n麼做）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2f"
		},
		{
			"id": "9aV8sumK",
			"type": "rectangle",
			"x": -1290.5,
			"y": -1373.8,
			"width": 437,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 401168297,
			"version": 2,
			"versionNonce": 1574451816,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LJNExhuf"
				},
				{
					"type": "arrow",
					"id": "85nvnt5P"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2g"
		},
		{
			"id": "LJNExhuf",
			"type": "text",
			"x": -1278.5,
			"y": -1366.8,
			"width": 413,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2078417559,
			"version": 2,
			"versionNonce": 917307416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Machine language：CPU 解碼的 bit patterns；x86、\nARM、RISC-V 各不同",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9aV8sumK",
			"originalText": "Machine language：CPU 解碼的 bit patterns；x86、\nARM、RISC-V 各不同",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2h"
		},
		{
			"id": "5QmZZ2zd",
			"type": "rectangle",
			"x": -1144.5,
			"y": -1305.8,
			"width": 456,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 372149840,
			"version": 2,
			"versionNonce": 380939624,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rVQrMPvq"
				},
				{
					"type": "arrow",
					"id": "YNdR7TwS"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2i"
		},
		{
			"id": "rVQrMPvq",
			"type": "text",
			"x": -1130.5,
			"y": -1296.8,
			"width": 428,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1575132757,
			"version": 2,
			"versionNonce": 1581595928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Compiler：source → compiler → machine code →\nrun（C／C++；翻一次跑多次）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5QmZZ2zd",
			"originalText": "Compiler：source → compiler → machine code →\nrun（C／C++；翻一次跑多次）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2j"
		},
		{
			"id": "J4vSLtdb",
			"type": "rectangle",
			"x": -1114.5,
			"y": -1228.8,
			"width": 426,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 362073757,
			"version": 2,
			"versionNonce": 25870440,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "jZtA4sJt"
				},
				{
					"type": "arrow",
					"id": "GhMCeLpN"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2k"
		},
		{
			"id": "jZtA4sJt",
			"type": "text",
			"x": -1100.5,
			"y": -1219.8,
			"width": 398,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 214048106,
			"version": 2,
			"versionNonce": 1104009752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Compilation vs Interpretation：不是互斥標籤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "J4vSLtdb",
			"originalText": "Compilation vs Interpretation：不是互斥標籤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2l"
		},
		{
			"id": "L39dXeYq",
			"type": "rectangle",
			"x": -1148.5,
			"y": -1155.5,
			"width": 460,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"UT3pU2Sz"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2021011813,
			"version": 2,
			"versionNonce": 1848013672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iz3nVnkW"
				},
				{
					"type": "arrow",
					"id": "wjPk3zcX"
				},
				{
					"type": "arrow",
					"id": "6pVGWq3n"
				},
				{
					"type": "arrow",
					"id": "fGYE77su"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2m"
		},
		{
			"id": "iz3nVnkW",
			"type": "text",
			"x": -1134.5,
			"y": -1146.5,
			"width": 432,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"UT3pU2Sz"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1672842446,
			"version": 2,
			"versionNonce": 1144706840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "CPython：source → parse／compile → bytecode\n→ runtime 執行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "L39dXeYq",
			"originalText": "CPython：source → parse／compile → bytecode\n→ runtime 執行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2n"
		},
		{
			"id": "NUcUckYW",
			"type": "rectangle",
			"x": -1497.5,
			"y": -1174.3,
			"width": 289,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1794573301,
			"version": 2,
			"versionNonce": 1389610600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4dZ8NY6H"
				},
				{
					"type": "arrow",
					"id": "6pVGWq3n"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2o"
		},
		{
			"id": "4dZ8NY6H",
			"type": "text",
			"x": -1485.5,
			"y": -1167.3,
			"width": 265,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2098920511,
			"version": 2,
			"versionNonce": 1241527320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ bytecode ≠ CPU machine code",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NUcUckYW",
			"originalText": "⚠ bytecode ≠ CPU machine code",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2p"
		},
		{
			"id": "VuhYmUYz",
			"type": "rectangle",
			"x": -1640.5,
			"y": -1126.3,
			"width": 432,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1295480976,
			"version": 2,
			"versionNonce": 2086582632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "w6wvqH4J"
				},
				{
					"type": "arrow",
					"id": "fGYE77su"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2q"
		},
		{
			"id": "w6wvqH4J",
			"type": "text",
			"x": -1628.5,
			"y": -1119.3,
			"width": 408,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1898754735,
			"version": 2,
			"versionNonce": 152170776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★⚠ 是非題「interpreter 翻成 machine language」：\n2021 答 T，新講義判 F → 問老師",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VuhYmUYz",
			"originalText": "★⚠ 是非題「interpreter 翻成 machine language」：\n2021 答 T，新講義判 F → 問老師",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2r"
		},
		{
			"id": "gzdUDis2",
			"type": "rectangle",
			"x": -1119.5,
			"y": -1058.3,
			"width": 431,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 450212839,
			"version": 2,
			"versionNonce": 1041452136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Phhb4nkN"
				},
				{
					"type": "arrow",
					"id": "MmPDykwY"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2s"
		},
		{
			"id": "Phhb4nkN",
			"type": "text",
			"x": -1105.5,
			"y": -1049.3,
			"width": 403,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1631356158,
			"version": 2,
			"versionNonce": 1491340824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Syntax error：整個 script 不會開始；Runtime\nerror：跑到一半失敗",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gzdUDis2",
			"originalText": "Syntax error：整個 script 不會開始；Runtime\nerror：跑到一半失敗",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2t"
		},
		{
			"id": "M4gYkEET",
			"type": "rectangle",
			"x": -960.5,
			"y": -936.55,
			"width": 272,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 664760681,
			"version": 2,
			"versionNonce": 566067048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EyiBbVYM"
				},
				{
					"type": "arrow",
					"id": "ipndTquz"
				},
				{
					"type": "arrow",
					"id": "SKbiAQaZ"
				},
				{
					"type": "arrow",
					"id": "6V8geGgR"
				},
				{
					"type": "arrow",
					"id": "VUrMv32N"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2u"
		},
		{
			"id": "EyiBbVYM",
			"type": "text",
			"x": -946.5,
			"y": -927.55,
			"width": 244,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1777771294,
			"version": 2,
			"versionNonce": 40536856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Interactive vs Script mode",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M4gYkEET",
			"originalText": "Interactive vs Script mode",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2v"
		},
		{
			"id": "LYN7qgth",
			"type": "rectangle",
			"x": -1179.5,
			"y": -981.3,
			"width": 159,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 180417414,
			"version": 2,
			"versionNonce": 396972648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Hdq5buP6"
				},
				{
					"type": "arrow",
					"id": "SKbiAQaZ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2w"
		},
		{
			"id": "Hdq5buP6",
			"type": "text",
			"x": -1167.5,
			"y": -974.3,
			"width": 135,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1791876039,
			"version": 2,
			"versionNonce": 270100504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": ">>> 3 + 5 顯示 8",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LYN7qgth",
			"originalText": ">>> 3 + 5 顯示 8",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2x"
		},
		{
			"id": "eMkdaZGE",
			"type": "rectangle",
			"x": -1401.5,
			"y": -933.3,
			"width": 381,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1200745334,
			"version": 2,
			"versionNonce": 648201576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eu8tijQn"
				},
				{
					"type": "arrow",
					"id": "6V8geGgR"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b2y"
		},
		{
			"id": "eu8tijQn",
			"type": "text",
			"x": -1389.5,
			"y": -926.3,
			"width": 357,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 645140528,
			"version": 2,
			"versionNonce": 501523736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "script 裡只寫 3 + 5 不顯示 → 要 print(3 + 5)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eMkdaZGE",
			"originalText": "script 裡只寫 3 + 5 不顯示 → 要 print(3 + 5)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2z"
		},
		{
			"id": "TjWaFXNy",
			"type": "rectangle",
			"x": -1408.5,
			"y": -885.3,
			"width": 388,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 362677221,
			"version": 2,
			"versionNonce": 469096552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qeWg7bSF"
				},
				{
					"type": "arrow",
					"id": "VUrMv32N"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b30"
		},
		{
			"id": "qeWg7bSF",
			"type": "text",
			"x": -1396.5,
			"y": -878.3,
			"width": 364,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1921556147,
			"version": 2,
			"versionNonce": 692077080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ >>> 打 Python；terminal 打 python main.py",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TjWaFXNy",
			"originalText": "⚠ >>> 打 Python；terminal 打 python main.py",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b31"
		},
		{
			"id": "PcPCmgS5",
			"type": "rectangle",
			"x": -1121.5,
			"y": -837.3,
			"width": 433,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1901201535,
			"version": 2,
			"versionNonce": 997100392,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MixTYRSU"
				},
				{
					"type": "arrow",
					"id": "vcphvwxF"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b32"
		},
		{
			"id": "MixTYRSU",
			"type": "text",
			"x": -1107.5,
			"y": -828.3,
			"width": 405,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 671831790,
			"version": 2,
			"versionNonce": 1629503256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "開發迴圈：Edit → Save → Run → Inspect →\nRevise",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PcPCmgS5",
			"originalText": "開發迴圈：Edit → Save → Run → Inspect →\nRevise",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b33"
		},
		{
			"id": "T3fS7hUk",
			"type": "rectangle",
			"x": -1010.5,
			"y": -691.55,
			"width": 322,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 857706122,
			"version": 2,
			"versionNonce": 1868095080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kP8zmp3P"
				},
				{
					"type": "arrow",
					"id": "RfzVFMvd"
				},
				{
					"type": "arrow",
					"id": "WH9S4uA4"
				},
				{
					"type": "arrow",
					"id": "T7cgfWZB"
				},
				{
					"type": "arrow",
					"id": "cEZNxNKv"
				},
				{
					"type": "arrow",
					"id": "rfTjq2ka"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b34"
		},
		{
			"id": "kP8zmp3P",
			"type": "text",
			"x": -996.5,
			"y": -682.55,
			"width": 294,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 237975537,
			"version": 2,
			"versionNonce": 1979227160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Syntax／Expression／Statement",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "T3fS7hUk",
			"originalText": "Syntax／Expression／Statement",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b35"
		},
		{
			"id": "JDVabgEY",
			"type": "rectangle",
			"x": -1395.5,
			"y": -760.3,
			"width": 325,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 26714586,
			"version": 2,
			"versionNonce": 2021708136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "m2dCYBWy"
				},
				{
					"type": "arrow",
					"id": "WH9S4uA4"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b36"
		},
		{
			"id": "m2dCYBWy",
			"type": "text",
			"x": -1383.5,
			"y": -753.3,
			"width": 301,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 26015155,
			"version": 2,
			"versionNonce": 1774016792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Syntax：文法；少冒號 → SyntaxError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JDVabgEY",
			"originalText": "Syntax：文法；少冒號 → SyntaxError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b37"
		},
		{
			"id": "5vtfX88Y",
			"type": "rectangle",
			"x": -1472.5,
			"y": -712.3,
			"width": 402,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1369390980,
			"version": 2,
			"versionNonce": 506618984,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "La2eeukf"
				},
				{
					"type": "arrow",
					"id": "T7cgfWZB"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b38"
		},
		{
			"id": "La2eeukf",
			"type": "text",
			"x": -1460.5,
			"y": -705.3,
			"width": 378,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 601437656,
			"version": 2,
			"versionNonce": 1608676888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Expression 產生值：3 + 5 → 8；10 > 3 → True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5vtfX88Y",
			"originalText": "Expression 產生值：3 + 5 → 8；10 > 3 → True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b39"
		},
		{
			"id": "VHRkAvwa",
			"type": "rectangle",
			"x": -1472.5,
			"y": -664.3,
			"width": 402,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1983373051,
			"version": 2,
			"versionNonce": 1580832616,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kDj7swPd"
				},
				{
					"type": "arrow",
					"id": "cEZNxNKv"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3A"
		},
		{
			"id": "kDj7swPd",
			"type": "text",
			"x": -1460.5,
			"y": -657.3,
			"width": 378,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1868753197,
			"version": 2,
			"versionNonce": 1834742552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Statement 可執行：result = 3 + 5；整個 if 結構",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VHRkAvwa",
			"originalText": "Statement 可執行：result = 3 + 5；整個 if 結構",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3B"
		},
		{
			"id": "wXGedvi8",
			"type": "rectangle",
			"x": -1486.5,
			"y": -616.3,
			"width": 416,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 763185300,
			"version": 2,
			"versionNonce": 484600424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3ZGVWeUQ"
				},
				{
					"type": "arrow",
					"id": "rfTjq2ka"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3C"
		},
		{
			"id": "3ZGVWeUQ",
			"type": "text",
			"x": -1474.5,
			"y": -609.3,
			"width": 392,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1264241432,
			"version": 2,
			"versionNonce": 1755172888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "print(result)＝expression statement；# 開始註解",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wXGedvi8",
			"originalText": "print(result)＝expression statement；# 開始註解",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3D"
		},
		{
			"id": "MkVZ6LAm",
			"type": "rectangle",
			"x": -1065.5,
			"y": -568.3,
			"width": 377,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 23187349,
			"version": 2,
			"versionNonce": 1425595752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pAPvCfmS"
				},
				{
					"type": "arrow",
					"id": "fMH7bhxk"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3E"
		},
		{
			"id": "pAPvCfmS",
			"type": "text",
			"x": -1051.5,
			"y": -559.3,
			"width": 349,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1779230102,
			"version": 2,
			"versionNonce": 966528280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Variable：名字指向資料，不是數學未知數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MkVZ6LAm",
			"originalText": "Variable：名字指向資料，不是數學未知數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3F"
		},
		{
			"id": "8MkLvUmp",
			"type": "rectangle",
			"x": -922.5,
			"y": -493.05,
			"width": 234,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"eawEQrjH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 345674489,
			"version": 2,
			"versionNonce": 1204351080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HsSMF77X"
				},
				{
					"type": "arrow",
					"id": "ufbLg7yX"
				},
				{
					"type": "arrow",
					"id": "25nYTFwy"
				},
				{
					"type": "arrow",
					"id": "wKTSS3CF"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3G"
		},
		{
			"id": "HsSMF77X",
			"type": "text",
			"x": -908.5,
			"y": -484.05,
			"width": 206,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"eawEQrjH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2055836054,
			"version": 2,
			"versionNonce": 701147672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ input() 一律回傳 str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8MkLvUmp",
			"originalText": "⚠ input() 一律回傳 str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3H"
		},
		{
			"id": "ztSyAuDp",
			"type": "rectangle",
			"x": -1192.5,
			"y": -513.8,
			"width": 210,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1409847466,
			"version": 2,
			"versionNonce": 756982632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SkQDeszb"
				},
				{
					"type": "arrow",
					"id": "25nYTFwy"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3I"
		},
		{
			"id": "SkQDeszb",
			"type": "text",
			"x": -1180.5,
			"y": -506.8,
			"width": 186,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 533302078,
			"version": 2,
			"versionNonce": 874358552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "輸入 3、5：x + y → 35",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ztSyAuDp",
			"originalText": "輸入 3、5：x + y → 35",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3J"
		},
		{
			"id": "xveF7gex",
			"type": "rectangle",
			"x": -1248.5,
			"y": -465.8,
			"width": 266,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 318355273,
			"version": 2,
			"versionNonce": 1665529448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "h8BWik6A"
				},
				{
					"type": "arrow",
					"id": "wKTSS3CF"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3K"
		},
		{
			"id": "h8BWik6A",
			"type": "text",
			"x": -1236.5,
			"y": -458.8,
			"width": 242,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 22968619,
			"version": 2,
			"versionNonce": 1426654232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "修：float(input()) → 8.0〔C〕",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xveF7gex",
			"originalText": "修：float(input()) → 8.0〔C〕",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3L"
		},
		{
			"id": "Q3BPgEV6",
			"type": "rectangle",
			"x": -721.5,
			"y": -18.22,
			"width": 390,
			"height": 84,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#d8f5a2",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 340161021,
			"version": 2,
			"versionNonce": 520808808,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yK4UYjW4"
				},
				{
					"type": "arrow",
					"id": "dab5y9dW"
				},
				{
					"type": "arrow",
					"id": "L96FGfxm"
				},
				{
					"type": "arrow",
					"id": "42GGQYJ2"
				},
				{
					"type": "arrow",
					"id": "qhMxKqm4"
				},
				{
					"type": "arrow",
					"id": "ibFYjWie"
				},
				{
					"type": "arrow",
					"id": "NHFkcdry"
				},
				{
					"type": "arrow",
					"id": "YXbufHSR"
				},
				{
					"type": "arrow",
					"id": "6VP2Dx3C"
				},
				{
					"type": "arrow",
					"id": "uFg6D5DF"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3M"
		},
		{
			"id": "yK4UYjW4",
			"type": "text",
			"x": -701.5,
			"y": -6.22,
			"width": 350,
			"height": 60,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1991411380,
			"version": 2,
			"versionNonce": 1518387480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q6 AI 會寫 code，為什麼還要\n學",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Q3BPgEV6",
			"originalText": "Q6 AI 會寫 code，為什麼還要\n學",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3N"
		},
		{
			"id": "36QqdkxA",
			"type": "rectangle",
			"x": -1214.5,
			"y": -387.8,
			"width": 417,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1010267187,
			"version": 2,
			"versionNonce": 465140840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FPNCBegi"
				},
				{
					"type": "arrow",
					"id": "L96FGfxm"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3O"
		},
		{
			"id": "FPNCBegi",
			"type": "text",
			"x": -1200.5,
			"y": -378.8,
			"width": 389,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 54330029,
			"version": 2,
			"versionNonce": 871947800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI code＝candidate solution，不是答案證明",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "36QqdkxA",
			"originalText": "AI code＝candidate solution，不是答案證明",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3P"
		},
		{
			"id": "bXGrSrey",
			"type": "rectangle",
			"x": -1199.5,
			"y": -333.3,
			"width": 402,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1384048663,
			"version": 2,
			"versionNonce": 1260236648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DnfPFmnA"
				},
				{
					"type": "arrow",
					"id": "42GGQYJ2"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3Q"
		},
		{
			"id": "DnfPFmnA",
			"type": "text",
			"x": -1185.5,
			"y": -324.3,
			"width": 374,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2026297333,
			"version": 2,
			"versionNonce": 1113938712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Ask → Inspect → Run → Test → Revise",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bXGrSrey",
			"originalText": "Ask → Inspect → Run → Test → Revise",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3R"
		},
		{
			"id": "sSJDx3rS",
			"type": "rectangle",
			"x": -1223.5,
			"y": -258.05,
			"width": 426,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 81956529,
			"version": 2,
			"versionNonce": 92504680,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XcnamR3G"
				},
				{
					"type": "arrow",
					"id": "qhMxKqm4"
				},
				{
					"type": "arrow",
					"id": "V45R6Snf"
				},
				{
					"type": "arrow",
					"id": "9VPz9EAA"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3S"
		},
		{
			"id": "XcnamR3G",
			"type": "text",
			"x": -1209.5,
			"y": -249.05,
			"width": 398,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 735552761,
			"version": 2,
			"versionNonce": 674904088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "故意錯誤 Celsius：c = input(...) → TypeError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sSJDx3rS",
			"originalText": "故意錯誤 Celsius：c = input(...) → TypeError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3T"
		},
		{
			"id": "t9hhJ3de",
			"type": "rectangle",
			"x": -1557.5,
			"y": -278.8,
			"width": 274,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1173745722,
			"version": 2,
			"versionNonce": 968291688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "696sXF52"
				},
				{
					"type": "arrow",
					"id": "V45R6Snf"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3U"
		},
		{
			"id": "696sXF52",
			"type": "text",
			"x": -1545.5,
			"y": -271.8,
			"width": 250,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 308429168,
			"version": 2,
			"versionNonce": 426472728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "修：c = float(input(\"Celsius: \"))",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "t9hhJ3de",
			"originalText": "修：c = float(input(\"Celsius: \"))",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3V"
		},
		{
			"id": "qaniQwDL",
			"type": "rectangle",
			"x": -1645.5,
			"y": -230.8,
			"width": 362,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 69693252,
			"version": 2,
			"versionNonce": 486803560,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dQ9xW9DL"
				},
				{
					"type": "arrow",
					"id": "9VPz9EAA"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3W"
		},
		{
			"id": "dQ9xW9DL",
			"type": "text",
			"x": -1633.5,
			"y": -223.8,
			"width": 338,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1502905189,
			"version": 2,
			"versionNonce": 728568344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕錯在 / 5：\"0\" * 9 是字串重複，不會錯",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qaniQwDL",
			"originalText": "〔C〕錯在 / 5：\"0\" * 9 是字串重複，不會錯",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3X"
		},
		{
			"id": "dGtWMPnG",
			"type": "rectangle",
			"x": -1208.5,
			"y": -130.5,
			"width": 411,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"mmNDae7T"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1669285599,
			"version": 2,
			"versionNonce": 1530313576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "M6HyR3uL"
				},
				{
					"type": "arrow",
					"id": "ibFYjWie"
				},
				{
					"type": "arrow",
					"id": "YTEarLvi"
				},
				{
					"type": "arrow",
					"id": "mzRADRzq"
				},
				{
					"type": "arrow",
					"id": "VYiE5Hhh"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3Y"
		},
		{
			"id": "M6HyR3uL",
			"type": "text",
			"x": -1194.5,
			"y": -121.5,
			"width": 383,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"mmNDae7T"
			],
			"frameId": null,
			"roundness": null,
			"seed": 170996578,
			"version": 2,
			"versionNonce": 624103192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Test case＝specified input＋independently\njustified expected result",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dGtWMPnG",
			"originalText": "Test case＝specified input＋independently\njustified expected result",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3Z"
		},
		{
			"id": "SsR55Axy",
			"type": "rectangle",
			"x": -1567.5,
			"y": -182.8,
			"width": 299,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1789445950,
			"version": 2,
			"versionNonce": 1184566888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EV9LXmCW"
				},
				{
					"type": "arrow",
					"id": "YTEarLvi"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3a"
		},
		{
			"id": "EV9LXmCW",
			"type": "text",
			"x": -1555.5,
			"y": -175.8,
			"width": 275,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 661230690,
			"version": 2,
			"versionNonce": 1328639000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "0 → 32、100 → 212、−40 → −40",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SsR55Axy",
			"originalText": "0 → 32、100 → 212、−40 → −40",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3b"
		},
		{
			"id": "zbsWP2Kv",
			"type": "rectangle",
			"x": -1551.5,
			"y": -116,
			"width": 283,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"6cwG5hnT"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 753452493,
			"version": 2,
			"versionNonce": 134021480,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JCEqN5NY"
				},
				{
					"type": "arrow",
					"id": "mzRADRzq"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3c"
		},
		{
			"id": "JCEqN5NY",
			"type": "text",
			"x": -1539.5,
			"y": -109,
			"width": 259,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"6cwG5hnT"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1040907393,
			"version": 2,
			"versionNonce": 1130113304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "AI 同意 AI ≠ independent oracle",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zbsWP2Kv",
			"originalText": "AI 同意 AI ≠ independent oracle",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3d"
		},
		{
			"id": "HtnKfsti",
			"type": "rectangle",
			"x": -1492.5,
			"y": -49.2,
			"width": 224,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"7bejmFYE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1856909650,
			"version": 2,
			"versionNonce": 1319670888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DX3bJSqx"
				},
				{
					"type": "arrow",
					"id": "VYiE5Hhh"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3e"
		},
		{
			"id": "DX3bJSqx",
			"type": "text",
			"x": -1480.5,
			"y": -42.2,
			"width": 200,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"7bejmFYE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 787333467,
			"version": 2,
			"versionNonce": 1025984024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "通過測試是證據，不是證明",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HtnKfsti",
			"originalText": "通過測試是證據，不是證明",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3f"
		},
		{
			"id": "7KZ2PY4v",
			"type": "rectangle",
			"x": -1258.5,
			"y": -1.2,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1732072163,
			"version": 2,
			"versionNonce": 6932328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "p3AjVQpu"
				},
				{
					"type": "arrow",
					"id": "NHFkcdry"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3g"
		},
		{
			"id": "p3AjVQpu",
			"type": "text",
			"x": -1244.5,
			"y": 7.8,
			"width": 433,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 661605256,
			"version": 2,
			"versionNonce": 1770439448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "開發循環：Understand → Design → Generate →\nRun → Debug → Verify",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7KZ2PY4v",
			"originalText": "開發循環：Understand → Design → Generate →\nRun → Debug → Verify",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3h"
		},
		{
			"id": "2VvKCidz",
			"type": "rectangle",
			"x": -902.5,
			"y": 163.95,
			"width": 105,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"9kvvJzAd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 225600694,
			"version": 2,
			"versionNonce": 1770822248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yXtvzSBC"
				},
				{
					"type": "arrow",
					"id": "YXbufHSR"
				},
				{
					"type": "arrow",
					"id": "yf75aEP2"
				},
				{
					"type": "arrow",
					"id": "BnENnCRW"
				},
				{
					"type": "arrow",
					"id": "ADePJMJc"
				},
				{
					"type": "arrow",
					"id": "Us8dUaGA"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3i"
		},
		{
			"id": "yXtvzSBC",
			"type": "text",
			"x": -888.5,
			"y": 172.95,
			"width": 77,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"9kvvJzAd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 181518545,
			"version": 2,
			"versionNonce": 921608216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "三種錯誤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2VvKCidz",
			"originalText": "三種錯誤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3j"
		},
		{
			"id": "53jydubM",
			"type": "rectangle",
			"x": -1265.5,
			"y": 75.8,
			"width": 303,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1106732113,
			"version": 2,
			"versionNonce": 1826426216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2i2LhSru"
				},
				{
					"type": "arrow",
					"id": "yf75aEP2"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3k"
		},
		{
			"id": "2i2LhSru",
			"type": "text",
			"x": -1253.5,
			"y": 82.8,
			"width": 279,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 278615870,
			"version": 2,
			"versionNonce": 626187544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Syntax：print(\"Hello\" → 無法 parse",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "53jydubM",
			"originalText": "Syntax：print(\"Hello\" → 無法 parse",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3l"
		},
		{
			"id": "8qfYyzUy",
			"type": "rectangle",
			"x": -1384.5,
			"y": 123.8,
			"width": 422,
			"height": 54,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1089517279,
			"version": 2,
			"versionNonce": 866590824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yeLyHTMp"
				},
				{
					"type": "arrow",
					"id": "BnENnCRW"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3m"
		},
		{
			"id": "yeLyHTMp",
			"type": "text",
			"x": -1372.5,
			"y": 130.8,
			"width": 398,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1002764044,
			"version": 2,
			"versionNonce": 371685912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Runtime：3 / 0 → ZeroDivisionError；\"65\" + 1 →\nTypeError；print(hello) → NameError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8qfYyzUy",
			"originalText": "Runtime：3 / 0 → ZeroDivisionError；\"65\" + 1 →\nTypeError；print(hello) → NameError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3n"
		},
		{
			"id": "H92xwVXa",
			"type": "rectangle",
			"x": -1346.5,
			"y": 191.8,
			"width": 384,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1584609144,
			"version": 2,
			"versionNonce": 1572262760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sgDWGz7h"
				},
				{
					"type": "arrow",
					"id": "ADePJMJc"
				},
				{
					"type": "arrow",
					"id": "rFyKbhjt"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3o"
		},
		{
			"id": "sgDWGz7h",
			"type": "text",
			"x": -1334.5,
			"y": 198.8,
			"width": 360,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 791752887,
			"version": 2,
			"versionNonce": 476083992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Logic：0 * 9 / 5 + 30 → 能跑但錯（應 +32）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "H92xwVXa",
			"originalText": "Logic：0 * 9 / 5 + 30 → 能跑但錯（應 +32）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3p"
		},
		{
			"id": "EQc8nfZW",
			"type": "rectangle",
			"x": -1645.5,
			"y": 191.8,
			"width": 239,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1238489190,
			"version": 2,
			"versionNonce": 827860584,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ib7P4kwk"
				},
				{
					"type": "arrow",
					"id": "rFyKbhjt"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3q"
		},
		{
			"id": "ib7P4kwk",
			"type": "text",
			"x": -1633.5,
			"y": 198.8,
			"width": 215,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 223317951,
			"version": 2,
			"versionNonce": 1282528280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕實際印 30.0，不是 30",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EQc8nfZW",
			"originalText": "〔C〕實際印 30.0，不是 30",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3r"
		},
		{
			"id": "9xUAN7W4",
			"type": "rectangle",
			"x": -1329.5,
			"y": 258.6,
			"width": 367,
			"height": 34,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#fff3bf",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"75FUxxFJ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 299883841,
			"version": 2,
			"versionNonce": 1263999336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "m2tWN87Y"
				},
				{
					"type": "arrow",
					"id": "Us8dUaGA"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3s"
		},
		{
			"id": "m2tWN87Y",
			"type": "text",
			"x": -1317.5,
			"y": 265.6,
			"width": 343,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"75FUxxFJ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1562405362,
			"version": 2,
			"versionNonce": 206541080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★ 「多數 logic error IDE 直接抓得到」→ F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9xUAN7W4",
			"originalText": "★ 「多數 logic error IDE 直接抓得到」→ F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3t"
		},
		{
			"id": "k95qc93B",
			"type": "rectangle",
			"x": -1190.5,
			"y": 306.6,
			"width": 393,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 149315359,
			"version": 2,
			"versionNonce": 1325378664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ByYupu8T"
				},
				{
					"type": "arrow",
					"id": "6VP2Dx3C"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3u"
		},
		{
			"id": "ByYupu8T",
			"type": "text",
			"x": -1176.5,
			"y": 315.6,
			"width": 365,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 822429750,
			"version": 2,
			"versionNonce": 1668132376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Debugging：Read error → Locate line →\nHypothesis → Test one fix",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "k95qc93B",
			"originalText": "Debugging：Read error → Locate line →\nHypothesis → Test one fix",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3v"
		},
		{
			"id": "7Z3cae74",
			"type": "rectangle",
			"x": -1242.5,
			"y": 383.6,
			"width": 445,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1767691840,
			"version": 2,
			"versionNonce": 371056488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2hckAhT6"
				},
				{
					"type": "arrow",
					"id": "uFg6D5DF"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3w"
		},
		{
			"id": "2hckAhT6",
			"type": "text",
			"x": -1228.5,
			"y": 392.6,
			"width": 417,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1871389174,
			"version": 2,
			"versionNonce": 1254107928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI 使用規範：可問解釋、candidate、最小修補、\n測試；要自己跑、比對、記錄、保密",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7Z3cae74",
			"originalText": "AI 使用規範：可問解釋、candidate、最小修補、\n測試；要自己跑、比對、記錄、保密",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3x"
		},
		{
			"id": "4EkgSF7R",
			"type": "rectangle",
			"x": -472.5,
			"y": 516.73,
			"width": 141,
			"height": 54,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#eebefa",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1521721254,
			"version": 2,
			"versionNonce": 1627239016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wzNrx5Wy"
				},
				{
					"type": "arrow",
					"id": "3Hpf9Hem"
				},
				{
					"type": "arrow",
					"id": "Y7VRynyy"
				},
				{
					"type": "arrow",
					"id": "uvRL4nCi"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b3y"
		},
		{
			"id": "wzNrx5Wy",
			"type": "text",
			"x": -452.5,
			"y": 528.73,
			"width": 101,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 230429181,
			"version": 2,
			"versionNonce": 2092632088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Practice",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4EkgSF7R",
			"originalText": "Practice",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3z"
		},
		{
			"id": "hU7BiJ48",
			"type": "rectangle",
			"x": -867.5,
			"y": 490.6,
			"width": 319,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#f8f0fc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1460474808,
			"version": 2,
			"versionNonce": 107685224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8ptsvM2K"
				},
				{
					"type": "arrow",
					"id": "Y7VRynyy"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b40"
		},
		{
			"id": "8ptsvM2K",
			"type": "text",
			"x": -853.5,
			"y": 499.6,
			"width": 291,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1320856478,
			"version": 2,
			"versionNonce": 1163019544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Gross pay：gross = hours * pay",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hU7BiJ48",
			"originalText": "Gross pay：gross = hours * pay",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b41"
		},
		{
			"id": "2CNBgvnv",
			"type": "rectangle",
			"x": -997.5,
			"y": 545.1,
			"width": 449,
			"height": 63,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#f8f0fc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 446290242,
			"version": 2,
			"versionNonce": 598882408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Rfk52uBz"
				},
				{
					"type": "arrow",
					"id": "uvRL4nCi"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b42"
		},
		{
			"id": "Rfk52uBz",
			"type": "text",
			"x": -983.5,
			"y": 554.1,
			"width": 421,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 226390301,
			"version": 2,
			"versionNonce": 1375330840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "km → miles：miles = km * 0.621371；至少兩個自\n己算的 test",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2CNBgvnv",
			"originalText": "km → miles：miles = km * 0.621371；至少兩個自\n己算的 test",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b43"
		},
		{
			"id": "fTacMbVR",
			"type": "rectangle",
			"x": -580.5,
			"y": 1032.7,
			"width": 249,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffec99",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1019053893,
			"version": 2,
			"versionNonce": 1285483368,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FsMZMj6A"
				},
				{
					"type": "arrow",
					"id": "8RSSvEzH"
				},
				{
					"type": "arrow",
					"id": "Q7watCAn"
				},
				{
					"type": "arrow",
					"id": "GnbaQCfz"
				},
				{
					"type": "arrow",
					"id": "bS4LcSNQ"
				},
				{
					"type": "arrow",
					"id": "8hkZivUE"
				},
				{
					"type": "arrow",
					"id": "7gwfDddQ"
				},
				{
					"type": "arrow",
					"id": "Zttx9Xr2"
				},
				{
					"type": "arrow",
					"id": "625nSLpm"
				},
				{
					"type": "arrow",
					"id": "3ZmP6jti"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b44"
		},
		{
			"id": "FsMZMj6A",
			"type": "text",
			"x": -560.5,
			"y": 1044.7,
			"width": 209,
			"height": 30,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 175908991,
			"version": 2,
			"versionNonce": 27647768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q7 Git 與 GitHub",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fTacMbVR",
			"originalText": "Q7 Git 與 GitHub",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b45"
		},
		{
			"id": "qwC2XFd2",
			"type": "rectangle",
			"x": -1109.5,
			"y": 652.1,
			"width": 453,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 672338382,
			"version": 2,
			"versionNonce": 998063720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GWfbnSsx"
				},
				{
					"type": "arrow",
					"id": "Q7watCAn"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b46"
		},
		{
			"id": "GWfbnSsx",
			"type": "text",
			"x": -1095.5,
			"y": 661.1,
			"width": 425,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1691842699,
			"version": 2,
			"versionNonce": 885668888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "version control：取代 main_final2.py 式手動版本",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qwC2XFd2",
			"originalText": "version control：取代 main_final2.py 式手動版本",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b47"
		},
		{
			"id": "v5kmFtPP",
			"type": "rectangle",
			"x": -1090.5,
			"y": 706.6,
			"width": 434,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 392075555,
			"version": 2,
			"versionNonce": 18428264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QrPxG6MB"
				},
				{
					"type": "arrow",
					"id": "GnbaQCfz"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b48"
		},
		{
			"id": "QrPxG6MB",
			"type": "text",
			"x": -1076.5,
			"y": 715.6,
			"width": 406,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1224837512,
			"version": 2,
			"versionNonce": 492501272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Git（版本控制系統）≠ GitHub（遠端 hosting）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "v5kmFtPP",
			"originalText": "Git（版本控制系統）≠ GitHub（遠端 hosting）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b49"
		},
		{
			"id": "ZQ55Ex4Z",
			"type": "rectangle",
			"x": -1080.5,
			"y": 761.1,
			"width": 424,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1358159598,
			"version": 2,
			"versionNonce": 884917352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WJ67fx4p"
				},
				{
					"type": "arrow",
					"id": "bS4LcSNQ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4A"
		},
		{
			"id": "WJ67fx4p",
			"type": "text",
			"x": -1066.5,
			"y": 770.1,
			"width": 396,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 759423988,
			"version": 2,
			"versionNonce": 248256024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Repository＝project folder＋version history\n（.git）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZQ55Ex4Z",
			"originalText": "Repository＝project folder＋version history\n（.git）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4B"
		},
		{
			"id": "CeecciQr",
			"type": "rectangle",
			"x": -871.5,
			"y": 969.05,
			"width": 215,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1708350043,
			"version": 2,
			"versionNonce": 607778664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LjzDamdj"
				},
				{
					"type": "arrow",
					"id": "8hkZivUE"
				},
				{
					"type": "arrow",
					"id": "E4A8WdMJ"
				},
				{
					"type": "arrow",
					"id": "efN33tme"
				},
				{
					"type": "arrow",
					"id": "PnVt6d6y"
				},
				{
					"type": "arrow",
					"id": "dhZSaF74"
				},
				{
					"type": "arrow",
					"id": "VTsxDA4w"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4C"
		},
		{
			"id": "LjzDamdj",
			"type": "text",
			"x": -857.5,
			"y": 978.05,
			"width": 187,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 286697834,
			"version": 2,
			"versionNonce": 1309774616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Save／Commit／Push",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CeecciQr",
			"originalText": "Save／Commit／Push",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4D"
		},
		{
			"id": "8Y4fkQTj",
			"type": "rectangle",
			"x": -1192.5,
			"y": 838.1,
			"width": 261,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 559896428,
			"version": 2,
			"versionNonce": 64408168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "A35MjH8t"
				},
				{
					"type": "arrow",
					"id": "E4A8WdMJ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4E"
		},
		{
			"id": "A35MjH8t",
			"type": "text",
			"x": -1180.5,
			"y": 845.1,
			"width": 237,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 824663911,
			"version": 2,
			"versionNonce": 1637838872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Save：寫回本機檔案（Ctrl+S）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8Y4fkQTj",
			"originalText": "Save：寫回本機檔案（Ctrl+S）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4F"
		},
		{
			"id": "HsWXd9ch",
			"type": "rectangle",
			"x": -1237.5,
			"y": 904.9,
			"width": 306,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"Y8igY8uY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 626576531,
			"version": 2,
			"versionNonce": 509689192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xUTMKWRp"
				},
				{
					"type": "arrow",
					"id": "efN33tme"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4G"
		},
		{
			"id": "xUTMKWRp",
			"type": "text",
			"x": -1225.5,
			"y": 911.9,
			"width": 282,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Y8igY8uY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 742975344,
			"version": 2,
			"versionNonce": 1634315544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Commit：local checkpoint＋message",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HsWXd9ch",
			"originalText": "Commit：local checkpoint＋message",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4H"
		},
		{
			"id": "xC9NrDtg",
			"type": "rectangle",
			"x": -1106.5,
			"y": 971.7,
			"width": 175,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"h7F3wWuG"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 483101850,
			"version": 2,
			"versionNonce": 86331496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XncGssgp"
				},
				{
					"type": "arrow",
					"id": "PnVt6d6y"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4I"
		},
		{
			"id": "XncGssgp",
			"type": "text",
			"x": -1094.5,
			"y": 978.7,
			"width": 151,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"h7F3wWuG"
			],
			"frameId": null,
			"roundness": null,
			"seed": 374241495,
			"version": 2,
			"versionNonce": 1189366296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Push：傳到 remote",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xC9NrDtg",
			"originalText": "Push：傳到 remote",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4J"
		},
		{
			"id": "vEBmcvzL",
			"type": "rectangle",
			"x": -1354.5,
			"y": 1019.7,
			"width": 423,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 192411483,
			"version": 2,
			"versionNonce": 1072628584,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tkJbs3ba"
				},
				{
					"type": "arrow",
					"id": "dhZSaF74"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4K"
		},
		{
			"id": "tkJbs3ba",
			"type": "text",
			"x": -1342.5,
			"y": 1026.7,
			"width": 399,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 790211675,
			"version": 2,
			"versionNonce": 1023624984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "流程：Edit + Save → Review + Commit → Push →\nVerify online",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vEBmcvzL",
			"originalText": "流程：Edit + Save → Review + Commit → Push →\nVerify online",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4L"
		},
		{
			"id": "yRsJ3Xv4",
			"type": "rectangle",
			"x": -1357.5,
			"y": 1106.5,
			"width": 426,
			"height": 34,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"YNTHzANM"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 411713578,
			"version": 2,
			"versionNonce": 2097829480,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4QHKH66v"
				},
				{
					"type": "arrow",
					"id": "VTsxDA4w"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4M"
		},
		{
			"id": "4QHKH66v",
			"type": "text",
			"x": -1345.5,
			"y": 1113.5,
			"width": 402,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YNTHzANM"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1108676189,
			"version": 2,
			"versionNonce": 1882891288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "commit 之後再改、再存，要重新 commit 才會被 push",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yRsJ3Xv4",
			"originalText": "commit 之後再改、再存，要重新 commit 才會被 push",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4N"
		},
		{
			"id": "NZxhhgD6",
			"type": "rectangle",
			"x": -1110.5,
			"y": 1154.5,
			"width": 454,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 674935102,
			"version": 2,
			"versionNonce": 1094928744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RqBuL4rC"
				},
				{
					"type": "arrow",
					"id": "7gwfDddQ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4O"
		},
		{
			"id": "RqBuL4rC",
			"type": "text",
			"x": -1096.5,
			"y": 1163.5,
			"width": 426,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 802221657,
			"version": 2,
			"versionNonce": 1585340696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "GitHub Desktop：第一次 Publish repository，之\n後 Push origin",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NZxhhgD6",
			"originalText": "GitHub Desktop：第一次 Publish repository，之\n後 Push origin",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4P"
		},
		{
			"id": "D29sHNTm",
			"type": "rectangle",
			"x": -1117.5,
			"y": 1250.3,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"y67hHGkb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1073131259,
			"version": 2,
			"versionNonce": 400940136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "U3qgUd2v"
				},
				{
					"type": "arrow",
					"id": "Zttx9Xr2"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4Q"
		},
		{
			"id": "U3qgUd2v",
			"type": "text",
			"x": -1103.5,
			"y": 1259.3,
			"width": 433,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"y67hHGkb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 615724476,
			"version": 2,
			"versionNonce": 658669080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Verify online：看得到 main.py、最新 commit、第二\n次修改",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "D29sHNTm",
			"originalText": "Verify online：看得到 main.py、最新 commit、第二\n次修改",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4R"
		},
		{
			"id": "JeTAY4FC",
			"type": "rectangle",
			"x": -1118.5,
			"y": 1327.3,
			"width": 462,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1058907115,
			"version": 2,
			"versionNonce": 1119752040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rc78fJU2"
				},
				{
					"type": "arrow",
					"id": "625nSLpm"
				},
				{
					"type": "arrow",
					"id": "iwes5587"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4S"
		},
		{
			"id": "rc78fJU2",
			"type": "text",
			"x": -1104.5,
			"y": 1336.3,
			"width": 434,
			"height": 45,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 531420860,
			"version": 2,
			"versionNonce": 1534786328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不能 commit：密碼、API key、token、私人資料、\n別人答案、未檢查的 AI transcript",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JeTAY4FC",
			"originalText": "不能 commit：密碼、API key、token、私人資料、\n別人答案、未檢查的 AI transcript",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4T"
		},
		{
			"id": "jFWBDia4",
			"type": "rectangle",
			"x": -1596.5,
			"y": 1331.8,
			"width": 418,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 298767066,
			"version": 2,
			"versionNonce": 1779950184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9pukLtAt"
				},
				{
					"type": "arrow",
					"id": "iwes5587"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4U"
		},
		{
			"id": "9pukLtAt",
			"type": "text",
			"x": -1584.5,
			"y": 1338.8,
			"width": 394,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2023128676,
			"version": 2,
			"versionNonce": 1302059032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": ".gitignore 只擋未追蹤的檔；已 commit 的 secret →\nrevoke／rotate",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jFWBDia4",
			"originalText": ".gitignore 只擋未追蹤的檔；已 commit 的 secret →\nrevoke／rotate",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4V"
		},
		{
			"id": "JNT3xBRn",
			"type": "rectangle",
			"x": -1117.5,
			"y": 1404.3,
			"width": 461,
			"height": 85.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1066666019,
			"version": 2,
			"versionNonce": 1287607656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WCY2YtMd"
				},
				{
					"type": "arrow",
					"id": "3ZmP6jti"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4W"
		},
		{
			"id": "WCY2YtMd",
			"type": "text",
			"x": -1103.5,
			"y": 1413.3,
			"width": 433,
			"height": 67.5,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1918495365,
			"version": 2,
			"versionNonce": 1637422360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "CLI：git init -b main → git add → git commit\n-m → git remote add origin → git push -u origin\nmain",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JNT3xBRn",
			"originalText": "CLI：git init -b main → git add → git commit\n-m → git remote add origin → git push -u origin\nmain",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4X"
		},
		{
			"id": "KN9hFdpx",
			"type": "rectangle",
			"x": 1002.5,
			"y": -794,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YrUenJFB"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1679060743,
			"version": 2,
			"versionNonce": 1879074920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JcU95eeE"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4Y"
		},
		{
			"id": "JcU95eeE",
			"type": "text",
			"x": 1009.5,
			"y": -791,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YrUenJFB"
			],
			"frameId": null,
			"roundness": null,
			"seed": 517258831,
			"version": 2,
			"versionNonce": 1558622744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KN9hFdpx",
			"originalText": "Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4Z"
		},
		{
			"id": "9LcK8VHE",
			"type": "rectangle",
			"x": 892.5,
			"y": -124.6,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"CGCMHuqA"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1312008357,
			"version": 2,
			"versionNonce": 1336351592,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sMcPZkne"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4a"
		},
		{
			"id": "sMcPZkne",
			"type": "text",
			"x": 899.5,
			"y": -121.6,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"CGCMHuqA"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1484849880,
			"version": 2,
			"versionNonce": 913878808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q002",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9LcK8VHE",
			"originalText": "Q002",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4b"
		},
		{
			"id": "7iMgYCWw",
			"type": "rectangle",
			"x": 1341.5,
			"y": -39.95,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Q4MeYS7H"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1440271783,
			"version": 2,
			"versionNonce": 234843752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bNHKk7Pa"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4c"
		},
		{
			"id": "bNHKk7Pa",
			"type": "text",
			"x": 1348.5,
			"y": -36.95,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Q4MeYS7H"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1354873415,
			"version": 2,
			"versionNonce": 1724058648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T002",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7iMgYCWw",
			"originalText": "T002",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4d"
		},
		{
			"id": "kh4CB38K",
			"type": "rectangle",
			"x": 1360.5,
			"y": 162.85,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Gfs8BXKR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1751371325,
			"version": 2,
			"versionNonce": 601186664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uVKq9viP"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4e"
		},
		{
			"id": "uVKq9viP",
			"type": "text",
			"x": 1367.5,
			"y": 165.85,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Gfs8BXKR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 433234046,
			"version": 2,
			"versionNonce": 934922520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kh4CB38K",
			"originalText": "T001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4f"
		},
		{
			"id": "PNZG7qut",
			"type": "rectangle",
			"x": 1054.5,
			"y": 997.65,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"de7ntvWW"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 577784263,
			"version": 2,
			"versionNonce": 276100200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WjFKCGkn"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4g"
		},
		{
			"id": "WjFKCGkn",
			"type": "text",
			"x": 1061.5,
			"y": 1000.65,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"de7ntvWW"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1074920319,
			"version": 2,
			"versionNonce": 349234712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PNZG7qut",
			"originalText": "Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4h"
		},
		{
			"id": "8jsRXn4c",
			"type": "rectangle",
			"x": -731.5,
			"y": -1174.3,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"UT3pU2Sz"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1975034895,
			"version": 2,
			"versionNonce": 162146152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xEJjgTtr"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4i"
		},
		{
			"id": "xEJjgTtr",
			"type": "text",
			"x": -724.5,
			"y": -1171.3,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"UT3pU2Sz"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2040473558,
			"version": 2,
			"versionNonce": 1526489880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T007",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8jsRXn4c",
			"originalText": "T007",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4j"
		},
		{
			"id": "EwZGBgvg",
			"type": "rectangle",
			"x": -731.5,
			"y": -511.85,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"eawEQrjH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1143937781,
			"version": 2,
			"versionNonce": 734067304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LSVrg2ja"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4k"
		},
		{
			"id": "LSVrg2ja",
			"type": "text",
			"x": -724.5,
			"y": -508.85,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"eawEQrjH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 422172027,
			"version": 2,
			"versionNonce": 682639384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T013",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EwZGBgvg",
			"originalText": "T013",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4l"
		},
		{
			"id": "u9f4BEee",
			"type": "rectangle",
			"x": -840.5,
			"y": -149.3,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"mmNDae7T"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 851763897,
			"version": 2,
			"versionNonce": 696610152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aVBwDQXQ"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4m"
		},
		{
			"id": "aVBwDQXQ",
			"type": "text",
			"x": -833.5,
			"y": -146.3,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"mmNDae7T"
			],
			"frameId": null,
			"roundness": null,
			"seed": 314211500,
			"version": 2,
			"versionNonce": 769686808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T010",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "u9f4BEee",
			"originalText": "T010",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4n"
		},
		{
			"id": "mahsfHRQ",
			"type": "rectangle",
			"x": -1311.5,
			"y": -134.8,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"6cwG5hnT"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 322734393,
			"version": 2,
			"versionNonce": 2084798568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3QMfaVkx"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4o"
		},
		{
			"id": "3QMfaVkx",
			"type": "text",
			"x": -1304.5,
			"y": -131.8,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"6cwG5hnT"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1591015244,
			"version": 2,
			"versionNonce": 2080447000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T086",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mahsfHRQ",
			"originalText": "T086",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4p"
		},
		{
			"id": "LXSqFbdD",
			"type": "rectangle",
			"x": -1311.5,
			"y": -68,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"7bejmFYE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 109836868,
			"version": 2,
			"versionNonce": 331821928,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zsUhqKGS"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4q"
		},
		{
			"id": "zsUhqKGS",
			"type": "text",
			"x": -1304.5,
			"y": -65,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"7bejmFYE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1687664729,
			"version": 2,
			"versionNonce": 1443239704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q005",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LXSqFbdD",
			"originalText": "Q005",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4r"
		},
		{
			"id": "gdMJnD7E",
			"type": "rectangle",
			"x": -840.5,
			"y": 145.15,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"9kvvJzAd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1607573412,
			"version": 2,
			"versionNonce": 106727016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qr84Fa63"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4s"
		},
		{
			"id": "qr84Fa63",
			"type": "text",
			"x": -833.5,
			"y": 148.15,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"9kvvJzAd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1115295439,
			"version": 2,
			"versionNonce": 6517784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q003",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gdMJnD7E",
			"originalText": "Q003",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4t"
		},
		{
			"id": "rXUihshX",
			"type": "rectangle",
			"x": -1005.5,
			"y": 239.8,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"75FUxxFJ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1818234860,
			"version": 2,
			"versionNonce": 1087338856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pvAkkRnM"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4u"
		},
		{
			"id": "pvAkkRnM",
			"type": "text",
			"x": -998.5,
			"y": 242.8,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"75FUxxFJ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1880403891,
			"version": 2,
			"versionNonce": 286077208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T008",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rXUihshX",
			"originalText": "T008",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4v"
		},
		{
			"id": "VspXQhMJ",
			"type": "rectangle",
			"x": -974.5,
			"y": 886.1,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Y8igY8uY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1471501820,
			"version": 2,
			"versionNonce": 913050728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2ttnxixi"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4w"
		},
		{
			"id": "2ttnxixi",
			"type": "text",
			"x": -967.5,
			"y": 889.1,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"Y8igY8uY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1250253881,
			"version": 2,
			"versionNonce": 1064783384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T009",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VspXQhMJ",
			"originalText": "T009",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4x"
		},
		{
			"id": "kug3Zaxr",
			"type": "rectangle",
			"x": -974.5,
			"y": 952.9,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"h7F3wWuG"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2130900989,
			"version": 2,
			"versionNonce": 285097832,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ASQkmGV7"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b4y"
		},
		{
			"id": "ASQkmGV7",
			"type": "text",
			"x": -967.5,
			"y": 955.9,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"h7F3wWuG"
			],
			"frameId": null,
			"roundness": null,
			"seed": 473945504,
			"version": 2,
			"versionNonce": 882232088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q004",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kug3Zaxr",
			"originalText": "Q004",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4z"
		},
		{
			"id": "7JT9pNQx",
			"type": "rectangle",
			"x": -974.5,
			"y": 1087.7,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YNTHzANM"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 29849546,
			"version": 2,
			"versionNonce": 1624380008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "a2TguZv3"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b50"
		},
		{
			"id": "a2TguZv3",
			"type": "text",
			"x": -967.5,
			"y": 1090.7,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"YNTHzANM"
			],
			"frameId": null,
			"roundness": null,
			"seed": 285932814,
			"version": 2,
			"versionNonce": 1524410392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T087",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7JT9pNQx",
			"originalText": "T087",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b51"
		},
		{
			"id": "GhiZeUFb",
			"type": "rectangle",
			"x": -699.5,
			"y": 1231.5,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"y67hHGkb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 19821411,
			"version": 2,
			"versionNonce": 1286833512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JSzGBQm4"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b52"
		},
		{
			"id": "JSzGBQm4",
			"type": "text",
			"x": -692.5,
			"y": 1234.5,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"y67hHGkb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1702043042,
			"version": 2,
			"versionNonce": 775939352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q035",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GhiZeUFb",
			"originalText": "Q035",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b53"
		},
		{
			"id": "BLUsN9kk",
			"type": "text",
			"x": -1645.5,
			"y": -1746.8,
			"width": 1075,
			"height": 50,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 846451357,
			"version": 2,
			"versionNonce": 1106155624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 1｜Deck 1：電腦如何解決問題（W1）",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 1｜Deck 1：電腦如何解決問題（W1）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b54"
		},
		{
			"id": "wPjss35v",
			"type": "text",
			"x": -1645.5,
			"y": -1684.8,
			"width": 1545,
			"height": 45,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1696724861,
			"version": 2,
			"versionNonce": 204702232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Deck 1 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的練\n習題。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Deck 1 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的練\n習題。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b55"
		},
		{
			"id": "DAhP6mFq",
			"type": "rectangle",
			"x": -1645.5,
			"y": -1617.8,
			"width": 137,
			"height": 38,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "#fff3bf",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 602107139,
			"version": 2,
			"versionNonce": 609176424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5ZsdNB3X"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b56"
		},
		{
			"id": "5ZsdNB3X",
			"type": "text",
			"x": -1631.5,
			"y": -1608.8,
			"width": 109,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1129879434,
			"version": 2,
			"versionNonce": 61570840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★ 考古題考過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DAhP6mFq",
			"originalText": "★ 考古題考過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b57"
		},
		{
			"id": "5DrsQ9tF",
			"type": "rectangle",
			"x": -1484.5,
			"y": -1617.8,
			"width": 120,
			"height": 38,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 333518350,
			"version": 2,
			"versionNonce": 2116132456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JpdU3wEr"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b58"
		},
		{
			"id": "JpdU3wEr",
			"type": "text",
			"x": -1470.5,
			"y": -1608.8,
			"width": 92,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1790695503,
			"version": 2,
			"versionNonce": 622582808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5DrsQ9tF",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b59"
		},
		{
			"id": "DhBvbDY9",
			"type": "rectangle",
			"x": -1340.5,
			"y": -1617.8,
			"width": 330,
			"height": 38,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 474757661,
			"version": 2,
			"versionNonce": 808554856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zAstH6Me"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b5A"
		},
		{
			"id": "zAstH6Me",
			"type": "text",
			"x": -1326.5,
			"y": -1608.8,
			"width": 302,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 427803170,
			"version": 2,
			"versionNonce": 1383635224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕Claude 補充（投影片與講義沒有）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DhBvbDY9",
			"originalText": "〔C〕Claude 補充（投影片與講義沒有）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5B"
		},
		{
			"id": "z7cZqJPr",
			"type": "rectangle",
			"x": -986.5,
			"y": -1617.8,
			"width": 278,
			"height": 38,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1436719427,
			"version": 2,
			"versionNonce": 566961256,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "H6F4uy3f"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b5C"
		},
		{
			"id": "H6F4uy3f",
			"type": "text",
			"x": -972.5,
			"y": -1608.8,
			"width": 250,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 759295347,
			"version": 2,
			"versionNonce": 255178264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例題考到、原本心智圖沒有的觀念",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "z7cZqJPr",
			"originalText": "例題考到、原本心智圖沒有的觀念",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5D"
		},
		{
			"id": "g8vFBrjq",
			"type": "rectangle",
			"x": -684.5,
			"y": -1610.2,
			"width": 90,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#1c7ed6",
			"backgroundColor": "#d0ebff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1773766510,
			"version": 2,
			"versionNonce": 1891260264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GATYKYkx"
				}
			],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"index": "b5E"
		},
		{
			"id": "GATYKYkx",
			"type": "text",
			"x": -677.5,
			"y": -1607.2,
			"width": 76,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#1864ab",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1016924985,
			"version": 2,
			"versionNonce": 1346843416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001 Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g8vFBrjq",
			"originalText": "T001 Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5F"
		},
		{
			"id": "NrJ6ptZ4",
			"type": "text",
			"x": -586.5,
			"y": -1608.8,
			"width": 101,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1946515621,
			"version": 2,
			"versionNonce": 558574184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858132595,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "老師例題題號",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "老師例題題號",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5G"
		}
	],
	"appState": {
		"gridSize": 20,
		"viewBackgroundColor": "#ffffff"
	},
	"files": {}
}
```
%%