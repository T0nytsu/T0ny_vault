---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "Claude 整理（考前速查）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
〔C〕考前速查
易錯陷阱與必背輸出 ^mqKdSnMd

型態與運算 ^XehU9Sdt

"65" + 1 → TypeError；"3" + "5" → 35；"3" * 5
→ 33333 ^fradP6Eh

/ 一定 float：45 / 60 → 0.75；0 * 9 / 5 + 30
→ 30.0 ^CmnbKHFQ

// floor：45 // 60 → 0；-7 // 3 → −3 ^amKjSsXR

% 餘數：83 % 60 → 23 ^sdqmwQTr

** 次方、右結合：2 ** 3 ** 2 → 512；-3 ** 2
→ −9 ^pPReuSP7

^ 是 XOR：1 ^ 10 → 11；2 ^ 3 → 1 ^ZKGVmiub

int(12.9) → 12；int(-1.7) → −1（向零） ^sdBBuVDY

int("12.5")、int("30.0") → ValueError ^hMgbTQPN

round(2.5) → 2；round(3.5) → 4 ^Hitrxdke

0.1 + 0.2 → 0.30000000000000004 ^vYFcapNd

print ^3Zwfnevh

print() 回傳 None ^dssBKa39

sep 預設一個空白；end 預設換行 ^J6hxbXyT

print("A", "B", sep="") → AB ^qBxRWbRD

f"{x:.2f}" 產生字串；四捨五入只影響顯示 ^GrqEGumX

名稱與指派 ^9GZU67ct

b = a 不會追蹤 a 之後的改變 ^fxmLzDt4

存起來的結果不會重算（miles、time_ok） ^FnHR8gfH

a, b = b, a + b：右邊先算完 ^AdTmyxHB

字串不可變：s.replace(...) 要再指派；s[0] = "c" →
TypeError ^ESvr6VFz

條件 ^5zZL4z8D

第一個為真的分支勝出 → 窄條件放前面 ^xn9QExGr

x == 30 or 60 → 永遠 truthy ^em8yFBhV

and／or 回傳運算元：0 or 7 → 7 ^UKHQZSDP

短路：and 左邊 False 就不算右邊 ^uh3neM2E

"9" > "30" → True（字串比順序） ^WGMRYEjj

bool("False") → True ^yDMYKkzS

迴圈 ^t95UhWu2

range 含頭不含尾；step 0 → ValueError；方向不
合 → 空 ^ZmsUMcpm

初始化放迴圈外 ^xXLjCQKy

continue 跳過更新 → 無窮迴圈 ^NLJ8YtWR

break 只跳出最內層 ^xQgUj8d2

for-else：沒 break 才執行 ^8q4L894y

while True 一定要有 break 路徑 ^DTkxCCKP

字串 ^hLVFuvmt

索引越界 → IndexError；切片越界 → 不報錯 ^fdcvM2jt

find 找不到 → −1（不要當 bool 用） ^Yjng6Zpy

count 不重疊 ^dApuK3M4

strip 只去兩端；strip("km") 是字元集合 ^CLrxZfQs

split(",") 保留空欄位；split() 依空白切 ^d6BSMdT3

len 是碼位數，不是 bytes，也不是看到的字數 ^C4f6Gy2C

錯誤類型 ^6Bg3Ti63

SyntaxError：缺冒號、括號沒關、= 當 == ^777VZFDk

IndentationError：縮排對不齊（SyntaxError 的
一種） ^4MavLUQU

NameError：名稱沒定義（hello、true） ^xyGsGWzF

TypeError："65" + 1、"30" > 0、s[0] = "c" ^z2tMjWMv

ValueError：int("12.5")、range(0, 5, 0) ^EUm5aazp

ZeroDivisionError：3 / 0 ^uR9QJxHT

IndexError："Campus"[6] ^kMnpQT49

Logic error：沒有錯誤訊息，但結果不符規格 ^F4AP7e2T

PROG1 期中心智圖 7｜〔C〕考前速查：易錯陷阱與必背輸出 ^CXezwpXK

整張是 Claude 整理的考前速查，不是投影片或講義原文。 ^mSjgLukL

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "ZT4ZLLqx",
			"type": "arrow",
			"x": 200,
			"y": -0.0,
			"width": 150,
			"height": 432.12,
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
			"seed": 1556313709,
			"version": 2,
			"versionNonce": 2132939624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-432.12
				],
				[
					150,
					-432.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "93hhAArF",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 273.38,
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
			"seed": 1661504099,
			"version": 2,
			"versionNonce": 172570392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-273.38
				],
				[
					76,
					-273.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TDuuqSbx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "EjjFZKNH",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 196.38,
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
			"seed": 959199881,
			"version": 2,
			"versionNonce": 56321640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-196.38
				],
				[
					76,
					-196.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "u2Dt8cAt",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "yUA28eVx",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 130.63,
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
			"seed": 378931939,
			"version": 2,
			"versionNonce": 2135069720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-130.63
				],
				[
					76,
					-130.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "m4Gnhrez",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "pbHwkXCr",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 76.13,
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
			"seed": 392161870,
			"version": 2,
			"versionNonce": 2062702952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-76.13
				],
				[
					76,
					-76.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "p9Mu9g62",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "93eYdg7s",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 10.38,
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
			"seed": 1268485712,
			"version": 2,
			"versionNonce": 654856472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-10.38
				],
				[
					76,
					-10.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4dLhFF4B",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "GxWbShLb",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 55.37,
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
			"seed": 1979943686,
			"version": 2,
			"versionNonce": 1764945000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					55.37
				],
				[
					76,
					55.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "b8LHtE8s",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "iqGYTLpv",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 109.87,
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
			"seed": 1032848724,
			"version": 2,
			"versionNonce": 688811544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					109.87
				],
				[
					76,
					109.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "q3vgW9YE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "WkAd3fzM",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 164.37,
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
			"seed": 1192293008,
			"version": 2,
			"versionNonce": 132718440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					164.37
				],
				[
					76,
					164.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2WQiCf8H",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "tkVZSvrg",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 218.87,
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
			"seed": 1270836129,
			"version": 2,
			"versionNonce": 508095256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					218.87
				],
				[
					76,
					218.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "G9JnPHuA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "iGnz8aeR",
			"type": "arrow",
			"x": 516,
			"y": -432.12,
			"width": 76,
			"height": 273.37,
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
			"seed": 1368476945,
			"version": 2,
			"versionNonce": 2002842216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					273.37
				],
				[
					76,
					273.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uYRccD7n",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "K9arZhNp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "pfXxrAiB",
			"type": "arrow",
			"x": 200,
			"y": -0.0,
			"width": 150,
			"height": 7.5,
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
			"seed": 1479814259,
			"version": 2,
			"versionNonce": 1630259224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					7.5
				],
				[
					150,
					7.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zRiFdv4D",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "DpexsM3x",
			"type": "arrow",
			"x": 449,
			"y": 7.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 1370631315,
			"version": 2,
			"versionNonce": 1852204392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-81.75
				],
				[
					76,
					-81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zRiFdv4D",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3ExcuEkv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "3KcVadWR",
			"type": "arrow",
			"x": 449,
			"y": 7.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 1881549541,
			"version": 2,
			"versionNonce": 1571489048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-27.25
				],
				[
					76,
					-27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zRiFdv4D",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6BZ5Tben",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "VMFynvHh",
			"type": "arrow",
			"x": 449,
			"y": 7.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 9659109,
			"version": 2,
			"versionNonce": 1782937704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					27.25
				],
				[
					76,
					27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zRiFdv4D",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RKpzcP5H",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "MeepKA4x",
			"type": "arrow",
			"x": 449,
			"y": 7.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 854070008,
			"version": 2,
			"versionNonce": 1631232536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					81.75
				],
				[
					76,
					81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zRiFdv4D",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7Rtb9nAR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "wjWkRTKw",
			"type": "arrow",
			"x": 200,
			"y": -0.0,
			"width": 150,
			"height": 261.12,
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
			"seed": 798389850,
			"version": 2,
			"versionNonce": 1590307688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					261.12
				],
				[
					150,
					261.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bPTuAHR7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "3vWRCPwQ",
			"type": "arrow",
			"x": 516,
			"y": 261.12,
			"width": 76,
			"height": 87.37,
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
			"seed": 1646192121,
			"version": 2,
			"versionNonce": 1791926040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-87.37
				],
				[
					76,
					-87.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bPTuAHR7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "F3kh6CXc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "ZEgg5NSd",
			"type": "arrow",
			"x": 516,
			"y": 261.12,
			"width": 76,
			"height": 32.87,
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
			"seed": 646102855,
			"version": 2,
			"versionNonce": 1715502696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-32.87
				],
				[
					76,
					-32.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bPTuAHR7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "T8afMqvx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "avk2cbyW",
			"type": "arrow",
			"x": 516,
			"y": 261.12,
			"width": 76,
			"height": 21.63,
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
			"seed": 1008464512,
			"version": 2,
			"versionNonce": 2061171736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					21.63
				],
				[
					76,
					21.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bPTuAHR7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "s8EHEkzq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "aecECMT7",
			"type": "arrow",
			"x": 516,
			"y": 261.12,
			"width": 76,
			"height": 87.38,
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
			"seed": 1252370167,
			"version": 2,
			"versionNonce": 1903456616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					87.38
				],
				[
					76,
					87.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bPTuAHR7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tx9NNib7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "rR9hmYzs",
			"type": "arrow",
			"x": 200,
			"y": -0.0,
			"width": 150,
			"height": 580.5,
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
			"seed": 2079482993,
			"version": 2,
			"versionNonce": 1666431256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					580.5
				],
				[
					150,
					580.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "EMwMv4tU",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 136.25,
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
			"seed": 1384328527,
			"version": 2,
			"versionNonce": 2008155240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-136.25
				],
				[
					76,
					-136.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KXTRq8KB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "LqRMLU4d",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 1358543743,
			"version": 2,
			"versionNonce": 397202968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-81.75
				],
				[
					76,
					-81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SxDWAP6W",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "RyKfy9KV",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 1117598215,
			"version": 2,
			"versionNonce": 650458984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-27.25
				],
				[
					76,
					-27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KUkp5FPD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "vbmYtmMe",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 27.25,
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
			"seed": 638121814,
			"version": 2,
			"versionNonce": 2094682904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					27.25
				],
				[
					76,
					27.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Z5Tj5PrZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "52kFex2u",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 81.75,
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
			"seed": 122105150,
			"version": 2,
			"versionNonce": 318376552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					81.75
				],
				[
					76,
					81.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rTpb79dc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "ChLJYiPU",
			"type": "arrow",
			"x": 442,
			"y": 580.5,
			"width": 76,
			"height": 136.25,
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
			"seed": 1065878517,
			"version": 2,
			"versionNonce": 961556504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					136.25
				],
				[
					76,
					136.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "QBZmZuYz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SSBf9GhG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "QWt8yXcX",
			"type": "arrow",
			"x": -200,
			"y": -0.0,
			"width": 150,
			"height": 417.12,
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
			"seed": 1583587933,
			"version": 2,
			"versionNonce": 1729920360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-417.12
				],
				[
					-150,
					-417.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "8K76HjEb",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 141.88,
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
			"seed": 1612593676,
			"version": 2,
			"versionNonce": 84045080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-141.88
				],
				[
					-76,
					-141.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "M6XFYphA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "WaHyLEh7",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 76.13,
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
			"seed": 765336540,
			"version": 2,
			"versionNonce": 343445608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-76.13
				],
				[
					-76,
					-76.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2W9fWWft",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "YWrRrgh2",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 21.63,
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
			"seed": 1676862271,
			"version": 2,
			"versionNonce": 2036664856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-21.63
				],
				[
					-76,
					-21.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Cid8J4TR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "PvDSLhTL",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 32.87,
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
			"seed": 2096291825,
			"version": 2,
			"versionNonce": 47858536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4QF8pDew",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "H6LUSDPS",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 87.37,
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
			"seed": 395193477,
			"version": 2,
			"versionNonce": 1634469656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					87.37
				],
				[
					-76,
					87.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fJvAYUJ9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "DUTaebqc",
			"type": "arrow",
			"x": -442,
			"y": -417.12,
			"width": 76,
			"height": 141.87,
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
			"seed": 1839279511,
			"version": 2,
			"versionNonce": 1083020904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					141.87
				],
				[
					-76,
					141.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "putPsmsx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tE5XdsEN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "RY6tZz5M",
			"type": "arrow",
			"x": -200,
			"y": -0.0,
			"width": 150,
			"height": 54.5,
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
			"seed": 1371099584,
			"version": 2,
			"versionNonce": 160130072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-54.5
				],
				[
					-150,
					-54.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "TAF7ZekG",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 1535867627,
			"version": 2,
			"versionNonce": 845056360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Taq8jYei",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "g8gz3mkz",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 1345829517,
			"version": 2,
			"versionNonce": 263659800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "a8mLvKcK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "7Nhs7UUd",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 202314876,
			"version": 2,
			"versionNonce": 1134107752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "e2QmiYsU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "xfGBNg8X",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 1866219924,
			"version": 2,
			"versionNonce": 862141976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3LGzu4QA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "VRFz5zpw",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 653446957,
			"version": 2,
			"versionNonce": 369708904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wdXFTrKT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "LXmYknBH",
			"type": "arrow",
			"x": -442,
			"y": -54.5,
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
			"seed": 632005772,
			"version": 2,
			"versionNonce": 629390104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "cz9SEDbG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2AeqqmU8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "cJrVDphB",
			"type": "arrow",
			"x": -200,
			"y": -0.0,
			"width": 150,
			"height": 368.25,
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
			"seed": 1122161658,
			"version": 2,
			"versionNonce": 838541928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					368.25
				],
				[
					-150,
					368.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "8c57QmvZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "PNzSTtrH",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 202,
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
			"seed": 1115852443,
			"version": 2,
			"versionNonce": 1485608984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-202
				],
				[
					-76,
					-202
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7desH3Jw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "JdAwRsyS",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 136.25,
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
			"seed": 575450469,
			"version": 2,
			"versionNonce": 909809000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YDwcGEa2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "j3hhZKj4",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 70.5,
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
			"seed": 218501612,
			"version": 2,
			"versionNonce": 1349637400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-70.5
				],
				[
					-76,
					-70.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "guBUi3Pr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "AXDnNSZ2",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 16,
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
			"seed": 1203881720,
			"version": 2,
			"versionNonce": 135506024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					-16
				],
				[
					-76,
					-16
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "h6J7fLTS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "Y4nkjB6r",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 38.5,
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
			"seed": 1221833849,
			"version": 2,
			"versionNonce": 1923576344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					38.5
				],
				[
					-76,
					38.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XuMEK2Q9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "GZGPLttf",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 93,
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
			"seed": 1802009052,
			"version": 2,
			"versionNonce": 55729000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					93
				],
				[
					-76,
					93
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ZTuCbTdu",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "gUTDT8WN",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 147.5,
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
			"seed": 951967802,
			"version": 2,
			"versionNonce": 1445031704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					147.5
				],
				[
					-76,
					147.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "E2YHxQPm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "LVmh7zBW",
			"type": "arrow",
			"x": -491,
			"y": 368.25,
			"width": 76,
			"height": 202,
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
			"seed": 1175738035,
			"version": 2,
			"versionNonce": 709013096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
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
					202
				],
				[
					-76,
					202
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vAWr4J2M",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eME2x2JB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "8c57QmvZ",
			"type": "rectangle",
			"x": -200,
			"y": -67,
			"width": 400,
			"height": 134,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#343a40",
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
			"seed": 1541656362,
			"version": 2,
			"versionNonce": 324258840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mqKdSnMd"
				},
				{
					"type": "arrow",
					"id": "ZT4ZLLqx"
				},
				{
					"type": "arrow",
					"id": "pfXxrAiB"
				},
				{
					"type": "arrow",
					"id": "wjWkRTKw"
				},
				{
					"type": "arrow",
					"id": "rR9hmYzs"
				},
				{
					"type": "arrow",
					"id": "QWt8yXcX"
				},
				{
					"type": "arrow",
					"id": "RY6tZz5M"
				},
				{
					"type": "arrow",
					"id": "cJrVDphB"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "ap"
		},
		{
			"id": "mqKdSnMd",
			"type": "text",
			"x": -168,
			"y": -45,
			"width": 336,
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
			"seed": 958535013,
			"version": 2,
			"versionNonce": 1437639016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "〔C〕考前速查\n易錯陷阱與必背輸出",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8c57QmvZ",
			"originalText": "〔C〕考前速查\n易錯陷阱與必背輸出",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "aq"
		},
		{
			"id": "uYRccD7n",
			"type": "rectangle",
			"x": 350,
			"y": -459.12,
			"width": 166,
			"height": 54,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "#a5d8ff",
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
			"seed": 518228632,
			"version": 2,
			"versionNonce": 338856216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XehU9Sdt"
				},
				{
					"type": "arrow",
					"id": "ZT4ZLLqx"
				},
				{
					"type": "arrow",
					"id": "93hhAArF"
				},
				{
					"type": "arrow",
					"id": "EjjFZKNH"
				},
				{
					"type": "arrow",
					"id": "yUA28eVx"
				},
				{
					"type": "arrow",
					"id": "pbHwkXCr"
				},
				{
					"type": "arrow",
					"id": "93eYdg7s"
				},
				{
					"type": "arrow",
					"id": "GxWbShLb"
				},
				{
					"type": "arrow",
					"id": "iqGYTLpv"
				},
				{
					"type": "arrow",
					"id": "WkAd3fzM"
				},
				{
					"type": "arrow",
					"id": "tkVZSvrg"
				},
				{
					"type": "arrow",
					"id": "iGnz8aeR"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "ar"
		},
		{
			"id": "XehU9Sdt",
			"type": "text",
			"x": 370,
			"y": -447.12,
			"width": 126,
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
			"seed": 2024548160,
			"version": 2,
			"versionNonce": 1692939368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "型態與運算",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uYRccD7n",
			"originalText": "型態與運算",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "as"
		},
		{
			"id": "TDuuqSbx",
			"type": "rectangle",
			"x": 592,
			"y": -737,
			"width": 454,
			"height": 63,
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
			"seed": 1225939163,
			"version": 2,
			"versionNonce": 1680975384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fradP6Eh"
				},
				{
					"type": "arrow",
					"id": "93hhAArF"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "at"
		},
		{
			"id": "fradP6Eh",
			"type": "text",
			"x": 606,
			"y": -728,
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
			"seed": 980100888,
			"version": 2,
			"versionNonce": 1840605032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "\"65\" + 1 → TypeError；\"3\" + \"5\" → 35；\"3\" * 5\n→ 33333",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TDuuqSbx",
			"originalText": "\"65\" + 1 → TypeError；\"3\" + \"5\" → 35；\"3\" * 5\n→ 33333",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "au"
		},
		{
			"id": "u2Dt8cAt",
			"type": "rectangle",
			"x": 592,
			"y": -660,
			"width": 453,
			"height": 63,
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
			"seed": 2070014261,
			"version": 2,
			"versionNonce": 4530968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CmnbKHFQ"
				},
				{
					"type": "arrow",
					"id": "EjjFZKNH"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "av"
		},
		{
			"id": "CmnbKHFQ",
			"type": "text",
			"x": 606,
			"y": -651,
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
			"seed": 1685161893,
			"version": 2,
			"versionNonce": 1818507880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "/ 一定 float：45 / 60 → 0.75；0 * 9 / 5 + 30\n→ 30.0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "u2Dt8cAt",
			"originalText": "/ 一定 float：45 / 60 → 0.75；0 * 9 / 5 + 30\n→ 30.0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "aw"
		},
		{
			"id": "m4Gnhrez",
			"type": "rectangle",
			"x": 592,
			"y": -583,
			"width": 375,
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
			"seed": 684499913,
			"version": 2,
			"versionNonce": 652279832,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "amKjSsXR"
				},
				{
					"type": "arrow",
					"id": "yUA28eVx"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "ax"
		},
		{
			"id": "amKjSsXR",
			"type": "text",
			"x": 606,
			"y": -574,
			"width": 347,
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
			"seed": 1999413959,
			"version": 2,
			"versionNonce": 1942007144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "// floor：45 // 60 → 0；-7 // 3 → −3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "m4Gnhrez",
			"originalText": "// floor：45 // 60 → 0；-7 // 3 → −3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "ay"
		},
		{
			"id": "p9Mu9g62",
			"type": "rectangle",
			"x": 592,
			"y": -528.5,
			"width": 248,
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
			"seed": 1716086910,
			"version": 2,
			"versionNonce": 670645528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sdqmwQTr"
				},
				{
					"type": "arrow",
					"id": "pbHwkXCr"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "az"
		},
		{
			"id": "sdqmwQTr",
			"type": "text",
			"x": 606,
			"y": -519.5,
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
			"seed": 2060917979,
			"version": 2,
			"versionNonce": 1561772136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "% 餘數：83 % 60 → 23",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "p9Mu9g62",
			"originalText": "% 餘數：83 % 60 → 23",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b00"
		},
		{
			"id": "4dLhFF4B",
			"type": "rectangle",
			"x": 592,
			"y": -474,
			"width": 443,
			"height": 63,
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
			"seed": 672120432,
			"version": 2,
			"versionNonce": 889313816,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pPReuSP7"
				},
				{
					"type": "arrow",
					"id": "93eYdg7s"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b01"
		},
		{
			"id": "pPReuSP7",
			"type": "text",
			"x": 606,
			"y": -465,
			"width": 415,
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
			"seed": 416644043,
			"version": 2,
			"versionNonce": 2016572264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "** 次方、右結合：2 ** 3 ** 2 → 512；-3 ** 2\n→ −9",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4dLhFF4B",
			"originalText": "** 次方、右結合：2 ** 3 ** 2 → 512；-3 ** 2\n→ −9",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b02"
		},
		{
			"id": "b8LHtE8s",
			"type": "rectangle",
			"x": 592,
			"y": -397,
			"width": 341,
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
			"seed": 2088856282,
			"version": 2,
			"versionNonce": 820959000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZKGVmiub"
				},
				{
					"type": "arrow",
					"id": "GxWbShLb"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b03"
		},
		{
			"id": "ZKGVmiub",
			"type": "text",
			"x": 606,
			"y": -388,
			"width": 313,
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
			"seed": 1672401023,
			"version": 2,
			"versionNonce": 996132456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "^ 是 XOR：1 ^ 10 → 11；2 ^ 3 → 1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "b8LHtE8s",
			"originalText": "^ 是 XOR：1 ^ 10 → 11；2 ^ 3 → 1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b04"
		},
		{
			"id": "q3vgW9YE",
			"type": "rectangle",
			"x": 592,
			"y": -342.5,
			"width": 376,
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
			"seed": 1020409386,
			"version": 2,
			"versionNonce": 3421208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sdBBuVDY"
				},
				{
					"type": "arrow",
					"id": "iqGYTLpv"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b05"
		},
		{
			"id": "sdBBuVDY",
			"type": "text",
			"x": 606,
			"y": -333.5,
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
			"seed": 298378600,
			"version": 2,
			"versionNonce": 1936374120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "int(12.9) → 12；int(-1.7) → −1（向零）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "q3vgW9YE",
			"originalText": "int(12.9) → 12；int(-1.7) → −1（向零）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b06"
		},
		{
			"id": "2WQiCf8H",
			"type": "rectangle",
			"x": 592,
			"y": -288,
			"width": 360,
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
			"seed": 325236329,
			"version": 2,
			"versionNonce": 1489367320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hMgbTQPN"
				},
				{
					"type": "arrow",
					"id": "WkAd3fzM"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b07"
		},
		{
			"id": "hMgbTQPN",
			"type": "text",
			"x": 606,
			"y": -279,
			"width": 332,
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
			"seed": 1148890639,
			"version": 2,
			"versionNonce": 1939819624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "int(\"12.5\")、int(\"30.0\") → ValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2WQiCf8H",
			"originalText": "int(\"12.5\")、int(\"30.0\") → ValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b08"
		},
		{
			"id": "G9JnPHuA",
			"type": "rectangle",
			"x": 592,
			"y": -233.5,
			"width": 328,
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
			"seed": 1548392717,
			"version": 2,
			"versionNonce": 303566360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Hitrxdke"
				},
				{
					"type": "arrow",
					"id": "tkVZSvrg"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b09"
		},
		{
			"id": "Hitrxdke",
			"type": "text",
			"x": 606,
			"y": -224.5,
			"width": 300,
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
			"seed": 2116538286,
			"version": 2,
			"versionNonce": 1170833256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "round(2.5) → 2；round(3.5) → 4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G9JnPHuA",
			"originalText": "round(2.5) → 2；round(3.5) → 4",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0A"
		},
		{
			"id": "K9arZhNp",
			"type": "rectangle",
			"x": 592,
			"y": -179,
			"width": 367,
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
			"seed": 714947920,
			"version": 2,
			"versionNonce": 1964935960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vYFcapNd"
				},
				{
					"type": "arrow",
					"id": "iGnz8aeR"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0B"
		},
		{
			"id": "vYFcapNd",
			"type": "text",
			"x": 606,
			"y": -170,
			"width": 339,
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
			"seed": 1522111760,
			"version": 2,
			"versionNonce": 1513443944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "0.1 + 0.2 → 0.30000000000000004",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "K9arZhNp",
			"originalText": "0.1 + 0.2 → 0.30000000000000004",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0C"
		},
		{
			"id": "zRiFdv4D",
			"type": "rectangle",
			"x": 350,
			"y": -19.5,
			"width": 99,
			"height": 54,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#b2f2bb",
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
			"seed": 1785387986,
			"version": 2,
			"versionNonce": 206399512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3Zwfnevh"
				},
				{
					"type": "arrow",
					"id": "pfXxrAiB"
				},
				{
					"type": "arrow",
					"id": "DpexsM3x"
				},
				{
					"type": "arrow",
					"id": "3KcVadWR"
				},
				{
					"type": "arrow",
					"id": "VMFynvHh"
				},
				{
					"type": "arrow",
					"id": "MeepKA4x"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0D"
		},
		{
			"id": "3Zwfnevh",
			"type": "text",
			"x": 370,
			"y": -7.5,
			"width": 59,
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
			"seed": 1668385231,
			"version": 2,
			"versionNonce": 934200680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "print",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zRiFdv4D",
			"originalText": "print",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0E"
		},
		{
			"id": "3ExcuEkv",
			"type": "rectangle",
			"x": 525,
			"y": -94.5,
			"width": 183,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
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
			"seed": 1714212126,
			"version": 2,
			"versionNonce": 1939383576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dssBKa39"
				},
				{
					"type": "arrow",
					"id": "DpexsM3x"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0F"
		},
		{
			"id": "dssBKa39",
			"type": "text",
			"x": 539,
			"y": -85.5,
			"width": 155,
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
			"seed": 365288909,
			"version": 2,
			"versionNonce": 729929832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "print() 回傳 None",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3ExcuEkv",
			"originalText": "print() 回傳 None",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0G"
		},
		{
			"id": "6BZ5Tben",
			"type": "rectangle",
			"x": 525,
			"y": -40,
			"width": 310,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
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
			"seed": 1033216678,
			"version": 2,
			"versionNonce": 678707736,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J6hxbXyT"
				},
				{
					"type": "arrow",
					"id": "3KcVadWR"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0H"
		},
		{
			"id": "J6hxbXyT",
			"type": "text",
			"x": 539,
			"y": -31,
			"width": 282,
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
			"seed": 1495280547,
			"version": 2,
			"versionNonce": 2038074216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "sep 預設一個空白；end 預設換行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6BZ5Tben",
			"originalText": "sep 預設一個空白；end 預設換行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0I"
		},
		{
			"id": "RKpzcP5H",
			"type": "rectangle",
			"x": 525,
			"y": 14.5,
			"width": 276,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
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
			"seed": 842842039,
			"version": 2,
			"versionNonce": 1507082008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qBxRWbRD"
				},
				{
					"type": "arrow",
					"id": "VMFynvHh"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0J"
		},
		{
			"id": "qBxRWbRD",
			"type": "text",
			"x": 539,
			"y": 23.5,
			"width": 248,
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
			"seed": 596425890,
			"version": 2,
			"versionNonce": 199548520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "print(\"A\", \"B\", sep=\"\") → AB",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RKpzcP5H",
			"originalText": "print(\"A\", \"B\", sep=\"\") → AB",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0K"
		},
		{
			"id": "7Rtb9nAR",
			"type": "rectangle",
			"x": 525,
			"y": 69,
			"width": 383,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ebfbee",
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
			"seed": 1809913557,
			"version": 2,
			"versionNonce": 942447640,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GrqEGumX"
				},
				{
					"type": "arrow",
					"id": "MeepKA4x"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0L"
		},
		{
			"id": "GrqEGumX",
			"type": "text",
			"x": 539,
			"y": 78,
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
			"seed": 1905966011,
			"version": 2,
			"versionNonce": 596431208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "f\"{x:.2f}\" 產生字串；四捨五入只影響顯示",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7Rtb9nAR",
			"originalText": "f\"{x:.2f}\" 產生字串；四捨五入只影響顯示",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0M"
		},
		{
			"id": "bPTuAHR7",
			"type": "rectangle",
			"x": 350,
			"y": 234.12,
			"width": 166,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#ffd8a8",
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
			"seed": 1326896019,
			"version": 2,
			"versionNonce": 1165056280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9GZU67ct"
				},
				{
					"type": "arrow",
					"id": "wjWkRTKw"
				},
				{
					"type": "arrow",
					"id": "3vWRCPwQ"
				},
				{
					"type": "arrow",
					"id": "ZEgg5NSd"
				},
				{
					"type": "arrow",
					"id": "avk2cbyW"
				},
				{
					"type": "arrow",
					"id": "aecECMT7"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0N"
		},
		{
			"id": "9GZU67ct",
			"type": "text",
			"x": 370,
			"y": 246.12,
			"width": 126,
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
			"seed": 1823856218,
			"version": 2,
			"versionNonce": 129918056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "名稱與指派",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bPTuAHR7",
			"originalText": "名稱與指派",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0O"
		},
		{
			"id": "F3kh6CXc",
			"type": "rectangle",
			"x": 592,
			"y": 153.5,
			"width": 276,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
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
			"seed": 1756532320,
			"version": 2,
			"versionNonce": 622229016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fxmLzDt4"
				},
				{
					"type": "arrow",
					"id": "3vWRCPwQ"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0P"
		},
		{
			"id": "fxmLzDt4",
			"type": "text",
			"x": 606,
			"y": 162.5,
			"width": 248,
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
			"seed": 1458771331,
			"version": 2,
			"versionNonce": 910530408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "b = a 不會追蹤 a 之後的改變",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "F3kh6CXc",
			"originalText": "b = a 不會追蹤 a 之後的改變",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0Q"
		},
		{
			"id": "T8afMqvx",
			"type": "rectangle",
			"x": 592,
			"y": 208,
			"width": 383,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
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
			"seed": 1345966912,
			"version": 2,
			"versionNonce": 1812984600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FnHR8gfH"
				},
				{
					"type": "arrow",
					"id": "ZEgg5NSd"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0R"
		},
		{
			"id": "FnHR8gfH",
			"type": "text",
			"x": 606,
			"y": 217,
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
			"seed": 1706552564,
			"version": 2,
			"versionNonce": 326003304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "存起來的結果不會重算（miles、time_ok）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "T8afMqvx",
			"originalText": "存起來的結果不會重算（miles、time_ok）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0S"
		},
		{
			"id": "s8EHEkzq",
			"type": "rectangle",
			"x": 592,
			"y": 262.5,
			"width": 268,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
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
			"seed": 1232106460,
			"version": 2,
			"versionNonce": 1892798488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AdTmyxHB"
				},
				{
					"type": "arrow",
					"id": "avk2cbyW"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0T"
		},
		{
			"id": "AdTmyxHB",
			"type": "text",
			"x": 606,
			"y": 271.5,
			"width": 240,
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
			"seed": 1123540987,
			"version": 2,
			"versionNonce": 436526440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "a, b = b, a + b：右邊先算完",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "s8EHEkzq",
			"originalText": "a, b = b, a + b：右邊先算完",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0U"
		},
		{
			"id": "tx9NNib7",
			"type": "rectangle",
			"x": 592,
			"y": 317,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
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
			"seed": 21777847,
			"version": 2,
			"versionNonce": 458231064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ESvr6VFz"
				},
				{
					"type": "arrow",
					"id": "aecECMT7"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0V"
		},
		{
			"id": "ESvr6VFz",
			"type": "text",
			"x": 606,
			"y": 326,
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
			"seed": 2088951565,
			"version": 2,
			"versionNonce": 190115944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "字串不可變：s.replace(...) 要再指派；s[0] = \"c\" →\nTypeError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tx9NNib7",
			"originalText": "字串不可變：s.replace(...) 要再指派；s[0] = \"c\" →\nTypeError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0W"
		},
		{
			"id": "QBZmZuYz",
			"type": "rectangle",
			"x": 350,
			"y": 553.5,
			"width": 92,
			"height": 54,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#d0bfff",
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
			"seed": 1089795011,
			"version": 2,
			"versionNonce": 889104920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5zZL4z8D"
				},
				{
					"type": "arrow",
					"id": "rR9hmYzs"
				},
				{
					"type": "arrow",
					"id": "EMwMv4tU"
				},
				{
					"type": "arrow",
					"id": "LqRMLU4d"
				},
				{
					"type": "arrow",
					"id": "RyKfy9KV"
				},
				{
					"type": "arrow",
					"id": "vbmYtmMe"
				},
				{
					"type": "arrow",
					"id": "52kFex2u"
				},
				{
					"type": "arrow",
					"id": "ChLJYiPU"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0X"
		},
		{
			"id": "5zZL4z8D",
			"type": "text",
			"x": 370,
			"y": 565.5,
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
			"seed": 1597356207,
			"version": 2,
			"versionNonce": 522888040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "條件",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QBZmZuYz",
			"originalText": "條件",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0Y"
		},
		{
			"id": "KXTRq8KB",
			"type": "rectangle",
			"x": 518,
			"y": 424,
			"width": 361,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 1188542851,
			"version": 2,
			"versionNonce": 953263896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xn9QExGr"
				},
				{
					"type": "arrow",
					"id": "EMwMv4tU"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0Z"
		},
		{
			"id": "xn9QExGr",
			"type": "text",
			"x": 532,
			"y": 433,
			"width": 333,
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
			"seed": 1814703627,
			"version": 2,
			"versionNonce": 869398120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "第一個為真的分支勝出 → 窄條件放前面",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KXTRq8KB",
			"originalText": "第一個為真的分支勝出 → 窄條件放前面",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0a"
		},
		{
			"id": "SxDWAP6W",
			"type": "rectangle",
			"x": 518,
			"y": 478.5,
			"width": 295,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 836129133,
			"version": 2,
			"versionNonce": 591201304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "em8yFBhV"
				},
				{
					"type": "arrow",
					"id": "LqRMLU4d"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0b"
		},
		{
			"id": "em8yFBhV",
			"type": "text",
			"x": 532,
			"y": 487.5,
			"width": 267,
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
			"seed": 2003991009,
			"version": 2,
			"versionNonce": 2115430760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "x == 30 or 60 → 永遠 truthy",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SxDWAP6W",
			"originalText": "x == 30 or 60 → 永遠 truthy",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0c"
		},
		{
			"id": "KUkp5FPD",
			"type": "rectangle",
			"x": 518,
			"y": 533,
			"width": 318,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 129552875,
			"version": 2,
			"versionNonce": 1110753560,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UKHQZSDP"
				},
				{
					"type": "arrow",
					"id": "RyKfy9KV"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0d"
		},
		{
			"id": "UKHQZSDP",
			"type": "text",
			"x": 532,
			"y": 542,
			"width": 290,
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
			"seed": 870346236,
			"version": 2,
			"versionNonce": 960855144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "and／or 回傳運算元：0 or 7 → 7",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KUkp5FPD",
			"originalText": "and／or 回傳運算元：0 or 7 → 7",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0e"
		},
		{
			"id": "Z5Tj5PrZ",
			"type": "rectangle",
			"x": 518,
			"y": 587.5,
			"width": 316,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 1705772952,
			"version": 2,
			"versionNonce": 86826520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uh3neM2E"
				},
				{
					"type": "arrow",
					"id": "vbmYtmMe"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0f"
		},
		{
			"id": "uh3neM2E",
			"type": "text",
			"x": 532,
			"y": 596.5,
			"width": 288,
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
			"seed": 2009691367,
			"version": 2,
			"versionNonce": 1462349672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "短路：and 左邊 False 就不算右邊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Z5Tj5PrZ",
			"originalText": "短路：and 左邊 False 就不算右邊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0g"
		},
		{
			"id": "rTpb79dc",
			"type": "rectangle",
			"x": 518,
			"y": 642,
			"width": 324,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 1556514826,
			"version": 2,
			"versionNonce": 1293507352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WGMRYEjj"
				},
				{
					"type": "arrow",
					"id": "52kFex2u"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0h"
		},
		{
			"id": "WGMRYEjj",
			"type": "text",
			"x": 532,
			"y": 651,
			"width": 296,
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
			"seed": 247655275,
			"version": 2,
			"versionNonce": 806322792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "\"9\" > \"30\" → True（字串比順序）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rTpb79dc",
			"originalText": "\"9\" > \"30\" → True（字串比順序）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0i"
		},
		{
			"id": "SSBf9GhG",
			"type": "rectangle",
			"x": 518,
			"y": 696.5,
			"width": 218,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
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
			"seed": 1565872010,
			"version": 2,
			"versionNonce": 1013856280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yDMYKkzS"
				},
				{
					"type": "arrow",
					"id": "ChLJYiPU"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0j"
		},
		{
			"id": "yDMYKkzS",
			"type": "text",
			"x": 532,
			"y": 705.5,
			"width": 190,
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
			"seed": 1625424230,
			"version": 2,
			"versionNonce": 851637608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "bool(\"False\") → True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SSBf9GhG",
			"originalText": "bool(\"False\") → True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0k"
		},
		{
			"id": "putPsmsx",
			"type": "rectangle",
			"x": -442,
			"y": -444.12,
			"width": 92,
			"height": 54,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#99e9f2",
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
			"seed": 1366435896,
			"version": 2,
			"versionNonce": 119502104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "t95UhWu2"
				},
				{
					"type": "arrow",
					"id": "QWt8yXcX"
				},
				{
					"type": "arrow",
					"id": "8K76HjEb"
				},
				{
					"type": "arrow",
					"id": "WaHyLEh7"
				},
				{
					"type": "arrow",
					"id": "YWrRrgh2"
				},
				{
					"type": "arrow",
					"id": "PvDSLhTL"
				},
				{
					"type": "arrow",
					"id": "H6LUSDPS"
				},
				{
					"type": "arrow",
					"id": "DUTaebqc"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0l"
		},
		{
			"id": "t95UhWu2",
			"type": "text",
			"x": -422,
			"y": -432.12,
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
			"seed": 752896003,
			"version": 2,
			"versionNonce": 344983656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "迴圈",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "putPsmsx",
			"originalText": "迴圈",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0m"
		},
		{
			"id": "M6XFYphA",
			"type": "rectangle",
			"x": -974,
			"y": -590.5,
			"width": 456,
			"height": 63,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 1929707551,
			"version": 2,
			"versionNonce": 1117852184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZmsUMcpm"
				},
				{
					"type": "arrow",
					"id": "8K76HjEb"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0n"
		},
		{
			"id": "ZmsUMcpm",
			"type": "text",
			"x": -960,
			"y": -581.5,
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
			"seed": 146701222,
			"version": 2,
			"versionNonce": 21150568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "range 含頭不含尾；step 0 → ValueError；方向不\n合 → 空",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M6XFYphA",
			"originalText": "range 含頭不含尾；step 0 → ValueError；方向不\n合 → 空",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0o"
		},
		{
			"id": "2W9fWWft",
			"type": "rectangle",
			"x": -678,
			"y": -513.5,
			"width": 160,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 1935385462,
			"version": 2,
			"versionNonce": 904335128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xXLjCQKy"
				},
				{
					"type": "arrow",
					"id": "WaHyLEh7"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0p"
		},
		{
			"id": "xXLjCQKy",
			"type": "text",
			"x": -664,
			"y": -504.5,
			"width": 132,
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
			"seed": 589209027,
			"version": 2,
			"versionNonce": 1260850792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "初始化放迴圈外",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2W9fWWft",
			"originalText": "初始化放迴圈外",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0q"
		},
		{
			"id": "Cid8J4TR",
			"type": "rectangle",
			"x": -812,
			"y": -459,
			"width": 294,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 194067684,
			"version": 2,
			"versionNonce": 694512664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NLJ8YtWR"
				},
				{
					"type": "arrow",
					"id": "YWrRrgh2"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0r"
		},
		{
			"id": "NLJ8YtWR",
			"type": "text",
			"x": -798,
			"y": -450,
			"width": 266,
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
			"seed": 1330078987,
			"version": 2,
			"versionNonce": 453575016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "continue 跳過更新 → 無窮迴圈",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Cid8J4TR",
			"originalText": "continue 跳過更新 → 無窮迴圈",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0s"
		},
		{
			"id": "4QF8pDew",
			"type": "rectangle",
			"x": -715,
			"y": -404.5,
			"width": 197,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 416182544,
			"version": 2,
			"versionNonce": 923805976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xQgUj8d2"
				},
				{
					"type": "arrow",
					"id": "PvDSLhTL"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0t"
		},
		{
			"id": "xQgUj8d2",
			"type": "text",
			"x": -701,
			"y": -395.5,
			"width": 169,
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
			"seed": 1158357637,
			"version": 2,
			"versionNonce": 540316776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "break 只跳出最內層",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4QF8pDew",
			"originalText": "break 只跳出最內層",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0u"
		},
		{
			"id": "fJvAYUJ9",
			"type": "rectangle",
			"x": -774,
			"y": -350,
			"width": 256,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 1057553130,
			"version": 2,
			"versionNonce": 442189336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8q4L894y"
				},
				{
					"type": "arrow",
					"id": "H6LUSDPS"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0v"
		},
		{
			"id": "8q4L894y",
			"type": "text",
			"x": -760,
			"y": -341,
			"width": 228,
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
			"seed": 1900769310,
			"version": 2,
			"versionNonce": 1081460584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "for-else：沒 break 才執行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fJvAYUJ9",
			"originalText": "for-else：沒 break 才執行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0w"
		},
		{
			"id": "tE5XdsEN",
			"type": "rectangle",
			"x": -822,
			"y": -295.5,
			"width": 304,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
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
			"seed": 1973855129,
			"version": 2,
			"versionNonce": 3851032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DTkxCCKP"
				},
				{
					"type": "arrow",
					"id": "DUTaebqc"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0x"
		},
		{
			"id": "DTkxCCKP",
			"type": "text",
			"x": -808,
			"y": -286.5,
			"width": 276,
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
			"seed": 815816641,
			"version": 2,
			"versionNonce": 1209571944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "while True 一定要有 break 路徑",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tE5XdsEN",
			"originalText": "while True 一定要有 break 路徑",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0y"
		},
		{
			"id": "cz9SEDbG",
			"type": "rectangle",
			"x": -442,
			"y": -81.5,
			"width": 92,
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
			"seed": 1309086255,
			"version": 2,
			"versionNonce": 1461887000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hLVFuvmt"
				},
				{
					"type": "arrow",
					"id": "RY6tZz5M"
				},
				{
					"type": "arrow",
					"id": "TAF7ZekG"
				},
				{
					"type": "arrow",
					"id": "g8gz3mkz"
				},
				{
					"type": "arrow",
					"id": "7Nhs7UUd"
				},
				{
					"type": "arrow",
					"id": "xfGBNg8X"
				},
				{
					"type": "arrow",
					"id": "VRFz5zpw"
				},
				{
					"type": "arrow",
					"id": "LXmYknBH"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b0z"
		},
		{
			"id": "hLVFuvmt",
			"type": "text",
			"x": -422,
			"y": -69.5,
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
			"seed": 1296839241,
			"version": 2,
			"versionNonce": 434703720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "字串",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cz9SEDbG",
			"originalText": "字串",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b10"
		},
		{
			"id": "Taq8jYei",
			"type": "rectangle",
			"x": -937,
			"y": -211,
			"width": 419,
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
			"seed": 1214648227,
			"version": 2,
			"versionNonce": 520543512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fdcvM2jt"
				},
				{
					"type": "arrow",
					"id": "TAF7ZekG"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b11"
		},
		{
			"id": "fdcvM2jt",
			"type": "text",
			"x": -923,
			"y": -202,
			"width": 391,
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
			"seed": 1548151378,
			"version": 2,
			"versionNonce": 1597186152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "索引越界 → IndexError；切片越界 → 不報錯",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Taq8jYei",
			"originalText": "索引越界 → IndexError；切片越界 → 不報錯",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b12"
		},
		{
			"id": "a8mLvKcK",
			"type": "rectangle",
			"x": -860,
			"y": -156.5,
			"width": 342,
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
			"seed": 267684491,
			"version": 2,
			"versionNonce": 962296344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Yjng6Zpy"
				},
				{
					"type": "arrow",
					"id": "g8gz3mkz"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b13"
		},
		{
			"id": "Yjng6Zpy",
			"type": "text",
			"x": -846,
			"y": -147.5,
			"width": 314,
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
			"seed": 1795781921,
			"version": 2,
			"versionNonce": 935514984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "find 找不到 → −1（不要當 bool 用）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "a8mLvKcK",
			"originalText": "find 找不到 → −1（不要當 bool 用）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b14"
		},
		{
			"id": "e2QmiYsU",
			"type": "rectangle",
			"x": -662,
			"y": -102,
			"width": 144,
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
			"seed": 1556563927,
			"version": 2,
			"versionNonce": 957642520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dApuK3M4"
				},
				{
					"type": "arrow",
					"id": "7Nhs7UUd"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b15"
		},
		{
			"id": "dApuK3M4",
			"type": "text",
			"x": -648,
			"y": -93,
			"width": 116,
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
			"seed": 1014534108,
			"version": 2,
			"versionNonce": 1776559720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "count 不重疊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "e2QmiYsU",
			"originalText": "count 不重疊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b16"
		},
		{
			"id": "3LGzu4QA",
			"type": "rectangle",
			"x": -886,
			"y": -47.5,
			"width": 368,
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
			"seed": 957757505,
			"version": 2,
			"versionNonce": 849728536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CLrxZfQs"
				},
				{
					"type": "arrow",
					"id": "xfGBNg8X"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b17"
		},
		{
			"id": "CLrxZfQs",
			"type": "text",
			"x": -872,
			"y": -38.5,
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
			"seed": 164412660,
			"version": 2,
			"versionNonce": 308484456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "strip 只去兩端；strip(\"km\") 是字元集合",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3LGzu4QA",
			"originalText": "strip 只去兩端；strip(\"km\") 是字元集合",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b18"
		},
		{
			"id": "wdXFTrKT",
			"type": "rectangle",
			"x": -874,
			"y": 7,
			"width": 356,
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
			"seed": 1023520585,
			"version": 2,
			"versionNonce": 201560344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "d6BSMdT3"
				},
				{
					"type": "arrow",
					"id": "VRFz5zpw"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b19"
		},
		{
			"id": "d6BSMdT3",
			"type": "text",
			"x": -860,
			"y": 16,
			"width": 328,
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
			"seed": 554717204,
			"version": 2,
			"versionNonce": 1418439784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "split(\",\") 保留空欄位；split() 依空白切",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wdXFTrKT",
			"originalText": "split(\",\") 保留空欄位；split() 依空白切",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1A"
		},
		{
			"id": "2AeqqmU8",
			"type": "rectangle",
			"x": -934,
			"y": 61.5,
			"width": 416,
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
			"seed": 1887301641,
			"version": 2,
			"versionNonce": 1285664280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "C4f6Gy2C"
				},
				{
					"type": "arrow",
					"id": "LXmYknBH"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1B"
		},
		{
			"id": "C4f6Gy2C",
			"type": "text",
			"x": -920,
			"y": 70.5,
			"width": 388,
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
			"seed": 1394839614,
			"version": 2,
			"versionNonce": 170516328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "len 是碼位數，不是 bytes，也不是看到的字數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2AeqqmU8",
			"originalText": "len 是碼位數，不是 bytes，也不是看到的字數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1C"
		},
		{
			"id": "vAWr4J2M",
			"type": "rectangle",
			"x": -491,
			"y": 341.25,
			"width": 141,
			"height": 54,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#d8f5a2",
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
			"seed": 47869557,
			"version": 2,
			"versionNonce": 1836329752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6Bg3Ti63"
				},
				{
					"type": "arrow",
					"id": "cJrVDphB"
				},
				{
					"type": "arrow",
					"id": "PNzSTtrH"
				},
				{
					"type": "arrow",
					"id": "JdAwRsyS"
				},
				{
					"type": "arrow",
					"id": "j3hhZKj4"
				},
				{
					"type": "arrow",
					"id": "AXDnNSZ2"
				},
				{
					"type": "arrow",
					"id": "Y4nkjB6r"
				},
				{
					"type": "arrow",
					"id": "GZGPLttf"
				},
				{
					"type": "arrow",
					"id": "gUTDT8WN"
				},
				{
					"type": "arrow",
					"id": "LVmh7zBW"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1D"
		},
		{
			"id": "6Bg3Ti63",
			"type": "text",
			"x": -471,
			"y": 353.25,
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
			"seed": 1334537651,
			"version": 2,
			"versionNonce": 1938403944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "錯誤類型",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vAWr4J2M",
			"originalText": "錯誤類型",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1E"
		},
		{
			"id": "7desH3Jw",
			"type": "rectangle",
			"x": -957,
			"y": 146,
			"width": 390,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 157236702,
			"version": 2,
			"versionNonce": 686753816,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "777VZFDk"
				},
				{
					"type": "arrow",
					"id": "PNzSTtrH"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1F"
		},
		{
			"id": "777VZFDk",
			"type": "text",
			"x": -943,
			"y": 155,
			"width": 362,
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
			"seed": 936322348,
			"version": 2,
			"versionNonce": 1735861608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "SyntaxError：缺冒號、括號沒關、= 當 ==",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7desH3Jw",
			"originalText": "SyntaxError：缺冒號、括號沒關、= 當 ==",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1G"
		},
		{
			"id": "YDwcGEa2",
			"type": "rectangle",
			"x": -1018,
			"y": 200.5,
			"width": 451,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 517261980,
			"version": 2,
			"versionNonce": 1258702104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4MavLUQU"
				},
				{
					"type": "arrow",
					"id": "JdAwRsyS"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1H"
		},
		{
			"id": "4MavLUQU",
			"type": "text",
			"x": -1004,
			"y": 209.5,
			"width": 423,
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
			"seed": 1593071236,
			"version": 2,
			"versionNonce": 54409320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "IndentationError：縮排對不齊（SyntaxError 的\n一種）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YDwcGEa2",
			"originalText": "IndentationError：縮排對不齊（SyntaxError 的\n一種）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1I"
		},
		{
			"id": "guBUi3Pr",
			"type": "rectangle",
			"x": -934,
			"y": 277.5,
			"width": 367,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 1989724243,
			"version": 2,
			"versionNonce": 19784216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xyGsGWzF"
				},
				{
					"type": "arrow",
					"id": "j3hhZKj4"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1J"
		},
		{
			"id": "xyGsGWzF",
			"type": "text",
			"x": -920,
			"y": 286.5,
			"width": 339,
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
			"seed": 2039998758,
			"version": 2,
			"versionNonce": 1521150824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "NameError：名稱沒定義（hello、true）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "guBUi3Pr",
			"originalText": "NameError：名稱沒定義（hello、true）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1K"
		},
		{
			"id": "h6J7fLTS",
			"type": "rectangle",
			"x": -974,
			"y": 332,
			"width": 407,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 665665605,
			"version": 2,
			"versionNonce": 710532888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "z2tMjWMv"
				},
				{
					"type": "arrow",
					"id": "AXDnNSZ2"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1L"
		},
		{
			"id": "z2tMjWMv",
			"type": "text",
			"x": -960,
			"y": 341,
			"width": 379,
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
			"seed": 1005187725,
			"version": 2,
			"versionNonce": 671694440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "TypeError：\"65\" + 1、\"30\" > 0、s[0] = \"c\"",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "h6J7fLTS",
			"originalText": "TypeError：\"65\" + 1、\"30\" > 0、s[0] = \"c\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1M"
		},
		{
			"id": "XuMEK2Q9",
			"type": "rectangle",
			"x": -939,
			"y": 386.5,
			"width": 372,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 1637782965,
			"version": 2,
			"versionNonce": 654195736,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EUm5aazp"
				},
				{
					"type": "arrow",
					"id": "Y4nkjB6r"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1N"
		},
		{
			"id": "EUm5aazp",
			"type": "text",
			"x": -925,
			"y": 395.5,
			"width": 344,
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
			"seed": 2000982472,
			"version": 2,
			"versionNonce": 2082812264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "ValueError：int(\"12.5\")、range(0, 5, 0)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XuMEK2Q9",
			"originalText": "ValueError：int(\"12.5\")、range(0, 5, 0)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1O"
		},
		{
			"id": "ZTuCbTdu",
			"type": "rectangle",
			"x": -825,
			"y": 441,
			"width": 258,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 878736531,
			"version": 2,
			"versionNonce": 688847128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uR9QJxHT"
				},
				{
					"type": "arrow",
					"id": "GZGPLttf"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1P"
		},
		{
			"id": "uR9QJxHT",
			"type": "text",
			"x": -811,
			"y": 450,
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
			"seed": 1678472183,
			"version": 2,
			"versionNonce": 1850393704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "ZeroDivisionError：3 / 0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZTuCbTdu",
			"originalText": "ZeroDivisionError：3 / 0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Q"
		},
		{
			"id": "E2YHxQPm",
			"type": "rectangle",
			"x": -822,
			"y": 495.5,
			"width": 255,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 1769823822,
			"version": 2,
			"versionNonce": 67114520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kMnpQT49"
				},
				{
					"type": "arrow",
					"id": "gUTDT8WN"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1R"
		},
		{
			"id": "kMnpQT49",
			"type": "text",
			"x": -808,
			"y": 504.5,
			"width": 227,
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
			"seed": 913934340,
			"version": 2,
			"versionNonce": 1279653736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "IndexError：\"Campus\"[6]",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "E2YHxQPm",
			"originalText": "IndexError：\"Campus\"[6]",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1S"
		},
		{
			"id": "eME2x2JB",
			"type": "rectangle",
			"x": -972,
			"y": 550,
			"width": 405,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
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
			"seed": 1185157000,
			"version": 2,
			"versionNonce": 2093323032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "F4AP7e2T"
				},
				{
					"type": "arrow",
					"id": "LVmh7zBW"
				}
			],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"index": "b1T"
		},
		{
			"id": "F4AP7e2T",
			"type": "text",
			"x": -958,
			"y": 559,
			"width": 377,
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
			"seed": 1333572363,
			"version": 2,
			"versionNonce": 1247988328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Logic error：沒有錯誤訊息，但結果不符規格",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eME2x2JB",
			"originalText": "Logic error：沒有錯誤訊息，但結果不符規格",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1U"
		},
		{
			"id": "CXezwpXK",
			"type": "text",
			"x": -1018,
			"y": -971.5,
			"width": 1131,
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
			"seed": 555441238,
			"version": 2,
			"versionNonce": 433287192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 7｜〔C〕考前速查：易錯陷阱與必背輸出",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 7｜〔C〕考前速查：易錯陷阱與必背輸出",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "mSjgLukL",
			"type": "text",
			"x": -1018,
			"y": -909.5,
			"width": 483,
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
			"seed": 1880283947,
			"version": 2,
			"versionNonce": 862797160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858155109,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "整張是 Claude 整理的考前速查，不是投影片或講義原文。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "整張是 Claude 整理的考前速查，不是投影片或講義原文。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1W"
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