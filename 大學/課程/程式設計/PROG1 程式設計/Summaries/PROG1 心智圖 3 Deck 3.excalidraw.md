---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Deck 3 整理]]"
  - "Midterm_Practice_Student.pdf（老師的 140 題例題，T001–T100、Q001–Q040）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
程式如何做決策
Deck 3・W6 ^bWxeGJEJ

驅動問題 ^qVLLdwqV

有效資料 → 報告；無效 → 說明原因，不計算、不
除以零 ^AdtBi8sA

新政策：Short ≤ 30 分；Medium ≤ 60 分；Long
> 60 分 ^i8iPZR9s

寫下的假設 ≠ 會執行的檢查 ^J8DAgndW

Q1 規則變成是非問題 ^XwZWBQNi

v0.3 規則 ^AJB5XGLX

route_name == "" → 拒絕（精確空字串） ^Cmve7PxL

距離非有限或負 → 拒絕；0 km 有效 ^J4mkAPev

時間 ≤ 0 → 拒絕 ^BuQxj4Ap

無效：只印第一個錯誤；有效：三行報告＋分類 ^Qwsqxd6c

比較運算子 > >= < <= == != → bool ^fr4rrez8

時間 > 0；距離 >= 0（⚠ 差一條橫線就是不同規則） ^eiAkqLnW

= 綁定；== 比較 ^a7P8AyCE

⚠ time_ok 存的是當時的 True，不會自動重算 ^G248DvWY

型態影響比較 ^TBmQBK8Y

"30" == 30 → False ^zSZXgtQA

⚠ "9" > "30" → True（文字順序） ^dLDWLZgH

⚠ "30" > 0 → TypeError ^xBxeyE9Q

math.isfinite：12.5、0.0 → True；inf、nan →
False ^PUDXs6aS

Q2 多個條件 ^p88rpDU9

and：全部成立；or：任一成立 ^Ym9paRc7

拒絕條件：(km < 0) or (min <= 0) ^vuqsDSaj

⚠ 寫成 and → 兩個都壞才拒絕；要測「單一欄位失敗」
才抓得到 ^mZBkU9cJ

d 有限時：not (d >= 0 and m > 0) 和 d < 0 or m <=
0 抓到同一批（De Morgan） ^JtyatGyk

not 是邏輯否定；& | ~ 是位元運算（不要用 ~ 當
not） ^y54TH8Xu

優先序：not > and > or ^2exS3nQg

valid and a or b ≠ valid and (a or b)（valid = False、
60 分：前者 True、後者 False） ^RVG3Tz9e

0 < t <= 30 ≡ (t > 0) and (t <= 30) ^uK6A4HUL

短路求值 ^Y46mpxjZ

and 左邊 False → 不算右邊（保護除法） ^qp3N87Jt

or 左邊 True → 不算右邊 ^tvFkejgX

⚠ duration_min == 30 or 60 → 60（truthy），
不是比較 ^7QCbMRsr

Lab 1：一般／零時間／空標籤／無窮距離／零距離
→ True、False、False、False、True ^ATq8ZB5V

Q3 條件選擇要執行的程式 ^QrTFtLKb

冒號開始區塊；縮排決定歸屬（四個空格是慣例） ^QkfUPJ2J

if／else：恰好走一條路 ^yCrPdSNa

印出 False 不會阻止下一行 ^gajdmmNi

⚠ 警告不是保護：除法在 if 外 → 印 Error 後仍
ZeroDivisionError ^BPKvS4Fh

合法縮排也可能是錯的演算法 ^UYLMNZBK

三種失敗 ^pECpZkni

Syntax：if duration_min > 0（缺冒號） ^8berH6jw

Runtime："30" > 0 ^ZSxJDWkf

Logic：duration_min >= 0（允許零） ^fCd9UdrF

Lab 2：(15, 30) → 30.00 km/h；(15, 0)、(15,
−1) → 只印錯誤 ^F6VTeSrN

Q4 超過兩種結果 ^s5pPCvM6

if／elif／else：第一個為真的分支勝出 ^KudHZCy3

45 → Medium ^3wfjydES

⚠ 兩個獨立 if 都會執行：20 → Short＋Medium ^XtPNnYVM

巢狀：外層先驗證，內層才分類（0 不能變 Short） ^dxZ9ZP6v

邊界：1、29、30 → Short；31、60 → Medium；
61 → Long ^HXtYwstk

用原始整數分鐘分類，不用格式化後的字串 ^j3yiZimh

Q5 條件順序也是規格 ^C8XNjJrw

⚠ 先判 <= 60 再判 <= 30 → Short 永遠到不了
（20 → Medium） ^ZYP5hkiP

Path reasoning：走到 elif t <= 60 時已知 t > 30 ^2tBuSyMt

錯誤優先序（v0.3） ^RAEdgxTS

1 空標籤 → 2 非有限距離 → 3 負距離 → 4 非正時間 ^dzFdsQZW

空標籤＋負距離＋零時間 → 只印標籤錯誤 ^W7e8p2u9

「只報第一個錯」vs「報全部錯」是不同需求 ^2KiXRfY9

拒絕案例不能出現任何報告 ^Sadh8Cyj

結果要完整且不重疊：錯誤／Short／Medium／
Long ^hF8KLynA

" "（只有空白）仍算非空；Deck 5 才改政策 ^HYv7LRip

電腦基礎：比較與跳躍 ^BuzLDfFZ

LOAD 放值 → CMP 比較 → JLT 小於就跳 →
OUT 印 → JMP 無條件跳 → HALT ^BZh4N4yX

score 59 → 跳到 fail；60 → pass 後 JMP done ^JBWLZeju

⚠ 刪掉 JMP done → pass、fail 都印（像兩個獨
立 if） ^FiZNquci

下一個指令不一定是下一行 ^amH9cDZu

Q6 測試決策、審查 AI ^EpmHH8Kh

三類測試 ^antPFiZX

邊界：29／30／31、59／60／61 ^Dcx6UwxB

單一欄位失敗：空標籤、負距離、零或負時間、NaN／
inf ^CnpYX4kH

互動：兩個錯同時出現、零距離＋有效時間 ^Y4yjqdii

故意錯誤 candidate ^MK365ugE

1 km／0 min → 除零（and 防護太弱） ^98RWaZub

−1 km／30 min → 被接受 ^v5SpFW3P

5 km／30 min → Medium（應 Short） ^EYpjnRPz

最小修補：and → or；< 30 → <= 30 ^yfmy5pSR

trip_decisions.py：驗證鏈 if／elif → 最後 else 裡
計算、分類、四行報告 ^Yy4cjxjq

Test case＝input＋expected＋actual＋pass/fail
理由 ^yUrqyHXJ

交付：spec_deck3.md、tests_deck3.md、
ai_use_deck3.md ^LjnV4GAd

選讀 ^963HiCPS

Truthiness ^7spme65L

bool(0) → False；bool("0") → True；bool("False")
→ True ^8AjE9ueP

⚠ and／or 回傳運算元：0 or 7 → 7；"ok" and 5 →
5 ^wt8tkr8u

not "" → True ^SfGHNx96

比較值用 ==，不要用 is ^jQ6JDutg

try／except ValueError：解析（能不能變型態）vs
驗證（值合不合法） ^bxAa5iQT

int("45.0") 仍失敗 ^JvygbpyM

不要偷偷放寬或收緊規格；新政策要新測試 ^eamME4sV

T026 ^4WFVbrvU

T032 ^9GX4L6LB

T034 T065 ^AymKDQR7

T027 ^bLdHDQDL

T028 ^afG799Ua

T067 ^Y2wgEgGY

T029 ^v8wccPmi

T062 ^8Ppz3SYs

T033 T064 Q013 Q031 ^kiMx4kUM

T063 ^ZwyiyrUF

Q015 ^VTh26KHd

T030 ^ZaeSyWpX

T031 T066 ^xmUxUQjL

Q011 ^233j98EQ

Q012 ^Awr8G2ZV

T093 Q014 ^QnUxpUQq

T088 ^2xRJBZKW

Q025 ^vGhL3wZR

T089 ^avYdyPby

PROG1 期中心智圖 3｜Deck 3：程式如何做決策（W6） ^7WEDfiYb

來源：PROG1 Deck 3 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的
練習題。 ^Ma77G7Tt

⚠ 易錯陷阱 ^vk9Ejpwm

例題考到、原本心智圖沒有的觀念 ^a56NreP3

T001 Q001 ^xGy9q9q2

老師例題題號 ^dbRrQyUV

T089 ^vkvey3MQ

Extension 延伸題，講義說不代表考試範圍 ^ZCbi9dXL

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "j2tUUGJP",
			"type": "arrow",
			"x": 163,
			"y": -0.0,
			"width": 150,
			"height": 983.72,
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
			"seed": 1411302571,
			"version": 2,
			"versionNonce": 328038168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-983.72
				],
				[
					150,
					-983.72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "u9xPJXUW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "2LCVj4Fz",
			"type": "arrow",
			"x": 454,
			"y": -983.72,
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
			"seed": 740041390,
			"version": 2,
			"versionNonce": 1333470824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-71.38
				],
				[
					76,
					-71.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "u9xPJXUW",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aiBxcLrW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "6eX3KPri",
			"type": "arrow",
			"x": 454,
			"y": -983.72,
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
			"seed": 28213756,
			"version": 2,
			"versionNonce": 1442763800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					5.62
				],
				[
					76,
					5.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "u9xPJXUW",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nn2sF63n",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "taU4fyrq",
			"type": "arrow",
			"x": 454,
			"y": -983.72,
			"width": 76,
			"height": 71.37,
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
			"seed": 1752043459,
			"version": 2,
			"versionNonce": 756685160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					71.37
				],
				[
					76,
					71.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "u9xPJXUW",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8AnYxESz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "kMYEspgm",
			"type": "arrow",
			"x": 163,
			"y": -0.0,
			"width": 150,
			"height": 513.15,
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
			"seed": 173498055,
			"version": 2,
			"versionNonce": 1547473176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-513.15
				],
				[
					150,
					-513.15
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "tv4BiSzd",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 245.95,
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
			"seed": 623808276,
			"version": 2,
			"versionNonce": 6466664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-245.95
				],
				[
					76,
					-245.95
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YXJFadxS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "KwLPUfbS",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 110.4,
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
			"seed": 752304609,
			"version": 2,
			"versionNonce": 767208984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-110.4
				],
				[
					76,
					-110.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VxqWkSYm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "dUaAqTVC",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 55.9,
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
			"seed": 297229863,
			"version": 2,
			"versionNonce": 589356904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-55.9
				],
				[
					76,
					-55.9
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pzeVp5ih",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "8iYGtjPL",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 17.4,
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
			"seed": 422313898,
			"version": 2,
			"versionNonce": 1131227928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					17.4
				],
				[
					76,
					17.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TKwQs3uM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "YAGzKDcH",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 116.65,
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
			"seed": 23588593,
			"version": 2,
			"versionNonce": 1436594792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					116.65
				],
				[
					76,
					116.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SEaE8tPe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "74Xz8ZCs",
			"type": "arrow",
			"x": 593,
			"y": -513.15,
			"width": 76,
			"height": 245.95,
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
			"seed": 1904195371,
			"version": 2,
			"versionNonce": 1472727064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					245.95
				],
				[
					76,
					245.95
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JtJreEDD",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "c2XsSbRw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "7QUh4cdU",
			"type": "arrow",
			"x": 782,
			"y": -759.1,
			"width": 60,
			"height": 72,
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
			"seed": 681573005,
			"version": 2,
			"versionNonce": 1856906600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-72
				],
				[
					60,
					-72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YXJFadxS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "p5ENSyVC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "uKwdFqQi",
			"type": "arrow",
			"x": 782,
			"y": -759.1,
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
			"seed": 424787290,
			"version": 2,
			"versionNonce": 918504728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "YXJFadxS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "czaHdg82",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "XQKFzUUQ",
			"type": "arrow",
			"x": 782,
			"y": -759.1,
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
			"seed": 243247523,
			"version": 2,
			"versionNonce": 194328680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "YXJFadxS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Gxtv3cVf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "QBdGhY3J",
			"type": "arrow",
			"x": 782,
			"y": -759.1,
			"width": 60,
			"height": 72,
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
			"seed": 2109940583,
			"version": 2,
			"versionNonce": 231137816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					72
				],
				[
					60,
					72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YXJFadxS",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vf4KmGgA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "fYntUZnB",
			"type": "arrow",
			"x": 1004,
			"y": -623.55,
			"width": 60,
			"height": 3.25,
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
			"seed": 1376790408,
			"version": 2,
			"versionNonce": 1075964776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "VxqWkSYm",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GbpbKeDw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "En9sFV7B",
			"type": "arrow",
			"x": 811,
			"y": -396.5,
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
			"seed": 786574498,
			"version": 2,
			"versionNonce": 1003675416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "SEaE8tPe",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "w5c43siw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "xTcaPQVj",
			"type": "arrow",
			"x": 811,
			"y": -396.5,
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
			"seed": 1534265527,
			"version": 2,
			"versionNonce": 1184906856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "SEaE8tPe",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fPEivy4z",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "vwEJHAdF",
			"type": "arrow",
			"x": 811,
			"y": -396.5,
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
			"seed": 1435694601,
			"version": 2,
			"versionNonce": 559365144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "SEaE8tPe",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aDSvpKZV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "x2AHxQ3e",
			"type": "arrow",
			"x": 163,
			"y": -0.0,
			"width": 150,
			"height": 178.23,
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
			"seed": 1336723144,
			"version": 2,
			"versionNonce": 802959720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					178.23
				],
				[
					150,
					178.23
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "We4KXPAG",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 330.88,
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
			"seed": 557016864,
			"version": 2,
			"versionNonce": 1883765016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-330.88
				],
				[
					76,
					-330.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tH83KLGC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "zYPpFbTG",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 226.23,
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
			"seed": 1492702206,
			"version": 2,
			"versionNonce": 320980072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-226.23
				],
				[
					76,
					-226.23
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RdyU62cE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "ts2hKbrx",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 91.53,
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
			"seed": 792721036,
			"version": 2,
			"versionNonce": 2082018840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-91.53
				],
				[
					76,
					-91.53
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EQfeNWBw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "WKXdxXGb",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 28.77,
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
			"seed": 958292394,
			"version": 2,
			"versionNonce": 1044182888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					28.77
				],
				[
					76,
					28.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kXSb4EYX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "6CVfd3v2",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 129.77,
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
			"seed": 150126126,
			"version": 2,
			"versionNonce": 163484440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					129.77
				],
				[
					76,
					129.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "itPh3Ns9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "sptjBB7g",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 235.07,
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
			"seed": 2094204348,
			"version": 2,
			"versionNonce": 1702480488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					235.07
				],
				[
					76,
					235.07
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "r3Fahhm6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "ULzNgfGy",
			"type": "arrow",
			"x": 501,
			"y": 178.23,
			"width": 76,
			"height": 330.87,
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
			"seed": 257973718,
			"version": 2,
			"versionNonce": 531394584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					330.87
				],
				[
					76,
					330.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gJFJHTbZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "L5q5e8UR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "rDXTt2A2",
			"type": "arrow",
			"x": 897,
			"y": -48,
			"width": 60,
			"height": 43.4,
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
			"seed": 613051857,
			"version": 2,
			"versionNonce": 1403272552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-43.4
				],
				[
					60,
					-43.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "RdyU62cE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "K97hpbHw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "s8afKjg9",
			"type": "arrow",
			"x": 897,
			"y": -48,
			"width": 60,
			"height": 43.4,
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
			"seed": 1761301132,
			"version": 2,
			"versionNonce": 1440132376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					43.4
				],
				[
					60,
					43.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "RdyU62cE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bXuBNbmk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "fcNYLRVL",
			"type": "arrow",
			"x": 813,
			"y": 207,
			"width": 60,
			"height": 29,
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
			"seed": 179705838,
			"version": 2,
			"versionNonce": 436752488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-29
				],
				[
					60,
					-29
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "kXSb4EYX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zQSZ2fib",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "GWPSZAEJ",
			"type": "arrow",
			"x": 813,
			"y": 207,
			"width": 60,
			"height": 29,
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
			"seed": 1202783973,
			"version": 2,
			"versionNonce": 632375832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					29
				],
				[
					60,
					29
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "kXSb4EYX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NGwdgqNK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "yqLsRSLh",
			"type": "arrow",
			"x": 757,
			"y": 308,
			"width": 60,
			"height": 24,
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
			"seed": 1909045500,
			"version": 2,
			"versionNonce": 1081213800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "itPh3Ns9",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "i6E32ZNs",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "ZwptvRuv",
			"type": "arrow",
			"x": 757,
			"y": 308,
			"width": 60,
			"height": 24,
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
			"seed": 222685690,
			"version": 2,
			"versionNonce": 976242456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "itPh3Ns9",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7VnFvi3u",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "5JQwzTuD",
			"type": "arrow",
			"x": 163,
			"y": -0.0,
			"width": 150,
			"height": 829.97,
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
			"seed": 1591218480,
			"version": 2,
			"versionNonce": 1965905512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					829.97
				],
				[
					150,
					829.97
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "RFNqir4v",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 225.12,
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
			"seed": 1347593108,
			"version": 2,
			"versionNonce": 1070048280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-225.12
				],
				[
					76,
					-225.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TTefqhXn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "j4dHRM8z",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 170.62,
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
			"seed": 1439016944,
			"version": 2,
			"versionNonce": 1023822184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-170.62
				],
				[
					76,
					-170.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xrJa2zMV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "4zzPYQ5w",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 116.12,
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
			"seed": 1278403885,
			"version": 2,
			"versionNonce": 879452440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-116.12
				],
				[
					76,
					-116.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vNAiBVLG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "Dih487av",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 50.37,
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
			"seed": 1141788314,
			"version": 2,
			"versionNonce": 591977576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-50.37
				],
				[
					76,
					-50.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "faAaj9fC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "4G46n7Vf",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 15.38,
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
			"seed": 1528098402,
			"version": 2,
			"versionNonce": 932150808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					15.38
				],
				[
					76,
					15.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YeCUaPvj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "WKJFcp67",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 114.63,
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
			"seed": 714295272,
			"version": 2,
			"versionNonce": 1774260072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					114.63
				],
				[
					76,
					114.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KNuYdWVm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "xbPFr5TV",
			"type": "arrow",
			"x": 647,
			"y": 829.97,
			"width": 76,
			"height": 225.13,
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
			"seed": 1159892673,
			"version": 2,
			"versionNonce": 1512569624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					225.13
				],
				[
					76,
					225.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "yJQ8FuvY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ghyN8WvG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "PTRiD5wr",
			"type": "arrow",
			"x": 828,
			"y": 944.6,
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
			"seed": 1190128745,
			"version": 2,
			"versionNonce": 951771752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "KNuYdWVm",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "X28yRBbN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "EiSKRgVQ",
			"type": "arrow",
			"x": 828,
			"y": 944.6,
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
			"seed": 683517451,
			"version": 2,
			"versionNonce": 1856559128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "KNuYdWVm",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jMt5wc8P",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "asdWc6Kh",
			"type": "arrow",
			"x": 828,
			"y": 944.6,
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
			"seed": 141045527,
			"version": 2,
			"versionNonce": 1325553000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "KNuYdWVm",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QjZugZeR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "XCRuDVUb",
			"type": "arrow",
			"x": -163,
			"y": -0.0,
			"width": 150,
			"height": 919.55,
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
			"seed": 143453448,
			"version": 2,
			"versionNonce": 1493570840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-919.55
				],
				[
					-150,
					-919.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "MPBM4Eeq",
			"type": "arrow",
			"x": -547,
			"y": -919.55,
			"width": 76,
			"height": 139.05,
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
			"seed": 690504367,
			"version": 2,
			"versionNonce": 836986984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-139.05
				],
				[
					-76,
					-139.05
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "hb5AVM6T",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "UqKDzuBW",
			"type": "arrow",
			"x": -547,
			"y": -919.55,
			"width": 76,
			"height": 65.75,
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
			"seed": 429512682,
			"version": 2,
			"versionNonce": 1588834840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-65.75
				],
				[
					-76,
					-65.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bJHt8yV7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "PUE8VSDA",
			"type": "arrow",
			"x": -547,
			"y": -919.55,
			"width": 76,
			"height": 11.25,
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
			"seed": 1596402364,
			"version": 2,
			"versionNonce": 1563040616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-11.25
				],
				[
					-76,
					-11.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "iDg7VeL5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "tqVgmUsz",
			"type": "arrow",
			"x": -547,
			"y": -919.55,
			"width": 76,
			"height": 73.3,
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
			"seed": 273927720,
			"version": 2,
			"versionNonce": 1990569752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					73.3
				],
				[
					-76,
					73.3
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aKx73SvN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "Nvx4NzMd",
			"type": "arrow",
			"x": -547,
			"y": -919.55,
			"width": 76,
			"height": 139.05,
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
			"seed": 939635676,
			"version": 2,
			"versionNonce": 1931636328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					139.05
				],
				[
					-76,
					139.05
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sUVzHpNC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WQMD5bQC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "qypdVUst",
			"type": "arrow",
			"x": -970,
			"y": -1058.6,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1777543498,
			"version": 2,
			"versionNonce": 424676376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "hb5AVM6T",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VgJfv6dK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "B9MsP7sT",
			"type": "arrow",
			"x": -163,
			"y": -0.0,
			"width": 150,
			"height": 464.83,
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
			"seed": 440954664,
			"version": 2,
			"versionNonce": 1821925736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-464.83
				],
				[
					-150,
					-464.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "JwJUf6DR",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 201.12,
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
			"seed": 157017567,
			"version": 2,
			"versionNonce": 279365912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-201.12
				],
				[
					-76,
					-201.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uFfvXEDY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "iALFdKtg",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 135.37,
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
			"seed": 1635796838,
			"version": 2,
			"versionNonce": 1222112360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-135.37
				],
				[
					-76,
					-135.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "B4FdktrU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "CKQMNrCP",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 60.12,
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
			"seed": 974327591,
			"version": 2,
			"versionNonce": 1209919000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-60.12
				],
				[
					-76,
					-60.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wb32mCZv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "d6rj2wDQ",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 15.13,
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
			"seed": 1412349291,
			"version": 2,
			"versionNonce": 1034757992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					15.13
				],
				[
					-76,
					15.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jCGNkjwQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "GwwaXJaP",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 69.63,
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
			"seed": 1491048410,
			"version": 2,
			"versionNonce": 480863000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					69.63
				],
				[
					-76,
					69.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rxqYyc44",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "6BVz5VF6",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 135.38,
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
			"seed": 666113812,
			"version": 2,
			"versionNonce": 1734605416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					135.38
				],
				[
					-76,
					135.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VTjibWuM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "JWPwMHeu",
			"type": "arrow",
			"x": -597,
			"y": -464.83,
			"width": 76,
			"height": 201.13,
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
			"seed": 287395704,
			"version": 2,
			"versionNonce": 750600216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					201.13
				],
				[
					-76,
					201.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "sLGLVj72",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pLVGbfsj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "chY84hpT",
			"type": "arrow",
			"x": -871,
			"y": -524.95,
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
			"seed": 673120979,
			"version": 2,
			"versionNonce": 2026401128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "wb32mCZv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8uThtVZj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "HSPhwQqt",
			"type": "arrow",
			"x": -871,
			"y": -524.95,
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
			"seed": 981419148,
			"version": 2,
			"versionNonce": 676166936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "wb32mCZv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "THh3Epc3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "erjiCHw5",
			"type": "arrow",
			"x": -163,
			"y": -0.0,
			"width": 150,
			"height": 69.33,
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
			"seed": 1578700327,
			"version": 2,
			"versionNonce": 1797685352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-69.33
				],
				[
					-150,
					-69.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "negL5YYY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "NWY43GNL",
			"type": "arrow",
			"x": -603,
			"y": -69.33,
			"width": 76,
			"height": 98.62,
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
			"seed": 1602353333,
			"version": 2,
			"versionNonce": 550378008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-98.62
				],
				[
					-76,
					-98.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "negL5YYY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3UyWXVEZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "dZL83q4w",
			"type": "arrow",
			"x": -603,
			"y": -69.33,
			"width": 76,
			"height": 32.87,
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
			"seed": 2145284682,
			"version": 2,
			"versionNonce": 776614760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-32.87
				],
				[
					-76,
					-32.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "negL5YYY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GV7FQYjm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "brGn2pzv",
			"type": "arrow",
			"x": -603,
			"y": -69.33,
			"width": 76,
			"height": 32.88,
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
			"seed": 1017337177,
			"version": 2,
			"versionNonce": 1496520472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					32.88
				],
				[
					-76,
					32.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "negL5YYY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KT4Viu2d",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "8P6RQgVM",
			"type": "arrow",
			"x": -603,
			"y": -69.33,
			"width": 76,
			"height": 98.63,
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
			"seed": 114970488,
			"version": 2,
			"versionNonce": 1484752488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					98.63
				],
				[
					-76,
					98.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "negL5YYY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7edf5FNs",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "88TRcwrp",
			"type": "arrow",
			"x": -163,
			"y": -0.0,
			"width": 150,
			"height": 420.6,
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
			"seed": 1843044270,
			"version": 2,
			"versionNonce": 368079896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					420.6
				],
				[
					-150,
					420.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "2XUrZisP",
			"type": "arrow",
			"x": -613,
			"y": 420.6,
			"width": 76,
			"height": 233.25,
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
			"seed": 1131429977,
			"version": 2,
			"versionNonce": 1452439912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-233.25
				],
				[
					-76,
					-233.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KcN8BHHC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "9r2YB3Jd",
			"type": "arrow",
			"x": -613,
			"y": 420.6,
			"width": 76,
			"height": 55.25,
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
			"seed": 1584428863,
			"version": 2,
			"versionNonce": 1828335896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-55.25
				],
				[
					-76,
					-55.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CgxUfdiT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "ac5McGp5",
			"type": "arrow",
			"x": -613,
			"y": 420.6,
			"width": 76,
			"height": 79.25,
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
			"seed": 1864866193,
			"version": 2,
			"versionNonce": 466553960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					79.25
				],
				[
					-76,
					79.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jzgfvXKA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "G42jdAKA",
			"type": "arrow",
			"x": -613,
			"y": 420.6,
			"width": 76,
			"height": 156.25,
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
			"seed": 1520022824,
			"version": 2,
			"versionNonce": 365186584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					156.25
				],
				[
					-76,
					156.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YG9uxCe6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "Qf8z93A2",
			"type": "arrow",
			"x": -613,
			"y": 420.6,
			"width": 76,
			"height": 233.25,
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
			"seed": 1401827110,
			"version": 2,
			"versionNonce": 1375813480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					233.25
				],
				[
					-76,
					233.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "aw5SCrXc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ygTauf4y",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "shh2Ua39",
			"type": "arrow",
			"x": -794,
			"y": 187.35,
			"width": 60,
			"height": 58,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1689231243,
			"version": 2,
			"versionNonce": 960678680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-58
				],
				[
					-60,
					-58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KcN8BHHC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Xa5gmUCN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0A"
		},
		{
			"id": "Jgv4J4kM",
			"type": "arrow",
			"x": -794,
			"y": 187.35,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 350582595,
			"version": 2,
			"versionNonce": 158667368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "KcN8BHHC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xsQ86cbd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0B"
		},
		{
			"id": "pberap7r",
			"type": "arrow",
			"x": -794,
			"y": 187.35,
			"width": 60,
			"height": 58,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 306845632,
			"version": 2,
			"versionNonce": 1105831960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					58
				],
				[
					-60,
					58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KcN8BHHC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2fdPc5MH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0C"
		},
		{
			"id": "bJ4gC3v5",
			"type": "arrow",
			"x": -889,
			"y": 365.35,
			"width": 60,
			"height": 72,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 580280642,
			"version": 2,
			"versionNonce": 1760986472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "CgxUfdiT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "digDASyT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0D"
		},
		{
			"id": "Z8f7s4ch",
			"type": "arrow",
			"x": -889,
			"y": 365.35,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 185931577,
			"version": 2,
			"versionNonce": 732751128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "CgxUfdiT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "D3dgSJa2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0E"
		},
		{
			"id": "nnZfNCKA",
			"type": "arrow",
			"x": -889,
			"y": 365.35,
			"width": 60,
			"height": 24,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1015529651,
			"version": 2,
			"versionNonce": 1574017128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "CgxUfdiT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9AvCXfpc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0F"
		},
		{
			"id": "wEeTSBRk",
			"type": "arrow",
			"x": -889,
			"y": 365.35,
			"width": 60,
			"height": 72,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 246781802,
			"version": 2,
			"versionNonce": 1409319448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "CgxUfdiT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zvVdube2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0G"
		},
		{
			"id": "w3fr4Up2",
			"type": "arrow",
			"x": -163,
			"y": -0.0,
			"width": 150,
			"height": 969.77,
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
			"seed": 1444045509,
			"version": 2,
			"versionNonce": 1272073064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					969.77
				],
				[
					-150,
					969.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HMzqYFEL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "baEtxFX4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0H"
		},
		{
			"id": "7ax2dzvN",
			"type": "arrow",
			"x": -405,
			"y": 969.77,
			"width": 76,
			"height": 107.62,
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
			"seed": 172187520,
			"version": 2,
			"versionNonce": 1238925080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-107.62
				],
				[
					-76,
					-107.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "baEtxFX4",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rjcXrDJc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0I"
		},
		{
			"id": "eHYGpinq",
			"type": "arrow",
			"x": -405,
			"y": 969.77,
			"width": 76,
			"height": 41.88,
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
			"seed": 1843864828,
			"version": 2,
			"versionNonce": 1027907176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					41.88
				],
				[
					-76,
					41.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "baEtxFX4",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eQreJ9fm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0J"
		},
		{
			"id": "MMwDkujb",
			"type": "arrow",
			"x": -405,
			"y": 969.77,
			"width": 76,
			"height": 107.63,
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
			"seed": 1449423101,
			"version": 2,
			"versionNonce": 497605656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					107.63
				],
				[
					-76,
					107.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "baEtxFX4",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YLqaCkQ9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0K"
		},
		{
			"id": "AyshnPEv",
			"type": "arrow",
			"x": -609,
			"y": 862.15,
			"width": 60,
			"height": 87,
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
			"seed": 655743528,
			"version": 2,
			"versionNonce": 318017896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-87
				],
				[
					-60,
					-87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjcXrDJc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dQeXU5Lc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0L"
		},
		{
			"id": "StEGpRy7",
			"type": "arrow",
			"x": -609,
			"y": 862.15,
			"width": 60,
			"height": 19,
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
			"seed": 2007197069,
			"version": 2,
			"versionNonce": 828741912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					-19
				],
				[
					-60,
					-19
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjcXrDJc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "DVFKXivD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0M"
		},
		{
			"id": "fi33azVU",
			"type": "arrow",
			"x": -609,
			"y": 862.15,
			"width": 60,
			"height": 39,
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
			"seed": 131251195,
			"version": 2,
			"versionNonce": 875439208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					39
				],
				[
					-60,
					39
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjcXrDJc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nrWWkCzx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0N"
		},
		{
			"id": "jSUcGJLR",
			"type": "arrow",
			"x": -609,
			"y": 862.15,
			"width": 60,
			"height": 87,
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
			"seed": 75434926,
			"version": 2,
			"versionNonce": 142784024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
					87
				],
				[
					-60,
					87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjcXrDJc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "iW22tSPx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0O"
		},
		{
			"id": "ACAhWCSi",
			"type": "arrow",
			"x": -941,
			"y": 1011.65,
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
			"seed": 743103685,
			"version": 2,
			"versionNonce": 1052596072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
				"elementId": "eQreJ9fm",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Dp9naX6k",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0P"
		},
		{
			"id": "HMzqYFEL",
			"type": "rectangle",
			"x": -163,
			"y": -67,
			"width": 326,
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
			"seed": 973582437,
			"version": 2,
			"versionNonce": 401879832,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bWxeGJEJ"
				},
				{
					"type": "arrow",
					"id": "j2tUUGJP"
				},
				{
					"type": "arrow",
					"id": "kMYEspgm"
				},
				{
					"type": "arrow",
					"id": "x2AHxQ3e"
				},
				{
					"type": "arrow",
					"id": "5JQwzTuD"
				},
				{
					"type": "arrow",
					"id": "XCRuDVUb"
				},
				{
					"type": "arrow",
					"id": "B9MsP7sT"
				},
				{
					"type": "arrow",
					"id": "erjiCHw5"
				},
				{
					"type": "arrow",
					"id": "88TRcwrp"
				},
				{
					"type": "arrow",
					"id": "w3fr4Up2"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0Q"
		},
		{
			"id": "bWxeGJEJ",
			"type": "text",
			"x": -131,
			"y": -45,
			"width": 262,
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
			"seed": 188741784,
			"version": 2,
			"versionNonce": 921578088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "程式如何做決策\nDeck 3・W6",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HMzqYFEL",
			"originalText": "程式如何做決策\nDeck 3・W6",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0R"
		},
		{
			"id": "u9xPJXUW",
			"type": "rectangle",
			"x": 313,
			"y": -1010.72,
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
			"seed": 70860871,
			"version": 2,
			"versionNonce": 372117528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qVLLdwqV"
				},
				{
					"type": "arrow",
					"id": "j2tUUGJP"
				},
				{
					"type": "arrow",
					"id": "2LCVj4Fz"
				},
				{
					"type": "arrow",
					"id": "6eX3KPri"
				},
				{
					"type": "arrow",
					"id": "taU4fyrq"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0S"
		},
		{
			"id": "qVLLdwqV",
			"type": "text",
			"x": 333,
			"y": -998.72,
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
			"seed": 1202196197,
			"version": 2,
			"versionNonce": 931962216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "驅動問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "u9xPJXUW",
			"originalText": "驅動問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0T"
		},
		{
			"id": "aiBxcLrW",
			"type": "rectangle",
			"x": 530,
			"y": -1086.6,
			"width": 450,
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
			"seed": 1922811302,
			"version": 2,
			"versionNonce": 1260670232,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AdtBi8sA"
				},
				{
					"type": "arrow",
					"id": "2LCVj4Fz"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0U"
		},
		{
			"id": "AdtBi8sA",
			"type": "text",
			"x": 544,
			"y": -1077.6,
			"width": 422,
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
			"seed": 917358950,
			"version": 2,
			"versionNonce": 568635496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "有效資料 → 報告；無效 → 說明原因，不計算、不\n除以零",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aiBxcLrW",
			"originalText": "有效資料 → 報告；無效 → 說明原因，不計算、不\n除以零",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0V"
		},
		{
			"id": "nn2sF63n",
			"type": "rectangle",
			"x": 530,
			"y": -1009.6,
			"width": 447,
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
			"seed": 1620267156,
			"version": 2,
			"versionNonce": 1615522328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "i8iPZR9s"
				},
				{
					"type": "arrow",
					"id": "6eX3KPri"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0W"
		},
		{
			"id": "i8iPZR9s",
			"type": "text",
			"x": 544,
			"y": -1000.6,
			"width": 419,
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
			"seed": 389084296,
			"version": 2,
			"versionNonce": 1304585064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "新政策：Short ≤ 30 分；Medium ≤ 60 分；Long\n> 60 分",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nn2sF63n",
			"originalText": "新政策：Short ≤ 30 分；Medium ≤ 60 分；Long\n> 60 分",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0X"
		},
		{
			"id": "8AnYxESz",
			"type": "rectangle",
			"x": 530,
			"y": -932.6,
			"width": 259,
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
			"seed": 320088360,
			"version": 2,
			"versionNonce": 815130392,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J8DAgndW"
				},
				{
					"type": "arrow",
					"id": "taU4fyrq"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0Y"
		},
		{
			"id": "J8DAgndW",
			"type": "text",
			"x": 544,
			"y": -923.6,
			"width": 231,
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
			"seed": 924503407,
			"version": 2,
			"versionNonce": 963753576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "寫下的假設 ≠ 會執行的檢查",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8AnYxESz",
			"originalText": "寫下的假設 ≠ 會執行的檢查",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0Z"
		},
		{
			"id": "JtJreEDD",
			"type": "rectangle",
			"x": 313,
			"y": -540.15,
			"width": 280,
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
			"seed": 2098958454,
			"version": 2,
			"versionNonce": 410600472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XwZWBQNi"
				},
				{
					"type": "arrow",
					"id": "kMYEspgm"
				},
				{
					"type": "arrow",
					"id": "tv4BiSzd"
				},
				{
					"type": "arrow",
					"id": "KwLPUfbS"
				},
				{
					"type": "arrow",
					"id": "dUaAqTVC"
				},
				{
					"type": "arrow",
					"id": "8iYGtjPL"
				},
				{
					"type": "arrow",
					"id": "YAGzKDcH"
				},
				{
					"type": "arrow",
					"id": "74Xz8ZCs"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0a"
		},
		{
			"id": "XwZWBQNi",
			"type": "text",
			"x": 333,
			"y": -528.15,
			"width": 240,
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
			"seed": 1184106300,
			"version": 2,
			"versionNonce": 968796520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q1 規則變成是非問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JtJreEDD",
			"originalText": "Q1 規則變成是非問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0b"
		},
		{
			"id": "YXJFadxS",
			"type": "rectangle",
			"x": 669,
			"y": -779.35,
			"width": 113,
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
			"seed": 337052832,
			"version": 2,
			"versionNonce": 1172898072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AJB5XGLX"
				},
				{
					"type": "arrow",
					"id": "tv4BiSzd"
				},
				{
					"type": "arrow",
					"id": "7QUh4cdU"
				},
				{
					"type": "arrow",
					"id": "uKwdFqQi"
				},
				{
					"type": "arrow",
					"id": "XQKFzUUQ"
				},
				{
					"type": "arrow",
					"id": "QBdGhY3J"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0c"
		},
		{
			"id": "AJB5XGLX",
			"type": "text",
			"x": 683,
			"y": -770.35,
			"width": 85,
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
			"seed": 1281759493,
			"version": 2,
			"versionNonce": 703937640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "v0.3 規則",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YXJFadxS",
			"originalText": "v0.3 規則",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0d"
		},
		{
			"id": "p5ENSyVC",
			"type": "rectangle",
			"x": 842,
			"y": -848.1,
			"width": 341,
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
			"seed": 936011990,
			"version": 2,
			"versionNonce": 140058136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Cmve7PxL"
				},
				{
					"type": "arrow",
					"id": "7QUh4cdU"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0e"
		},
		{
			"id": "Cmve7PxL",
			"type": "text",
			"x": 854,
			"y": -841.1,
			"width": 317,
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
			"seed": 679019966,
			"version": 2,
			"versionNonce": 467758952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "route_name == \"\" → 拒絕（精確空字串）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "p5ENSyVC",
			"originalText": "route_name == \"\" → 拒絕（精確空字串）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0f"
		},
		{
			"id": "czaHdg82",
			"type": "rectangle",
			"x": 842,
			"y": -800.1,
			"width": 298,
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
			"seed": 1640118991,
			"version": 2,
			"versionNonce": 549296920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J4mkAPev"
				},
				{
					"type": "arrow",
					"id": "uKwdFqQi"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0g"
		},
		{
			"id": "J4mkAPev",
			"type": "text",
			"x": 854,
			"y": -793.1,
			"width": 274,
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
			"seed": 1088121785,
			"version": 2,
			"versionNonce": 131023464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "距離非有限或負 → 拒絕；0 km 有效",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "czaHdg82",
			"originalText": "距離非有限或負 → 拒絕；0 km 有效",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0h"
		},
		{
			"id": "Gxtv3cVf",
			"type": "rectangle",
			"x": 842,
			"y": -752.1,
			"width": 155,
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
			"seed": 2107616647,
			"version": 2,
			"versionNonce": 294287384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BuQxj4Ap"
				},
				{
					"type": "arrow",
					"id": "XQKFzUUQ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0i"
		},
		{
			"id": "BuQxj4Ap",
			"type": "text",
			"x": 854,
			"y": -745.1,
			"width": 131,
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
			"seed": 1531931647,
			"version": 2,
			"versionNonce": 2089465192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "時間 ≤ 0 → 拒絕",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Gxtv3cVf",
			"originalText": "時間 ≤ 0 → 拒絕",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0j"
		},
		{
			"id": "vf4KmGgA",
			"type": "rectangle",
			"x": 842,
			"y": -704.1,
			"width": 373,
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
			"seed": 134183218,
			"version": 2,
			"versionNonce": 1857271064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Qwsqxd6c"
				},
				{
					"type": "arrow",
					"id": "QBdGhY3J"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0k"
		},
		{
			"id": "Qwsqxd6c",
			"type": "text",
			"x": 854,
			"y": -697.1,
			"width": 349,
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
			"seed": 527353344,
			"version": 2,
			"versionNonce": 1331677288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "無效：只印第一個錯誤；有效：三行報告＋分類",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vf4KmGgA",
			"originalText": "無效：只印第一個錯誤；有效：三行報告＋分類",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0l"
		},
		{
			"id": "VxqWkSYm",
			"type": "rectangle",
			"x": 669,
			"y": -643.8,
			"width": 335,
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
			"seed": 1777941355,
			"version": 2,
			"versionNonce": 766333464,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fr4rrez8"
				},
				{
					"type": "arrow",
					"id": "KwLPUfbS"
				},
				{
					"type": "arrow",
					"id": "fYntUZnB"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0m"
		},
		{
			"id": "fr4rrez8",
			"type": "text",
			"x": 683,
			"y": -634.8,
			"width": 307,
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
			"seed": 1186005972,
			"version": 2,
			"versionNonce": 1276803944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "比較運算子 > >= < <= == != → bool",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VxqWkSYm",
			"originalText": "比較運算子 > >= < <= == != → bool",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0n"
		},
		{
			"id": "GbpbKeDw",
			"type": "rectangle",
			"x": 1064,
			"y": -637.3,
			"width": 422,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"C6TwmiDR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 128187367,
			"version": 2,
			"versionNonce": 1969966872,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eiAkqLnW"
				},
				{
					"type": "arrow",
					"id": "fYntUZnB"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0o"
		},
		{
			"id": "eiAkqLnW",
			"type": "text",
			"x": 1076,
			"y": -630.3,
			"width": 398,
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
				"C6TwmiDR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 706183829,
			"version": 2,
			"versionNonce": 1694944872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "時間 > 0；距離 >= 0（⚠ 差一條橫線就是不同規則）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GbpbKeDw",
			"originalText": "時間 > 0；距離 >= 0（⚠ 差一條橫線就是不同規則）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0p"
		},
		{
			"id": "pzeVp5ih",
			"type": "rectangle",
			"x": 669,
			"y": -589.3,
			"width": 169,
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
			"seed": 357962413,
			"version": 2,
			"versionNonce": 1851894808,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "a7P8AyCE"
				},
				{
					"type": "arrow",
					"id": "dUaAqTVC"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0q"
		},
		{
			"id": "a7P8AyCE",
			"type": "text",
			"x": 683,
			"y": -580.3,
			"width": 141,
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
			"seed": 2013624448,
			"version": 2,
			"versionNonce": 1659945320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "= 綁定；== 比較",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pzeVp5ih",
			"originalText": "= 綁定；== 比較",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0r"
		},
		{
			"id": "TKwQs3uM",
			"type": "rectangle",
			"x": 669,
			"y": -516,
			"width": 425,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"Axh97NTL"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1813757259,
			"version": 2,
			"versionNonce": 310667544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G248DvWY"
				},
				{
					"type": "arrow",
					"id": "8iYGtjPL"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0s"
		},
		{
			"id": "G248DvWY",
			"type": "text",
			"x": 683,
			"y": -507,
			"width": 397,
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
				"Axh97NTL"
			],
			"frameId": null,
			"roundness": null,
			"seed": 226865116,
			"version": 2,
			"versionNonce": 354702440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ time_ok 存的是當時的 True，不會自動重算",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TKwQs3uM",
			"originalText": "⚠ time_ok 存的是當時的 True，不會自動重算",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0t"
		},
		{
			"id": "SEaE8tPe",
			"type": "rectangle",
			"x": 669,
			"y": -416.75,
			"width": 142,
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
			"seed": 1131327287,
			"version": 2,
			"versionNonce": 2101839384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TBmQBK8Y"
				},
				{
					"type": "arrow",
					"id": "YAGzKDcH"
				},
				{
					"type": "arrow",
					"id": "En9sFV7B"
				},
				{
					"type": "arrow",
					"id": "xTcaPQVj"
				},
				{
					"type": "arrow",
					"id": "vwEJHAdF"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0u"
		},
		{
			"id": "TBmQBK8Y",
			"type": "text",
			"x": 683,
			"y": -407.75,
			"width": 114,
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
			"seed": 410154943,
			"version": 2,
			"versionNonce": 23955304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "型態影響比較",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SEaE8tPe",
			"originalText": "型態影響比較",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0v"
		},
		{
			"id": "w5c43siw",
			"type": "rectangle",
			"x": 871,
			"y": -461.5,
			"width": 183,
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
			"seed": 1237583817,
			"version": 2,
			"versionNonce": 1000276760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zSZXgtQA"
				},
				{
					"type": "arrow",
					"id": "En9sFV7B"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0w"
		},
		{
			"id": "zSZXgtQA",
			"type": "text",
			"x": 883,
			"y": -454.5,
			"width": 159,
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
			"seed": 1335081013,
			"version": 2,
			"versionNonce": 337140328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"30\" == 30 → False",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "w5c43siw",
			"originalText": "\"30\" == 30 → False",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0x"
		},
		{
			"id": "fPEivy4z",
			"type": "rectangle",
			"x": 871,
			"y": -413.5,
			"width": 294,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
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
			"seed": 1851609611,
			"version": 2,
			"versionNonce": 469688344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dLDWLZgH"
				},
				{
					"type": "arrow",
					"id": "xTcaPQVj"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b0y"
		},
		{
			"id": "dLDWLZgH",
			"type": "text",
			"x": 883,
			"y": -406.5,
			"width": 270,
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
			"seed": 2119130466,
			"version": 2,
			"versionNonce": 1341181288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ \"9\" > \"30\" → True（文字順序）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fPEivy4z",
			"originalText": "⚠ \"9\" > \"30\" → True（文字順序）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0z"
		},
		{
			"id": "aDSvpKZV",
			"type": "rectangle",
			"x": 871,
			"y": -365.5,
			"width": 227,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
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
			"seed": 1728293392,
			"version": 2,
			"versionNonce": 2119900440,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xBxeyE9Q"
				},
				{
					"type": "arrow",
					"id": "vwEJHAdF"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b10"
		},
		{
			"id": "xBxeyE9Q",
			"type": "text",
			"x": 883,
			"y": -358.5,
			"width": 203,
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
			"seed": 1361371591,
			"version": 2,
			"versionNonce": 2118312040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ \"30\" > 0 → TypeError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aDSvpKZV",
			"originalText": "⚠ \"30\" > 0 → TypeError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b11"
		},
		{
			"id": "c2XsSbRw",
			"type": "rectangle",
			"x": 669,
			"y": -298.7,
			"width": 439,
			"height": 63,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"isq3n58b"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 340335742,
			"version": 2,
			"versionNonce": 606583320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PUDXs6aS"
				},
				{
					"type": "arrow",
					"id": "74Xz8ZCs"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b12"
		},
		{
			"id": "PUDXs6aS",
			"type": "text",
			"x": 683,
			"y": -289.7,
			"width": 411,
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
				"isq3n58b"
			],
			"frameId": null,
			"roundness": null,
			"seed": 398020369,
			"version": 2,
			"versionNonce": 1591382888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "math.isfinite：12.5、0.0 → True；inf、nan →\nFalse",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "c2XsSbRw",
			"originalText": "math.isfinite：12.5、0.0 → True；inf、nan →\nFalse",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b13"
		},
		{
			"id": "gJFJHTbZ",
			"type": "rectangle",
			"x": 313,
			"y": 151.23,
			"width": 188,
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
			"seed": 320009658,
			"version": 2,
			"versionNonce": 5814040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "p88rpDU9"
				},
				{
					"type": "arrow",
					"id": "x2AHxQ3e"
				},
				{
					"type": "arrow",
					"id": "We4KXPAG"
				},
				{
					"type": "arrow",
					"id": "zYPpFbTG"
				},
				{
					"type": "arrow",
					"id": "ts2hKbrx"
				},
				{
					"type": "arrow",
					"id": "WKXdxXGb"
				},
				{
					"type": "arrow",
					"id": "6CVfd3v2"
				},
				{
					"type": "arrow",
					"id": "sptjBB7g"
				},
				{
					"type": "arrow",
					"id": "ULzNgfGy"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b14"
		},
		{
			"id": "p88rpDU9",
			"type": "text",
			"x": 333,
			"y": 163.23,
			"width": 148,
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
			"seed": 1328140449,
			"version": 2,
			"versionNonce": 1476650600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q2 多個條件",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gJFJHTbZ",
			"originalText": "Q2 多個條件",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b15"
		},
		{
			"id": "tH83KLGC",
			"type": "rectangle",
			"x": 577,
			"y": -172.9,
			"width": 285,
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
				"rcEJ2mcU"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2125072533,
			"version": 2,
			"versionNonce": 123868184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Ym9paRc7"
				},
				{
					"type": "arrow",
					"id": "We4KXPAG"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b16"
		},
		{
			"id": "Ym9paRc7",
			"type": "text",
			"x": 591,
			"y": -163.9,
			"width": 257,
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
				"rcEJ2mcU"
			],
			"frameId": null,
			"roundness": null,
			"seed": 563307770,
			"version": 2,
			"versionNonce": 646633832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "and：全部成立；or：任一成立",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tH83KLGC",
			"originalText": "and：全部成立；or：任一成立",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b17"
		},
		{
			"id": "RdyU62cE",
			"type": "rectangle",
			"x": 577,
			"y": -68.25,
			"width": 320,
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
				"sDnF7vab"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1268169823,
			"version": 2,
			"versionNonce": 2134364440,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vuqsDSaj"
				},
				{
					"type": "arrow",
					"id": "zYPpFbTG"
				},
				{
					"type": "arrow",
					"id": "rDXTt2A2"
				},
				{
					"type": "arrow",
					"id": "s8afKjg9"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b18"
		},
		{
			"id": "vuqsDSaj",
			"type": "text",
			"x": 591,
			"y": -59.25,
			"width": 292,
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
				"sDnF7vab"
			],
			"frameId": null,
			"roundness": null,
			"seed": 847067976,
			"version": 2,
			"versionNonce": 230386792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "拒絕條件：(km < 0) or (min <= 0)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RdyU62cE",
			"originalText": "拒絕條件：(km < 0) or (min <= 0)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b19"
		},
		{
			"id": "K97hpbHw",
			"type": "rectangle",
			"x": 957,
			"y": -118.4,
			"width": 444,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
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
			"seed": 2085189156,
			"version": 2,
			"versionNonce": 1330507288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mZBkU9cJ"
				},
				{
					"type": "arrow",
					"id": "rDXTt2A2"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1A"
		},
		{
			"id": "mZBkU9cJ",
			"type": "text",
			"x": 969,
			"y": -111.4,
			"width": 420,
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
			"seed": 1659176312,
			"version": 2,
			"versionNonce": 123838312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 寫成 and → 兩個都壞才拒絕；要測「單一欄位失敗」\n才抓得到",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "K97hpbHw",
			"originalText": "⚠ 寫成 and → 兩個都壞才拒絕；要測「單一欄位失敗」\n才抓得到",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1B"
		},
		{
			"id": "bXuBNbmk",
			"type": "rectangle",
			"x": 957,
			"y": -31.6,
			"width": 432,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"teiRQvmK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 182314970,
			"version": 2,
			"versionNonce": 1352166168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JtyatGyk"
				},
				{
					"type": "arrow",
					"id": "s8afKjg9"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1C"
		},
		{
			"id": "JtyatGyk",
			"type": "text",
			"x": 969,
			"y": -24.6,
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
			"groupIds": [
				"teiRQvmK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1765757594,
			"version": 2,
			"versionNonce": 1942581864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "d 有限時：not (d >= 0 and m > 0) 和 d < 0 or m <=\n0 抓到同一批（De Morgan）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bXuBNbmk",
			"originalText": "d 有限時：not (d >= 0 and m > 0) 和 d < 0 or m <=\n0 抓到同一批（De Morgan）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1D"
		},
		{
			"id": "EQfeNWBw",
			"type": "rectangle",
			"x": 577,
			"y": 55.2,
			"width": 446,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"5VLxiTwg"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 478965594,
			"version": 2,
			"versionNonce": 495667224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "y54TH8Xu"
				},
				{
					"type": "arrow",
					"id": "ts2hKbrx"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "y54TH8Xu",
			"type": "text",
			"x": 591,
			"y": 64.2,
			"width": 418,
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
				"5VLxiTwg"
			],
			"frameId": null,
			"roundness": null,
			"seed": 876134110,
			"version": 2,
			"versionNonce": 1237247336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "not 是邏輯否定；& | ~ 是位元運算（不要用 ~ 當\nnot）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EQfeNWBw",
			"originalText": "not 是邏輯否定；& | ~ 是位元運算（不要用 ~ 當\nnot）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "kXSb4EYX",
			"type": "rectangle",
			"x": 577,
			"y": 186.75,
			"width": 236,
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
			"seed": 605647287,
			"version": 2,
			"versionNonce": 1645905176,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2exS3nQg"
				},
				{
					"type": "arrow",
					"id": "WKXdxXGb"
				},
				{
					"type": "arrow",
					"id": "fcNYLRVL"
				},
				{
					"type": "arrow",
					"id": "GWPSZAEJ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "2exS3nQg",
			"type": "text",
			"x": 591,
			"y": 195.75,
			"width": 208,
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
			"seed": 486892923,
			"version": 2,
			"versionNonce": 1183709288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "優先序：not > and > or",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kXSb4EYX",
			"originalText": "優先序：not > and > or",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "zQSZ2fib",
			"type": "rectangle",
			"x": 873,
			"y": 151,
			"width": 445,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"6B6trsWw"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1523703557,
			"version": 2,
			"versionNonce": 733618712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RVG3Tz9e"
				},
				{
					"type": "arrow",
					"id": "fcNYLRVL"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "RVG3Tz9e",
			"type": "text",
			"x": 885,
			"y": 158,
			"width": 421,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"6B6trsWw"
			],
			"frameId": null,
			"roundness": null,
			"seed": 915954854,
			"version": 2,
			"versionNonce": 503491432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "valid and a or b ≠ valid and (a or b)（valid = False、\n60 分：前者 True、後者 False）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zQSZ2fib",
			"originalText": "valid and a or b ≠ valid and (a or b)（valid = False、\n60 分：前者 True、後者 False）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "NGwdgqNK",
			"type": "rectangle",
			"x": 873,
			"y": 219,
			"width": 315,
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
			"seed": 1954412174,
			"version": 2,
			"versionNonce": 962469656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uK6A4HUL"
				},
				{
					"type": "arrow",
					"id": "GWPSZAEJ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "uK6A4HUL",
			"type": "text",
			"x": 885,
			"y": 226,
			"width": 291,
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
			"seed": 680070256,
			"version": 2,
			"versionNonce": 711523944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "0 < t <= 30 ≡ (t > 0) and (t <= 30)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NGwdgqNK",
			"originalText": "0 < t <= 30 ≡ (t > 0) and (t <= 30)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "itPh3Ns9",
			"type": "rectangle",
			"x": 577,
			"y": 287.75,
			"width": 180,
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
				"BZ6d2NCs"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1671696590,
			"version": 2,
			"versionNonce": 1266318360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Y46mpxjZ"
				},
				{
					"type": "arrow",
					"id": "6CVfd3v2"
				},
				{
					"type": "arrow",
					"id": "yqLsRSLh"
				},
				{
					"type": "arrow",
					"id": "ZwptvRuv"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "Y46mpxjZ",
			"type": "text",
			"x": 628.5,
			"y": 296.75,
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
				"BZ6d2NCs"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1926347856,
			"version": 2,
			"versionNonce": 478998888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "短路求值",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "itPh3Ns9",
			"originalText": "短路求值",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "i6E32ZNs",
			"type": "rectangle",
			"x": 817,
			"y": 267,
			"width": 336,
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
			"seed": 975699154,
			"version": 2,
			"versionNonce": 1946368280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qp3N87Jt"
				},
				{
					"type": "arrow",
					"id": "yqLsRSLh"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "qp3N87Jt",
			"type": "text",
			"x": 829,
			"y": 274,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1800714399,
			"version": 2,
			"versionNonce": 733643880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "and 左邊 False → 不算右邊（保護除法）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "i6E32ZNs",
			"originalText": "and 左邊 False → 不算右邊（保護除法）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "7VnFvi3u",
			"type": "rectangle",
			"x": 817,
			"y": 315,
			"width": 222,
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
			"seed": 1895661476,
			"version": 2,
			"versionNonce": 1718375960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tvFkejgX"
				},
				{
					"type": "arrow",
					"id": "ZwptvRuv"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "tvFkejgX",
			"type": "text",
			"x": 829,
			"y": 322,
			"width": 198,
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
			"seed": 273466375,
			"version": 2,
			"versionNonce": 1170061160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "or 左邊 True → 不算右邊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7VnFvi3u",
			"originalText": "or 左邊 True → 不算右邊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "r3Fahhm6",
			"type": "rectangle",
			"x": 577,
			"y": 381.8,
			"width": 459,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"69Fg6m39"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1617459236,
			"version": 2,
			"versionNonce": 1202311960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7QCbMRsr"
				},
				{
					"type": "arrow",
					"id": "sptjBB7g"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "7QCbMRsr",
			"type": "text",
			"x": 591,
			"y": 390.8,
			"width": 431,
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
				"69Fg6m39"
			],
			"frameId": null,
			"roundness": null,
			"seed": 357297648,
			"version": 2,
			"versionNonce": 1055033960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ duration_min == 30 or 60 → 60（truthy），\n不是比較",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "r3Fahhm6",
			"originalText": "⚠ duration_min == 30 or 60 → 60（truthy），\n不是比較",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "L5q5e8UR",
			"type": "rectangle",
			"x": 577,
			"y": 477.6,
			"width": 448,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"DzWsAEdH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1528769081,
			"version": 2,
			"versionNonce": 2117054488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ATq8ZB5V"
				},
				{
					"type": "arrow",
					"id": "ULzNgfGy"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "ATq8ZB5V",
			"type": "text",
			"x": 591,
			"y": 486.6,
			"width": 420,
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
				"DzWsAEdH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1127622194,
			"version": 2,
			"versionNonce": 32832872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab 1：一般／零時間／空標籤／無窮距離／零距離\n→ True、False、False、False、True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "L5q5e8UR",
			"originalText": "Lab 1：一般／零時間／空標籤／無窮距離／零距離\n→ True、False、False、False、True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "yJQ8FuvY",
			"type": "rectangle",
			"x": 313,
			"y": 802.97,
			"width": 334,
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
			"seed": 1678114730,
			"version": 2,
			"versionNonce": 32632088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QrTFtLKb"
				},
				{
					"type": "arrow",
					"id": "5JQwzTuD"
				},
				{
					"type": "arrow",
					"id": "RFNqir4v"
				},
				{
					"type": "arrow",
					"id": "j4dHRM8z"
				},
				{
					"type": "arrow",
					"id": "4zzPYQ5w"
				},
				{
					"type": "arrow",
					"id": "Dih487av"
				},
				{
					"type": "arrow",
					"id": "4G46n7Vf"
				},
				{
					"type": "arrow",
					"id": "WKJFcp67"
				},
				{
					"type": "arrow",
					"id": "xbPFr5TV"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "QrTFtLKb",
			"type": "text",
			"x": 333,
			"y": 814.97,
			"width": 294,
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
			"seed": 1511784811,
			"version": 2,
			"versionNonce": 1078005864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q3 條件選擇要執行的程式",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yJQ8FuvY",
			"originalText": "Q3 條件選擇要執行的程式",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "TTefqhXn",
			"type": "rectangle",
			"x": 723,
			"y": 584.6,
			"width": 438,
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
			"seed": 32300525,
			"version": 2,
			"versionNonce": 744786456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QkfUPJ2J"
				},
				{
					"type": "arrow",
					"id": "RFNqir4v"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "QkfUPJ2J",
			"type": "text",
			"x": 737,
			"y": 593.6,
			"width": 410,
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
			"seed": 458943683,
			"version": 2,
			"versionNonce": 563266408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "冒號開始區塊；縮排決定歸屬（四個空格是慣例）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TTefqhXn",
			"originalText": "冒號開始區塊；縮排決定歸屬（四個空格是慣例）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "xrJa2zMV",
			"type": "rectangle",
			"x": 723,
			"y": 639.1,
			"width": 227,
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
			"seed": 196753967,
			"version": 2,
			"versionNonce": 142313240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yCrPdSNa"
				},
				{
					"type": "arrow",
					"id": "j4dHRM8z"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "yCrPdSNa",
			"type": "text",
			"x": 737,
			"y": 648.1,
			"width": 199,
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
			"seed": 2081271458,
			"version": 2,
			"versionNonce": 1949701736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "if／else：恰好走一條路",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xrJa2zMV",
			"originalText": "if／else：恰好走一條路",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "vNAiBVLG",
			"type": "rectangle",
			"x": 723,
			"y": 693.6,
			"width": 258,
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
			"seed": 1367333503,
			"version": 2,
			"versionNonce": 581624856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gajdmmNi"
				},
				{
					"type": "arrow",
					"id": "4zzPYQ5w"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "gajdmmNi",
			"type": "text",
			"x": 737,
			"y": 702.6,
			"width": 230,
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
			"seed": 420822370,
			"version": 2,
			"versionNonce": 1559693672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "印出 False 不會阻止下一行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vNAiBVLG",
			"originalText": "印出 False 不會阻止下一行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "faAaj9fC",
			"type": "rectangle",
			"x": 723,
			"y": 748.1,
			"width": 440,
			"height": 63,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffc9c9",
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
			"seed": 829297095,
			"version": 2,
			"versionNonce": 1491509528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BPKvS4Fh"
				},
				{
					"type": "arrow",
					"id": "Dih487av"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "BPKvS4Fh",
			"type": "text",
			"x": 737,
			"y": 757.1,
			"width": 412,
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
			"seed": 1523390828,
			"version": 2,
			"versionNonce": 119643240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 警告不是保護：除法在 if 外 → 印 Error 後仍\nZeroDivisionError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "faAaj9fC",
			"originalText": "⚠ 警告不是保護：除法在 if 外 → 印 Error 後仍\nZeroDivisionError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "YeCUaPvj",
			"type": "rectangle",
			"x": 723,
			"y": 825.1,
			"width": 272,
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
			"seed": 907144034,
			"version": 2,
			"versionNonce": 715308568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UYLMNZBK"
				},
				{
					"type": "arrow",
					"id": "4G46n7Vf"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "UYLMNZBK",
			"type": "text",
			"x": 737,
			"y": 834.1,
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
			"seed": 1445044020,
			"version": 2,
			"versionNonce": 1417793384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "合法縮排也可能是錯的演算法",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YeCUaPvj",
			"originalText": "合法縮排也可能是錯的演算法",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "KNuYdWVm",
			"type": "rectangle",
			"x": 723,
			"y": 924.35,
			"width": 105,
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
			"seed": 287783668,
			"version": 2,
			"versionNonce": 148060952,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pECpZkni"
				},
				{
					"type": "arrow",
					"id": "WKJFcp67"
				},
				{
					"type": "arrow",
					"id": "PTRiD5wr"
				},
				{
					"type": "arrow",
					"id": "EiSKRgVQ"
				},
				{
					"type": "arrow",
					"id": "asdWc6Kh"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "pECpZkni",
			"type": "text",
			"x": 737,
			"y": 933.35,
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
			"seed": 1260010485,
			"version": 2,
			"versionNonce": 224633448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "三種失敗",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KNuYdWVm",
			"originalText": "三種失敗",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "X28yRBbN",
			"type": "rectangle",
			"x": 888,
			"y": 879.6,
			"width": 334,
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
			"seed": 1859171739,
			"version": 2,
			"versionNonce": 636229656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8berH6jw"
				},
				{
					"type": "arrow",
					"id": "PTRiD5wr"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "8berH6jw",
			"type": "text",
			"x": 900,
			"y": 886.6,
			"width": 310,
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
			"seed": 937437663,
			"version": 2,
			"versionNonce": 278074728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Syntax：if duration_min > 0（缺冒號）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "X28yRBbN",
			"originalText": "Syntax：if duration_min > 0（缺冒號）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "jMt5wc8P",
			"type": "rectangle",
			"x": 888,
			"y": 927.6,
			"width": 172,
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
			"seed": 1774542714,
			"version": 2,
			"versionNonce": 1172395288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZSxJDWkf"
				},
				{
					"type": "arrow",
					"id": "EiSKRgVQ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "ZSxJDWkf",
			"type": "text",
			"x": 900,
			"y": 934.6,
			"width": 148,
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
			"seed": 1879035827,
			"version": 2,
			"versionNonce": 56371304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Runtime：\"30\" > 0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jMt5wc8P",
			"originalText": "Runtime：\"30\" > 0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "QjZugZeR",
			"type": "rectangle",
			"x": 888,
			"y": 975.6,
			"width": 309,
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
			"seed": 1329494444,
			"version": 2,
			"versionNonce": 237433368,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fCd9UdrF"
				},
				{
					"type": "arrow",
					"id": "asdWc6Kh"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "fCd9UdrF",
			"type": "text",
			"x": 900,
			"y": 982.6,
			"width": 285,
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
			"seed": 133948595,
			"version": 2,
			"versionNonce": 25877352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Logic：duration_min >= 0（允許零）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QjZugZeR",
			"originalText": "Logic：duration_min >= 0（允許零）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "ghyN8WvG",
			"type": "rectangle",
			"x": 723,
			"y": 1023.6,
			"width": 435,
			"height": 63,
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
			"seed": 59634132,
			"version": 2,
			"versionNonce": 1437658904,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "F6VTeSrN"
				},
				{
					"type": "arrow",
					"id": "xbPFr5TV"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "F6VTeSrN",
			"type": "text",
			"x": 737,
			"y": 1032.6,
			"width": 407,
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
			"seed": 1401498974,
			"version": 2,
			"versionNonce": 1298869864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab 2：(15, 30) → 30.00 km/h；(15, 0)、(15,\n−1) → 只印錯誤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ghyN8WvG",
			"originalText": "Lab 2：(15, 30) → 30.00 km/h；(15, 0)、(15,\n−1) → 只印錯誤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "sUVzHpNC",
			"type": "rectangle",
			"x": -547,
			"y": -946.55,
			"width": 234,
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
			"seed": 702253005,
			"version": 2,
			"versionNonce": 1962101784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "s5pPCvM6"
				},
				{
					"type": "arrow",
					"id": "XCRuDVUb"
				},
				{
					"type": "arrow",
					"id": "MPBM4Eeq"
				},
				{
					"type": "arrow",
					"id": "UqKDzuBW"
				},
				{
					"type": "arrow",
					"id": "PUE8VSDA"
				},
				{
					"type": "arrow",
					"id": "tqVgmUsz"
				},
				{
					"type": "arrow",
					"id": "Nvx4NzMd"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "s5pPCvM6",
			"type": "text",
			"x": -527,
			"y": -934.55,
			"width": 194,
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
			"seed": 105903775,
			"version": 2,
			"versionNonce": 2143887720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q4 超過兩種結果",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sUVzHpNC",
			"originalText": "Q4 超過兩種結果",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "hb5AVM6T",
			"type": "rectangle",
			"x": -970,
			"y": -1078.85,
			"width": 347,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"xChKyEff"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1706449526,
			"version": 2,
			"versionNonce": 367135000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KudHZCy3"
				},
				{
					"type": "arrow",
					"id": "MPBM4Eeq"
				},
				{
					"type": "arrow",
					"id": "qypdVUst"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "KudHZCy3",
			"type": "text",
			"x": -956,
			"y": -1069.85,
			"width": 319,
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
				"xChKyEff"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2117371234,
			"version": 2,
			"versionNonce": 938521704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "if／elif／else：第一個為真的分支勝出",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hb5AVM6T",
			"originalText": "if／elif／else：第一個為真的分支勝出",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "VgJfv6dK",
			"type": "rectangle",
			"x": -1161,
			"y": -1075.6,
			"width": 131,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
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
			"seed": 500728963,
			"version": 2,
			"versionNonce": 66135576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3wfjydES"
				},
				{
					"type": "arrow",
					"id": "qypdVUst"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "3wfjydES",
			"type": "text",
			"x": -1149,
			"y": -1068.6,
			"width": 107,
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
			"seed": 1533659526,
			"version": 2,
			"versionNonce": 1269688168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "45 → Medium",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VgJfv6dK",
			"originalText": "45 → Medium",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "bJHt8yV7",
			"type": "rectangle",
			"x": -1067,
			"y": -1005.55,
			"width": 444,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"TihHH8wn"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1300182866,
			"version": 2,
			"versionNonce": 2081727256,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XtPNnYVM"
				},
				{
					"type": "arrow",
					"id": "UqKDzuBW"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "XtPNnYVM",
			"type": "text",
			"x": -1053,
			"y": -996.55,
			"width": 416,
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
				"TihHH8wn"
			],
			"frameId": null,
			"roundness": null,
			"seed": 815892880,
			"version": 2,
			"versionNonce": 2001517160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 兩個獨立 if 都會執行：20 → Short＋Medium",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bJHt8yV7",
			"originalText": "⚠ 兩個獨立 if 都會執行：20 → Short＋Medium",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "iDg7VeL5",
			"type": "rectangle",
			"x": -1085,
			"y": -951.05,
			"width": 462,
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
			"seed": 1856169784,
			"version": 2,
			"versionNonce": 2092990488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dxZ9ZP6v"
				},
				{
					"type": "arrow",
					"id": "PUE8VSDA"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "dxZ9ZP6v",
			"type": "text",
			"x": -1071,
			"y": -942.05,
			"width": 434,
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
			"seed": 1234907816,
			"version": 2,
			"versionNonce": 228142440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "巢狀：外層先驗證，內層才分類（0 不能變 Short）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iDg7VeL5",
			"originalText": "巢狀：外層先驗證，內層才分類（0 不能變 Short）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "aKx73SvN",
			"type": "rectangle",
			"x": -1082,
			"y": -877.75,
			"width": 459,
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
				"hEwwpMMb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 747462839,
			"version": 2,
			"versionNonce": 367574296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HXtYwstk"
				},
				{
					"type": "arrow",
					"id": "tqVgmUsz"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "HXtYwstk",
			"type": "text",
			"x": -1068,
			"y": -868.75,
			"width": 431,
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
				"hEwwpMMb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1099700366,
			"version": 2,
			"versionNonce": 668942440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "邊界：1、29、30 → Short；31、60 → Medium；\n61 → Long",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aKx73SvN",
			"originalText": "邊界：1、29、30 → Short；31、60 → Medium；\n61 → Long",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "WQMD5bQC",
			"type": "rectangle",
			"x": -1006,
			"y": -800.75,
			"width": 383,
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
			"seed": 1098512513,
			"version": 2,
			"versionNonce": 956389912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "j3yiZimh"
				},
				{
					"type": "arrow",
					"id": "Nvx4NzMd"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "j3yiZimh",
			"type": "text",
			"x": -992,
			"y": -791.75,
			"width": 355,
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
			"seed": 365312861,
			"version": 2,
			"versionNonce": 1441461096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "用原始整數分鐘分類，不用格式化後的字串",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WQMD5bQC",
			"originalText": "用原始整數分鐘分類，不用格式化後的字串",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "sLGLVj72",
			"type": "rectangle",
			"x": -597,
			"y": -491.83,
			"width": 284,
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
			"seed": 1558614860,
			"version": 2,
			"versionNonce": 150886168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "C8XNjJrw"
				},
				{
					"type": "arrow",
					"id": "B9MsP7sT"
				},
				{
					"type": "arrow",
					"id": "JwJUf6DR"
				},
				{
					"type": "arrow",
					"id": "iALFdKtg"
				},
				{
					"type": "arrow",
					"id": "CKQMNrCP"
				},
				{
					"type": "arrow",
					"id": "d6rj2wDQ"
				},
				{
					"type": "arrow",
					"id": "GwwaXJaP"
				},
				{
					"type": "arrow",
					"id": "6BVz5VF6"
				},
				{
					"type": "arrow",
					"id": "JWPwMHeu"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "C8XNjJrw",
			"type": "text",
			"x": -577,
			"y": -479.83,
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
			"seed": 1556644402,
			"version": 2,
			"versionNonce": 1309165160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q5 條件順序也是規格",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sLGLVj72",
			"originalText": "Q5 條件順序也是規格",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "uFfvXEDY",
			"type": "rectangle",
			"x": -1115,
			"y": -697.45,
			"width": 442,
			"height": 63,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"xYJLCRtF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1795215082,
			"version": 2,
			"versionNonce": 710128664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZYP5hkiP"
				},
				{
					"type": "arrow",
					"id": "JwJUf6DR"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "ZYP5hkiP",
			"type": "text",
			"x": -1101,
			"y": -688.45,
			"width": 414,
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
				"xYJLCRtF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 277645180,
			"version": 2,
			"versionNonce": 486750568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 先判 <= 60 再判 <= 30 → Short 永遠到不了\n（20 → Medium）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uFfvXEDY",
			"originalText": "⚠ 先判 <= 60 再判 <= 30 → Short 永遠到不了\n（20 → Medium）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "B4FdktrU",
			"type": "rectangle",
			"x": -1135,
			"y": -620.45,
			"width": 462,
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
			"seed": 1974332258,
			"version": 2,
			"versionNonce": 318075160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2tBuSyMt"
				},
				{
					"type": "arrow",
					"id": "iALFdKtg"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "2tBuSyMt",
			"type": "text",
			"x": -1121,
			"y": -611.45,
			"width": 434,
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
			"seed": 1112336927,
			"version": 2,
			"versionNonce": 1445448808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Path reasoning：走到 elif t <= 60 時已知 t > 30",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "B4FdktrU",
			"originalText": "Path reasoning：走到 elif t <= 60 時已知 t > 30",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "wb32mCZv",
			"type": "rectangle",
			"x": -871,
			"y": -545.2,
			"width": 198,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"emXbdmYC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1653744451,
			"version": 2,
			"versionNonce": 1515687448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RAEdgxTS"
				},
				{
					"type": "arrow",
					"id": "CKQMNrCP"
				},
				{
					"type": "arrow",
					"id": "chY84hpT"
				},
				{
					"type": "arrow",
					"id": "HSPhwQqt"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "RAEdgxTS",
			"type": "text",
			"x": -857,
			"y": -536.2,
			"width": 170,
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
				"emXbdmYC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1567435465,
			"version": 2,
			"versionNonce": 1128398696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "錯誤優先序（v0.3）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wb32mCZv",
			"originalText": "錯誤優先序（v0.3）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "8uThtVZj",
			"type": "rectangle",
			"x": -1358,
			"y": -565.95,
			"width": 427,
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
			"seed": 2063915328,
			"version": 2,
			"versionNonce": 158206744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dzFdsQZW"
				},
				{
					"type": "arrow",
					"id": "chY84hpT"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "dzFdsQZW",
			"type": "text",
			"x": -1346,
			"y": -558.95,
			"width": 403,
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
			"seed": 1801102829,
			"version": 2,
			"versionNonce": 345887336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "1 空標籤 → 2 非有限距離 → 3 負距離 → 4 非正時間",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8uThtVZj",
			"originalText": "1 空標籤 → 2 非有限距離 → 3 負距離 → 4 非正時間",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "THh3Epc3",
			"type": "rectangle",
			"x": -1267,
			"y": -517.95,
			"width": 336,
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
			"seed": 998768566,
			"version": 2,
			"versionNonce": 1789716504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "W7e8p2u9"
				},
				{
					"type": "arrow",
					"id": "HSPhwQqt"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "W7e8p2u9",
			"type": "text",
			"x": -1255,
			"y": -510.95,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 942643791,
			"version": 2,
			"versionNonce": 285689192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "空標籤＋負距離＋零時間 → 只印標籤錯誤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "THh3Epc3",
			"originalText": "空標籤＋負距離＋零時間 → 只印標籤錯誤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "jCGNkjwQ",
			"type": "rectangle",
			"x": -1076,
			"y": -469.95,
			"width": 403,
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
			"seed": 1061991209,
			"version": 2,
			"versionNonce": 1510483224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2KiXRfY9"
				},
				{
					"type": "arrow",
					"id": "d6rj2wDQ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "2KiXRfY9",
			"type": "text",
			"x": -1062,
			"y": -460.95,
			"width": 375,
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
			"seed": 476472872,
			"version": 2,
			"versionNonce": 1170888808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "「只報第一個錯」vs「報全部錯」是不同需求",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jCGNkjwQ",
			"originalText": "「只報第一個錯」vs「報全部錯」是不同需求",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "rxqYyc44",
			"type": "rectangle",
			"x": -926,
			"y": -415.45,
			"width": 253,
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
			"seed": 1820939702,
			"version": 2,
			"versionNonce": 351519256,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Sadh8Cyj"
				},
				{
					"type": "arrow",
					"id": "GwwaXJaP"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "Sadh8Cyj",
			"type": "text",
			"x": -912,
			"y": -406.45,
			"width": 225,
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
			"seed": 1835760922,
			"version": 2,
			"versionNonce": 917703528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "拒絕案例不能出現任何報告",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rxqYyc44",
			"originalText": "拒絕案例不能出現任何報告",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "VTjibWuM",
			"type": "rectangle",
			"x": -1096,
			"y": -360.95,
			"width": 423,
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
			"seed": 329276254,
			"version": 2,
			"versionNonce": 174309144,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hF8KLynA"
				},
				{
					"type": "arrow",
					"id": "6BVz5VF6"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "hF8KLynA",
			"type": "text",
			"x": -1082,
			"y": -351.95,
			"width": 395,
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
			"seed": 1600304452,
			"version": 2,
			"versionNonce": 235757160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "結果要完整且不重疊：錯誤／Short／Medium／\nLong",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VTjibWuM",
			"originalText": "結果要完整且不重疊：錯誤／Short／Medium／\nLong",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "pLVGbfsj",
			"type": "rectangle",
			"x": -1073,
			"y": -283.95,
			"width": 400,
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
			"seed": 1913647350,
			"version": 2,
			"versionNonce": 718019608,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HYv7LRip"
				},
				{
					"type": "arrow",
					"id": "JWPwMHeu"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "HYv7LRip",
			"type": "text",
			"x": -1059,
			"y": -274.95,
			"width": 372,
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
			"seed": 801177397,
			"version": 2,
			"versionNonce": 1285902696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "\" \"（只有空白）仍算非空；Deck 5 才改政策",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pLVGbfsj",
			"originalText": "\" \"（只有空白）仍算非空；Deck 5 才改政策",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "negL5YYY",
			"type": "rectangle",
			"x": -603,
			"y": -96.33,
			"width": 290,
			"height": 54,
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
			"seed": 594010835,
			"version": 2,
			"versionNonce": 941676824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BuzLDfFZ"
				},
				{
					"type": "arrow",
					"id": "erjiCHw5"
				},
				{
					"type": "arrow",
					"id": "NWY43GNL"
				},
				{
					"type": "arrow",
					"id": "dZL83q4w"
				},
				{
					"type": "arrow",
					"id": "brGn2pzv"
				},
				{
					"type": "arrow",
					"id": "8P6RQgVM"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "BuzLDfFZ",
			"type": "text",
			"x": -583,
			"y": -84.33,
			"width": 250,
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
			"seed": 115544079,
			"version": 2,
			"versionNonce": 2043077736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "電腦基礎：比較與跳躍",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "negL5YYY",
			"originalText": "電腦基礎：比較與跳躍",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "3UyWXVEZ",
			"type": "rectangle",
			"x": -1098,
			"y": -199.45,
			"width": 419,
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
			"seed": 1116993735,
			"version": 2,
			"versionNonce": 366343704,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BZh4N4yX"
				},
				{
					"type": "arrow",
					"id": "NWY43GNL"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "BZh4N4yX",
			"type": "text",
			"x": -1084,
			"y": -190.45,
			"width": 391,
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
			"seed": 250551651,
			"version": 2,
			"versionNonce": 1396578152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "LOAD 放值 → CMP 比較 → JLT 小於就跳 →\nOUT 印 → JMP 無條件跳 → HALT",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3UyWXVEZ",
			"originalText": "LOAD 放值 → CMP 比較 → JLT 小於就跳 →\nOUT 印 → JMP 無條件跳 → HALT",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "GV7FQYjm",
			"type": "rectangle",
			"x": -1132,
			"y": -122.45,
			"width": 453,
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
			"seed": 903556874,
			"version": 2,
			"versionNonce": 417297176,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JBWLZeju"
				},
				{
					"type": "arrow",
					"id": "dZL83q4w"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "JBWLZeju",
			"type": "text",
			"x": -1118,
			"y": -113.45,
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
			"seed": 514894450,
			"version": 2,
			"versionNonce": 2102848104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "score 59 → 跳到 fail；60 → pass 後 JMP done",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GV7FQYjm",
			"originalText": "score 59 → 跳到 fail；60 → pass 後 JMP done",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "KT4Viu2d",
			"type": "rectangle",
			"x": -1126,
			"y": -67.95,
			"width": 447,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffc9c9",
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
			"seed": 572941005,
			"version": 2,
			"versionNonce": 1471238168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FiZNquci"
				},
				{
					"type": "arrow",
					"id": "brGn2pzv"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2W"
		},
		{
			"id": "FiZNquci",
			"type": "text",
			"x": -1112,
			"y": -58.95,
			"width": 419,
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
			"seed": 1802075014,
			"version": 2,
			"versionNonce": 853368168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 刪掉 JMP done → pass、fail 都印（像兩個獨\n立 if）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KT4Viu2d",
			"originalText": "⚠ 刪掉 JMP done → pass、fail 都印（像兩個獨\n立 if）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "7edf5FNs",
			"type": "rectangle",
			"x": -932,
			"y": 9.05,
			"width": 253,
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
			"seed": 1230058197,
			"version": 2,
			"versionNonce": 2050985240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "amH9cDZu"
				},
				{
					"type": "arrow",
					"id": "8P6RQgVM"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "amH9cDZu",
			"type": "text",
			"x": -918,
			"y": 18.05,
			"width": 225,
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
			"seed": 1804652977,
			"version": 2,
			"versionNonce": 1964863592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "下一個指令不一定是下一行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7edf5FNs",
			"originalText": "下一個指令不一定是下一行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "aw5SCrXc",
			"type": "rectangle",
			"x": -613,
			"y": 393.6,
			"width": 300,
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
			"seed": 379511927,
			"version": 2,
			"versionNonce": 167651864,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EpmHH8Kh"
				},
				{
					"type": "arrow",
					"id": "88TRcwrp"
				},
				{
					"type": "arrow",
					"id": "2XUrZisP"
				},
				{
					"type": "arrow",
					"id": "9r2YB3Jd"
				},
				{
					"type": "arrow",
					"id": "ac5McGp5"
				},
				{
					"type": "arrow",
					"id": "G42jdAKA"
				},
				{
					"type": "arrow",
					"id": "Qf8z93A2"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "EpmHH8Kh",
			"type": "text",
			"x": -593,
			"y": 405.6,
			"width": 260,
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
			"seed": 449560870,
			"version": 2,
			"versionNonce": 1004741480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q6 測試決策、審查 AI",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aw5SCrXc",
			"originalText": "Q6 測試決策、審查 AI",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
		},
		{
			"id": "KcN8BHHC",
			"type": "rectangle",
			"x": -794,
			"y": 167.1,
			"width": 105,
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
			"seed": 992665235,
			"version": 2,
			"versionNonce": 1105274648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "antPFiZX"
				},
				{
					"type": "arrow",
					"id": "2XUrZisP"
				},
				{
					"type": "arrow",
					"id": "shh2Ua39"
				},
				{
					"type": "arrow",
					"id": "Jgv4J4kM"
				},
				{
					"type": "arrow",
					"id": "pberap7r"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2c"
		},
		{
			"id": "antPFiZX",
			"type": "text",
			"x": -780,
			"y": 176.1,
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
			"seed": 1688067300,
			"version": 2,
			"versionNonce": 628782696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "三類測試",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KcN8BHHC",
			"originalText": "三類測試",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2d"
		},
		{
			"id": "Xa5gmUCN",
			"type": "rectangle",
			"x": -1132,
			"y": 112.35,
			"width": 278,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"Z98A76Hp"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 217584729,
			"version": 2,
			"versionNonce": 1583121432,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Dcx6UwxB"
				},
				{
					"type": "arrow",
					"id": "shh2Ua39"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2e"
		},
		{
			"id": "Dcx6UwxB",
			"type": "text",
			"x": -1120,
			"y": 119.35,
			"width": 254,
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
				"Z98A76Hp"
			],
			"frameId": null,
			"roundness": null,
			"seed": 273943035,
			"version": 2,
			"versionNonce": 649029992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "邊界：29／30／31、59／60／61",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Xa5gmUCN",
			"originalText": "邊界：29／30／31、59／60／61",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2f"
		},
		{
			"id": "xsQ86cbd",
			"type": "rectangle",
			"x": -1273,
			"y": 160.35,
			"width": 419,
			"height": 54,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 1133905015,
			"version": 2,
			"versionNonce": 1835286808,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CnpYX4kH"
				},
				{
					"type": "arrow",
					"id": "Jgv4J4kM"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2g"
		},
		{
			"id": "CnpYX4kH",
			"type": "text",
			"x": -1261,
			"y": 167.35,
			"width": 395,
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
			"seed": 371505400,
			"version": 2,
			"versionNonce": 986578024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "單一欄位失敗：空標籤、負距離、零或負時間、NaN／\ninf",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xsQ86cbd",
			"originalText": "單一欄位失敗：空標籤、負距離、零或負時間、NaN／\ninf",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2h"
		},
		{
			"id": "2fdPc5MH",
			"type": "rectangle",
			"x": -1194,
			"y": 228.35,
			"width": 340,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 1761131916,
			"version": 2,
			"versionNonce": 510418456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Y4yjqdii"
				},
				{
					"type": "arrow",
					"id": "pberap7r"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2i"
		},
		{
			"id": "Y4yjqdii",
			"type": "text",
			"x": -1182,
			"y": 235.35,
			"width": 316,
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
			"seed": 1336113972,
			"version": 2,
			"versionNonce": 329396072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "互動：兩個錯同時出現、零距離＋有效時間",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2fdPc5MH",
			"originalText": "互動：兩個錯同時出現、零距離＋有效時間",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2j"
		},
		{
			"id": "CgxUfdiT",
			"type": "rectangle",
			"x": -889,
			"y": 345.1,
			"width": 200,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#f8f0fc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"4w8BDqTD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2049874552,
			"version": 2,
			"versionNonce": 308861720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MK365ugE"
				},
				{
					"type": "arrow",
					"id": "9r2YB3Jd"
				},
				{
					"type": "arrow",
					"id": "bJ4gC3v5"
				},
				{
					"type": "arrow",
					"id": "Z8f7s4ch"
				},
				{
					"type": "arrow",
					"id": "nnZfNCKA"
				},
				{
					"type": "arrow",
					"id": "wEeTSBRk"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2k"
		},
		{
			"id": "MK365ugE",
			"type": "text",
			"x": -875,
			"y": 354.1,
			"width": 172,
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
				"4w8BDqTD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 441847098,
			"version": 2,
			"versionNonce": 1232601704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "故意錯誤 candidate",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CgxUfdiT",
			"originalText": "故意錯誤 candidate",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2l"
		},
		{
			"id": "digDASyT",
			"type": "rectangle",
			"x": -1263,
			"y": 276.35,
			"width": 314,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 217077141,
			"version": 2,
			"versionNonce": 734902296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "98RWaZub"
				},
				{
					"type": "arrow",
					"id": "bJ4gC3v5"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2m"
		},
		{
			"id": "98RWaZub",
			"type": "text",
			"x": -1251,
			"y": 283.35,
			"width": 290,
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
			"seed": 493594685,
			"version": 2,
			"versionNonce": 186348904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "1 km／0 min → 除零（and 防護太弱）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "digDASyT",
			"originalText": "1 km／0 min → 除零（and 防護太弱）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2n"
		},
		{
			"id": "D3dgSJa2",
			"type": "rectangle",
			"x": -1164,
			"y": 324.35,
			"width": 215,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 344962266,
			"version": 2,
			"versionNonce": 1586427160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "v5SpFW3P"
				},
				{
					"type": "arrow",
					"id": "Z8f7s4ch"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2o"
		},
		{
			"id": "v5SpFW3P",
			"type": "text",
			"x": -1152,
			"y": 331.35,
			"width": 191,
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
			"seed": 313986939,
			"version": 2,
			"versionNonce": 1306036328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "−1 km／30 min → 被接受",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "D3dgSJa2",
			"originalText": "−1 km／30 min → 被接受",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2p"
		},
		{
			"id": "9AvCXfpc",
			"type": "rectangle",
			"x": -1267,
			"y": 372.35,
			"width": 318,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 501581908,
			"version": 2,
			"versionNonce": 2134552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EYpjnRPz"
				},
				{
					"type": "arrow",
					"id": "nnZfNCKA"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2q"
		},
		{
			"id": "EYpjnRPz",
			"type": "text",
			"x": -1255,
			"y": 379.35,
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
			"seed": 411018913,
			"version": 2,
			"versionNonce": 2105228136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "5 km／30 min → Medium（應 Short）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9AvCXfpc",
			"originalText": "5 km／30 min → Medium（應 Short）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2r"
		},
		{
			"id": "zvVdube2",
			"type": "rectangle",
			"x": -1261,
			"y": 420.35,
			"width": 312,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 1418596453,
			"version": 2,
			"versionNonce": 393645848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yfmy5pSR"
				},
				{
					"type": "arrow",
					"id": "wEeTSBRk"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2s"
		},
		{
			"id": "yfmy5pSR",
			"type": "text",
			"x": -1249,
			"y": 427.35,
			"width": 288,
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
			"seed": 628165580,
			"version": 2,
			"versionNonce": 743411304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "最小修補：and → or；< 30 → <= 30",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zvVdube2",
			"originalText": "最小修補：and → or；< 30 → <= 30",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2t"
		},
		{
			"id": "jzgfvXKA",
			"type": "rectangle",
			"x": -1150,
			"y": 468.35,
			"width": 461,
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
			"seed": 721845091,
			"version": 2,
			"versionNonce": 755297304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Yy4cjxjq"
				},
				{
					"type": "arrow",
					"id": "ac5McGp5"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2u"
		},
		{
			"id": "Yy4cjxjq",
			"type": "text",
			"x": -1136,
			"y": 477.35,
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
			"seed": 23981363,
			"version": 2,
			"versionNonce": 1126269288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "trip_decisions.py：驗證鏈 if／elif → 最後 else 裡\n計算、分類、四行報告",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jzgfvXKA",
			"originalText": "trip_decisions.py：驗證鏈 if／elif → 最後 else 裡\n計算、分類、四行報告",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2v"
		},
		{
			"id": "YG9uxCe6",
			"type": "rectangle",
			"x": -1147,
			"y": 545.35,
			"width": 458,
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
			"seed": 975356522,
			"version": 2,
			"versionNonce": 448768280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yUrqyHXJ"
				},
				{
					"type": "arrow",
					"id": "G42jdAKA"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2w"
		},
		{
			"id": "yUrqyHXJ",
			"type": "text",
			"x": -1133,
			"y": 554.35,
			"width": 430,
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
			"seed": 1587422842,
			"version": 2,
			"versionNonce": 826086504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Test case＝input＋expected＋actual＋pass/fail\n理由",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YG9uxCe6",
			"originalText": "Test case＝input＋expected＋actual＋pass/fail\n理由",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2x"
		},
		{
			"id": "ygTauf4y",
			"type": "rectangle",
			"x": -1087,
			"y": 622.35,
			"width": 398,
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
			"seed": 716416364,
			"version": 2,
			"versionNonce": 1545258520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LjnV4GAd"
				},
				{
					"type": "arrow",
					"id": "Qf8z93A2"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b2y"
		},
		{
			"id": "LjnV4GAd",
			"type": "text",
			"x": -1073,
			"y": 631.35,
			"width": 370,
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
			"seed": 893085984,
			"version": 2,
			"versionNonce": 476989288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "交付：spec_deck3.md、tests_deck3.md、\nai_use_deck3.md",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ygTauf4y",
			"originalText": "交付：spec_deck3.md、tests_deck3.md、\nai_use_deck3.md",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2z"
		},
		{
			"id": "baEtxFX4",
			"type": "rectangle",
			"x": -405,
			"y": 942.77,
			"width": 92,
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
			"seed": 470826359,
			"version": 2,
			"versionNonce": 1577730840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "963HiCPS"
				},
				{
					"type": "arrow",
					"id": "w3fr4Up2"
				},
				{
					"type": "arrow",
					"id": "7ax2dzvN"
				},
				{
					"type": "arrow",
					"id": "eHYGpinq"
				},
				{
					"type": "arrow",
					"id": "MMwDkujb"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b30"
		},
		{
			"id": "963HiCPS",
			"type": "text",
			"x": -385,
			"y": 954.77,
			"width": 52,
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
			"seed": 2070071904,
			"version": 2,
			"versionNonce": 285284968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "選讀",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "baEtxFX4",
			"originalText": "選讀",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b31"
		},
		{
			"id": "rjcXrDJc",
			"type": "rectangle",
			"x": -609,
			"y": 841.9,
			"width": 128,
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
			"seed": 422570986,
			"version": 2,
			"versionNonce": 1325539352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7spme65L"
				},
				{
					"type": "arrow",
					"id": "7ax2dzvN"
				},
				{
					"type": "arrow",
					"id": "AyshnPEv"
				},
				{
					"type": "arrow",
					"id": "StEGpRy7"
				},
				{
					"type": "arrow",
					"id": "fi33azVU"
				},
				{
					"type": "arrow",
					"id": "jSUcGJLR"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b32"
		},
		{
			"id": "7spme65L",
			"type": "text",
			"x": -595,
			"y": 850.9,
			"width": 100,
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
			"seed": 1304155479,
			"version": 2,
			"versionNonce": 834768232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Truthiness",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rjcXrDJc",
			"originalText": "Truthiness",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b33"
		},
		{
			"id": "dQeXU5Lc",
			"type": "rectangle",
			"x": -1091,
			"y": 748.15,
			"width": 422,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"sT5dgZzb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 991165158,
			"version": 2,
			"versionNonce": 1861639448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8AjE9ueP"
				},
				{
					"type": "arrow",
					"id": "AyshnPEv"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b34"
		},
		{
			"id": "8AjE9ueP",
			"type": "text",
			"x": -1079,
			"y": 755.15,
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
			"groupIds": [
				"sT5dgZzb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 253891483,
			"version": 2,
			"versionNonce": 1744543848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "bool(0) → False；bool(\"0\") → True；bool(\"False\")\n→ True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dQeXU5Lc",
			"originalText": "bool(0) → False；bool(\"0\") → True；bool(\"False\")\n→ True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b35"
		},
		{
			"id": "DVFKXivD",
			"type": "rectangle",
			"x": -1096,
			"y": 816.15,
			"width": 427,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
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
			"seed": 2116970324,
			"version": 2,
			"versionNonce": 1599797784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wt8tkr8u"
				},
				{
					"type": "arrow",
					"id": "StEGpRy7"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b36"
		},
		{
			"id": "wt8tkr8u",
			"type": "text",
			"x": -1084,
			"y": 823.15,
			"width": 403,
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
			"seed": 1033747355,
			"version": 2,
			"versionNonce": 326849384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ and／or 回傳運算元：0 or 7 → 7；\"ok\" and 5 →\n5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DVFKXivD",
			"originalText": "⚠ and／or 回傳運算元：0 or 7 → 7；\"ok\" and 5 →\n5",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b37"
		},
		{
			"id": "nrWWkCzx",
			"type": "rectangle",
			"x": -809,
			"y": 884.15,
			"width": 140,
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
			"seed": 345947242,
			"version": 2,
			"versionNonce": 1931736856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SfGHNx96"
				},
				{
					"type": "arrow",
					"id": "fi33azVU"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b38"
		},
		{
			"id": "SfGHNx96",
			"type": "text",
			"x": -797,
			"y": 891.15,
			"width": 116,
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
			"seed": 458443582,
			"version": 2,
			"versionNonce": 982296168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "not \"\" → True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nrWWkCzx",
			"originalText": "not \"\" → True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b39"
		},
		{
			"id": "iW22tSPx",
			"type": "rectangle",
			"x": -872,
			"y": 932.15,
			"width": 203,
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
			"seed": 1928424881,
			"version": 2,
			"versionNonce": 2126861336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "jQ6JDutg"
				},
				{
					"type": "arrow",
					"id": "jSUcGJLR"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3A"
		},
		{
			"id": "jQ6JDutg",
			"type": "text",
			"x": -860,
			"y": 939.15,
			"width": 179,
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
			"seed": 1267807941,
			"version": 2,
			"versionNonce": 972790120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "比較值用 ==，不要用 is",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iW22tSPx",
			"originalText": "比較值用 ==，不要用 is",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3B"
		},
		{
			"id": "eQreJ9fm",
			"type": "rectangle",
			"x": -941,
			"y": 980.15,
			"width": 460,
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
			"seed": 2066951112,
			"version": 2,
			"versionNonce": 674435352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bxAa5iQT"
				},
				{
					"type": "arrow",
					"id": "eHYGpinq"
				},
				{
					"type": "arrow",
					"id": "ACAhWCSi"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3C"
		},
		{
			"id": "bxAa5iQT",
			"type": "text",
			"x": -927,
			"y": 989.15,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 2031009906,
			"version": 2,
			"versionNonce": 1964256360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "try／except ValueError：解析（能不能變型態）vs\n驗證（值合不合法）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eQreJ9fm",
			"originalText": "try／except ValueError：解析（能不能變型態）vs\n驗證（值合不合法）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3D"
		},
		{
			"id": "Dp9naX6k",
			"type": "rectangle",
			"x": -1167,
			"y": 994.65,
			"width": 166,
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
			"seed": 504742365,
			"version": 2,
			"versionNonce": 920727064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JvygbpyM"
				},
				{
					"type": "arrow",
					"id": "ACAhWCSi"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3E"
		},
		{
			"id": "JvygbpyM",
			"type": "text",
			"x": -1155,
			"y": 1001.65,
			"width": 142,
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
			"seed": 1560839534,
			"version": 2,
			"versionNonce": 94527336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "int(\"45.0\") 仍失敗",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Dp9naX6k",
			"originalText": "int(\"45.0\") 仍失敗",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3F"
		},
		{
			"id": "YLqaCkQ9",
			"type": "rectangle",
			"x": -864,
			"y": 1057.15,
			"width": 383,
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
			"seed": 1429611188,
			"version": 2,
			"versionNonce": 1673767704,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eamME4sV"
				},
				{
					"type": "arrow",
					"id": "MMwDkujb"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3G"
		},
		{
			"id": "eamME4sV",
			"type": "text",
			"x": -850,
			"y": 1066.15,
			"width": 355,
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
			"seed": 1946400960,
			"version": 2,
			"versionNonce": 1811034728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不要偷偷放寬或收緊規格；新政策要新測試",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YLqaCkQ9",
			"originalText": "不要偷偷放寬或收緊規格；新政策要新測試",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3H"
		},
		{
			"id": "8MYcm9cS",
			"type": "rectangle",
			"x": 1443,
			"y": -656.1,
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
				"C6TwmiDR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 864723922,
			"version": 2,
			"versionNonce": 693012504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4WFVbrvU"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3I"
		},
		{
			"id": "4WFVbrvU",
			"type": "text",
			"x": 1450,
			"y": -653.1,
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
				"C6TwmiDR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 762748969,
			"version": 2,
			"versionNonce": 1053795688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T026",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8MYcm9cS",
			"originalText": "T026",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3J"
		},
		{
			"id": "a7zxBXCF",
			"type": "rectangle",
			"x": 1051,
			"y": -534.8,
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
				"Axh97NTL"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 925445753,
			"version": 2,
			"versionNonce": 326485272,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9GX4L6LB"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3K"
		},
		{
			"id": "9GX4L6LB",
			"type": "text",
			"x": 1058,
			"y": -531.8,
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
				"Axh97NTL"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1061249288,
			"version": 2,
			"versionNonce": 1535555688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T032",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "a7zxBXCF",
			"originalText": "T032",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3L"
		},
		{
			"id": "gxyuJ7Ek",
			"type": "rectangle",
			"x": 1024,
			"y": -317.5,
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
			"groupIds": [
				"isq3n58b"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1743950724,
			"version": 2,
			"versionNonce": 263021080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AymKDQR7"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3M"
		},
		{
			"id": "AymKDQR7",
			"type": "text",
			"x": 1031,
			"y": -314.5,
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
			"groupIds": [
				"isq3n58b"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1189291894,
			"version": 2,
			"versionNonce": 367225704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T034 T065",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gxyuJ7Ek",
			"originalText": "T034 T065",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3N"
		},
		{
			"id": "tePveVKF",
			"type": "rectangle",
			"x": 819,
			"y": -191.7,
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
				"rcEJ2mcU"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 729985276,
			"version": 2,
			"versionNonce": 1021927192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bLdHDQDL"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3O"
		},
		{
			"id": "bLdHDQDL",
			"type": "text",
			"x": 826,
			"y": -188.7,
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
				"rcEJ2mcU"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1130474648,
			"version": 2,
			"versionNonce": 1748090472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T027",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tePveVKF",
			"originalText": "T027",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3P"
		},
		{
			"id": "hHKRQSiF",
			"type": "rectangle",
			"x": 854,
			"y": -87.05,
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
				"sDnF7vab"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 217854243,
			"version": 2,
			"versionNonce": 1000193048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "afG799Ua"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3Q"
		},
		{
			"id": "afG799Ua",
			"type": "text",
			"x": 861,
			"y": -84.05,
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
				"sDnF7vab"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1811969228,
			"version": 2,
			"versionNonce": 591245672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T028",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hHKRQSiF",
			"originalText": "T028",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3R"
		},
		{
			"id": "SxCyjB3U",
			"type": "rectangle",
			"x": 1346,
			"y": -50.4,
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
				"teiRQvmK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1796770300,
			"version": 2,
			"versionNonce": 2109634840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Y2wgEgGY"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3S"
		},
		{
			"id": "Y2wgEgGY",
			"type": "text",
			"x": 1353,
			"y": -47.4,
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
				"teiRQvmK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1340628954,
			"version": 2,
			"versionNonce": 508773480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T067",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SxCyjB3U",
			"originalText": "T067",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3T"
		},
		{
			"id": "FkmxMS2n",
			"type": "rectangle",
			"x": 980,
			"y": 36.4,
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
				"5VLxiTwg"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2003066680,
			"version": 2,
			"versionNonce": 381654552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "v8wccPmi"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3U"
		},
		{
			"id": "v8wccPmi",
			"type": "text",
			"x": 987,
			"y": 39.4,
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
				"5VLxiTwg"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1997630277,
			"version": 2,
			"versionNonce": 1732147048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T029",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FkmxMS2n",
			"originalText": "T029",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3V"
		},
		{
			"id": "Q4WwUyQM",
			"type": "rectangle",
			"x": 1275,
			"y": 132.2,
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
				"6B6trsWw"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 931996305,
			"version": 2,
			"versionNonce": 194319128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8Ppz3SYs"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3W"
		},
		{
			"id": "8Ppz3SYs",
			"type": "text",
			"x": 1282,
			"y": 135.2,
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
				"6B6trsWw"
			],
			"frameId": null,
			"roundness": null,
			"seed": 802731564,
			"version": 2,
			"versionNonce": 1917536872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T062",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Q4WwUyQM",
			"originalText": "T062",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3X"
		},
		{
			"id": "6keWuxtq",
			"type": "rectangle",
			"x": 591,
			"y": 268.95,
			"width": 172,
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
				"BZ6d2NCs"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1147530524,
			"version": 2,
			"versionNonce": 582152216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kiMx4kUM"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3Y"
		},
		{
			"id": "kiMx4kUM",
			"type": "text",
			"x": 598,
			"y": 271.95,
			"width": 158,
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
				"BZ6d2NCs"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1383241656,
			"version": 2,
			"versionNonce": 1246084456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T033 T064 Q013 Q031",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6keWuxtq",
			"originalText": "T033 T064 Q013 Q031",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3Z"
		},
		{
			"id": "QjZCzNYd",
			"type": "rectangle",
			"x": 993,
			"y": 363,
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
				"69Fg6m39"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1725921711,
			"version": 2,
			"versionNonce": 873278744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZwyiyrUF"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3a"
		},
		{
			"id": "ZwyiyrUF",
			"type": "text",
			"x": 1000,
			"y": 366,
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
				"69Fg6m39"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1118990359,
			"version": 2,
			"versionNonce": 1081725032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T063",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QjZCzNYd",
			"originalText": "T063",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3b"
		},
		{
			"id": "HuWuAQUp",
			"type": "rectangle",
			"x": 982,
			"y": 458.8,
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
				"DzWsAEdH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1367717092,
			"version": 2,
			"versionNonce": 2031602200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VTh26KHd"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3c"
		},
		{
			"id": "VTh26KHd",
			"type": "text",
			"x": 989,
			"y": 461.8,
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
				"DzWsAEdH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1247820460,
			"version": 2,
			"versionNonce": 481526632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q015",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HuWuAQUp",
			"originalText": "Q015",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3d"
		},
		{
			"id": "xiEvaZbz",
			"type": "rectangle",
			"x": -666,
			"y": -1097.65,
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
				"xChKyEff"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 895136298,
			"version": 2,
			"versionNonce": 1556530968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZaeSyWpX"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3e"
		},
		{
			"id": "ZaeSyWpX",
			"type": "text",
			"x": -659,
			"y": -1094.65,
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
				"xChKyEff"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1950600163,
			"version": 2,
			"versionNonce": 1295963752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T030",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xiEvaZbz",
			"originalText": "T030",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3f"
		},
		{
			"id": "PDMKq4BL",
			"type": "rectangle",
			"x": -707,
			"y": -1024.35,
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
			"groupIds": [
				"TihHH8wn"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1293995918,
			"version": 2,
			"versionNonce": 1267606552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xmUxUQjL"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3g"
		},
		{
			"id": "xmUxUQjL",
			"type": "text",
			"x": -700,
			"y": -1021.35,
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
			"groupIds": [
				"TihHH8wn"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2006471203,
			"version": 2,
			"versionNonce": 384289128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T031 T066",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PDMKq4BL",
			"originalText": "T031 T066",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3h"
		},
		{
			"id": "fFASVw6H",
			"type": "rectangle",
			"x": -666,
			"y": -896.55,
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
				"hEwwpMMb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1510885864,
			"version": 2,
			"versionNonce": 56746264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "233j98EQ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3i"
		},
		{
			"id": "233j98EQ",
			"type": "text",
			"x": -659,
			"y": -893.55,
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
				"hEwwpMMb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 560344040,
			"version": 2,
			"versionNonce": 1157258344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q011",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fFASVw6H",
			"originalText": "Q011",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3j"
		},
		{
			"id": "MAcsXZu9",
			"type": "rectangle",
			"x": -716,
			"y": -716.25,
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
				"xYJLCRtF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1388101730,
			"version": 2,
			"versionNonce": 1672871448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Awr8G2ZV"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3k"
		},
		{
			"id": "Awr8G2ZV",
			"type": "text",
			"x": -709,
			"y": -713.25,
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
				"xYJLCRtF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1158073767,
			"version": 2,
			"versionNonce": 1497534312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q012",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MAcsXZu9",
			"originalText": "Q012",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3l"
		},
		{
			"id": "YMESKqZe",
			"type": "rectangle",
			"x": -757,
			"y": -564,
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
			"groupIds": [
				"emXbdmYC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 831322066,
			"version": 2,
			"versionNonce": 1031699224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QnUxpUQq"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3m"
		},
		{
			"id": "QnUxpUQq",
			"type": "text",
			"x": -750,
			"y": -561,
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
			"groupIds": [
				"emXbdmYC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1156894286,
			"version": 2,
			"versionNonce": 1007444584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T093 Q014",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YMESKqZe",
			"originalText": "T093 Q014",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3n"
		},
		{
			"id": "fmAGcNTN",
			"type": "rectangle",
			"x": -897,
			"y": 93.55,
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
				"Z98A76Hp"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1721340226,
			"version": 2,
			"versionNonce": 590305304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2xRJBZKW"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3o"
		},
		{
			"id": "2xRJBZKW",
			"type": "text",
			"x": -890,
			"y": 96.55,
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
				"Z98A76Hp"
			],
			"frameId": null,
			"roundness": null,
			"seed": 750291203,
			"version": 2,
			"versionNonce": 1814287720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T088",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fmAGcNTN",
			"originalText": "T088",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3p"
		},
		{
			"id": "g5zhLJ6j",
			"type": "rectangle",
			"x": -732,
			"y": 326.3,
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
				"4w8BDqTD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 122081902,
			"version": 2,
			"versionNonce": 951883032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vGhL3wZR"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3q"
		},
		{
			"id": "vGhL3wZR",
			"type": "text",
			"x": -725,
			"y": 329.3,
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
				"4w8BDqTD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1566243840,
			"version": 2,
			"versionNonce": 785705064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q025",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g5zhLJ6j",
			"originalText": "Q025",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3r"
		},
		{
			"id": "jNtUaREZ",
			"type": "rectangle",
			"x": -712,
			"y": 729.35,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#868e96",
			"backgroundColor": "#f1f3f5",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"sT5dgZzb"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2033762253,
			"version": 2,
			"versionNonce": 60437016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "avYdyPby"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3s"
		},
		{
			"id": "avYdyPby",
			"type": "text",
			"x": -705,
			"y": 732.35,
			"width": 35,
			"height": 16.8,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [
				"sT5dgZzb"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1495918511,
			"version": 2,
			"versionNonce": 1072405352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T089",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jNtUaREZ",
			"originalText": "T089",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3t"
		},
		{
			"id": "7WEDfiYb",
			"type": "text",
			"x": -1358,
			"y": -1354.65,
			"width": 1057,
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
			"seed": 1953133396,
			"version": 2,
			"versionNonce": 985411352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 3｜Deck 3：程式如何做決策（W6）",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 3｜Deck 3：程式如何做決策（W6）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3u"
		},
		{
			"id": "Ma77G7Tt",
			"type": "text",
			"x": -1358,
			"y": -1292.65,
			"width": 1530,
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
			"seed": 266450702,
			"version": 2,
			"versionNonce": 28569192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Deck 3 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Deck 3 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3v"
		},
		{
			"id": "GdmABvif",
			"type": "rectangle",
			"x": -1358,
			"y": -1225.65,
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
			"seed": 1360628036,
			"version": 2,
			"versionNonce": 378965016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vk9Ejpwm"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3w"
		},
		{
			"id": "vk9Ejpwm",
			"type": "text",
			"x": -1344,
			"y": -1216.65,
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
			"seed": 1845173290,
			"version": 2,
			"versionNonce": 754573672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GdmABvif",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3x"
		},
		{
			"id": "WVgx6x9v",
			"type": "rectangle",
			"x": -1214,
			"y": -1225.65,
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
			"seed": 1606986484,
			"version": 2,
			"versionNonce": 555567384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "a56NreP3"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b3y"
		},
		{
			"id": "a56NreP3",
			"type": "text",
			"x": -1200,
			"y": -1216.65,
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
			"seed": 1703002264,
			"version": 2,
			"versionNonce": 17396840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例題考到、原本心智圖沒有的觀念",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WVgx6x9v",
			"originalText": "例題考到、原本心智圖沒有的觀念",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3z"
		},
		{
			"id": "vYcTSprW",
			"type": "rectangle",
			"x": -912,
			"y": -1218.05,
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
			"seed": 263860768,
			"version": 2,
			"versionNonce": 96757272,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xGy9q9q2"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b40"
		},
		{
			"id": "xGy9q9q2",
			"type": "text",
			"x": -905,
			"y": -1215.05,
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
			"seed": 760321615,
			"version": 2,
			"versionNonce": 1940825960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001 Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vYcTSprW",
			"originalText": "T001 Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b41"
		},
		{
			"id": "dbRrQyUV",
			"type": "text",
			"x": -814,
			"y": -1216.65,
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
			"seed": 134763200,
			"version": 2,
			"versionNonce": 1635771160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
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
			"index": "b42"
		},
		{
			"id": "xZfMLjes",
			"type": "rectangle",
			"x": -685,
			"y": -1218.05,
			"width": 49,
			"height": 22.8,
			"angle": 0,
			"strokeColor": "#868e96",
			"backgroundColor": "#f1f3f5",
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
			"seed": 1825503778,
			"version": 2,
			"versionNonce": 1630894696,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vkvey3MQ"
				}
			],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"index": "b43"
		},
		{
			"id": "vkvey3MQ",
			"type": "text",
			"x": -678,
			"y": -1215.05,
			"width": 35,
			"height": 16.8,
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
			"seed": 888475448,
			"version": 2,
			"versionNonce": 314818584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T089",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xZfMLjes",
			"originalText": "T089",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b44"
		},
		{
			"id": "ZCbi9dXL",
			"type": "text",
			"x": -628,
			"y": -1216.65,
			"width": 319,
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
			"seed": 130668991,
			"version": 2,
			"versionNonce": 1013575016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858140799,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Extension 延伸題，講義說不代表考試範圍",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Extension 延伸題，講義說不代表考試範圍",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b45"
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