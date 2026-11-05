---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Deck 2 整理]]"
  - "Midterm_Practice_Student.pdf（老師的 140 題例題，T001–T100、Q001–Q040）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
程式如何表示真實世界
Deck 2・W4 ^PRfXDJdr

驅動問題 ^kvF2T4Tt

12.5 km、45 min → 顯示名稱、英里、km/h ^W5egDXfT

數字看起來對還不夠，意義與單位也要對 ^55Mm5cgf

Q1 問題需要哪些資訊 ^X2h6Pff6

沒有角色與單位的數字是模糊的（12.5 是 km？miles？
分鐘？價格？） ^kunBL8bQ

Data contract v0.2 ^xXY6chyJ

route_name: str：非空、原樣保留 ^TP5vfcnN

distance_km: float：有限、非負 ^FZrUq5s7

duration_min: int：正整數分鐘 ^6LvAV3ER

報告：miles、speed_kmh，兩位小數＋單位 ^qkQ5gmyB

0.621371 是課程近似值 ^upfKcgiZ

規格寫著限制 ≠ 程式真的檢查 ^FZaxVNwr

先手算答案 ^eF4C2kpE

12.5 × 0.621371 = 7.7671375 → 7.77 miles ^qba8jPEF

45 / 60 = 0.75 h；12.5 / 0.75 = 16.666… → 16.67
km/h ^8e2Kt6Wd

Test oracle：獨立答案，不抄程式輸出 ^dAEgqUYM

例：3 km、30 min → 6 km/h（不是 0.1） ^tgBdQmff

AI 先要規格：Do not write code yet ^3VmR7s7D

Q2 為什麼要型態 ^XcZinhad

int（45 分鐘）、float（12.5 km）、str（路線名
稱） ^8Rh9Jj88

bool 在 Deck 3；⚠ Python 沒有 char 型態 ^ehks8kLF

print 會藏型態 → 用 type()：<class 'int'>、
<class 'str'> ^wfeTmCzJ

⚠ "007" 是 label：int("007") → 7，前導零不見
（資料模型錯誤） ^f2RKypaz

Q3 名稱如何指向資料 ^cpKEnvMs

Assignment：先算右邊，再綁左邊 ^HTdDCtXH

不是會回傳 None 的運算式 ^XikWVSCa

x = x + 1 是更新，不是方程式 ^iVYYb9B7

沒綁定就讀 → NameError ^yFxwzsMU

a = 10; b = a; a = 20 → 20 10 ^EGyQujVE

不是 live link，也不是「一定複製」 ^3PtAvJNq

⚠ Stale result：miles 不會自動重算 → 6.21371 ^KRwMvFUj

命名 ^bH8a29mr

distance_km、duration_min、MILES_PER_KM、
MINUTES_PER_HOUR ^TaPP7VXu

區分大小寫、snake_case、不能數字開頭／空格／保留
字 ^AUxYMVCu

大寫常數只是慣例 ^fwkzWYL3

⚠ 不要拿 input、float、str 當變數名 ^VRXNmdEe

Q4 輸入與轉型 ^tLBbZGAS

input() 回傳不含換行的 str：輸入 3、5 → 35 ^D7JKUfXQ

轉型 ^skFkmMKP

int("45") → 45 ^hyjHvSBb

float("12.5") → 12.5 ^J4V3mnKs

str(12.5) → "12.5" ^3xQbfztJ

int(12.9) → 12（向零截斷） ^Pm4ezyLg

⚠ int("12.5") → ValueError ^nym42m88

⚠ 不要 int(float(text)) 偷改資料 ^fsvFWy3Y

Read → convert → bind → use；
float(input(...)) 由內往外讀 ^LYtYAPt7

Conversion ≠ validation：int("0")、float("-3.5")
都成功但違規 ^9U6zudJX

Q5 數量關係寫成運算式 ^wqY9TR4X

單位轉換是演算法的一部分 ^PzCBKQNx

duration_h = duration_min / 60 ^XhkMX5Fe

speed_kmh = distance_km / duration_h ^q4d9rP75

⚠ 故意錯誤：60 km／60 min → 1.0 km/h（其實
是 km/min） ^djquniP8

⚠ km / min / 60 ≠ km / (min / 60) ^7nzF7gF7

運算子 ^CrCEgnE3

45 / 60 → 0.75（比例） ^NcXQmXBT

6 / 3 → 2.0、6 // 3 → 2：/ 一定得 float，兩個
int 做 // 得 int ^wyxU2JHW

45 // 60 → 0（floor） ^J5YYQRW9

83 // 60 → 1；83 % 60 → 23（1 小時 23 分） ^YDwf3z8P

3 ** 2 → 9 ^i2i5mTbp

2 + 3 * 4 → 14（先乘除後加減） ^bVQDkECS

⚠★ 次方是 **，^ 是 XOR〔C〕 ^Ey3xhs9x

f-string ^aFspiPSA

f"{miles:.2f}" → 7.77；只改顯示，不改值 ^xL8Y54Ci

print(miles) → 7.7671375000000005 ^mS263Kny

浮點數：0.1 + 0.2 → 0.30000000000000004；
.2f → 0.30 ^r4aJxspW

浮點加法不保證結合律：(1e16 + -1e16) + 1.0 → 1.0，
1e16 + (-1e16 + 1.0) → 0.0 ^XuKu7ChD

Trip Summary v0.2 三段：取得資料 → 計算衍生值
→ 顯示報告 ^mkJMtwc3

關係測試 ^8UKHYtZn

12.5／90 → 速度減半 8.33 ^EwVpewAf

25／90 → 速度加倍回 16.67 ^Ran7sZye

電腦基礎：位元表示整數 ^ECpTFN4h

bit 兩狀態；1 byte = 8 bits ^Ac5D7mQt

權重 128 64 32 16 8 4 2 1 ^2JeuZvNE

00001101 = 8 + 4 + 1 = 13 ^7VNkyc2v

編碼：選不超過的最大權重（貪婪） ^aSgnz632

n bits → 2ⁿ 種圖樣 ^Y6yCCfRn

unsigned：0 ～ 2ⁿ − 1 ^NcTst57X

8 bits：256 種，0–255；16 bits：65,536 種，
0–65,535 ^7P5iqSzG

兩個 8-bit unsigned 相加最大 510；9-bit 二補數只到
255，裝不下 ^mhhKKUsD

Two's complement ^xNBzUqS8

−5：00000101 反轉 → 11111010 加 1 → 11111011 ^YzDqaG73

最高位權重 −128：−128 + 64 + 32 + 16 + 8 + 2 + 1
= −5 ^xYnZRT58

範圍：−2ⁿ⁻¹ ～ 2ⁿ⁻¹ − 1（8 bits：−128 ～ 127） ^bJgvWbis

11111011：unsigned 251／signed −5 ^ncq7mUBp

Python int 任意精度：127 + 1 → 128（不會溢位） ^KtjRKDEp

練習：31 → 00011111；10000000 → 128 或
−128 ^Bu5aEFCg

★ 1 byte = 8 bits（T）；任何數字都用／都能用
8 bits（F） ^3jvs9MRM

Q6 AI 實作與驗證 ^2Uj5MibU

Prompt：只用學過的工具；不要 loops、functions、
packages、validation ^UNebvjdF

故意錯誤 candidate 三違規（007／3.5／30） ^22ikYUUb

int(float()) 截斷 3.5 → 速度 6.00（應 7.00） ^NGUv9ANG

除以係數 → 4.83 miles（應 2.17） ^BD66T67p

沒印 route ^kifSpSg4

測試矩陣 ^XAQLrGCG

12.5／45 → 7.77／16.67 ^8CUfjTRV

0／30 → 0.00／0.00（零距離有效） ^qFYbLuZS

60／60 → 37.28／60.00 ^RVVRV8uG

3.5／30 → 2.17／7.00 ^V4JbRi6c

不要改 expected 去配合錯程式 ^dUWti3uy

Workflow：Specify → Predict → Generate →
Inspect → Run tests → Revise ^BHdpqgZX

延伸欄位：12,500.00 m 或 0.75 h ^qDr759K4

Git：commit Add tested trip summary with
explicit units；⚠ 不要 force push ^58PPKiuM

專題點子：印刷費 10 × 2.5 = 25；讀書 20 × 3 /
60 = 1 h；用電 100 × 2 / 1000 = 0.2 kWh ^WuVhkb6a

選讀：精確規則 ^HzdNMeqz

截斷 vs floor vs ceil ^Jex2cNpg

int(-1.7) → −1（向零） ^T3BQzXfy

math.floor(-1.7) → −2；math.ceil(-1.7) → −1 ^RaK77CBP

-7 // 3 → −3；int(-7 / 3) → −2 ^bTpW3DNv

-7 % 3 → 2；b ≠ 0 時 a == (a // b) * b + a % b 一
定成立 ^vGQsZznQ

round(2.5) → 2；round(3.5) → 4（tie to even） ^C6MmFu7t

次方 ^JBPB47Ub

2 ** 3 ** 2 → 512（右結合） ^DsVatpd7

-3 ** 2 → −9；(-3) ** 2 → 9 ^FCqerJZj

x += y 更新數值 ^gUmzVwFT

★ result = print("Hello") → 印 Hello，result 是
None ^taAJZZWq

f"{12.345:.2f}" → "12.35"，型態是 str ^4ssmWssg

Q006 ^u8Uuv6JU

T015 ^acWH9tM3

T016 Q007 ^hBdJSwxJ

Q027 ^zuPMviLz

T068 ^iLeUi9FW

T013 ^VTy2xeAZ

T014 ^PwnptdK4

Q008 ^aTxv9du2

T022 ^G5GEQCKW

T018 T019 ^AWPWqwHv

Q010 ^7yZ87sKG

T021 ^fkHjcMvy

T020 ^Qs2YPtgA

T025 ^ZTsDS639

Q033 ^CvLDxyky

T091 ^aG3beNYm

T003 ^Q8xb4Hqx

Q009 ^gVbY8bBr

T005 ^aKBqXRwc

T070 ^fACBKAiB

Q032 ^MFgAnT3W

T006 ^GcVARtrt

T069 ^gjfykh4N

T024 T072 ^9F7D5aK2

T004 ^Nd4Ja43c

T071 ^wcYjpdkY

T017 ^dsrGqq66

T023 ^euD7CP6b

PROG1 期中心智圖 2｜Deck 2：程式如何表示真實世界（W4） ^xeM4UMVM

來源：PROG1 Deck 2 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的
練習題。 ^YL886git

★ 考古題考過 ^ufFGtWrW

⚠ 易錯陷阱 ^phN687sH

〔C〕Claude 補充（投影片與講義沒有） ^TpnBg7Ks

例題考到、原本心智圖沒有的觀念 ^tGmNamsm

T001 Q001 ^P34iNMpm

老師例題題號 ^Nvr9LHfA

T089 ^fJ6BczQ2

Extension 延伸題，講義說不代表考試範圍 ^p5ysVqXc

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "UZ6Axgj2",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 1612.85,
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
			"seed": 1464291467,
			"version": 2,
			"versionNonce": 1277235224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-1612.85
				],
				[
					150,
					-1612.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4cCbNMVi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "pECg3hvS",
			"type": "arrow",
			"x": 509.5,
			"y": -1612.85,
			"width": 76,
			"height": 27.25,
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
			"seed": 1306892542,
			"version": 2,
			"versionNonce": 1313447272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "4cCbNMVi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "886KPTWE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "vJK7wdE4",
			"type": "arrow",
			"x": 509.5,
			"y": -1612.85,
			"width": 76,
			"height": 27.25,
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
			"seed": 119041873,
			"version": 2,
			"versionNonce": 1253526808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "4cCbNMVi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "w5QjQCeH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "Kfs76q8b",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 1197.22,
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
			"seed": 529041437,
			"version": 2,
			"versionNonce": 1493282920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-1197.22
				],
				[
					150,
					-1197.22
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "XKJYwfPW",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 292.63,
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
			"seed": 531922361,
			"version": 2,
			"versionNonce": 1971186200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-292.63
				],
				[
					76,
					-292.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "r4dqHwSB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "VYt2BTYa",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 134.13,
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
			"seed": 488507354,
			"version": 2,
			"versionNonce": 423584616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-134.13
				],
				[
					76,
					-134.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "E8ZKAtjM",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 13.12,
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
			"seed": 310791597,
			"version": 2,
			"versionNonce": 661186328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					13.12
				],
				[
					76,
					13.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "78BSNtCr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "4Sv5iMzP",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 93.37,
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
			"seed": 682157188,
			"version": 2,
			"versionNonce": 223262312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					93.37
				],
				[
					76,
					93.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3gGxQiMP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "g9impweF",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 183.62,
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
			"seed": 1761742907,
			"version": 2,
			"versionNonce": 1022116888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					183.62
				],
				[
					76,
					183.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TKDvfTft",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "HDX2wWsz",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 238.12,
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
			"seed": 148377476,
			"version": 2,
			"versionNonce": 167487848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					238.12
				],
				[
					76,
					238.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JHirLQuA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "tp9eBKrm",
			"type": "arrow",
			"x": 648.5,
			"y": -1197.22,
			"width": 76,
			"height": 292.62,
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
			"seed": 414328765,
			"version": 2,
			"versionNonce": 1677459736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					292.62
				],
				[
					76,
					292.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "eGdHt7bd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sb2UKJmk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "NeavrVqn",
			"type": "arrow",
			"x": 933.5,
			"y": -1331.35,
			"width": 60,
			"height": 96,
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
			"seed": 374001942,
			"version": 2,
			"versionNonce": 1787968616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fDiQTgT9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "c4mME6nD",
			"type": "arrow",
			"x": 933.5,
			"y": -1331.35,
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
			"seed": 896037454,
			"version": 2,
			"versionNonce": 1812733464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Du7WsXSv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "j53w4BKE",
			"type": "arrow",
			"x": 933.5,
			"y": -1331.35,
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
			"seed": 1191197576,
			"version": 2,
			"versionNonce": 1088319336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bBWsfUYS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "3tubs6Zs",
			"type": "arrow",
			"x": 933.5,
			"y": -1331.35,
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
			"seed": 1198239043,
			"version": 2,
			"versionNonce": 370187032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "x6wqGfwL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "xk73JqG7",
			"type": "arrow",
			"x": 933.5,
			"y": -1331.35,
			"width": 60,
			"height": 96,
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
			"seed": 748235588,
			"version": 2,
			"versionNonce": 86786664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "cftNYxCc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4kbQ3WDh",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "9aJ6U9qC",
			"type": "arrow",
			"x": 847.5,
			"y": -1103.85,
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
			"seed": 868206199,
			"version": 2,
			"versionNonce": 1685944344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "3gGxQiMP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XbMwPvkY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "Cf4YWqxe",
			"type": "arrow",
			"x": 847.5,
			"y": -1103.85,
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
			"seed": 635314565,
			"version": 2,
			"versionNonce": 1179104616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "3gGxQiMP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cEn5eV8C",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "XGESE9i7",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 676.4,
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
			"seed": 248430472,
			"version": 2,
			"versionNonce": 1799795992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-676.4
				],
				[
					150,
					-676.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ReXcbyEy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "TvPEUKdR",
			"type": "arrow",
			"x": 605.5,
			"y": -676.4,
			"width": 76,
			"height": 113.65,
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
			"seed": 1368693926,
			"version": 2,
			"versionNonce": 1501349992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-113.65
				],
				[
					76,
					-113.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ReXcbyEy",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "c6jw3ZWj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "RB8C3UXb",
			"type": "arrow",
			"x": 605.5,
			"y": -676.4,
			"width": 76,
			"height": 47.9,
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
			"seed": 948546547,
			"version": 2,
			"versionNonce": 534794776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-47.9
				],
				[
					76,
					-47.9
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ReXcbyEy",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qRT7aXna",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "c9BdArRd",
			"type": "arrow",
			"x": 605.5,
			"y": -676.4,
			"width": 76,
			"height": 17.85,
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
			"seed": 1257085771,
			"version": 2,
			"versionNonce": 177699688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					17.85
				],
				[
					76,
					17.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ReXcbyEy",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TKxA3jKG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "EUmRbmwg",
			"type": "arrow",
			"x": 605.5,
			"y": -676.4,
			"width": 76,
			"height": 113.65,
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
			"seed": 1256686763,
			"version": 2,
			"versionNonce": 691949336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					113.65
				],
				[
					76,
					113.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ReXcbyEy",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "UiYe5Xrs",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "V6qwW8Qy",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 287.62,
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
			"seed": 1359608899,
			"version": 2,
			"versionNonce": 1273220712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-287.62
				],
				[
					150,
					-287.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "fJsFMTP8",
			"type": "arrow",
			"x": 652.5,
			"y": -287.62,
			"width": 76,
			"height": 179.38,
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
			"seed": 1657566289,
			"version": 2,
			"versionNonce": 802466840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-179.38
				],
				[
					76,
					-179.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "UceH6GiR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "KQ7xEDUp",
			"type": "arrow",
			"x": 652.5,
			"y": -287.62,
			"width": 76,
			"height": 124.88,
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
			"seed": 183389538,
			"version": 2,
			"versionNonce": 1714274664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-124.88
				],
				[
					76,
					-124.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RJUxJmc3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "Ad3GwxpR",
			"type": "arrow",
			"x": 652.5,
			"y": -287.62,
			"width": 76,
			"height": 51.58,
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
			"seed": 433725040,
			"version": 2,
			"versionNonce": 764897560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-51.58
				],
				[
					76,
					-51.58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ru5judQJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "XL77JzcE",
			"type": "arrow",
			"x": 652.5,
			"y": -287.62,
			"width": 76,
			"height": 21.72,
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
			"seed": 342494486,
			"version": 2,
			"versionNonce": 683758696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					21.72
				],
				[
					76,
					21.72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jnEm264M",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "bGxqciHy",
			"type": "arrow",
			"x": 652.5,
			"y": -287.62,
			"width": 76,
			"height": 179.37,
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
			"seed": 336958881,
			"version": 2,
			"versionNonce": 1039828504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					179.37
				],
				[
					76,
					179.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "UtKQqXLP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rvWab98j",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "6ZnPJj5C",
			"type": "arrow",
			"x": 1043.5,
			"y": -467,
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
			"seed": 319876750,
			"version": 2,
			"versionNonce": 426411880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "UceH6GiR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ibPLTjsE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "ZR3frvwF",
			"type": "arrow",
			"x": 1013.5,
			"y": -412.5,
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
			"seed": 266244885,
			"version": 2,
			"versionNonce": 1844577048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "RJUxJmc3",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "55P54QMM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "aGh3xHK3",
			"type": "arrow",
			"x": 1034.5,
			"y": -339.2,
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
			"seed": 1271842921,
			"version": 2,
			"versionNonce": 611670632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "ru5judQJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "AGXV543u",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "mLjqCUCb",
			"type": "arrow",
			"x": 796.5,
			"y": -108.25,
			"width": 60,
			"height": 96.4,
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
			"seed": 275454223,
			"version": 2,
			"versionNonce": 200400920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-96.4
				],
				[
					60,
					-96.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rvWab98j",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7msswgBE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "FgJ2M5Yz",
			"type": "arrow",
			"x": 796.5,
			"y": -108.25,
			"width": 60,
			"height": 28.4,
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
			"seed": 1615773259,
			"version": 2,
			"versionNonce": 1286458728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-28.4
				],
				[
					60,
					-28.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rvWab98j",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "n75tV2YL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "EvxgMrPs",
			"type": "arrow",
			"x": 796.5,
			"y": -108.25,
			"width": 60,
			"height": 48.4,
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
			"seed": 1612725383,
			"version": 2,
			"versionNonce": 2012093720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					48.4
				],
				[
					60,
					48.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rvWab98j",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6GVZKSiQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "qHB8hgMX",
			"type": "arrow",
			"x": 796.5,
			"y": -108.25,
			"width": 60,
			"height": 96.4,
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
			"seed": 2051212544,
			"version": 2,
			"versionNonce": 1533010024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					96.4
				],
				[
					60,
					96.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rvWab98j",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yVswsZ8C",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "8GZmNKQS",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 312.98,
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
			"seed": 915175881,
			"version": 2,
			"versionNonce": 1935325720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					312.98
				],
				[
					150,
					312.98
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rjc68t8R",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "TRiWJ6E9",
			"type": "arrow",
			"x": 577.5,
			"y": 312.98,
			"width": 76,
			"height": 224.78,
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
			"seed": 154902883,
			"version": 2,
			"versionNonce": 274174824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-224.78
				],
				[
					76,
					-224.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjc68t8R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HFwFY2kD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "bv23HrsU",
			"type": "arrow",
			"x": 577.5,
			"y": 312.98,
			"width": 76,
			"height": 44.13,
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
			"seed": 291012414,
			"version": 2,
			"versionNonce": 1898690328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-44.13
				],
				[
					76,
					-44.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjc68t8R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "smnmAZkK",
			"type": "arrow",
			"x": 577.5,
			"y": 312.98,
			"width": 76,
			"height": 147.77,
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
			"seed": 271410240,
			"version": 2,
			"versionNonce": 1373693544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					147.77
				],
				[
					76,
					147.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjc68t8R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "scff6SHr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "3J7LukYb",
			"type": "arrow",
			"x": 577.5,
			"y": 312.98,
			"width": 76,
			"height": 224.77,
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
			"seed": 1276324934,
			"version": 2,
			"versionNonce": 1708463128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					224.77
				],
				[
					76,
					224.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rjc68t8R",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eJ3vVhhy",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "XU4h46fG",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 129.4,
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
			"seed": 1801307964,
			"version": 2,
			"versionNonce": 1556601192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-129.4
				],
				[
					60,
					-129.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Th2JsRSe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "msVQFaPg",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 81.4,
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
			"seed": 1639705940,
			"version": 2,
			"versionNonce": 390779160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YtPHtNBW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "Leybj5Zt",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 33.4,
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
			"seed": 501159561,
			"version": 2,
			"versionNonce": 1951951976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jJjdQwCP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "6HtQc4m5",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 14.6,
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
			"seed": 1932134545,
			"version": 2,
			"versionNonce": 1828777496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CLdqfXNe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "ratcDyT5",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 81.4,
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
			"seed": 2130186066,
			"version": 2,
			"versionNonce": 308191080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sPRhVNMa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "v8Vvfn2u",
			"type": "arrow",
			"x": 721.5,
			"y": 268.85,
			"width": 60,
			"height": 129.4,
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
			"seed": 203567539,
			"version": 2,
			"versionNonce": 1072392984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					129.4
				],
				[
					60,
					129.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "WVZQVC3E",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vijppati",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "JhrtVFvy",
			"type": "arrow",
			"x": 218.5,
			"y": -0.0,
			"width": 150,
			"height": 1136.8,
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
			"seed": 586721729,
			"version": 2,
			"versionNonce": 388395624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					1136.8
				],
				[
					150,
					1136.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "TWnekcyi",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 482.55,
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
			"seed": 1102726926,
			"version": 2,
			"versionNonce": 712919064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-482.55
				],
				[
					76,
					-482.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nvbaFHLq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "vHQME7jK",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 377.25,
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
			"seed": 1829065165,
			"version": 2,
			"versionNonce": 2038162792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-377.25
				],
				[
					76,
					-377.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mThJiGj7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "SgqHYn32",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 311.5,
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
			"seed": 1699647052,
			"version": 2,
			"versionNonce": 1487766808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-311.5
				],
				[
					76,
					-311.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8vrfqQWV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "C7sJcCnM",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 68.65,
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
			"seed": 1648230969,
			"version": 2,
			"versionNonce": 1990916200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-68.65
				],
				[
					76,
					-68.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "QAQjkUdS",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 213.75,
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
			"seed": 2144426786,
			"version": 2,
			"versionNonce": 1475158552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					213.75
				],
				[
					76,
					213.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "y8rsWkhK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "nfQNWWE3",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 319.05,
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
			"seed": 1768621506,
			"version": 2,
			"versionNonce": 1115663208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					319.05
				],
				[
					76,
					319.05
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Ub2MtUhz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "RbKsAUmr",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 396.05,
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
			"seed": 488603092,
			"version": 2,
			"versionNonce": 1731272472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					396.05
				],
				[
					76,
					396.05
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jsYhTsGD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "Ee2q9AhE",
			"type": "arrow",
			"x": 677.5,
			"y": 1136.8,
			"width": 76,
			"height": 482.55,
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
			"seed": 1789072806,
			"version": 2,
			"versionNonce": 927333992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					482.55
				],
				[
					76,
					482.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "zYnHzxpf",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "e8J6UbdF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "2bHXbrTN",
			"type": "arrow",
			"x": 1006.5,
			"y": 654.25,
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
			"seed": 886592163,
			"version": 2,
			"versionNonce": 1189968920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "nvbaFHLq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BX7RAtgG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "Va8t3f2U",
			"type": "arrow",
			"x": 1006.5,
			"y": 654.25,
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
			"seed": 1103710110,
			"version": 2,
			"versionNonce": 97120616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "nvbaFHLq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "r4ccBMLV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "hwRRNm4u",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 191.6,
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
			"seed": 637341544,
			"version": 2,
			"versionNonce": 152451352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-191.6
				],
				[
					60,
					-191.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "E9K5YBRZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "h4huma5Z",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 114.8,
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
			"seed": 1853226360,
			"version": 2,
			"versionNonce": 1700234344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-114.8
				],
				[
					60,
					-114.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tWjCgAZP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "6EUcrvcJ",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 56.8,
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
			"seed": 348825673,
			"version": 2,
			"versionNonce": 1629443608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-56.8
				],
				[
					60,
					-56.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "685qiBXQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "9YvYbNwQ",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 10,
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
			"seed": 437262160,
			"version": 2,
			"versionNonce": 1136310120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					10
				],
				[
					60,
					10
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MdhtXC5x",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "uMhJBrLX",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 58,
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
			"seed": 1955847035,
			"version": 2,
			"versionNonce": 1945948952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					58
				],
				[
					60,
					58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PkfsYb78",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "YmWJrH9v",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 124.8,
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
			"seed": 742287717,
			"version": 2,
			"versionNonce": 1967098472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					124.8
				],
				[
					60,
					124.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "feCtuy8d",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "X2KeRPi3",
			"type": "arrow",
			"x": 839.5,
			"y": 1068.15,
			"width": 60,
			"height": 191.6,
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
			"seed": 21801281,
			"version": 2,
			"versionNonce": 673361944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					191.6
				],
				[
					60,
					191.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "6a5FmW89",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rJEZbqXU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "RLs2vnFA",
			"type": "arrow",
			"x": 853.5,
			"y": 1350.55,
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
			"seed": 1513811305,
			"version": 2,
			"versionNonce": 1689386344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "y8rsWkhK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Qw9W4S7G",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "AMZLGL7s",
			"type": "arrow",
			"x": 853.5,
			"y": 1350.55,
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
			"seed": 279054516,
			"version": 2,
			"versionNonce": 1971645720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "y8rsWkhK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ksJgbs3N",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "WwQ8NVmC",
			"type": "arrow",
			"x": 1213.5,
			"y": 1455.85,
			"width": 60,
			"height": 9.4,
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
			"seed": 1402336234,
			"version": 2,
			"versionNonce": 1130238056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					9.4
				],
				[
					60,
					9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Ub2MtUhz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GS7R6Jsq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "XqynJ9WG",
			"type": "arrow",
			"x": 858.5,
			"y": 1619.35,
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
			"seed": 650111149,
			"version": 2,
			"versionNonce": 899123736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "e8J6UbdF",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jSdyNkWL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "34Aw7jEi",
			"type": "arrow",
			"x": 858.5,
			"y": 1619.35,
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
			"seed": 598687813,
			"version": 2,
			"versionNonce": 957334376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "e8J6UbdF",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xBLyr52p",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "XJLsKLVH",
			"type": "arrow",
			"x": -218.5,
			"y": -0.0,
			"width": 150,
			"height": 705.17,
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
			"seed": 2100251766,
			"version": 2,
			"versionNonce": 1934526232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-705.17
				],
				[
					-150,
					-705.17
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "ftsKYhYL",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 401.03,
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
			"seed": 534825081,
			"version": 2,
			"versionNonce": 336795240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-401.03
				],
				[
					-76,
					-401.03
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kP3QNssF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "amFNzrzx",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 325.78,
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
			"seed": 518059662,
			"version": 2,
			"versionNonce": 991814680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-325.78
				],
				[
					-76,
					-325.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sgnV6znN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0A"
		},
		{
			"id": "pCpRyau3",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 171.98,
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
			"seed": 2092245307,
			"version": 2,
			"versionNonce": 2033453416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-171.98
				],
				[
					-76,
					-171.98
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Yw82CRr6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0B"
		},
		{
			"id": "XYjxkRiq",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 68.62,
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
			"seed": 1742800233,
			"version": 2,
			"versionNonce": 1794744600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					68.62
				],
				[
					-76,
					68.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ccv8JrrK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0C"
		},
		{
			"id": "jGQk4J3P",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 239.47,
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
			"seed": 1969985015,
			"version": 2,
			"versionNonce": 331258984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					239.47
				],
				[
					-76,
					239.47
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gQTQmGqg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0D"
		},
		{
			"id": "nVw4nPmD",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 324.02,
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
			"seed": 704416227,
			"version": 2,
			"versionNonce": 39173656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					324.02
				],
				[
					-76,
					324.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sJ9mBzbM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0E"
		},
		{
			"id": "8ydjubAs",
			"type": "arrow",
			"x": -682.5,
			"y": -705.17,
			"width": 76,
			"height": 401.02,
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
			"seed": 2118167866,
			"version": 2,
			"versionNonce": 1165938536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					401.02
				],
				[
					-76,
					401.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7D27LAis",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zb67GXgV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0F"
		},
		{
			"id": "f2WtnNt7",
			"type": "arrow",
			"x": -1028.5,
			"y": -1030.95,
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
			"seed": 1479689969,
			"version": 2,
			"versionNonce": 1915108120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "sgnV6znN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mh7F65vV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0G"
		},
		{
			"id": "jGxzg55V",
			"type": "arrow",
			"x": -1028.5,
			"y": -1030.95,
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
			"seed": 168456244,
			"version": 2,
			"versionNonce": 1455465064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "sgnV6znN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ALWbWgZA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0H"
		},
		{
			"id": "wCEuAAwF",
			"type": "arrow",
			"x": -956.5,
			"y": -877.15,
			"width": 60,
			"height": 81.8,
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
			"seed": 1226600440,
			"version": 2,
			"versionNonce": 1826560024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-81.8
				],
				[
					-60,
					-81.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Yw82CRr6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PqCZwLE4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0I"
		},
		{
			"id": "fimTBeCx",
			"type": "arrow",
			"x": -956.5,
			"y": -877.15,
			"width": 60,
			"height": 5,
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
			"seed": 1847749221,
			"version": 2,
			"versionNonce": 642782568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "Yw82CRr6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2XYCvadH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0J"
		},
		{
			"id": "Wy6KKgGT",
			"type": "arrow",
			"x": -956.5,
			"y": -877.15,
			"width": 60,
			"height": 81.8,
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
			"seed": 1207828032,
			"version": 2,
			"versionNonce": 913593624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					81.8
				],
				[
					-60,
					81.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Yw82CRr6",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eSYyGgNX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0K"
		},
		{
			"id": "UAiYY68H",
			"type": "arrow",
			"x": -947.5,
			"y": -636.55,
			"width": 60,
			"height": 100.8,
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
			"seed": 505666684,
			"version": 2,
			"versionNonce": 1501112424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-100.8
				],
				[
					-60,
					-100.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ccv8JrrK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LJmyrSMv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0L"
		},
		{
			"id": "urNiWWe7",
			"type": "arrow",
			"x": -947.5,
			"y": -636.55,
			"width": 60,
			"height": 42.8,
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
			"seed": 2007293901,
			"version": 2,
			"versionNonce": 1952051736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-42.8
				],
				[
					-60,
					-42.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ccv8JrrK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nB5k84Z4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0M"
		},
		{
			"id": "S9LFjYxJ",
			"type": "arrow",
			"x": -947.5,
			"y": -636.55,
			"width": 60,
			"height": 34,
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
			"seed": 694503257,
			"version": 2,
			"versionNonce": 201841512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					34
				],
				[
					-60,
					34
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ccv8JrrK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Vy2Gtx22",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0N"
		},
		{
			"id": "8pegfZk9",
			"type": "arrow",
			"x": -947.5,
			"y": -636.55,
			"width": 60,
			"height": 100.8,
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
			"seed": 1049956880,
			"version": 2,
			"versionNonce": 2105798424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					100.8
				],
				[
					-60,
					100.8
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ccv8JrrK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rGJUksRw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0O"
		},
		{
			"id": "TAwVDXzX",
			"type": "arrow",
			"x": -218.5,
			"y": -0.0,
			"width": 150,
			"height": 140.85,
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
			"seed": 163839560,
			"version": 2,
			"versionNonce": 4730472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					140.85
				],
				[
					-150,
					140.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0P"
		},
		{
			"id": "EiqkMuZ4",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 338,
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
			"seed": 1080238633,
			"version": 2,
			"versionNonce": 711347224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-338
				],
				[
					-76,
					-338
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "G939Qfja",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Q"
		},
		{
			"id": "L4WsV8VC",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 227.5,
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
			"seed": 1435187828,
			"version": 2,
			"versionNonce": 1325801832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-227.5
				],
				[
					-76,
					-227.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "V8nUqSkX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0R"
		},
		{
			"id": "LAgbaRXS",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 59.5,
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
			"seed": 1077286295,
			"version": 2,
			"versionNonce": 620038424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-59.5
				],
				[
					-76,
					-59.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "diArVRrX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0S"
		},
		{
			"id": "985uL4d5",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 63.75,
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
			"seed": 1291535245,
			"version": 2,
			"versionNonce": 395162728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					63.75
				],
				[
					-76,
					63.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "f74dZrL8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0T"
		},
		{
			"id": "YV6VNwLw",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 129.5,
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
			"seed": 1308207221,
			"version": 2,
			"versionNonce": 950281752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					129.5
				],
				[
					-76,
					129.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ivCiebqZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0U"
		},
		{
			"id": "VPaWqVAc",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 195.25,
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
			"seed": 466876916,
			"version": 2,
			"versionNonce": 799729512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					195.25
				],
				[
					-76,
					195.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "P44gYbYk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0V"
		},
		{
			"id": "CkALCSED",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 261,
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
			"seed": 13103304,
			"version": 2,
			"versionNonce": 577217304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					261
				],
				[
					-76,
					261
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GS8BWqYW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0W"
		},
		{
			"id": "PUtWWpwf",
			"type": "arrow",
			"x": -619.5,
			"y": 140.85,
			"width": 76,
			"height": 338,
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
			"seed": 811182459,
			"version": 2,
			"versionNonce": 1403632232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					338
				],
				[
					-76,
					338
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ubxefJr2",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NcriqK7R",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0X"
		},
		{
			"id": "gBxeNuab",
			"type": "arrow",
			"x": -1118.5,
			"y": -86.65,
			"width": 60,
			"height": 48,
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
			"seed": 1749736425,
			"version": 2,
			"versionNonce": 1622376472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "V8nUqSkX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xNEz3R96",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Y"
		},
		{
			"id": "FSMJ7L83",
			"type": "arrow",
			"x": -1118.5,
			"y": -86.65,
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
			"seed": 999033296,
			"version": 2,
			"versionNonce": 1448488296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "V8nUqSkX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vPbwB6VT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Z"
		},
		{
			"id": "p4s3aNuy",
			"type": "arrow",
			"x": -1118.5,
			"y": -86.65,
			"width": 60,
			"height": 48,
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
			"seed": 1687149109,
			"version": 2,
			"versionNonce": 58440984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "V8nUqSkX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uGUB6u92",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0a"
		},
		{
			"id": "8vkAinec",
			"type": "arrow",
			"x": -800.5,
			"y": 81.35,
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
			"seed": 96642487,
			"version": 2,
			"versionNonce": 1358708840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "diArVRrX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "83K3AWmd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0b"
		},
		{
			"id": "XPFmmDHW",
			"type": "arrow",
			"x": -800.5,
			"y": 81.35,
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
			"seed": 1724918996,
			"version": 2,
			"versionNonce": 2083805720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "diArVRrX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Z4ZiPyjv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0c"
		},
		{
			"id": "utaXfKtn",
			"type": "arrow",
			"x": -800.5,
			"y": 81.35,
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
			"seed": 1133512010,
			"version": 2,
			"versionNonce": 1399321448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "diArVRrX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uBiukY9d",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0d"
		},
		{
			"id": "J5YcnEY9",
			"type": "arrow",
			"x": -800.5,
			"y": 81.35,
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
			"seed": 940720195,
			"version": 2,
			"versionNonce": 1842435864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "diArVRrX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "C9cXkMEj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0e"
		},
		{
			"id": "SLdfHkQH",
			"type": "arrow",
			"x": -218.5,
			"y": -0.0,
			"width": 150,
			"height": 891.38,
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
			"seed": 2121312590,
			"version": 2,
			"versionNonce": 333792872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					891.38
				],
				[
					-150,
					891.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "KQCqjitG",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0f"
		},
		{
			"id": "TjTZCxgd",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 233.63,
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
			"seed": 1721192162,
			"version": 2,
			"versionNonce": 2093397016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-233.63
				],
				[
					-76,
					-233.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gWcv8RiX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0g"
		},
		{
			"id": "xMUfducC",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 85.98,
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
			"seed": 1239062945,
			"version": 2,
			"versionNonce": 524302696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-85.98
				],
				[
					-76,
					-85.98
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "s6q3T4cE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0h"
		},
		{
			"id": "J5SEjYCZ",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 10.73,
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
			"seed": 1000041547,
			"version": 2,
			"versionNonce": 520646936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-10.73
				],
				[
					-76,
					-10.73
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dULBiTSr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0i"
		},
		{
			"id": "8C35eaQL",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 83.32,
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
			"seed": 1365518023,
			"version": 2,
			"versionNonce": 147115112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					83.32
				],
				[
					-76,
					83.32
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CfFkRgqG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0j"
		},
		{
			"id": "zh2b9Dhv",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 149.07,
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
			"seed": 1767885887,
			"version": 2,
			"versionNonce": 1812631064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					149.07
				],
				[
					-76,
					149.07
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7jfXRCpa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0k"
		},
		{
			"id": "rdCW66BB",
			"type": "arrow",
			"x": -584.5,
			"y": 891.38,
			"width": 76,
			"height": 233.62,
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
			"seed": 1469420778,
			"version": 2,
			"versionNonce": 440336232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					233.62
				],
				[
					-76,
					233.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "DZQuBCYH",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sC6XcKEC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0l"
		},
		{
			"id": "SerchQEW",
			"type": "arrow",
			"x": -868.5,
			"y": 657.75,
			"width": 60,
			"height": 86.4,
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
			"seed": 928642549,
			"version": 2,
			"versionNonce": 1824590616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-86.4
				],
				[
					-60,
					-86.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gWcv8RiX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yTbfPMP4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0m"
		},
		{
			"id": "Kp4HeL65",
			"type": "arrow",
			"x": -868.5,
			"y": 657.75,
			"width": 60,
			"height": 38.4,
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
			"seed": 1427173900,
			"version": 2,
			"versionNonce": 66769512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					-38.4
				],
				[
					-60,
					-38.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gWcv8RiX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pbyBf9dc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0n"
		},
		{
			"id": "8XhjeEYe",
			"type": "arrow",
			"x": -868.5,
			"y": 657.75,
			"width": 60,
			"height": 9.6,
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
			"seed": 1189407185,
			"version": 2,
			"versionNonce": 1805641752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					9.6
				],
				[
					-60,
					9.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gWcv8RiX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pMTSKS2G",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0o"
		},
		{
			"id": "fSunhLMK",
			"type": "arrow",
			"x": -868.5,
			"y": 657.75,
			"width": 60,
			"height": 86.4,
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
			"seed": 1162027383,
			"version": 2,
			"versionNonce": 214189416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
					86.4
				],
				[
					-60,
					86.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "gWcv8RiX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JRgz6zNc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0p"
		},
		{
			"id": "HCAMaqLY",
			"type": "arrow",
			"x": -728.5,
			"y": 880.65,
			"width": 60,
			"height": 24,
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
			"seed": 1590174755,
			"version": 2,
			"versionNonce": 1151018264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "dULBiTSr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vNAgGQeT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0q"
		},
		{
			"id": "j4rdfeNj",
			"type": "arrow",
			"x": -728.5,
			"y": 880.65,
			"width": 60,
			"height": 24,
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
			"seed": 1965086108,
			"version": 2,
			"versionNonce": 1105680488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
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
				"elementId": "dULBiTSr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "t6VqnNRW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0r"
		},
		{
			"id": "KQCqjitG",
			"type": "rectangle",
			"x": -218.5,
			"y": -67,
			"width": 437,
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
			"seed": 272740102,
			"version": 2,
			"versionNonce": 891732504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PRfXDJdr"
				},
				{
					"type": "arrow",
					"id": "UZ6Axgj2"
				},
				{
					"type": "arrow",
					"id": "Kfs76q8b"
				},
				{
					"type": "arrow",
					"id": "XGESE9i7"
				},
				{
					"type": "arrow",
					"id": "V6qwW8Qy"
				},
				{
					"type": "arrow",
					"id": "8GZmNKQS"
				},
				{
					"type": "arrow",
					"id": "JhrtVFvy"
				},
				{
					"type": "arrow",
					"id": "XJLsKLVH"
				},
				{
					"type": "arrow",
					"id": "TAwVDXzX"
				},
				{
					"type": "arrow",
					"id": "SLdfHkQH"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b0s"
		},
		{
			"id": "PRfXDJdr",
			"type": "text",
			"x": -186.5,
			"y": -45,
			"width": 373,
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
			"seed": 484224714,
			"version": 2,
			"versionNonce": 657460072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "程式如何表示真實世界\nDeck 2・W4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KQCqjitG",
			"originalText": "程式如何表示真實世界\nDeck 2・W4",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0t"
		},
		{
			"id": "4cCbNMVi",
			"type": "rectangle",
			"x": 368.5,
			"y": -1639.85,
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
			"seed": 1625285590,
			"version": 2,
			"versionNonce": 741785368,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kvF2T4Tt"
				},
				{
					"type": "arrow",
					"id": "UZ6Axgj2"
				},
				{
					"type": "arrow",
					"id": "pECg3hvS"
				},
				{
					"type": "arrow",
					"id": "vJK7wdE4"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b0u"
		},
		{
			"id": "kvF2T4Tt",
			"type": "text",
			"x": 388.5,
			"y": -1627.85,
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
			"seed": 171718476,
			"version": 2,
			"versionNonce": 1726635624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "驅動問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4cCbNMVi",
			"originalText": "驅動問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0v"
		},
		{
			"id": "886KPTWE",
			"type": "rectangle",
			"x": 585.5,
			"y": -1660.35,
			"width": 397,
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
			"seed": 1336355294,
			"version": 2,
			"versionNonce": 440343576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "W5egDXfT"
				},
				{
					"type": "arrow",
					"id": "pECg3hvS"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b0w"
		},
		{
			"id": "W5egDXfT",
			"type": "text",
			"x": 599.5,
			"y": -1651.35,
			"width": 369,
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
			"seed": 148078591,
			"version": 2,
			"versionNonce": 31609192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "12.5 km、45 min → 顯示名稱、英里、km/h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "886KPTWE",
			"originalText": "12.5 km、45 min → 顯示名稱、英里、km/h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0x"
		},
		{
			"id": "w5QjQCeH",
			"type": "rectangle",
			"x": 585.5,
			"y": -1605.85,
			"width": 364,
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
			"seed": 182791728,
			"version": 2,
			"versionNonce": 1093916952,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "55Mm5cgf"
				},
				{
					"type": "arrow",
					"id": "vJK7wdE4"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b0y"
		},
		{
			"id": "55Mm5cgf",
			"type": "text",
			"x": 599.5,
			"y": -1596.85,
			"width": 336,
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
			"seed": 1641530081,
			"version": 2,
			"versionNonce": 2137252968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "數字看起來對還不夠，意義與單位也要對",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "w5QjQCeH",
			"originalText": "數字看起來對還不夠，意義與單位也要對",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0z"
		},
		{
			"id": "eGdHt7bd",
			"type": "rectangle",
			"x": 368.5,
			"y": -1224.22,
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
			"seed": 444902206,
			"version": 2,
			"versionNonce": 76084760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "X2h6Pff6"
				},
				{
					"type": "arrow",
					"id": "Kfs76q8b"
				},
				{
					"type": "arrow",
					"id": "XKJYwfPW"
				},
				{
					"type": "arrow",
					"id": "VYt2BTYa"
				},
				{
					"type": "arrow",
					"id": "E8ZKAtjM"
				},
				{
					"type": "arrow",
					"id": "4Sv5iMzP"
				},
				{
					"type": "arrow",
					"id": "g9impweF"
				},
				{
					"type": "arrow",
					"id": "HDX2wWsz"
				},
				{
					"type": "arrow",
					"id": "tp9eBKrm"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b10"
		},
		{
			"id": "X2h6Pff6",
			"type": "text",
			"x": 388.5,
			"y": -1212.22,
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
			"seed": 511004761,
			"version": 2,
			"versionNonce": 490411880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q1 問題需要哪些資訊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eGdHt7bd",
			"originalText": "Q1 問題需要哪些資訊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b11"
		},
		{
			"id": "r4dqHwSB",
			"type": "rectangle",
			"x": 724.5,
			"y": -1521.35,
			"width": 480,
			"height": 63,
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
			"seed": 1014152323,
			"version": 2,
			"versionNonce": 959607576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kunBL8bQ"
				},
				{
					"type": "arrow",
					"id": "XKJYwfPW"
				}
			],
			"updated": 1793858136855,
			"link": null,
			"locked": false,
			"index": "b12"
		},
		{
			"id": "kunBL8bQ",
			"type": "text",
			"x": 738.5,
			"y": -1512.35,
			"width": 452,
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
			"seed": 924179252,
			"version": 2,
			"versionNonce": 2142497384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "沒有角色與單位的數字是模糊的（12.5 是 km？miles？\n分鐘？價格？）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "r4dqHwSB",
			"originalText": "沒有角色與單位的數字是模糊的（12.5 是 km？miles？\n分鐘？價格？）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b13"
		},
		{
			"id": "cftNYxCc",
			"type": "rectangle",
			"x": 724.5,
			"y": -1351.6,
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
			"seed": 1188482593,
			"version": 2,
			"versionNonce": 1973702680,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xXY6chyJ"
				},
				{
					"type": "arrow",
					"id": "VYt2BTYa"
				},
				{
					"type": "arrow",
					"id": "NeavrVqn"
				},
				{
					"type": "arrow",
					"id": "c4mME6nD"
				},
				{
					"type": "arrow",
					"id": "j53w4BKE"
				},
				{
					"type": "arrow",
					"id": "3tubs6Zs"
				},
				{
					"type": "arrow",
					"id": "xk73JqG7"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b14"
		},
		{
			"id": "xXY6chyJ",
			"type": "text",
			"x": 738.5,
			"y": -1342.6,
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
			"seed": 1779880057,
			"version": 2,
			"versionNonce": 1637506408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Data contract v0.2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cftNYxCc",
			"originalText": "Data contract v0.2",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b15"
		},
		{
			"id": "fDiQTgT9",
			"type": "rectangle",
			"x": 993.5,
			"y": -1444.35,
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
			"seed": 1868263700,
			"version": 2,
			"versionNonce": 1641188632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TP5vfcnN"
				},
				{
					"type": "arrow",
					"id": "NeavrVqn"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b16"
		},
		{
			"id": "TP5vfcnN",
			"type": "text",
			"x": 1005.5,
			"y": -1437.35,
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
			"seed": 816542502,
			"version": 2,
			"versionNonce": 1144680552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "route_name: str：非空、原樣保留",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fDiQTgT9",
			"originalText": "route_name: str：非空、原樣保留",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b17"
		},
		{
			"id": "Du7WsXSv",
			"type": "rectangle",
			"x": 993.5,
			"y": -1396.35,
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
			"seed": 1352944658,
			"version": 2,
			"versionNonce": 120662552,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FZrUq5s7"
				},
				{
					"type": "arrow",
					"id": "c4mME6nD"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b18"
		},
		{
			"id": "FZrUq5s7",
			"type": "text",
			"x": 1005.5,
			"y": -1389.35,
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
			"seed": 300519955,
			"version": 2,
			"versionNonce": 526394216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "distance_km: float：有限、非負",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Du7WsXSv",
			"originalText": "distance_km: float：有限、非負",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b19"
		},
		{
			"id": "bBWsfUYS",
			"type": "rectangle",
			"x": 993.5,
			"y": -1348.35,
			"width": 259,
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
			"seed": 1833707204,
			"version": 2,
			"versionNonce": 548677400,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6LvAV3ER"
				},
				{
					"type": "arrow",
					"id": "j53w4BKE"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1A"
		},
		{
			"id": "6LvAV3ER",
			"type": "text",
			"x": 1005.5,
			"y": -1341.35,
			"width": 235,
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
			"seed": 64004587,
			"version": 2,
			"versionNonce": 290944616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "duration_min: int：正整數分鐘",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bBWsfUYS",
			"originalText": "duration_min: int：正整數分鐘",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1B"
		},
		{
			"id": "x6wqGfwL",
			"type": "rectangle",
			"x": 993.5,
			"y": -1300.35,
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
			"seed": 1785111907,
			"version": 2,
			"versionNonce": 1791984664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qkQ5gmyB"
				},
				{
					"type": "arrow",
					"id": "3tubs6Zs"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1C"
		},
		{
			"id": "qkQ5gmyB",
			"type": "text",
			"x": 1005.5,
			"y": -1293.35,
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
			"seed": 570528407,
			"version": 2,
			"versionNonce": 250374504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "報告：miles、speed_kmh，兩位小數＋單位",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "x6wqGfwL",
			"originalText": "報告：miles、speed_kmh，兩位小數＋單位",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1D"
		},
		{
			"id": "4kbQ3WDh",
			"type": "rectangle",
			"x": 993.5,
			"y": -1252.35,
			"width": 202,
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
			"seed": 1434617428,
			"version": 2,
			"versionNonce": 1937195288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "upfKcgiZ"
				},
				{
					"type": "arrow",
					"id": "xk73JqG7"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "upfKcgiZ",
			"type": "text",
			"x": 1005.5,
			"y": -1245.35,
			"width": 178,
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
			"seed": 511280567,
			"version": 2,
			"versionNonce": 325778536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "0.621371 是課程近似值",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4kbQ3WDh",
			"originalText": "0.621371 是課程近似值",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "78BSNtCr",
			"type": "rectangle",
			"x": 724.5,
			"y": -1204.35,
			"width": 278,
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
			"seed": 1236057822,
			"version": 2,
			"versionNonce": 1780440600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FZaxVNwr"
				},
				{
					"type": "arrow",
					"id": "E8ZKAtjM"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "FZaxVNwr",
			"type": "text",
			"x": 738.5,
			"y": -1195.35,
			"width": 250,
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
			"seed": 1445551110,
			"version": 2,
			"versionNonce": 1352609640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "規格寫著限制 ≠ 程式真的檢查",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "78BSNtCr",
			"originalText": "規格寫著限制 ≠ 程式真的檢查",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "3gGxQiMP",
			"type": "rectangle",
			"x": 724.5,
			"y": -1124.1,
			"width": 123,
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
			"seed": 494934586,
			"version": 2,
			"versionNonce": 1874582296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eF4C2kpE"
				},
				{
					"type": "arrow",
					"id": "4Sv5iMzP"
				},
				{
					"type": "arrow",
					"id": "9aJ6U9qC"
				},
				{
					"type": "arrow",
					"id": "Cf4YWqxe"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "eF4C2kpE",
			"type": "text",
			"x": 738.5,
			"y": -1115.1,
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
			"seed": 984095638,
			"version": 2,
			"versionNonce": 1591018088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "先手算答案",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3gGxQiMP",
			"originalText": "先手算答案",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "XbMwPvkY",
			"type": "rectangle",
			"x": 907.5,
			"y": -1149.85,
			"width": 358,
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
			"seed": 1221064203,
			"version": 2,
			"versionNonce": 1723906072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qba8jPEF"
				},
				{
					"type": "arrow",
					"id": "9aJ6U9qC"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "qba8jPEF",
			"type": "text",
			"x": 919.5,
			"y": -1142.85,
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
			"seed": 749205129,
			"version": 2,
			"versionNonce": 1826125160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "12.5 × 0.621371 = 7.7671375 → 7.77 miles",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XbMwPvkY",
			"originalText": "12.5 × 0.621371 = 7.7671375 → 7.77 miles",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "cEn5eV8C",
			"type": "rectangle",
			"x": 907.5,
			"y": -1101.85,
			"width": 428,
			"height": 54,
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
			"seed": 784522964,
			"version": 2,
			"versionNonce": 1126298904,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8e2Kt6Wd"
				},
				{
					"type": "arrow",
					"id": "Cf4YWqxe"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "8e2Kt6Wd",
			"type": "text",
			"x": 919.5,
			"y": -1094.85,
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
			"seed": 1090773763,
			"version": 2,
			"versionNonce": 1878362216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "45 / 60 = 0.75 h；12.5 / 0.75 = 16.666… → 16.67\nkm/h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cEn5eV8C",
			"originalText": "45 / 60 = 0.75 h；12.5 / 0.75 = 16.666… → 16.67\nkm/h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "TKDvfTft",
			"type": "rectangle",
			"x": 724.5,
			"y": -1033.85,
			"width": 357,
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
			"seed": 1943434857,
			"version": 2,
			"versionNonce": 1515426328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dAEgqUYM"
				},
				{
					"type": "arrow",
					"id": "g9impweF"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "dAEgqUYM",
			"type": "text",
			"x": 738.5,
			"y": -1024.85,
			"width": 329,
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
			"seed": 477484960,
			"version": 2,
			"versionNonce": 1408777064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Test oracle：獨立答案，不抄程式輸出",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TKDvfTft",
			"originalText": "Test oracle：獨立答案，不抄程式輸出",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "JHirLQuA",
			"type": "rectangle",
			"x": 724.5,
			"y": -979.35,
			"width": 386,
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
			"seed": 1279229518,
			"version": 2,
			"versionNonce": 860458776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tgBdQmff"
				},
				{
					"type": "arrow",
					"id": "HDX2wWsz"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "tgBdQmff",
			"type": "text",
			"x": 738.5,
			"y": -970.35,
			"width": 358,
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
			"seed": 2026410598,
			"version": 2,
			"versionNonce": 724340328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "例：3 km、30 min → 6 km/h（不是 0.1）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JHirLQuA",
			"originalText": "例：3 km、30 min → 6 km/h（不是 0.1）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "sb2UKJmk",
			"type": "rectangle",
			"x": 724.5,
			"y": -924.85,
			"width": 357,
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
			"seed": 1934844195,
			"version": 2,
			"versionNonce": 1450699800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3VmR7s7D"
				},
				{
					"type": "arrow",
					"id": "tp9eBKrm"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "3VmR7s7D",
			"type": "text",
			"x": 738.5,
			"y": -915.85,
			"width": 329,
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
			"seed": 1229391853,
			"version": 2,
			"versionNonce": 1583251816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI 先要規格：Do not write code yet",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sb2UKJmk",
			"originalText": "AI 先要規格：Do not write code yet",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "ReXcbyEy",
			"type": "rectangle",
			"x": 368.5,
			"y": -703.4,
			"width": 237,
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
			"seed": 116248727,
			"version": 2,
			"versionNonce": 500345112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XcZinhad"
				},
				{
					"type": "arrow",
					"id": "XGESE9i7"
				},
				{
					"type": "arrow",
					"id": "TvPEUKdR"
				},
				{
					"type": "arrow",
					"id": "RB8C3UXb"
				},
				{
					"type": "arrow",
					"id": "c9BdArRd"
				},
				{
					"type": "arrow",
					"id": "EUmRbmwg"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "XcZinhad",
			"type": "text",
			"x": 388.5,
			"y": -691.4,
			"width": 197,
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
			"seed": 1014475574,
			"version": 2,
			"versionNonce": 1557795944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q2 為什麼要型態",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ReXcbyEy",
			"originalText": "Q2 為什麼要型態",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "c6jw3ZWj",
			"type": "rectangle",
			"x": 681.5,
			"y": -821.55,
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
				"4XkTsYnH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1826896036,
			"version": 2,
			"versionNonce": 80594456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8Rh9Jj88"
				},
				{
					"type": "arrow",
					"id": "TvPEUKdR"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "8Rh9Jj88",
			"type": "text",
			"x": 695.5,
			"y": -812.55,
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
				"4XkTsYnH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 85647898,
			"version": 2,
			"versionNonce": 1282099048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "int（45 分鐘）、float（12.5 km）、str（路線名\n稱）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "c6jw3ZWj",
			"originalText": "int（45 分鐘）、float（12.5 km）、str（路線名\n稱）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "qRT7aXna",
			"type": "rectangle",
			"x": 681.5,
			"y": -744.55,
			"width": 407,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
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
			"seed": 2102636824,
			"version": 2,
			"versionNonce": 2019377944,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ehks8kLF"
				},
				{
					"type": "arrow",
					"id": "RB8C3UXb"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "ehks8kLF",
			"type": "text",
			"x": 695.5,
			"y": -735.55,
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
			"seed": 1142150539,
			"version": 2,
			"versionNonce": 962468456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "bool 在 Deck 3；⚠ Python 沒有 char 型態",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qRT7aXna",
			"originalText": "bool 在 Deck 3；⚠ Python 沒有 char 型態",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "TKxA3jKG",
			"type": "rectangle",
			"x": 681.5,
			"y": -690.05,
			"width": 411,
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
			"seed": 164058663,
			"version": 2,
			"versionNonce": 653598744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wfeTmCzJ"
				},
				{
					"type": "arrow",
					"id": "c9BdArRd"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "wfeTmCzJ",
			"type": "text",
			"x": 695.5,
			"y": -681.05,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1243048521,
			"version": 2,
			"versionNonce": 1182698856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "print 會藏型態 → 用 type()：<class 'int'>、\n<class 'str'>",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TKxA3jKG",
			"originalText": "print 會藏型態 → 用 type()：<class 'int'>、\n<class 'str'>",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "UiYe5Xrs",
			"type": "rectangle",
			"x": 681.5,
			"y": -594.25,
			"width": 439,
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
				"7gzqFGwC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 640629305,
			"version": 2,
			"versionNonce": 1351179544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "f2RKypaz"
				},
				{
					"type": "arrow",
					"id": "EUmRbmwg"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "f2RKypaz",
			"type": "text",
			"x": 695.5,
			"y": -585.25,
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
				"7gzqFGwC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 462590920,
			"version": 2,
			"versionNonce": 1561895016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ \"007\" 是 label：int(\"007\") → 7，前導零不見\n（資料模型錯誤）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UiYe5Xrs",
			"originalText": "⚠ \"007\" 是 label：int(\"007\") → 7，前導零不見\n（資料模型錯誤）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "UtKQqXLP",
			"type": "rectangle",
			"x": 368.5,
			"y": -314.62,
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
			"seed": 838204621,
			"version": 2,
			"versionNonce": 378403352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cpKEnvMs"
				},
				{
					"type": "arrow",
					"id": "V6qwW8Qy"
				},
				{
					"type": "arrow",
					"id": "fJsFMTP8"
				},
				{
					"type": "arrow",
					"id": "KQ7xEDUp"
				},
				{
					"type": "arrow",
					"id": "Ad3GwxpR"
				},
				{
					"type": "arrow",
					"id": "XL77JzcE"
				},
				{
					"type": "arrow",
					"id": "bGxqciHy"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "cpKEnvMs",
			"type": "text",
			"x": 388.5,
			"y": -302.62,
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
			"seed": 72671241,
			"version": 2,
			"versionNonce": 1559778152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q3 名稱如何指向資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UtKQqXLP",
			"originalText": "Q3 名稱如何指向資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "UceH6GiR",
			"type": "rectangle",
			"x": 728.5,
			"y": -487.25,
			"width": 315,
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
			"seed": 665502390,
			"version": 2,
			"versionNonce": 1274476312,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HTdDCtXH"
				},
				{
					"type": "arrow",
					"id": "fJsFMTP8"
				},
				{
					"type": "arrow",
					"id": "6ZnPJj5C"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "HTdDCtXH",
			"type": "text",
			"x": 742.5,
			"y": -478.25,
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
			"seed": 993419171,
			"version": 2,
			"versionNonce": 1281992296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Assignment：先算右邊，再綁左邊",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UceH6GiR",
			"originalText": "Assignment：先算右邊，再綁左邊",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "ibPLTjsE",
			"type": "rectangle",
			"x": 1103.5,
			"y": -484,
			"width": 226,
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
			"seed": 1851690146,
			"version": 2,
			"versionNonce": 1161319448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XikWVSCa"
				},
				{
					"type": "arrow",
					"id": "6ZnPJj5C"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "XikWVSCa",
			"type": "text",
			"x": 1115.5,
			"y": -477,
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
			"seed": 161446285,
			"version": 2,
			"versionNonce": 137927016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "不是會回傳 None 的運算式",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ibPLTjsE",
			"originalText": "不是會回傳 None 的運算式",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "RJUxJmc3",
			"type": "rectangle",
			"x": 728.5,
			"y": -432.75,
			"width": 285,
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
			"seed": 1045788403,
			"version": 2,
			"versionNonce": 675680536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iVYYb9B7"
				},
				{
					"type": "arrow",
					"id": "KQ7xEDUp"
				},
				{
					"type": "arrow",
					"id": "ZR3frvwF"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "iVYYb9B7",
			"type": "text",
			"x": 742.5,
			"y": -423.75,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 65166853,
			"version": 2,
			"versionNonce": 1940991080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "x = x + 1 是更新，不是方程式",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RJUxJmc3",
			"originalText": "x = x + 1 是更新，不是方程式",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "55P54QMM",
			"type": "rectangle",
			"x": 1073.5,
			"y": -429.5,
			"width": 220,
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
			"seed": 1867003865,
			"version": 2,
			"versionNonce": 1016344088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yFxwzsMU"
				},
				{
					"type": "arrow",
					"id": "ZR3frvwF"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "yFxwzsMU",
			"type": "text",
			"x": 1085.5,
			"y": -422.5,
			"width": 196,
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
			"seed": 1797156649,
			"version": 2,
			"versionNonce": 681533288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "沒綁定就讀 → NameError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "55P54QMM",
			"originalText": "沒綁定就讀 → NameError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "ru5judQJ",
			"type": "rectangle",
			"x": 728.5,
			"y": -359.45,
			"width": 306,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"WbVqWxEu"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1939939489,
			"version": 2,
			"versionNonce": 991341336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EGyQujVE"
				},
				{
					"type": "arrow",
					"id": "Ad3GwxpR"
				},
				{
					"type": "arrow",
					"id": "aGh3xHK3"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "EGyQujVE",
			"type": "text",
			"x": 742.5,
			"y": -350.45,
			"width": 278,
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
				"WbVqWxEu"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1649358480,
			"version": 2,
			"versionNonce": 659501672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "a = 10; b = a; a = 20 → 20 10",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ru5judQJ",
			"originalText": "a = 10; b = a; a = 20 → 20 10",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "AGXV543u",
			"type": "rectangle",
			"x": 1094.5,
			"y": -356.2,
			"width": 288,
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
			"seed": 1383514725,
			"version": 2,
			"versionNonce": 507611160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3PtAvJNq"
				},
				{
					"type": "arrow",
					"id": "aGh3xHK3"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "3PtAvJNq",
			"type": "text",
			"x": 1106.5,
			"y": -349.2,
			"width": 264,
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
			"seed": 967729972,
			"version": 2,
			"versionNonce": 109880680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "不是 live link，也不是「一定複製」",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AGXV543u",
			"originalText": "不是 live link，也不是「一定複製」",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "jnEm264M",
			"type": "rectangle",
			"x": 728.5,
			"y": -286.15,
			"width": 442,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"zkugmic5"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1589555940,
			"version": 2,
			"versionNonce": 1913177368,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KRwMvFUj"
				},
				{
					"type": "arrow",
					"id": "XL77JzcE"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "KRwMvFUj",
			"type": "text",
			"x": 742.5,
			"y": -277.15,
			"width": 414,
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
				"zkugmic5"
			],
			"frameId": null,
			"roundness": null,
			"seed": 361775713,
			"version": 2,
			"versionNonce": 597932136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ Stale result：miles 不會自動重算 → 6.21371",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jnEm264M",
			"originalText": "⚠ Stale result：miles 不會自動重算 → 6.21371",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "rvWab98j",
			"type": "rectangle",
			"x": 728.5,
			"y": -128.5,
			"width": 68,
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
			"seed": 468376213,
			"version": 2,
			"versionNonce": 601907736,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bH8a29mr"
				},
				{
					"type": "arrow",
					"id": "bGxqciHy"
				},
				{
					"type": "arrow",
					"id": "mLjqCUCb"
				},
				{
					"type": "arrow",
					"id": "FgJ2M5Yz"
				},
				{
					"type": "arrow",
					"id": "EvxgMrPs"
				},
				{
					"type": "arrow",
					"id": "qHB8hgMX"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "bH8a29mr",
			"type": "text",
			"x": 742.5,
			"y": -119.5,
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
			"seed": 1238507620,
			"version": 2,
			"versionNonce": 1382050664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "命名",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rvWab98j",
			"originalText": "命名",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "7msswgBE",
			"type": "rectangle",
			"x": 856.5,
			"y": -231.65,
			"width": 407,
			"height": 54,
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
			"seed": 235733722,
			"version": 2,
			"versionNonce": 1388076824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TaPP7VXu"
				},
				{
					"type": "arrow",
					"id": "mLjqCUCb"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "TaPP7VXu",
			"type": "text",
			"x": 868.5,
			"y": -224.65,
			"width": 383,
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
			"seed": 1462290302,
			"version": 2,
			"versionNonce": 219070056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "distance_km、duration_min、MILES_PER_KM、\nMINUTES_PER_HOUR",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7msswgBE",
			"originalText": "distance_km、duration_min、MILES_PER_KM、\nMINUTES_PER_HOUR",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "n75tV2YL",
			"type": "rectangle",
			"x": 856.5,
			"y": -163.65,
			"width": 431,
			"height": 54,
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
			"seed": 1713928051,
			"version": 2,
			"versionNonce": 521190424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AUxYMVCu"
				},
				{
					"type": "arrow",
					"id": "FgJ2M5Yz"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "AUxYMVCu",
			"type": "text",
			"x": 868.5,
			"y": -156.65,
			"width": 407,
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
			"seed": 39642059,
			"version": 2,
			"versionNonce": 612020584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "區分大小寫、snake_case、不能數字開頭／空格／保留\n字",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "n75tV2YL",
			"originalText": "區分大小寫、snake_case、不能數字開頭／空格／保留\n字",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "6GVZKSiQ",
			"type": "rectangle",
			"x": 856.5,
			"y": -76.85,
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
			"groupIds": [
				"tUmvV89t"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1766972701,
			"version": 2,
			"versionNonce": 2060548376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fwkzWYL3"
				},
				{
					"type": "arrow",
					"id": "EvxgMrPs"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "fwkzWYL3",
			"type": "text",
			"x": 868.5,
			"y": -69.85,
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
			"groupIds": [
				"tUmvV89t"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1280313221,
			"version": 2,
			"versionNonce": 1878017128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "大寫常數只是慣例",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6GVZKSiQ",
			"originalText": "大寫常數只是慣例",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "yVswsZ8C",
			"type": "rectangle",
			"x": 856.5,
			"y": -28.85,
			"width": 316,
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
			"seed": 375814674,
			"version": 2,
			"versionNonce": 2037552664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VRXNmdEe"
				},
				{
					"type": "arrow",
					"id": "qHB8hgMX"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "VRXNmdEe",
			"type": "text",
			"x": 868.5,
			"y": -21.85,
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
			"seed": 1632383957,
			"version": 2,
			"versionNonce": 2101049192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 不要拿 input、float、str 當變數名",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yVswsZ8C",
			"originalText": "⚠ 不要拿 input、float、str 當變數名",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "rjc68t8R",
			"type": "rectangle",
			"x": 368.5,
			"y": 285.98,
			"width": 209,
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
			"seed": 1390032034,
			"version": 2,
			"versionNonce": 535302936,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tLBbZGAS"
				},
				{
					"type": "arrow",
					"id": "8GZmNKQS"
				},
				{
					"type": "arrow",
					"id": "TRiWJ6E9"
				},
				{
					"type": "arrow",
					"id": "bv23HrsU"
				},
				{
					"type": "arrow",
					"id": "smnmAZkK"
				},
				{
					"type": "arrow",
					"id": "3J7LukYb"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "tLBbZGAS",
			"type": "text",
			"x": 388.5,
			"y": 297.98,
			"width": 169,
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
			"seed": 682255642,
			"version": 2,
			"versionNonce": 1084770920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q4 輸入與轉型",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rjc68t8R",
			"originalText": "Q4 輸入與轉型",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "HFwFY2kD",
			"type": "rectangle",
			"x": 653.5,
			"y": 67.95,
			"width": 424,
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
				"UH6TmpLf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1657958906,
			"version": 2,
			"versionNonce": 883290136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "D7JKUfXQ"
				},
				{
					"type": "arrow",
					"id": "TRiWJ6E9"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "D7JKUfXQ",
			"type": "text",
			"x": 667.5,
			"y": 76.95,
			"width": 396,
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
				"UH6TmpLf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 695014707,
			"version": 2,
			"versionNonce": 1157807464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "input() 回傳不含換行的 str：輸入 3、5 → 35",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HFwFY2kD",
			"originalText": "input() 回傳不含換行的 str：輸入 3、5 → 35",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "WVZQVC3E",
			"type": "rectangle",
			"x": 653.5,
			"y": 248.6,
			"width": 68,
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
			"seed": 1061681972,
			"version": 2,
			"versionNonce": 262155544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "skFkmMKP"
				},
				{
					"type": "arrow",
					"id": "bv23HrsU"
				},
				{
					"type": "arrow",
					"id": "XU4h46fG"
				},
				{
					"type": "arrow",
					"id": "msVQFaPg"
				},
				{
					"type": "arrow",
					"id": "Leybj5Zt"
				},
				{
					"type": "arrow",
					"id": "6HtQc4m5"
				},
				{
					"type": "arrow",
					"id": "ratcDyT5"
				},
				{
					"type": "arrow",
					"id": "v8Vvfn2u"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "skFkmMKP",
			"type": "text",
			"x": 667.5,
			"y": 257.6,
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
			"seed": 944900612,
			"version": 2,
			"versionNonce": 1536610408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "轉型",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WVZQVC3E",
			"originalText": "轉型",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "Th2JsRSe",
			"type": "rectangle",
			"x": 781.5,
			"y": 122.45,
			"width": 144,
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
			"seed": 1775501614,
			"version": 2,
			"versionNonce": 1783286296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hyjHvSBb"
				},
				{
					"type": "arrow",
					"id": "XU4h46fG"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "hyjHvSBb",
			"type": "text",
			"x": 793.5,
			"y": 129.45,
			"width": 120,
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
			"seed": 319399633,
			"version": 2,
			"versionNonce": 1278247784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "int(\"45\") → 45",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Th2JsRSe",
			"originalText": "int(\"45\") → 45",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "YtPHtNBW",
			"type": "rectangle",
			"x": 781.5,
			"y": 170.45,
			"width": 189,
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
			"seed": 1416300485,
			"version": 2,
			"versionNonce": 798607128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J4V3mnKs"
				},
				{
					"type": "arrow",
					"id": "msVQFaPg"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "J4V3mnKs",
			"type": "text",
			"x": 793.5,
			"y": 177.45,
			"width": 165,
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
			"seed": 535869437,
			"version": 2,
			"versionNonce": 85710440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "float(\"12.5\") → 12.5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YtPHtNBW",
			"originalText": "float(\"12.5\") → 12.5",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "jJjdQwCP",
			"type": "rectangle",
			"x": 781.5,
			"y": 218.45,
			"width": 174,
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
			"seed": 796309532,
			"version": 2,
			"versionNonce": 1275143192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3xQbfztJ"
				},
				{
					"type": "arrow",
					"id": "Leybj5Zt"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "3xQbfztJ",
			"type": "text",
			"x": 793.5,
			"y": 225.45,
			"width": 150,
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
			"seed": 2084782239,
			"version": 2,
			"versionNonce": 1260702056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "str(12.5) → \"12.5\"",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jJjdQwCP",
			"originalText": "str(12.5) → \"12.5\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "CLdqfXNe",
			"type": "rectangle",
			"x": 781.5,
			"y": 266.45,
			"width": 242,
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
			"seed": 1778732116,
			"version": 2,
			"versionNonce": 2104811800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Pm4ezyLg"
				},
				{
					"type": "arrow",
					"id": "6HtQc4m5"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "Pm4ezyLg",
			"type": "text",
			"x": 793.5,
			"y": 273.45,
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
			"seed": 1071921312,
			"version": 2,
			"versionNonce": 1771527272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "int(12.9) → 12（向零截斷）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CLdqfXNe",
			"originalText": "int(12.9) → 12（向零截斷）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "sPRhVNMa",
			"type": "rectangle",
			"x": 781.5,
			"y": 333.25,
			"width": 243,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"NQDHX784"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1377615028,
			"version": 2,
			"versionNonce": 594083352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nym42m88"
				},
				{
					"type": "arrow",
					"id": "ratcDyT5"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "nym42m88",
			"type": "text",
			"x": 793.5,
			"y": 340.25,
			"width": 219,
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
				"NQDHX784"
			],
			"frameId": null,
			"roundness": null,
			"seed": 19024363,
			"version": 2,
			"versionNonce": 1648332648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ int(\"12.5\") → ValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sPRhVNMa",
			"originalText": "⚠ int(\"12.5\") → ValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "vijppati",
			"type": "rectangle",
			"x": 781.5,
			"y": 381.25,
			"width": 289,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
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
			"seed": 305527481,
			"version": 2,
			"versionNonce": 248609560,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fsvFWy3Y"
				},
				{
					"type": "arrow",
					"id": "v8Vvfn2u"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "fsvFWy3Y",
			"type": "text",
			"x": 793.5,
			"y": 388.25,
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
			"seed": 2102040243,
			"version": 2,
			"versionNonce": 493445736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 不要 int(float(text)) 偷改資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vijppati",
			"originalText": "⚠ 不要 int(float(text)) 偷改資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "scff6SHr",
			"type": "rectangle",
			"x": 653.5,
			"y": 429.25,
			"width": 329,
			"height": 63,
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
			"seed": 1460332694,
			"version": 2,
			"versionNonce": 1377982488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LYtYAPt7"
				},
				{
					"type": "arrow",
					"id": "smnmAZkK"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "LYtYAPt7",
			"type": "text",
			"x": 667.5,
			"y": 438.25,
			"width": 301,
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
			"seed": 1610916722,
			"version": 2,
			"versionNonce": 434165096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Read → convert → bind → use；\nfloat(input(...)) 由內往外讀",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "scff6SHr",
			"originalText": "Read → convert → bind → use；\nfloat(input(...)) 由內往外讀",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "eJ3vVhhy",
			"type": "rectangle",
			"x": 653.5,
			"y": 506.25,
			"width": 450,
			"height": 63,
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
			"seed": 1185617434,
			"version": 2,
			"versionNonce": 290428184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9U6zudJX"
				},
				{
					"type": "arrow",
					"id": "3J7LukYb"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "9U6zudJX",
			"type": "text",
			"x": 667.5,
			"y": 515.25,
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
			"seed": 1369429091,
			"version": 2,
			"versionNonce": 485615720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Conversion ≠ validation：int(\"0\")、float(\"-3.5\")\n都成功但違規",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eJ3vVhhy",
			"originalText": "Conversion ≠ validation：int(\"0\")、float(\"-3.5\")\n都成功但違規",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "zYnHzxpf",
			"type": "rectangle",
			"x": 368.5,
			"y": 1109.8,
			"width": 309,
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
			"seed": 1834283941,
			"version": 2,
			"versionNonce": 1372402200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wqY9TR4X"
				},
				{
					"type": "arrow",
					"id": "JhrtVFvy"
				},
				{
					"type": "arrow",
					"id": "TWnekcyi"
				},
				{
					"type": "arrow",
					"id": "vHQME7jK"
				},
				{
					"type": "arrow",
					"id": "SgqHYn32"
				},
				{
					"type": "arrow",
					"id": "C7sJcCnM"
				},
				{
					"type": "arrow",
					"id": "QAQjkUdS"
				},
				{
					"type": "arrow",
					"id": "nfQNWWE3"
				},
				{
					"type": "arrow",
					"id": "RbKsAUmr"
				},
				{
					"type": "arrow",
					"id": "Ee2q9AhE"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "wqY9TR4X",
			"type": "text",
			"x": 388.5,
			"y": 1121.8,
			"width": 269,
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
			"seed": 667902475,
			"version": 2,
			"versionNonce": 1651022696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q5 數量關係寫成運算式",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zYnHzxpf",
			"originalText": "Q5 數量關係寫成運算式",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "nvbaFHLq",
			"type": "rectangle",
			"x": 753.5,
			"y": 634,
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
			"groupIds": [
				"3sBPfUL4"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1665635036,
			"version": 2,
			"versionNonce": 1250897688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PzCBKQNx"
				},
				{
					"type": "arrow",
					"id": "TWnekcyi"
				},
				{
					"type": "arrow",
					"id": "2bHXbrTN"
				},
				{
					"type": "arrow",
					"id": "Va8t3f2U"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "PzCBKQNx",
			"type": "text",
			"x": 767.5,
			"y": 643,
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
			"groupIds": [
				"3sBPfUL4"
			],
			"frameId": null,
			"roundness": null,
			"seed": 610200273,
			"version": 2,
			"versionNonce": 1284566632,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "單位轉換是演算法的一部分",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nvbaFHLq",
			"originalText": "單位轉換是演算法的一部分",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "BX7RAtgG",
			"type": "rectangle",
			"x": 1066.5,
			"y": 613.25,
			"width": 280,
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
			"seed": 1437150403,
			"version": 2,
			"versionNonce": 873040920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XhkMX5Fe"
				},
				{
					"type": "arrow",
					"id": "2bHXbrTN"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "XhkMX5Fe",
			"type": "text",
			"x": 1078.5,
			"y": 620.25,
			"width": 256,
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
			"seed": 1628701771,
			"version": 2,
			"versionNonce": 339140968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "duration_h = duration_min / 60",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BX7RAtgG",
			"originalText": "duration_h = duration_min / 60",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "r4ccBMLV",
			"type": "rectangle",
			"x": 1066.5,
			"y": 661.25,
			"width": 342,
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
			"seed": 1308638566,
			"version": 2,
			"versionNonce": 405817624,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "q4d9rP75"
				},
				{
					"type": "arrow",
					"id": "Va8t3f2U"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2W"
		},
		{
			"id": "q4d9rP75",
			"type": "text",
			"x": 1078.5,
			"y": 668.25,
			"width": 318,
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
			"seed": 1314747512,
			"version": 2,
			"versionNonce": 2024174696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "speed_kmh = distance_km / duration_h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "r4ccBMLV",
			"originalText": "speed_kmh = distance_km / duration_h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "mThJiGj7",
			"type": "rectangle",
			"x": 753.5,
			"y": 728.05,
			"width": 445,
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
				"LAvQgJpR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 497400258,
			"version": 2,
			"versionNonce": 578250264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "djquniP8"
				},
				{
					"type": "arrow",
					"id": "vHQME7jK"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "djquniP8",
			"type": "text",
			"x": 767.5,
			"y": 737.05,
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
			"groupIds": [
				"LAvQgJpR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 229858689,
			"version": 2,
			"versionNonce": 1873520488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 故意錯誤：60 km／60 min → 1.0 km/h（其實\n是 km/min）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mThJiGj7",
			"originalText": "⚠ 故意錯誤：60 km／60 min → 1.0 km/h（其實\n是 km/min）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "8vrfqQWV",
			"type": "rectangle",
			"x": 753.5,
			"y": 805.05,
			"width": 343,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
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
			"seed": 809095748,
			"version": 2,
			"versionNonce": 1876091672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7nzF7gF7"
				},
				{
					"type": "arrow",
					"id": "SgqHYn32"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "7nzF7gF7",
			"type": "text",
			"x": 767.5,
			"y": 814.05,
			"width": 315,
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
			"seed": 574773268,
			"version": 2,
			"versionNonce": 1435662952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ km / min / 60 ≠ km / (min / 60)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8vrfqQWV",
			"originalText": "⚠ km / min / 60 ≠ km / (min / 60)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
		},
		{
			"id": "6a5FmW89",
			"type": "rectangle",
			"x": 753.5,
			"y": 1047.9,
			"width": 86,
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
			"seed": 1691166730,
			"version": 2,
			"versionNonce": 1589035032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CrCEgnE3"
				},
				{
					"type": "arrow",
					"id": "C7sJcCnM"
				},
				{
					"type": "arrow",
					"id": "hwRRNm4u"
				},
				{
					"type": "arrow",
					"id": "h4huma5Z"
				},
				{
					"type": "arrow",
					"id": "6EUcrvcJ"
				},
				{
					"type": "arrow",
					"id": "9YvYbNwQ"
				},
				{
					"type": "arrow",
					"id": "uMhJBrLX"
				},
				{
					"type": "arrow",
					"id": "YmWJrH9v"
				},
				{
					"type": "arrow",
					"id": "X2KeRPi3"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2c"
		},
		{
			"id": "CrCEgnE3",
			"type": "text",
			"x": 767.5,
			"y": 1056.9,
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
			"seed": 1845214093,
			"version": 2,
			"versionNonce": 489090408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "運算子",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6a5FmW89",
			"originalText": "運算子",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2d"
		},
		{
			"id": "E9K5YBRZ",
			"type": "rectangle",
			"x": 899.5,
			"y": 859.55,
			"width": 220,
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
			"seed": 1642410574,
			"version": 2,
			"versionNonce": 1595342104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NcXQmXBT"
				},
				{
					"type": "arrow",
					"id": "hwRRNm4u"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2e"
		},
		{
			"id": "NcXQmXBT",
			"type": "text",
			"x": 911.5,
			"y": 866.55,
			"width": 196,
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
			"seed": 703006457,
			"version": 2,
			"versionNonce": 2142568552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "45 / 60 → 0.75（比例）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "E9K5YBRZ",
			"originalText": "45 / 60 → 0.75（比例）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2f"
		},
		{
			"id": "tWjCgAZP",
			"type": "rectangle",
			"x": 899.5,
			"y": 926.35,
			"width": 411,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"XtweWLEt"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 583412260,
			"version": 2,
			"versionNonce": 1114085912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wyxU2JHW"
				},
				{
					"type": "arrow",
					"id": "h4huma5Z"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2g"
		},
		{
			"id": "wyxU2JHW",
			"type": "text",
			"x": 911.5,
			"y": 933.35,
			"width": 387,
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
				"XtweWLEt"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1106234943,
			"version": 2,
			"versionNonce": 755544936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "6 / 3 → 2.0、6 // 3 → 2：/ 一定得 float，兩個\nint 做 // 得 int",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tWjCgAZP",
			"originalText": "6 / 3 → 2.0、6 // 3 → 2：/ 一定得 float，兩個\nint 做 // 得 int",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2h"
		},
		{
			"id": "685qiBXQ",
			"type": "rectangle",
			"x": 899.5,
			"y": 994.35,
			"width": 208,
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
			"seed": 1866198477,
			"version": 2,
			"versionNonce": 194811672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "J5YYQRW9"
				},
				{
					"type": "arrow",
					"id": "6EUcrvcJ"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2i"
		},
		{
			"id": "J5YYQRW9",
			"type": "text",
			"x": 911.5,
			"y": 1001.35,
			"width": 184,
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
			"seed": 2125371294,
			"version": 2,
			"versionNonce": 2070808168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "45 // 60 → 0（floor）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "685qiBXQ",
			"originalText": "45 // 60 → 0（floor）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2j"
		},
		{
			"id": "MdhtXC5x",
			"type": "rectangle",
			"x": 899.5,
			"y": 1061.15,
			"width": 403,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"VnYyynDc"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1513514782,
			"version": 2,
			"versionNonce": 1059714072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YDwf3z8P"
				},
				{
					"type": "arrow",
					"id": "9YvYbNwQ"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2k"
		},
		{
			"id": "YDwf3z8P",
			"type": "text",
			"x": 911.5,
			"y": 1068.15,
			"width": 379,
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
				"VnYyynDc"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1273896748,
			"version": 2,
			"versionNonce": 397474152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "83 // 60 → 1；83 % 60 → 23（1 小時 23 分）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MdhtXC5x",
			"originalText": "83 // 60 → 1；83 % 60 → 23（1 小時 23 分）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2l"
		},
		{
			"id": "PkfsYb78",
			"type": "rectangle",
			"x": 899.5,
			"y": 1109.15,
			"width": 119,
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
			"seed": 1622936928,
			"version": 2,
			"versionNonce": 855879960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "i2i5mTbp"
				},
				{
					"type": "arrow",
					"id": "uMhJBrLX"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2m"
		},
		{
			"id": "i2i5mTbp",
			"type": "text",
			"x": 911.5,
			"y": 1116.15,
			"width": 95,
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
			"seed": 1195320565,
			"version": 2,
			"versionNonce": 891128936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "3 ** 2 → 9",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PkfsYb78",
			"originalText": "3 ** 2 → 9",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2n"
		},
		{
			"id": "feCtuy8d",
			"type": "rectangle",
			"x": 899.5,
			"y": 1175.95,
			"width": 280,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"zXLGhJy7"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 765483627,
			"version": 2,
			"versionNonce": 1587400216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bVQDkECS"
				},
				{
					"type": "arrow",
					"id": "YmWJrH9v"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2o"
		},
		{
			"id": "bVQDkECS",
			"type": "text",
			"x": 911.5,
			"y": 1182.95,
			"width": 256,
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
				"zXLGhJy7"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1121982551,
			"version": 2,
			"versionNonce": 1031782248,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "2 + 3 * 4 → 14（先乘除後加減）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "feCtuy8d",
			"originalText": "2 + 3 * 4 → 14（先乘除後加減）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2p"
		},
		{
			"id": "rJEZbqXU",
			"type": "rectangle",
			"x": 899.5,
			"y": 1242.75,
			"width": 274,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "dashed",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"fJwc7XeF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 848956861,
			"version": 2,
			"versionNonce": 720128792,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Ey3xhs9x"
				},
				{
					"type": "arrow",
					"id": "X2KeRPi3"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2q"
		},
		{
			"id": "Ey3xhs9x",
			"type": "text",
			"x": 911.5,
			"y": 1249.75,
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
			"groupIds": [
				"fJwc7XeF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 830248686,
			"version": 2,
			"versionNonce": 19108456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠★ 次方是 **，^ 是 XOR〔C〕",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rJEZbqXU",
			"originalText": "⚠★ 次方是 **，^ 是 XOR〔C〕",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2r"
		},
		{
			"id": "y8rsWkhK",
			"type": "rectangle",
			"x": 753.5,
			"y": 1330.3,
			"width": 100,
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
			"seed": 1537716491,
			"version": 2,
			"versionNonce": 1113794584,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aFspiPSA"
				},
				{
					"type": "arrow",
					"id": "QAQjkUdS"
				},
				{
					"type": "arrow",
					"id": "RLs2vnFA"
				},
				{
					"type": "arrow",
					"id": "AMZLGL7s"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2s"
		},
		{
			"id": "aFspiPSA",
			"type": "text",
			"x": 767.5,
			"y": 1339.3,
			"width": 72,
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
			"seed": 2043011048,
			"version": 2,
			"versionNonce": 1725236584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "f-string",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "y8rsWkhK",
			"originalText": "f-string",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2t"
		},
		{
			"id": "Qw9W4S7G",
			"type": "rectangle",
			"x": 913.5,
			"y": 1309.55,
			"width": 339,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"rPH8wQwF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1787781050,
			"version": 2,
			"versionNonce": 1626760472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xL8Y54Ci"
				},
				{
					"type": "arrow",
					"id": "RLs2vnFA"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2u"
		},
		{
			"id": "xL8Y54Ci",
			"type": "text",
			"x": 925.5,
			"y": 1316.55,
			"width": 315,
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
				"rPH8wQwF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1261063786,
			"version": 2,
			"versionNonce": 467671144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "f\"{miles:.2f}\" → 7.77；只改顯示，不改值",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Qw9W4S7G",
			"originalText": "f\"{miles:.2f}\" → 7.77；只改顯示，不改值",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2v"
		},
		{
			"id": "ksJgbs3N",
			"type": "rectangle",
			"x": 913.5,
			"y": 1357.55,
			"width": 321,
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
			"seed": 9890277,
			"version": 2,
			"versionNonce": 605684248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mS263Kny"
				},
				{
					"type": "arrow",
					"id": "AMZLGL7s"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2w"
		},
		{
			"id": "mS263Kny",
			"type": "text",
			"x": 925.5,
			"y": 1364.55,
			"width": 297,
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
			"seed": 1480193292,
			"version": 2,
			"versionNonce": 1141951336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "print(miles) → 7.7671375000000005",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ksJgbs3N",
			"originalText": "print(miles) → 7.7671375000000005",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2x"
		},
		{
			"id": "Ub2MtUhz",
			"type": "rectangle",
			"x": 753.5,
			"y": 1424.35,
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
				"qS5hiLap"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1944297913,
			"version": 2,
			"versionNonce": 1522663192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "r4aJxspW"
				},
				{
					"type": "arrow",
					"id": "nfQNWWE3"
				},
				{
					"type": "arrow",
					"id": "WwQ8NVmC"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b2y"
		},
		{
			"id": "r4aJxspW",
			"type": "text",
			"x": 767.5,
			"y": 1433.35,
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
				"qS5hiLap"
			],
			"frameId": null,
			"roundness": null,
			"seed": 245692914,
			"version": 2,
			"versionNonce": 699604584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "浮點數：0.1 + 0.2 → 0.30000000000000004；\n.2f → 0.30",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Ub2MtUhz",
			"originalText": "浮點數：0.1 + 0.2 → 0.30000000000000004；\n.2f → 0.30",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2z"
		},
		{
			"id": "GS7R6Jsq",
			"type": "rectangle",
			"x": 1273.5,
			"y": 1438.25,
			"width": 431,
			"height": 54,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"EEGMC4FZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1519497515,
			"version": 2,
			"versionNonce": 1432509464,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XuKu7ChD"
				},
				{
					"type": "arrow",
					"id": "WwQ8NVmC"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b30"
		},
		{
			"id": "XuKu7ChD",
			"type": "text",
			"x": 1285.5,
			"y": 1445.25,
			"width": 407,
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
				"EEGMC4FZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1611067408,
			"version": 2,
			"versionNonce": 1838354792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "浮點加法不保證結合律：(1e16 + -1e16) + 1.0 → 1.0，\n1e16 + (-1e16 + 1.0) → 0.0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GS7R6Jsq",
			"originalText": "浮點加法不保證結合律：(1e16 + -1e16) + 1.0 → 1.0，\n1e16 + (-1e16 + 1.0) → 0.0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b31"
		},
		{
			"id": "jsYhTsGD",
			"type": "rectangle",
			"x": 753.5,
			"y": 1501.35,
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
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1630867141,
			"version": 2,
			"versionNonce": 904861976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mkJMtwc3"
				},
				{
					"type": "arrow",
					"id": "RbKsAUmr"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b32"
		},
		{
			"id": "mkJMtwc3",
			"type": "text",
			"x": 767.5,
			"y": 1510.35,
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
			"seed": 369873686,
			"version": 2,
			"versionNonce": 922526824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Trip Summary v0.2 三段：取得資料 → 計算衍生值\n→ 顯示報告",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jsYhTsGD",
			"originalText": "Trip Summary v0.2 三段：取得資料 → 計算衍生值\n→ 顯示報告",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b33"
		},
		{
			"id": "e8J6UbdF",
			"type": "rectangle",
			"x": 753.5,
			"y": 1599.1,
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
			"seed": 669244804,
			"version": 2,
			"versionNonce": 1071396376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8UKHYtZn"
				},
				{
					"type": "arrow",
					"id": "Ee2q9AhE"
				},
				{
					"type": "arrow",
					"id": "XqynJ9WG"
				},
				{
					"type": "arrow",
					"id": "34Aw7jEi"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b34"
		},
		{
			"id": "8UKHYtZn",
			"type": "text",
			"x": 767.5,
			"y": 1608.1,
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
			"seed": 1726276527,
			"version": 2,
			"versionNonce": 1673254760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "關係測試",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "e8J6UbdF",
			"originalText": "關係測試",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b35"
		},
		{
			"id": "jSdyNkWL",
			"type": "rectangle",
			"x": 918.5,
			"y": 1578.35,
			"width": 235,
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
			"seed": 638919933,
			"version": 2,
			"versionNonce": 673035032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EwVpewAf"
				},
				{
					"type": "arrow",
					"id": "XqynJ9WG"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b36"
		},
		{
			"id": "EwVpewAf",
			"type": "text",
			"x": 930.5,
			"y": 1585.35,
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
			"seed": 1466891514,
			"version": 2,
			"versionNonce": 941402728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "12.5／90 → 速度減半 8.33",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jSdyNkWL",
			"originalText": "12.5／90 → 速度減半 8.33",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b37"
		},
		{
			"id": "xBLyr52p",
			"type": "rectangle",
			"x": 918.5,
			"y": 1626.35,
			"width": 247,
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
			"seed": 224325946,
			"version": 2,
			"versionNonce": 1697091608,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Ran7sZye"
				},
				{
					"type": "arrow",
					"id": "34Aw7jEi"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b38"
		},
		{
			"id": "Ran7sZye",
			"type": "text",
			"x": 930.5,
			"y": 1633.35,
			"width": 223,
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
			"seed": 1675164219,
			"version": 2,
			"versionNonce": 250289512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "25／90 → 速度加倍回 16.67",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xBLyr52p",
			"originalText": "25／90 → 速度加倍回 16.67",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b39"
		},
		{
			"id": "7D27LAis",
			"type": "rectangle",
			"x": -682.5,
			"y": -732.17,
			"width": 314,
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
			"seed": 436748332,
			"version": 2,
			"versionNonce": 2129513752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ECpTFN4h"
				},
				{
					"type": "arrow",
					"id": "XJLsKLVH"
				},
				{
					"type": "arrow",
					"id": "ftsKYhYL"
				},
				{
					"type": "arrow",
					"id": "amFNzrzx"
				},
				{
					"type": "arrow",
					"id": "pCpRyau3"
				},
				{
					"type": "arrow",
					"id": "XYjxkRiq"
				},
				{
					"type": "arrow",
					"id": "jGQk4J3P"
				},
				{
					"type": "arrow",
					"id": "nVw4nPmD"
				},
				{
					"type": "arrow",
					"id": "8ydjubAs"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3A"
		},
		{
			"id": "ECpTFN4h",
			"type": "text",
			"x": -662.5,
			"y": -720.17,
			"width": 274,
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
			"seed": 775454170,
			"version": 2,
			"versionNonce": 158543976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "電腦基礎：位元表示整數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7D27LAis",
			"originalText": "電腦基礎：位元表示整數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3B"
		},
		{
			"id": "kP3QNssF",
			"type": "rectangle",
			"x": -1030.5,
			"y": -1126.45,
			"width": 272,
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
				"rfp3pj6Z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1669535188,
			"version": 2,
			"versionNonce": 1592027672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Ac5D7mQt"
				},
				{
					"type": "arrow",
					"id": "ftsKYhYL"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3C"
		},
		{
			"id": "Ac5D7mQt",
			"type": "text",
			"x": -1016.5,
			"y": -1117.45,
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
			"groupIds": [
				"rfp3pj6Z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1730747321,
			"version": 2,
			"versionNonce": 1065411432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "bit 兩狀態；1 byte = 8 bits",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kP3QNssF",
			"originalText": "bit 兩狀態；1 byte = 8 bits",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3D"
		},
		{
			"id": "sgnV6znN",
			"type": "rectangle",
			"x": -1028.5,
			"y": -1051.2,
			"width": 270,
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
				"5i54zbAL"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1516454533,
			"version": 2,
			"versionNonce": 536831768,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2JeuZvNE"
				},
				{
					"type": "arrow",
					"id": "amFNzrzx"
				},
				{
					"type": "arrow",
					"id": "f2WtnNt7"
				},
				{
					"type": "arrow",
					"id": "jGxzg55V"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3E"
		},
		{
			"id": "2JeuZvNE",
			"type": "text",
			"x": -1014.5,
			"y": -1042.2,
			"width": 242,
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
				"5i54zbAL"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1971572162,
			"version": 2,
			"versionNonce": 1868576360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "權重 128 64 32 16 8 4 2 1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sgnV6znN",
			"originalText": "權重 128 64 32 16 8 4 2 1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3F"
		},
		{
			"id": "mh7F65vV",
			"type": "rectangle",
			"x": -1324.5,
			"y": -1071.95,
			"width": 236,
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
			"seed": 966894379,
			"version": 2,
			"versionNonce": 1588773912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7VNkyc2v"
				},
				{
					"type": "arrow",
					"id": "f2WtnNt7"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3G"
		},
		{
			"id": "7VNkyc2v",
			"type": "text",
			"x": -1312.5,
			"y": -1064.95,
			"width": 212,
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
			"seed": 1951138263,
			"version": 2,
			"versionNonce": 769468776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "00001101 = 8 + 4 + 1 = 13",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mh7F65vV",
			"originalText": "00001101 = 8 + 4 + 1 = 13",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3H"
		},
		{
			"id": "ALWbWgZA",
			"type": "rectangle",
			"x": -1378.5,
			"y": -1023.95,
			"width": 290,
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
			"seed": 830472236,
			"version": 2,
			"versionNonce": 150110488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aSgnz632"
				},
				{
					"type": "arrow",
					"id": "jGxzg55V"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3I"
		},
		{
			"id": "aSgnz632",
			"type": "text",
			"x": -1366.5,
			"y": -1016.95,
			"width": 266,
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
			"seed": 1644286978,
			"version": 2,
			"versionNonce": 373537896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "編碼：選不超過的最大權重（貪婪）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ALWbWgZA",
			"originalText": "編碼：選不超過的最大權重（貪婪）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3J"
		},
		{
			"id": "Yw82CRr6",
			"type": "rectangle",
			"x": -956.5,
			"y": -897.4,
			"width": 198,
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
			"seed": 562581779,
			"version": 2,
			"versionNonce": 775069208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Y6yCCfRn"
				},
				{
					"type": "arrow",
					"id": "pCpRyau3"
				},
				{
					"type": "arrow",
					"id": "wCEuAAwF"
				},
				{
					"type": "arrow",
					"id": "fimTBeCx"
				},
				{
					"type": "arrow",
					"id": "Wy6KKgGT"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3K"
		},
		{
			"id": "Y6yCCfRn",
			"type": "text",
			"x": -942.5,
			"y": -888.4,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 943835028,
			"version": 2,
			"versionNonce": 2053107560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "n bits → 2ⁿ 種圖樣",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Yw82CRr6",
			"originalText": "n bits → 2ⁿ 種圖樣",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3L"
		},
		{
			"id": "PqCZwLE4",
			"type": "rectangle",
			"x": -1213.5,
			"y": -975.95,
			"width": 197,
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
			"seed": 5049922,
			"version": 2,
			"versionNonce": 1332157208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NcTst57X"
				},
				{
					"type": "arrow",
					"id": "wCEuAAwF"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3M"
		},
		{
			"id": "NcTst57X",
			"type": "text",
			"x": -1201.5,
			"y": -968.95,
			"width": 173,
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
			"seed": 1431154595,
			"version": 2,
			"versionNonce": 310231656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "unsigned：0 ～ 2ⁿ − 1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PqCZwLE4",
			"originalText": "unsigned：0 ～ 2ⁿ − 1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3N"
		},
		{
			"id": "2XYCvadH",
			"type": "rectangle",
			"x": -1417.5,
			"y": -909.15,
			"width": 401,
			"height": 54,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"hhNSHus4"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 21258829,
			"version": 2,
			"versionNonce": 788789272,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7P5iqSzG"
				},
				{
					"type": "arrow",
					"id": "fimTBeCx"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3O"
		},
		{
			"id": "7P5iqSzG",
			"type": "text",
			"x": -1405.5,
			"y": -902.15,
			"width": 377,
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
				"hhNSHus4"
			],
			"frameId": null,
			"roundness": null,
			"seed": 524365575,
			"version": 2,
			"versionNonce": 761869672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "8 bits：256 種，0–255；16 bits：65,536 種，\n0–65,535",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2XYCvadH",
			"originalText": "8 bits：256 種，0–255；16 bits：65,536 種，\n0–65,535",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3P"
		},
		{
			"id": "eSYyGgNX",
			"type": "rectangle",
			"x": -1448.5,
			"y": -822.35,
			"width": 432,
			"height": 54,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"89sBYV75"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1453242935,
			"version": 2,
			"versionNonce": 553465112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mhhKKUsD"
				},
				{
					"type": "arrow",
					"id": "Wy6KKgGT"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3Q"
		},
		{
			"id": "mhhKKUsD",
			"type": "text",
			"x": -1436.5,
			"y": -815.35,
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
				"89sBYV75"
			],
			"frameId": null,
			"roundness": null,
			"seed": 303362079,
			"version": 2,
			"versionNonce": 1617840232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "兩個 8-bit unsigned 相加最大 510；9-bit 二補數只到\n255，裝不下",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eSYyGgNX",
			"originalText": "兩個 8-bit unsigned 相加最大 510；9-bit 二補數只到\n255，裝不下",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3R"
		},
		{
			"id": "ccv8JrrK",
			"type": "rectangle",
			"x": -947.5,
			"y": -656.8,
			"width": 189,
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
				"CWysNLbE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 724941425,
			"version": 2,
			"versionNonce": 1522979352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xNBzUqS8"
				},
				{
					"type": "arrow",
					"id": "XYjxkRiq"
				},
				{
					"type": "arrow",
					"id": "UAiYY68H"
				},
				{
					"type": "arrow",
					"id": "urNiWWe7"
				},
				{
					"type": "arrow",
					"id": "S9LFjYxJ"
				},
				{
					"type": "arrow",
					"id": "8pegfZk9"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3S"
		},
		{
			"id": "xNBzUqS8",
			"type": "text",
			"x": -933.5,
			"y": -647.8,
			"width": 161,
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
				"CWysNLbE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 594823622,
			"version": 2,
			"versionNonce": 928578408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Two's complement",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ccv8JrrK",
			"originalText": "Two's complement",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3T"
		},
		{
			"id": "LJmyrSMv",
			"type": "rectangle",
			"x": -1409.5,
			"y": -754.35,
			"width": 402,
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
			"seed": 340716065,
			"version": 2,
			"versionNonce": 1129631512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YzDqaG73"
				},
				{
					"type": "arrow",
					"id": "UAiYY68H"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3U"
		},
		{
			"id": "YzDqaG73",
			"type": "text",
			"x": -1397.5,
			"y": -747.35,
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
			"seed": 1057473610,
			"version": 2,
			"versionNonce": 1685409384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "−5：00000101 反轉 → 11111010 加 1 → 11111011",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LJmyrSMv",
			"originalText": "−5：00000101 反轉 → 11111010 加 1 → 11111011",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3V"
		},
		{
			"id": "nB5k84Z4",
			"type": "rectangle",
			"x": -1436.5,
			"y": -706.35,
			"width": 429,
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
			"seed": 163578876,
			"version": 2,
			"versionNonce": 1125854232,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xYnZRT58"
				},
				{
					"type": "arrow",
					"id": "urNiWWe7"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3W"
		},
		{
			"id": "xYnZRT58",
			"type": "text",
			"x": -1424.5,
			"y": -699.35,
			"width": 405,
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
			"seed": 1180098037,
			"version": 2,
			"versionNonce": 1888436584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "最高位權重 −128：−128 + 64 + 32 + 16 + 8 + 2 + 1\n= −5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nB5k84Z4",
			"originalText": "最高位權重 −128：−128 + 64 + 32 + 16 + 8 + 2 + 1\n= −5",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3X"
		},
		{
			"id": "Vy2Gtx22",
			"type": "rectangle",
			"x": -1401.5,
			"y": -619.55,
			"width": 394,
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
				"53iEuzXi"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1445856968,
			"version": 2,
			"versionNonce": 336455960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bJgvWbis"
				},
				{
					"type": "arrow",
					"id": "S9LFjYxJ"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3Y"
		},
		{
			"id": "bJgvWbis",
			"type": "text",
			"x": -1389.5,
			"y": -612.55,
			"width": 370,
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
				"53iEuzXi"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1759319616,
			"version": 2,
			"versionNonce": 1794298984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "範圍：−2ⁿ⁻¹ ～ 2ⁿ⁻¹ − 1（8 bits：−128 ～ 127）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Vy2Gtx22",
			"originalText": "範圍：−2ⁿ⁻¹ ～ 2ⁿ⁻¹ − 1（8 bits：−128 ～ 127）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3Z"
		},
		{
			"id": "rGJUksRw",
			"type": "rectangle",
			"x": -1305.5,
			"y": -552.75,
			"width": 298,
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
				"YNeE7Kix"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 438678712,
			"version": 2,
			"versionNonce": 295765528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ncq7mUBp"
				},
				{
					"type": "arrow",
					"id": "8pegfZk9"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3a"
		},
		{
			"id": "ncq7mUBp",
			"type": "text",
			"x": -1293.5,
			"y": -545.75,
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
			"groupIds": [
				"YNeE7Kix"
			],
			"frameId": null,
			"roundness": null,
			"seed": 53800070,
			"version": 2,
			"versionNonce": 426510184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "11111011：unsigned 251／signed −5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rGJUksRw",
			"originalText": "11111011：unsigned 251／signed −5",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3b"
		},
		{
			"id": "gQTQmGqg",
			"type": "rectangle",
			"x": -1226.5,
			"y": -485.95,
			"width": 468,
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
				"ybPq9cqP"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1124450377,
			"version": 2,
			"versionNonce": 147358488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KtjRKDEp"
				},
				{
					"type": "arrow",
					"id": "jGQk4J3P"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3c"
		},
		{
			"id": "KtjRKDEp",
			"type": "text",
			"x": -1212.5,
			"y": -476.95,
			"width": 440,
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
				"ybPq9cqP"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2130994706,
			"version": 2,
			"versionNonce": 675732072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Python int 任意精度：127 + 1 → 128（不會溢位）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gQTQmGqg",
			"originalText": "Python int 任意精度：127 + 1 → 128（不會溢位）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3d"
		},
		{
			"id": "sJ9mBzbM",
			"type": "rectangle",
			"x": -1178.5,
			"y": -412.65,
			"width": 420,
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
				"GuyTY5Yh"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 197816148,
			"version": 2,
			"versionNonce": 133718040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Bu5aEFCg"
				},
				{
					"type": "arrow",
					"id": "nVw4nPmD"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3e"
		},
		{
			"id": "Bu5aEFCg",
			"type": "text",
			"x": -1164.5,
			"y": -403.65,
			"width": 392,
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
				"GuyTY5Yh"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1523893282,
			"version": 2,
			"versionNonce": 1515146600,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "練習：31 → 00011111；10000000 → 128 或\n−128",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sJ9mBzbM",
			"originalText": "練習：31 → 00011111；10000000 → 128 或\n−128",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3f"
		},
		{
			"id": "zb67GXgV",
			"type": "rectangle",
			"x": -1207.5,
			"y": -335.65,
			"width": 449,
			"height": 63,
			"angle": 0,
			"strokeColor": "#5c940d",
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
			"seed": 398187192,
			"version": 2,
			"versionNonce": 790928664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3jvs9MRM"
				},
				{
					"type": "arrow",
					"id": "8ydjubAs"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3g"
		},
		{
			"id": "3jvs9MRM",
			"type": "text",
			"x": -1193.5,
			"y": -326.65,
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
			"seed": 132628373,
			"version": 2,
			"versionNonce": 953245800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ 1 byte = 8 bits（T）；任何數字都用／都能用\n8 bits（F）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zb67GXgV",
			"originalText": "★ 1 byte = 8 bits（T）；任何數字都用／都能用\n8 bits（F）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3h"
		},
		{
			"id": "ubxefJr2",
			"type": "rectangle",
			"x": -619.5,
			"y": 113.85,
			"width": 251,
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
			"seed": 1959843301,
			"version": 2,
			"versionNonce": 2143369752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2Uj5MibU"
				},
				{
					"type": "arrow",
					"id": "TAwVDXzX"
				},
				{
					"type": "arrow",
					"id": "EiqkMuZ4"
				},
				{
					"type": "arrow",
					"id": "L4WsV8VC"
				},
				{
					"type": "arrow",
					"id": "LAgbaRXS"
				},
				{
					"type": "arrow",
					"id": "985uL4d5"
				},
				{
					"type": "arrow",
					"id": "YV6VNwLw"
				},
				{
					"type": "arrow",
					"id": "VPaWqVAc"
				},
				{
					"type": "arrow",
					"id": "CkALCSED"
				},
				{
					"type": "arrow",
					"id": "PUtWWpwf"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3i"
		},
		{
			"id": "2Uj5MibU",
			"type": "text",
			"x": -599.5,
			"y": 125.85,
			"width": 211,
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
			"seed": 862656668,
			"version": 2,
			"versionNonce": 1134105448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q6 AI 實作與驗證",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ubxefJr2",
			"originalText": "Q6 AI 實作與驗證",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3j"
		},
		{
			"id": "G939Qfja",
			"type": "rectangle",
			"x": -1169.5,
			"y": -228.65,
			"width": 474,
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
			"seed": 1151847764,
			"version": 2,
			"versionNonce": 750925592,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UNebvjdF"
				},
				{
					"type": "arrow",
					"id": "EiqkMuZ4"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3k"
		},
		{
			"id": "UNebvjdF",
			"type": "text",
			"x": -1155.5,
			"y": -219.65,
			"width": 446,
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
			"seed": 256211974,
			"version": 2,
			"versionNonce": 552756840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Prompt：只用學過的工具；不要 loops、functions、\npackages、validation",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G939Qfja",
			"originalText": "Prompt：只用學過的工具；不要 loops、functions、\npackages、validation",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3l"
		},
		{
			"id": "V8nUqSkX",
			"type": "rectangle",
			"x": -1118.5,
			"y": -106.9,
			"width": 423,
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
			"seed": 1517828692,
			"version": 2,
			"versionNonce": 1788580888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "22ikYUUb"
				},
				{
					"type": "arrow",
					"id": "L4WsV8VC"
				},
				{
					"type": "arrow",
					"id": "gBxeNuab"
				},
				{
					"type": "arrow",
					"id": "FSMJ7L83"
				},
				{
					"type": "arrow",
					"id": "p4s3aNuy"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3m"
		},
		{
			"id": "22ikYUUb",
			"type": "text",
			"x": -1104.5,
			"y": -97.9,
			"width": 395,
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
			"seed": 1222636766,
			"version": 2,
			"versionNonce": 1302944104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "故意錯誤 candidate 三違規（007／3.5／30）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "V8nUqSkX",
			"originalText": "故意錯誤 candidate 三違規（007／3.5／30）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3n"
		},
		{
			"id": "xNEz3R96",
			"type": "rectangle",
			"x": -1563.5,
			"y": -151.65,
			"width": 385,
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
			"seed": 2057016942,
			"version": 2,
			"versionNonce": 1061245208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NGUv9ANG"
				},
				{
					"type": "arrow",
					"id": "gBxeNuab"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3o"
		},
		{
			"id": "NGUv9ANG",
			"type": "text",
			"x": -1551.5,
			"y": -144.65,
			"width": 361,
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
			"seed": 729203713,
			"version": 2,
			"versionNonce": 1292495976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "int(float()) 截斷 3.5 → 速度 6.00（應 7.00）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xNEz3R96",
			"originalText": "int(float()) 截斷 3.5 → 速度 6.00（應 7.00）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3p"
		},
		{
			"id": "vPbwB6VT",
			"type": "rectangle",
			"x": -1466.5,
			"y": -103.65,
			"width": 288,
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
			"seed": 1777659119,
			"version": 2,
			"versionNonce": 1378315800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BD66T67p"
				},
				{
					"type": "arrow",
					"id": "FSMJ7L83"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3q"
		},
		{
			"id": "BD66T67p",
			"type": "text",
			"x": -1454.5,
			"y": -96.65,
			"width": 264,
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
			"seed": 477233195,
			"version": 2,
			"versionNonce": 1491083112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "除以係數 → 4.83 miles（應 2.17）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vPbwB6VT",
			"originalText": "除以係數 → 4.83 miles（應 2.17）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3r"
		},
		{
			"id": "uGUB6u92",
			"type": "rectangle",
			"x": -1288.5,
			"y": -55.65,
			"width": 110,
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
			"seed": 2023354993,
			"version": 2,
			"versionNonce": 1010952984,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kifSpSg4"
				},
				{
					"type": "arrow",
					"id": "p4s3aNuy"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3s"
		},
		{
			"id": "kifSpSg4",
			"type": "text",
			"x": -1276.5,
			"y": -48.65,
			"width": 86,
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
			"seed": 1481588831,
			"version": 2,
			"versionNonce": 293073512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "沒印 route",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uGUB6u92",
			"originalText": "沒印 route",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3t"
		},
		{
			"id": "diArVRrX",
			"type": "rectangle",
			"x": -800.5,
			"y": 61.1,
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
			"seed": 2084428745,
			"version": 2,
			"versionNonce": 1476708376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XAQLrGCG"
				},
				{
					"type": "arrow",
					"id": "LAgbaRXS"
				},
				{
					"type": "arrow",
					"id": "8vkAinec"
				},
				{
					"type": "arrow",
					"id": "XPFmmDHW"
				},
				{
					"type": "arrow",
					"id": "utaXfKtn"
				},
				{
					"type": "arrow",
					"id": "J5YcnEY9"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3u"
		},
		{
			"id": "XAQLrGCG",
			"type": "text",
			"x": -786.5,
			"y": 70.1,
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
			"seed": 1588980715,
			"version": 2,
			"versionNonce": 765289832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "測試矩陣",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "diArVRrX",
			"originalText": "測試矩陣",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3v"
		},
		{
			"id": "83K3AWmd",
			"type": "rectangle",
			"x": -1076.5,
			"y": -7.65,
			"width": 216,
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
			"seed": 1512092311,
			"version": 2,
			"versionNonce": 291767576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8CUfjTRV"
				},
				{
					"type": "arrow",
					"id": "8vkAinec"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3w"
		},
		{
			"id": "8CUfjTRV",
			"type": "text",
			"x": -1064.5,
			"y": -0.65,
			"width": 192,
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
			"seed": 1464973235,
			"version": 2,
			"versionNonce": 714897512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "12.5／45 → 7.77／16.67",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "83K3AWmd",
			"originalText": "12.5／45 → 7.77／16.67",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3x"
		},
		{
			"id": "Z4ZiPyjv",
			"type": "rectangle",
			"x": -1170.5,
			"y": 40.35,
			"width": 310,
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
			"seed": 2088137505,
			"version": 2,
			"versionNonce": 903062040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qFYbLuZS"
				},
				{
					"type": "arrow",
					"id": "XPFmmDHW"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b3y"
		},
		{
			"id": "qFYbLuZS",
			"type": "text",
			"x": -1158.5,
			"y": 47.35,
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
			"seed": 21470878,
			"version": 2,
			"versionNonce": 2084645736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "0／30 → 0.00／0.00（零距離有效）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Z4ZiPyjv",
			"originalText": "0／30 → 0.00／0.00（零距離有效）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3z"
		},
		{
			"id": "uBiukY9d",
			"type": "rectangle",
			"x": -1086.5,
			"y": 88.35,
			"width": 226,
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
			"seed": 810986403,
			"version": 2,
			"versionNonce": 1145544472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RVVRV8uG"
				},
				{
					"type": "arrow",
					"id": "utaXfKtn"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b40"
		},
		{
			"id": "RVVRV8uG",
			"type": "text",
			"x": -1074.5,
			"y": 95.35,
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
			"seed": 714648066,
			"version": 2,
			"versionNonce": 1020755560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "60／60 → 37.28／60.00",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uBiukY9d",
			"originalText": "60／60 → 37.28／60.00",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b41"
		},
		{
			"id": "C9cXkMEj",
			"type": "rectangle",
			"x": -1063.5,
			"y": 136.35,
			"width": 203,
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
			"seed": 1677338627,
			"version": 2,
			"versionNonce": 1026817048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "V4JbRi6c"
				},
				{
					"type": "arrow",
					"id": "J5YcnEY9"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b42"
		},
		{
			"id": "V4JbRi6c",
			"type": "text",
			"x": -1051.5,
			"y": 143.35,
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
			"seed": 1879837108,
			"version": 2,
			"versionNonce": 1563128168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "3.5／30 → 2.17／7.00",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "C9cXkMEj",
			"originalText": "3.5／30 → 2.17／7.00",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b43"
		},
		{
			"id": "f74dZrL8",
			"type": "rectangle",
			"x": -989.5,
			"y": 184.35,
			"width": 294,
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
			"seed": 410597734,
			"version": 2,
			"versionNonce": 1921825048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dUWti3uy"
				},
				{
					"type": "arrow",
					"id": "985uL4d5"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b44"
		},
		{
			"id": "dUWti3uy",
			"type": "text",
			"x": -975.5,
			"y": 193.35,
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
			"seed": 1367261347,
			"version": 2,
			"versionNonce": 1418265704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不要改 expected 去配合錯程式",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "f74dZrL8",
			"originalText": "不要改 expected 去配合錯程式",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b45"
		},
		{
			"id": "ivCiebqZ",
			"type": "rectangle",
			"x": -1129.5,
			"y": 238.85,
			"width": 434,
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
			"seed": 1679709881,
			"version": 2,
			"versionNonce": 1472583192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BHdpqgZX"
				},
				{
					"type": "arrow",
					"id": "YV6VNwLw"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b46"
		},
		{
			"id": "BHdpqgZX",
			"type": "text",
			"x": -1115.5,
			"y": 247.85,
			"width": 406,
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
			"seed": 1153851667,
			"version": 2,
			"versionNonce": 1354512232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Workflow：Specify → Predict → Generate →\nInspect → Run tests → Revise",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ivCiebqZ",
			"originalText": "Workflow：Specify → Predict → Generate →\nInspect → Run tests → Revise",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b47"
		},
		{
			"id": "P44gYbYk",
			"type": "rectangle",
			"x": -1018.5,
			"y": 315.85,
			"width": 323,
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
			"seed": 1320743643,
			"version": 2,
			"versionNonce": 1372803864,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qDr759K4"
				},
				{
					"type": "arrow",
					"id": "VPaWqVAc"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b48"
		},
		{
			"id": "qDr759K4",
			"type": "text",
			"x": -1004.5,
			"y": 324.85,
			"width": 295,
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
			"seed": 549005787,
			"version": 2,
			"versionNonce": 1712392808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "延伸欄位：12,500.00 m 或 0.75 h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "P44gYbYk",
			"originalText": "延伸欄位：12,500.00 m 或 0.75 h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b49"
		},
		{
			"id": "GS8BWqYW",
			"type": "rectangle",
			"x": -1111.5,
			"y": 370.35,
			"width": 416,
			"height": 63,
			"angle": 0,
			"strokeColor": "#9c36b5",
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
			"seed": 2011110109,
			"version": 2,
			"versionNonce": 120139800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "58PPKiuM"
				},
				{
					"type": "arrow",
					"id": "CkALCSED"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4A"
		},
		{
			"id": "58PPKiuM",
			"type": "text",
			"x": -1097.5,
			"y": 379.35,
			"width": 388,
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
			"seed": 534918302,
			"version": 2,
			"versionNonce": 1062436200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Git：commit Add tested trip summary with\nexplicit units；⚠ 不要 force push",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GS8BWqYW",
			"originalText": "Git：commit Add tested trip summary with\nexplicit units；⚠ 不要 force push",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4B"
		},
		{
			"id": "NcriqK7R",
			"type": "rectangle",
			"x": -1148.5,
			"y": 447.35,
			"width": 453,
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
			"seed": 1417314155,
			"version": 2,
			"versionNonce": 800812312,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WuVhkb6a"
				},
				{
					"type": "arrow",
					"id": "PUtWWpwf"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4C"
		},
		{
			"id": "WuVhkb6a",
			"type": "text",
			"x": -1134.5,
			"y": 456.35,
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
			"seed": 2033315565,
			"version": 2,
			"versionNonce": 1305448552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "專題點子：印刷費 10 × 2.5 = 25；讀書 20 × 3 /\n60 = 1 h；用電 100 × 2 / 1000 = 0.2 kWh",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NcriqK7R",
			"originalText": "專題點子：印刷費 10 × 2.5 = 25；讀書 20 × 3 /\n60 = 1 h；用電 100 × 2 / 1000 = 0.2 kWh",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4D"
		},
		{
			"id": "DZQuBCYH",
			"type": "rectangle",
			"x": -584.5,
			"y": 864.38,
			"width": 216,
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
			"seed": 1288649255,
			"version": 2,
			"versionNonce": 1694370328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HzdNMeqz"
				},
				{
					"type": "arrow",
					"id": "SLdfHkQH"
				},
				{
					"type": "arrow",
					"id": "TjTZCxgd"
				},
				{
					"type": "arrow",
					"id": "xMUfducC"
				},
				{
					"type": "arrow",
					"id": "J5SEjYCZ"
				},
				{
					"type": "arrow",
					"id": "8C35eaQL"
				},
				{
					"type": "arrow",
					"id": "zh2b9Dhv"
				},
				{
					"type": "arrow",
					"id": "rdCW66BB"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4E"
		},
		{
			"id": "HzdNMeqz",
			"type": "text",
			"x": -564.5,
			"y": 876.38,
			"width": 176,
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
			"seed": 1990030662,
			"version": 2,
			"versionNonce": 2035368808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "選讀：精確規則",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DZQuBCYH",
			"originalText": "選讀：精確規則",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4F"
		},
		{
			"id": "gWcv8RiX",
			"type": "rectangle",
			"x": -868.5,
			"y": 637.5,
			"width": 208,
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
			"seed": 1667366950,
			"version": 2,
			"versionNonce": 1910834968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Jex2cNpg"
				},
				{
					"type": "arrow",
					"id": "TjTZCxgd"
				},
				{
					"type": "arrow",
					"id": "SerchQEW"
				},
				{
					"type": "arrow",
					"id": "Kp4HeL65"
				},
				{
					"type": "arrow",
					"id": "8XhjeEYe"
				},
				{
					"type": "arrow",
					"id": "fSunhLMK"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4G"
		},
		{
			"id": "Jex2cNpg",
			"type": "text",
			"x": -854.5,
			"y": 646.5,
			"width": 180,
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
			"seed": 109856330,
			"version": 2,
			"versionNonce": 1344575080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "截斷 vs floor vs ceil",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gWcv8RiX",
			"originalText": "截斷 vs floor vs ceil",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4H"
		},
		{
			"id": "yTbfPMP4",
			"type": "rectangle",
			"x": -1128.5,
			"y": 554.35,
			"width": 200,
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
			"seed": 983436378,
			"version": 2,
			"versionNonce": 585393176,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "T3BQzXfy"
				},
				{
					"type": "arrow",
					"id": "SerchQEW"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4I"
		},
		{
			"id": "T3BQzXfy",
			"type": "text",
			"x": -1116.5,
			"y": 561.35,
			"width": 176,
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
			"seed": 480763196,
			"version": 2,
			"versionNonce": 924158312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "int(-1.7) → −1（向零）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yTbfPMP4",
			"originalText": "int(-1.7) → −1（向零）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4J"
		},
		{
			"id": "pbyBf9dc",
			"type": "rectangle",
			"x": -1298.5,
			"y": 602.35,
			"width": 370,
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
			"seed": 1159397787,
			"version": 2,
			"versionNonce": 368058648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RaK77CBP"
				},
				{
					"type": "arrow",
					"id": "Kp4HeL65"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4K"
		},
		{
			"id": "RaK77CBP",
			"type": "text",
			"x": -1286.5,
			"y": 609.35,
			"width": 346,
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
			"seed": 1557555916,
			"version": 2,
			"versionNonce": 426777704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "math.floor(-1.7) → −2；math.ceil(-1.7) → −1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pbyBf9dc",
			"originalText": "math.floor(-1.7) → −2；math.ceil(-1.7) → −1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4L"
		},
		{
			"id": "pMTSKS2G",
			"type": "rectangle",
			"x": -1208.5,
			"y": 650.35,
			"width": 280,
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
			"seed": 2064018170,
			"version": 2,
			"versionNonce": 175914520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bTpW3DNv"
				},
				{
					"type": "arrow",
					"id": "8XhjeEYe"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4M"
		},
		{
			"id": "bTpW3DNv",
			"type": "text",
			"x": -1196.5,
			"y": 657.35,
			"width": 256,
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
			"seed": 123394890,
			"version": 2,
			"versionNonce": 419450728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "-7 // 3 → −3；int(-7 / 3) → −2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pMTSKS2G",
			"originalText": "-7 // 3 → −3；int(-7 / 3) → −2",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4N"
		},
		{
			"id": "JRgz6zNc",
			"type": "rectangle",
			"x": -1364.5,
			"y": 717.15,
			"width": 436,
			"height": 54,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"MfZ6rwev"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1845852312,
			"version": 2,
			"versionNonce": 830257944,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vGQsZznQ"
				},
				{
					"type": "arrow",
					"id": "fSunhLMK"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4O"
		},
		{
			"id": "vGQsZznQ",
			"type": "text",
			"x": -1352.5,
			"y": 724.15,
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
			"groupIds": [
				"MfZ6rwev"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1783828248,
			"version": 2,
			"versionNonce": 1041375848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "-7 % 3 → 2；b ≠ 0 時 a == (a // b) * b + a % b 一\n定成立",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JRgz6zNc",
			"originalText": "-7 % 3 → 2；b ≠ 0 時 a == (a // b) * b + a % b 一\n定成立",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4P"
		},
		{
			"id": "s6q3T4cE",
			"type": "rectangle",
			"x": -1125.5,
			"y": 785.15,
			"width": 465,
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
			"seed": 1904627932,
			"version": 2,
			"versionNonce": 2103810072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "C6MmFu7t"
				},
				{
					"type": "arrow",
					"id": "xMUfducC"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4Q"
		},
		{
			"id": "C6MmFu7t",
			"type": "text",
			"x": -1111.5,
			"y": 794.15,
			"width": 437,
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
			"seed": 1575874594,
			"version": 2,
			"versionNonce": 661755240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "round(2.5) → 2；round(3.5) → 4（tie to even）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "s6q3T4cE",
			"originalText": "round(2.5) → 2；round(3.5) → 4（tie to even）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4R"
		},
		{
			"id": "dULBiTSr",
			"type": "rectangle",
			"x": -728.5,
			"y": 860.4,
			"width": 68,
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
			"seed": 814124649,
			"version": 2,
			"versionNonce": 1915409688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JBPB47Ub"
				},
				{
					"type": "arrow",
					"id": "J5SEjYCZ"
				},
				{
					"type": "arrow",
					"id": "HCAMaqLY"
				},
				{
					"type": "arrow",
					"id": "j4rdfeNj"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4S"
		},
		{
			"id": "JBPB47Ub",
			"type": "text",
			"x": -714.5,
			"y": 869.4,
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
			"seed": 771259151,
			"version": 2,
			"versionNonce": 980068456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "次方",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dULBiTSr",
			"originalText": "次方",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4T"
		},
		{
			"id": "vNAgGQeT",
			"type": "rectangle",
			"x": -1049.5,
			"y": 839.65,
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
			"seed": 163475896,
			"version": 2,
			"versionNonce": 1967157784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DsVatpd7"
				},
				{
					"type": "arrow",
					"id": "HCAMaqLY"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4U"
		},
		{
			"id": "DsVatpd7",
			"type": "text",
			"x": -1037.5,
			"y": 846.65,
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
			"seed": 940825149,
			"version": 2,
			"versionNonce": 1388927848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "2 ** 3 ** 2 → 512（右結合）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vNAgGQeT",
			"originalText": "2 ** 3 ** 2 → 512（右結合）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4V"
		},
		{
			"id": "t6VqnNRW",
			"type": "rectangle",
			"x": -1052.5,
			"y": 887.65,
			"width": 264,
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
			"seed": 2106624847,
			"version": 2,
			"versionNonce": 496660248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FCqerJZj"
				},
				{
					"type": "arrow",
					"id": "j4rdfeNj"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4W"
		},
		{
			"id": "FCqerJZj",
			"type": "text",
			"x": -1040.5,
			"y": 894.65,
			"width": 240,
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
			"seed": 683334725,
			"version": 2,
			"versionNonce": 1926868584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "-3 ** 2 → −9；(-3) ** 2 → 9",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "t6VqnNRW",
			"originalText": "-3 ** 2 → −9；(-3) ** 2 → 9",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4X"
		},
		{
			"id": "CfFkRgqG",
			"type": "rectangle",
			"x": -828.5,
			"y": 954.45,
			"width": 168,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"9ZyVGhKS"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1110414415,
			"version": 2,
			"versionNonce": 61656088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gUmzVwFT"
				},
				{
					"type": "arrow",
					"id": "8C35eaQL"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4Y"
		},
		{
			"id": "gUmzVwFT",
			"type": "text",
			"x": -814.5,
			"y": 963.45,
			"width": 140,
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
				"9ZyVGhKS"
			],
			"frameId": null,
			"roundness": null,
			"seed": 32353316,
			"version": 2,
			"versionNonce": 1936171368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "x += y 更新數值",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CfFkRgqG",
			"originalText": "x += y 更新數值",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4Z"
		},
		{
			"id": "7jfXRCpa",
			"type": "rectangle",
			"x": -1101.5,
			"y": 1008.95,
			"width": 441,
			"height": 63,
			"angle": 0,
			"strokeColor": "#e67700",
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
			"seed": 178419111,
			"version": 2,
			"versionNonce": 292260120,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "taAJZZWq"
				},
				{
					"type": "arrow",
					"id": "zh2b9Dhv"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4a"
		},
		{
			"id": "taAJZZWq",
			"type": "text",
			"x": -1087.5,
			"y": 1017.95,
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
			"seed": 141217181,
			"version": 2,
			"versionNonce": 868168808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ result = print(\"Hello\") → 印 Hello，result 是\nNone",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7jfXRCpa",
			"originalText": "★ result = print(\"Hello\") → 印 Hello，result 是\nNone",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4b"
		},
		{
			"id": "sC6XcKEC",
			"type": "rectangle",
			"x": -1030.5,
			"y": 1104.75,
			"width": 370,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e67700",
			"backgroundColor": "#fff9db",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"hndXk3FD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 552175910,
			"version": 2,
			"versionNonce": 1380623896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4ssmWssg"
				},
				{
					"type": "arrow",
					"id": "rdCW66BB"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4c"
		},
		{
			"id": "4ssmWssg",
			"type": "text",
			"x": -1016.5,
			"y": 1113.75,
			"width": 342,
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
				"hndXk3FD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1805625839,
			"version": 2,
			"versionNonce": 1236035432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "f\"{12.345:.2f}\" → \"12.35\"，型態是 str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sC6XcKEC",
			"originalText": "f\"{12.345:.2f}\" → \"12.35\"，型態是 str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4d"
		},
		{
			"id": "P7QhBDLR",
			"type": "rectangle",
			"x": 1086.5,
			"y": -840.35,
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
				"4XkTsYnH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1242712686,
			"version": 2,
			"versionNonce": 1128145688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "u8Uuv6JU"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4e"
		},
		{
			"id": "u8Uuv6JU",
			"type": "text",
			"x": 1093.5,
			"y": -837.35,
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
				"4XkTsYnH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 825254827,
			"version": 2,
			"versionNonce": 830159464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q006",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "P7QhBDLR",
			"originalText": "Q006",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4f"
		},
		{
			"id": "mSjRFyZx",
			"type": "rectangle",
			"x": 1077.5,
			"y": -613.05,
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
				"7gzqFGwC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 271380543,
			"version": 2,
			"versionNonce": 582615064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "acWH9tM3"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4g"
		},
		{
			"id": "acWH9tM3",
			"type": "text",
			"x": 1084.5,
			"y": -610.05,
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
				"7gzqFGwC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 533106374,
			"version": 2,
			"versionNonce": 2113383784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T015",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mSjRFyZx",
			"originalText": "T015",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4h"
		},
		{
			"id": "hUTL3Ks2",
			"type": "rectangle",
			"x": 950.5,
			"y": -378.25,
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
				"WbVqWxEu"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1737377491,
			"version": 2,
			"versionNonce": 1085422872,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hBdJSwxJ"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4i"
		},
		{
			"id": "hBdJSwxJ",
			"type": "text",
			"x": 957.5,
			"y": -375.25,
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
				"WbVqWxEu"
			],
			"frameId": null,
			"roundness": null,
			"seed": 726710658,
			"version": 2,
			"versionNonce": 141410408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T016 Q007",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hUTL3Ks2",
			"originalText": "T016 Q007",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4j"
		},
		{
			"id": "iwCRg3sA",
			"type": "rectangle",
			"x": 1127.5,
			"y": -304.95,
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
				"zkugmic5"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1623722511,
			"version": 2,
			"versionNonce": 1318771224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zuPMviLz"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4k"
		},
		{
			"id": "zuPMviLz",
			"type": "text",
			"x": 1134.5,
			"y": -301.95,
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
				"zkugmic5"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1007536183,
			"version": 2,
			"versionNonce": 547976040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q027",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iwCRg3sA",
			"originalText": "Q027",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4l"
		},
		{
			"id": "7L2PfpSX",
			"type": "rectangle",
			"x": 971.5,
			"y": -95.65,
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
				"tUmvV89t"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 621753870,
			"version": 2,
			"versionNonce": 795334424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iLeUi9FW"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4m"
		},
		{
			"id": "iLeUi9FW",
			"type": "text",
			"x": 978.5,
			"y": -92.65,
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
				"tUmvV89t"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2131857094,
			"version": 2,
			"versionNonce": 1022805608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T068",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7L2PfpSX",
			"originalText": "T068",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4n"
		},
		{
			"id": "GPJdxbaX",
			"type": "rectangle",
			"x": 1034.5,
			"y": 49.15,
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
				"UH6TmpLf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1063325089,
			"version": 2,
			"versionNonce": 1200436248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VTy2xeAZ"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4o"
		},
		{
			"id": "VTy2xeAZ",
			"type": "text",
			"x": 1041.5,
			"y": 52.15,
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
				"UH6TmpLf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2107642877,
			"version": 2,
			"versionNonce": 706853224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T013",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GPJdxbaX",
			"originalText": "T013",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4p"
		},
		{
			"id": "ucH4K6m4",
			"type": "rectangle",
			"x": 981.5,
			"y": 314.45,
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
				"NQDHX784"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1299044283,
			"version": 2,
			"versionNonce": 1291776280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PwnptdK4"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4q"
		},
		{
			"id": "PwnptdK4",
			"type": "text",
			"x": 988.5,
			"y": 317.45,
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
				"NQDHX784"
			],
			"frameId": null,
			"roundness": null,
			"seed": 537880578,
			"version": 2,
			"versionNonce": 997608552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T014",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ucH4K6m4",
			"originalText": "T014",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4r"
		},
		{
			"id": "vzX3itqG",
			"type": "rectangle",
			"x": 963.5,
			"y": 615.2,
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
				"3sBPfUL4"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2113017102,
			"version": 2,
			"versionNonce": 389090840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aTxv9du2"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4s"
		},
		{
			"id": "aTxv9du2",
			"type": "text",
			"x": 970.5,
			"y": 618.2,
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
				"3sBPfUL4"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1542282412,
			"version": 2,
			"versionNonce": 2059435880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q008",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vzX3itqG",
			"originalText": "Q008",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4t"
		},
		{
			"id": "Yp3G5Gtm",
			"type": "rectangle",
			"x": 1155.5,
			"y": 709.25,
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
				"LAvQgJpR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1722199820,
			"version": 2,
			"versionNonce": 1863813912,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G5GEQCKW"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4u"
		},
		{
			"id": "G5GEQCKW",
			"type": "text",
			"x": 1162.5,
			"y": 712.25,
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
				"LAvQgJpR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 806715621,
			"version": 2,
			"versionNonce": 1481396840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Yp3G5Gtm",
			"originalText": "T022",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4v"
		},
		{
			"id": "usfrKjAq",
			"type": "rectangle",
			"x": 1226.5,
			"y": 907.55,
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
				"XtweWLEt"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1041172720,
			"version": 2,
			"versionNonce": 1596352536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AWPWqwHv"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4w"
		},
		{
			"id": "AWPWqwHv",
			"type": "text",
			"x": 1233.5,
			"y": 910.55,
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
				"XtweWLEt"
			],
			"frameId": null,
			"roundness": null,
			"seed": 509471271,
			"version": 2,
			"versionNonce": 1525007720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T018 T019",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "usfrKjAq",
			"originalText": "T018 T019",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4x"
		},
		{
			"id": "JPPKSzm6",
			"type": "rectangle",
			"x": 1259.5,
			"y": 1042.35,
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
				"VnYyynDc"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1437580950,
			"version": 2,
			"versionNonce": 55682328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7yZ87sKG"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b4y"
		},
		{
			"id": "7yZ87sKG",
			"type": "text",
			"x": 1266.5,
			"y": 1045.35,
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
				"VnYyynDc"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1486793181,
			"version": 2,
			"versionNonce": 1339611240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q010",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JPPKSzm6",
			"originalText": "Q010",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4z"
		},
		{
			"id": "YJrTuXmK",
			"type": "rectangle",
			"x": 1136.5,
			"y": 1157.15,
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
				"zXLGhJy7"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 603927849,
			"version": 2,
			"versionNonce": 1494041112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fkHjcMvy"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b50"
		},
		{
			"id": "fkHjcMvy",
			"type": "text",
			"x": 1143.5,
			"y": 1160.15,
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
				"zXLGhJy7"
			],
			"frameId": null,
			"roundness": null,
			"seed": 907616806,
			"version": 2,
			"versionNonce": 2062650216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T021",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YJrTuXmK",
			"originalText": "T021",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b51"
		},
		{
			"id": "YbYhUuWt",
			"type": "rectangle",
			"x": 1130.5,
			"y": 1223.95,
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
				"fJwc7XeF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1686573445,
			"version": 2,
			"versionNonce": 256720664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Qs2YPtgA"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b52"
		},
		{
			"id": "Qs2YPtgA",
			"type": "text",
			"x": 1137.5,
			"y": 1226.95,
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
				"fJwc7XeF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1812838063,
			"version": 2,
			"versionNonce": 1182522984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T020",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YbYhUuWt",
			"originalText": "T020",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b53"
		},
		{
			"id": "JLL9bMwQ",
			"type": "rectangle",
			"x": 1209.5,
			"y": 1290.75,
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
				"rPH8wQwF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 119379355,
			"version": 2,
			"versionNonce": 1451596824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZTsDS639"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b54"
		},
		{
			"id": "ZTsDS639",
			"type": "text",
			"x": 1216.5,
			"y": 1293.75,
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
				"rPH8wQwF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 31151533,
			"version": 2,
			"versionNonce": 1933824360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T025",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JLL9bMwQ",
			"originalText": "T025",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b55"
		},
		{
			"id": "smkssSTg",
			"type": "rectangle",
			"x": 1170.5,
			"y": 1405.55,
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
				"qS5hiLap"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1754239453,
			"version": 2,
			"versionNonce": 816470296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CvLDxyky"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b56"
		},
		{
			"id": "CvLDxyky",
			"type": "text",
			"x": 1177.5,
			"y": 1408.55,
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
				"qS5hiLap"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1212741741,
			"version": 2,
			"versionNonce": 1217750120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q033",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "smkssSTg",
			"originalText": "Q033",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b57"
		},
		{
			"id": "bn5up2pB",
			"type": "rectangle",
			"x": 1661.5,
			"y": 1419.45,
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
				"EEGMC4FZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1012164983,
			"version": 2,
			"versionNonce": 1093629464,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aG3beNYm"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b58"
		},
		{
			"id": "aG3beNYm",
			"type": "text",
			"x": 1668.5,
			"y": 1422.45,
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
				"EEGMC4FZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 955672602,
			"version": 2,
			"versionNonce": 1144821608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T091",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bn5up2pB",
			"originalText": "T091",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b59"
		},
		{
			"id": "zVaZNFkL",
			"type": "rectangle",
			"x": -801.5,
			"y": -1145.25,
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
				"rfp3pj6Z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1586550652,
			"version": 2,
			"versionNonce": 487125784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Q8xb4Hqx"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5A"
		},
		{
			"id": "Q8xb4Hqx",
			"type": "text",
			"x": -794.5,
			"y": -1142.25,
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
				"rfp3pj6Z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 65534807,
			"version": 2,
			"versionNonce": 1250257512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T003",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zVaZNFkL",
			"originalText": "T003",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5B"
		},
		{
			"id": "mjcivVMs",
			"type": "rectangle",
			"x": -801.5,
			"y": -1070,
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
				"5i54zbAL"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 152904602,
			"version": 2,
			"versionNonce": 447402008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gVbY8bBr"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5C"
		},
		{
			"id": "gVbY8bBr",
			"type": "text",
			"x": -794.5,
			"y": -1067,
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
				"5i54zbAL"
			],
			"frameId": null,
			"roundness": null,
			"seed": 133972818,
			"version": 2,
			"versionNonce": 1446763880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q009",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mjcivVMs",
			"originalText": "Q009",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5D"
		},
		{
			"id": "HKpAib97",
			"type": "rectangle",
			"x": -1059.5,
			"y": -927.95,
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
				"hhNSHus4"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 25303886,
			"version": 2,
			"versionNonce": 571018520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aKBqXRwc"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5E"
		},
		{
			"id": "aKBqXRwc",
			"type": "text",
			"x": -1052.5,
			"y": -924.95,
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
				"hhNSHus4"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1023284529,
			"version": 2,
			"versionNonce": 682356840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T005",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HKpAib97",
			"originalText": "T005",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5F"
		},
		{
			"id": "6xbnDFUz",
			"type": "rectangle",
			"x": -1059.5,
			"y": -841.15,
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
				"89sBYV75"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1729065569,
			"version": 2,
			"versionNonce": 2090314264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fACBKAiB"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5G"
		},
		{
			"id": "fACBKAiB",
			"type": "text",
			"x": -1052.5,
			"y": -838.15,
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
				"89sBYV75"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1664604540,
			"version": 2,
			"versionNonce": 2040636264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T070",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6xbnDFUz",
			"originalText": "T070",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5H"
		},
		{
			"id": "LXxE2LmK",
			"type": "rectangle",
			"x": -801.5,
			"y": -675.6,
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
				"CWysNLbE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1676716279,
			"version": 2,
			"versionNonce": 625649432,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MFgAnT3W"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5I"
		},
		{
			"id": "MFgAnT3W",
			"type": "text",
			"x": -794.5,
			"y": -672.6,
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
				"CWysNLbE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1639247160,
			"version": 2,
			"versionNonce": 661190248,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q032",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LXxE2LmK",
			"originalText": "Q032",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5J"
		},
		{
			"id": "uPp4wv2w",
			"type": "rectangle",
			"x": -1050.5,
			"y": -638.35,
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
				"53iEuzXi"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2067103933,
			"version": 2,
			"versionNonce": 412484632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GcVARtrt"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5K"
		},
		{
			"id": "GcVARtrt",
			"type": "text",
			"x": -1043.5,
			"y": -635.35,
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
				"53iEuzXi"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1611304253,
			"version": 2,
			"versionNonce": 1724770664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T006",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uPp4wv2w",
			"originalText": "T006",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5L"
		},
		{
			"id": "7PddDnXy",
			"type": "rectangle",
			"x": -1050.5,
			"y": -571.55,
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
				"YNeE7Kix"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1193112106,
			"version": 2,
			"versionNonce": 611172632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gjfykh4N"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5M"
		},
		{
			"id": "gjfykh4N",
			"type": "text",
			"x": -1043.5,
			"y": -568.55,
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
				"YNeE7Kix"
			],
			"frameId": null,
			"roundness": null,
			"seed": 302836743,
			"version": 2,
			"versionNonce": 1931246696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T069",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7PddDnXy",
			"originalText": "T069",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5N"
		},
		{
			"id": "dynsVLpz",
			"type": "rectangle",
			"x": -842.5,
			"y": -504.75,
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
				"ybPq9cqP"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 978533591,
			"version": 2,
			"versionNonce": 944102936,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9F7D5aK2"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5O"
		},
		{
			"id": "9F7D5aK2",
			"type": "text",
			"x": -835.5,
			"y": -501.75,
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
				"ybPq9cqP"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1945115311,
			"version": 2,
			"versionNonce": 1042329448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T024 T072",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dynsVLpz",
			"originalText": "T024 T072",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5P"
		},
		{
			"id": "ZvX3S9DP",
			"type": "rectangle",
			"x": -801.5,
			"y": -431.45,
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
				"GuyTY5Yh"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 364114617,
			"version": 2,
			"versionNonce": 890395416,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Nd4Ja43c"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5Q"
		},
		{
			"id": "Nd4Ja43c",
			"type": "text",
			"x": -794.5,
			"y": -428.45,
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
				"GuyTY5Yh"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1584308134,
			"version": 2,
			"versionNonce": 539394664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T004",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZvX3S9DP",
			"originalText": "T004",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5R"
		},
		{
			"id": "KqwJmv4T",
			"type": "rectangle",
			"x": -971.5,
			"y": 698.35,
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
				"MfZ6rwev"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1073785104,
			"version": 2,
			"versionNonce": 1028077592,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wcYjpdkY"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5S"
		},
		{
			"id": "wcYjpdkY",
			"type": "text",
			"x": -964.5,
			"y": 701.35,
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
				"MfZ6rwev"
			],
			"frameId": null,
			"roundness": null,
			"seed": 968534303,
			"version": 2,
			"versionNonce": 133821800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T071",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KqwJmv4T",
			"originalText": "T071",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5T"
		},
		{
			"id": "NTSLJGEk",
			"type": "rectangle",
			"x": -703.5,
			"y": 935.65,
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
				"9ZyVGhKS"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 196438591,
			"version": 2,
			"versionNonce": 81294616,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dsrGqq66"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5U"
		},
		{
			"id": "dsrGqq66",
			"type": "text",
			"x": -696.5,
			"y": 938.65,
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
				"9ZyVGhKS"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1024988909,
			"version": 2,
			"versionNonce": 719784040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T017",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NTSLJGEk",
			"originalText": "T017",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5V"
		},
		{
			"id": "uzGx5mDq",
			"type": "rectangle",
			"x": -703.5,
			"y": 1085.95,
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
				"hndXk3FD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 526402462,
			"version": 2,
			"versionNonce": 557453848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "euD7CP6b"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5W"
		},
		{
			"id": "euD7CP6b",
			"type": "text",
			"x": -696.5,
			"y": 1088.95,
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
				"hndXk3FD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 889061084,
			"version": 2,
			"versionNonce": 884587368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T023",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uzGx5mDq",
			"originalText": "T023",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5X"
		},
		{
			"id": "xeM4UMVM",
			"type": "text",
			"x": -1563.5,
			"y": -1917.35,
			"width": 1186,
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
			"seed": 1729458127,
			"version": 2,
			"versionNonce": 1499467544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 2｜Deck 2：程式如何表示真實世界（W4）",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 2｜Deck 2：程式如何表示真實世界（W4）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5Y"
		},
		{
			"id": "YL886git",
			"type": "text",
			"x": -1563.5,
			"y": -1855.35,
			"width": 1532,
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
			"seed": 1702278598,
			"version": 2,
			"versionNonce": 2008944232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Deck 2 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Deck 2 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5Z"
		},
		{
			"id": "aNrcJBS9",
			"type": "rectangle",
			"x": -1563.5,
			"y": -1788.35,
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
			"seed": 2077843905,
			"version": 2,
			"versionNonce": 1975413784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ufFGtWrW"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5a"
		},
		{
			"id": "ufFGtWrW",
			"type": "text",
			"x": -1549.5,
			"y": -1779.35,
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
			"seed": 1571653290,
			"version": 2,
			"versionNonce": 482345320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★ 考古題考過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aNrcJBS9",
			"originalText": "★ 考古題考過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5b"
		},
		{
			"id": "QXu94WCc",
			"type": "rectangle",
			"x": -1402.5,
			"y": -1788.35,
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
			"seed": 401127940,
			"version": 2,
			"versionNonce": 273230104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "phN687sH"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5c"
		},
		{
			"id": "phN687sH",
			"type": "text",
			"x": -1388.5,
			"y": -1779.35,
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
			"seed": 1674545944,
			"version": 2,
			"versionNonce": 1393267816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QXu94WCc",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5d"
		},
		{
			"id": "AduPyY6D",
			"type": "rectangle",
			"x": -1258.5,
			"y": -1788.35,
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
			"seed": 878348362,
			"version": 2,
			"versionNonce": 1685341720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TpnBg7Ks"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5e"
		},
		{
			"id": "TpnBg7Ks",
			"type": "text",
			"x": -1244.5,
			"y": -1779.35,
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
			"seed": 759107028,
			"version": 2,
			"versionNonce": 7128936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "〔C〕Claude 補充（投影片與講義沒有）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AduPyY6D",
			"originalText": "〔C〕Claude 補充（投影片與講義沒有）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5f"
		},
		{
			"id": "f77szdE8",
			"type": "rectangle",
			"x": -904.5,
			"y": -1788.35,
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
			"seed": 1281544127,
			"version": 2,
			"versionNonce": 523485976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tGmNamsm"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5g"
		},
		{
			"id": "tGmNamsm",
			"type": "text",
			"x": -890.5,
			"y": -1779.35,
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
			"seed": 540526680,
			"version": 2,
			"versionNonce": 1898945128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例題考到、原本心智圖沒有的觀念",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "f77szdE8",
			"originalText": "例題考到、原本心智圖沒有的觀念",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5h"
		},
		{
			"id": "EdSTgxHD",
			"type": "rectangle",
			"x": -602.5,
			"y": -1780.75,
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
			"seed": 1165143158,
			"version": 2,
			"versionNonce": 788242456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "P34iNMpm"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5i"
		},
		{
			"id": "P34iNMpm",
			"type": "text",
			"x": -595.5,
			"y": -1777.75,
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
			"seed": 1594742661,
			"version": 2,
			"versionNonce": 136318312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001 Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EdSTgxHD",
			"originalText": "T001 Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5j"
		},
		{
			"id": "Nvr9LHfA",
			"type": "text",
			"x": -504.5,
			"y": -1779.35,
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
			"seed": 623712809,
			"version": 2,
			"versionNonce": 331341080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
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
			"index": "b5k"
		},
		{
			"id": "bj7SRdyL",
			"type": "rectangle",
			"x": -375.5,
			"y": -1780.75,
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
			"seed": 1947823753,
			"version": 2,
			"versionNonce": 1854546024,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fJ6BczQ2"
				}
			],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"index": "b5l"
		},
		{
			"id": "fJ6BczQ2",
			"type": "text",
			"x": -368.5,
			"y": -1777.75,
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
			"seed": 2039761453,
			"version": 2,
			"versionNonce": 787773976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T089",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bj7SRdyL",
			"originalText": "T089",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5m"
		},
		{
			"id": "p5ysVqXc",
			"type": "text",
			"x": -318.5,
			"y": -1779.35,
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
			"seed": 292188673,
			"version": 2,
			"versionNonce": 1144640360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858136856,
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
			"index": "b5n"
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