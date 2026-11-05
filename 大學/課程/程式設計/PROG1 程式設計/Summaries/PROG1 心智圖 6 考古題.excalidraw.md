---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Midterm 考古題]]"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
Midterm 題型與考點
考古題 A・B ^3pK2vSjP

兩份考卷 ^2Zacs4u9

考古題 A：年份不明，7 題、110 分 ^gK3CSNTm

考古題 B：Fall 2021，8 題、105 分，附手寫參考
答案 ^eK5Ankiz

⚠ A 卷上的手寫答案不是官方，有錯：A2、A4、
1(e)、1(h)、1(k) ^2xNzjrcB

〔C〕所有答案都用 Python 3.13 驗證過 ^wCFmaAF2

是非題（依主題） ^aptLPSHi

指令集 ^t3adK3AL

不同處理單元可有不同 instruction set → T ^zbLZbmB4

ARM 遵循 RISC → T；遵循 CISC → F ^FaT7U7um

同指令集、效能可不同 → T ^dWHfgnu7

記憶體 ^cszvpMfp

L1 比 L2 小 → T；L1 比 L2 大 → F ^KLJY99fT

L1 比 L2 快 → T ^eXAcT5EA

DRAM 斷電資料消失 → T ^X8zC2jjv

時脈 ^inTshfjw

3.8 GHz「should have better performance」→ F ^nA6Da9kT

3.8 GHz「possibly worse」→ T ^94cJVAwJ

軟體 ^gayWmgeV

「OS 提供的都是 system software」→ F ^6DCkJksK

「OS 提供的可以不是 system software」→ T ^J2ZypiXT

Python ^3RGgXa7C

statement 以換行分隔 → T ^UPGVkNxM

能跨平台是因為「完全相同的 interpreter」→ F ^Vi8nSHVn

多數 logic error IDE 直接抓得到 → F ^ZHUSxjH2

⚠ interpreter 執行前翻成 machine language → 2021
答 T；新講義判 F → 問老師 ^Wd5QeNKe

資料表示 ^vf4jGyUf

所有資料都是 0／1 → T ^D8iF7kUw

1 byte = 8 bits → T ^R4VG95W3

任何數字都能用 8 bits 無損表示 → F ^AbbxLuQz

任何數字都用 8 bits → F ^4F7C6BEt

只看一個 byte 就能解讀意義 → F ^JCJAEx2L

數字字元是 0／1，圖片音樂不是 → F ^JSNVMUAB

輸出題型（必練） ^eLirGxh3

print 套 print ^xcY8C8Ww

A2：a = "3"、b = 5、a*b → 33333None. ^hZUCaH8r

B2："3" + "5" → 35None. ^aVnZQjcK

規則：內層先印並回傳 None；外層印 None，再接 end ^JtVKeYMw

位元運算 ^LhJtEaGV

A3：1^10 → 11；1|10 → 11 → 11,11. ^gWSg5usF

B3：1<<10 → 1024；1^10 → 11 → 1024,11. ^4JWteZSi

for ＋ 同時指派 ^ism3ST2L

A4：a,b = a+b, a*b 跑 5 次 → 330 ^YXMctwy5

(1,1) → (2,1) → (3,2) → (5,6) → (11,30) →
(41,330) ^7Fwuumqj

B4：a,b = b, a+b 跑 10 次 → 144 ^BKxVnW3F

質因數分解（for ＋ while True ＋ break） ^LpHi72pZ

A5：1024 = 2¹⁰ → 210（sep="" 沒空白） ^SGSt3a6A

B5：2056 = 2³ × 257 → 2 3、257 1（sep=" "） ^c5hUGTqf

⚠ CurNum/i 變 float，但印的是 i 與 count ^UGKQ2SAh

倍增到超過 ^j5jZStTJ

A6：99864 → 65536（2¹⁶） ^YMq3tBvm

B6：15431543 → 8388608（2²³） ^5HyGnTyQ

規則：印出 ≤ Num 的最大 2 的次方 ^U4kL2BsS

Fibonacci 找 index ^sXDFghJp

A7：6765 是第 20 項 → 20 ^fZM3DPrJ

不是 Fibonacci 數 → 印 −1 ^qicKyjLN

改錯題（B7，10 分） ^rm7gb7V2

while true: → while True: ^xiSt5gtP

〔C〕Python 裡其實是 NameError，不是
SyntaxError ^8Jrfbd4h

if b = Num: → if b == Num:（SyntaxError） ^bfBbdRJa

else: 縮排對齊 if／elif（IndentationError） ^7atVzuWT

有任何 syntax error，整支程式一行都不會跑 ^aMFYpFjw

改好後輸出 20 ^sBRbYFWh

B8（5 分） ^3XBjHZR7

寫出兩位授課老師姓名 ^sahAZdGj

錯字不計分，對 1 個 2 分 ^AknPQVWi

〔C〕解題 SOP ^uExMm2iZ

畫追蹤表：每一輪寫下所有變數 ^QLkkdaaW

盯 end、sep：有沒有換行、有沒有空白 ^3PpJcHqn

/ 一定是 float；// 往下取整 ^8kbEvc8w

字串 × 整數＝重複；字串 + 字串＝串接 ^b4N4X6RV

while True：找出每條 break 路徑 ^FG2sezyU

是非題：抓絕對詞（Any、all、exactly、should） ^7ckZVLbq

PROG1 期中心智圖 6｜考古題：Midterm 題型與考點 ^j2t4wBDH

來源：PROG1 Midterm 考古題（考古題 A、B）。已拿掉「新講義沒教的舊考點」補充。 ^aq7CZx8F

⚠ 易錯陷阱 ^d8JqhFdH

〔C〕Claude 補充（投影片與講義沒有） ^EMsweLWV

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "eWeCw8Vw",
			"type": "arrow",
			"x": 203.5,
			"y": -0.0,
			"width": 150,
			"height": 505,
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
			"seed": 751891194,
			"version": 2,
			"versionNonce": 1385743208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-505
				],
				[
					150,
					-505
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9bvatdvZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "AEyyrCyW",
			"type": "arrow",
			"x": 494.5,
			"y": -505,
			"width": 76,
			"height": 104.25,
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
			"seed": 1324246419,
			"version": 2,
			"versionNonce": 1389725464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-104.25
				],
				[
					76,
					-104.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9bvatdvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RAa5EAHy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "YJ4VrAj9",
			"type": "arrow",
			"x": 494.5,
			"y": -505,
			"width": 76,
			"height": 38.5,
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
			"seed": 951927423,
			"version": 2,
			"versionNonce": 343676520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-38.5
				],
				[
					76,
					-38.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9bvatdvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FsMQKDg7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "89GMj5UX",
			"type": "arrow",
			"x": 494.5,
			"y": -505,
			"width": 76,
			"height": 38.5,
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
			"seed": 1616241782,
			"version": 2,
			"versionNonce": 298116120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					38.5
				],
				[
					76,
					38.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9bvatdvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "W77afJdJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "cqy8XH4t",
			"type": "arrow",
			"x": 494.5,
			"y": -505,
			"width": 76,
			"height": 104.25,
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
			"seed": 857320577,
			"version": 2,
			"versionNonce": 75303272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					104.25
				],
				[
					76,
					104.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9bvatdvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HFE6fwAd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "kscqAS8D",
			"type": "arrow",
			"x": 203.5,
			"y": -0.0,
			"width": 150,
			"height": 110.5,
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
			"seed": 1938493008,
			"version": 2,
			"versionNonce": 1421910296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					110.5
				],
				[
					150,
					110.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "VCWNZUxj",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 382,
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
			"seed": 1150239924,
			"version": 2,
			"versionNonce": 1307024488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-382
				],
				[
					76,
					-382
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kfKZhmB2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "SVaPMSFb",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 238,
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
			"seed": 322713174,
			"version": 2,
			"versionNonce": 456965656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-238
				],
				[
					76,
					-238
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Ek696cSN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "5Afyu48z",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 118,
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
			"seed": 1466063783,
			"version": 2,
			"versionNonce": 1384632168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-118
				],
				[
					76,
					-118
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XnJecF87",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "53HFUkJ5",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 22,
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
			"seed": 1101805883,
			"version": 2,
			"versionNonce": 1445804824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-22
				],
				[
					76,
					-22
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PupHuMMe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "tnbA49QE",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 127,
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
			"seed": 1304660570,
			"version": 2,
			"versionNonce": 1521066600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					127
				],
				[
					76,
					127
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QNzBABkq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "VZ3dJiAe",
			"type": "arrow",
			"x": 593.5,
			"y": 110.5,
			"width": 76,
			"height": 382,
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
			"seed": 1259950567,
			"version": 2,
			"versionNonce": 939923480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					382
				],
				[
					76,
					382
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NReRHgT8",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "rDAeDWhF",
			"type": "arrow",
			"x": 755.5,
			"y": -271.5,
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
			"seed": 694827065,
			"version": 2,
			"versionNonce": 1159271784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "kfKZhmB2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mXLSysfj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "62LXJE39",
			"type": "arrow",
			"x": 755.5,
			"y": -271.5,
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
			"seed": 554031537,
			"version": 2,
			"versionNonce": 79385880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "kfKZhmB2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wsAyCnqS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "PViA6j23",
			"type": "arrow",
			"x": 755.5,
			"y": -271.5,
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
			"seed": 1168662846,
			"version": 2,
			"versionNonce": 924985448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "kfKZhmB2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GEBis3qG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "jGN8TC7p",
			"type": "arrow",
			"x": 755.5,
			"y": -127.5,
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
			"seed": 806698246,
			"version": 2,
			"versionNonce": 1640034840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "Ek696cSN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nuFEnAFL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "KpC8PXy2",
			"type": "arrow",
			"x": 755.5,
			"y": -127.5,
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
			"seed": 1406040989,
			"version": 2,
			"versionNonce": 1284561768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "Ek696cSN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "UiLF8HMd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "YkhJuDu5",
			"type": "arrow",
			"x": 755.5,
			"y": -127.5,
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
			"seed": 662393288,
			"version": 2,
			"versionNonce": 638250776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "Ek696cSN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SXvjtCJJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "qDxnWtws",
			"type": "arrow",
			"x": 737.5,
			"y": -7.5,
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
			"seed": 1065286977,
			"version": 2,
			"versionNonce": 1202794088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "XnJecF87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XjUbRpVV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "APnku6p8",
			"type": "arrow",
			"x": 737.5,
			"y": -7.5,
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
			"seed": 1052418127,
			"version": 2,
			"versionNonce": 705514520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "XnJecF87",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nPp4AAWW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "avKn4drn",
			"type": "arrow",
			"x": 737.5,
			"y": 88.5,
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
			"seed": 927677392,
			"version": 2,
			"versionNonce": 1095704936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "PupHuMMe",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XkXFJCHA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "uTLKDkjN",
			"type": "arrow",
			"x": 737.5,
			"y": 88.5,
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
			"seed": 2089569067,
			"version": 2,
			"versionNonce": 398199064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "PupHuMMe",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "N7J8e7Rk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "SWpKXNF3",
			"type": "arrow",
			"x": 764.5,
			"y": 237.5,
			"width": 60,
			"height": 77,
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
			"seed": 1854863904,
			"version": 2,
			"versionNonce": 1488368744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-77
				],
				[
					60,
					-77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QNzBABkq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "W8bFpQZJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "xy6k3gFa",
			"type": "arrow",
			"x": 764.5,
			"y": 237.5,
			"width": 60,
			"height": 29,
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
			"seed": 1161104537,
			"version": 2,
			"versionNonce": 982197784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "QNzBABkq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NWtk7qzK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "XyEau2dM",
			"type": "arrow",
			"x": 764.5,
			"y": 237.5,
			"width": 60,
			"height": 19,
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
			"seed": 1810873438,
			"version": 2,
			"versionNonce": 1672734568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					19
				],
				[
					60,
					19
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QNzBABkq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "N97ceQrx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "SEvrUVyW",
			"type": "arrow",
			"x": 764.5,
			"y": 237.5,
			"width": 60,
			"height": 77,
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
			"seed": 1806520109,
			"version": 2,
			"versionNonce": 1332650776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					77
				],
				[
					60,
					77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QNzBABkq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PxkCYrKd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "DGJjgKUm",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
			"width": 60,
			"height": 120,
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
			"seed": 299852883,
			"version": 2,
			"versionNonce": 512932456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-120
				],
				[
					60,
					-120
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QA8WrZVw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "cF3UMfB7",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
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
			"seed": 327534820,
			"version": 2,
			"versionNonce": 1423605784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SLh3ZpZJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "p4GWtcGB",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
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
			"seed": 413839782,
			"version": 2,
			"versionNonce": 1545547112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "DRe6EUB5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "tsEUCeGx",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
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
			"seed": 1800510067,
			"version": 2,
			"versionNonce": 1522711832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BqaZYdeC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "BqudvGuf",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
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
			"seed": 211695409,
			"version": 2,
			"versionNonce": 900022376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ja3Xviyc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "rJnR2xwh",
			"type": "arrow",
			"x": 774.5,
			"y": 492.5,
			"width": 60,
			"height": 120,
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
			"seed": 881712037,
			"version": 2,
			"versionNonce": 1385912856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					120
				],
				[
					60,
					120
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CSzSNAFB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WBTBRiJA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "nS5pzmLp",
			"type": "arrow",
			"x": -203.5,
			"y": -0.0,
			"width": 150,
			"height": 394,
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
			"seed": 1659941271,
			"version": 2,
			"versionNonce": 988869480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-394
				],
				[
					-150,
					-394
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "5L24XKLe",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 310,
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
			"seed": 1044595389,
			"version": 2,
			"versionNonce": 1599624984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-310
				],
				[
					-76,
					-310
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3UK4QKnK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "9c2RDipS",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 190,
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
			"seed": 645789921,
			"version": 2,
			"versionNonce": 575555176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-190
				],
				[
					-76,
					-190
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "83fgV8zQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "cDgabj8a",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 79,
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
			"seed": 1442634678,
			"version": 2,
			"versionNonce": 627946520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-79
				],
				[
					-76,
					-79
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XUPiBdwM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "RgYfF5Dt",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 46,
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
			"seed": 1861992816,
			"version": 2,
			"versionNonce": 2022259048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					46
				],
				[
					-76,
					46
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KSUL65VU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "aZfVxCv3",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 190,
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
			"seed": 467813207,
			"version": 2,
			"versionNonce": 449802520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					190
				],
				[
					-76,
					190
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fVyEgsrP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "KpA2Mw89",
			"type": "arrow",
			"x": -593.5,
			"y": -394,
			"width": 76,
			"height": 310,
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
			"seed": 228681567,
			"version": 2,
			"versionNonce": 1357761640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					310
				],
				[
					-76,
					310
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YH4L5Es5",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "u5kQsXRG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "9FaedMww",
			"type": "arrow",
			"x": -818.5,
			"y": -704,
			"width": 60,
			"height": 48,
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
			"seed": 1920438458,
			"version": 2,
			"versionNonce": 1458671128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "3UK4QKnK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uHnZha2A",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "pfrxExRR",
			"type": "arrow",
			"x": -818.5,
			"y": -704,
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
			"seed": 992554515,
			"version": 2,
			"versionNonce": 1967652712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "3UK4QKnK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rV5Hx4yJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "wKRDJQuc",
			"type": "arrow",
			"x": -818.5,
			"y": -704,
			"width": 60,
			"height": 48,
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
			"seed": 373953250,
			"version": 2,
			"versionNonce": 1657277208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "3UK4QKnK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Jjcr3WAz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "Yj4TNCs8",
			"type": "arrow",
			"x": -774.5,
			"y": -584,
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
			"seed": 492077584,
			"version": 2,
			"versionNonce": 367252072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "83fgV8zQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FkBJnrz3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "zc268DN6",
			"type": "arrow",
			"x": -774.5,
			"y": -584,
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
			"seed": 1982715542,
			"version": 2,
			"versionNonce": 147253272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "83fgV8zQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EnPgkDKR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "nQePrK6T",
			"type": "arrow",
			"x": -835.5,
			"y": -473,
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
			"seed": 2051278709,
			"version": 2,
			"versionNonce": 2039301480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-29
				],
				[
					-60,
					-29
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "XUPiBdwM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "j9ZLv9Up",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "f4dHePtF",
			"type": "arrow",
			"x": -835.5,
			"y": -473,
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
			"seed": 2124779857,
			"version": 2,
			"versionNonce": 618800408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					29
				],
				[
					-60,
					29
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "XUPiBdwM",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cN58FANp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "zQqfcKK5",
			"type": "arrow",
			"x": -1193.5,
			"y": -502,
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
			"seed": 1360008040,
			"version": 2,
			"versionNonce": 764434536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "j9ZLv9Up",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yz9eYcn5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "Jz7BwVme",
			"type": "arrow",
			"x": -1064.5,
			"y": -348,
			"width": 60,
			"height": 48,
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
			"seed": 2133657553,
			"version": 2,
			"versionNonce": 1955447320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "KSUL65VU",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3xHuFYdh",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "tEapkefs",
			"type": "arrow",
			"x": -1064.5,
			"y": -348,
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
			"seed": 40279379,
			"version": 2,
			"versionNonce": 901319528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "KSUL65VU",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MDyFfppg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "pTjySLuW",
			"type": "arrow",
			"x": -1064.5,
			"y": -348,
			"width": 60,
			"height": 48,
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
			"seed": 1122480994,
			"version": 2,
			"versionNonce": 1723711256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "KSUL65VU",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qA8qrFDD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "NSq4fFWv",
			"type": "arrow",
			"x": -792.5,
			"y": -204,
			"width": 60,
			"height": 48,
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
			"seed": 301397617,
			"version": 2,
			"versionNonce": 1012096616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "fVyEgsrP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wUDeJGFJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "Ch6Sm5Dh",
			"type": "arrow",
			"x": -792.5,
			"y": -204,
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
			"seed": 1999271679,
			"version": 2,
			"versionNonce": 1810242584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "fVyEgsrP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "istX7hrA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "hWUSNG69",
			"type": "arrow",
			"x": -792.5,
			"y": -204,
			"width": 60,
			"height": 48,
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
			"seed": 1794859951,
			"version": 2,
			"versionNonce": 1110135144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "fVyEgsrP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rJY4N9Bc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "tfJ2eFGm",
			"type": "arrow",
			"x": -861.5,
			"y": -84,
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
			"seed": 1782092268,
			"version": 2,
			"versionNonce": 1174067480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "u5kQsXRG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2XJHQ47t",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "EHjQgLt7",
			"type": "arrow",
			"x": -861.5,
			"y": -84,
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
			"seed": 1852752622,
			"version": 2,
			"versionNonce": 1317856360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "u5kQsXRG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zLTDq93i",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "22ptDpy9",
			"type": "arrow",
			"x": -203.5,
			"y": -0.0,
			"width": 150,
			"height": 140.38,
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
			"seed": 1704184781,
			"version": 2,
			"versionNonce": 1483732504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					140.38
				],
				[
					-150,
					140.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "ZtbyP9xr",
			"type": "arrow",
			"x": -638.5,
			"y": 140.38,
			"width": 76,
			"height": 112.38,
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
			"seed": 1032667595,
			"version": 2,
			"versionNonce": 524556136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-112.38
				],
				[
					-76,
					-112.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wSrZKZuf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "EzUHd8e4",
			"type": "arrow",
			"x": -638.5,
			"y": 140.38,
			"width": 76,
			"height": 51.13,
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
			"seed": 2106152520,
			"version": 2,
			"versionNonce": 2017030936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-51.13
				],
				[
					-76,
					-51.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "F7jhpujg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "mESp8GC8",
			"type": "arrow",
			"x": -638.5,
			"y": 140.38,
			"width": 76,
			"height": 3.37,
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
			"seed": 1385547089,
			"version": 2,
			"versionNonce": 1486678632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					3.37
				],
				[
					-76,
					3.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "A5YQhbaU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "epRQuqH5",
			"type": "arrow",
			"x": -638.5,
			"y": 140.38,
			"width": 76,
			"height": 57.87,
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
			"seed": 1581460911,
			"version": 2,
			"versionNonce": 1003180056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					57.87
				],
				[
					-76,
					57.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SnPiNfKy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "fhHfhVmg",
			"type": "arrow",
			"x": -638.5,
			"y": 140.38,
			"width": 76,
			"height": 112.37,
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
			"seed": 1612214341,
			"version": 2,
			"versionNonce": 895704424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					112.37
				],
				[
					-76,
					112.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "VDH6uuqL",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "p7hfmATB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "Y3sk8uJA",
			"type": "arrow",
			"x": -967.5,
			"y": 28,
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
			"seed": 751055128,
			"version": 2,
			"versionNonce": 1259965720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
				"elementId": "wSrZKZuf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gguVgYeY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "ymDmsKhC",
			"type": "arrow",
			"x": -203.5,
			"y": -0.0,
			"width": 150,
			"height": 364.5,
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
			"seed": 885170374,
			"version": 2,
			"versionNonce": 920875112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					364.5
				],
				[
					-150,
					364.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "m9g5CZhW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "BzpxVTNt",
			"type": "arrow",
			"x": -529.5,
			"y": 364.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 612711272,
			"version": 2,
			"versionNonce": 798501400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-27.25
				],
				[
					-76,
					-27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "m9g5CZhW",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zyXnjCqK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "vtzeWCVw",
			"type": "arrow",
			"x": -529.5,
			"y": 364.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 114097789,
			"version": 2,
			"versionNonce": 1424565096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					27.25
				],
				[
					-76,
					27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "m9g5CZhW",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "T757jxRH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "y8f7UTGe",
			"type": "arrow",
			"x": -203.5,
			"y": -0.0,
			"width": 150,
			"height": 612.5,
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
			"seed": 54696203,
			"version": 2,
			"versionNonce": 607856408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					612.5
				],
				[
					-150,
					612.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ydqEapNw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "BKVcrkjV",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 136.25,
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
			"seed": 1386593955,
			"version": 2,
			"versionNonce": 767587944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-136.25
				],
				[
					-76,
					-136.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gRuB3ZZJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "D5MFXHh7",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 680182229,
			"version": 2,
			"versionNonce": 1702265880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-81.75
				],
				[
					-76,
					-81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ShCrwF7X",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "7enGUjA8",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 1691468017,
			"version": 2,
			"versionNonce": 909470056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					-27.25
				],
				[
					-76,
					-27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dMDwEpUH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "Zj5FumUP",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 1388850864,
			"version": 2,
			"versionNonce": 20857112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					27.25
				],
				[
					-76,
					27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Z5nx6kRr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "iFbxT5ha",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 468118185,
			"version": 2,
			"versionNonce": 1771306088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					81.75
				],
				[
					-76,
					81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "diPEjcUw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "DbhPDdqv",
			"type": "arrow",
			"x": -571.5,
			"y": 612.5,
			"width": 76,
			"height": 136.25,
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
			"seed": 930119457,
			"version": 2,
			"versionNonce": 654728728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
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
					136.25
				],
				[
					-76,
					136.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DpJu3rxA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3UhYH6xT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "ydqEapNw",
			"type": "rectangle",
			"x": -203.5,
			"y": -67,
			"width": 407,
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
			"seed": 1415942878,
			"version": 2,
			"versionNonce": 2041065320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3pK2vSjP"
				},
				{
					"type": "arrow",
					"id": "eWeCw8Vw"
				},
				{
					"type": "arrow",
					"id": "kscqAS8D"
				},
				{
					"type": "arrow",
					"id": "nS5pzmLp"
				},
				{
					"type": "arrow",
					"id": "22ptDpy9"
				},
				{
					"type": "arrow",
					"id": "ymDmsKhC"
				},
				{
					"type": "arrow",
					"id": "y8f7UTGe"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0A"
		},
		{
			"id": "3pK2vSjP",
			"type": "text",
			"x": -171.5,
			"y": -45,
			"width": 343,
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
			"seed": 151306802,
			"version": 2,
			"versionNonce": 2009258776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "Midterm 題型與考點\n考古題 A・B",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ydqEapNw",
			"originalText": "Midterm 題型與考點\n考古題 A・B",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0B"
		},
		{
			"id": "9bvatdvZ",
			"type": "rectangle",
			"x": 353.5,
			"y": -532,
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
			"seed": 2125618419,
			"version": 2,
			"versionNonce": 2126381672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2Zacs4u9"
				},
				{
					"type": "arrow",
					"id": "eWeCw8Vw"
				},
				{
					"type": "arrow",
					"id": "AEyyrCyW"
				},
				{
					"type": "arrow",
					"id": "YJ4VrAj9"
				},
				{
					"type": "arrow",
					"id": "89GMj5UX"
				},
				{
					"type": "arrow",
					"id": "cqy8XH4t"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0C"
		},
		{
			"id": "2Zacs4u9",
			"type": "text",
			"x": 373.5,
			"y": -520,
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
			"seed": 196629800,
			"version": 2,
			"versionNonce": 1441249304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "兩份考卷",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9bvatdvZ",
			"originalText": "兩份考卷",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0D"
		},
		{
			"id": "RAa5EAHy",
			"type": "rectangle",
			"x": 570.5,
			"y": -629.5,
			"width": 326,
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
			"seed": 696420080,
			"version": 2,
			"versionNonce": 664892776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gK3CSNTm"
				},
				{
					"type": "arrow",
					"id": "AEyyrCyW"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0E"
		},
		{
			"id": "gK3CSNTm",
			"type": "text",
			"x": 584.5,
			"y": -620.5,
			"width": 298,
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
			"seed": 1543406056,
			"version": 2,
			"versionNonce": 896070936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "考古題 A：年份不明，7 題、110 分",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RAa5EAHy",
			"originalText": "考古題 A：年份不明，7 題、110 分",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0F"
		},
		{
			"id": "FsMQKDg7",
			"type": "rectangle",
			"x": 570.5,
			"y": -575,
			"width": 454,
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
			"seed": 410230628,
			"version": 2,
			"versionNonce": 1771997288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eK5Ankiz"
				},
				{
					"type": "arrow",
					"id": "YJ4VrAj9"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0G"
		},
		{
			"id": "eK5Ankiz",
			"type": "text",
			"x": 584.5,
			"y": -566,
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
			"seed": 2127841347,
			"version": 2,
			"versionNonce": 1807389208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "考古題 B：Fall 2021，8 題、105 分，附手寫參考\n答案",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FsMQKDg7",
			"originalText": "考古題 B：Fall 2021，8 題、105 分，附手寫參考\n答案",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0H"
		},
		{
			"id": "W77afJdJ",
			"type": "rectangle",
			"x": 570.5,
			"y": -498,
			"width": 441,
			"height": 63,
			"angle": 0,
			"strokeColor": "#1971c2",
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
			"seed": 1037445104,
			"version": 2,
			"versionNonce": 813775720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2xNzjrcB"
				},
				{
					"type": "arrow",
					"id": "89GMj5UX"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0I"
		},
		{
			"id": "2xNzjrcB",
			"type": "text",
			"x": 584.5,
			"y": -489,
			"width": 413,
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
			"seed": 170904864,
			"version": 2,
			"versionNonce": 2144374552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ A 卷上的手寫答案不是官方，有錯：A2、A4、\n1(e)、1(h)、1(k)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "W77afJdJ",
			"originalText": "⚠ A 卷上的手寫答案不是官方，有錯：A2、A4、\n1(e)、1(h)、1(k)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0J"
		},
		{
			"id": "HFE6fwAd",
			"type": "rectangle",
			"x": 570.5,
			"y": -421,
			"width": 368,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#e7f5ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 534125377,
			"version": 2,
			"versionNonce": 244682344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wCFmaAF2"
				},
				{
					"type": "arrow",
					"id": "cqy8XH4t"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0K"
		},
		{
			"id": "wCFmaAF2",
			"type": "text",
			"x": 584.5,
			"y": -412,
			"width": 340,
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
			"seed": 1303118513,
			"version": 2,
			"versionNonce": 2048846872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "〔C〕所有答案都用 Python 3.13 驗證過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HFE6fwAd",
			"originalText": "〔C〕所有答案都用 Python 3.13 驗證過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0L"
		},
		{
			"id": "NReRHgT8",
			"type": "rectangle",
			"x": 353.5,
			"y": 83.5,
			"width": 240,
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
			"seed": 771454600,
			"version": 2,
			"versionNonce": 1822916968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aptLPSHi"
				},
				{
					"type": "arrow",
					"id": "kscqAS8D"
				},
				{
					"type": "arrow",
					"id": "VCWNZUxj"
				},
				{
					"type": "arrow",
					"id": "SVaPMSFb"
				},
				{
					"type": "arrow",
					"id": "5Afyu48z"
				},
				{
					"type": "arrow",
					"id": "53HFUkJ5"
				},
				{
					"type": "arrow",
					"id": "tnbA49QE"
				},
				{
					"type": "arrow",
					"id": "VZ3dJiAe"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0M"
		},
		{
			"id": "aptLPSHi",
			"type": "text",
			"x": 373.5,
			"y": 95.5,
			"width": 200,
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
			"seed": 651322127,
			"version": 2,
			"versionNonce": 882485528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "是非題（依主題）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NReRHgT8",
			"originalText": "是非題（依主題）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0N"
		},
		{
			"id": "kfKZhmB2",
			"type": "rectangle",
			"x": 669.5,
			"y": -291.75,
			"width": 86,
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
			"seed": 1862529051,
			"version": 2,
			"versionNonce": 973280360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "t3adK3AL"
				},
				{
					"type": "arrow",
					"id": "VCWNZUxj"
				},
				{
					"type": "arrow",
					"id": "rDAeDWhF"
				},
				{
					"type": "arrow",
					"id": "62LXJE39"
				},
				{
					"type": "arrow",
					"id": "PViA6j23"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0O"
		},
		{
			"id": "t3adK3AL",
			"type": "text",
			"x": 683.5,
			"y": -282.75,
			"width": 58,
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
			"seed": 1391392020,
			"version": 2,
			"versionNonce": 716490264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "指令集",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kfKZhmB2",
			"originalText": "指令集",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0P"
		},
		{
			"id": "mXLSysfj",
			"type": "rectangle",
			"x": 815.5,
			"y": -336.5,
			"width": 362,
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
			"seed": 1034900669,
			"version": 2,
			"versionNonce": 477382504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zbLZbmB4"
				},
				{
					"type": "arrow",
					"id": "rDAeDWhF"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0Q"
		},
		{
			"id": "zbLZbmB4",
			"type": "text",
			"x": 827.5,
			"y": -329.5,
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
			"seed": 57034618,
			"version": 2,
			"versionNonce": 1231307544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "不同處理單元可有不同 instruction set → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mXLSysfj",
			"originalText": "不同處理單元可有不同 instruction set → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0R"
		},
		{
			"id": "wsAyCnqS",
			"type": "rectangle",
			"x": 815.5,
			"y": -288.5,
			"width": 331,
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
			"seed": 10499210,
			"version": 2,
			"versionNonce": 541530728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FaT7U7um"
				},
				{
					"type": "arrow",
					"id": "62LXJE39"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0S"
		},
		{
			"id": "FaT7U7um",
			"type": "text",
			"x": 827.5,
			"y": -281.5,
			"width": 307,
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
			"seed": 126362538,
			"version": 2,
			"versionNonce": 1058807832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "ARM 遵循 RISC → T；遵循 CISC → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wsAyCnqS",
			"originalText": "ARM 遵循 RISC → T；遵循 CISC → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0T"
		},
		{
			"id": "GEBis3qG",
			"type": "rectangle",
			"x": 815.5,
			"y": -240.5,
			"width": 235,
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
			"seed": 689729526,
			"version": 2,
			"versionNonce": 1749519720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dWHfgnu7"
				},
				{
					"type": "arrow",
					"id": "PViA6j23"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0U"
		},
		{
			"id": "dWHfgnu7",
			"type": "text",
			"x": 827.5,
			"y": -233.5,
			"width": 211,
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
			"seed": 413651873,
			"version": 2,
			"versionNonce": 1271946520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "同指令集、效能可不同 → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GEBis3qG",
			"originalText": "同指令集、效能可不同 → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0V"
		},
		{
			"id": "Ek696cSN",
			"type": "rectangle",
			"x": 669.5,
			"y": -147.75,
			"width": 86,
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
			"seed": 861119861,
			"version": 2,
			"versionNonce": 1572970600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cszvpMfp"
				},
				{
					"type": "arrow",
					"id": "SVaPMSFb"
				},
				{
					"type": "arrow",
					"id": "jGN8TC7p"
				},
				{
					"type": "arrow",
					"id": "KpC8PXy2"
				},
				{
					"type": "arrow",
					"id": "YkhJuDu5"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0W"
		},
		{
			"id": "cszvpMfp",
			"type": "text",
			"x": 683.5,
			"y": -138.75,
			"width": 58,
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
			"seed": 1367654426,
			"version": 2,
			"versionNonce": 284490264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "記憶體",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Ek696cSN",
			"originalText": "記憶體",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0X"
		},
		{
			"id": "nuFEnAFL",
			"type": "rectangle",
			"x": 815.5,
			"y": -192.5,
			"width": 306,
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
			"seed": 1988554107,
			"version": 2,
			"versionNonce": 1619088232,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KLJY99fT"
				},
				{
					"type": "arrow",
					"id": "jGN8TC7p"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0Y"
		},
		{
			"id": "KLJY99fT",
			"type": "text",
			"x": 827.5,
			"y": -185.5,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 925266035,
			"version": 2,
			"versionNonce": 1635645208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "L1 比 L2 小 → T；L1 比 L2 大 → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nuFEnAFL",
			"originalText": "L1 比 L2 小 → T；L1 比 L2 大 → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0Z"
		},
		{
			"id": "UiLF8HMd",
			"type": "rectangle",
			"x": 815.5,
			"y": -144.5,
			"width": 159,
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
			"seed": 1041737236,
			"version": 2,
			"versionNonce": 1993516648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eXAcT5EA"
				},
				{
					"type": "arrow",
					"id": "KpC8PXy2"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0a"
		},
		{
			"id": "eXAcT5EA",
			"type": "text",
			"x": 827.5,
			"y": -137.5,
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
			"seed": 2056125077,
			"version": 2,
			"versionNonce": 299848728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "L1 比 L2 快 → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UiLF8HMd",
			"originalText": "L1 比 L2 快 → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0b"
		},
		{
			"id": "SXvjtCJJ",
			"type": "rectangle",
			"x": 815.5,
			"y": -96.5,
			"width": 225,
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
			"seed": 875750457,
			"version": 2,
			"versionNonce": 2105645416,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "X8zC2jjv"
				},
				{
					"type": "arrow",
					"id": "YkhJuDu5"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0c"
		},
		{
			"id": "X8zC2jjv",
			"type": "text",
			"x": 827.5,
			"y": -89.5,
			"width": 201,
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
			"seed": 1685832369,
			"version": 2,
			"versionNonce": 1208815896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "DRAM 斷電資料消失 → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SXvjtCJJ",
			"originalText": "DRAM 斷電資料消失 → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0d"
		},
		{
			"id": "XnJecF87",
			"type": "rectangle",
			"x": 669.5,
			"y": -27.75,
			"width": 68,
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
			"seed": 1242117588,
			"version": 2,
			"versionNonce": 1473916008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "inTshfjw"
				},
				{
					"type": "arrow",
					"id": "5Afyu48z"
				},
				{
					"type": "arrow",
					"id": "qDxnWtws"
				},
				{
					"type": "arrow",
					"id": "APnku6p8"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0e"
		},
		{
			"id": "inTshfjw",
			"type": "text",
			"x": 683.5,
			"y": -18.75,
			"width": 40,
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
			"seed": 201772948,
			"version": 2,
			"versionNonce": 1266363928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "時脈",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XnJecF87",
			"originalText": "時脈",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0f"
		},
		{
			"id": "XjUbRpVV",
			"type": "rectangle",
			"x": 797.5,
			"y": -48.5,
			"width": 412,
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
			"seed": 1420091678,
			"version": 2,
			"versionNonce": 531128168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nA6Da9kT"
				},
				{
					"type": "arrow",
					"id": "qDxnWtws"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0g"
		},
		{
			"id": "nA6Da9kT",
			"type": "text",
			"x": 809.5,
			"y": -41.5,
			"width": 388,
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
			"seed": 156264537,
			"version": 2,
			"versionNonce": 1428007704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "3.8 GHz「should have better performance」→ F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XjUbRpVV",
			"originalText": "3.8 GHz「should have better performance」→ F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0h"
		},
		{
			"id": "nPp4AAWW",
			"type": "rectangle",
			"x": 797.5,
			"y": -0.5,
			"width": 275,
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
			"seed": 1158827479,
			"version": 2,
			"versionNonce": 1429746280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "94cJVAwJ"
				},
				{
					"type": "arrow",
					"id": "APnku6p8"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0i"
		},
		{
			"id": "94cJVAwJ",
			"type": "text",
			"x": 809.5,
			"y": 6.5,
			"width": 251,
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
			"seed": 1346224759,
			"version": 2,
			"versionNonce": 1600686104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "3.8 GHz「possibly worse」→ T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nPp4AAWW",
			"originalText": "3.8 GHz「possibly worse」→ T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0j"
		},
		{
			"id": "PupHuMMe",
			"type": "rectangle",
			"x": 669.5,
			"y": 68.25,
			"width": 68,
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
			"seed": 1961267584,
			"version": 2,
			"versionNonce": 257271144,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gayWmgeV"
				},
				{
					"type": "arrow",
					"id": "53HFUkJ5"
				},
				{
					"type": "arrow",
					"id": "avKn4drn"
				},
				{
					"type": "arrow",
					"id": "uTLKDkjN"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0k"
		},
		{
			"id": "gayWmgeV",
			"type": "text",
			"x": 683.5,
			"y": 77.25,
			"width": 40,
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
			"seed": 1445228636,
			"version": 2,
			"versionNonce": 1984939288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "軟體",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PupHuMMe",
			"originalText": "軟體",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0l"
		},
		{
			"id": "XkXFJCHA",
			"type": "rectangle",
			"x": 797.5,
			"y": 47.5,
			"width": 346,
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
			"seed": 1497995593,
			"version": 2,
			"versionNonce": 726448232,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6DCkJksK"
				},
				{
					"type": "arrow",
					"id": "avKn4drn"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0m"
		},
		{
			"id": "6DCkJksK",
			"type": "text",
			"x": 809.5,
			"y": 54.5,
			"width": 322,
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
			"seed": 19526349,
			"version": 2,
			"versionNonce": 122118680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "「OS 提供的都是 system software」→ F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XkXFJCHA",
			"originalText": "「OS 提供的都是 system software」→ F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0n"
		},
		{
			"id": "N7J8e7Rk",
			"type": "rectangle",
			"x": 797.5,
			"y": 95.5,
			"width": 382,
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
			"seed": 1159555373,
			"version": 2,
			"versionNonce": 2095672168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J2ZypiXT"
				},
				{
					"type": "arrow",
					"id": "uTLKDkjN"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0o"
		},
		{
			"id": "J2ZypiXT",
			"type": "text",
			"x": 809.5,
			"y": 102.5,
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
			"seed": 184826160,
			"version": 2,
			"versionNonce": 826498840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "「OS 提供的可以不是 system software」→ T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "N7J8e7Rk",
			"originalText": "「OS 提供的可以不是 system software」→ T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0p"
		},
		{
			"id": "QNzBABkq",
			"type": "rectangle",
			"x": 669.5,
			"y": 217.25,
			"width": 95,
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
			"seed": 1929186996,
			"version": 2,
			"versionNonce": 2121776744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3RGgXa7C"
				},
				{
					"type": "arrow",
					"id": "tnbA49QE"
				},
				{
					"type": "arrow",
					"id": "SWpKXNF3"
				},
				{
					"type": "arrow",
					"id": "xy6k3gFa"
				},
				{
					"type": "arrow",
					"id": "XyEau2dM"
				},
				{
					"type": "arrow",
					"id": "SEvrUVyW"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0q"
		},
		{
			"id": "3RGgXa7C",
			"type": "text",
			"x": 683.5,
			"y": 226.25,
			"width": 67,
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
			"seed": 1704973658,
			"version": 2,
			"versionNonce": 347585560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Python",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QNzBABkq",
			"originalText": "Python",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0r"
		},
		{
			"id": "W8bFpQZJ",
			"type": "rectangle",
			"x": 824.5,
			"y": 143.5,
			"width": 242,
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
			"seed": 48462360,
			"version": 2,
			"versionNonce": 12824936,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UPGVkNxM"
				},
				{
					"type": "arrow",
					"id": "SWpKXNF3"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0s"
		},
		{
			"id": "UPGVkNxM",
			"type": "text",
			"x": 836.5,
			"y": 150.5,
			"width": 218,
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
			"seed": 593337511,
			"version": 2,
			"versionNonce": 597195032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "statement 以換行分隔 → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "W8bFpQZJ",
			"originalText": "statement 以換行分隔 → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0t"
		},
		{
			"id": "NWtk7qzK",
			"type": "rectangle",
			"x": 824.5,
			"y": 191.5,
			"width": 384,
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
			"seed": 1602738988,
			"version": 2,
			"versionNonce": 1528382568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Vi8nSHVn"
				},
				{
					"type": "arrow",
					"id": "xy6k3gFa"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0u"
		},
		{
			"id": "Vi8nSHVn",
			"type": "text",
			"x": 836.5,
			"y": 198.5,
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
			"seed": 1078684030,
			"version": 2,
			"versionNonce": 1901696536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "能跨平台是因為「完全相同的 interpreter」→ F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NWtk7qzK",
			"originalText": "能跨平台是因為「完全相同的 interpreter」→ F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0v"
		},
		{
			"id": "N97ceQrx",
			"type": "rectangle",
			"x": 824.5,
			"y": 239.5,
			"width": 316,
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
			"seed": 918327386,
			"version": 2,
			"versionNonce": 457471848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZHUSxjH2"
				},
				{
					"type": "arrow",
					"id": "XyEau2dM"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0w"
		},
		{
			"id": "ZHUSxjH2",
			"type": "text",
			"x": 836.5,
			"y": 246.5,
			"width": 292,
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
			"seed": 139200708,
			"version": 2,
			"versionNonce": 49222424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "多數 logic error IDE 直接抓得到 → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "N97ceQrx",
			"originalText": "多數 logic error IDE 直接抓得到 → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0x"
		},
		{
			"id": "PxkCYrKd",
			"type": "rectangle",
			"x": 824.5,
			"y": 287.5,
			"width": 436,
			"height": 54,
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
			"seed": 1126163996,
			"version": 2,
			"versionNonce": 898714216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Wd5QeNKe"
				},
				{
					"type": "arrow",
					"id": "SEvrUVyW"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b0y"
		},
		{
			"id": "Wd5QeNKe",
			"type": "text",
			"x": 836.5,
			"y": 294.5,
			"width": 412,
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
			"seed": 1437666265,
			"version": 2,
			"versionNonce": 516747288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ interpreter 執行前翻成 machine language → 2021\n答 T；新講義判 F → 問老師",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PxkCYrKd",
			"originalText": "⚠ interpreter 執行前翻成 machine language → 2021\n答 T；新講義判 F → 問老師",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0z"
		},
		{
			"id": "CSzSNAFB",
			"type": "rectangle",
			"x": 669.5,
			"y": 472.25,
			"width": 105,
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
			"seed": 681844443,
			"version": 2,
			"versionNonce": 885767528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vf4jGyUf"
				},
				{
					"type": "arrow",
					"id": "VZ3dJiAe"
				},
				{
					"type": "arrow",
					"id": "DGJjgKUm"
				},
				{
					"type": "arrow",
					"id": "cF3UMfB7"
				},
				{
					"type": "arrow",
					"id": "p4GWtcGB"
				},
				{
					"type": "arrow",
					"id": "tsEUCeGx"
				},
				{
					"type": "arrow",
					"id": "BqudvGuf"
				},
				{
					"type": "arrow",
					"id": "rJnR2xwh"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b10"
		},
		{
			"id": "vf4jGyUf",
			"type": "text",
			"x": 683.5,
			"y": 481.25,
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
			"seed": 121230651,
			"version": 2,
			"versionNonce": 484912408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "資料表示",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CSzSNAFB",
			"originalText": "資料表示",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b11"
		},
		{
			"id": "QA8WrZVw",
			"type": "rectangle",
			"x": 834.5,
			"y": 355.5,
			"width": 210,
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
			"seed": 1626735711,
			"version": 2,
			"versionNonce": 1782567016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "D8iF7kUw"
				},
				{
					"type": "arrow",
					"id": "DGJjgKUm"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b12"
		},
		{
			"id": "D8iF7kUw",
			"type": "text",
			"x": 846.5,
			"y": 362.5,
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
			"seed": 389019181,
			"version": 2,
			"versionNonce": 917621272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "所有資料都是 0／1 → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QA8WrZVw",
			"originalText": "所有資料都是 0／1 → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b13"
		},
		{
			"id": "SLh3ZpZJ",
			"type": "rectangle",
			"x": 834.5,
			"y": 403.5,
			"width": 190,
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
			"seed": 1754734412,
			"version": 2,
			"versionNonce": 498697064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "R4VG95W3"
				},
				{
					"type": "arrow",
					"id": "cF3UMfB7"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b14"
		},
		{
			"id": "R4VG95W3",
			"type": "text",
			"x": 846.5,
			"y": 410.5,
			"width": 166,
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
			"seed": 1777188364,
			"version": 2,
			"versionNonce": 1461765912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "1 byte = 8 bits → T",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SLh3ZpZJ",
			"originalText": "1 byte = 8 bits → T",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b15"
		},
		{
			"id": "DRe6EUB5",
			"type": "rectangle",
			"x": 834.5,
			"y": 451.5,
			"width": 310,
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
			"seed": 2136514347,
			"version": 2,
			"versionNonce": 1032115816,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AbbxLuQz"
				},
				{
					"type": "arrow",
					"id": "p4GWtcGB"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b16"
		},
		{
			"id": "AbbxLuQz",
			"type": "text",
			"x": 846.5,
			"y": 458.5,
			"width": 286,
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
			"seed": 2057344299,
			"version": 2,
			"versionNonce": 1789404184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "任何數字都能用 8 bits 無損表示 → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DRe6EUB5",
			"originalText": "任何數字都能用 8 bits 無損表示 → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b17"
		},
		{
			"id": "BqaZYdeC",
			"type": "rectangle",
			"x": 834.5,
			"y": 499.5,
			"width": 221,
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
			"seed": 1730735958,
			"version": 2,
			"versionNonce": 242076008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4F7C6BEt"
				},
				{
					"type": "arrow",
					"id": "tsEUCeGx"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b18"
		},
		{
			"id": "4F7C6BEt",
			"type": "text",
			"x": 846.5,
			"y": 506.5,
			"width": 197,
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
			"seed": 1641085522,
			"version": 2,
			"versionNonce": 792453400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "任何數字都用 8 bits → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BqaZYdeC",
			"originalText": "任何數字都用 8 bits → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b19"
		},
		{
			"id": "ja3Xviyc",
			"type": "rectangle",
			"x": 834.5,
			"y": 547.5,
			"width": 281,
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
			"seed": 500322663,
			"version": 2,
			"versionNonce": 1539333224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JCJAEx2L"
				},
				{
					"type": "arrow",
					"id": "BqudvGuf"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1A"
		},
		{
			"id": "JCJAEx2L",
			"type": "text",
			"x": 846.5,
			"y": 554.5,
			"width": 257,
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
			"seed": 1438310559,
			"version": 2,
			"versionNonce": 72351256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "只看一個 byte 就能解讀意義 → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ja3Xviyc",
			"originalText": "只看一個 byte 就能解讀意義 → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1B"
		},
		{
			"id": "WBTBRiJA",
			"type": "rectangle",
			"x": 834.5,
			"y": 595.5,
			"width": 306,
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
			"seed": 1459831889,
			"version": 2,
			"versionNonce": 659066728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JSNVMUAB"
				},
				{
					"type": "arrow",
					"id": "rJnR2xwh"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1C"
		},
		{
			"id": "JSNVMUAB",
			"type": "text",
			"x": 846.5,
			"y": 602.5,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 580110265,
			"version": 2,
			"versionNonce": 987265816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "數字字元是 0／1，圖片音樂不是 → F",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WBTBRiJA",
			"originalText": "數字字元是 0／1，圖片音樂不是 → F",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1D"
		},
		{
			"id": "YH4L5Es5",
			"type": "rectangle",
			"x": -593.5,
			"y": -421,
			"width": 240,
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
			"seed": 2002168423,
			"version": 2,
			"versionNonce": 1498571368,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eLirGxh3"
				},
				{
					"type": "arrow",
					"id": "nS5pzmLp"
				},
				{
					"type": "arrow",
					"id": "5L24XKLe"
				},
				{
					"type": "arrow",
					"id": "9c2RDipS"
				},
				{
					"type": "arrow",
					"id": "cDgabj8a"
				},
				{
					"type": "arrow",
					"id": "RgYfF5Dt"
				},
				{
					"type": "arrow",
					"id": "aZfVxCv3"
				},
				{
					"type": "arrow",
					"id": "KpA2Mw89"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "eLirGxh3",
			"type": "text",
			"x": -573.5,
			"y": -409,
			"width": 200,
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
			"seed": 1068627388,
			"version": 2,
			"versionNonce": 1699305496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "輸出題型（必練）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YH4L5Es5",
			"originalText": "輸出題型（必練）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "3UK4QKnK",
			"type": "rectangle",
			"x": -818.5,
			"y": -724.25,
			"width": 149,
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
			"seed": 684572535,
			"version": 2,
			"versionNonce": 1890178408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xcY8C8Ww"
				},
				{
					"type": "arrow",
					"id": "5L24XKLe"
				},
				{
					"type": "arrow",
					"id": "9FaedMww"
				},
				{
					"type": "arrow",
					"id": "pfrxExRR"
				},
				{
					"type": "arrow",
					"id": "wKRDJQuc"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "xcY8C8Ww",
			"type": "text",
			"x": -804.5,
			"y": -715.25,
			"width": 121,
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
			"seed": 1856962000,
			"version": 2,
			"versionNonce": 664179992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "print 套 print",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3UK4QKnK",
			"originalText": "print 套 print",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "uHnZha2A",
			"type": "rectangle",
			"x": -1222.5,
			"y": -769,
			"width": 344,
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
			"seed": 1055534718,
			"version": 2,
			"versionNonce": 849012840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hZUCaH8r"
				},
				{
					"type": "arrow",
					"id": "9FaedMww"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "hZUCaH8r",
			"type": "text",
			"x": -1210.5,
			"y": -762,
			"width": 320,
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
			"seed": 282126255,
			"version": 2,
			"versionNonce": 120861208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A2：a = \"3\"、b = 5、a*b → 33333None.",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uHnZha2A",
			"originalText": "A2：a = \"3\"、b = 5、a*b → 33333None.",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "rV5Hx4yJ",
			"type": "rectangle",
			"x": -1104.5,
			"y": -721,
			"width": 226,
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
			"seed": 634088717,
			"version": 2,
			"versionNonce": 1525783400,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aVnZQjcK"
				},
				{
					"type": "arrow",
					"id": "pfrxExRR"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "aVnZQjcK",
			"type": "text",
			"x": -1092.5,
			"y": -714,
			"width": 202,
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
			"seed": 672885383,
			"version": 2,
			"versionNonce": 991309592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "B2：\"3\" + \"5\" → 35None.",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rV5Hx4yJ",
			"originalText": "B2：\"3\" + \"5\" → 35None.",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "Jjcr3WAz",
			"type": "rectangle",
			"x": -1308.5,
			"y": -673,
			"width": 430,
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
			"seed": 1005539323,
			"version": 2,
			"versionNonce": 1274670696,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JtVKeYMw"
				},
				{
					"type": "arrow",
					"id": "wKRDJQuc"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "JtVKeYMw",
			"type": "text",
			"x": -1296.5,
			"y": -666,
			"width": 406,
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
			"seed": 1259777129,
			"version": 2,
			"versionNonce": 2075167768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "規則：內層先印並回傳 None；外層印 None，再接 end",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Jjcr3WAz",
			"originalText": "規則：內層先印並回傳 None；外層印 None，再接 end",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "83fgV8zQ",
			"type": "rectangle",
			"x": -774.5,
			"y": -604.25,
			"width": 105,
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
			"seed": 1295192624,
			"version": 2,
			"versionNonce": 1048568168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LhJtEaGV"
				},
				{
					"type": "arrow",
					"id": "9c2RDipS"
				},
				{
					"type": "arrow",
					"id": "Yj4TNCs8"
				},
				{
					"type": "arrow",
					"id": "zc268DN6"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "LhJtEaGV",
			"type": "text",
			"x": -760.5,
			"y": -595.25,
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
			"seed": 1319471141,
			"version": 2,
			"versionNonce": 1391937816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "位元運算",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "83fgV8zQ",
			"originalText": "位元運算",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "FkBJnrz3",
			"type": "rectangle",
			"x": -1132.5,
			"y": -625,
			"width": 298,
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
			"seed": 1493023800,
			"version": 2,
			"versionNonce": 1909421160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gWSg5usF"
				},
				{
					"type": "arrow",
					"id": "Yj4TNCs8"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "gWSg5usF",
			"type": "text",
			"x": -1120.5,
			"y": -618,
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
			"seed": 1705471518,
			"version": 2,
			"versionNonce": 1818125848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A3：1^10 → 11；1|10 → 11 → 11,11.",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FkBJnrz3",
			"originalText": "A3：1^10 → 11；1|10 → 11 → 11,11.",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "EnPgkDKR",
			"type": "rectangle",
			"x": -1197.5,
			"y": -577,
			"width": 363,
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
			"seed": 438989910,
			"version": 2,
			"versionNonce": 1538565992,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4JWteZSi"
				},
				{
					"type": "arrow",
					"id": "zc268DN6"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "4JWteZSi",
			"type": "text",
			"x": -1185.5,
			"y": -570,
			"width": 339,
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
			"seed": 983666582,
			"version": 2,
			"versionNonce": 1692001048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "B3：1<<10 → 1024；1^10 → 11 → 1024,11.",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EnPgkDKR",
			"originalText": "B3：1<<10 → 1024；1^10 → 11 → 1024,11.",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "XUPiBdwM",
			"type": "rectangle",
			"x": -835.5,
			"y": -493.25,
			"width": 166,
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
			"seed": 1313073430,
			"version": 2,
			"versionNonce": 1484487272,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ism3ST2L"
				},
				{
					"type": "arrow",
					"id": "cDgabj8a"
				},
				{
					"type": "arrow",
					"id": "nQePrK6T"
				},
				{
					"type": "arrow",
					"id": "f4dHePtF"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "ism3ST2L",
			"type": "text",
			"x": -821.5,
			"y": -484.25,
			"width": 138,
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
			"seed": 1461847203,
			"version": 2,
			"versionNonce": 450740248,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "for ＋ 同時指派",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XUPiBdwM",
			"originalText": "for ＋ 同時指派",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "j9ZLv9Up",
			"type": "rectangle",
			"x": -1193.5,
			"y": -519,
			"width": 298,
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
			"seed": 532772092,
			"version": 2,
			"versionNonce": 1525673320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YXMctwy5"
				},
				{
					"type": "arrow",
					"id": "nQePrK6T"
				},
				{
					"type": "arrow",
					"id": "zQqfcKK5"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "YXMctwy5",
			"type": "text",
			"x": -1181.5,
			"y": -512,
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
			"seed": 1513834188,
			"version": 2,
			"versionNonce": 2120088856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A4：a,b = a+b, a*b 跑 5 次 → 330",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "j9ZLv9Up",
			"originalText": "A4：a,b = a+b, a*b 跑 5 次 → 330",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "yz9eYcn5",
			"type": "rectangle",
			"x": -1621.5,
			"y": -529,
			"width": 368,
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
			"seed": 813442511,
			"version": 2,
			"versionNonce": 475922536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7Fwuumqj"
				},
				{
					"type": "arrow",
					"id": "zQqfcKK5"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "7Fwuumqj",
			"type": "text",
			"x": -1609.5,
			"y": -522,
			"width": 344,
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
			"seed": 1436160663,
			"version": 2,
			"versionNonce": 1624152600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "(1,1) → (2,1) → (3,2) → (5,6) → (11,30) →\n(41,330)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yz9eYcn5",
			"originalText": "(1,1) → (2,1) → (3,2) → (5,6) → (11,30) →\n(41,330)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "cN58FANp",
			"type": "rectangle",
			"x": -1180.5,
			"y": -461,
			"width": 285,
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
			"seed": 2098139008,
			"version": 2,
			"versionNonce": 1284617064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BKxVnW3F"
				},
				{
					"type": "arrow",
					"id": "f4dHePtF"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "BKxVnW3F",
			"type": "text",
			"x": -1168.5,
			"y": -454,
			"width": 261,
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
			"seed": 1802064830,
			"version": 2,
			"versionNonce": 1159960344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "B4：a,b = b, a+b 跑 10 次 → 144",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cN58FANp",
			"originalText": "B4：a,b = b, a+b 跑 10 次 → 144",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "KSUL65VU",
			"type": "rectangle",
			"x": -1064.5,
			"y": -368.25,
			"width": 395,
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
			"seed": 516089228,
			"version": 2,
			"versionNonce": 1104610920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LpHi72pZ"
				},
				{
					"type": "arrow",
					"id": "RgYfF5Dt"
				},
				{
					"type": "arrow",
					"id": "Jz7BwVme"
				},
				{
					"type": "arrow",
					"id": "tEapkefs"
				},
				{
					"type": "arrow",
					"id": "pTjySLuW"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "LpHi72pZ",
			"type": "text",
			"x": -1050.5,
			"y": -359.25,
			"width": 367,
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
			"seed": 1851686338,
			"version": 2,
			"versionNonce": 802223128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "質因數分解（for ＋ while True ＋ break）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KSUL65VU",
			"originalText": "質因數分解（for ＋ while True ＋ break）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "3xHuFYdh",
			"type": "rectangle",
			"x": -1470.5,
			"y": -413,
			"width": 346,
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
			"seed": 251911211,
			"version": 2,
			"versionNonce": 687470952,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SGSt3a6A"
				},
				{
					"type": "arrow",
					"id": "Jz7BwVme"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "SGSt3a6A",
			"type": "text",
			"x": -1458.5,
			"y": -406,
			"width": 322,
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
			"seed": 1598619371,
			"version": 2,
			"versionNonce": 1992995096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A5：1024 = 2¹⁰ → 210（sep=\"\" 沒空白）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3xHuFYdh",
			"originalText": "A5：1024 = 2¹⁰ → 210（sep=\"\" 沒空白）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "MDyFfppg",
			"type": "rectangle",
			"x": -1531.5,
			"y": -365,
			"width": 407,
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
			"seed": 1091857315,
			"version": 2,
			"versionNonce": 893815912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "c5hUGTqf"
				},
				{
					"type": "arrow",
					"id": "tEapkefs"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "c5hUGTqf",
			"type": "text",
			"x": -1519.5,
			"y": -358,
			"width": 383,
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
			"seed": 178887770,
			"version": 2,
			"versionNonce": 293916184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "B5：2056 = 2³ × 257 → 2 3、257 1（sep=\" \"）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MDyFfppg",
			"originalText": "B5：2056 = 2³ × 257 → 2 3、257 1（sep=\" \"）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "qA8qrFDD",
			"type": "rectangle",
			"x": -1482.5,
			"y": -317,
			"width": 358,
			"height": 34,
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
			"seed": 252446314,
			"version": 2,
			"versionNonce": 1351139176,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UGKQ2SAh"
				},
				{
					"type": "arrow",
					"id": "pTjySLuW"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "UGKQ2SAh",
			"type": "text",
			"x": -1470.5,
			"y": -310,
			"width": 334,
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
			"seed": 1351393656,
			"version": 2,
			"versionNonce": 1760774936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ CurNum/i 變 float，但印的是 i 與 count",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qA8qrFDD",
			"originalText": "⚠ CurNum/i 變 float，但印的是 i 與 count",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "fVyEgsrP",
			"type": "rectangle",
			"x": -792.5,
			"y": -224.25,
			"width": 123,
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
			"seed": 942303225,
			"version": 2,
			"versionNonce": 1259115112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "j5jZStTJ"
				},
				{
					"type": "arrow",
					"id": "aZfVxCv3"
				},
				{
					"type": "arrow",
					"id": "NSq4fFWv"
				},
				{
					"type": "arrow",
					"id": "Ch6Sm5Dh"
				},
				{
					"type": "arrow",
					"id": "hWUSNG69"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "j5jZStTJ",
			"type": "text",
			"x": -778.5,
			"y": -215.25,
			"width": 95,
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
			"seed": 545510238,
			"version": 2,
			"versionNonce": 663365656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "倍增到超過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fVyEgsrP",
			"originalText": "倍增到超過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "wUDeJGFJ",
			"type": "rectangle",
			"x": -1104.5,
			"y": -269,
			"width": 252,
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
			"seed": 69244472,
			"version": 2,
			"versionNonce": 194905448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YMq3tBvm"
				},
				{
					"type": "arrow",
					"id": "NSq4fFWv"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "YMq3tBvm",
			"type": "text",
			"x": -1092.5,
			"y": -262,
			"width": 228,
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
			"seed": 1485693583,
			"version": 2,
			"versionNonce": 155018520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A6：99864 → 65536（2¹⁶）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wUDeJGFJ",
			"originalText": "A6：99864 → 65536（2¹⁶）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "istX7hrA",
			"type": "rectangle",
			"x": -1149.5,
			"y": -221,
			"width": 297,
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
			"seed": 839597428,
			"version": 2,
			"versionNonce": 1065949288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5HyGnTyQ"
				},
				{
					"type": "arrow",
					"id": "Ch6Sm5Dh"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "5HyGnTyQ",
			"type": "text",
			"x": -1137.5,
			"y": -214,
			"width": 273,
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
			"seed": 143225427,
			"version": 2,
			"versionNonce": 729874968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "B6：15431543 → 8388608（2²³）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "istX7hrA",
			"originalText": "B6：15431543 → 8388608（2²³）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "rJY4N9Bc",
			"type": "rectangle",
			"x": -1144.5,
			"y": -173,
			"width": 292,
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
			"seed": 1853023892,
			"version": 2,
			"versionNonce": 177851240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "U4kL2BsS"
				},
				{
					"type": "arrow",
					"id": "hWUSNG69"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "U4kL2BsS",
			"type": "text",
			"x": -1132.5,
			"y": -166,
			"width": 268,
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
			"seed": 2062386837,
			"version": 2,
			"versionNonce": 1565064984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "規則：印出 ≤ Num 的最大 2 的次方",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rJY4N9Bc",
			"originalText": "規則：印出 ≤ Num 的最大 2 的次方",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "u5kQsXRG",
			"type": "rectangle",
			"x": -861.5,
			"y": -104.25,
			"width": 192,
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
			"seed": 1040255707,
			"version": 2,
			"versionNonce": 924589672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sXDFghJp"
				},
				{
					"type": "arrow",
					"id": "KpA2Mw89"
				},
				{
					"type": "arrow",
					"id": "tfJ2eFGm"
				},
				{
					"type": "arrow",
					"id": "EHjQgLt7"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "sXDFghJp",
			"type": "text",
			"x": -847.5,
			"y": -95.25,
			"width": 164,
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
			"seed": 2141923690,
			"version": 2,
			"versionNonce": 1862884376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Fibonacci 找 index",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "u5kQsXRG",
			"originalText": "Fibonacci 找 index",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "2XJHQ47t",
			"type": "rectangle",
			"x": -1169.5,
			"y": -125,
			"width": 248,
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
			"seed": 517344438,
			"version": 2,
			"versionNonce": 1708921192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fZM3DPrJ"
				},
				{
					"type": "arrow",
					"id": "tfJ2eFGm"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "fZM3DPrJ",
			"type": "text",
			"x": -1157.5,
			"y": -118,
			"width": 224,
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
			"seed": 1451098283,
			"version": 2,
			"versionNonce": 45488408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A7：6765 是第 20 項 → 20",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2XJHQ47t",
			"originalText": "A7：6765 是第 20 項 → 20",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "zLTDq93i",
			"type": "rectangle",
			"x": -1151.5,
			"y": -77,
			"width": 230,
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
			"seed": 122632840,
			"version": 2,
			"versionNonce": 1042654312,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qicKyjLN"
				},
				{
					"type": "arrow",
					"id": "EHjQgLt7"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "qicKyjLN",
			"type": "text",
			"x": -1139.5,
			"y": -70,
			"width": 206,
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
			"seed": 1487225430,
			"version": 2,
			"versionNonce": 1539520024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "不是 Fibonacci 數 → 印 −1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zLTDq93i",
			"originalText": "不是 Fibonacci 數 → 印 −1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "VDH6uuqL",
			"type": "rectangle",
			"x": -638.5,
			"y": 113.38,
			"width": 285,
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
			"seed": 1039392698,
			"version": 2,
			"versionNonce": 499439464,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rm7gb7V2"
				},
				{
					"type": "arrow",
					"id": "22ptDpy9"
				},
				{
					"type": "arrow",
					"id": "ZtbyP9xr"
				},
				{
					"type": "arrow",
					"id": "EzUHd8e4"
				},
				{
					"type": "arrow",
					"id": "mESp8GC8"
				},
				{
					"type": "arrow",
					"id": "epRQuqH5"
				},
				{
					"type": "arrow",
					"id": "fhHfhVmg"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "rm7gb7V2",
			"type": "text",
			"x": -618.5,
			"y": 125.38,
			"width": 245,
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
			"seed": 2035057850,
			"version": 2,
			"versionNonce": 790934296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "改錯題（B7，10 分）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VDH6uuqL",
			"originalText": "改錯題（B7，10 分）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "wSrZKZuf",
			"type": "rectangle",
			"x": -967.5,
			"y": 7.75,
			"width": 253,
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
			"seed": 136162612,
			"version": 2,
			"versionNonce": 1225108072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xiSt5gtP"
				},
				{
					"type": "arrow",
					"id": "ZtbyP9xr"
				},
				{
					"type": "arrow",
					"id": "Y3sk8uJA"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "xiSt5gtP",
			"type": "text",
			"x": -953.5,
			"y": 16.75,
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
			"seed": 477385754,
			"version": 2,
			"versionNonce": 1934528536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "while true: → while True:",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wSrZKZuf",
			"originalText": "while true: → while True:",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "gguVgYeY",
			"type": "rectangle",
			"x": -1364.5,
			"y": 1,
			"width": 337,
			"height": 54,
			"angle": 0,
			"strokeColor": "#6741d9",
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
			"seed": 1422542743,
			"version": 2,
			"versionNonce": 448011624,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8Jrfbd4h"
				},
				{
					"type": "arrow",
					"id": "Y3sk8uJA"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "8Jrfbd4h",
			"type": "text",
			"x": -1352.5,
			"y": 8,
			"width": 313,
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
			"seed": 1312620353,
			"version": 2,
			"versionNonce": 808766744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕Python 裡其實是 NameError，不是\nSyntaxError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gguVgYeY",
			"originalText": "〔C〕Python 裡其實是 NameError，不是\nSyntaxError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "F7jhpujg",
			"type": "rectangle",
			"x": -1126.5,
			"y": 69,
			"width": 412,
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
			"seed": 1120464564,
			"version": 2,
			"versionNonce": 874262632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bfBbdRJa"
				},
				{
					"type": "arrow",
					"id": "EzUHd8e4"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "bfBbdRJa",
			"type": "text",
			"x": -1112.5,
			"y": 78,
			"width": 384,
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
			"seed": 146538252,
			"version": 2,
			"versionNonce": 1330342424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "if b = Num: → if b == Num:（SyntaxError）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "F7jhpujg",
			"originalText": "if b = Num: → if b == Num:（SyntaxError）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "A5YQhbaU",
			"type": "rectangle",
			"x": -1124.5,
			"y": 123.5,
			"width": 410,
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
			"seed": 345749697,
			"version": 2,
			"versionNonce": 755622760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7atVzuWT"
				},
				{
					"type": "arrow",
					"id": "mESp8GC8"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "7atVzuWT",
			"type": "text",
			"x": -1110.5,
			"y": 132.5,
			"width": 382,
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
			"seed": 444174243,
			"version": 2,
			"versionNonce": 1803970328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "else: 縮排對齊 if／elif（IndentationError）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "A5YQhbaU",
			"originalText": "else: 縮排對齊 if／elif（IndentationError）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "SnPiNfKy",
			"type": "rectangle",
			"x": -1124.5,
			"y": 178,
			"width": 410,
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
			"seed": 1857151799,
			"version": 2,
			"versionNonce": 1137260136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aMFYpFjw"
				},
				{
					"type": "arrow",
					"id": "epRQuqH5"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "aMFYpFjw",
			"type": "text",
			"x": -1110.5,
			"y": 187,
			"width": 382,
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
			"seed": 1174297943,
			"version": 2,
			"versionNonce": 559531032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "有任何 syntax error，整支程式一行都不會跑",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SnPiNfKy",
			"originalText": "有任何 syntax error，整支程式一行都不會跑",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "p7hfmATB",
			"type": "rectangle",
			"x": -870.5,
			"y": 232.5,
			"width": 156,
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
			"seed": 149313149,
			"version": 2,
			"versionNonce": 220604776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sBRbYFWh"
				},
				{
					"type": "arrow",
					"id": "fhHfhVmg"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "sBRbYFWh",
			"type": "text",
			"x": -856.5,
			"y": 241.5,
			"width": 128,
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
			"seed": 1068054356,
			"version": 2,
			"versionNonce": 1589215512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "改好後輸出 20",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "p7hfmATB",
			"originalText": "改好後輸出 20",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "m9g5CZhW",
			"type": "rectangle",
			"x": -529.5,
			"y": 337.5,
			"width": 176,
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
			"seed": 929675772,
			"version": 2,
			"versionNonce": 611105896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3XBjHZR7"
				},
				{
					"type": "arrow",
					"id": "ymDmsKhC"
				},
				{
					"type": "arrow",
					"id": "BzpxVTNt"
				},
				{
					"type": "arrow",
					"id": "vtzeWCVw"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "3XBjHZR7",
			"type": "text",
			"x": -509.5,
			"y": 349.5,
			"width": 136,
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
			"seed": 108169278,
			"version": 2,
			"versionNonce": 857316888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "B8（5 分）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "m9g5CZhW",
			"originalText": "B8（5 分）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "zyXnjCqK",
			"type": "rectangle",
			"x": -821.5,
			"y": 317,
			"width": 216,
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
			"seed": 1472507871,
			"version": 2,
			"versionNonce": 1533603688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sahAZdGj"
				},
				{
					"type": "arrow",
					"id": "BzpxVTNt"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "sahAZdGj",
			"type": "text",
			"x": -807.5,
			"y": 326,
			"width": 188,
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
			"seed": 2035952251,
			"version": 2,
			"versionNonce": 527309592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "寫出兩位授課老師姓名",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zyXnjCqK",
			"originalText": "寫出兩位授課老師姓名",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "T757jxRH",
			"type": "rectangle",
			"x": -853.5,
			"y": 371.5,
			"width": 248,
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
			"seed": 8524884,
			"version": 2,
			"versionNonce": 1785119336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AknPQVWi"
				},
				{
					"type": "arrow",
					"id": "vtzeWCVw"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "AknPQVWi",
			"type": "text",
			"x": -839.5,
			"y": 380.5,
			"width": 220,
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
			"seed": 1261379641,
			"version": 2,
			"versionNonce": 1714092056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "錯字不計分，對 1 個 2 分",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "T757jxRH",
			"originalText": "錯字不計分，對 1 個 2 分",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "DpJu3rxA",
			"type": "rectangle",
			"x": -571.5,
			"y": 585.5,
			"width": 218,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fcc2d7",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1681687305,
			"version": 2,
			"versionNonce": 540161384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uExMm2iZ"
				},
				{
					"type": "arrow",
					"id": "y8f7UTGe"
				},
				{
					"type": "arrow",
					"id": "BKVcrkjV"
				},
				{
					"type": "arrow",
					"id": "D5MFXHh7"
				},
				{
					"type": "arrow",
					"id": "7enGUjA8"
				},
				{
					"type": "arrow",
					"id": "Zj5FumUP"
				},
				{
					"type": "arrow",
					"id": "iFbxT5ha"
				},
				{
					"type": "arrow",
					"id": "DbhPDdqv"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "uExMm2iZ",
			"type": "text",
			"x": -551.5,
			"y": 597.5,
			"width": 178,
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
			"seed": 1895383828,
			"version": 2,
			"versionNonce": 1531196696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "〔C〕解題 SOP",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DpJu3rxA",
			"originalText": "〔C〕解題 SOP",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "gRuB3ZZJ",
			"type": "rectangle",
			"x": -937.5,
			"y": 456,
			"width": 290,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 735002363,
			"version": 2,
			"versionNonce": 303515752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QLkkdaaW"
				},
				{
					"type": "arrow",
					"id": "BKVcrkjV"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "QLkkdaaW",
			"type": "text",
			"x": -923.5,
			"y": 465,
			"width": 262,
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
			"seed": 156659322,
			"version": 2,
			"versionNonce": 875418136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "畫追蹤表：每一輪寫下所有變數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gRuB3ZZJ",
			"originalText": "畫追蹤表：每一輪寫下所有變數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "ShCrwF7X",
			"type": "rectangle",
			"x": -1005.5,
			"y": 510.5,
			"width": 358,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 842979072,
			"version": 2,
			"versionNonce": 1273101160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3PpJcHqn"
				},
				{
					"type": "arrow",
					"id": "D5MFXHh7"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "3PpJcHqn",
			"type": "text",
			"x": -991.5,
			"y": 519.5,
			"width": 330,
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
			"seed": 2130808215,
			"version": 2,
			"versionNonce": 1474023192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "盯 end、sep：有沒有換行、有沒有空白",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ShCrwF7X",
			"originalText": "盯 end、sep：有沒有換行、有沒有空白",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "dMDwEpUH",
			"type": "rectangle",
			"x": -921.5,
			"y": 565,
			"width": 274,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1415652566,
			"version": 2,
			"versionNonce": 2145275496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8kbEvc8w"
				},
				{
					"type": "arrow",
					"id": "7enGUjA8"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "8kbEvc8w",
			"type": "text",
			"x": -907.5,
			"y": 574,
			"width": 246,
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
			"seed": 130810905,
			"version": 2,
			"versionNonce": 784477208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "/ 一定是 float；// 往下取整",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dMDwEpUH",
			"originalText": "/ 一定是 float；// 往下取整",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "Z5nx6kRr",
			"type": "rectangle",
			"x": -1006.5,
			"y": 619.5,
			"width": 359,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 60489445,
			"version": 2,
			"versionNonce": 920142184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "b4N4X6RV"
				},
				{
					"type": "arrow",
					"id": "Zj5FumUP"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "b4N4X6RV",
			"type": "text",
			"x": -992.5,
			"y": 628.5,
			"width": 331,
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
			"seed": 387178539,
			"version": 2,
			"versionNonce": 1926555928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "字串 × 整數＝重複；字串 + 字串＝串接",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Z5nx6kRr",
			"originalText": "字串 × 整數＝重複；字串 + 字串＝串接",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "diPEjcUw",
			"type": "rectangle",
			"x": -962.5,
			"y": 674,
			"width": 315,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2064850516,
			"version": 2,
			"versionNonce": 1823848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FG2sezyU"
				},
				{
					"type": "arrow",
					"id": "iFbxT5ha"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "FG2sezyU",
			"type": "text",
			"x": -948.5,
			"y": 683,
			"width": 287,
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
			"seed": 886802136,
			"version": 2,
			"versionNonce": 2139620888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "while True：找出每條 break 路徑",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "diPEjcUw",
			"originalText": "while True：找出每條 break 路徑",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "3UhYH6xT",
			"type": "rectangle",
			"x": -1092.5,
			"y": 728.5,
			"width": 445,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff0f6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1026783194,
			"version": 2,
			"versionNonce": 561317736,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7ckZVLbq"
				},
				{
					"type": "arrow",
					"id": "DbhPDdqv"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "7ckZVLbq",
			"type": "text",
			"x": -1078.5,
			"y": 737.5,
			"width": 417,
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
			"seed": 1455355637,
			"version": 2,
			"versionNonce": 567247640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "是非題：抓絕對詞（Any、all、exactly、should）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3UhYH6xT",
			"originalText": "是非題：抓絕對詞（Any、all、exactly、should）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "j2t4wBDH",
			"type": "text",
			"x": -1621.5,
			"y": -1003.5,
			"width": 992,
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
			"seed": 1805362559,
			"version": 2,
			"versionNonce": 1194318440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 6｜考古題：Midterm 題型與考點",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 6｜考古題：Midterm 題型與考點",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2W"
		},
		{
			"id": "aq7CZx8F",
			"type": "text",
			"x": -1621.5,
			"y": -941.5,
			"width": 741,
			"height": 22.5,
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
			"seed": 921841378,
			"version": 2,
			"versionNonce": 1746886680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Midterm 考古題（考古題 A、B）。已拿掉「新講義沒教的舊考點」補充。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Midterm 考古題（考古題 A、B）。已拿掉「新講義沒教的舊考點」補充。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "2kUQvRYc",
			"type": "rectangle",
			"x": -1621.5,
			"y": -897,
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
			"seed": 887219928,
			"version": 2,
			"versionNonce": 874007912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "d8JqhFdH"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "d8JqhFdH",
			"type": "text",
			"x": -1607.5,
			"y": -888,
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
			"seed": 630737155,
			"version": 2,
			"versionNonce": 1919655192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2kUQvRYc",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "MW5FEVWD",
			"type": "rectangle",
			"x": -1477.5,
			"y": -897,
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
			"seed": 1363172979,
			"version": 2,
			"versionNonce": 1903845480,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EMsweLWV"
				}
			],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "EMsweLWV",
			"type": "text",
			"x": -1463.5,
			"y": -888,
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
			"seed": 2071861710,
			"version": 2,
			"versionNonce": 1109932568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858152414,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕Claude 補充（投影片與講義沒有）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MW5FEVWD",
			"originalText": "〔C〕Claude 補充（投影片與講義沒有）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
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