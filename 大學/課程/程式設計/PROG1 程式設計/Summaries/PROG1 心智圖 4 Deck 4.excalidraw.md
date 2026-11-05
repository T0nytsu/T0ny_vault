---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Deck 4 整理]]"
  - "Midterm_Practice_Student.pdf（老師的 140 題例題，T001–T100、Q001–Q040）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
程式如何重複工作
Deck 4・W7 ^3783pxTd

驅動問題 ^YajXbijf

多筆行程、跳過無效、最後摘要 ^d9uMbrb8

Campus 12.5／45、Bad −1／30、Station 3.5／
30、DONE ^DH5XBEkr

→ 2 筆、16.00 km、75 min、12.80 km/h ^2LyMbQwj

Q1 要重複的是什麼 ^5DNgEGCr

複製三份程式 ✗ → 規則寫一次，用迴圈決定要不要
再做 ^gpthhWfA

迴圈之前：初始化 session 狀態（0 筆、0.0 km） ^zagVwNpt

每次迴圈：讀一筆 → 停止／拒絕／接受 ^4c5aCZr6

迴圈之後：印一次摘要 ^k5SJgvMy

iteration ≠ session；被拒絕也用掉一次 iteration ^6xKmsLqS

v0.4 協定 ^iKk6qbJL

精確大寫 DONE → 立即停止，不問距離時間 ^FbQAKfg7

無效 → 印第一個錯誤，總和不變 ^ZiBSEKNW

有效 → 報告，筆數與總和各更新一次 ^ypb38Q6d

沒有有效資料 → 明確訊息，不算平均 ^JEBMXz7G

⚠ 零距離仍是資料，不能拿 0 當結束命令 ^UCAQ9wWm

Q2 for 逐項處理 ^ix6XnCMY

for character in "loop" → l o o p（重複值照樣處
理） ^f66JZgFZ

iterable：能依序提供下一項 ^WExbyMNy

縮排決定重複範圍：Finished 在外面只印一次 ^mBPr2f28

range（含頭不含尾） ^U9hfj8ri

range(4) → 0, 1, 2, 3 ^9U7Xihbw

range(1, 4) → 1, 2, 3 ^rCbDGrF2

range(6, 0, -2) → 6, 4, 2 ^SDamLrvA

range(8, 3) → 空（合法） ^fTjMEW7P

⚠ range(0, 5, 0) → ValueError ^VyBge7hb

range(5, 1, -2) → 5, 3；range(2, 2) → 空（零次也正
常） ^9KFtyuqL

迴圈裡改 i 不影響下一輪：range 照樣給下一個值 ^MV3Xh4CP

迭代次數 ≠ 成功次數（0、20、30 → 試 3 次接受
2 次） ^nkxTgxsd

★ 考古題 A4、B4：固定次數 for＋同時指派 ^mRKpQNxR

Q3 記住前面的資料 ^CcWa4wQW

counter：有幾筆；accumulator：加起來多少 ^xQKyrjvS

迴圈前初始化一次；只在接受時更新 ^A5ZWz79b

1 + 2 + 3 + 4 → 10 ^juwX3Ubn

Loop invariant：每輪結束 total＝已處理項目的和；
n = 0 時仍成立 ^qrMzDAxn

⚠ total = 0 放進迴圈 → 只剩最後的 4 ^5xrzMGyW

總和只描述「已接受的前綴」 ^YQL3gnkS

平均要先說清楚平均什麼 ^PUjKJUSe

mean duration = 75 / 2 = 37.5 min ^g97HAsJQ

overall speed = 16 / 1.25 = 12.8 km/h ^7uFisvJA

⚠ (16.67 + 7.00) / 2 ≈ 11.83 是另一個問題 ^WDTJnAhU

Lab A：10、20、30 → 20.0；有拒絕時分母不能
寫死 3 ^2vp2MF2h

Q4 while 與停止 ^XppQruja

每次先檢查條件；一開始就假 → 零次 ^vHuNJEsb

countdown：3 2 1 Go（for range(3, 0, -1) 結果
相同） ^MNVPK8kL

Sentinel：while True → 先讀 route → if
route_name == "DONE": break ^hVwwEXU6

先比對 DONE 再轉型：int("DONE") → ValueError ^aV5S79kG

選迴圈看「下一項從哪來、何時停」 ^YhugEsZx

走訪每個字元 → for ch in text ^4UdX9SUm

剛好 n 次 → for i in range(n) ^g6TDhaqe

讀到 DONE → while True ＋ break ^B5FZHxyQ

收滿 n 筆有效 → while accepted_count < n ^smxLfwsn

0、20、30、40 → 試 4 次接受 3 次 ^mX9gADz2

倍增 while x < n: x *= 2：結束時 x / 2 < n ≤ x，
不是 x ≤ n < 2x（n = 3 → x = 4） ^YdsGKnvk

找 ≤ n 的最大 2 的次方：條件寫 p * 2 <= n；寫成
p < n 時 n = 31 會得 32 ^ZpSyBntT

★ 考古題：while True ＋ break（質因數、倍增、
Fibonacci） ^R5zzVbyG

Q5 停止、略過、繼續 ^78AZVRQQ

break：離開最內層迴圈 ^vcpKSDDx

continue：跳過本輪剩下，進下一輪 ^2xVdLWcC

DONE → break；無效完整資料 → continue ^M4Ujer2Z

error 每筆重設；總和跨筆保留 ^V7cN46a4

摘要在迴圈後；accepted_count == 0 → 不做除法 ^FApQqziq

⚠ continue 跳過 i += 1 → 無窮迴圈 ^8Qm2YKF9

修：skip 路徑也更新，或改 for i in range(1, 4) → 1 3 ^BiFJTuiF

終止推理 ^kK2rCAmj

for 有限 range：迭代器前進 ^QLGFq2Ja

countdown while：更新不能被跳過 ^ayn2ns8d

DONE 迴圈：靠使用者最後輸入 DONE ^HYsQeNFn

巢狀迴圈：外層每換 i，內層重來 → (1,1)…(2,3) ^4kAHunNt

⚠ 內層 break 只出內層 → (1,1)、(2,1) ^gcc5iYFU

Lab B：BLANK 1 break、BLANK 2 continue；0,
20, −5, 30, DONE → 2；DONE 開頭 → 0 ^fLKYEFK3

電腦基礎：向後跳躍與記憶體區域
性 ^8N6qpyZ5

教學迴圈：CMP R0, 3 → JGE done → OUT →
ADD R0, 1 → JMP loop → 輸出 0 1 2 ^YTemFRiw

刪 ADD → 一直輸出 0；刪 JMP → 只輸出 0 ^cQ8MvEJX

CPU → cache（小、近）→ RAM（大）；SSD 存
檔案 ^cAkcy4Xw

hit：資料已在這層；miss：往下層找 ^qdHwiLSx

Temporal locality：100 → 100 → 100 ^Degqq5nc

Spatial locality：100 → 104 → 108 ^jJWHzxCR

讀 0、1、2、0（一列 0–3）→ Miss、Hit、Hit、
Hit ^d8bYYEwG

不要用小 Python 迴圈計時證明 cache 效果 ^Lpj7mT2g

時脈較高不保證每個程式都比較快 ^tf6dxJvQ

★ L1 比 L2 小又快 → 見心智圖 6 ^rE8G2fuY

Q6 驗證 loop 與 session ^db7mik9Z

有順序的 session 測試 ^mJrK6wqT

一開始 DONE → 0 筆、不問數值、不算平均 ^KhsH3pD5

一筆有效 → 報告一次、摘要一次 ^eHQdRGc6

有效 → 無效 → 有效 → 只加兩筆 ^RheJm6tX

有效 → 無效 → DONE → 保留第一筆總和 ^2wjqqkdF

全部無效 → 不除以零 ^fDVEvhX3

零距離、重複、30／60 邊界 ^MAgxEGi3

也要測不該發生的：多餘提示、被拒資料的報告、錯
的總和 ^2xVhrjew

故意錯誤：count 在拒絕前＋total 每輪清零 → 3
3.5（應 2 16.0） ^Eav44472

三條路徑：STOP（break）／SKIP（continue）／
ACCEPT（報告＋更新一次） ^8BDAyLWh

trip_log.py 五區：初始化 → 輸入與停止 → 驗證與
略過 → 接受報告與更新 → 最後摘要 ^Lr6mX4yW

AI 先做有界追蹤（≤ 6 輪），再提最小 patch ^xTpTxhDm

選讀 ^zLStCKGU

for-else：正常跑完（沒 break）才執行 ^BvL7pqZ4

target 7 → Not found；target 3 → Found ^VSVNMEHN

try／except 解析恢復：是新承諾，不是原本能力 ^t53k7qRH

最長行程：第一筆建候選；更長才換；同時間保留第
一筆；空 session 不印 ^bSPxBy8f

Q020 ^zvJb4VRy

T042 ^HrnZVpNr

T035 ^WJEnBaxx

T073 ^RprXKkK5

T036 ^RUwZXTQY

T074 ^zXgR8NtQ

T044 ^vUGGnENH

Q016 ^GqD5F8CL

T043 ^mH7vznJM

T037 Q017 ^fbw4CMTK

T045 T077 Q029 ^hLBF34Wp

T038 ^tukjRrAZ

Q019 ^kG58tZKx

T041 ^rNudwRgE

T092 ^iWASBq2e

Q040 ^SdYQsTqw

Q018 ^Pgj47F4W

T039 ^xdbifTRz

T076 ^QVmD5wXN

T078 ^HMTdKk3K

T075 Q030 ^KaJWfRN8

T046 ^ZYd4W6j6

T097 Q026 ^yP6LX8DZ

T040 ^DQxm6MiP

T011 ^FDPMS2et

T061 ^rfrV8XdS

T012 ^CmJknciv

T079 ^b7jvwzFR

T098 ^2Qd2L3Jf

PROG1 期中心智圖 4｜Deck 4：程式如何重複工作（W7） ^W7JUbZZS

來源：PROG1 Deck 4 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的
練習題。 ^FKAzBNwk

★ 考古題考過 ^8ckZMadk

⚠ 易錯陷阱 ^pKacABmA

例題考到、原本心智圖沒有的觀念 ^vNJKyrNE

T001 Q001 ^pm9riYcT

老師例題題號 ^L6B9j5vy

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "as8GzRPU",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 1426.83,
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
			"seed": 2124110499,
			"version": 2,
			"versionNonce": 159644952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-1426.83
				],
				[
					150,
					-1426.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "X85j8Rze",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "NySMrtTD",
			"type": "arrow",
			"x": 472.5,
			"y": -1426.83,
			"width": 76,
			"height": 32.87,
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
			"seed": 2053277780,
			"version": 2,
			"versionNonce": 1050148968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "X85j8Rze",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wDvbhDhG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "VYUx3USe",
			"type": "arrow",
			"x": 472.5,
			"y": -1426.83,
			"width": 76,
			"height": 32.88,
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
			"seed": 1269396963,
			"version": 2,
			"versionNonce": 389323288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					32.88
				],
				[
					76,
					32.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "X85j8Rze",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "AuEdX5mU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "4Xb9tAys",
			"type": "arrow",
			"x": 991.5,
			"y": -1393.95,
			"width": 60,
			"height": 0,
			"angle": 0,
			"strokeColor": "#1971c2",
			"backgroundColor": "transparent",
			"fillStyle": "solid",
			"strokeWidth": 1.5,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1965903264,
			"version": 2,
			"versionNonce": 395031400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "AuEdX5mU",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mGmZkbFj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "MnwupKMv",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 1039.68,
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
			"seed": 1898850280,
			"version": 2,
			"versionNonce": 1053398808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-1039.68
				],
				[
					150,
					-1039.68
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "A8NWgHGc",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 247.27,
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
			"seed": 329509536,
			"version": 2,
			"versionNonce": 496043624,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-247.27
				],
				[
					76,
					-247.27
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YZqjDy2H",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "ZsbmsyMC",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 181.52,
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
			"seed": 144411736,
			"version": 2,
			"versionNonce": 79098904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-181.52
				],
				[
					76,
					-181.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7H8x2X33",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "vzRy4aCP",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 127.02,
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
			"seed": 1202244675,
			"version": 2,
			"versionNonce": 2104752488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-127.02
				],
				[
					76,
					-127.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bn4WwVKV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "tb8arqUp",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 72.52,
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
			"seed": 2112691918,
			"version": 2,
			"versionNonce": 1055961368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-72.52
				],
				[
					76,
					-72.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2yDPPdZc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "9cEB9B5f",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 18.02,
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
			"seed": 2146189150,
			"version": 2,
			"versionNonce": 1786809448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-18.02
				],
				[
					76,
					-18.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Y39ArsAZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "NTiH4q9N",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 114.63,
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
			"seed": 720451949,
			"version": 2,
			"versionNonce": 1693109784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "caxnfwF7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "gckUSzzt",
			"type": "arrow",
			"x": 586.5,
			"y": -1039.68,
			"width": 76,
			"height": 247.28,
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
			"seed": 787128114,
			"version": 2,
			"versionNonce": 1317191528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					247.28
				],
				[
					76,
					247.28
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "TAYHDTqZ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LFcadkb8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "YULdmkQf",
			"type": "arrow",
			"x": 775.5,
			"y": -925.05,
			"width": 60,
			"height": 81.4,
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
			"seed": 1226601451,
			"version": 2,
			"versionNonce": 1603881752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "caxnfwF7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EpRTrq3H",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "NE8LvuKT",
			"type": "arrow",
			"x": 775.5,
			"y": -925.05,
			"width": 60,
			"height": 14.6,
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
			"seed": 1274101993,
			"version": 2,
			"versionNonce": 2043056744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-14.6
				],
				[
					60,
					-14.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "caxnfwF7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yaUJmgAv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "3WTbN8PC",
			"type": "arrow",
			"x": 775.5,
			"y": -925.05,
			"width": 60,
			"height": 33.4,
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
			"seed": 1250296567,
			"version": 2,
			"versionNonce": 1500522520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					33.4
				],
				[
					60,
					33.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "caxnfwF7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PMm7DuDu",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "9CBLUEdQ",
			"type": "arrow",
			"x": 775.5,
			"y": -925.05,
			"width": 60,
			"height": 81.4,
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
			"seed": 1200643342,
			"version": 2,
			"versionNonce": 1394083176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "caxnfwF7",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MP5fiNVX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "GAhbvBqh",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 342.53,
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
			"seed": 463095318,
			"version": 2,
			"versionNonce": 241394968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-342.53
				],
				[
					150,
					-342.53
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "iAGc8r2F",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 354.12,
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
			"seed": 1156366103,
			"version": 2,
			"versionNonce": 130226280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-354.12
				],
				[
					76,
					-354.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "C322P6n5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "62yekq59",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 288.37,
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
			"seed": 74958929,
			"version": 2,
			"versionNonce": 468124184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-288.37
				],
				[
					76,
					-288.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "M9LHH6pK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "4B8Z6tZw",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 233.87,
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
			"seed": 442379262,
			"version": 2,
			"versionNonce": 999541608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-233.87
				],
				[
					76,
					-233.87
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ceSB6eQP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "KeRkLNiH",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 29.42,
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
			"seed": 1665544950,
			"version": 2,
			"versionNonce": 1357840152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-29.42
				],
				[
					76,
					-29.42
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "7L3E7Q9L",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 203.83,
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
			"seed": 52963519,
			"version": 2,
			"versionNonce": 953556584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					203.83
				],
				[
					76,
					203.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HZVUEymU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "6S5QFGwF",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 288.38,
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
			"seed": 631986038,
			"version": 2,
			"versionNonce": 2112838680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					288.38
				],
				[
					76,
					288.38
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FxJVkajq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "KchLNXtX",
			"type": "arrow",
			"x": 566.5,
			"y": -342.53,
			"width": 76,
			"height": 354.13,
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
			"seed": 737252932,
			"version": 2,
			"versionNonce": 542511464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					354.13
				],
				[
					76,
					354.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nTt2HRNz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PyXgvGjt",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "XhsjQSgs",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 153.2,
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
			"seed": 1429529889,
			"version": 2,
			"versionNonce": 1155275032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-153.2
				],
				[
					60,
					-153.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Dd2rXLJe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "hTjS3YZL",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 86.4,
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
			"seed": 1909575300,
			"version": 2,
			"versionNonce": 425698408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-86.4
				],
				[
					60,
					-86.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FQt6KpCG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "pG3y6Vug",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 19.6,
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
			"seed": 2005735075,
			"version": 2,
			"versionNonce": 1764308504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-19.6
				],
				[
					60,
					-19.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mBcnanVG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "cSk5aUpg",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 28.4,
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
			"seed": 1949623546,
			"version": 2,
			"versionNonce": 29284200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					28.4
				],
				[
					60,
					28.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kK8uwrSS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "VJCgDw3k",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 76.4,
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
			"seed": 370626245,
			"version": 2,
			"versionNonce": 533377816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					76.4
				],
				[
					60,
					76.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JRMg24Dk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "tsHbVTwy",
			"type": "arrow",
			"x": 850.5,
			"y": -371.95,
			"width": 60,
			"height": 153.2,
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
			"seed": 1850408809,
			"version": 2,
			"versionNonce": 499100264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					153.2
				],
				[
					60,
					153.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "anqnurYB",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zMD7fQie",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "8CVkAwGq",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 386.07,
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
			"seed": 1644883316,
			"version": 2,
			"versionNonce": 1597280280,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					386.07
				],
				[
					150,
					386.07
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "yxnQj9fh",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 271.17,
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
			"seed": 1452384370,
			"version": 2,
			"versionNonce": 1210981736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-271.17
				],
				[
					76,
					-271.17
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7aJU73aY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "wsPmizLu",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 216.67,
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
			"seed": 59095834,
			"version": 2,
			"versionNonce": 794479896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-216.67
				],
				[
					76,
					-216.67
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JGSz97uw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "68UwgQSN",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 162.17,
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
			"seed": 1287580503,
			"version": 2,
			"versionNonce": 576073832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-162.17
				],
				[
					76,
					-162.17
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LpEYhARf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "8MQJMyUr",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 77.62,
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
			"seed": 795734376,
			"version": 2,
			"versionNonce": 2041670168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-77.62
				],
				[
					76,
					-77.62
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cfqrcanz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "YPhKJhfX",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 6.93,
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
			"seed": 40548006,
			"version": 2,
			"versionNonce": 1141105512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					6.93
				],
				[
					76,
					6.93
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5TK5pAfY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "ffXXeHVL",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 61.43,
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
			"seed": 1629427990,
			"version": 2,
			"versionNonce": 1496082200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					61.43
				],
				[
					76,
					61.43
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ij9hHijC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "jYjbq7aj",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 160.68,
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
			"seed": 152616647,
			"version": 2,
			"versionNonce": 1803761256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					160.68
				],
				[
					76,
					160.68
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yH2c8KA9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "tdStvWc4",
			"type": "arrow",
			"x": 590.5,
			"y": 386.07,
			"width": 76,
			"height": 271.18,
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
			"seed": 526089426,
			"version": 2,
			"versionNonce": 1782563864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					271.18
				],
				[
					76,
					271.18
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "YKEjLT4u",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vN86B8m3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "8h9ku82E",
			"type": "arrow",
			"x": 900.5,
			"y": 546.75,
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
			"seed": 424933945,
			"version": 2,
			"versionNonce": 765471080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "yH2c8KA9",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "m7hqUipb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "Fqa9jNvT",
			"type": "arrow",
			"x": 900.5,
			"y": 546.75,
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
			"seed": 1661901490,
			"version": 2,
			"versionNonce": 450855192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "yH2c8KA9",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QpuYmbKW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "SKcvpd53",
			"type": "arrow",
			"x": 900.5,
			"y": 546.75,
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
			"seed": 386522781,
			"version": 2,
			"versionNonce": 631684200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "yH2c8KA9",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5987aiiL",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "YH44zzZN",
			"type": "arrow",
			"x": 181.5,
			"y": -0.0,
			"width": 150,
			"height": 1110.12,
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
			"seed": 1391941848,
			"version": 2,
			"versionNonce": 2055183896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					1110.12
				],
				[
					150,
					1110.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "zbduLGQG",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 338.32,
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
			"seed": 127447559,
			"version": 2,
			"versionNonce": 627240808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-338.32
				],
				[
					76,
					-338.32
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "46pU4kiZ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "QfWEQXZM",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 253.77,
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
			"seed": 1730296812,
			"version": 2,
			"versionNonce": 169089816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-253.77
				],
				[
					76,
					-253.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Qf8jdQXV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "DHqFxUdS",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 176.77,
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
			"seed": 423211899,
			"version": 2,
			"versionNonce": 1696645736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-176.77
				],
				[
					76,
					-176.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9weZgXTc",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "tQC7wnFg",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 42.27,
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
			"seed": 1768481970,
			"version": 2,
			"versionNonce": 202438680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-42.27
				],
				[
					76,
					-42.27
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FBzhX9ua",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "WaFjZDrA",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 80.98,
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
			"seed": 1901241941,
			"version": 2,
			"versionNonce": 866923880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					80.98
				],
				[
					76,
					80.98
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5XuWTj5k",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "K93rvhwr",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 165.53,
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
			"seed": 819707473,
			"version": 2,
			"versionNonce": 1416246552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					165.53
				],
				[
					76,
					165.53
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wBkQJEGr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "r8VEQLy4",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 261.33,
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
			"seed": 641164914,
			"version": 2,
			"versionNonce": 642861160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					261.33
				],
				[
					76,
					261.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aUuD3yZk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "7ZTTwPx5",
			"type": "arrow",
			"x": 557.5,
			"y": 1110.12,
			"width": 76,
			"height": 338.33,
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
			"seed": 1403775821,
			"version": 2,
			"versionNonce": 412340760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					338.33
				],
				[
					76,
					338.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "LJ9CbGCt",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5y5aGQ9x",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "L2Bx72FH",
			"type": "arrow",
			"x": 1018.5,
			"y": 933.35,
			"width": 60,
			"height": 9.4,
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
			"seed": 1863008031,
			"version": 2,
			"versionNonce": 1222376296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "9weZgXTc",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "uudweeQp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "73RL8Aki",
			"type": "arrow",
			"x": 960.5,
			"y": 1067.85,
			"width": 60,
			"height": 72,
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
			"seed": 1079935427,
			"version": 2,
			"versionNonce": 1065471768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "FBzhX9ua",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "3iXwzPev",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "d8h9RAmh",
			"type": "arrow",
			"x": 960.5,
			"y": 1067.85,
			"width": 60,
			"height": 24,
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
			"seed": 1963203881,
			"version": 2,
			"versionNonce": 1301827176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "FBzhX9ua",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ygM3u3ZM",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "sV7iuhaS",
			"type": "arrow",
			"x": 960.5,
			"y": 1067.85,
			"width": 60,
			"height": 24,
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
			"seed": 1389138901,
			"version": 2,
			"versionNonce": 833104920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "FBzhX9ua",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zpAwizk2",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "YJcZqeZT",
			"type": "arrow",
			"x": 960.5,
			"y": 1067.85,
			"width": 60,
			"height": 72,
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
			"seed": 620875614,
			"version": 2,
			"versionNonce": 1028800872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "FBzhX9ua",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tSWahfQ7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "LiaYnucc",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 785.48,
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
			"seed": 682153627,
			"version": 2,
			"versionNonce": 687532312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-785.48
				],
				[
					-150,
					-785.48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "WJTHZhym",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 324.77,
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
			"seed": 767754273,
			"version": 2,
			"versionNonce": 659936360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-324.77
				],
				[
					-76,
					-324.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BnvhbWju",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "Uhusn9u9",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 251.47,
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
			"seed": 989032058,
			"version": 2,
			"versionNonce": 15599128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-251.47
				],
				[
					-76,
					-251.47
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ej8Q2qkR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "6XYhcthE",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 178.17,
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
			"seed": 1118238329,
			"version": 2,
			"versionNonce": 1366230888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-178.17
				],
				[
					-76,
					-178.17
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SqWgwWXa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "3xt24btF",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 123.67,
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
			"seed": 885100240,
			"version": 2,
			"versionNonce": 108364568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-123.67
				],
				[
					-76,
					-123.67
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fhXmc8vN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "BEpvyB3j",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 50.37,
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
			"seed": 445410088,
			"version": 2,
			"versionNonce": 1743379048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-50.37
				],
				[
					-76,
					-50.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "g7sK6YRR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "3WUu4sRC",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 22.93,
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
			"seed": 2022168618,
			"version": 2,
			"versionNonce": 1208311832,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					22.93
				],
				[
					-76,
					22.93
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ei32iHru",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "BSARj2ma",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 131.58,
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
			"seed": 963839184,
			"version": 2,
			"versionNonce": 764562792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					131.58
				],
				[
					-76,
					131.58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "xh8ZbYYv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "FfQQbgsR",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 259.03,
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
			"seed": 170050457,
			"version": 2,
			"versionNonce": 1704041752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					259.03
				],
				[
					-76,
					259.03
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dkCi9aqp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "G7KCHQaF",
			"type": "arrow",
			"x": -615.5,
			"y": -785.48,
			"width": 76,
			"height": 324.78,
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
			"seed": 333747367,
			"version": 2,
			"versionNonce": 733241448,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					324.78
				],
				[
					-76,
					324.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U83SvdRz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "C4ktU9QG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "HDiLEPa9",
			"type": "arrow",
			"x": -1030.5,
			"y": -762.55,
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
			"seed": 643790113,
			"version": 2,
			"versionNonce": 1619933720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "ei32iHru",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Vtb4s422",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "kJ4iSCv2",
			"type": "arrow",
			"x": -796.5,
			"y": -653.9,
			"width": 60,
			"height": 57.4,
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
			"seed": 223405218,
			"version": 2,
			"versionNonce": 1646007144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-57.4
				],
				[
					-60,
					-57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "xh8ZbYYv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jBy9UxdN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "kTiwGvcP",
			"type": "arrow",
			"x": -796.5,
			"y": -653.9,
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
			"seed": 1187092267,
			"version": 2,
			"versionNonce": 1810839320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					9.4
				],
				[
					-60,
					9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "xh8ZbYYv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MEVtFJLn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "CHfWgFv7",
			"type": "arrow",
			"x": -796.5,
			"y": -653.9,
			"width": 60,
			"height": 57.4,
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
			"seed": 1408552516,
			"version": 2,
			"versionNonce": 1997891176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "xh8ZbYYv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "w4FBsYjP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "Twki3cR9",
			"type": "arrow",
			"x": -1120.5,
			"y": -526.45,
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
			"seed": 797556447,
			"version": 2,
			"versionNonce": 1009292312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					9.4
				],
				[
					-60,
					9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dkCi9aqp",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VWuhCmwm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "gvT2LYKY",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 79.37,
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
			"seed": 1030807757,
			"version": 2,
			"versionNonce": 1735154024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-79.37
				],
				[
					-150,
					-79.37
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "jc6bJKJd",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 274.33,
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
			"seed": 1506706650,
			"version": 2,
			"versionNonce": 1462653208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-274.33
				],
				[
					-76,
					-274.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gqTMBgKd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0A"
		},
		{
			"id": "tFueWyCd",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 178.53,
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
			"seed": 1799071877,
			"version": 2,
			"versionNonce": 913108072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-178.53
				],
				[
					-76,
					-178.53
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RyHBXr7q",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0B"
		},
		{
			"id": "99GXjpyK",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 112.78,
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
			"seed": 1782633048,
			"version": 2,
			"versionNonce": 1685351960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-112.78
				],
				[
					-76,
					-112.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "2wxGFmWH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0C"
		},
		{
			"id": "JzGbYmnd",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 39.48,
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
			"seed": 1902263705,
			"version": 2,
			"versionNonce": 501423976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-39.48
				],
				[
					-76,
					-39.48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "syxJDVP8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0D"
		},
		{
			"id": "jtdUjsFb",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 15.02,
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
			"seed": 111295960,
			"version": 2,
			"versionNonce": 2096032536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					15.02
				],
				[
					-76,
					15.02
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9wGij4jb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0E"
		},
		{
			"id": "6cTkMJs8",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 80.77,
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
			"seed": 1066343681,
			"version": 2,
			"versionNonce": 1041953384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					80.77
				],
				[
					-76,
					80.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kZYe29CY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0F"
		},
		{
			"id": "mc685ezf",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 146.52,
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
			"seed": 374618541,
			"version": 2,
			"versionNonce": 2064762904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					146.52
				],
				[
					-76,
					146.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BEwS39LY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0G"
		},
		{
			"id": "7u5GeTN5",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 219.82,
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
			"seed": 1079904031,
			"version": 2,
			"versionNonce": 1306551656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					219.82
				],
				[
					-76,
					219.82
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VGmcEJ2R",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0H"
		},
		{
			"id": "Nhcwp42h",
			"type": "arrow",
			"x": -744.5,
			"y": -79.37,
			"width": 76,
			"height": 274.32,
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
			"seed": 1077546686,
			"version": 2,
			"versionNonce": 1255212312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					274.32
				],
				[
					-76,
					274.32
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rFtNvije",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Nbw3dEZp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0I"
		},
		{
			"id": "UxtkcsHr",
			"type": "arrow",
			"x": -1262.5,
			"y": -353.7,
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
			"seed": 2115231039,
			"version": 2,
			"versionNonce": 1249867880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "gqTMBgKd",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WBchT47U",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0J"
		},
		{
			"id": "x7x6ePRc",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 659.33,
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
			"seed": 789990125,
			"version": 2,
			"versionNonce": 966828568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					659.33
				],
				[
					-150,
					659.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0K"
		},
		{
			"id": "vEiCzcue",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 253.73,
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
			"seed": 1216224468,
			"version": 2,
			"versionNonce": 667167592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-253.73
				],
				[
					-76,
					-253.73
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0L"
		},
		{
			"id": "jqSzJehE",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 61.83,
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
			"seed": 70936223,
			"version": 2,
			"versionNonce": 1182048024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-61.83
				],
				[
					-76,
					-61.83
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YvsfLM4X",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0M"
		},
		{
			"id": "Eq7x43Tp",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 33.97,
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
			"seed": 1444658145,
			"version": 2,
			"versionNonce": 2147122792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					33.97
				],
				[
					-76,
					33.97
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4sTRd87p",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0N"
		},
		{
			"id": "AETwYNtP",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 110.97,
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
			"seed": 1710476000,
			"version": 2,
			"versionNonce": 1908472856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					110.97
				],
				[
					-76,
					110.97
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BFHLZBLF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0O"
		},
		{
			"id": "YgVCiDPk",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 187.97,
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
			"seed": 372768142,
			"version": 2,
			"versionNonce": 1139700072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					187.97
				],
				[
					-76,
					187.97
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kyP6eUrm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0P"
		},
		{
			"id": "NZQWvk5K",
			"type": "arrow",
			"x": -658.5,
			"y": 659.33,
			"width": 76,
			"height": 253.72,
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
			"seed": 2037451258,
			"version": 2,
			"versionNonce": 226081048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					253.72
				],
				[
					-76,
					253.72
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rEjyr3zP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sYfRvGcS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Q"
		},
		{
			"id": "9rDiXB6x",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 129.4,
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
			"seed": 1210351880,
			"version": 2,
			"versionNonce": 1793852520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-129.4
				],
				[
					-60,
					-129.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "v8epj8k5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0R"
		},
		{
			"id": "YYPeM39d",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 81.4,
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
			"seed": 1798053587,
			"version": 2,
			"versionNonce": 219338264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-81.4
				],
				[
					-60,
					-81.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FMbkXTVp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0S"
		},
		{
			"id": "yLvpwf74",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 33.4,
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
			"seed": 529915145,
			"version": 2,
			"versionNonce": 582956904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Q4Zu7vFb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0T"
		},
		{
			"id": "ASQykZai",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 33.4,
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
			"seed": 260572814,
			"version": 2,
			"versionNonce": 1434473240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					33.4
				],
				[
					-60,
					33.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "A5asqyCs",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0U"
		},
		{
			"id": "ngeXaLPi",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 81.4,
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
			"seed": 1216428168,
			"version": 2,
			"versionNonce": 2142505576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					81.4
				],
				[
					-60,
					81.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ByJkqqpD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0V"
		},
		{
			"id": "wRp4dq5g",
			"type": "arrow",
			"x": -956.5,
			"y": 405.6,
			"width": 60,
			"height": 129.4,
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
			"seed": 1534863786,
			"version": 2,
			"versionNonce": 221655064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					129.4
				],
				[
					-60,
					129.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "pC7ekHFi",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JXLkLwDg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0W"
		},
		{
			"id": "rm8FZF5F",
			"type": "arrow",
			"x": -181.5,
			"y": -0.0,
			"width": 150,
			"height": 1057.68,
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
			"seed": 857004957,
			"version": 2,
			"versionNonce": 748060008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					1057.68
				],
				[
					-150,
					1057.68
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "CgYRLWUJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vhCGxcEz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0X"
		},
		{
			"id": "eStyLE8E",
			"type": "arrow",
			"x": -423.5,
			"y": 1057.68,
			"width": 76,
			"height": 60.13,
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
			"seed": 1116254767,
			"version": 2,
			"versionNonce": 1814588696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-60.13
				],
				[
					-76,
					-60.13
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vhCGxcEz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ry4JFtLK",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Y"
		},
		{
			"id": "ifmcSzdu",
			"type": "arrow",
			"x": -423.5,
			"y": 1057.68,
			"width": 76,
			"height": 5.63,
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
			"seed": 523554398,
			"version": 2,
			"versionNonce": 447909992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					-5.63
				],
				[
					-76,
					-5.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vhCGxcEz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yQ5HEVjd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Z"
		},
		{
			"id": "meEtfqhH",
			"type": "arrow",
			"x": -423.5,
			"y": 1057.68,
			"width": 76,
			"height": 60.12,
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
			"seed": 1087933142,
			"version": 2,
			"versionNonce": 197855768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
					60.12
				],
				[
					-76,
					60.12
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "vhCGxcEz",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "PzKgNiP8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0a"
		},
		{
			"id": "UkUDPPRN",
			"type": "arrow",
			"x": -859.5,
			"y": 997.55,
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
			"seed": 1268185127,
			"version": 2,
			"versionNonce": 835994472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
				"elementId": "ry4JFtLK",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qvDYLRbA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0b"
		},
		{
			"id": "CgYRLWUJ",
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
			"seed": 1368997798,
			"version": 2,
			"versionNonce": 923928344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3783pxTd"
				},
				{
					"type": "arrow",
					"id": "as8GzRPU"
				},
				{
					"type": "arrow",
					"id": "MnwupKMv"
				},
				{
					"type": "arrow",
					"id": "GAhbvBqh"
				},
				{
					"type": "arrow",
					"id": "8CVkAwGq"
				},
				{
					"type": "arrow",
					"id": "YH44zzZN"
				},
				{
					"type": "arrow",
					"id": "LiaYnucc"
				},
				{
					"type": "arrow",
					"id": "gvT2LYKY"
				},
				{
					"type": "arrow",
					"id": "x7x6ePRc"
				},
				{
					"type": "arrow",
					"id": "rm8FZF5F"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0c"
		},
		{
			"id": "3783pxTd",
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
			"seed": 1503950694,
			"version": 2,
			"versionNonce": 4691560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "程式如何重複工作\nDeck 4・W7",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CgYRLWUJ",
			"originalText": "程式如何重複工作\nDeck 4・W7",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0d"
		},
		{
			"id": "X85j8Rze",
			"type": "rectangle",
			"x": 331.5,
			"y": -1453.83,
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
			"seed": 1085799936,
			"version": 2,
			"versionNonce": 980509720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YajXbijf"
				},
				{
					"type": "arrow",
					"id": "as8GzRPU"
				},
				{
					"type": "arrow",
					"id": "NySMrtTD"
				},
				{
					"type": "arrow",
					"id": "VYUx3USe"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0e"
		},
		{
			"id": "YajXbijf",
			"type": "text",
			"x": 351.5,
			"y": -1441.83,
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
			"seed": 1796033421,
			"version": 2,
			"versionNonce": 1792575848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "驅動問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "X85j8Rze",
			"originalText": "驅動問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0f"
		},
		{
			"id": "wDvbhDhG",
			"type": "rectangle",
			"x": 548.5,
			"y": -1479.95,
			"width": 290,
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
			"seed": 2078926973,
			"version": 2,
			"versionNonce": 870129944,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "d9uMbrb8"
				},
				{
					"type": "arrow",
					"id": "NySMrtTD"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0g"
		},
		{
			"id": "d9uMbrb8",
			"type": "text",
			"x": 562.5,
			"y": -1470.95,
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
			"seed": 1893330619,
			"version": 2,
			"versionNonce": 1557339240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "多筆行程、跳過無效、最後摘要",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wDvbhDhG",
			"originalText": "多筆行程、跳過無效、最後摘要",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0h"
		},
		{
			"id": "AuEdX5mU",
			"type": "rectangle",
			"x": 548.5,
			"y": -1425.45,
			"width": 443,
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
			"seed": 1047932234,
			"version": 2,
			"versionNonce": 1657355800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DH5XBEkr"
				},
				{
					"type": "arrow",
					"id": "VYUx3USe"
				},
				{
					"type": "arrow",
					"id": "4Xb9tAys"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0i"
		},
		{
			"id": "DH5XBEkr",
			"type": "text",
			"x": 562.5,
			"y": -1416.45,
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
			"seed": 1004114070,
			"version": 2,
			"versionNonce": 2013482856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Campus 12.5／45、Bad −1／30、Station 3.5／\n30、DONE",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AuEdX5mU",
			"originalText": "Campus 12.5／45、Bad −1／30、Station 3.5／\n30、DONE",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0j"
		},
		{
			"id": "mGmZkbFj",
			"type": "rectangle",
			"x": 1051.5,
			"y": -1410.95,
			"width": 343,
			"height": 34,
			"angle": 0,
			"strokeColor": "#1971c2",
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
			"seed": 2116976798,
			"version": 2,
			"versionNonce": 2016000792,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2LyMbQwj"
				},
				{
					"type": "arrow",
					"id": "4Xb9tAys"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0k"
		},
		{
			"id": "2LyMbQwj",
			"type": "text",
			"x": 1063.5,
			"y": -1403.95,
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
			"seed": 670278515,
			"version": 2,
			"versionNonce": 1152721512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "→ 2 筆、16.00 km、75 min、12.80 km/h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mGmZkbFj",
			"originalText": "→ 2 筆、16.00 km、75 min、12.80 km/h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0l"
		},
		{
			"id": "TAYHDTqZ",
			"type": "rectangle",
			"x": 331.5,
			"y": -1066.68,
			"width": 255,
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
			"seed": 1044907513,
			"version": 2,
			"versionNonce": 1718786072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5DNgEGCr"
				},
				{
					"type": "arrow",
					"id": "MnwupKMv"
				},
				{
					"type": "arrow",
					"id": "A8NWgHGc"
				},
				{
					"type": "arrow",
					"id": "ZsbmsyMC"
				},
				{
					"type": "arrow",
					"id": "vzRy4aCP"
				},
				{
					"type": "arrow",
					"id": "tb8arqUp"
				},
				{
					"type": "arrow",
					"id": "9cEB9B5f"
				},
				{
					"type": "arrow",
					"id": "NTiH4q9N"
				},
				{
					"type": "arrow",
					"id": "gckUSzzt"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0m"
		},
		{
			"id": "5DNgEGCr",
			"type": "text",
			"x": 351.5,
			"y": -1054.68,
			"width": 215,
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
			"seed": 563096615,
			"version": 2,
			"versionNonce": 1639224680,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q1 要重複的是什麼",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TAYHDTqZ",
			"originalText": "Q1 要重複的是什麼",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0n"
		},
		{
			"id": "YZqjDy2H",
			"type": "rectangle",
			"x": 662.5,
			"y": -1318.45,
			"width": 459,
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
			"seed": 1193459471,
			"version": 2,
			"versionNonce": 832034072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gpthhWfA"
				},
				{
					"type": "arrow",
					"id": "A8NWgHGc"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0o"
		},
		{
			"id": "gpthhWfA",
			"type": "text",
			"x": 676.5,
			"y": -1309.45,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1835761787,
			"version": 2,
			"versionNonce": 877504616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "複製三份程式 ✗ → 規則寫一次，用迴圈決定要不要\n再做",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YZqjDy2H",
			"originalText": "複製三份程式 ✗ → 規則寫一次，用迴圈決定要不要\n再做",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0p"
		},
		{
			"id": "7H8x2X33",
			"type": "rectangle",
			"x": 662.5,
			"y": -1241.45,
			"width": 449,
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
			"seed": 940299561,
			"version": 2,
			"versionNonce": 1057845784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zagVwNpt"
				},
				{
					"type": "arrow",
					"id": "ZsbmsyMC"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0q"
		},
		{
			"id": "zagVwNpt",
			"type": "text",
			"x": 676.5,
			"y": -1232.45,
			"width": 421,
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
			"seed": 1821684076,
			"version": 2,
			"versionNonce": 407657320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "迴圈之前：初始化 session 狀態（0 筆、0.0 km）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7H8x2X33",
			"originalText": "迴圈之前：初始化 session 狀態（0 筆、0.0 km）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0r"
		},
		{
			"id": "bn4WwVKV",
			"type": "rectangle",
			"x": 662.5,
			"y": -1186.95,
			"width": 361,
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
			"seed": 1055228609,
			"version": 2,
			"versionNonce": 633827096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4c5aCZr6"
				},
				{
					"type": "arrow",
					"id": "vzRy4aCP"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0s"
		},
		{
			"id": "4c5aCZr6",
			"type": "text",
			"x": 676.5,
			"y": -1177.95,
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
			"seed": 1450107450,
			"version": 2,
			"versionNonce": 268217960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "每次迴圈：讀一筆 → 停止／拒絕／接受",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bn4WwVKV",
			"originalText": "每次迴圈：讀一筆 → 停止／拒絕／接受",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0t"
		},
		{
			"id": "2yDPPdZc",
			"type": "rectangle",
			"x": 662.5,
			"y": -1132.45,
			"width": 216,
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
			"seed": 50743894,
			"version": 2,
			"versionNonce": 2117717016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "k5SJgvMy"
				},
				{
					"type": "arrow",
					"id": "tb8arqUp"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0u"
		},
		{
			"id": "k5SJgvMy",
			"type": "text",
			"x": 676.5,
			"y": -1123.45,
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
			"seed": 2043645112,
			"version": 2,
			"versionNonce": 1948950888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "迴圈之後：印一次摘要",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2yDPPdZc",
			"originalText": "迴圈之後：印一次摘要",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0v"
		},
		{
			"id": "Y39ArsAZ",
			"type": "rectangle",
			"x": 662.5,
			"y": -1077.95,
			"width": 451,
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
			"seed": 579715680,
			"version": 2,
			"versionNonce": 844663064,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6xKmsLqS"
				},
				{
					"type": "arrow",
					"id": "9cEB9B5f"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0w"
		},
		{
			"id": "6xKmsLqS",
			"type": "text",
			"x": 676.5,
			"y": -1068.95,
			"width": 423,
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
			"seed": 2095279552,
			"version": 2,
			"versionNonce": 606221416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "iteration ≠ session；被拒絕也用掉一次 iteration",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Y39ArsAZ",
			"originalText": "iteration ≠ session；被拒絕也用掉一次 iteration",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0x"
		},
		{
			"id": "caxnfwF7",
			"type": "rectangle",
			"x": 662.5,
			"y": -945.3,
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
			"groupIds": [
				"TULgHqYt"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 167284371,
			"version": 2,
			"versionNonce": 1301784088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iKk6qbJL"
				},
				{
					"type": "arrow",
					"id": "NTiH4q9N"
				},
				{
					"type": "arrow",
					"id": "YULdmkQf"
				},
				{
					"type": "arrow",
					"id": "NE8LvuKT"
				},
				{
					"type": "arrow",
					"id": "3WTbN8PC"
				},
				{
					"type": "arrow",
					"id": "9CBLUEdQ"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b0y"
		},
		{
			"id": "iKk6qbJL",
			"type": "text",
			"x": 676.5,
			"y": -936.3,
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
			"groupIds": [
				"TULgHqYt"
			],
			"frameId": null,
			"roundness": null,
			"seed": 651799022,
			"version": 2,
			"versionNonce": 900687720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "v0.4 協定",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "caxnfwF7",
			"originalText": "v0.4 協定",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b0z"
		},
		{
			"id": "EpRTrq3H",
			"type": "rectangle",
			"x": 835.5,
			"y": -1023.45,
			"width": 357,
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
			"seed": 1385711262,
			"version": 2,
			"versionNonce": 1290478360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FbQAKfg7"
				},
				{
					"type": "arrow",
					"id": "YULdmkQf"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b10"
		},
		{
			"id": "FbQAKfg7",
			"type": "text",
			"x": 847.5,
			"y": -1016.45,
			"width": 333,
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
			"seed": 802291676,
			"version": 2,
			"versionNonce": 622738024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "精確大寫 DONE → 立即停止，不問距離時間",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EpRTrq3H",
			"originalText": "精確大寫 DONE → 立即停止，不問距離時間",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b11"
		},
		{
			"id": "yaUJmgAv",
			"type": "rectangle",
			"x": 835.5,
			"y": -956.65,
			"width": 270,
			"height": 34,
			"angle": 0,
			"strokeColor": "#2f9e44",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"HYC9Vivm"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1455765638,
			"version": 2,
			"versionNonce": 1858535448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZiBSEKNW"
				},
				{
					"type": "arrow",
					"id": "NE8LvuKT"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b12"
		},
		{
			"id": "ZiBSEKNW",
			"type": "text",
			"x": 847.5,
			"y": -949.65,
			"width": 246,
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
				"HYC9Vivm"
			],
			"frameId": null,
			"roundness": null,
			"seed": 294488724,
			"version": 2,
			"versionNonce": 87731560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "無效 → 印第一個錯誤，總和不變",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yaUJmgAv",
			"originalText": "無效 → 印第一個錯誤，總和不變",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b13"
		},
		{
			"id": "PMm7DuDu",
			"type": "rectangle",
			"x": 835.5,
			"y": -908.65,
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
			"seed": 2021734894,
			"version": 2,
			"versionNonce": 52378904,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ypb38Q6d"
				},
				{
					"type": "arrow",
					"id": "3WTbN8PC"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b14"
		},
		{
			"id": "ypb38Q6d",
			"type": "text",
			"x": 847.5,
			"y": -901.65,
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
			"seed": 1042743767,
			"version": 2,
			"versionNonce": 793821288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "有效 → 報告，筆數與總和各更新一次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PMm7DuDu",
			"originalText": "有效 → 報告，筆數與總和各更新一次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b15"
		},
		{
			"id": "MP5fiNVX",
			"type": "rectangle",
			"x": 835.5,
			"y": -860.65,
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
			"seed": 240484358,
			"version": 2,
			"versionNonce": 996661784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "JEBMXz7G"
				},
				{
					"type": "arrow",
					"id": "9CBLUEdQ"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b16"
		},
		{
			"id": "JEBMXz7G",
			"type": "text",
			"x": 847.5,
			"y": -853.65,
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
			"seed": 442212714,
			"version": 2,
			"versionNonce": 1932292968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "沒有有效資料 → 明確訊息，不算平均",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MP5fiNVX",
			"originalText": "沒有有效資料 → 明確訊息，不算平均",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b17"
		},
		{
			"id": "LFcadkb8",
			"type": "rectangle",
			"x": 662.5,
			"y": -812.65,
			"width": 381,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#2f9e44",
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
			"seed": 1474897511,
			"version": 2,
			"versionNonce": 2056574744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UCAQ9wWm"
				},
				{
					"type": "arrow",
					"id": "gckUSzzt"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b18"
		},
		{
			"id": "UCAQ9wWm",
			"type": "text",
			"x": 676.5,
			"y": -803.65,
			"width": 353,
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
			"seed": 88729591,
			"version": 2,
			"versionNonce": 1192871528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 零距離仍是資料，不能拿 0 當結束命令",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LFcadkb8",
			"originalText": "⚠ 零距離仍是資料，不能拿 0 當結束命令",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b19"
		},
		{
			"id": "nTt2HRNz",
			"type": "rectangle",
			"x": 331.5,
			"y": -369.53,
			"width": 235,
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
			"seed": 1643029542,
			"version": 2,
			"versionNonce": 622474264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ix6XnCMY"
				},
				{
					"type": "arrow",
					"id": "GAhbvBqh"
				},
				{
					"type": "arrow",
					"id": "iAGc8r2F"
				},
				{
					"type": "arrow",
					"id": "62yekq59"
				},
				{
					"type": "arrow",
					"id": "4B8Z6tZw"
				},
				{
					"type": "arrow",
					"id": "KeRkLNiH"
				},
				{
					"type": "arrow",
					"id": "7L3E7Q9L"
				},
				{
					"type": "arrow",
					"id": "6S5QFGwF"
				},
				{
					"type": "arrow",
					"id": "KchLNXtX"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1A"
		},
		{
			"id": "ix6XnCMY",
			"type": "text",
			"x": 351.5,
			"y": -357.53,
			"width": 195,
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
			"seed": 2133521692,
			"version": 2,
			"versionNonce": 2011478376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q2 for 逐項處理",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nTt2HRNz",
			"originalText": "Q2 for 逐項處理",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1B"
		},
		{
			"id": "C322P6n5",
			"type": "rectangle",
			"x": 642.5,
			"y": -728.15,
			"width": 452,
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
			"seed": 1219328068,
			"version": 2,
			"versionNonce": 1894510872,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "f66JZgFZ"
				},
				{
					"type": "arrow",
					"id": "iAGc8r2F"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1C"
		},
		{
			"id": "f66JZgFZ",
			"type": "text",
			"x": 656.5,
			"y": -719.15,
			"width": 424,
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
			"seed": 50614717,
			"version": 2,
			"versionNonce": 1490635880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "for character in \"loop\" → l o o p（重複值照樣處\n理）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "C322P6n5",
			"originalText": "for character in \"loop\" → l o o p（重複值照樣處\n理）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1D"
		},
		{
			"id": "M9LHH6pK",
			"type": "rectangle",
			"x": 642.5,
			"y": -651.15,
			"width": 264,
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
			"seed": 411576613,
			"version": 2,
			"versionNonce": 897453592,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WExbyMNy"
				},
				{
					"type": "arrow",
					"id": "62yekq59"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "WExbyMNy",
			"type": "text",
			"x": 656.5,
			"y": -642.15,
			"width": 236,
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
			"seed": 583667436,
			"version": 2,
			"versionNonce": 1942191976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "iterable：能依序提供下一項",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M9LHH6pK",
			"originalText": "iterable：能依序提供下一項",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "ceSB6eQP",
			"type": "rectangle",
			"x": 642.5,
			"y": -596.65,
			"width": 407,
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
			"seed": 876765639,
			"version": 2,
			"versionNonce": 1002736408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mBPr2f28"
				},
				{
					"type": "arrow",
					"id": "4B8Z6tZw"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "mBPr2f28",
			"type": "text",
			"x": 656.5,
			"y": -587.65,
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
			"seed": 2068364633,
			"version": 2,
			"versionNonce": 955208296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "縮排決定重複範圍：Finished 在外面只印一次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ceSB6eQP",
			"originalText": "縮排決定重複範圍：Finished 在外面只印一次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "anqnurYB",
			"type": "rectangle",
			"x": 642.5,
			"y": -392.2,
			"width": 208,
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
			"seed": 735515148,
			"version": 2,
			"versionNonce": 238250008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "U9hfj8ri"
				},
				{
					"type": "arrow",
					"id": "KeRkLNiH"
				},
				{
					"type": "arrow",
					"id": "XhsjQSgs"
				},
				{
					"type": "arrow",
					"id": "hTjS3YZL"
				},
				{
					"type": "arrow",
					"id": "pG3y6Vug"
				},
				{
					"type": "arrow",
					"id": "cSk5aUpg"
				},
				{
					"type": "arrow",
					"id": "VJCgDw3k"
				},
				{
					"type": "arrow",
					"id": "tsHbVTwy"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "U9hfj8ri",
			"type": "text",
			"x": 656.5,
			"y": -383.2,
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
			"seed": 2124220443,
			"version": 2,
			"versionNonce": 791201128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "range（含頭不含尾）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "anqnurYB",
			"originalText": "range（含頭不含尾）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "Dd2rXLJe",
			"type": "rectangle",
			"x": 910.5,
			"y": -542.15,
			"width": 193,
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
			"seed": 1013962709,
			"version": 2,
			"versionNonce": 1220453656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9U7Xihbw"
				},
				{
					"type": "arrow",
					"id": "XhsjQSgs"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "9U7Xihbw",
			"type": "text",
			"x": 922.5,
			"y": -535.15,
			"width": 169,
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
			"seed": 814957198,
			"version": 2,
			"versionNonce": 599513192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "range(4) → 0, 1, 2, 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Dd2rXLJe",
			"originalText": "range(4) → 0, 1, 2, 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "FQt6KpCG",
			"type": "rectangle",
			"x": 910.5,
			"y": -475.35,
			"width": 190,
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
				"EDK6YFSj"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 295730686,
			"version": 2,
			"versionNonce": 1759134232,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rCbDGrF2"
				},
				{
					"type": "arrow",
					"id": "hTjS3YZL"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "rCbDGrF2",
			"type": "text",
			"x": 922.5,
			"y": -468.35,
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
			"groupIds": [
				"EDK6YFSj"
			],
			"frameId": null,
			"roundness": null,
			"seed": 37907345,
			"version": 2,
			"versionNonce": 1517587304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "range(1, 4) → 1, 2, 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FQt6KpCG",
			"originalText": "range(1, 4) → 1, 2, 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "mBcnanVG",
			"type": "rectangle",
			"x": 910.5,
			"y": -408.55,
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
			"groupIds": [
				"ykJVpj8g"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1344153586,
			"version": 2,
			"versionNonce": 494550808,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SDamLrvA"
				},
				{
					"type": "arrow",
					"id": "pG3y6Vug"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "SDamLrvA",
			"type": "text",
			"x": 922.5,
			"y": -401.55,
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
			"groupIds": [
				"ykJVpj8g"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1038691546,
			"version": 2,
			"versionNonce": 1033821800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "range(6, 0, -2) → 6, 4, 2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mBcnanVG",
			"originalText": "range(6, 0, -2) → 6, 4, 2",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "kK8uwrSS",
			"type": "rectangle",
			"x": 910.5,
			"y": -360.55,
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
			"seed": 574207491,
			"version": 2,
			"versionNonce": 387095576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fTjMEW7P"
				},
				{
					"type": "arrow",
					"id": "cSk5aUpg"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "fTjMEW7P",
			"type": "text",
			"x": 922.5,
			"y": -353.55,
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
			"seed": 1906300039,
			"version": 2,
			"versionNonce": 235327848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "range(8, 3) → 空（合法）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kK8uwrSS",
			"originalText": "range(8, 3) → 空（合法）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "JRMg24Dk",
			"type": "rectangle",
			"x": 910.5,
			"y": -312.55,
			"width": 269,
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
			"seed": 1429580441,
			"version": 2,
			"versionNonce": 1469536536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VyBge7hb"
				},
				{
					"type": "arrow",
					"id": "VJCgDw3k"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "VyBge7hb",
			"type": "text",
			"x": 922.5,
			"y": -305.55,
			"width": 245,
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
			"seed": 2051494866,
			"version": 2,
			"versionNonce": 318268520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ range(0, 5, 0) → ValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JRMg24Dk",
			"originalText": "⚠ range(0, 5, 0) → ValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "zMD7fQie",
			"type": "rectangle",
			"x": 910.5,
			"y": -245.75,
			"width": 436,
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
				"tpqK9ULK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1552559085,
			"version": 2,
			"versionNonce": 41711128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9KFtyuqL"
				},
				{
					"type": "arrow",
					"id": "tsHbVTwy"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "9KFtyuqL",
			"type": "text",
			"x": 922.5,
			"y": -238.75,
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
				"tpqK9ULK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1032555350,
			"version": 2,
			"versionNonce": 1245681512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "range(5, 1, -2) → 5, 3；range(2, 2) → 空（零次也正\n常）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zMD7fQie",
			"originalText": "range(5, 1, -2) → 5, 3；range(2, 2) → 空（零次也正\n常）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "HZVUEymU",
			"type": "rectangle",
			"x": 642.5,
			"y": -158.95,
			"width": 439,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#e8590c",
			"backgroundColor": "#fff4e6",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"L6RVy2dX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 56386426,
			"version": 2,
			"versionNonce": 750121752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MV3Xh4CP"
				},
				{
					"type": "arrow",
					"id": "7L3E7Q9L"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "MV3Xh4CP",
			"type": "text",
			"x": 656.5,
			"y": -149.95,
			"width": 411,
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
				"L6RVy2dX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 277449586,
			"version": 2,
			"versionNonce": 405301864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "迴圈裡改 i 不影響下一輪：range 照樣給下一個值",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HZVUEymU",
			"originalText": "迴圈裡改 i 不影響下一輪：range 照樣給下一個值",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "FxJVkajq",
			"type": "rectangle",
			"x": 642.5,
			"y": -85.65,
			"width": 454,
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
				"Se8hmwsC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1508065864,
			"version": 2,
			"versionNonce": 750243864,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nkxTgxsd"
				},
				{
					"type": "arrow",
					"id": "6S5QFGwF"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "nkxTgxsd",
			"type": "text",
			"x": 656.5,
			"y": -76.65,
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
			"groupIds": [
				"Se8hmwsC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1441059449,
			"version": 2,
			"versionNonce": 2004802920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "迭代次數 ≠ 成功次數（0、20、30 → 試 3 次接受\n2 次）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FxJVkajq",
			"originalText": "迭代次數 ≠ 成功次數（0、20、30 → 試 3 次接受\n2 次）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "PyXgvGjt",
			"type": "rectangle",
			"x": 642.5,
			"y": -8.65,
			"width": 408,
			"height": 40.5,
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
			"seed": 2126265786,
			"version": 2,
			"versionNonce": 1786121496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mRKpQNxR"
				},
				{
					"type": "arrow",
					"id": "KchLNXtX"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "mRKpQNxR",
			"type": "text",
			"x": 656.5,
			"y": 0.35,
			"width": 380,
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
			"seed": 285687591,
			"version": 2,
			"versionNonce": 697233512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ 考古題 A4、B4：固定次數 for＋同時指派",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PyXgvGjt",
			"originalText": "★ 考古題 A4、B4：固定次數 for＋同時指派",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "YKEjLT4u",
			"type": "rectangle",
			"x": 331.5,
			"y": 359.07,
			"width": 259,
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
			"seed": 1065253707,
			"version": 2,
			"versionNonce": 795126296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CcWa4wQW"
				},
				{
					"type": "arrow",
					"id": "8CVkAwGq"
				},
				{
					"type": "arrow",
					"id": "yxnQj9fh"
				},
				{
					"type": "arrow",
					"id": "wsPmizLu"
				},
				{
					"type": "arrow",
					"id": "68UwgQSN"
				},
				{
					"type": "arrow",
					"id": "8MQJMyUr"
				},
				{
					"type": "arrow",
					"id": "YPhKJhfX"
				},
				{
					"type": "arrow",
					"id": "ffXXeHVL"
				},
				{
					"type": "arrow",
					"id": "jYjbq7aj"
				},
				{
					"type": "arrow",
					"id": "tdStvWc4"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "CcWa4wQW",
			"type": "text",
			"x": 351.5,
			"y": 371.07,
			"width": 219,
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
			"seed": 341566418,
			"version": 2,
			"versionNonce": 1713677160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q3 記住前面的資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YKEjLT4u",
			"originalText": "Q3 記住前面的資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "7aJU73aY",
			"type": "rectangle",
			"x": 666.5,
			"y": 94.65,
			"width": 409,
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
				"qRh5gRV3"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1947530071,
			"version": 2,
			"versionNonce": 1987553048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xQKyrjvS"
				},
				{
					"type": "arrow",
					"id": "yxnQj9fh"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "xQKyrjvS",
			"type": "text",
			"x": 680.5,
			"y": 103.65,
			"width": 381,
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
				"qRh5gRV3"
			],
			"frameId": null,
			"roundness": null,
			"seed": 726855696,
			"version": 2,
			"versionNonce": 193721960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "counter：有幾筆；accumulator：加起來多少",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7aJU73aY",
			"originalText": "counter：有幾筆；accumulator：加起來多少",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "JGSz97uw",
			"type": "rectangle",
			"x": 666.5,
			"y": 149.15,
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
			"seed": 1271925962,
			"version": 2,
			"versionNonce": 1008927768,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "A5ZWz79b"
				},
				{
					"type": "arrow",
					"id": "wsPmizLu"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "A5ZWz79b",
			"type": "text",
			"x": 680.5,
			"y": 158.15,
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
			"seed": 449513493,
			"version": 2,
			"versionNonce": 1318119784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "迴圈前初始化一次；只在接受時更新",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JGSz97uw",
			"originalText": "迴圈前初始化一次；只在接受時更新",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "LpEYhARf",
			"type": "rectangle",
			"x": 666.5,
			"y": 203.65,
			"width": 202,
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
			"seed": 1951549973,
			"version": 2,
			"versionNonce": 1314570520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "juwX3Ubn"
				},
				{
					"type": "arrow",
					"id": "68UwgQSN"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "juwX3Ubn",
			"type": "text",
			"x": 680.5,
			"y": 212.65,
			"width": 174,
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
			"seed": 90620937,
			"version": 2,
			"versionNonce": 1786739816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "1 + 2 + 3 + 4 → 10",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LpEYhARf",
			"originalText": "1 + 2 + 3 + 4 → 10",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "cfqrcanz",
			"type": "rectangle",
			"x": 666.5,
			"y": 276.95,
			"width": 471,
			"height": 63,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#f3f0ff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"5nVHQqQX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1695485066,
			"version": 2,
			"versionNonce": 479387160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qrMzDAxn"
				},
				{
					"type": "arrow",
					"id": "8MQJMyUr"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "qrMzDAxn",
			"type": "text",
			"x": 680.5,
			"y": 285.95,
			"width": 443,
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
				"5nVHQqQX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1196101442,
			"version": 2,
			"versionNonce": 1361293160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Loop invariant：每輪結束 total＝已處理項目的和；\nn = 0 時仍成立",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cfqrcanz",
			"originalText": "Loop invariant：每輪結束 total＝已處理項目的和；\nn = 0 時仍成立",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "5TK5pAfY",
			"type": "rectangle",
			"x": 666.5,
			"y": 372.75,
			"width": 367,
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
				"wU2v8u8W"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1457905303,
			"version": 2,
			"versionNonce": 129981208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5xrzMGyW"
				},
				{
					"type": "arrow",
					"id": "YPhKJhfX"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "5xrzMGyW",
			"type": "text",
			"x": 680.5,
			"y": 381.75,
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
			"groupIds": [
				"wU2v8u8W"
			],
			"frameId": null,
			"roundness": null,
			"seed": 586034244,
			"version": 2,
			"versionNonce": 1523155560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ total = 0 放進迴圈 → 只剩最後的 4",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5TK5pAfY",
			"originalText": "⚠ total = 0 放進迴圈 → 只剩最後的 4",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "ij9hHijC",
			"type": "rectangle",
			"x": 666.5,
			"y": 427.25,
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
			"seed": 1350932459,
			"version": 2,
			"versionNonce": 844380184,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YQL3gnkS"
				},
				{
					"type": "arrow",
					"id": "ffXXeHVL"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "YQL3gnkS",
			"type": "text",
			"x": 680.5,
			"y": 436.25,
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
			"seed": 894112923,
			"version": 2,
			"versionNonce": 1983706472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "總和只描述「已接受的前綴」",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ij9hHijC",
			"originalText": "總和只描述「已接受的前綴」",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "yH2c8KA9",
			"type": "rectangle",
			"x": 666.5,
			"y": 526.5,
			"width": 234,
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
				"FiVUm5EP"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1401501455,
			"version": 2,
			"versionNonce": 1346729240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PUjKJUSe"
				},
				{
					"type": "arrow",
					"id": "jYjbq7aj"
				},
				{
					"type": "arrow",
					"id": "8h9ku82E"
				},
				{
					"type": "arrow",
					"id": "Fqa9jNvT"
				},
				{
					"type": "arrow",
					"id": "SKcvpd53"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "PUjKJUSe",
			"type": "text",
			"x": 680.5,
			"y": 535.5,
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
				"FiVUm5EP"
			],
			"frameId": null,
			"roundness": null,
			"seed": 346704288,
			"version": 2,
			"versionNonce": 1489635432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "平均要先說清楚平均什麼",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yH2c8KA9",
			"originalText": "平均要先說清楚平均什麼",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "m7hqUipb",
			"type": "rectangle",
			"x": 960.5,
			"y": 481.75,
			"width": 299,
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
			"seed": 601975111,
			"version": 2,
			"versionNonce": 1996952088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "g97HAsJQ"
				},
				{
					"type": "arrow",
					"id": "8h9ku82E"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "g97HAsJQ",
			"type": "text",
			"x": 972.5,
			"y": 488.75,
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
			"seed": 635768321,
			"version": 2,
			"versionNonce": 775732072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "mean duration = 75 / 2 = 37.5 min",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "m7hqUipb",
			"originalText": "mean duration = 75 / 2 = 37.5 min",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "QpuYmbKW",
			"type": "rectangle",
			"x": 960.5,
			"y": 529.75,
			"width": 325,
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
			"seed": 2055179485,
			"version": 2,
			"versionNonce": 1837960984,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "7uFisvJA"
				},
				{
					"type": "arrow",
					"id": "Fqa9jNvT"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "7uFisvJA",
			"type": "text",
			"x": 972.5,
			"y": 536.75,
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
			"seed": 1760525815,
			"version": 2,
			"versionNonce": 1222708840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "overall speed = 16 / 1.25 = 12.8 km/h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QpuYmbKW",
			"originalText": "overall speed = 16 / 1.25 = 12.8 km/h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "5987aiiL",
			"type": "rectangle",
			"x": 960.5,
			"y": 577.75,
			"width": 364,
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
			"seed": 1459548269,
			"version": 2,
			"versionNonce": 2085317656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WDTJnAhU"
				},
				{
					"type": "arrow",
					"id": "SKcvpd53"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "WDTJnAhU",
			"type": "text",
			"x": 972.5,
			"y": 584.75,
			"width": 340,
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
			"seed": 754339915,
			"version": 2,
			"versionNonce": 1367540072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ (16.67 + 7.00) / 2 ≈ 11.83 是另一個問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5987aiiL",
			"originalText": "⚠ (16.67 + 7.00) / 2 ≈ 11.83 是另一個問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "vN86B8m3",
			"type": "rectangle",
			"x": 666.5,
			"y": 625.75,
			"width": 448,
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
			"seed": 1843536025,
			"version": 2,
			"versionNonce": 1026959640,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2vp2MF2h"
				},
				{
					"type": "arrow",
					"id": "tdStvWc4"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "2vp2MF2h",
			"type": "text",
			"x": 680.5,
			"y": 634.75,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 95814850,
			"version": 2,
			"versionNonce": 2003735656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab A：10、20、30 → 20.0；有拒絕時分母不能\n寫死 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vN86B8m3",
			"originalText": "Lab A：10、20、30 → 20.0；有拒絕時分母不能\n寫死 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "LJ9CbGCt",
			"type": "rectangle",
			"x": 331.5,
			"y": 1083.12,
			"width": 226,
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
			"seed": 1869769436,
			"version": 2,
			"versionNonce": 1807828504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XppQruja"
				},
				{
					"type": "arrow",
					"id": "YH44zzZN"
				},
				{
					"type": "arrow",
					"id": "zbduLGQG"
				},
				{
					"type": "arrow",
					"id": "QfWEQXZM"
				},
				{
					"type": "arrow",
					"id": "DHqFxUdS"
				},
				{
					"type": "arrow",
					"id": "tQC7wnFg"
				},
				{
					"type": "arrow",
					"id": "WaFjZDrA"
				},
				{
					"type": "arrow",
					"id": "K93rvhwr"
				},
				{
					"type": "arrow",
					"id": "r8VEQLy4"
				},
				{
					"type": "arrow",
					"id": "7ZTTwPx5"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "XppQruja",
			"type": "text",
			"x": 351.5,
			"y": 1095.12,
			"width": 186,
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
			"seed": 523433685,
			"version": 2,
			"versionNonce": 544196456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q4 while 與停止",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LJ9CbGCt",
			"originalText": "Q4 while 與停止",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "46pU4kiZ",
			"type": "rectangle",
			"x": 633.5,
			"y": 751.55,
			"width": 342,
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
				"QwsPraaF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2006387638,
			"version": 2,
			"versionNonce": 887145240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vHuNJEsb"
				},
				{
					"type": "arrow",
					"id": "zbduLGQG"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "vHuNJEsb",
			"type": "text",
			"x": 647.5,
			"y": 760.55,
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
			"groupIds": [
				"QwsPraaF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 640253365,
			"version": 2,
			"versionNonce": 416455272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "每次先檢查條件；一開始就假 → 零次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "46pU4kiZ",
			"originalText": "每次先檢查條件；一開始就假 → 零次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "Qf8jdQXV",
			"type": "rectangle",
			"x": 633.5,
			"y": 824.85,
			"width": 448,
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
				"aPaS73JZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 831899967,
			"version": 2,
			"versionNonce": 118005784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MNVPK8kL"
				},
				{
					"type": "arrow",
					"id": "QfWEQXZM"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "MNVPK8kL",
			"type": "text",
			"x": 647.5,
			"y": 833.85,
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
				"aPaS73JZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1048904087,
			"version": 2,
			"versionNonce": 1130564968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "countdown：3 2 1 Go（for range(3, 0, -1) 結果\n相同）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Qf8jdQXV",
			"originalText": "countdown：3 2 1 Go（for range(3, 0, -1) 結果\n相同）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "9weZgXTc",
			"type": "rectangle",
			"x": 633.5,
			"y": 901.85,
			"width": 385,
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
			"seed": 1644541803,
			"version": 2,
			"versionNonce": 1647107352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hVwwEXU6"
				},
				{
					"type": "arrow",
					"id": "DHqFxUdS"
				},
				{
					"type": "arrow",
					"id": "L2Bx72FH"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "hVwwEXU6",
			"type": "text",
			"x": 647.5,
			"y": 910.85,
			"width": 357,
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
			"seed": 931695036,
			"version": 2,
			"versionNonce": 1231888488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Sentinel：while True → 先讀 route → if\nroute_name == \"DONE\": break",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9weZgXTc",
			"originalText": "Sentinel：while True → 先讀 route → if\nroute_name == \"DONE\": break",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "uudweeQp",
			"type": "rectangle",
			"x": 1078.5,
			"y": 925.75,
			"width": 409,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"uSZGD7Pf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1719468007,
			"version": 2,
			"versionNonce": 666991128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aV5S79kG"
				},
				{
					"type": "arrow",
					"id": "L2Bx72FH"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "aV5S79kG",
			"type": "text",
			"x": 1090.5,
			"y": 932.75,
			"width": 385,
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
				"uSZGD7Pf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 637769722,
			"version": 2,
			"versionNonce": 1253888872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "先比對 DONE 再轉型：int(\"DONE\") → ValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uudweeQp",
			"originalText": "先比對 DONE 再轉型：int(\"DONE\") → ValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "FBzhX9ua",
			"type": "rectangle",
			"x": 633.5,
			"y": 1047.6,
			"width": 327,
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
			"seed": 116686753,
			"version": 2,
			"versionNonce": 1790605080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YhugEsZx"
				},
				{
					"type": "arrow",
					"id": "tQC7wnFg"
				},
				{
					"type": "arrow",
					"id": "73RL8Aki"
				},
				{
					"type": "arrow",
					"id": "d8h9RAmh"
				},
				{
					"type": "arrow",
					"id": "sV7iuhaS"
				},
				{
					"type": "arrow",
					"id": "YJcZqeZT"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "YhugEsZx",
			"type": "text",
			"x": 647.5,
			"y": 1056.6,
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
			"seed": 2105442761,
			"version": 2,
			"versionNonce": 228468328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "選迴圈看「下一項從哪來、何時停」",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FBzhX9ua",
			"originalText": "選迴圈看「下一項從哪來、何時停」",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "3iXwzPev",
			"type": "rectangle",
			"x": 1020.5,
			"y": 978.85,
			"width": 267,
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
			"seed": 288275255,
			"version": 2,
			"versionNonce": 1066128408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4UdX9SUm"
				},
				{
					"type": "arrow",
					"id": "73RL8Aki"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "4UdX9SUm",
			"type": "text",
			"x": 1032.5,
			"y": 985.85,
			"width": 243,
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
			"seed": 1608273091,
			"version": 2,
			"versionNonce": 786241896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "走訪每個字元 → for ch in text",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3iXwzPev",
			"originalText": "走訪每個字元 → for ch in text",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "ygM3u3ZM",
			"type": "rectangle",
			"x": 1020.5,
			"y": 1026.85,
			"width": 254,
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
			"seed": 170762479,
			"version": 2,
			"versionNonce": 204050712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "g6TDhaqe"
				},
				{
					"type": "arrow",
					"id": "d8h9RAmh"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "g6TDhaqe",
			"type": "text",
			"x": 1032.5,
			"y": 1033.85,
			"width": 230,
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
			"seed": 116030734,
			"version": 2,
			"versionNonce": 1371909224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "剛好 n 次 → for i in range(n)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ygM3u3ZM",
			"originalText": "剛好 n 次 → for i in range(n)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "zpAwizk2",
			"type": "rectangle",
			"x": 1020.5,
			"y": 1074.85,
			"width": 297,
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
			"seed": 1552867496,
			"version": 2,
			"versionNonce": 1476898328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "B5FZHxyQ"
				},
				{
					"type": "arrow",
					"id": "sV7iuhaS"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "B5FZHxyQ",
			"type": "text",
			"x": 1032.5,
			"y": 1081.85,
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
			"seed": 1980842983,
			"version": 2,
			"versionNonce": 1344528232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "讀到 DONE → while True ＋ break",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zpAwizk2",
			"originalText": "讀到 DONE → while True ＋ break",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "tSWahfQ7",
			"type": "rectangle",
			"x": 1020.5,
			"y": 1122.85,
			"width": 363,
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
			"seed": 1234348319,
			"version": 2,
			"versionNonce": 471477016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "smxLfwsn"
				},
				{
					"type": "arrow",
					"id": "YJcZqeZT"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "smxLfwsn",
			"type": "text",
			"x": 1032.5,
			"y": 1129.85,
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
			"seed": 1386352600,
			"version": 2,
			"versionNonce": 1782821480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "收滿 n 筆有效 → while accepted_count < n",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tSWahfQ7",
			"originalText": "收滿 n 筆有效 → while accepted_count < n",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "5XuWTj5k",
			"type": "rectangle",
			"x": 633.5,
			"y": 1170.85,
			"width": 348,
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
			"seed": 1667178485,
			"version": 2,
			"versionNonce": 315951128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mX9gADz2"
				},
				{
					"type": "arrow",
					"id": "WaFjZDrA"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "mX9gADz2",
			"type": "text",
			"x": 647.5,
			"y": 1179.85,
			"width": 320,
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
			"seed": 1400613030,
			"version": 2,
			"versionNonce": 1995515240,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "0、20、30、40 → 試 4 次接受 3 次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5XuWTj5k",
			"originalText": "0、20、30、40 → 試 4 次接受 3 次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "wBkQJEGr",
			"type": "rectangle",
			"x": 633.5,
			"y": 1244.15,
			"width": 461,
			"height": 63,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"rtyhFewX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 192320344,
			"version": 2,
			"versionNonce": 137119000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YdsGKnvk"
				},
				{
					"type": "arrow",
					"id": "K93rvhwr"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "YdsGKnvk",
			"type": "text",
			"x": 647.5,
			"y": 1253.15,
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
				"rtyhFewX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 405194790,
			"version": 2,
			"versionNonce": 326645864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "倍增 while x < n: x *= 2：結束時 x / 2 < n ≤ x，\n不是 x ≤ n < 2x（n = 3 → x = 4）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wBkQJEGr",
			"originalText": "倍增 while x < n: x *= 2：結束時 x / 2 < n ≤ x，\n不是 x ≤ n < 2x（n = 3 → x = 4）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "aUuD3yZk",
			"type": "rectangle",
			"x": 633.5,
			"y": 1339.95,
			"width": 460,
			"height": 63,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#e3fafc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"JD7FG5CE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1372005178,
			"version": 2,
			"versionNonce": 697557528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZpSyBntT"
				},
				{
					"type": "arrow",
					"id": "r8VEQLy4"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "ZpSyBntT",
			"type": "text",
			"x": 647.5,
			"y": 1348.95,
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
				"JD7FG5CE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 66628154,
			"version": 2,
			"versionNonce": 1403317096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "找 ≤ n 的最大 2 的次方：條件寫 p * 2 <= n；寫成\np < n 時 n = 31 會得 32",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aUuD3yZk",
			"originalText": "找 ≤ n 的最大 2 的次方：條件寫 p * 2 <= n；寫成\np < n 時 n = 31 會得 32",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "5y5aGQ9x",
			"type": "rectangle",
			"x": 633.5,
			"y": 1416.95,
			"width": 453,
			"height": 63,
			"angle": 0,
			"strokeColor": "#0c8599",
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
			"seed": 295116625,
			"version": 2,
			"versionNonce": 1442832152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "R5zzVbyG"
				},
				{
					"type": "arrow",
					"id": "7ZTTwPx5"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "R5zzVbyG",
			"type": "text",
			"x": 647.5,
			"y": 1425.95,
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
			"seed": 1549209527,
			"version": 2,
			"versionNonce": 1908620904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ 考古題：while True ＋ break（質因數、倍增、\nFibonacci）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5y5aGQ9x",
			"originalText": "★ 考古題：while True ＋ break（質因數、倍增、\nFibonacci）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "U83SvdRz",
			"type": "rectangle",
			"x": -615.5,
			"y": -812.48,
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
			"seed": 821183757,
			"version": 2,
			"versionNonce": 1843674136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "78AZVRQQ"
				},
				{
					"type": "arrow",
					"id": "LiaYnucc"
				},
				{
					"type": "arrow",
					"id": "WJTHZhym"
				},
				{
					"type": "arrow",
					"id": "Uhusn9u9"
				},
				{
					"type": "arrow",
					"id": "6XYhcthE"
				},
				{
					"type": "arrow",
					"id": "3xt24btF"
				},
				{
					"type": "arrow",
					"id": "BEpvyB3j"
				},
				{
					"type": "arrow",
					"id": "3WUu4sRC"
				},
				{
					"type": "arrow",
					"id": "BSARj2ma"
				},
				{
					"type": "arrow",
					"id": "FfQQbgsR"
				},
				{
					"type": "arrow",
					"id": "G7KCHQaF"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "78AZVRQQ",
			"type": "text",
			"x": -595.5,
			"y": -800.48,
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
			"seed": 2147220046,
			"version": 2,
			"versionNonce": 2124362088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q5 停止、略過、繼續",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "U83SvdRz",
			"originalText": "Q5 停止、略過、繼續",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "BnvhbWju",
			"type": "rectangle",
			"x": -918.5,
			"y": -1130.5,
			"width": 227,
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
				"38ahX8XE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1474604153,
			"version": 2,
			"versionNonce": 590674200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vcpKSDDx"
				},
				{
					"type": "arrow",
					"id": "WJTHZhym"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "vcpKSDDx",
			"type": "text",
			"x": -904.5,
			"y": -1121.5,
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
			"groupIds": [
				"38ahX8XE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 816151158,
			"version": 2,
			"versionNonce": 293913704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "break：離開最內層迴圈",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BnvhbWju",
			"originalText": "break：離開最內層迴圈",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "ej8Q2qkR",
			"type": "rectangle",
			"x": -1019.5,
			"y": -1057.2,
			"width": 328,
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
				"xjuWtfn5"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 790332265,
			"version": 2,
			"versionNonce": 1231427096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2xVdLWcC"
				},
				{
					"type": "arrow",
					"id": "Uhusn9u9"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2W"
		},
		{
			"id": "2xVdLWcC",
			"type": "text",
			"x": -1005.5,
			"y": -1048.2,
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
			"groupIds": [
				"xjuWtfn5"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1131125839,
			"version": 2,
			"versionNonce": 2017458024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "continue：跳過本輪剩下，進下一輪",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ej8Q2qkR",
			"originalText": "continue：跳過本輪剩下，進下一輪",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "SqWgwWXa",
			"type": "rectangle",
			"x": -1094.5,
			"y": -983.9,
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
			"groupIds": [
				"y9W7cRah"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1809770629,
			"version": 2,
			"versionNonce": 627807000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "M4Ujer2Z"
				},
				{
					"type": "arrow",
					"id": "6XYhcthE"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "M4Ujer2Z",
			"type": "text",
			"x": -1080.5,
			"y": -974.9,
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
			"groupIds": [
				"y9W7cRah"
			],
			"frameId": null,
			"roundness": null,
			"seed": 75615468,
			"version": 2,
			"versionNonce": 1729940072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "DONE → break；無效完整資料 → continue",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SqWgwWXa",
			"originalText": "DONE → break；無效完整資料 → continue",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "fhXmc8vN",
			"type": "rectangle",
			"x": -977.5,
			"y": -929.4,
			"width": 286,
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
			"seed": 24824707,
			"version": 2,
			"versionNonce": 1035563032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "V7cN46a4"
				},
				{
					"type": "arrow",
					"id": "3xt24btF"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "V7cN46a4",
			"type": "text",
			"x": -963.5,
			"y": -920.4,
			"width": 258,
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
			"seed": 1060080197,
			"version": 2,
			"versionNonce": 686243176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "error 每筆重設；總和跨筆保留",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fhXmc8vN",
			"originalText": "error 每筆重設；總和跨筆保留",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
		},
		{
			"id": "g7sK6YRR",
			"type": "rectangle",
			"x": -1150.5,
			"y": -856.1,
			"width": 459,
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
				"HcDsSd4z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 866335943,
			"version": 2,
			"versionNonce": 709078296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FApQqziq"
				},
				{
					"type": "arrow",
					"id": "BEpvyB3j"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2c"
		},
		{
			"id": "FApQqziq",
			"type": "text",
			"x": -1136.5,
			"y": -847.1,
			"width": 431,
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
				"HcDsSd4z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 663993362,
			"version": 2,
			"versionNonce": 1324044392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "摘要在迴圈後；accepted_count == 0 → 不做除法",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g7sK6YRR",
			"originalText": "摘要在迴圈後；accepted_count == 0 → 不做除法",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2d"
		},
		{
			"id": "ei32iHru",
			"type": "rectangle",
			"x": -1030.5,
			"y": -782.8,
			"width": 339,
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
				"AHis2Vyd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 203103286,
			"version": 2,
			"versionNonce": 1685998104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8Qm2YKF9"
				},
				{
					"type": "arrow",
					"id": "3WUu4sRC"
				},
				{
					"type": "arrow",
					"id": "HDiLEPa9"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2e"
		},
		{
			"id": "8Qm2YKF9",
			"type": "text",
			"x": -1016.5,
			"y": -773.8,
			"width": 311,
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
				"AHis2Vyd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1674584631,
			"version": 2,
			"versionNonce": 1626669928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ continue 跳過 i += 1 → 無窮迴圈",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ei32iHru",
			"originalText": "⚠ continue 跳過 i += 1 → 無窮迴圈",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2f"
		},
		{
			"id": "Vtb4s422",
			"type": "rectangle",
			"x": -1523.5,
			"y": -779.55,
			"width": 433,
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
			"seed": 1773894738,
			"version": 2,
			"versionNonce": 391989016,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BiFJTuiF"
				},
				{
					"type": "arrow",
					"id": "HDiLEPa9"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2g"
		},
		{
			"id": "BiFJTuiF",
			"type": "text",
			"x": -1511.5,
			"y": -772.55,
			"width": 409,
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
			"seed": 1973421524,
			"version": 2,
			"versionNonce": 223368808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "修：skip 路徑也更新，或改 for i in range(1, 4) → 1 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Vtb4s422",
			"originalText": "修：skip 路徑也更新，或改 for i in range(1, 4) → 1 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2h"
		},
		{
			"id": "xh8ZbYYv",
			"type": "rectangle",
			"x": -796.5,
			"y": -674.15,
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
			"seed": 1982382579,
			"version": 2,
			"versionNonce": 1867818008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kK2rCAmj"
				},
				{
					"type": "arrow",
					"id": "BSARj2ma"
				},
				{
					"type": "arrow",
					"id": "kJ4iSCv2"
				},
				{
					"type": "arrow",
					"id": "kTiwGvcP"
				},
				{
					"type": "arrow",
					"id": "CHfWgFv7"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2i"
		},
		{
			"id": "kK2rCAmj",
			"type": "text",
			"x": -782.5,
			"y": -665.15,
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
			"seed": 1490338852,
			"version": 2,
			"versionNonce": 1489586536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "終止推理",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xh8ZbYYv",
			"originalText": "終止推理",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2j"
		},
		{
			"id": "jBy9UxdN",
			"type": "rectangle",
			"x": -1095.5,
			"y": -728.3,
			"width": 239,
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
			"seed": 373948367,
			"version": 2,
			"versionNonce": 1784176920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QLGFq2Ja"
				},
				{
					"type": "arrow",
					"id": "kJ4iSCv2"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2k"
		},
		{
			"id": "QLGFq2Ja",
			"type": "text",
			"x": -1083.5,
			"y": -721.3,
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
			"seed": 1154270918,
			"version": 2,
			"versionNonce": 1319885928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "for 有限 range：迭代器前進",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jBy9UxdN",
			"originalText": "for 有限 range：迭代器前進",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2l"
		},
		{
			"id": "MEVtFJLn",
			"type": "rectangle",
			"x": -1143.5,
			"y": -661.5,
			"width": 287,
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
				"uz7GiNwd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 888001407,
			"version": 2,
			"versionNonce": 668761624,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ayn2ns8d"
				},
				{
					"type": "arrow",
					"id": "kTiwGvcP"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2m"
		},
		{
			"id": "ayn2ns8d",
			"type": "text",
			"x": -1131.5,
			"y": -654.5,
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
			"groupIds": [
				"uz7GiNwd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 983054790,
			"version": 2,
			"versionNonce": 818155368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "countdown while：更新不能被跳過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MEVtFJLn",
			"originalText": "countdown while：更新不能被跳過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2n"
		},
		{
			"id": "w4FBsYjP",
			"type": "rectangle",
			"x": -1171.5,
			"y": -613.5,
			"width": 315,
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
			"seed": 53027040,
			"version": 2,
			"versionNonce": 953482008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HYsQeNFn"
				},
				{
					"type": "arrow",
					"id": "CHfWgFv7"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2o"
		},
		{
			"id": "HYsQeNFn",
			"type": "text",
			"x": -1159.5,
			"y": -606.5,
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
			"seed": 1415000379,
			"version": 2,
			"versionNonce": 660464232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "DONE 迴圈：靠使用者最後輸入 DONE",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "w4FBsYjP",
			"originalText": "DONE 迴圈：靠使用者最後輸入 DONE",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2p"
		},
		{
			"id": "dkCi9aqp",
			"type": "rectangle",
			"x": -1120.5,
			"y": -546.7,
			"width": 429,
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
				"R25NbwU8"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1868697236,
			"version": 2,
			"versionNonce": 1874188312,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4kAHunNt"
				},
				{
					"type": "arrow",
					"id": "FfQQbgsR"
				},
				{
					"type": "arrow",
					"id": "Twki3cR9"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2q"
		},
		{
			"id": "4kAHunNt",
			"type": "text",
			"x": -1106.5,
			"y": -537.7,
			"width": 401,
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
				"R25NbwU8"
			],
			"frameId": null,
			"roundness": null,
			"seed": 427957569,
			"version": 2,
			"versionNonce": 1900369256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "巢狀迴圈：外層每換 i，內層重來 → (1,1)…(2,3)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dkCi9aqp",
			"originalText": "巢狀迴圈：外層每換 i，內層重來 → (1,1)…(2,3)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2r"
		},
		{
			"id": "VWuhCmwm",
			"type": "rectangle",
			"x": -1500.5,
			"y": -534.05,
			"width": 320,
			"height": 34,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"XrURdY84"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 24093852,
			"version": 2,
			"versionNonce": 812848408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gcc5iYFU"
				},
				{
					"type": "arrow",
					"id": "Twki3cR9"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2s"
		},
		{
			"id": "gcc5iYFU",
			"type": "text",
			"x": -1488.5,
			"y": -527.05,
			"width": 296,
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
				"XrURdY84"
			],
			"frameId": null,
			"roundness": null,
			"seed": 409508446,
			"version": 2,
			"versionNonce": 331769960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 內層 break 只出內層 → (1,1)、(2,1)",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VWuhCmwm",
			"originalText": "⚠ 內層 break 只出內層 → (1,1)、(2,1)",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2t"
		},
		{
			"id": "C4ktU9QG",
			"type": "rectangle",
			"x": -1139.5,
			"y": -492.2,
			"width": 448,
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
			"seed": 289007584,
			"version": 2,
			"versionNonce": 1082176024,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fLKYEFK3"
				},
				{
					"type": "arrow",
					"id": "G7KCHQaF"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2u"
		},
		{
			"id": "fLKYEFK3",
			"type": "text",
			"x": -1125.5,
			"y": -483.2,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 269501736,
			"version": 2,
			"versionNonce": 179116904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab B：BLANK 1 break、BLANK 2 continue；0,\n20, −5, 30, DONE → 2；DONE 開頭 → 0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "C4ktU9QG",
			"originalText": "Lab B：BLANK 1 break、BLANK 2 continue；0,\n20, −5, 30, DONE → 2；DONE 開頭 → 0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2v"
		},
		{
			"id": "rFtNvije",
			"type": "rectangle",
			"x": -744.5,
			"y": -121.37,
			"width": 413,
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
			"seed": 210959628,
			"version": 2,
			"versionNonce": 382906136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8N6qpyZ5"
				},
				{
					"type": "arrow",
					"id": "gvT2LYKY"
				},
				{
					"type": "arrow",
					"id": "jc6bJKJd"
				},
				{
					"type": "arrow",
					"id": "tFueWyCd"
				},
				{
					"type": "arrow",
					"id": "99GXjpyK"
				},
				{
					"type": "arrow",
					"id": "JzGbYmnd"
				},
				{
					"type": "arrow",
					"id": "jtdUjsFb"
				},
				{
					"type": "arrow",
					"id": "6cTkMJs8"
				},
				{
					"type": "arrow",
					"id": "mc685ezf"
				},
				{
					"type": "arrow",
					"id": "7u5GeTN5"
				},
				{
					"type": "arrow",
					"id": "Nhcwp42h"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2w"
		},
		{
			"id": "8N6qpyZ5",
			"type": "text",
			"x": -724.5,
			"y": -109.37,
			"width": 373,
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
			"seed": 1239456948,
			"version": 2,
			"versionNonce": 2017816168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "電腦基礎：向後跳躍與記憶體區域\n性",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rFtNvije",
			"originalText": "電腦基礎：向後跳躍與記憶體區域\n性",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2x"
		},
		{
			"id": "gqTMBgKd",
			"type": "rectangle",
			"x": -1262.5,
			"y": -385.2,
			"width": 442,
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
			"seed": 1824175782,
			"version": 2,
			"versionNonce": 735906840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YTemFRiw"
				},
				{
					"type": "arrow",
					"id": "jc6bJKJd"
				},
				{
					"type": "arrow",
					"id": "UxtkcsHr"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b2y"
		},
		{
			"id": "YTemFRiw",
			"type": "text",
			"x": -1248.5,
			"y": -376.2,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 365492735,
			"version": 2,
			"versionNonce": 1432052072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "教學迴圈：CMP R0, 3 → JGE done → OUT →\nADD R0, 1 → JMP loop → 輸出 0 1 2",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gqTMBgKd",
			"originalText": "教學迴圈：CMP R0, 3 → JGE done → OUT →\nADD R0, 1 → JMP loop → 輸出 0 1 2",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2z"
		},
		{
			"id": "WBchT47U",
			"type": "rectangle",
			"x": -1691.5,
			"y": -370.7,
			"width": 369,
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
			"seed": 1312896628,
			"version": 2,
			"versionNonce": 1234422040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cQ8MvEJX"
				},
				{
					"type": "arrow",
					"id": "UxtkcsHr"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b30"
		},
		{
			"id": "cQ8MvEJX",
			"type": "text",
			"x": -1679.5,
			"y": -363.7,
			"width": 345,
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
			"seed": 1287522609,
			"version": 2,
			"versionNonce": 557511784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "刪 ADD → 一直輸出 0；刪 JMP → 只輸出 0",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WBchT47U",
			"originalText": "刪 ADD → 一直輸出 0；刪 JMP → 只輸出 0",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b31"
		},
		{
			"id": "RyHBXr7q",
			"type": "rectangle",
			"x": -1269.5,
			"y": -289.4,
			"width": 449,
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
				"KLiZqKKj"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1181756476,
			"version": 2,
			"versionNonce": 1533732376,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cAkcy4Xw"
				},
				{
					"type": "arrow",
					"id": "tFueWyCd"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b32"
		},
		{
			"id": "cAkcy4Xw",
			"type": "text",
			"x": -1255.5,
			"y": -280.4,
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
			"groupIds": [
				"KLiZqKKj"
			],
			"frameId": null,
			"roundness": null,
			"seed": 502740091,
			"version": 2,
			"versionNonce": 296757096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "CPU → cache（小、近）→ RAM（大）；SSD 存\n檔案",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RyHBXr7q",
			"originalText": "CPU → cache（小、近）→ RAM（大）；SSD 存\n檔案",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b33"
		},
		{
			"id": "2wxGFmWH",
			"type": "rectangle",
			"x": -1154.5,
			"y": -212.4,
			"width": 334,
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
			"seed": 1465451475,
			"version": 2,
			"versionNonce": 1045848856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qdHwiLSx"
				},
				{
					"type": "arrow",
					"id": "99GXjpyK"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b34"
		},
		{
			"id": "qdHwiLSx",
			"type": "text",
			"x": -1140.5,
			"y": -203.4,
			"width": 306,
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
			"seed": 888710315,
			"version": 2,
			"versionNonce": 1124530792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "hit：資料已在這層；miss：往下層找",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2wxGFmWH",
			"originalText": "hit：資料已在這層；miss：往下層找",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b35"
		},
		{
			"id": "syxJDVP8",
			"type": "rectangle",
			"x": -1184.5,
			"y": -139.1,
			"width": 364,
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
				"pqrEVygy"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2109502834,
			"version": 2,
			"versionNonce": 281690136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Degqq5nc"
				},
				{
					"type": "arrow",
					"id": "JzGbYmnd"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b36"
		},
		{
			"id": "Degqq5nc",
			"type": "text",
			"x": -1170.5,
			"y": -130.1,
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
			"groupIds": [
				"pqrEVygy"
			],
			"frameId": null,
			"roundness": null,
			"seed": 509496719,
			"version": 2,
			"versionNonce": 1745579368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Temporal locality：100 → 100 → 100",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "syxJDVP8",
			"originalText": "Temporal locality：100 → 100 → 100",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b37"
		},
		{
			"id": "9wGij4jb",
			"type": "rectangle",
			"x": -1165.5,
			"y": -84.6,
			"width": 345,
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
			"seed": 1162244647,
			"version": 2,
			"versionNonce": 45776152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "jJWHzxCR"
				},
				{
					"type": "arrow",
					"id": "jtdUjsFb"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b38"
		},
		{
			"id": "jJWHzxCR",
			"type": "text",
			"x": -1151.5,
			"y": -75.6,
			"width": 317,
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
			"seed": 48927358,
			"version": 2,
			"versionNonce": 2047443048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Spatial locality：100 → 104 → 108",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9wGij4jb",
			"originalText": "Spatial locality：100 → 104 → 108",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b39"
		},
		{
			"id": "kZYe29CY",
			"type": "rectangle",
			"x": -1267.5,
			"y": -30.1,
			"width": 447,
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
			"seed": 1229046607,
			"version": 2,
			"versionNonce": 630921752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "d8bYYEwG"
				},
				{
					"type": "arrow",
					"id": "6cTkMJs8"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3A"
		},
		{
			"id": "d8bYYEwG",
			"type": "text",
			"x": -1253.5,
			"y": -21.1,
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
			"seed": 260168531,
			"version": 2,
			"versionNonce": 1758278504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "讀 0、1、2、0（一列 0–3）→ Miss、Hit、Hit、\nHit",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kZYe29CY",
			"originalText": "讀 0、1、2、0（一列 0–3）→ Miss、Hit、Hit、\nHit",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3B"
		},
		{
			"id": "BEwS39LY",
			"type": "rectangle",
			"x": -1217.5,
			"y": 46.9,
			"width": 397,
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
			"seed": 1091836307,
			"version": 2,
			"versionNonce": 1012930328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Lpj7mT2g"
				},
				{
					"type": "arrow",
					"id": "mc685ezf"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3C"
		},
		{
			"id": "Lpj7mT2g",
			"type": "text",
			"x": -1203.5,
			"y": 55.9,
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
			"seed": 1035871332,
			"version": 2,
			"versionNonce": 1252165224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不要用小 Python 迴圈計時證明 cache 效果",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BEwS39LY",
			"originalText": "不要用小 Python 迴圈計時證明 cache 效果",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3D"
		},
		{
			"id": "VGmcEJ2R",
			"type": "rectangle",
			"x": -1129.5,
			"y": 120.2,
			"width": 309,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#5c940d",
			"backgroundColor": "#f4fce3",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"LRcw9SbV"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1396927105,
			"version": 2,
			"versionNonce": 192771096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tf6dxJvQ"
				},
				{
					"type": "arrow",
					"id": "7u5GeTN5"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3E"
		},
		{
			"id": "tf6dxJvQ",
			"type": "text",
			"x": -1115.5,
			"y": 129.2,
			"width": 281,
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
				"LRcw9SbV"
			],
			"frameId": null,
			"roundness": null,
			"seed": 942111208,
			"version": 2,
			"versionNonce": 206928232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "時脈較高不保證每個程式都比較快",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VGmcEJ2R",
			"originalText": "時脈較高不保證每個程式都比較快",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3F"
		},
		{
			"id": "Nbw3dEZp",
			"type": "rectangle",
			"x": -1142.5,
			"y": 174.7,
			"width": 322,
			"height": 40.5,
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
			"seed": 21551641,
			"version": 2,
			"versionNonce": 686240024,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rE8G2fuY"
				},
				{
					"type": "arrow",
					"id": "Nhcwp42h"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3G"
		},
		{
			"id": "rE8G2fuY",
			"type": "text",
			"x": -1128.5,
			"y": 183.7,
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
			"seed": 301522446,
			"version": 2,
			"versionNonce": 556928104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ L1 比 L2 小又快 → 見心智圖 6",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Nbw3dEZp",
			"originalText": "★ L1 比 L2 小又快 → 見心智圖 6",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3H"
		},
		{
			"id": "rEjyr3zP",
			"type": "rectangle",
			"x": -658.5,
			"y": 632.33,
			"width": 327,
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
			"seed": 621332565,
			"version": 2,
			"versionNonce": 1276202520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "db7mik9Z"
				},
				{
					"type": "arrow",
					"id": "x7x6ePRc"
				},
				{
					"type": "arrow",
					"id": "vEiCzcue"
				},
				{
					"type": "arrow",
					"id": "jqSzJehE"
				},
				{
					"type": "arrow",
					"id": "Eq7x43Tp"
				},
				{
					"type": "arrow",
					"id": "AETwYNtP"
				},
				{
					"type": "arrow",
					"id": "YgVCiDPk"
				},
				{
					"type": "arrow",
					"id": "NZQWvk5K"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3I"
		},
		{
			"id": "db7mik9Z",
			"type": "text",
			"x": -638.5,
			"y": 644.33,
			"width": 287,
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
			"seed": 2081186962,
			"version": 2,
			"versionNonce": 855916392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q6 驗證 loop 與 session",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rEjyr3zP",
			"originalText": "Q6 驗證 loop 與 session",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3J"
		},
		{
			"id": "pC7ekHFi",
			"type": "rectangle",
			"x": -956.5,
			"y": 385.35,
			"width": 222,
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
			"seed": 1560407080,
			"version": 2,
			"versionNonce": 502254360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mJrK6wqT"
				},
				{
					"type": "arrow",
					"id": "vEiCzcue"
				},
				{
					"type": "arrow",
					"id": "9rDiXB6x"
				},
				{
					"type": "arrow",
					"id": "YYPeM39d"
				},
				{
					"type": "arrow",
					"id": "yLvpwf74"
				},
				{
					"type": "arrow",
					"id": "ASQykZai"
				},
				{
					"type": "arrow",
					"id": "ngeXaLPi"
				},
				{
					"type": "arrow",
					"id": "wRp4dq5g"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3K"
		},
		{
			"id": "mJrK6wqT",
			"type": "text",
			"x": -942.5,
			"y": 394.35,
			"width": 194,
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
			"seed": 1073752793,
			"version": 2,
			"versionNonce": 1377309288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "有順序的 session 測試",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pC7ekHFi",
			"originalText": "有順序的 session 測試",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3L"
		},
		{
			"id": "v8epj8k5",
			"type": "rectangle",
			"x": -1374.5,
			"y": 259.2,
			"width": 358,
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
			"seed": 1513583761,
			"version": 2,
			"versionNonce": 150382616,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KhsH3pD5"
				},
				{
					"type": "arrow",
					"id": "9rDiXB6x"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3M"
		},
		{
			"id": "KhsH3pD5",
			"type": "text",
			"x": -1362.5,
			"y": 266.2,
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
			"seed": 1254949258,
			"version": 2,
			"versionNonce": 624526696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "一開始 DONE → 0 筆、不問數值、不算平均",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "v8epj8k5",
			"originalText": "一開始 DONE → 0 筆、不問數值、不算平均",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3N"
		},
		{
			"id": "FMbkXTVp",
			"type": "rectangle",
			"x": -1286.5,
			"y": 307.2,
			"width": 270,
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
			"seed": 1327574284,
			"version": 2,
			"versionNonce": 152691992,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eHQdRGc6"
				},
				{
					"type": "arrow",
					"id": "YYPeM39d"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3O"
		},
		{
			"id": "eHQdRGc6",
			"type": "text",
			"x": -1274.5,
			"y": 314.2,
			"width": 246,
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
			"seed": 1575022740,
			"version": 2,
			"versionNonce": 431265896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "一筆有效 → 報告一次、摘要一次",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FMbkXTVp",
			"originalText": "一筆有效 → 報告一次、摘要一次",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3P"
		},
		{
			"id": "Q4Zu7vFb",
			"type": "rectangle",
			"x": -1296.5,
			"y": 355.2,
			"width": 280,
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
			"seed": 438544810,
			"version": 2,
			"versionNonce": 2077065752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RheJm6tX"
				},
				{
					"type": "arrow",
					"id": "yLvpwf74"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3Q"
		},
		{
			"id": "RheJm6tX",
			"type": "text",
			"x": -1284.5,
			"y": 362.2,
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
			"seed": 1268006756,
			"version": 2,
			"versionNonce": 324356968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "有效 → 無效 → 有效 → 只加兩筆",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Q4Zu7vFb",
			"originalText": "有效 → 無效 → 有效 → 只加兩筆",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3R"
		},
		{
			"id": "A5asqyCs",
			"type": "rectangle",
			"x": -1360.5,
			"y": 422,
			"width": 344,
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
				"dyjX2AuE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 203470743,
			"version": 2,
			"versionNonce": 1879408408,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2wjqqkdF"
				},
				{
					"type": "arrow",
					"id": "ASQykZai"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3S"
		},
		{
			"id": "2wjqqkdF",
			"type": "text",
			"x": -1348.5,
			"y": 429,
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
			"groupIds": [
				"dyjX2AuE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 521729832,
			"version": 2,
			"versionNonce": 476552808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "有效 → 無效 → DONE → 保留第一筆總和",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "A5asqyCs",
			"originalText": "有效 → 無效 → DONE → 保留第一筆總和",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3T"
		},
		{
			"id": "ByJkqqpD",
			"type": "rectangle",
			"x": -1204.5,
			"y": 470,
			"width": 188,
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
			"seed": 1173869619,
			"version": 2,
			"versionNonce": 1983241240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fDVEvhX3"
				},
				{
					"type": "arrow",
					"id": "ngeXaLPi"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3U"
		},
		{
			"id": "fDVEvhX3",
			"type": "text",
			"x": -1192.5,
			"y": 477,
			"width": 164,
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
			"seed": 1178176974,
			"version": 2,
			"versionNonce": 364351848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "全部無效 → 不除以零",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ByJkqqpD",
			"originalText": "全部無效 → 不除以零",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3V"
		},
		{
			"id": "JXLkLwDg",
			"type": "rectangle",
			"x": -1256.5,
			"y": 518,
			"width": 240,
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
			"seed": 24748263,
			"version": 2,
			"versionNonce": 1884461336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MAgxEGi3"
				},
				{
					"type": "arrow",
					"id": "wRp4dq5g"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3W"
		},
		{
			"id": "MAgxEGi3",
			"type": "text",
			"x": -1244.5,
			"y": 525,
			"width": 216,
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
			"seed": 909888447,
			"version": 2,
			"versionNonce": 1720788072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "零距離、重複、30／60 邊界",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JXLkLwDg",
			"originalText": "零距離、重複、30／60 邊界",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3X"
		},
		{
			"id": "YvsfLM4X",
			"type": "rectangle",
			"x": -1191.5,
			"y": 566,
			"width": 457,
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
			"seed": 1958382332,
			"version": 2,
			"versionNonce": 1641002520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2xVhrjew"
				},
				{
					"type": "arrow",
					"id": "jqSzJehE"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3Y"
		},
		{
			"id": "2xVhrjew",
			"type": "text",
			"x": -1177.5,
			"y": 575,
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
			"seed": 946556341,
			"version": 2,
			"versionNonce": 750802792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "也要測不該發生的：多餘提示、被拒資料的報告、錯\n的總和",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YvsfLM4X",
			"originalText": "也要測不該發生的：多餘提示、被拒資料的報告、錯\n的總和",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3Z"
		},
		{
			"id": "4sTRd87p",
			"type": "rectangle",
			"x": -1181.5,
			"y": 661.8,
			"width": 447,
			"height": 63,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#f8f0fc",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"DsrVqSrf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 864413817,
			"version": 2,
			"versionNonce": 1067528984,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Eav44472"
				},
				{
					"type": "arrow",
					"id": "Eq7x43Tp"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3a"
		},
		{
			"id": "Eav44472",
			"type": "text",
			"x": -1167.5,
			"y": 670.8,
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
			"groupIds": [
				"DsrVqSrf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1891194811,
			"version": 2,
			"versionNonce": 1821452904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "故意錯誤：count 在拒絕前＋total 每輪清零 → 3\n3.5（應 2 16.0）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4sTRd87p",
			"originalText": "故意錯誤：count 在拒絕前＋total 每輪清零 → 3\n3.5（應 2 16.0）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3b"
		},
		{
			"id": "BFHLZBLF",
			"type": "rectangle",
			"x": -1192.5,
			"y": 738.8,
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
			"seed": 964723651,
			"version": 2,
			"versionNonce": 1077612568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8BDAyLWh"
				},
				{
					"type": "arrow",
					"id": "AETwYNtP"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3c"
		},
		{
			"id": "8BDAyLWh",
			"type": "text",
			"x": -1178.5,
			"y": 747.8,
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
			"seed": 967975651,
			"version": 2,
			"versionNonce": 1087348072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "三條路徑：STOP（break）／SKIP（continue）／\nACCEPT（報告＋更新一次）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BFHLZBLF",
			"originalText": "三條路徑：STOP（break）／SKIP（continue）／\nACCEPT（報告＋更新一次）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3d"
		},
		{
			"id": "kyP6eUrm",
			"type": "rectangle",
			"x": -1194.5,
			"y": 815.8,
			"width": 460,
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
			"seed": 1873707375,
			"version": 2,
			"versionNonce": 730942744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Lr6mX4yW"
				},
				{
					"type": "arrow",
					"id": "YgVCiDPk"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3e"
		},
		{
			"id": "Lr6mX4yW",
			"type": "text",
			"x": -1180.5,
			"y": 824.8,
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
			"seed": 614924838,
			"version": 2,
			"versionNonce": 180858984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "trip_log.py 五區：初始化 → 輸入與停止 → 驗證與\n略過 → 接受報告與更新 → 最後摘要",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kyP6eUrm",
			"originalText": "trip_log.py 五區：初始化 → 輸入與停止 → 驗證與\n略過 → 接受報告與更新 → 最後摘要",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3f"
		},
		{
			"id": "sYfRvGcS",
			"type": "rectangle",
			"x": -1149.5,
			"y": 892.8,
			"width": 415,
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
			"seed": 2064412812,
			"version": 2,
			"versionNonce": 722987544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xTpTxhDm"
				},
				{
					"type": "arrow",
					"id": "NZQWvk5K"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3g"
		},
		{
			"id": "xTpTxhDm",
			"type": "text",
			"x": -1135.5,
			"y": 901.8,
			"width": 387,
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
			"seed": 429079792,
			"version": 2,
			"versionNonce": 574972776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "AI 先做有界追蹤（≤ 6 輪），再提最小 patch",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sYfRvGcS",
			"originalText": "AI 先做有界追蹤（≤ 6 輪），再提最小 patch",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3h"
		},
		{
			"id": "vhCGxcEz",
			"type": "rectangle",
			"x": -423.5,
			"y": 1030.68,
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
			"seed": 1395798035,
			"version": 2,
			"versionNonce": 432203544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zLStCKGU"
				},
				{
					"type": "arrow",
					"id": "rm8FZF5F"
				},
				{
					"type": "arrow",
					"id": "eStyLE8E"
				},
				{
					"type": "arrow",
					"id": "ifmcSzdu"
				},
				{
					"type": "arrow",
					"id": "meEtfqhH"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3i"
		},
		{
			"id": "zLStCKGU",
			"type": "text",
			"x": -403.5,
			"y": 1042.68,
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
			"seed": 1210990157,
			"version": 2,
			"versionNonce": 93632104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "選讀",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vhCGxcEz",
			"originalText": "選讀",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3j"
		},
		{
			"id": "ry4JFtLK",
			"type": "rectangle",
			"x": -859.5,
			"y": 977.3,
			"width": 360,
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
			"seed": 648372504,
			"version": 2,
			"versionNonce": 1409696792,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BvL7pqZ4"
				},
				{
					"type": "arrow",
					"id": "eStyLE8E"
				},
				{
					"type": "arrow",
					"id": "UkUDPPRN"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3k"
		},
		{
			"id": "BvL7pqZ4",
			"type": "text",
			"x": -845.5,
			"y": 986.3,
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
			"seed": 834262781,
			"version": 2,
			"versionNonce": 159492456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "for-else：正常跑完（沒 break）才執行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ry4JFtLK",
			"originalText": "for-else：正常跑完（沒 break）才執行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3l"
		},
		{
			"id": "qvDYLRbA",
			"type": "rectangle",
			"x": -1287.5,
			"y": 980.55,
			"width": 368,
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
			"seed": 631513385,
			"version": 2,
			"versionNonce": 131465496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VSVNMEHN"
				},
				{
					"type": "arrow",
					"id": "UkUDPPRN"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3m"
		},
		{
			"id": "VSVNMEHN",
			"type": "text",
			"x": -1275.5,
			"y": 987.55,
			"width": 344,
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
			"seed": 859498332,
			"version": 2,
			"versionNonce": 156777576,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "target 7 → Not found；target 3 → Found",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qvDYLRbA",
			"originalText": "target 7 → Not found；target 3 → Found",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3n"
		},
		{
			"id": "yQ5HEVjd",
			"type": "rectangle",
			"x": -940.5,
			"y": 1031.8,
			"width": 441,
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
			"seed": 96335252,
			"version": 2,
			"versionNonce": 77995544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "t53k7qRH"
				},
				{
					"type": "arrow",
					"id": "ifmcSzdu"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3o"
		},
		{
			"id": "t53k7qRH",
			"type": "text",
			"x": -926.5,
			"y": 1040.8,
			"width": 413,
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
			"seed": 1699071845,
			"version": 2,
			"versionNonce": 384069480,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "try／except 解析恢復：是新承諾，不是原本能力",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yQ5HEVjd",
			"originalText": "try／except 解析恢復：是新承諾，不是原本能力",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3p"
		},
		{
			"id": "PzKgNiP8",
			"type": "rectangle",
			"x": -956.5,
			"y": 1086.3,
			"width": 457,
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
			"seed": 1667013162,
			"version": 2,
			"versionNonce": 191535896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bSPxBy8f"
				},
				{
					"type": "arrow",
					"id": "meEtfqhH"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3q"
		},
		{
			"id": "bSPxBy8f",
			"type": "text",
			"x": -942.5,
			"y": 1095.3,
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
			"seed": 645601954,
			"version": 2,
			"versionNonce": 712131176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "最長行程：第一筆建候選；更長才換；同時間保留第\n一筆；空 session 不印",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PzKgNiP8",
			"originalText": "最長行程：第一筆建候選；更長才換；同時間保留第\n一筆；空 session 不印",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3r"
		},
		{
			"id": "MRUrQCeN",
			"type": "rectangle",
			"x": 732.5,
			"y": -964.1,
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
				"TULgHqYt"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1175068366,
			"version": 2,
			"versionNonce": 513243160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zvJb4VRy"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3s"
		},
		{
			"id": "zvJb4VRy",
			"type": "text",
			"x": 739.5,
			"y": -961.1,
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
				"TULgHqYt"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1826902785,
			"version": 2,
			"versionNonce": 1389213032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q020",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MRUrQCeN",
			"originalText": "Q020",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3t"
		},
		{
			"id": "zspZxdYS",
			"type": "rectangle",
			"x": 1062.5,
			"y": -975.45,
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
				"HYC9Vivm"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1573561003,
			"version": 2,
			"versionNonce": 1377875224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HrnZVpNr"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3u"
		},
		{
			"id": "HrnZVpNr",
			"type": "text",
			"x": 1069.5,
			"y": -972.45,
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
				"HYC9Vivm"
			],
			"frameId": null,
			"roundness": null,
			"seed": 661503629,
			"version": 2,
			"versionNonce": 1698875496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T042",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zspZxdYS",
			"originalText": "T042",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3v"
		},
		{
			"id": "ZM5tDJyZ",
			"type": "rectangle",
			"x": 1057.5,
			"y": -494.15,
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
				"EDK6YFSj"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1374141266,
			"version": 2,
			"versionNonce": 461001240,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WJEnBaxx"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3w"
		},
		{
			"id": "WJEnBaxx",
			"type": "text",
			"x": 1064.5,
			"y": -491.15,
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
				"EDK6YFSj"
			],
			"frameId": null,
			"roundness": null,
			"seed": 22256166,
			"version": 2,
			"versionNonce": 765295464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T035",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZM5tDJyZ",
			"originalText": "T035",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3x"
		},
		{
			"id": "UXQgSQRF",
			"type": "rectangle",
			"x": 1093.5,
			"y": -427.35,
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
				"ykJVpj8g"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 110480965,
			"version": 2,
			"versionNonce": 563629848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RprXKkK5"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b3y"
		},
		{
			"id": "RprXKkK5",
			"type": "text",
			"x": 1100.5,
			"y": -424.35,
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
				"ykJVpj8g"
			],
			"frameId": null,
			"roundness": null,
			"seed": 720167306,
			"version": 2,
			"versionNonce": 506056296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T073",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UXQgSQRF",
			"originalText": "T073",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b3z"
		},
		{
			"id": "JawjXrHp",
			"type": "rectangle",
			"x": 1303.5,
			"y": -264.55,
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
				"tpqK9ULK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1807782636,
			"version": 2,
			"versionNonce": 216968216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RUwZXTQY"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b40"
		},
		{
			"id": "RUwZXTQY",
			"type": "text",
			"x": 1310.5,
			"y": -261.55,
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
				"tpqK9ULK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 88971366,
			"version": 2,
			"versionNonce": 2142486888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T036",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JawjXrHp",
			"originalText": "T036",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b41"
		},
		{
			"id": "Y5ai9dKS",
			"type": "rectangle",
			"x": 1038.5,
			"y": -177.75,
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
				"L6RVy2dX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1697517276,
			"version": 2,
			"versionNonce": 1467050264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zXgR8NtQ"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b42"
		},
		{
			"id": "zXgR8NtQ",
			"type": "text",
			"x": 1045.5,
			"y": -174.75,
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
				"L6RVy2dX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1615868417,
			"version": 2,
			"versionNonce": 562517096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T074",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Y5ai9dKS",
			"originalText": "T074",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b43"
		},
		{
			"id": "LUe8mYH6",
			"type": "rectangle",
			"x": 1053.5,
			"y": -104.45,
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
				"Se8hmwsC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1041431563,
			"version": 2,
			"versionNonce": 479495704,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vUGGnENH"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b44"
		},
		{
			"id": "vUGGnENH",
			"type": "text",
			"x": 1060.5,
			"y": -101.45,
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
				"Se8hmwsC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1856193228,
			"version": 2,
			"versionNonce": 158369640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T044",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LUe8mYH6",
			"originalText": "T044",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b45"
		},
		{
			"id": "mKqzkupP",
			"type": "rectangle",
			"x": 1032.5,
			"y": 75.85,
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
				"qRh5gRV3"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1245121700,
			"version": 2,
			"versionNonce": 1766589208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "GqD5F8CL"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b46"
		},
		{
			"id": "GqD5F8CL",
			"type": "text",
			"x": 1039.5,
			"y": 78.85,
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
				"qRh5gRV3"
			],
			"frameId": null,
			"roundness": null,
			"seed": 511725987,
			"version": 2,
			"versionNonce": 599480936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q016",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mKqzkupP",
			"originalText": "Q016",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b47"
		},
		{
			"id": "8QXqPSXW",
			"type": "rectangle",
			"x": 1094.5,
			"y": 258.15,
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
				"5nVHQqQX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1508013274,
			"version": 2,
			"versionNonce": 202104856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mH7vznJM"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b48"
		},
		{
			"id": "mH7vznJM",
			"type": "text",
			"x": 1101.5,
			"y": 261.15,
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
				"5nVHQqQX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 871848466,
			"version": 2,
			"versionNonce": 1932774760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T043",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8QXqPSXW",
			"originalText": "T043",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b49"
		},
		{
			"id": "RZHSNa4W",
			"type": "rectangle",
			"x": 949.5,
			"y": 353.95,
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
				"wU2v8u8W"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1011072578,
			"version": 2,
			"versionNonce": 1690836248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fbw4CMTK"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4A"
		},
		{
			"id": "fbw4CMTK",
			"type": "text",
			"x": 956.5,
			"y": 356.95,
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
				"wU2v8u8W"
			],
			"frameId": null,
			"roundness": null,
			"seed": 338788689,
			"version": 2,
			"versionNonce": 1093001320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T037 Q017",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RZHSNa4W",
			"originalText": "T037 Q017",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4B"
		},
		{
			"id": "Z885saBa",
			"type": "rectangle",
			"x": 775.5,
			"y": 507.7,
			"width": 131,
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
				"FiVUm5EP"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 787264602,
			"version": 2,
			"versionNonce": 888453656,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hLBF34Wp"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4C"
		},
		{
			"id": "hLBF34Wp",
			"type": "text",
			"x": 782.5,
			"y": 510.7,
			"width": 117,
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
				"FiVUm5EP"
			],
			"frameId": null,
			"roundness": null,
			"seed": 616247158,
			"version": 2,
			"versionNonce": 1297978216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T045 T077 Q029",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Z885saBa",
			"originalText": "T045 T077 Q029",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4D"
		},
		{
			"id": "mn9M9NKc",
			"type": "rectangle",
			"x": 932.5,
			"y": 732.75,
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
				"QwsPraaF"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1736989622,
			"version": 2,
			"versionNonce": 1871034136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tukjRrAZ"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4E"
		},
		{
			"id": "tukjRrAZ",
			"type": "text",
			"x": 939.5,
			"y": 735.75,
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
				"QwsPraaF"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1789819416,
			"version": 2,
			"versionNonce": 2116478568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T038",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mn9M9NKc",
			"originalText": "T038",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4F"
		},
		{
			"id": "CuETeNXm",
			"type": "rectangle",
			"x": 1038.5,
			"y": 806.05,
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
				"aPaS73JZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 796715190,
			"version": 2,
			"versionNonce": 149885976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kG58tZKx"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4G"
		},
		{
			"id": "kG58tZKx",
			"type": "text",
			"x": 1045.5,
			"y": 809.05,
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
				"aPaS73JZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1140642603,
			"version": 2,
			"versionNonce": 273537384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q019",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CuETeNXm",
			"originalText": "Q019",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4H"
		},
		{
			"id": "xcra94kY",
			"type": "rectangle",
			"x": 1444.5,
			"y": 906.95,
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
				"uSZGD7Pf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1085693039,
			"version": 2,
			"versionNonce": 1193595160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rNudwRgE"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4I"
		},
		{
			"id": "rNudwRgE",
			"type": "text",
			"x": 1451.5,
			"y": 909.95,
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
				"uSZGD7Pf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1743976105,
			"version": 2,
			"versionNonce": 1193176168,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T041",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xcra94kY",
			"originalText": "T041",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4J"
		},
		{
			"id": "NMLNvPbr",
			"type": "rectangle",
			"x": 1051.5,
			"y": 1225.35,
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
				"rtyhFewX"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1068518258,
			"version": 2,
			"versionNonce": 295366168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iWASBq2e"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4K"
		},
		{
			"id": "iWASBq2e",
			"type": "text",
			"x": 1058.5,
			"y": 1228.35,
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
				"rtyhFewX"
			],
			"frameId": null,
			"roundness": null,
			"seed": 305796581,
			"version": 2,
			"versionNonce": 476356456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T092",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NMLNvPbr",
			"originalText": "T092",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4L"
		},
		{
			"id": "P2yVEbeW",
			"type": "rectangle",
			"x": 1050.5,
			"y": 1321.15,
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
				"JD7FG5CE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1241652857,
			"version": 2,
			"versionNonce": 1095068440,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SdYQsTqw"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4M"
		},
		{
			"id": "SdYQsTqw",
			"type": "text",
			"x": 1057.5,
			"y": 1324.15,
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
				"JD7FG5CE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 555803127,
			"version": 2,
			"versionNonce": 1886155368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q040",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "P2yVEbeW",
			"originalText": "Q040",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4N"
		},
		{
			"id": "uiZvmbzk",
			"type": "rectangle",
			"x": -734.5,
			"y": -1149.3,
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
				"38ahX8XE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1976850554,
			"version": 2,
			"versionNonce": 1889028120,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Pgj47F4W"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4O"
		},
		{
			"id": "Pgj47F4W",
			"type": "text",
			"x": -727.5,
			"y": -1146.3,
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
				"38ahX8XE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 381306037,
			"version": 2,
			"versionNonce": 973202792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q018",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uiZvmbzk",
			"originalText": "Q018",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4P"
		},
		{
			"id": "ZH2jFirB",
			"type": "rectangle",
			"x": -734.5,
			"y": -1076,
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
				"xjuWtfn5"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 240432083,
			"version": 2,
			"versionNonce": 1267172632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xdbifTRz"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4Q"
		},
		{
			"id": "xdbifTRz",
			"type": "text",
			"x": -727.5,
			"y": -1073,
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
				"xjuWtfn5"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1429008764,
			"version": 2,
			"versionNonce": 913373288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T039",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZH2jFirB",
			"originalText": "T039",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4R"
		},
		{
			"id": "XEXwgNMQ",
			"type": "rectangle",
			"x": -734.5,
			"y": -1002.7,
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
				"y9W7cRah"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 81277470,
			"version": 2,
			"versionNonce": 1602691608,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "QVmD5wXN"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4S"
		},
		{
			"id": "QVmD5wXN",
			"type": "text",
			"x": -727.5,
			"y": -999.7,
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
				"y9W7cRah"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1441405370,
			"version": 2,
			"versionNonce": 428190568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T076",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XEXwgNMQ",
			"originalText": "T076",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4T"
		},
		{
			"id": "Y3fzVcLr",
			"type": "rectangle",
			"x": -734.5,
			"y": -874.9,
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
				"HcDsSd4z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 516642125,
			"version": 2,
			"versionNonce": 1804279576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HMTdKk3K"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4U"
		},
		{
			"id": "HMTdKk3K",
			"type": "text",
			"x": -727.5,
			"y": -871.9,
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
				"HcDsSd4z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1881146212,
			"version": 2,
			"versionNonce": 1032584808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T078",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Y3fzVcLr",
			"originalText": "T078",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4V"
		},
		{
			"id": "fVq7cGVh",
			"type": "rectangle",
			"x": -775.5,
			"y": -801.6,
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
				"AHis2Vyd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1903863413,
			"version": 2,
			"versionNonce": 805796888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KaJWfRN8"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4W"
		},
		{
			"id": "KaJWfRN8",
			"type": "text",
			"x": -768.5,
			"y": -798.6,
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
				"AHis2Vyd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 553182797,
			"version": 2,
			"versionNonce": 1397748072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T075 Q030",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fVq7cGVh",
			"originalText": "T075 Q030",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4X"
		},
		{
			"id": "WRyArDZu",
			"type": "rectangle",
			"x": -899.5,
			"y": -680.3,
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
				"uz7GiNwd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1108383763,
			"version": 2,
			"versionNonce": 1055930648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ZYd4W6j6"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4Y"
		},
		{
			"id": "ZYd4W6j6",
			"type": "text",
			"x": -892.5,
			"y": -677.3,
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
				"uz7GiNwd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1355787391,
			"version": 2,
			"versionNonce": 303924328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T046",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WRyArDZu",
			"originalText": "T046",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4Z"
		},
		{
			"id": "Md3aGiQi",
			"type": "rectangle",
			"x": -775.5,
			"y": -565.5,
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
				"R25NbwU8"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 808393244,
			"version": 2,
			"versionNonce": 1270437400,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yP6LX8DZ"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4a"
		},
		{
			"id": "yP6LX8DZ",
			"type": "text",
			"x": -768.5,
			"y": -562.5,
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
				"R25NbwU8"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1855113396,
			"version": 2,
			"versionNonce": 1740683112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T097 Q026",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Md3aGiQi",
			"originalText": "T097 Q026",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4b"
		},
		{
			"id": "3Be8s42N",
			"type": "rectangle",
			"x": -1223.5,
			"y": -552.85,
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
				"XrURdY84"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1341970416,
			"version": 2,
			"versionNonce": 2069287704,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DQxm6MiP"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4c"
		},
		{
			"id": "DQxm6MiP",
			"type": "text",
			"x": -1216.5,
			"y": -549.85,
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
				"XrURdY84"
			],
			"frameId": null,
			"roundness": null,
			"seed": 832246456,
			"version": 2,
			"versionNonce": 679840360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T040",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3Be8s42N",
			"originalText": "T040",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4d"
		},
		{
			"id": "qEeC8AEn",
			"type": "rectangle",
			"x": -863.5,
			"y": -308.2,
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
				"KLiZqKKj"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1536687269,
			"version": 2,
			"versionNonce": 876392472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FDPMS2et"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4e"
		},
		{
			"id": "FDPMS2et",
			"type": "text",
			"x": -856.5,
			"y": -305.2,
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
				"KLiZqKKj"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2014016266,
			"version": 2,
			"versionNonce": 1060633960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T011",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qEeC8AEn",
			"originalText": "T011",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4f"
		},
		{
			"id": "kbxMUF46",
			"type": "rectangle",
			"x": -863.5,
			"y": -157.9,
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
				"pqrEVygy"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1114110933,
			"version": 2,
			"versionNonce": 1851714840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rfrV8XdS"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4g"
		},
		{
			"id": "rfrV8XdS",
			"type": "text",
			"x": -856.5,
			"y": -154.9,
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
				"pqrEVygy"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1914160648,
			"version": 2,
			"versionNonce": 1562644584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T061",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kbxMUF46",
			"originalText": "T061",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4h"
		},
		{
			"id": "b8vq5rSV",
			"type": "rectangle",
			"x": -863.5,
			"y": 101.4,
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
				"LRcw9SbV"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2047412573,
			"version": 2,
			"versionNonce": 53578264,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CmJknciv"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4i"
		},
		{
			"id": "CmJknciv",
			"type": "text",
			"x": -856.5,
			"y": 104.4,
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
				"LRcw9SbV"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1014123687,
			"version": 2,
			"versionNonce": 706069352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T012",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "b8vq5rSV",
			"originalText": "T012",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4j"
		},
		{
			"id": "mu66X6mA",
			"type": "rectangle",
			"x": -1059.5,
			"y": 403.2,
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
				"dyjX2AuE"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 637789945,
			"version": 2,
			"versionNonce": 2108196632,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "b7jvwzFR"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4k"
		},
		{
			"id": "b7jvwzFR",
			"type": "text",
			"x": -1052.5,
			"y": 406.2,
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
				"dyjX2AuE"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1578806197,
			"version": 2,
			"versionNonce": 1951995496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T079",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mu66X6mA",
			"originalText": "T079",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4l"
		},
		{
			"id": "FGev2V5g",
			"type": "rectangle",
			"x": -777.5,
			"y": 643,
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
				"DsrVqSrf"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 29520856,
			"version": 2,
			"versionNonce": 1782047768,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2Qd2L3Jf"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4m"
		},
		{
			"id": "2Qd2L3Jf",
			"type": "text",
			"x": -770.5,
			"y": 646,
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
				"DsrVqSrf"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1700985667,
			"version": 2,
			"versionNonce": 1622804840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T098",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FGev2V5g",
			"originalText": "T098",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4n"
		},
		{
			"id": "W7JUbZZS",
			"type": "text",
			"x": -1691.5,
			"y": -1736.95,
			"width": 1093,
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
			"seed": 1394854381,
			"version": 2,
			"versionNonce": 651403544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 4｜Deck 4：程式如何重複工作（W7）",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 4｜Deck 4：程式如何重複工作（W7）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4o"
		},
		{
			"id": "FKAzBNwk",
			"type": "text",
			"x": -1691.5,
			"y": -1674.95,
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
			"seed": 102066558,
			"version": 2,
			"versionNonce": 444898408,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Deck 4 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Deck 4 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4p"
		},
		{
			"id": "6mcK6FJL",
			"type": "rectangle",
			"x": -1691.5,
			"y": -1607.95,
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
			"seed": 1510362557,
			"version": 2,
			"versionNonce": 854572568,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8ckZMadk"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4q"
		},
		{
			"id": "8ckZMadk",
			"type": "text",
			"x": -1677.5,
			"y": -1598.95,
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
			"seed": 261881500,
			"version": 2,
			"versionNonce": 59035496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★ 考古題考過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6mcK6FJL",
			"originalText": "★ 考古題考過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4r"
		},
		{
			"id": "PV4uiRtR",
			"type": "rectangle",
			"x": -1530.5,
			"y": -1607.95,
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
			"seed": 1622416447,
			"version": 2,
			"versionNonce": 2139110168,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pKacABmA"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4s"
		},
		{
			"id": "pKacABmA",
			"type": "text",
			"x": -1516.5,
			"y": -1598.95,
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
			"seed": 494931057,
			"version": 2,
			"versionNonce": 1678156392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PV4uiRtR",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4t"
		},
		{
			"id": "RHzXyYe2",
			"type": "rectangle",
			"x": -1386.5,
			"y": -1607.95,
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
			"seed": 1996340610,
			"version": 2,
			"versionNonce": 1056512024,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "vNJKyrNE"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4u"
		},
		{
			"id": "vNJKyrNE",
			"type": "text",
			"x": -1372.5,
			"y": -1598.95,
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
			"seed": 857978882,
			"version": 2,
			"versionNonce": 450237800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例題考到、原本心智圖沒有的觀念",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RHzXyYe2",
			"originalText": "例題考到、原本心智圖沒有的觀念",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4v"
		},
		{
			"id": "iNqmtShx",
			"type": "rectangle",
			"x": -1084.5,
			"y": -1600.35,
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
			"seed": 2017637217,
			"version": 2,
			"versionNonce": 894326040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pm9riYcT"
				}
			],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"index": "b4w"
		},
		{
			"id": "pm9riYcT",
			"type": "text",
			"x": -1077.5,
			"y": -1597.35,
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
			"seed": 137538115,
			"version": 2,
			"versionNonce": 1295984744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001 Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iNqmtShx",
			"originalText": "T001 Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b4x"
		},
		{
			"id": "L6B9j5vy",
			"type": "text",
			"x": -986.5,
			"y": -1598.95,
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
			"seed": 2080868689,
			"version": 2,
			"versionNonce": 133427736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858144564,
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
			"index": "b4y"
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