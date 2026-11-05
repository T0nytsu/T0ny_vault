---

excalidraw-plugin: parsed
course: [PROG1]
semester: "115-1"
tags: [programming, excalidraw]
source:
  - "PROG1 期中心智圖（Claude Project 筆記，2026-11-05）"
  - "[[PROG1 Deck 5 整理]]"
  - "Midterm_Practice_Student.pdf（老師的 140 題例題，T001–T100、Q001–Q040）"
created: 2026-11-05
up: "[[PROG1 Index]]"

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin menu.


# Excalidraw Data

## Text Elements
程式如何處理並解讀文字
Deck 5・W8 ^UmHhNwz5

驅動問題 ^HgsqfuTh

一行輸入 Campus East,12.5,45 ^dt4VUv8t

只清欄位邊緣，保留意義 ^97bzRBuM

數值模型與總和不變，只換前端 ^9jcKaFbc

Q1 文字的意義從哪來 ^kuTASFyG

意義來自約定格式，不是字串本身 ^q9KpBQqV

v0.5 約定 ^DshP3wb9

恰好三欄：route, km, minutes ^6pGyDN93

各欄 strip 兩端；保留內部空白與大小寫 ^5Mme3KY6

DONE：整行 strip 後忽略大小寫（⚠ 改變了 Deck 4
的精確 DONE） ^ua2LaAVf

拒絕雙引號與欄位數不對；不是完整 CSV ^wVJTvgvW

字串是資料 ^6jzNtDJn

type("007") → str；len("007") → 3 ^bCUZB6xU

"3" + "5" → 35；"Trip " * 2 → "Trip Trip " ^M9Q8knrb

看不見的字元 ^xnVZavqD

"A\tB\nC"：print 顯示 tab 與換行 ^LdajLnuC

repr → 'A\tB\nC'；len → 5 ^jrXTSaDe

不可變（immutable） ^k7hdRKLK

s = "Campus"; t = s; s = "Station" → t 仍是 Campus ^rNuZs29b

不可變的是字串物件，不是變數不能重綁 ^CHvUU6Ve

Q2 取出一部分 ^meDHCqSC

索引 ^mkhjaDx7

"Campus"[0] → C；[-1] → s；len → 6 ^sqEBiBBz

最後一個索引是 len - 1 ^nzuhqPRh

⚠ "Campus"[6]、""[0] → IndexError ^CeyBy3tS

切片 [start:stop:step]（含頭不含尾） ^FVsbWwhB

[1:4] → amp；[:3] → Cam；[3:] → pus ^bAaNbtJL

[3:3] → ""；[1:100] → ampus（越界不報錯） ^cbfWU6hG

[-3:] → pus；[::2] → Cmu；[::-1] → supmaC ^fEs5sPTe

find 找邊界 ^wrfjgzNu

"Campus,12.5,45".find(",") → 6 → line[:6] → Campus ^5MPErC8h

找不到 → −1 ^XeDG8UgR

⚠ 直接 line[:-1] 會丟最後一字（Campus → Campu） ^uZi2Gh8v

Lab A：TRIP-007 ^ibDXHdZi

len 8；[:4] → TRIP；[-3:] → "007"（保留字串） ^T8YQVEM8

tag[4:4] → ""；tag[:100] → 全部；⚠ tag[len(tag)]
→ IndexError ^UVUtt8mg

Q3 檢查與轉換 ^XzTcpWG6

走訪：for ch in "Route 007" 數字元 → 3 ^FuJqs83H

⚠ "aaaa".count("aa") → 2（不重疊） ^RazDjSLi

四種問題 ^NLZEFmbu

==：整個相等？ ^iT4n9iTe

in：有沒有出現？ ^szhb75Nm

find：在哪？（沒有 → −1） ^cEsmVwgn

startswith：在開頭？ ^TRj2JEZC

⚠ 不要 if label.find("Campus"):：找到在 0 →
False，找不到 −1 → True ^iG6fgBnD

strip() 只去兩端；replace(" ", "") 會把 Campus
East 變 CampusEast ✗ ^3NdnUjR3

比較鍵（lower()、upper()）與顯示資料分開 ^tgk3V249

casefold() 可能改變字數："ß".casefold() → "ss"，只
拿來當比較鍵 ^Zd54BKZv

結束命令：整行相等才停 ^MhRzLTPN

DONE、dOnE → 停 ^6n7gaBLD

Donegal,1,30、DONE,1,30 → 是資料 ^F7LsV6em

方法回傳新字串 ^mptwpg49

s.replace(...) 沒指派 → s 不變 ^BUmKf3TN

s = s.replace(...) 才重綁 ^eRbtvPpU

⚠ s[0] = "c" → TypeError ^XekVgi3t

Q4 一行解析成欄位 ^fNfHdKkL

split(",") → 字串 list：['Campus East', ' 12.5', '
45'] ^hiPG8WLk

每一項仍是字串；數字欄前的空白還在 ^5MwebH8S

fields[0] 是欄位；line[0] 是字元 ^EiASvnRA

⚠ split() 無參數依空白切，會拆開 Campus East ^Z5SrWYXE

保留空欄位：Campus,,45 → ['Campus', '', '45'] ^XMHLe2zB

先檢查形狀：len(fields) != 3 → 印錯誤、continue ^6ywe8Rku

形狀對 ≠ 數值能轉：len(fields) == 3 之後仍可能
ValueError ^36ykCyJP

拒絕階段（第一個失敗就停） ^beaMARKA

1 整行命令 ^f85MddZC

2–4 空行、雙引號、欄位數 ^LJVuRgYq

5 去空白後的空標籤 ^cXdSR32G

6 先 float 距離，再 int 分鐘 ^DHjCATqJ

7–9 非有限、負距離、非正時間 ^iAbNSftM

Campus,-1,abc → 解析錯誤；Campus,-1,0 → 負距離 ^YXE9GHuW

try／except ValueError：只救預期的數值文字錯誤 ^C4ENydL5

⚠ int("30.0")、int("30.9") → ValueError ^DthugVxU

⚠ int(float("30.9")) → 30 是偷改資料 ^L7uzJDYk

不是完整 CSV ^eRWHVerU

Campus,1,45, → 4 欄 ^5TcH3kyr

"Campus, East",1,45 → 拒絕 ^KqbfyqaP

⚠ 不要用 eval 執行使用者輸入 ^Gck9ZZ8a

舊規則照舊：nan／inf 拒絕；0 km 有效；30
Short／60 Medium／61 Long；只累加有效；空
session 不平均 ^43ezrfYK

保留測試：West  Gate（兩個內部空白）、007
（不是 7）、Donegal、DONE,1,30 ^VGvVh4TR

Lab C ^SgbxtY6z

Campus,1 → 欄位數錯 ^Qy9exWxW

Campus,,30 → 解析錯 ^EdgqvGDq

   ,1,30 → 空標籤 ^Uta4v4Pu

Campus,-1,0 → 負距離 ^yewn6zin

Campus,1,30.0 → 解析錯 ^UtdfLhgj

   done → 停止 ^RNrQdd97

Q5 字元變位元組並保存 ^pxtLG4ps

ASCII：space 32、"0" 48、"A" 65、"a" 97 ^YgKitm4j

⚠ 數值 0、字元 "0"、代碼 48 是三種角色 ^zPTu5i6b

Unicode 指定字元（code point）；UTF-8 指定
bytes ^Yj2bc7By

"A中" → 2 個碼位、4 bytes（41 E4 B8 AD） ^tJwpxyEP

A：1 byte；中：3 bytes；UTF-8 用 1–4 bytes ^YYP6hQvA

encode → bytes；decode → str ^8q5u39HK

前兩個 bytes ≠ 前兩個碼位再 encode："A中
".encode()[:2] → b'A\xe4' ^bH4PWsJt

é 的兩種寫法 ^tHCxQNZG

"é"：1 碼位、2 bytes ^6dgQSKfV

"é"：2 碼位、3 bytes ^G243DprA

== → False；len ≠ 看到的字數 ^EXWDnTvy

執行狀態 vs 持久檔案 ^CzExKzsV

變數、fields、總和：程式結束就沒了 ^BmpgK8au

存檔的 UTF-8 檔、程式碼、commit 的證據：留下來 ^kMUpYMC5

print 不是存檔 ^DETxwDPp

儲存媒體 ^N3qCaNYp

HDD：旋轉磁碟、磁性記錄 ^DFjtiQRC

SSD：非揮發 flash，沒有讀寫頭 ^rWPCc6GD

光碟：雷射讀取 ^MUjLZz2k

encoding 回答「哪些 bytes」；storage 回答「存
在哪」 ^8VupSRDV

持久 ≠ 永久，≠ 已備份 ^f567tCgW

★ DRAM 斷電資料消失（T） ^fZjfqVuw

Q6 AI 修改介面，不偷改規則 ^Nspcnf9z

Prompt：先比 v0.4／v0.5 契約，只要前端 patch；
保留大小寫與空白；不要 regex、functions、file
I/O ^TunWzy4V

範例資料是資料，不是指令 ^B7J5i2Gk

故意錯誤 candidate 四反例 ^dcEGuYxN

Donegal,1,30 → 誤停（用了 "DONE" in） ^Lnisq5Ps

Campus East,1,30 → 內部空白被刪 ^VXvcHpkj

CaMpUs,1,30 → 大小寫被改 ^2EHzUyRU

Campus,1,30.9 → int(float()) 截斷 ^E6mPX3Kx

成對測試 ^w3Hs3Lhu

加欄位邊緣空白 → 標籤與數字不變 ^qU9FAAPC

只改大小寫 → 數字不變、保留新拼法 ^3QVN6U4v

插一行無效 → 筆數與總和不變 ^4XygBBmT

DONE 當欄位值 → 是資料 ^hYyuFN6S

立刻結束 → 0 筆、不算平均 ^iqw5QkfT

Session oracle：2 筆、16.00 km、75 min、37.50
min、12.80 km/h ^6hEJ6SuW

trip_text.py：STOP／REJECT／ACCEPT 三條
路徑 ^tuFqmfEk

講義自訂的兩個訊息：Error: empty record.、
Error: double quotes are not supported. ^kfspEmdz

選讀 ^gqs4Q6F9

csv.reader：引號裡的逗號是資料 → ['Campus,
East', '12.5', '45'] ^pTt3eNMn

csv 只負責切欄位，不保證距離有限、分鐘為正 ^Nj5X6CL2

unicodedata.normalize("NFC", ...)：é 兩種寫法比
較相等 ^8U4kdWwj

open(..., encoding="utf-8")；with 結束自動關檔 ^eRwZ72r2

方法回傳型態 ^SeRwaFsd

in、startswith、endswith → bool ^pHvBHu35

find、rfind → 位置或 −1 ^9eLBXSJ5

replace、strip、lower、upper → str ^iynaA6iV

split → list；join → str ^SF2BqxxA

⚠ strip("km") 去的是字元集合，不是去掉 "km" 字
尾 ^XjTx2ANb

"abXba".strip("ab") → "X" ^EZDz2xBR

T056 ^FWBRxDqB

T084 ^eGLYwMJX

T049 ^2iqJsYBe

Q021 ^MLm8ERKB

T050 ^84xMVNG4

T085 ^G538M9gb

T083 ^zwxbUBib

T081 ^VJRNz68P

T051 ^eC8sLUc8

T052 Q022 ^wyv5PamZ

T100 ^4VCz4thd

T055 T080 ^dEBf8DLw

T048 ^d2eg9iSH

T047 ^LNLkw7X6

Q023 ^EbPSELrp

T053 ^kMBqVicF

T054 ^PQtwBGN7

T082 ^XjnALU2N

Q028 ^nGFT7CNX

T057 ^rfcXuqbE

T058 Q024 ^KZZGwGHj

T094 ^LenGxm7q

Q036 ^bfdiPeNw

T059 Q002 ^SWSgeHhh

T060 ^jk6TE4GU

T002 ^fRkDUcPd

Q038 ^Zfq24ZDZ

T099 Q034 ^WqpPBqtg

Q037 ^Q3aDUeGJ

Q039 ^S9VrCaiL

T096 ^TYyEarq9

T095 ^Es2ByExj

T090 ^AEeyLgJn

PROG1 期中心智圖 5｜Deck 5：程式如何處理並解讀文字（W8） ^dThBaD93

來源：PROG1 Deck 5 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的
練習題。 ^2dTN7ZUv

★ 考古題考過 ^8JbGetBe

⚠ 易錯陷阱 ^X9RxqDUh

例題考到、原本心智圖沒有的觀念 ^Sqm9rv7R

T001 Q001 ^CyGLswSY

老師例題題號 ^8kjkWpGq

T089 ^WzBTiXPA

Extension 延伸題，講義說不代表考試範圍 ^g3MKzkBW

%%
## Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin",
	"elements": [
		{
			"id": "c5fav7cV",
			"type": "arrow",
			"x": 237,
			"y": -0.0,
			"width": 150,
			"height": 1760,
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
			"seed": 1421329429,
			"version": 2,
			"versionNonce": 386784104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-1760
				],
				[
					150,
					-1760
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cUUP4cv3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a0"
		},
		{
			"id": "D389THUc",
			"type": "arrow",
			"x": 528,
			"y": -1760,
			"width": 76,
			"height": 54.5,
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
			"seed": 1423847713,
			"version": 2,
			"versionNonce": 232648472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-54.5
				],
				[
					76,
					-54.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "cUUP4cv3",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "p92QBy8X",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a1"
		},
		{
			"id": "MEU65BmR",
			"type": "arrow",
			"x": 528,
			"y": -1760,
			"width": 76,
			"height": 0,
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
			"seed": 1577266123,
			"version": 2,
			"versionNonce": 982396520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					76,
					0
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "cUUP4cv3",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GFExJ6uQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a2"
		},
		{
			"id": "5bEEEF7u",
			"type": "arrow",
			"x": 528,
			"y": -1760,
			"width": 76,
			"height": 54.5,
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
			"seed": 452499193,
			"version": 2,
			"versionNonce": 528501784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					54.5
				],
				[
					76,
					54.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "cUUP4cv3",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6NnRFLV7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a3"
		},
		{
			"id": "a6FtY8wm",
			"type": "arrow",
			"x": 237,
			"y": -0.0,
			"width": 150,
			"height": 1362.58,
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
			"seed": 2035199255,
			"version": 2,
			"versionNonce": 1351360872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-1362.58
				],
				[
					150,
					-1362.58
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a4"
		},
		{
			"id": "BG4TggsE",
			"type": "arrow",
			"x": 667,
			"y": -1362.58,
			"width": 76,
			"height": 258.42,
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
			"seed": 1005218541,
			"version": 2,
			"versionNonce": 1724844312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-258.42
				],
				[
					76,
					-258.42
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LcDDLreF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a5"
		},
		{
			"id": "FdSa3Sy4",
			"type": "arrow",
			"x": 667,
			"y": -1362.58,
			"width": 76,
			"height": 115.77,
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
			"seed": 740112173,
			"version": 2,
			"versionNonce": 2018751592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-115.77
				],
				[
					76,
					-115.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NAnSzUdR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a6"
		},
		{
			"id": "aULAykmD",
			"type": "arrow",
			"x": 667,
			"y": -1362.58,
			"width": 76,
			"height": 47.63,
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
			"seed": 229498734,
			"version": 2,
			"versionNonce": 792602136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					47.63
				],
				[
					76,
					47.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "f7HePCwP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a7"
		},
		{
			"id": "QB2J9NAp",
			"type": "arrow",
			"x": 667,
			"y": -1362.58,
			"width": 76,
			"height": 143.63,
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
			"seed": 504956391,
			"version": 2,
			"versionNonce": 129034088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					143.63
				],
				[
					76,
					143.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RPmVz3GC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a8"
		},
		{
			"id": "FNe6Y8qG",
			"type": "arrow",
			"x": 667,
			"y": -1362.58,
			"width": 76,
			"height": 258.43,
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
			"seed": 2104254353,
			"version": 2,
			"versionNonce": 901882648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					258.43
				],
				[
					76,
					258.43
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "EerFG7nx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KbkzH685",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "a9"
		},
		{
			"id": "zZsWKUiW",
			"type": "arrow",
			"x": 856,
			"y": -1478.35,
			"width": 60,
			"height": 91.4,
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
			"seed": 934085509,
			"version": 2,
			"versionNonce": 988789352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-91.4
				],
				[
					60,
					-91.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NAnSzUdR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YUTVQiEA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aA"
		},
		{
			"id": "cpFYdnuc",
			"type": "arrow",
			"x": 856,
			"y": -1478.35,
			"width": 60,
			"height": 24.6,
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
			"seed": 2072058750,
			"version": 2,
			"versionNonce": 2026733592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-24.6
				],
				[
					60,
					-24.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NAnSzUdR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VEmX36vY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aB"
		},
		{
			"id": "iZ4UxwQT",
			"type": "arrow",
			"x": 856,
			"y": -1478.35,
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
			"seed": 2092856713,
			"version": 2,
			"versionNonce": 1692151144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "NAnSzUdR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "K7wepTnA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aC"
		},
		{
			"id": "L5kX7b7Z",
			"type": "arrow",
			"x": 856,
			"y": -1478.35,
			"width": 60,
			"height": 91.4,
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
			"seed": 342439000,
			"version": 2,
			"versionNonce": 139836696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					91.4
				],
				[
					60,
					91.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "NAnSzUdR",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5xZGyF3S",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aD"
		},
		{
			"id": "xYQtratb",
			"type": "arrow",
			"x": 866,
			"y": -1314.95,
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
			"seed": 1444024850,
			"version": 2,
			"versionNonce": 516046952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "f7HePCwP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mLxF8FWw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aE"
		},
		{
			"id": "atQ5EFcF",
			"type": "arrow",
			"x": 866,
			"y": -1314.95,
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
			"seed": 1093264626,
			"version": 2,
			"versionNonce": 1439586840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "f7HePCwP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ZeXEpCMW",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aF"
		},
		{
			"id": "SfzaHzhs",
			"type": "arrow",
			"x": 885,
			"y": -1218.95,
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
			"seed": 1799199466,
			"version": 2,
			"versionNonce": 2020471656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RPmVz3GC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "g5hePmWJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aG"
		},
		{
			"id": "u3ZrqgTw",
			"type": "arrow",
			"x": 885,
			"y": -1218.95,
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
			"seed": 735754167,
			"version": 2,
			"versionNonce": 69949208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RPmVz3GC",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rWyHW9aX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aH"
		},
		{
			"id": "3ighJdS5",
			"type": "arrow",
			"x": 951,
			"y": -1104.15,
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
			"seed": 1089750971,
			"version": 2,
			"versionNonce": 673924712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "KbkzH685",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sDDEGYuF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aI"
		},
		{
			"id": "Mk5mrzQ4",
			"type": "arrow",
			"x": 951,
			"y": -1104.15,
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
			"seed": 1241506643,
			"version": 2,
			"versionNonce": 937473048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "KbkzH685",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RRQw8D5T",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aJ"
		},
		{
			"id": "wPdUdkU2",
			"type": "arrow",
			"x": 237,
			"y": -0.0,
			"width": 150,
			"height": 714.75,
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
			"seed": 1050434331,
			"version": 2,
			"versionNonce": 986069352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-714.75
				],
				[
					150,
					-714.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "rzChspnr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aK"
		},
		{
			"id": "n6ejuY4u",
			"type": "arrow",
			"x": 599,
			"y": -714.75,
			"width": 76,
			"height": 230,
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
			"seed": 2034871046,
			"version": 2,
			"versionNonce": 1726116120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-230
				],
				[
					76,
					-230
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzChspnr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nUyeZcxP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aL"
		},
		{
			"id": "gkTncPbX",
			"type": "arrow",
			"x": 599,
			"y": -714.75,
			"width": 76,
			"height": 67.2,
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
			"seed": 2064007893,
			"version": 2,
			"versionNonce": 1133169768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-67.2
				],
				[
					76,
					-67.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzChspnr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BX7hcRLq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aM"
		},
		{
			"id": "gPWN9ADF",
			"type": "arrow",
			"x": 599,
			"y": -714.75,
			"width": 76,
			"height": 95.6,
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
			"seed": 2139060275,
			"version": 2,
			"versionNonce": 681872920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					95.6
				],
				[
					76,
					95.6
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzChspnr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FrKFeCUw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aN"
		},
		{
			"id": "yy4pDNDN",
			"type": "arrow",
			"x": 599,
			"y": -714.75,
			"width": 76,
			"height": 230,
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
			"seed": 1949533480,
			"version": 2,
			"versionNonce": 205848424,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					230
				],
				[
					76,
					230
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzChspnr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "25nnVhYv",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aO"
		},
		{
			"id": "SVU2xjqw",
			"type": "arrow",
			"x": 743,
			"y": -944.75,
			"width": 60,
			"height": 57.4,
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
			"seed": 1802277964,
			"version": 2,
			"versionNonce": 102435608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-57.4
				],
				[
					60,
					-57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nUyeZcxP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "X66LemQP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aP"
		},
		{
			"id": "4TjxB65e",
			"type": "arrow",
			"x": 743,
			"y": -944.75,
			"width": 60,
			"height": 9.4,
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
			"seed": 504535405,
			"version": 2,
			"versionNonce": 1161876072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-9.4
				],
				[
					60,
					-9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nUyeZcxP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "iqR858F6",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aQ"
		},
		{
			"id": "RGiv2AF7",
			"type": "arrow",
			"x": 743,
			"y": -944.75,
			"width": 60,
			"height": 57.4,
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
			"seed": 981322851,
			"version": 2,
			"versionNonce": 1236920344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					57.4
				],
				[
					60,
					57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nUyeZcxP",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KBjZYJNT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aR"
		},
		{
			"id": "6K4trHGq",
			"type": "arrow",
			"x": 1039,
			"y": -781.95,
			"width": 60,
			"height": 57.4,
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
			"seed": 1514089936,
			"version": 2,
			"versionNonce": 894059880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-57.4
				],
				[
					60,
					-57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "BX7hcRLq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "29Ae9K7T",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aS"
		},
		{
			"id": "QqwNj7VQ",
			"type": "arrow",
			"x": 1039,
			"y": -781.95,
			"width": 60,
			"height": 9.4,
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
			"seed": 749476159,
			"version": 2,
			"versionNonce": 1333077272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "BX7hcRLq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QWi2kQyd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aT"
		},
		{
			"id": "AVDnDReG",
			"type": "arrow",
			"x": 1039,
			"y": -781.95,
			"width": 60,
			"height": 57.4,
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
			"seed": 1518188399,
			"version": 2,
			"versionNonce": 1772968040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					57.4
				],
				[
					60,
					57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "BX7hcRLq",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "J2tCnkN3",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aU"
		},
		{
			"id": "w9cY9Vn8",
			"type": "arrow",
			"x": 803,
			"y": -619.15,
			"width": 60,
			"height": 57.4,
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
			"seed": 1951952310,
			"version": 2,
			"versionNonce": 1421918744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-57.4
				],
				[
					60,
					-57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "FrKFeCUw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qQyZGAzQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aV"
		},
		{
			"id": "nfwqJF3j",
			"type": "arrow",
			"x": 803,
			"y": -619.15,
			"width": 60,
			"height": 9.4,
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
			"seed": 504316555,
			"version": 2,
			"versionNonce": 1714817896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-9.4
				],
				[
					60,
					-9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "FrKFeCUw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aepWVLM7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aW"
		},
		{
			"id": "znz28Ptw",
			"type": "arrow",
			"x": 803,
			"y": -619.15,
			"width": 60,
			"height": 57.4,
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
			"seed": 1587483883,
			"version": 2,
			"versionNonce": 1217445656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					57.4
				],
				[
					60,
					57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "FrKFeCUw",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4M2ZiCLG",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aX"
		},
		{
			"id": "K4XGNmH3",
			"type": "arrow",
			"x": 870,
			"y": -484.75,
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
			"seed": 953020637,
			"version": 2,
			"versionNonce": 1429233256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "25nnVhYv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "JFdnPpZ9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aY"
		},
		{
			"id": "CdraHAfZ",
			"type": "arrow",
			"x": 870,
			"y": -484.75,
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
			"seed": 1820417997,
			"version": 2,
			"versionNonce": 458824728,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "25nnVhYv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XncZk9eJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aZ"
		},
		{
			"id": "CXbKBTFH",
			"type": "arrow",
			"x": 237,
			"y": -0.0,
			"width": 150,
			"height": 28.48,
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
			"seed": 647531529,
			"version": 2,
			"versionNonce": 929583464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					28.48
				],
				[
					150,
					28.48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aa"
		},
		{
			"id": "2QaDKMy6",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 374.18,
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
			"seed": 787423094,
			"version": 2,
			"versionNonce": 252565784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-374.18
				],
				[
					76,
					-374.18
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yzWByTZh",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ab"
		},
		{
			"id": "fB8AwVfj",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 300.88,
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
			"seed": 1609618405,
			"version": 2,
			"versionNonce": 338289768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-300.88
				],
				[
					76,
					-300.88
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "gYujgzcS",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ac"
		},
		{
			"id": "b63BPFQT",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 177.63,
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
			"seed": 50777892,
			"version": 2,
			"versionNonce": 119731736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-177.63
				],
				[
					76,
					-177.63
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cBBTPS8Z",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ad"
		},
		{
			"id": "mGP5wHuL",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 24.33,
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
			"seed": 1496460653,
			"version": 2,
			"versionNonce": 692131688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-24.33
				],
				[
					76,
					-24.33
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5hgN3QNp",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ae"
		},
		{
			"id": "9jTtdhcD",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 71.47,
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
			"seed": 558766481,
			"version": 2,
			"versionNonce": 1485599512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					71.47
				],
				[
					76,
					71.47
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YhH2AXNQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "af"
		},
		{
			"id": "NzDvjaUE",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 162.77,
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
			"seed": 2004943815,
			"version": 2,
			"versionNonce": 452586088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					162.77
				],
				[
					76,
					162.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "G5M3GR3Q",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ag"
		},
		{
			"id": "WStMCjvk",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 244.77,
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
			"seed": 1305532712,
			"version": 2,
			"versionNonce": 431902744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					244.77
				],
				[
					76,
					244.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ZBaNJCau",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ah"
		},
		{
			"id": "pMKid5BG",
			"type": "arrow",
			"x": 597,
			"y": 28.48,
			"width": 76,
			"height": 374.17,
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
			"seed": 795169366,
			"version": 2,
			"versionNonce": 606100840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					374.17
				],
				[
					76,
					374.17
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "AeWWH69P",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "D5FRgnjs",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ai"
		},
		{
			"id": "Y6rudwAj",
			"type": "arrow",
			"x": 778,
			"y": -149.15,
			"width": 60,
			"height": 72,
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
			"seed": 663562263,
			"version": 2,
			"versionNonce": 1923910936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "cBBTPS8Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mmPF6ba8",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aj"
		},
		{
			"id": "G9XtMWwc",
			"type": "arrow",
			"x": 778,
			"y": -149.15,
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
			"seed": 1820956088,
			"version": 2,
			"versionNonce": 1174433896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "cBBTPS8Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "jFLhiFdn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ak"
		},
		{
			"id": "Zp8sAdWg",
			"type": "arrow",
			"x": 778,
			"y": -149.15,
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
			"seed": 2076943310,
			"version": 2,
			"versionNonce": 1825253912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "cBBTPS8Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "96aXrGTC",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "al"
		},
		{
			"id": "QUUi9CkC",
			"type": "arrow",
			"x": 778,
			"y": -149.15,
			"width": 60,
			"height": 72,
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
			"seed": 1985975864,
			"version": 2,
			"versionNonce": 2019959656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "cBBTPS8Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VJRKMGUP",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "am"
		},
		{
			"id": "Hzy855sx",
			"type": "arrow",
			"x": 1069,
			"y": 191.25,
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
			"seed": 2030676852,
			"version": 2,
			"versionNonce": 1125000984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "G5M3GR3Q",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "G9iU6Bhk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "an"
		},
		{
			"id": "XX5hzjtJ",
			"type": "arrow",
			"x": 907,
			"y": 273.25,
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
			"seed": 690894095,
			"version": 2,
			"versionNonce": 1503491688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "ZBaNJCau",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "eJHFaU4Q",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ao"
		},
		{
			"id": "HmBXMraq",
			"type": "arrow",
			"x": 907,
			"y": 273.25,
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
			"seed": 312509258,
			"version": 2,
			"versionNonce": 837387288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "ZBaNJCau",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "u4VqzVCk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ap"
		},
		{
			"id": "gWydKbgX",
			"type": "arrow",
			"x": 833,
			"y": 402.65,
			"width": 60,
			"height": 57.4,
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
			"seed": 285706005,
			"version": 2,
			"versionNonce": 1584556392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-57.4
				],
				[
					60,
					-57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "D5FRgnjs",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ayLziZxj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aq"
		},
		{
			"id": "Gfc3U69P",
			"type": "arrow",
			"x": 833,
			"y": 402.65,
			"width": 60,
			"height": 9.4,
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
			"seed": 552681449,
			"version": 2,
			"versionNonce": 1196507416,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-9.4
				],
				[
					60,
					-9.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "D5FRgnjs",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "YcduKesH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ar"
		},
		{
			"id": "8ahK7Bci",
			"type": "arrow",
			"x": 833,
			"y": 402.65,
			"width": 60,
			"height": 57.4,
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
			"seed": 997899955,
			"version": 2,
			"versionNonce": 36764776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					57.4
				],
				[
					60,
					57.4
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "D5FRgnjs",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MiXL2SK4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "as"
		},
		{
			"id": "ZXekJBiT",
			"type": "arrow",
			"x": 237,
			"y": -0.0,
			"width": 150,
			"height": 1168,
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
			"seed": 1117724677,
			"version": 2,
			"versionNonce": 851009048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					1168
				],
				[
					150,
					1168
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "at"
		},
		{
			"id": "EnHwsfFs",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 529.75,
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
			"seed": 2019793652,
			"version": 2,
			"versionNonce": 1990537064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-529.75
				],
				[
					76,
					-529.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "aUmPYWeQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "au"
		},
		{
			"id": "FT6TdDZ9",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 371.55,
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
			"seed": 1131849316,
			"version": 2,
			"versionNonce": 353753880,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-371.55
				],
				[
					76,
					-371.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QiDacq4S",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "av"
		},
		{
			"id": "pJ6ZiMBK",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 193.55,
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
			"seed": 1107613761,
			"version": 2,
			"versionNonce": 1411056232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-193.55
				],
				[
					76,
					-193.55
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "aw"
		},
		{
			"id": "nuXCzpby",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 7.85,
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
			"seed": 1046346719,
			"version": 2,
			"versionNonce": 1356511256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					7.85
				],
				[
					76,
					7.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SMEesmMJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ax"
		},
		{
			"id": "QkHmQyJm",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 137.25,
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
			"seed": 814773921,
			"version": 2,
			"versionNonce": 1230927208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					137.25
				],
				[
					76,
					137.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "iBtZS2fT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "ay"
		},
		{
			"id": "8JDQyJFf",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 259,
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
			"seed": 491622082,
			"version": 2,
			"versionNonce": 1509684504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					259
				],
				[
					76,
					259
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mBYFTAsx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "az"
		},
		{
			"id": "Ki8p3WqU",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 347.25,
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
			"seed": 779544225,
			"version": 2,
			"versionNonce": 1270581352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					347.25
				],
				[
					76,
					347.25
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4JEJJ7kT",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b00"
		},
		{
			"id": "ZYZpJaTz",
			"type": "arrow",
			"x": 646,
			"y": 1168,
			"width": 76,
			"height": 529.75,
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
			"seed": 1881012222,
			"version": 2,
			"versionNonce": 99455512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					529.75
				],
				[
					76,
					529.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "nWYNg3RQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b01"
		},
		{
			"id": "EN4CGn5r",
			"type": "arrow",
			"x": 1160,
			"y": 638.25,
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
			"seed": 215615407,
			"version": 2,
			"versionNonce": 1191066472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "aUmPYWeQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Mu4pDgRz",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b02"
		},
		{
			"id": "CpsVAGUW",
			"type": "arrow",
			"x": 1160,
			"y": 638.25,
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
			"seed": 1797068820,
			"version": 2,
			"versionNonce": 1537445656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "aUmPYWeQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SkFVY7Vm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b03"
		},
		{
			"id": "BUhfXAzR",
			"type": "arrow",
			"x": 1160,
			"y": 638.25,
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
			"seed": 794067477,
			"version": 2,
			"versionNonce": 1299353192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "aUmPYWeQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "r2xjH2Pf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b04"
		},
		{
			"id": "t6fncGCW",
			"type": "arrow",
			"x": 1160,
			"y": 638.25,
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
			"seed": 1064949424,
			"version": 2,
			"versionNonce": 1670507544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "aUmPYWeQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4WSzuRrb",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b05"
		},
		{
			"id": "ixiEA6BC",
			"type": "arrow",
			"x": 1177,
			"y": 796.45,
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
			"seed": 987414240,
			"version": 2,
			"versionNonce": 1206157672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "QiDacq4S",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Z7UYKR7k",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b06"
		},
		{
			"id": "3YjEHdCr",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
			"width": 60,
			"height": 120,
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
			"seed": 626140761,
			"version": 2,
			"versionNonce": 2007804184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "cEX8UWFk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b07"
		},
		{
			"id": "Ug4gch9w",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
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
			"seed": 48419088,
			"version": 2,
			"versionNonce": 631247976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "FpfWyHQi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b08"
		},
		{
			"id": "F5sLDDb8",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
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
			"seed": 2049647372,
			"version": 2,
			"versionNonce": 325568024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RvLhUSug",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b09"
		},
		{
			"id": "FpzLbpdP",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
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
			"seed": 259602981,
			"version": 2,
			"versionNonce": 208750440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kiEfe5qu",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0A"
		},
		{
			"id": "C7gwbzGr",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
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
			"seed": 54906124,
			"version": 2,
			"versionNonce": 599212824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8aVbyFqq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0B"
		},
		{
			"id": "RhKfqHeL",
			"type": "arrow",
			"x": 994,
			"y": 974.45,
			"width": 60,
			"height": 120,
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
			"seed": 1123899117,
			"version": 2,
			"versionNonce": 144972392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wSkBJTvA",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6avnXGSV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0C"
		},
		{
			"id": "qJQQXGaq",
			"type": "arrow",
			"x": 1181,
			"y": 1175.85,
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
			"seed": 289468075,
			"version": 2,
			"versionNonce": 1460609048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SMEesmMJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "GXxPbX9Z",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0D"
		},
		{
			"id": "X2q7saXX",
			"type": "arrow",
			"x": 1181,
			"y": 1175.85,
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
			"seed": 11126979,
			"version": 2,
			"versionNonce": 1023708520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SMEesmMJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "A399VZCt",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0E"
		},
		{
			"id": "PKxDVxsT",
			"type": "arrow",
			"x": 868,
			"y": 1305.25,
			"width": 60,
			"height": 48,
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
			"seed": 1748192637,
			"version": 2,
			"versionNonce": 1835228440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "iBtZS2fT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "h6fkMSQm",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0F"
		},
		{
			"id": "xVQEJqcZ",
			"type": "arrow",
			"x": 868,
			"y": 1305.25,
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
			"seed": 153365973,
			"version": 2,
			"versionNonce": 316579944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "iBtZS2fT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "C8dVD5en",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0G"
		},
		{
			"id": "FmAdMxgZ",
			"type": "arrow",
			"x": 868,
			"y": 1305.25,
			"width": 60,
			"height": 48,
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
			"seed": 632854651,
			"version": 2,
			"versionNonce": 136837656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "iBtZS2fT",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Pfjn7iVq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0H"
		},
		{
			"id": "tESW9fbQ",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
			"width": 60,
			"height": 120,
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
			"seed": 1300058562,
			"version": 2,
			"versionNonce": 1778275176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "WRqMxTnA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0I"
		},
		{
			"id": "DWqYp9Kg",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
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
			"seed": 1914771488,
			"version": 2,
			"versionNonce": 2052126488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "HwsePN4D",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0J"
		},
		{
			"id": "7s5yd4AD",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
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
			"seed": 1072724553,
			"version": 2,
			"versionNonce": 1219470952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fnHcmdkN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0K"
		},
		{
			"id": "RPZkEzNp",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
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
			"seed": 1401214547,
			"version": 2,
			"versionNonce": 408048664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VGnF2hDa",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0L"
		},
		{
			"id": "VsjSxYTA",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
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
			"seed": 585052036,
			"version": 2,
			"versionNonce": 197040488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qhzzYbnq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0M"
		},
		{
			"id": "jUPV5AjM",
			"type": "arrow",
			"x": 803,
			"y": 1697.75,
			"width": 60,
			"height": 120,
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
			"seed": 1103690820,
			"version": 2,
			"versionNonce": 136319256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "SPC2U5xx",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "qEZQjJr7",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0N"
		},
		{
			"id": "nMqKfexc",
			"type": "arrow",
			"x": -237,
			"y": -0.0,
			"width": 150,
			"height": 705.45,
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
			"seed": 384234252,
			"version": 2,
			"versionNonce": 376908904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-705.45
				],
				[
					-150,
					-705.45
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0O"
		},
		{
			"id": "bVPkj827",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 443.2,
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
			"seed": 1476188401,
			"version": 2,
			"versionNonce": 288239128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-443.2
				],
				[
					-76,
					-443.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5m4SYinV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0P"
		},
		{
			"id": "zecP6vbv",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 286.75,
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
			"seed": 2119953448,
			"version": 2,
			"versionNonce": 44392296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-286.75
				],
				[
					-76,
					-286.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Uc6SLTXN",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Q"
		},
		{
			"id": "PSSxCBEG",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 94.35,
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
			"seed": 644756774,
			"version": 2,
			"versionNonce": 1819323160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-94.35
				],
				[
					-76,
					-94.35
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "nyLHwHQj",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0R"
		},
		{
			"id": "Xz3GrFbm",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 49.65,
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
			"seed": 218519416,
			"version": 2,
			"versionNonce": 1351955048,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					49.65
				],
				[
					-76,
					49.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XvyqeS7Z",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0S"
		},
		{
			"id": "Df2AHMwU",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 193.65,
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
			"seed": 4104929,
			"version": 2,
			"versionNonce": 341542936,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					193.65
				],
				[
					-76,
					193.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "K6FxG3Qr",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0T"
		},
		{
			"id": "DeK8BjaZ",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 304.15,
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
			"seed": 1664485633,
			"version": 2,
			"versionNonce": 387097960,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					304.15
				],
				[
					-76,
					304.15
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "75qx32fd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0U"
		},
		{
			"id": "pSq8BzM4",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 369.9,
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
			"seed": 1714830574,
			"version": 2,
			"versionNonce": 350405912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					369.9
				],
				[
					-76,
					369.9
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "kZhPc7e5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0V"
		},
		{
			"id": "khxwWcPm",
			"type": "arrow",
			"x": -696,
			"y": -705.45,
			"width": 76,
			"height": 443.2,
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
			"seed": 1159457055,
			"version": 2,
			"versionNonce": 862566504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					443.2
				],
				[
					-76,
					443.2
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "7B5ujLyJ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SNRUf5aH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0W"
		},
		{
			"id": "775iSV7A",
			"type": "arrow",
			"x": -1176,
			"y": -1148.65,
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
			"seed": 1412481071,
			"version": 2,
			"versionNonce": 1534747160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "5m4SYinV",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "EGe2cQbD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0X"
		},
		{
			"id": "k4KGfwuV",
			"type": "arrow",
			"x": -1209,
			"y": -992.2,
			"width": 60,
			"height": 86.4,
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
			"seed": 796456695,
			"version": 2,
			"versionNonce": 2036755304,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "Uc6SLTXN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "6ayDX3mi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Y"
		},
		{
			"id": "U58PqwQx",
			"type": "arrow",
			"x": -1209,
			"y": -992.2,
			"width": 60,
			"height": 38.4,
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
			"seed": 1271309479,
			"version": 2,
			"versionNonce": 118906648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "Uc6SLTXN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "zRA5fhyA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0Z"
		},
		{
			"id": "qrEvjQgu",
			"type": "arrow",
			"x": -1209,
			"y": -992.2,
			"width": 60,
			"height": 9.6,
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
			"seed": 283311551,
			"version": 2,
			"versionNonce": 1666498152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "Uc6SLTXN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5bidCHGD",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0a"
		},
		{
			"id": "VsSqKVsD",
			"type": "arrow",
			"x": -1209,
			"y": -992.2,
			"width": 60,
			"height": 86.4,
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
			"seed": 407631100,
			"version": 2,
			"versionNonce": 942324760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "Uc6SLTXN",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "NySmdD8Q",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0b"
		},
		{
			"id": "5hTWpzGD",
			"type": "arrow",
			"x": -913,
			"y": -799.8,
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
			"seed": 1824414778,
			"version": 2,
			"versionNonce": 1107341672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "nyLHwHQj",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "fpgYEqqU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0c"
		},
		{
			"id": "WiP3FGtj",
			"type": "arrow",
			"x": -913,
			"y": -799.8,
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
			"seed": 2037533322,
			"version": 2,
			"versionNonce": 1621850392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "nyLHwHQj",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wB93K76c",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0d"
		},
		{
			"id": "Yy8Pp7g7",
			"type": "arrow",
			"x": -913,
			"y": -799.8,
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
			"seed": 1866698416,
			"version": 2,
			"versionNonce": 1823884392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "nyLHwHQj",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "VyiuRkdd",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0e"
		},
		{
			"id": "AwKbFqfU",
			"type": "arrow",
			"x": -985,
			"y": -655.8,
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
			"seed": 1596149158,
			"version": 2,
			"versionNonce": 336369176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "XvyqeS7Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "mm2P7EDi",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0f"
		},
		{
			"id": "NJWbbCWV",
			"type": "arrow",
			"x": -985,
			"y": -655.8,
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
			"seed": 1542126699,
			"version": 2,
			"versionNonce": 1900115816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "XvyqeS7Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "sAFCPMZX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0g"
		},
		{
			"id": "9a3sCaDm",
			"type": "arrow",
			"x": -985,
			"y": -655.8,
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
			"seed": 1022121538,
			"version": 2,
			"versionNonce": 1463948056,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "XvyqeS7Z",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "KVzCCBU9",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0h"
		},
		{
			"id": "qUwdRD6C",
			"type": "arrow",
			"x": -877,
			"y": -511.8,
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
			"seed": 1587844447,
			"version": 2,
			"versionNonce": 1139690088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "K6FxG3Qr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "T86gBdFE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0i"
		},
		{
			"id": "rLmxwxSp",
			"type": "arrow",
			"x": -877,
			"y": -511.8,
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
			"seed": 1587145022,
			"version": 2,
			"versionNonce": 1891627032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "K6FxG3Qr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8wfjUSxA",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0j"
		},
		{
			"id": "Tw7m9TMt",
			"type": "arrow",
			"x": -877,
			"y": -511.8,
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
			"seed": 1947294949,
			"version": 2,
			"versionNonce": 1871232360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "K6FxG3Qr",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "8vBtbp8A",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0k"
		},
		{
			"id": "wAaUa7VN",
			"type": "arrow",
			"x": -237,
			"y": -0.0,
			"width": 150,
			"height": 218.52,
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
			"seed": 344691257,
			"version": 2,
			"versionNonce": 947531032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					218.52
				],
				[
					-150,
					218.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0l"
		},
		{
			"id": "i84GKMZz",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 373.77,
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
			"seed": 1197424819,
			"version": 2,
			"versionNonce": 1163710568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-373.77
				],
				[
					-76,
					-373.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4YuBHEFu",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0m"
		},
		{
			"id": "cSDwYddJ",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 296.77,
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
			"seed": 812235152,
			"version": 2,
			"versionNonce": 1743047192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-296.77
				],
				[
					-76,
					-296.77
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "bXKh2pH5",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0n"
		},
		{
			"id": "uxbkWPEC",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 173.52,
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
			"seed": 1147335202,
			"version": 2,
			"versionNonce": 221676392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-173.52
				],
				[
					-76,
					-173.52
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "RVmMMJCY",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0o"
		},
		{
			"id": "iwxJu4SH",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 42.48,
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
			"seed": 132504341,
			"version": 2,
			"versionNonce": 1777583896,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					42.48
				],
				[
					-76,
					42.48
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0p"
		},
		{
			"id": "4wzTL9nJ",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 200.98,
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
			"seed": 1261645119,
			"version": 2,
			"versionNonce": 895604328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					200.98
				],
				[
					-76,
					200.98
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tniZFMYU",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0q"
		},
		{
			"id": "SMmiC3SE",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 296.78,
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
			"seed": 149549800,
			"version": 2,
			"versionNonce": 723199000,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					296.78
				],
				[
					-76,
					296.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "BYUvkH8N",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0r"
		},
		{
			"id": "UjwwxEzz",
			"type": "arrow",
			"x": -761,
			"y": 218.52,
			"width": 76,
			"height": 373.78,
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
			"seed": 1839170034,
			"version": 2,
			"versionNonce": 44747112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					373.78
				],
				[
					-76,
					373.78
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "9UzpSnuX",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Qy3pMDRe",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0s"
		},
		{
			"id": "NhPnjuYH",
			"type": "arrow",
			"x": -1100,
			"y": 45,
			"width": 60,
			"height": 72,
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
			"seed": 1461208897,
			"version": 2,
			"versionNonce": 1766777112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RVmMMJCY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "tV3vpTr4",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0t"
		},
		{
			"id": "xgQHguqa",
			"type": "arrow",
			"x": -1100,
			"y": 45,
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
			"seed": 746671520,
			"version": 2,
			"versionNonce": 1079860328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RVmMMJCY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "MkPYreKg",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0u"
		},
		{
			"id": "CsdYXCRQ",
			"type": "arrow",
			"x": -1100,
			"y": 45,
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
			"seed": 1007740437,
			"version": 2,
			"versionNonce": 67304984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RVmMMJCY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "QZmswNmF",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0v"
		},
		{
			"id": "ibnmSkRd",
			"type": "arrow",
			"x": -1100,
			"y": 45,
			"width": 60,
			"height": 72,
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
			"seed": 959245098,
			"version": 2,
			"versionNonce": 1883606888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "RVmMMJCY",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pED7Reff",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0w"
		},
		{
			"id": "6LLEn7HL",
			"type": "arrow",
			"x": -942,
			"y": 261,
			"width": 60,
			"height": 96,
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
			"seed": 1305483585,
			"version": 2,
			"versionNonce": 1277917976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-96
				],
				[
					-60,
					-96
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "vZBmk8eJ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0x"
		},
		{
			"id": "4HUVCDur",
			"type": "arrow",
			"x": -942,
			"y": 261,
			"width": 60,
			"height": 48,
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
			"seed": 694258400,
			"version": 2,
			"versionNonce": 2058314344,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CckpTVdB",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0y"
		},
		{
			"id": "AwcVT3Df",
			"type": "arrow",
			"x": -942,
			"y": 261,
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
			"seed": 1797766869,
			"version": 2,
			"versionNonce": 1413240856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "yV874EPH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b0z"
		},
		{
			"id": "gqWZGTny",
			"type": "arrow",
			"x": -942,
			"y": 261,
			"width": 60,
			"height": 48,
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
			"seed": 1745078058,
			"version": 2,
			"versionNonce": 1583797608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "dbSkgR8M",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b10"
		},
		{
			"id": "WDMtVHdy",
			"type": "arrow",
			"x": -942,
			"y": 261,
			"width": 60,
			"height": 96,
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
			"seed": 1178377901,
			"version": 2,
			"versionNonce": 1076466968,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					96
				],
				[
					-60,
					96
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "ASnBzMyE",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "AMz5FkVf",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b11"
		},
		{
			"id": "FPsuEaJQ",
			"type": "arrow",
			"x": -237,
			"y": -0.0,
			"width": 150,
			"height": 927.75,
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
			"seed": 1867484863,
			"version": 2,
			"versionNonce": 1622665320,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					927.75
				],
				[
					-150,
					927.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "G4BLCNSv",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b12"
		},
		{
			"id": "mTgDCDx6",
			"type": "arrow",
			"x": -479,
			"y": 927.75,
			"width": 76,
			"height": 209.65,
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
			"seed": 1606021630,
			"version": 2,
			"versionNonce": 359084568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-209.65
				],
				[
					-76,
					-209.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "wELM4z2t",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b13"
		},
		{
			"id": "KCS2zkLm",
			"type": "arrow",
			"x": -479,
			"y": 927.75,
			"width": 76,
			"height": 113.85,
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
			"seed": 824456052,
			"version": 2,
			"versionNonce": 1030658920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-113.85
				],
				[
					-76,
					-113.85
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "pFjexcyw",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b14"
		},
		{
			"id": "fScZQXtt",
			"type": "arrow",
			"x": -479,
			"y": 927.75,
			"width": 76,
			"height": 48.1,
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
			"seed": 385546771,
			"version": 2,
			"versionNonce": 183054104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					-48.1
				],
				[
					-76,
					-48.1
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "4Sph2aky",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b15"
		},
		{
			"id": "kt9NzBTM",
			"type": "arrow",
			"x": -479,
			"y": 927.75,
			"width": 76,
			"height": 75.15,
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
			"seed": 754726870,
			"version": 2,
			"versionNonce": 1456926312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					75.15
				],
				[
					-76,
					75.15
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "LNv378bV",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b16"
		},
		{
			"id": "pUWbCXkD",
			"type": "arrow",
			"x": -479,
			"y": 927.75,
			"width": 76,
			"height": 209.65,
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
			"seed": 1250696015,
			"version": 2,
			"versionNonce": 1495501848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
					209.65
				],
				[
					-76,
					209.65
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "SKNxh5fQ",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "XU9PULSn",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b17"
		},
		{
			"id": "h6WKhumW",
			"type": "arrow",
			"x": -977,
			"y": 718.1,
			"width": 60,
			"height": 9.4,
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
			"seed": 671791259,
			"version": 2,
			"versionNonce": 1706877288,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "wELM4z2t",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "CTqWarTq",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b18"
		},
		{
			"id": "x8xSbPVH",
			"type": "arrow",
			"x": -697,
			"y": 1002.9,
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
			"seed": 283432131,
			"version": 2,
			"versionNonce": 168446232,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "LNv378bV",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "52Hdj5xH",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b19"
		},
		{
			"id": "ubmbSrLD",
			"type": "arrow",
			"x": -697,
			"y": 1002.9,
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
			"seed": 1687612603,
			"version": 2,
			"versionNonce": 694973544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "LNv378bV",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "t7mWSiMk",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b1A"
		},
		{
			"id": "3psycaCm",
			"type": "arrow",
			"x": -697,
			"y": 1002.9,
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
			"seed": 1561647700,
			"version": 2,
			"versionNonce": 1225877016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "LNv378bV",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "7JEwxByx",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b1B"
		},
		{
			"id": "KH3xPPLm",
			"type": "arrow",
			"x": -697,
			"y": 1002.9,
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
			"seed": 453400579,
			"version": 2,
			"versionNonce": 397518696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "LNv378bV",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "Rq9jMR85",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b1C"
		},
		{
			"id": "3vWWsN9d",
			"type": "arrow",
			"x": -1005,
			"y": 1137.4,
			"width": 60,
			"height": 9.4,
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
			"seed": 597589382,
			"version": 2,
			"versionNonce": 858579736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
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
				"elementId": "XU9PULSn",
				"focus": 0,
				"gap": 1
			},
			"endBinding": {
				"elementId": "5EnZ8WaR",
				"focus": 0,
				"gap": 1
			},
			"startArrowhead": null,
			"endArrowhead": null,
			"elbowed": false,
			"index": "b1D"
		},
		{
			"id": "G4BLCNSv",
			"type": "rectangle",
			"x": -237,
			"y": -67,
			"width": 474,
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
			"seed": 767610671,
			"version": 2,
			"versionNonce": 215513704,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UmHhNwz5"
				},
				{
					"type": "arrow",
					"id": "c5fav7cV"
				},
				{
					"type": "arrow",
					"id": "a6FtY8wm"
				},
				{
					"type": "arrow",
					"id": "wPdUdkU2"
				},
				{
					"type": "arrow",
					"id": "CXbKBTFH"
				},
				{
					"type": "arrow",
					"id": "ZXekJBiT"
				},
				{
					"type": "arrow",
					"id": "nMqKfexc"
				},
				{
					"type": "arrow",
					"id": "wAaUa7VN"
				},
				{
					"type": "arrow",
					"id": "FPsuEaJQ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1E"
		},
		{
			"id": "UmHhNwz5",
			"type": "text",
			"x": -205,
			"y": -45,
			"width": 410,
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
			"seed": 444975023,
			"version": 2,
			"versionNonce": 651214872,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 36,
			"fontFamily": 5,
			"text": "程式如何處理並解讀文字\nDeck 5・W8",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G4BLCNSv",
			"originalText": "程式如何處理並解讀文字\nDeck 5・W8",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1F"
		},
		{
			"id": "cUUP4cv3",
			"type": "rectangle",
			"x": 387,
			"y": -1787,
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
			"seed": 118877186,
			"version": 2,
			"versionNonce": 2074930536,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HgsqfuTh"
				},
				{
					"type": "arrow",
					"id": "c5fav7cV"
				},
				{
					"type": "arrow",
					"id": "D389THUc"
				},
				{
					"type": "arrow",
					"id": "MEU65BmR"
				},
				{
					"type": "arrow",
					"id": "5bEEEF7u"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1G"
		},
		{
			"id": "HgsqfuTh",
			"type": "text",
			"x": 407,
			"y": -1775,
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
			"seed": 1887455359,
			"version": 2,
			"versionNonce": 334560536,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "驅動問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cUUP4cv3",
			"originalText": "驅動問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1H"
		},
		{
			"id": "p92QBy8X",
			"type": "rectangle",
			"x": 604,
			"y": -1834.75,
			"width": 298,
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
			"seed": 1918347092,
			"version": 2,
			"versionNonce": 494600296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dt4VUv8t"
				},
				{
					"type": "arrow",
					"id": "D389THUc"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1I"
		},
		{
			"id": "dt4VUv8t",
			"type": "text",
			"x": 618,
			"y": -1825.75,
			"width": 270,
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
			"seed": 900188457,
			"version": 2,
			"versionNonce": 1275173400,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "一行輸入 Campus East,12.5,45",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "p92QBy8X",
			"originalText": "一行輸入 Campus East,12.5,45",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1J"
		},
		{
			"id": "GFExJ6uQ",
			"type": "rectangle",
			"x": 604,
			"y": -1780.25,
			"width": 234,
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
			"seed": 204242525,
			"version": 2,
			"versionNonce": 571388776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "97bzRBuM"
				},
				{
					"type": "arrow",
					"id": "MEU65BmR"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1K"
		},
		{
			"id": "97bzRBuM",
			"type": "text",
			"x": 618,
			"y": -1771.25,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1715137820,
			"version": 2,
			"versionNonce": 1375115032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "只清欄位邊緣，保留意義",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GFExJ6uQ",
			"originalText": "只清欄位邊緣，保留意義",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1L"
		},
		{
			"id": "6NnRFLV7",
			"type": "rectangle",
			"x": 604,
			"y": -1725.75,
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
			"seed": 1502781172,
			"version": 2,
			"versionNonce": 1605633640,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9jcKaFbc"
				},
				{
					"type": "arrow",
					"id": "5bEEEF7u"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1M"
		},
		{
			"id": "9jcKaFbc",
			"type": "text",
			"x": 618,
			"y": -1716.75,
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
			"seed": 454686682,
			"version": 2,
			"versionNonce": 709096472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "數值模型與總和不變，只換前端",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6NnRFLV7",
			"originalText": "數值模型與總和不變，只換前端",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1N"
		},
		{
			"id": "EerFG7nx",
			"type": "rectangle",
			"x": 387,
			"y": -1389.58,
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
			"seed": 346564368,
			"version": 2,
			"versionNonce": 53934440,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kuTASFyG"
				},
				{
					"type": "arrow",
					"id": "a6FtY8wm"
				},
				{
					"type": "arrow",
					"id": "BG4TggsE"
				},
				{
					"type": "arrow",
					"id": "FdSa3Sy4"
				},
				{
					"type": "arrow",
					"id": "aULAykmD"
				},
				{
					"type": "arrow",
					"id": "QB2J9NAp"
				},
				{
					"type": "arrow",
					"id": "FNe6Y8qG"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1O"
		},
		{
			"id": "kuTASFyG",
			"type": "text",
			"x": 407,
			"y": -1377.58,
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
			"seed": 1538773244,
			"version": 2,
			"versionNonce": 719171864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q1 文字的意義從哪來",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EerFG7nx",
			"originalText": "Q1 文字的意義從哪來",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1P"
		},
		{
			"id": "LcDDLreF",
			"type": "rectangle",
			"x": 743,
			"y": -1641.25,
			"width": 309,
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
			"seed": 768166930,
			"version": 2,
			"versionNonce": 1071877224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "q9KpBQqV"
				},
				{
					"type": "arrow",
					"id": "BG4TggsE"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1Q"
		},
		{
			"id": "q9KpBQqV",
			"type": "text",
			"x": 757,
			"y": -1632.25,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1243022848,
			"version": 2,
			"versionNonce": 1261948440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "意義來自約定格式，不是字串本身",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LcDDLreF",
			"originalText": "意義來自約定格式，不是字串本身",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1R"
		},
		{
			"id": "NAnSzUdR",
			"type": "rectangle",
			"x": 743,
			"y": -1498.6,
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
			"seed": 1823397483,
			"version": 2,
			"versionNonce": 2139471720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DshP3wb9"
				},
				{
					"type": "arrow",
					"id": "FdSa3Sy4"
				},
				{
					"type": "arrow",
					"id": "zZsWKUiW"
				},
				{
					"type": "arrow",
					"id": "cpFYdnuc"
				},
				{
					"type": "arrow",
					"id": "iZ4UxwQT"
				},
				{
					"type": "arrow",
					"id": "L5kX7b7Z"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1S"
		},
		{
			"id": "DshP3wb9",
			"type": "text",
			"x": 757,
			"y": -1489.6,
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
			"seed": 85275807,
			"version": 2,
			"versionNonce": 1950763800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "v0.5 約定",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NAnSzUdR",
			"originalText": "v0.5 約定",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1T"
		},
		{
			"id": "YUTVQiEA",
			"type": "rectangle",
			"x": 916,
			"y": -1586.75,
			"width": 253,
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
			"seed": 131387409,
			"version": 2,
			"versionNonce": 308908648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6pGyDN93"
				},
				{
					"type": "arrow",
					"id": "zZsWKUiW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1U"
		},
		{
			"id": "6pGyDN93",
			"type": "text",
			"x": 928,
			"y": -1579.75,
			"width": 229,
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
			"seed": 704244049,
			"version": 2,
			"versionNonce": 1350379544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "恰好三欄：route, km, minutes",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YUTVQiEA",
			"originalText": "恰好三欄：route, km, minutes",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1V"
		},
		{
			"id": "VEmX36vY",
			"type": "rectangle",
			"x": 916,
			"y": -1519.95,
			"width": 325,
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
				"jmTfwthc"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1107259199,
			"version": 2,
			"versionNonce": 1599800680,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5Mme3KY6"
				},
				{
					"type": "arrow",
					"id": "cpFYdnuc"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1W"
		},
		{
			"id": "5Mme3KY6",
			"type": "text",
			"x": 928,
			"y": -1512.95,
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
			"groupIds": [
				"jmTfwthc"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1286535691,
			"version": 2,
			"versionNonce": 466642200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "各欄 strip 兩端；保留內部空白與大小寫",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VEmX36vY",
			"originalText": "各欄 strip 兩端；保留內部空白與大小寫",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1X"
		},
		{
			"id": "K7wepTnA",
			"type": "rectangle",
			"x": 916,
			"y": -1471.95,
			"width": 424,
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
			"seed": 1763756549,
			"version": 2,
			"versionNonce": 329652328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ua2LaAVf"
				},
				{
					"type": "arrow",
					"id": "iZ4UxwQT"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1Y"
		},
		{
			"id": "ua2LaAVf",
			"type": "text",
			"x": 928,
			"y": -1464.95,
			"width": 400,
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
			"seed": 818103214,
			"version": 2,
			"versionNonce": 1941176856,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "DONE：整行 strip 後忽略大小寫（⚠ 改變了 Deck 4\n的精確 DONE）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "K7wepTnA",
			"originalText": "DONE：整行 strip 後忽略大小寫（⚠ 改變了 Deck 4\n的精確 DONE）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1Z"
		},
		{
			"id": "5xZGyF3S",
			"type": "rectangle",
			"x": 916,
			"y": -1403.95,
			"width": 327,
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
			"seed": 1422307327,
			"version": 2,
			"versionNonce": 1394002792,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wVJTvgvW"
				},
				{
					"type": "arrow",
					"id": "L5kX7b7Z"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1a"
		},
		{
			"id": "wVJTvgvW",
			"type": "text",
			"x": 928,
			"y": -1396.95,
			"width": 303,
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
			"seed": 1459431564,
			"version": 2,
			"versionNonce": 656146200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "拒絕雙引號與欄位數不對；不是完整 CSV",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5xZGyF3S",
			"originalText": "拒絕雙引號與欄位數不對；不是完整 CSV",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1b"
		},
		{
			"id": "f7HePCwP",
			"type": "rectangle",
			"x": 743,
			"y": -1335.2,
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
			"seed": 1892622060,
			"version": 2,
			"versionNonce": 1744379496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6jzNtDJn"
				},
				{
					"type": "arrow",
					"id": "aULAykmD"
				},
				{
					"type": "arrow",
					"id": "xYQtratb"
				},
				{
					"type": "arrow",
					"id": "atQ5EFcF"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1c"
		},
		{
			"id": "6jzNtDJn",
			"type": "text",
			"x": 757,
			"y": -1326.2,
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
			"seed": 371798677,
			"version": 2,
			"versionNonce": 108813336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "字串是資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "f7HePCwP",
			"originalText": "字串是資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1d"
		},
		{
			"id": "mLxF8FWw",
			"type": "rectangle",
			"x": 926,
			"y": -1355.95,
			"width": 307,
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
			"seed": 2146795422,
			"version": 2,
			"versionNonce": 1931022696,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bCUZB6xU"
				},
				{
					"type": "arrow",
					"id": "xYQtratb"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1e"
		},
		{
			"id": "bCUZB6xU",
			"type": "text",
			"x": 938,
			"y": -1348.95,
			"width": 283,
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
			"seed": 1658088045,
			"version": 2,
			"versionNonce": 868817176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "type(\"007\") → str；len(\"007\") → 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mLxF8FWw",
			"originalText": "type(\"007\") → str；len(\"007\") → 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1f"
		},
		{
			"id": "ZeXEpCMW",
			"type": "rectangle",
			"x": 926,
			"y": -1307.95,
			"width": 365,
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
			"seed": 986982084,
			"version": 2,
			"versionNonce": 465740904,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "M9Q8knrb"
				},
				{
					"type": "arrow",
					"id": "atQ5EFcF"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1g"
		},
		{
			"id": "M9Q8knrb",
			"type": "text",
			"x": 938,
			"y": -1300.95,
			"width": 341,
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
			"seed": 1571347448,
			"version": 2,
			"versionNonce": 1920349720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"3\" + \"5\" → 35；\"Trip \" * 2 → \"Trip Trip \"",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZeXEpCMW",
			"originalText": "\"3\" + \"5\" → 35；\"Trip \" * 2 → \"Trip Trip \"",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1h"
		},
		{
			"id": "RPmVz3GC",
			"type": "rectangle",
			"x": 743,
			"y": -1239.2,
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
			"seed": 1854611083,
			"version": 2,
			"versionNonce": 1069668200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xnVZavqD"
				},
				{
					"type": "arrow",
					"id": "QB2J9NAp"
				},
				{
					"type": "arrow",
					"id": "SfzaHzhs"
				},
				{
					"type": "arrow",
					"id": "u3ZrqgTw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1i"
		},
		{
			"id": "xnVZavqD",
			"type": "text",
			"x": 757,
			"y": -1230.2,
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
			"seed": 1043548869,
			"version": 2,
			"versionNonce": 2004333336,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "看不見的字元",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RPmVz3GC",
			"originalText": "看不見的字元",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1j"
		},
		{
			"id": "g5hePmWJ",
			"type": "rectangle",
			"x": 945,
			"y": -1259.95,
			"width": 292,
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
			"seed": 1305624838,
			"version": 2,
			"versionNonce": 593668712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LdajLnuC"
				},
				{
					"type": "arrow",
					"id": "SfzaHzhs"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1k"
		},
		{
			"id": "LdajLnuC",
			"type": "text",
			"x": 957,
			"y": -1252.95,
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
			"seed": 1823306600,
			"version": 2,
			"versionNonce": 960598040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"A\\tB\\nC\"：print 顯示 tab 與換行",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g5hePmWJ",
			"originalText": "\"A\\tB\\nC\"：print 顯示 tab 與換行",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1l"
		},
		{
			"id": "rWyHW9aX",
			"type": "rectangle",
			"x": 945,
			"y": -1211.95,
			"width": 241,
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
			"seed": 81903072,
			"version": 2,
			"versionNonce": 561061224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "jrXTSaDe"
				},
				{
					"type": "arrow",
					"id": "u3ZrqgTw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1m"
		},
		{
			"id": "jrXTSaDe",
			"type": "text",
			"x": 957,
			"y": -1204.95,
			"width": 217,
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
			"seed": 132602310,
			"version": 2,
			"versionNonce": 1070058776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "repr → 'A\\tB\\nC'；len → 5",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rWyHW9aX",
			"originalText": "repr → 'A\\tB\\nC'；len → 5",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1n"
		},
		{
			"id": "KbkzH685",
			"type": "rectangle",
			"x": 743,
			"y": -1124.4,
			"width": 208,
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
			"seed": 1274505724,
			"version": 2,
			"versionNonce": 1530474600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "k7hdRKLK"
				},
				{
					"type": "arrow",
					"id": "FNe6Y8qG"
				},
				{
					"type": "arrow",
					"id": "3ighJdS5"
				},
				{
					"type": "arrow",
					"id": "Mk5mrzQ4"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1o"
		},
		{
			"id": "k7hdRKLK",
			"type": "text",
			"x": 757,
			"y": -1115.4,
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
			"seed": 1584042702,
			"version": 2,
			"versionNonce": 1954441752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不可變（immutable）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KbkzH685",
			"originalText": "不可變（immutable）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1p"
		},
		{
			"id": "sDDEGYuF",
			"type": "rectangle",
			"x": 1011,
			"y": -1145.15,
			"width": 437,
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
				"dGfTUD9z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 402624703,
			"version": 2,
			"versionNonce": 1753670504,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rNuZs29b"
				},
				{
					"type": "arrow",
					"id": "3ighJdS5"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1q"
		},
		{
			"id": "rNuZs29b",
			"type": "text",
			"x": 1023,
			"y": -1138.15,
			"width": 413,
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
				"dGfTUD9z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 695885229,
			"version": 2,
			"versionNonce": 1918461720,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "s = \"Campus\"; t = s; s = \"Station\" → t 仍是 Campus",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sDDEGYuF",
			"originalText": "s = \"Campus\"; t = s; s = \"Station\" → t 仍是 Campus",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1r"
		},
		{
			"id": "RRQw8D5T",
			"type": "rectangle",
			"x": 1011,
			"y": -1097.15,
			"width": 323,
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
			"seed": 701935057,
			"version": 2,
			"versionNonce": 128333416,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CHvUU6Ve"
				},
				{
					"type": "arrow",
					"id": "Mk5mrzQ4"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1s"
		},
		{
			"id": "CHvUU6Ve",
			"type": "text",
			"x": 1023,
			"y": -1090.15,
			"width": 299,
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
			"seed": 264304496,
			"version": 2,
			"versionNonce": 1439482904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "不可變的是字串物件，不是變數不能重綁",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RRQw8D5T",
			"originalText": "不可變的是字串物件，不是變數不能重綁",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1t"
		},
		{
			"id": "rzChspnr",
			"type": "rectangle",
			"x": 387,
			"y": -741.75,
			"width": 212,
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
			"seed": 1615575314,
			"version": 2,
			"versionNonce": 1298344296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "meDHCqSC"
				},
				{
					"type": "arrow",
					"id": "wPdUdkU2"
				},
				{
					"type": "arrow",
					"id": "n6ejuY4u"
				},
				{
					"type": "arrow",
					"id": "gkTncPbX"
				},
				{
					"type": "arrow",
					"id": "gPWN9ADF"
				},
				{
					"type": "arrow",
					"id": "yy4pDNDN"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1u"
		},
		{
			"id": "meDHCqSC",
			"type": "text",
			"x": 407,
			"y": -729.75,
			"width": 172,
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
			"seed": 733530200,
			"version": 2,
			"versionNonce": 214728984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q2 取出一部分",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rzChspnr",
			"originalText": "Q2 取出一部分",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1v"
		},
		{
			"id": "nUyeZcxP",
			"type": "rectangle",
			"x": 675,
			"y": -965,
			"width": 68,
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
			"seed": 1953934657,
			"version": 2,
			"versionNonce": 1426701416,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mkhjaDx7"
				},
				{
					"type": "arrow",
					"id": "n6ejuY4u"
				},
				{
					"type": "arrow",
					"id": "SVU2xjqw"
				},
				{
					"type": "arrow",
					"id": "4TjxB65e"
				},
				{
					"type": "arrow",
					"id": "RGiv2AF7"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1w"
		},
		{
			"id": "mkhjaDx7",
			"type": "text",
			"x": 689,
			"y": -956,
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
			"seed": 655877316,
			"version": 2,
			"versionNonce": 650944024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "索引",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nUyeZcxP",
			"originalText": "索引",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1x"
		},
		{
			"id": "X66LemQP",
			"type": "rectangle",
			"x": 803,
			"y": -1019.15,
			"width": 323,
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
			"seed": 468497525,
			"version": 2,
			"versionNonce": 1885728616,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "sqEBiBBz"
				},
				{
					"type": "arrow",
					"id": "SVU2xjqw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b1y"
		},
		{
			"id": "sqEBiBBz",
			"type": "text",
			"x": 815,
			"y": -1012.15,
			"width": 299,
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
			"seed": 362658119,
			"version": 2,
			"versionNonce": 616635160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"Campus\"[0] → C；[-1] → s；len → 6",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "X66LemQP",
			"originalText": "\"Campus\"[0] → C；[-1] → s；len → 6",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b1z"
		},
		{
			"id": "iqR858F6",
			"type": "rectangle",
			"x": 803,
			"y": -971.15,
			"width": 197,
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
			"seed": 1314089879,
			"version": 2,
			"versionNonce": 1472447080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nzuhqPRh"
				},
				{
					"type": "arrow",
					"id": "4TjxB65e"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b20"
		},
		{
			"id": "nzuhqPRh",
			"type": "text",
			"x": 815,
			"y": -964.15,
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
			"seed": 1037383964,
			"version": 2,
			"versionNonce": 1226700824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "最後一個索引是 len - 1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iqR858F6",
			"originalText": "最後一個索引是 len - 1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b21"
		},
		{
			"id": "KBjZYJNT",
			"type": "rectangle",
			"x": 803,
			"y": -904.35,
			"width": 317,
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
				"BRAbXeCU"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 647503752,
			"version": 2,
			"versionNonce": 1508849000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CeyBy3tS"
				},
				{
					"type": "arrow",
					"id": "RGiv2AF7"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b22"
		},
		{
			"id": "CeyBy3tS",
			"type": "text",
			"x": 815,
			"y": -897.35,
			"width": 293,
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
				"BRAbXeCU"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1043999168,
			"version": 2,
			"versionNonce": 1742157080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ \"Campus\"[6]、\"\"[0] → IndexError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KBjZYJNT",
			"originalText": "⚠ \"Campus\"[6]、\"\"[0] → IndexError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b23"
		},
		{
			"id": "BX7hcRLq",
			"type": "rectangle",
			"x": 675,
			"y": -802.2,
			"width": 364,
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
				"xLCbYxGK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1331294611,
			"version": 2,
			"versionNonce": 204753000,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FVsbWwhB"
				},
				{
					"type": "arrow",
					"id": "gkTncPbX"
				},
				{
					"type": "arrow",
					"id": "6K4trHGq"
				},
				{
					"type": "arrow",
					"id": "QqwNj7VQ"
				},
				{
					"type": "arrow",
					"id": "AVDnDReG"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b24"
		},
		{
			"id": "FVsbWwhB",
			"type": "text",
			"x": 689,
			"y": -793.2,
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
				"xLCbYxGK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 245885569,
			"version": 2,
			"versionNonce": 912314904,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "切片 [start:stop:step]（含頭不含尾）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BX7hcRLq",
			"originalText": "切片 [start:stop:step]（含頭不含尾）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b25"
		},
		{
			"id": "29Ae9K7T",
			"type": "rectangle",
			"x": 1099,
			"y": -856.35,
			"width": 333,
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
			"seed": 2066581084,
			"version": 2,
			"versionNonce": 2053045096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bAaNbtJL"
				},
				{
					"type": "arrow",
					"id": "6K4trHGq"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b26"
		},
		{
			"id": "bAaNbtJL",
			"type": "text",
			"x": 1111,
			"y": -849.35,
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
			"seed": 832556432,
			"version": 2,
			"versionNonce": 464441112,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "[1:4] → amp；[:3] → Cam；[3:] → pus",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "29Ae9K7T",
			"originalText": "[1:4] → amp；[:3] → Cam；[3:] → pus",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b27"
		},
		{
			"id": "QWi2kQyd",
			"type": "rectangle",
			"x": 1099,
			"y": -789.55,
			"width": 373,
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
				"tT9hJXvR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1146422229,
			"version": 2,
			"versionNonce": 1455115880,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cbfWU6hG"
				},
				{
					"type": "arrow",
					"id": "QqwNj7VQ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b28"
		},
		{
			"id": "cbfWU6hG",
			"type": "text",
			"x": 1111,
			"y": -782.55,
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
			"groupIds": [
				"tT9hJXvR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 152958063,
			"version": 2,
			"versionNonce": 3484696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "[3:3] → \"\"；[1:100] → ampus（越界不報錯）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QWi2kQyd",
			"originalText": "[3:3] → \"\"；[1:100] → ampus（越界不報錯）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b29"
		},
		{
			"id": "J2tCnkN3",
			"type": "rectangle",
			"x": 1099,
			"y": -741.55,
			"width": 375,
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
			"seed": 819222120,
			"version": 2,
			"versionNonce": 706036072,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fEs5sPTe"
				},
				{
					"type": "arrow",
					"id": "AVDnDReG"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2A"
		},
		{
			"id": "fEs5sPTe",
			"type": "text",
			"x": 1111,
			"y": -734.55,
			"width": 351,
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
			"seed": 1713256798,
			"version": 2,
			"versionNonce": 501737752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "[-3:] → pus；[::2] → Cmu；[::-1] → supmaC",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "J2tCnkN3",
			"originalText": "[-3:] → pus；[::2] → Cmu；[::-1] → supmaC",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2B"
		},
		{
			"id": "FrKFeCUw",
			"type": "rectangle",
			"x": 675,
			"y": -639.4,
			"width": 128,
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
			"seed": 1673316383,
			"version": 2,
			"versionNonce": 62444648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wrfjgzNu"
				},
				{
					"type": "arrow",
					"id": "gPWN9ADF"
				},
				{
					"type": "arrow",
					"id": "w9cY9Vn8"
				},
				{
					"type": "arrow",
					"id": "nfwqJF3j"
				},
				{
					"type": "arrow",
					"id": "znz28Ptw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2C"
		},
		{
			"id": "wrfjgzNu",
			"type": "text",
			"x": 689,
			"y": -630.4,
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
			"seed": 421122755,
			"version": 2,
			"versionNonce": 1346045464,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "find 找邊界",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FrKFeCUw",
			"originalText": "find 找邊界",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2D"
		},
		{
			"id": "qQyZGAzQ",
			"type": "rectangle",
			"x": 863,
			"y": -693.55,
			"width": 433,
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
			"seed": 874773347,
			"version": 2,
			"versionNonce": 695338856,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5MPErC8h"
				},
				{
					"type": "arrow",
					"id": "w9cY9Vn8"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2E"
		},
		{
			"id": "5MPErC8h",
			"type": "text",
			"x": 875,
			"y": -686.55,
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
			"seed": 664294416,
			"version": 2,
			"versionNonce": 1679983384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"Campus,12.5,45\".find(\",\") → 6 → line[:6] → Campus",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qQyZGAzQ",
			"originalText": "\"Campus,12.5,45\".find(\",\") → 6 → line[:6] → Campus",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2F"
		},
		{
			"id": "aepWVLM7",
			"type": "rectangle",
			"x": 863,
			"y": -645.55,
			"width": 121,
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
			"seed": 1581008583,
			"version": 2,
			"versionNonce": 1200413288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XeDG8UgR"
				},
				{
					"type": "arrow",
					"id": "nfwqJF3j"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2G"
		},
		{
			"id": "XeDG8UgR",
			"type": "text",
			"x": 875,
			"y": -638.55,
			"width": 97,
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
			"seed": 1020419933,
			"version": 2,
			"versionNonce": 1746034712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "找不到 → −1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aepWVLM7",
			"originalText": "找不到 → −1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2H"
		},
		{
			"id": "4M2ZiCLG",
			"type": "rectangle",
			"x": 863,
			"y": -578.75,
			"width": 423,
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
				"hB5nVRx6"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 954137889,
			"version": 2,
			"versionNonce": 550849896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uZi2Gh8v"
				},
				{
					"type": "arrow",
					"id": "znz28Ptw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2I"
		},
		{
			"id": "uZi2Gh8v",
			"type": "text",
			"x": 875,
			"y": -571.75,
			"width": 399,
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
				"hB5nVRx6"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1303863292,
			"version": 2,
			"versionNonce": 2080283928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 直接 line[:-1] 會丟最後一字（Campus → Campu）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4M2ZiCLG",
			"originalText": "⚠ 直接 line[:-1] 會丟最後一字（Campus → Campu）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2J"
		},
		{
			"id": "25nnVhYv",
			"type": "rectangle",
			"x": 675,
			"y": -505,
			"width": 195,
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
			"seed": 1714201831,
			"version": 2,
			"versionNonce": 1050108008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ibDXHdZi"
				},
				{
					"type": "arrow",
					"id": "yy4pDNDN"
				},
				{
					"type": "arrow",
					"id": "K4XGNmH3"
				},
				{
					"type": "arrow",
					"id": "CdraHAfZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2K"
		},
		{
			"id": "ibDXHdZi",
			"type": "text",
			"x": 689,
			"y": -496,
			"width": 167,
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
			"seed": 2054414637,
			"version": 2,
			"versionNonce": 559626776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab A：TRIP-007",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "25nnVhYv",
			"originalText": "Lab A：TRIP-007",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2L"
		},
		{
			"id": "JFdnPpZ9",
			"type": "rectangle",
			"x": 930,
			"y": -530.75,
			"width": 412,
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
			"seed": 1323585566,
			"version": 2,
			"versionNonce": 547296104,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "T8YQVEM8"
				},
				{
					"type": "arrow",
					"id": "K4XGNmH3"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2M"
		},
		{
			"id": "T8YQVEM8",
			"type": "text",
			"x": 942,
			"y": -523.75,
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
			"seed": 2045445964,
			"version": 2,
			"versionNonce": 186398488,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "len 8；[:4] → TRIP；[-3:] → \"007\"（保留字串）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JFdnPpZ9",
			"originalText": "len 8；[:4] → TRIP；[-3:] → \"007\"（保留字串）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2N"
		},
		{
			"id": "XncZk9eJ",
			"type": "rectangle",
			"x": 930,
			"y": -482.75,
			"width": 438,
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
			"seed": 2134803069,
			"version": 2,
			"versionNonce": 1832412776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UVUtt8mg"
				},
				{
					"type": "arrow",
					"id": "CdraHAfZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2O"
		},
		{
			"id": "UVUtt8mg",
			"type": "text",
			"x": 942,
			"y": -475.75,
			"width": 414,
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
			"seed": 1354975722,
			"version": 2,
			"versionNonce": 1840616472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "tag[4:4] → \"\"；tag[:100] → 全部；⚠ tag[len(tag)]\n→ IndexError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XncZk9eJ",
			"originalText": "tag[4:4] → \"\"；tag[:100] → 全部；⚠ tag[len(tag)]\n→ IndexError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2P"
		},
		{
			"id": "AeWWH69P",
			"type": "rectangle",
			"x": 387,
			"y": 1.48,
			"width": 210,
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
			"seed": 1777439067,
			"version": 2,
			"versionNonce": 556751208,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XzTcpWG6"
				},
				{
					"type": "arrow",
					"id": "CXbKBTFH"
				},
				{
					"type": "arrow",
					"id": "2QaDKMy6"
				},
				{
					"type": "arrow",
					"id": "fB8AwVfj"
				},
				{
					"type": "arrow",
					"id": "b63BPFQT"
				},
				{
					"type": "arrow",
					"id": "mGP5wHuL"
				},
				{
					"type": "arrow",
					"id": "9jTtdhcD"
				},
				{
					"type": "arrow",
					"id": "NzDvjaUE"
				},
				{
					"type": "arrow",
					"id": "WStMCjvk"
				},
				{
					"type": "arrow",
					"id": "pMKid5BG"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2Q"
		},
		{
			"id": "XzTcpWG6",
			"type": "text",
			"x": 407,
			"y": 13.48,
			"width": 170,
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
			"seed": 44184569,
			"version": 2,
			"versionNonce": 1327190296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q3 檢查與轉換",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AeWWH69P",
			"originalText": "Q3 檢查與轉換",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2R"
		},
		{
			"id": "yzWByTZh",
			"type": "rectangle",
			"x": 673,
			"y": -365.95,
			"width": 389,
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
				"YNsJFqPu"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1985639071,
			"version": 2,
			"versionNonce": 1070591080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FuJqs83H"
				},
				{
					"type": "arrow",
					"id": "2QaDKMy6"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2S"
		},
		{
			"id": "FuJqs83H",
			"type": "text",
			"x": 687,
			"y": -356.95,
			"width": 361,
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
				"YNsJFqPu"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1256755449,
			"version": 2,
			"versionNonce": 1455517208,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "走訪：for ch in \"Route 007\" 數字元 → 3",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yzWByTZh",
			"originalText": "走訪：for ch in \"Route 007\" 數字元 → 3",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2T"
		},
		{
			"id": "gYujgzcS",
			"type": "rectangle",
			"x": 673,
			"y": -292.65,
			"width": 354,
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
				"E4s9tMes"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1679442319,
			"version": 2,
			"versionNonce": 48635752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RazDjSLi"
				},
				{
					"type": "arrow",
					"id": "fB8AwVfj"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2U"
		},
		{
			"id": "RazDjSLi",
			"type": "text",
			"x": 687,
			"y": -283.65,
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
			"groupIds": [
				"E4s9tMes"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1618907941,
			"version": 2,
			"versionNonce": 496757528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ \"aaaa\".count(\"aa\") → 2（不重疊）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gYujgzcS",
			"originalText": "⚠ \"aaaa\".count(\"aa\") → 2（不重疊）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2V"
		},
		{
			"id": "cBBTPS8Z",
			"type": "rectangle",
			"x": 673,
			"y": -169.4,
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
			"seed": 425648275,
			"version": 2,
			"versionNonce": 180220520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "NLZEFmbu"
				},
				{
					"type": "arrow",
					"id": "b63BPFQT"
				},
				{
					"type": "arrow",
					"id": "Y6rudwAj"
				},
				{
					"type": "arrow",
					"id": "G9XtMWwc"
				},
				{
					"type": "arrow",
					"id": "Zp8sAdWg"
				},
				{
					"type": "arrow",
					"id": "QUUi9CkC"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2W"
		},
		{
			"id": "NLZEFmbu",
			"type": "text",
			"x": 687,
			"y": -160.4,
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
			"seed": 767569142,
			"version": 2,
			"versionNonce": 2115946520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "四種問題",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cBBTPS8Z",
			"originalText": "四種問題",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2X"
		},
		{
			"id": "mmPF6ba8",
			"type": "rectangle",
			"x": 838,
			"y": -238.15,
			"width": 144,
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
			"seed": 1699362487,
			"version": 2,
			"versionNonce": 237200744,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iT4n9iTe"
				},
				{
					"type": "arrow",
					"id": "Y6rudwAj"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2Y"
		},
		{
			"id": "iT4n9iTe",
			"type": "text",
			"x": 850,
			"y": -231.15,
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
			"seed": 1170912770,
			"version": 2,
			"versionNonce": 1681786136,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "==：整個相等？",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mmPF6ba8",
			"originalText": "==：整個相等？",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2Z"
		},
		{
			"id": "jFLhiFdn",
			"type": "rectangle",
			"x": 838,
			"y": -190.15,
			"width": 155,
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
			"seed": 597707008,
			"version": 2,
			"versionNonce": 174225512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "szhb75Nm"
				},
				{
					"type": "arrow",
					"id": "G9XtMWwc"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2a"
		},
		{
			"id": "szhb75Nm",
			"type": "text",
			"x": 850,
			"y": -183.15,
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
			"seed": 381897125,
			"version": 2,
			"versionNonce": 493724184,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "in：有沒有出現？",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jFLhiFdn",
			"originalText": "in：有沒有出現？",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2b"
		},
		{
			"id": "96aXrGTC",
			"type": "rectangle",
			"x": 838,
			"y": -142.15,
			"width": 234,
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
			"seed": 902061006,
			"version": 2,
			"versionNonce": 1934044008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cEsmVwgn"
				},
				{
					"type": "arrow",
					"id": "Zp8sAdWg"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2c"
		},
		{
			"id": "cEsmVwgn",
			"type": "text",
			"x": 850,
			"y": -135.15,
			"width": 210,
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
			"seed": 1239744685,
			"version": 2,
			"versionNonce": 681680664,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "find：在哪？（沒有 → −1）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "96aXrGTC",
			"originalText": "find：在哪？（沒有 → −1）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2d"
		},
		{
			"id": "VJRKMGUP",
			"type": "rectangle",
			"x": 838,
			"y": -94.15,
			"width": 196,
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
			"seed": 1473675364,
			"version": 2,
			"versionNonce": 1662877288,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TRj2JEZC"
				},
				{
					"type": "arrow",
					"id": "QUUi9CkC"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2e"
		},
		{
			"id": "TRj2JEZC",
			"type": "text",
			"x": 850,
			"y": -87.15,
			"width": 172,
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
			"seed": 266877505,
			"version": 2,
			"versionNonce": 105774104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "startswith：在開頭？",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VJRKMGUP",
			"originalText": "startswith：在開頭？",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2f"
		},
		{
			"id": "5hgN3QNp",
			"type": "rectangle",
			"x": 673,
			"y": -27.35,
			"width": 420,
			"height": 63,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"gKzE4nxH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 139380782,
			"version": 2,
			"versionNonce": 1253142888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iG6fgBnD"
				},
				{
					"type": "arrow",
					"id": "mGP5wHuL"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2g"
		},
		{
			"id": "iG6fgBnD",
			"type": "text",
			"x": 687,
			"y": -18.35,
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
				"gKzE4nxH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 804475487,
			"version": 2,
			"versionNonce": 140949784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ 不要 if label.find(\"Campus\"):：找到在 0 →\nFalse，找不到 −1 → True",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5hgN3QNp",
			"originalText": "⚠ 不要 if label.find(\"Campus\"):：找到在 0 →\nFalse，找不到 −1 → True",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2h"
		},
		{
			"id": "YhH2AXNQ",
			"type": "rectangle",
			"x": 673,
			"y": 68.45,
			"width": 429,
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
				"nTuDSzFn"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 820471511,
			"version": 2,
			"versionNonce": 558826600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3NdnUjR3"
				},
				{
					"type": "arrow",
					"id": "9jTtdhcD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2i"
		},
		{
			"id": "3NdnUjR3",
			"type": "text",
			"x": 687,
			"y": 77.45,
			"width": 401,
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
				"nTuDSzFn"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1284250260,
			"version": 2,
			"versionNonce": 576706072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "strip() 只去兩端；replace(\" \", \"\") 會把 Campus\nEast 變 CampusEast ✗",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YhH2AXNQ",
			"originalText": "strip() 只去兩端；replace(\" \", \"\") 會把 Campus\nEast 變 CampusEast ✗",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2j"
		},
		{
			"id": "G5M3GR3Q",
			"type": "rectangle",
			"x": 673,
			"y": 171,
			"width": 396,
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
			"seed": 183869660,
			"version": 2,
			"versionNonce": 348272488,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tgk3V249"
				},
				{
					"type": "arrow",
					"id": "NzDvjaUE"
				},
				{
					"type": "arrow",
					"id": "Hzy855sx"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2k"
		},
		{
			"id": "tgk3V249",
			"type": "text",
			"x": 687,
			"y": 180,
			"width": 368,
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
			"seed": 1875819709,
			"version": 2,
			"versionNonce": 959271704,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "比較鍵（lower()、upper()）與顯示資料分開",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G5M3GR3Q",
			"originalText": "比較鍵（lower()、upper()）與顯示資料分開",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2l"
		},
		{
			"id": "G9iU6Bhk",
			"type": "rectangle",
			"x": 1129,
			"y": 164.25,
			"width": 428,
			"height": 54,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"u73627NZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 839985788,
			"version": 2,
			"versionNonce": 962005608,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Zd54BKZv"
				},
				{
					"type": "arrow",
					"id": "Hzy855sx"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2m"
		},
		{
			"id": "Zd54BKZv",
			"type": "text",
			"x": 1141,
			"y": 171.25,
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
			"groupIds": [
				"u73627NZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1804560012,
			"version": 2,
			"versionNonce": 1933783064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "casefold() 可能改變字數：\"ß\".casefold() → \"ss\"，只\n拿來當比較鍵",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "G9iU6Bhk",
			"originalText": "casefold() 可能改變字數：\"ß\".casefold() → \"ss\"，只\n拿來當比較鍵",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2n"
		},
		{
			"id": "ZBaNJCau",
			"type": "rectangle",
			"x": 673,
			"y": 253,
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
				"sjbNaEXp"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 559621040,
			"version": 2,
			"versionNonce": 970554728,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MhRzLTPN"
				},
				{
					"type": "arrow",
					"id": "WStMCjvk"
				},
				{
					"type": "arrow",
					"id": "XX5hzjtJ"
				},
				{
					"type": "arrow",
					"id": "HmBXMraq"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2o"
		},
		{
			"id": "MhRzLTPN",
			"type": "text",
			"x": 687,
			"y": 262,
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
				"sjbNaEXp"
			],
			"frameId": null,
			"roundness": null,
			"seed": 986351999,
			"version": 2,
			"versionNonce": 144010520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "結束命令：整行相等才停",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZBaNJCau",
			"originalText": "結束命令：整行相等才停",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2p"
		},
		{
			"id": "eJHFaU4Q",
			"type": "rectangle",
			"x": 967,
			"y": 232.25,
			"width": 179,
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
			"seed": 1864247974,
			"version": 2,
			"versionNonce": 127242344,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6n7gaBLD"
				},
				{
					"type": "arrow",
					"id": "XX5hzjtJ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2q"
		},
		{
			"id": "6n7gaBLD",
			"type": "text",
			"x": 979,
			"y": 239.25,
			"width": 155,
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
			"seed": 818267606,
			"version": 2,
			"versionNonce": 311953944,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "DONE、dOnE → 停",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "eJHFaU4Q",
			"originalText": "DONE、dOnE → 停",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2r"
		},
		{
			"id": "u4VqzVCk",
			"type": "rectangle",
			"x": 967,
			"y": 280.25,
			"width": 305,
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
			"seed": 1633919605,
			"version": 2,
			"versionNonce": 173491048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "F7LsV6em"
				},
				{
					"type": "arrow",
					"id": "HmBXMraq"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2s"
		},
		{
			"id": "F7LsV6em",
			"type": "text",
			"x": 979,
			"y": 287.25,
			"width": 281,
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
			"seed": 1629368649,
			"version": 2,
			"versionNonce": 1547634456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Donegal,1,30、DONE,1,30 → 是資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "u4VqzVCk",
			"originalText": "Donegal,1,30、DONE,1,30 → 是資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2t"
		},
		{
			"id": "D5FRgnjs",
			"type": "rectangle",
			"x": 673,
			"y": 382.4,
			"width": 160,
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
				"6LJtDwer"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1650413909,
			"version": 2,
			"versionNonce": 1349162600,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "mptwpg49"
				},
				{
					"type": "arrow",
					"id": "pMKid5BG"
				},
				{
					"type": "arrow",
					"id": "gWydKbgX"
				},
				{
					"type": "arrow",
					"id": "Gfc3U69P"
				},
				{
					"type": "arrow",
					"id": "8ahK7Bci"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2u"
		},
		{
			"id": "mptwpg49",
			"type": "text",
			"x": 687,
			"y": 391.4,
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
			"groupIds": [
				"6LJtDwer"
			],
			"frameId": null,
			"roundness": null,
			"seed": 982281490,
			"version": 2,
			"versionNonce": 838755352,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "方法回傳新字串",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "D5FRgnjs",
			"originalText": "方法回傳新字串",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2v"
		},
		{
			"id": "ayLziZxj",
			"type": "rectangle",
			"x": 893,
			"y": 328.25,
			"width": 256,
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
			"seed": 1761985189,
			"version": 2,
			"versionNonce": 1050380648,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BUmKf3TN"
				},
				{
					"type": "arrow",
					"id": "gWydKbgX"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2w"
		},
		{
			"id": "BUmKf3TN",
			"type": "text",
			"x": 905,
			"y": 335.25,
			"width": 232,
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
			"seed": 659865589,
			"version": 2,
			"versionNonce": 835330328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "s.replace(...) 沒指派 → s 不變",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ayLziZxj",
			"originalText": "s.replace(...) 沒指派 → s 不變",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2x"
		},
		{
			"id": "YcduKesH",
			"type": "rectangle",
			"x": 893,
			"y": 376.25,
			"width": 209,
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
			"seed": 731787197,
			"version": 2,
			"versionNonce": 1077288040,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eRbtvPpU"
				},
				{
					"type": "arrow",
					"id": "Gfc3U69P"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b2y"
		},
		{
			"id": "eRbtvPpU",
			"type": "text",
			"x": 905,
			"y": 383.25,
			"width": 185,
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
			"seed": 503356034,
			"version": 2,
			"versionNonce": 454442520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "s = s.replace(...) 才重綁",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YcduKesH",
			"originalText": "s = s.replace(...) 才重綁",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b2z"
		},
		{
			"id": "MiXL2SK4",
			"type": "rectangle",
			"x": 893,
			"y": 443.05,
			"width": 237,
			"height": 34,
			"angle": 0,
			"strokeColor": "#6741d9",
			"backgroundColor": "#ffc9c9",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"7KzUyEbk"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 359436159,
			"version": 2,
			"versionNonce": 1996902248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XekVgi3t"
				},
				{
					"type": "arrow",
					"id": "8ahK7Bci"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b30"
		},
		{
			"id": "XekVgi3t",
			"type": "text",
			"x": 905,
			"y": 450.05,
			"width": 213,
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
				"7KzUyEbk"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1959963291,
			"version": 2,
			"versionNonce": 517389080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ s[0] = \"c\" → TypeError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MiXL2SK4",
			"originalText": "⚠ s[0] = \"c\" → TypeError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b31"
		},
		{
			"id": "nWYNg3RQ",
			"type": "rectangle",
			"x": 387,
			"y": 1141,
			"width": 259,
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
			"seed": 1546787465,
			"version": 2,
			"versionNonce": 1800938088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fNfHdKkL"
				},
				{
					"type": "arrow",
					"id": "ZXekJBiT"
				},
				{
					"type": "arrow",
					"id": "EnHwsfFs"
				},
				{
					"type": "arrow",
					"id": "FT6TdDZ9"
				},
				{
					"type": "arrow",
					"id": "pJ6ZiMBK"
				},
				{
					"type": "arrow",
					"id": "nuXCzpby"
				},
				{
					"type": "arrow",
					"id": "QkHmQyJm"
				},
				{
					"type": "arrow",
					"id": "8JDQyJFf"
				},
				{
					"type": "arrow",
					"id": "Ki8p3WqU"
				},
				{
					"type": "arrow",
					"id": "ZYZpJaTz"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b32"
		},
		{
			"id": "fNfHdKkL",
			"type": "text",
			"x": 407,
			"y": 1153,
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
			"seed": 263500275,
			"version": 2,
			"versionNonce": 796891160,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q4 一行解析成欄位",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nWYNg3RQ",
			"originalText": "Q4 一行解析成欄位",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b33"
		},
		{
			"id": "aUmPYWeQ",
			"type": "rectangle",
			"x": 722,
			"y": 606.75,
			"width": 438,
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
				"qpscKJVd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 535582562,
			"version": 2,
			"versionNonce": 1006081384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hiPG8WLk"
				},
				{
					"type": "arrow",
					"id": "EnHwsfFs"
				},
				{
					"type": "arrow",
					"id": "EN4CGn5r"
				},
				{
					"type": "arrow",
					"id": "CpsVAGUW"
				},
				{
					"type": "arrow",
					"id": "BUhfXAzR"
				},
				{
					"type": "arrow",
					"id": "t6fncGCW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b34"
		},
		{
			"id": "hiPG8WLk",
			"type": "text",
			"x": 736,
			"y": 615.75,
			"width": 410,
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
				"qpscKJVd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 931787493,
			"version": 2,
			"versionNonce": 1359271192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "split(\",\") → 字串 list：['Campus East', ' 12.5', '\n45']",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aUmPYWeQ",
			"originalText": "split(\",\") → 字串 list：['Campus East', ' 12.5', '\n45']",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b35"
		},
		{
			"id": "Mu4pDgRz",
			"type": "rectangle",
			"x": 1220,
			"y": 539.85,
			"width": 307,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"s6CsVw5h"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 623980913,
			"version": 2,
			"versionNonce": 1311811688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5MwebH8S"
				},
				{
					"type": "arrow",
					"id": "EN4CGn5r"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b36"
		},
		{
			"id": "5MwebH8S",
			"type": "text",
			"x": 1232,
			"y": 546.85,
			"width": 283,
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
				"s6CsVw5h"
			],
			"frameId": null,
			"roundness": null,
			"seed": 78775968,
			"version": 2,
			"versionNonce": 1759146520,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "每一項仍是字串；數字欄前的空白還在",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Mu4pDgRz",
			"originalText": "每一項仍是字串；數字欄前的空白還在",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b37"
		},
		{
			"id": "SkFVY7Vm",
			"type": "rectangle",
			"x": 1220,
			"y": 587.85,
			"width": 275,
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
			"seed": 2037029960,
			"version": 2,
			"versionNonce": 2110741352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EiASvnRA"
				},
				{
					"type": "arrow",
					"id": "CpsVAGUW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b38"
		},
		{
			"id": "EiASvnRA",
			"type": "text",
			"x": 1232,
			"y": 594.85,
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
			"seed": 1009343118,
			"version": 2,
			"versionNonce": 234123032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "fields[0] 是欄位；line[0] 是字元",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SkFVY7Vm",
			"originalText": "fields[0] 是欄位；line[0] 是字元",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b39"
		},
		{
			"id": "r2xjH2Pf",
			"type": "rectangle",
			"x": 1220,
			"y": 635.85,
			"width": 396,
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
			"seed": 932535845,
			"version": 2,
			"versionNonce": 1293921896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Z5SrWYXE"
				},
				{
					"type": "arrow",
					"id": "BUhfXAzR"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3A"
		},
		{
			"id": "Z5SrWYXE",
			"type": "text",
			"x": 1232,
			"y": 642.85,
			"width": 372,
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
			"seed": 1765898120,
			"version": 2,
			"versionNonce": 1489423384,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ split() 無參數依空白切，會拆開 Campus East",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "r2xjH2Pf",
			"originalText": "⚠ split() 無參數依空白切，會拆開 Campus East",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3B"
		},
		{
			"id": "4WSzuRrb",
			"type": "rectangle",
			"x": 1220,
			"y": 702.65,
			"width": 375,
			"height": 34,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"9hU8SGdd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1162747217,
			"version": 2,
			"versionNonce": 351117672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XMHLe2zB"
				},
				{
					"type": "arrow",
					"id": "t6fncGCW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3C"
		},
		{
			"id": "XMHLe2zB",
			"type": "text",
			"x": 1232,
			"y": 709.65,
			"width": 351,
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
				"9hU8SGdd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 123293094,
			"version": 2,
			"versionNonce": 860195096,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "保留空欄位：Campus,,45 → ['Campus', '', '45']",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4WSzuRrb",
			"originalText": "保留空欄位：Campus,,45 → ['Campus', '', '45']",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3D"
		},
		{
			"id": "QiDacq4S",
			"type": "rectangle",
			"x": 722,
			"y": 776.2,
			"width": 455,
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
			"seed": 1367164199,
			"version": 2,
			"versionNonce": 881144936,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6ywe8Rku"
				},
				{
					"type": "arrow",
					"id": "FT6TdDZ9"
				},
				{
					"type": "arrow",
					"id": "ixiEA6BC"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3E"
		},
		{
			"id": "6ywe8Rku",
			"type": "text",
			"x": 736,
			"y": 785.2,
			"width": 427,
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
			"seed": 499547812,
			"version": 2,
			"versionNonce": 686073368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "先檢查形狀：len(fields) != 3 → 印錯誤、continue",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QiDacq4S",
			"originalText": "先檢查形狀：len(fields) != 3 → 印錯誤、continue",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3F"
		},
		{
			"id": "Z7UYKR7k",
			"type": "rectangle",
			"x": 1237,
			"y": 769.45,
			"width": 390,
			"height": 54,
			"angle": 0,
			"strokeColor": "#0c8599",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"ER8Kasaz"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 169649652,
			"version": 2,
			"versionNonce": 1102210920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "36ykCyJP"
				},
				{
					"type": "arrow",
					"id": "ixiEA6BC"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3G"
		},
		{
			"id": "36ykCyJP",
			"type": "text",
			"x": 1249,
			"y": 776.45,
			"width": 366,
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
				"ER8Kasaz"
			],
			"frameId": null,
			"roundness": null,
			"seed": 816195982,
			"version": 2,
			"versionNonce": 915940120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "形狀對 ≠ 數值能轉：len(fields) == 3 之後仍可能\nValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Z7UYKR7k",
			"originalText": "形狀對 ≠ 數值能轉：len(fields) == 3 之後仍可能\nValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3H"
		},
		{
			"id": "wSkBJTvA",
			"type": "rectangle",
			"x": 722,
			"y": 954.2,
			"width": 272,
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
				"9TSU4gk6"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1352834849,
			"version": 2,
			"versionNonce": 952187496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "beaMARKA"
				},
				{
					"type": "arrow",
					"id": "pJ6ZiMBK"
				},
				{
					"type": "arrow",
					"id": "3YjEHdCr"
				},
				{
					"type": "arrow",
					"id": "Ug4gch9w"
				},
				{
					"type": "arrow",
					"id": "F5sLDDb8"
				},
				{
					"type": "arrow",
					"id": "FpzLbpdP"
				},
				{
					"type": "arrow",
					"id": "C7gwbzGr"
				},
				{
					"type": "arrow",
					"id": "RhKfqHeL"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3I"
		},
		{
			"id": "beaMARKA",
			"type": "text",
			"x": 736,
			"y": 963.2,
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
				"9TSU4gk6"
			],
			"frameId": null,
			"roundness": null,
			"seed": 801201053,
			"version": 2,
			"versionNonce": 450101272,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "拒絕階段（第一個失敗就停）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wSkBJTvA",
			"originalText": "拒絕階段（第一個失敗就停）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3J"
		},
		{
			"id": "cEX8UWFk",
			"type": "rectangle",
			"x": 1054,
			"y": 837.45,
			"width": 106,
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
			"seed": 1947910232,
			"version": 2,
			"versionNonce": 746433896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "f85MddZC"
				},
				{
					"type": "arrow",
					"id": "3YjEHdCr"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3K"
		},
		{
			"id": "f85MddZC",
			"type": "text",
			"x": 1066,
			"y": 844.45,
			"width": 82,
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
			"seed": 1013872091,
			"version": 2,
			"versionNonce": 629947672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "1 整行命令",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cEX8UWFk",
			"originalText": "1 整行命令",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3L"
		},
		{
			"id": "FpfWyHQi",
			"type": "rectangle",
			"x": 1054,
			"y": 885.45,
			"width": 231,
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
			"seed": 1452424939,
			"version": 2,
			"versionNonce": 1983103080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LJVuRgYq"
				},
				{
					"type": "arrow",
					"id": "Ug4gch9w"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3M"
		},
		{
			"id": "LJVuRgYq",
			"type": "text",
			"x": 1066,
			"y": 892.45,
			"width": 207,
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
			"seed": 94211410,
			"version": 2,
			"versionNonce": 137681432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "2–4 空行、雙引號、欄位數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FpfWyHQi",
			"originalText": "2–4 空行、雙引號、欄位數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3N"
		},
		{
			"id": "RvLhUSug",
			"type": "rectangle",
			"x": 1054,
			"y": 933.45,
			"width": 175,
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
			"seed": 1859816889,
			"version": 2,
			"versionNonce": 1705997160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "cXdSR32G"
				},
				{
					"type": "arrow",
					"id": "F5sLDDb8"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3O"
		},
		{
			"id": "cXdSR32G",
			"type": "text",
			"x": 1066,
			"y": 940.45,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1282544814,
			"version": 2,
			"versionNonce": 633460504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "5 去空白後的空標籤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RvLhUSug",
			"originalText": "5 去空白後的空標籤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3P"
		},
		{
			"id": "kiEfe5qu",
			"type": "rectangle",
			"x": 1054,
			"y": 981.45,
			"width": 248,
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
			"seed": 467128515,
			"version": 2,
			"versionNonce": 1899808360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DHjCATqJ"
				},
				{
					"type": "arrow",
					"id": "FpzLbpdP"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3Q"
		},
		{
			"id": "DHjCATqJ",
			"type": "text",
			"x": 1066,
			"y": 988.45,
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
			"seed": 752166329,
			"version": 2,
			"versionNonce": 1655125016,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "6 先 float 距離，再 int 分鐘",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kiEfe5qu",
			"originalText": "6 先 float 距離，再 int 分鐘",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3R"
		},
		{
			"id": "8aVbyFqq",
			"type": "rectangle",
			"x": 1054,
			"y": 1029.45,
			"width": 262,
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
			"seed": 1916890693,
			"version": 2,
			"versionNonce": 1705490792,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iAbNSftM"
				},
				{
					"type": "arrow",
					"id": "C7gwbzGr"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3S"
		},
		{
			"id": "iAbNSftM",
			"type": "text",
			"x": 1066,
			"y": 1036.45,
			"width": 238,
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
			"seed": 60163471,
			"version": 2,
			"versionNonce": 1960374552,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "7–9 非有限、負距離、非正時間",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8aVbyFqq",
			"originalText": "7–9 非有限、負距離、非正時間",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3T"
		},
		{
			"id": "6avnXGSV",
			"type": "rectangle",
			"x": 1054,
			"y": 1077.45,
			"width": 414,
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
			"seed": 670654807,
			"version": 2,
			"versionNonce": 373050472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YXE9GHuW"
				},
				{
					"type": "arrow",
					"id": "RhKfqHeL"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3U"
		},
		{
			"id": "YXE9GHuW",
			"type": "text",
			"x": 1066,
			"y": 1084.45,
			"width": 390,
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
			"seed": 108475793,
			"version": 2,
			"versionNonce": 868945432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,-1,abc → 解析錯誤；Campus,-1,0 → 負距離",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6avnXGSV",
			"originalText": "Campus,-1,abc → 解析錯誤；Campus,-1,0 → 負距離",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3V"
		},
		{
			"id": "SMEesmMJ",
			"type": "rectangle",
			"x": 722,
			"y": 1155.6,
			"width": 459,
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
			"seed": 339917294,
			"version": 2,
			"versionNonce": 214335336,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "C4ENydL5"
				},
				{
					"type": "arrow",
					"id": "nuXCzpby"
				},
				{
					"type": "arrow",
					"id": "qJQQXGaq"
				},
				{
					"type": "arrow",
					"id": "X2q7saXX"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3W"
		},
		{
			"id": "C4ENydL5",
			"type": "text",
			"x": 736,
			"y": 1164.6,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 113885661,
			"version": 2,
			"versionNonce": 1752271640,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "try／except ValueError：只救預期的數值文字錯誤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SMEesmMJ",
			"originalText": "try／except ValueError：只救預期的數值文字錯誤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3X"
		},
		{
			"id": "GXxPbX9Z",
			"type": "rectangle",
			"x": 1241,
			"y": 1125.45,
			"width": 344,
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
			"seed": 2030687872,
			"version": 2,
			"versionNonce": 965890664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DthugVxU"
				},
				{
					"type": "arrow",
					"id": "qJQQXGaq"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3Y"
		},
		{
			"id": "DthugVxU",
			"type": "text",
			"x": 1253,
			"y": 1132.45,
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
			"seed": 919402876,
			"version": 2,
			"versionNonce": 490760216,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ int(\"30.0\")、int(\"30.9\") → ValueError",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GXxPbX9Z",
			"originalText": "⚠ int(\"30.0\")、int(\"30.9\") → ValueError",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3Z"
		},
		{
			"id": "A399VZCt",
			"type": "rectangle",
			"x": 1241,
			"y": 1192.25,
			"width": 326,
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
				"77E8kqML"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 564942751,
			"version": 2,
			"versionNonce": 594265448,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "L7uzJDYk"
				},
				{
					"type": "arrow",
					"id": "X2q7saXX"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3a"
		},
		{
			"id": "L7uzJDYk",
			"type": "text",
			"x": 1253,
			"y": 1199.25,
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
			"groupIds": [
				"77E8kqML"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1147156988,
			"version": 2,
			"versionNonce": 1848354072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ int(float(\"30.9\")) → 30 是偷改資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "A399VZCt",
			"originalText": "⚠ int(float(\"30.9\")) → 30 是偷改資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3b"
		},
		{
			"id": "iBtZS2fT",
			"type": "rectangle",
			"x": 722,
			"y": 1285,
			"width": 146,
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
			"seed": 849713618,
			"version": 2,
			"versionNonce": 396286056,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eRWHVerU"
				},
				{
					"type": "arrow",
					"id": "QkHmQyJm"
				},
				{
					"type": "arrow",
					"id": "PKxDVxsT"
				},
				{
					"type": "arrow",
					"id": "xVQEJqcZ"
				},
				{
					"type": "arrow",
					"id": "FmAdMxgZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3c"
		},
		{
			"id": "eRWHVerU",
			"type": "text",
			"x": 736,
			"y": 1294,
			"width": 118,
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
			"seed": 1568589533,
			"version": 2,
			"versionNonce": 1487356440,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "不是完整 CSV",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "iBtZS2fT",
			"originalText": "不是完整 CSV",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3d"
		},
		{
			"id": "h6fkMSQm",
			"type": "rectangle",
			"x": 928,
			"y": 1240.25,
			"width": 186,
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
			"seed": 847206270,
			"version": 2,
			"versionNonce": 1509395304,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "5TcH3kyr"
				},
				{
					"type": "arrow",
					"id": "PKxDVxsT"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3e"
		},
		{
			"id": "5TcH3kyr",
			"type": "text",
			"x": 940,
			"y": 1247.25,
			"width": 162,
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
			"seed": 254907605,
			"version": 2,
			"versionNonce": 195510040,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,1,45, → 4 欄",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "h6fkMSQm",
			"originalText": "Campus,1,45, → 4 欄",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3f"
		},
		{
			"id": "C8dVD5en",
			"type": "rectangle",
			"x": 928,
			"y": 1288.25,
			"width": 243,
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
			"seed": 225710051,
			"version": 2,
			"versionNonce": 1421991528,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KqbfyqaP"
				},
				{
					"type": "arrow",
					"id": "xVQEJqcZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3g"
		},
		{
			"id": "KqbfyqaP",
			"type": "text",
			"x": 940,
			"y": 1295.25,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1483997247,
			"version": 2,
			"versionNonce": 933207064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"Campus, East\",1,45 → 拒絕",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "C8dVD5en",
			"originalText": "\"Campus, East\",1,45 → 拒絕",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3h"
		},
		{
			"id": "Pfjn7iVq",
			"type": "rectangle",
			"x": 928,
			"y": 1336.25,
			"width": 258,
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
			"seed": 880540656,
			"version": 2,
			"versionNonce": 1221185896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Gck9ZZ8a"
				},
				{
					"type": "arrow",
					"id": "FmAdMxgZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3i"
		},
		{
			"id": "Gck9ZZ8a",
			"type": "text",
			"x": 940,
			"y": 1343.25,
			"width": 234,
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
			"seed": 127734612,
			"version": 2,
			"versionNonce": 1585731864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 不要用 eval 執行使用者輸入",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Pfjn7iVq",
			"originalText": "⚠ 不要用 eval 執行使用者輸入",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3j"
		},
		{
			"id": "mBYFTAsx",
			"type": "rectangle",
			"x": 722,
			"y": 1384.25,
			"width": 430,
			"height": 85.5,
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
			"seed": 66692473,
			"version": 2,
			"versionNonce": 2103141480,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "43ezrfYK"
				},
				{
					"type": "arrow",
					"id": "8JDQyJFf"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3k"
		},
		{
			"id": "43ezrfYK",
			"type": "text",
			"x": 736,
			"y": 1393.25,
			"width": 402,
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
			"seed": 1141758929,
			"version": 2,
			"versionNonce": 600405528,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "舊規則照舊：nan／inf 拒絕；0 km 有效；30\nShort／60 Medium／61 Long；只累加有效；空\nsession 不平均",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mBYFTAsx",
			"originalText": "舊規則照舊：nan／inf 拒絕；0 km 有效；30\nShort／60 Medium／61 Long；只累加有效；空\nsession 不平均",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3l"
		},
		{
			"id": "4JEJJ7kT",
			"type": "rectangle",
			"x": 722,
			"y": 1483.75,
			"width": 429,
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
			"seed": 1875267640,
			"version": 2,
			"versionNonce": 1883412328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VGvVh4TR"
				},
				{
					"type": "arrow",
					"id": "Ki8p3WqU"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3m"
		},
		{
			"id": "VGvVh4TR",
			"type": "text",
			"x": 736,
			"y": 1492.75,
			"width": 401,
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
			"seed": 583097468,
			"version": 2,
			"versionNonce": 476246808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "保留測試：West  Gate（兩個內部空白）、007\n（不是 7）、Donegal、DONE,1,30",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4JEJJ7kT",
			"originalText": "保留測試：West  Gate（兩個內部空白）、007\n（不是 7）、Donegal、DONE,1,30",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3n"
		},
		{
			"id": "SPC2U5xx",
			"type": "rectangle",
			"x": 722,
			"y": 1677.5,
			"width": 81,
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
			"seed": 1462406047,
			"version": 2,
			"versionNonce": 97217128,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SgbxtY6z"
				},
				{
					"type": "arrow",
					"id": "ZYZpJaTz"
				},
				{
					"type": "arrow",
					"id": "tESW9fbQ"
				},
				{
					"type": "arrow",
					"id": "DWqYp9Kg"
				},
				{
					"type": "arrow",
					"id": "7s5yd4AD"
				},
				{
					"type": "arrow",
					"id": "RPZkEzNp"
				},
				{
					"type": "arrow",
					"id": "VsjSxYTA"
				},
				{
					"type": "arrow",
					"id": "jUPV5AjM"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3o"
		},
		{
			"id": "SgbxtY6z",
			"type": "text",
			"x": 736,
			"y": 1686.5,
			"width": 53,
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
			"seed": 1821609664,
			"version": 2,
			"versionNonce": 516214808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Lab C",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SPC2U5xx",
			"originalText": "Lab C",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3p"
		},
		{
			"id": "WRqMxTnA",
			"type": "rectangle",
			"x": 863,
			"y": 1560.75,
			"width": 191,
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
			"seed": 34996970,
			"version": 2,
			"versionNonce": 952229224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Qy9exWxW"
				},
				{
					"type": "arrow",
					"id": "tESW9fbQ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3q"
		},
		{
			"id": "Qy9exWxW",
			"type": "text",
			"x": 875,
			"y": 1567.75,
			"width": 167,
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
			"seed": 1112228507,
			"version": 2,
			"versionNonce": 316869912,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,1 → 欄位數錯",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WRqMxTnA",
			"originalText": "Campus,1 → 欄位數錯",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3r"
		},
		{
			"id": "HwsePN4D",
			"type": "rectangle",
			"x": 863,
			"y": 1608.75,
			"width": 193,
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
			"seed": 1381009900,
			"version": 2,
			"versionNonce": 1248981096,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EdgqvGDq"
				},
				{
					"type": "arrow",
					"id": "DWqYp9Kg"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3s"
		},
		{
			"id": "EdgqvGDq",
			"type": "text",
			"x": 875,
			"y": 1615.75,
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
			"seed": 574056900,
			"version": 2,
			"versionNonce": 1110551064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,,30 → 解析錯",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HwsePN4D",
			"originalText": "Campus,,30 → 解析錯",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3t"
		},
		{
			"id": "fnHcmdkN",
			"type": "rectangle",
			"x": 863,
			"y": 1656.75,
			"width": 162,
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
			"seed": 1194015327,
			"version": 2,
			"versionNonce": 1923588968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Uta4v4Pu"
				},
				{
					"type": "arrow",
					"id": "7s5yd4AD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3u"
		},
		{
			"id": "Uta4v4Pu",
			"type": "text",
			"x": 875,
			"y": 1663.75,
			"width": 138,
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
			"seed": 944279639,
			"version": 2,
			"versionNonce": 665102104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "   ,1,30 → 空標籤",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fnHcmdkN",
			"originalText": "   ,1,30 → 空標籤",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3v"
		},
		{
			"id": "VGnF2hDa",
			"type": "rectangle",
			"x": 863,
			"y": 1704.75,
			"width": 196,
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
			"seed": 1007287982,
			"version": 2,
			"versionNonce": 263124584,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yewn6zin"
				},
				{
					"type": "arrow",
					"id": "RPZkEzNp"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3w"
		},
		{
			"id": "yewn6zin",
			"type": "text",
			"x": 875,
			"y": 1711.75,
			"width": 172,
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
			"seed": 624820621,
			"version": 2,
			"versionNonce": 1068499992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,-1,0 → 負距離",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VGnF2hDa",
			"originalText": "Campus,-1,0 → 負距離",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3x"
		},
		{
			"id": "qhzzYbnq",
			"type": "rectangle",
			"x": 863,
			"y": 1752.75,
			"width": 214,
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
			"seed": 1394740375,
			"version": 2,
			"versionNonce": 1448339816,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "UtdfLhgj"
				},
				{
					"type": "arrow",
					"id": "VsjSxYTA"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b3y"
		},
		{
			"id": "UtdfLhgj",
			"type": "text",
			"x": 875,
			"y": 1759.75,
			"width": 190,
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
			"seed": 464253936,
			"version": 2,
			"versionNonce": 1481097496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,1,30.0 → 解析錯",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qhzzYbnq",
			"originalText": "Campus,1,30.0 → 解析錯",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b3z"
		},
		{
			"id": "qEZQjJr7",
			"type": "rectangle",
			"x": 863,
			"y": 1800.75,
			"width": 146,
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
			"seed": 1106210869,
			"version": 2,
			"versionNonce": 31620200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RNrQdd97"
				},
				{
					"type": "arrow",
					"id": "jUPV5AjM"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b40"
		},
		{
			"id": "RNrQdd97",
			"type": "text",
			"x": 875,
			"y": 1807.75,
			"width": 122,
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
			"seed": 710046536,
			"version": 2,
			"versionNonce": 1625284120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "   done → 停止",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qEZQjJr7",
			"originalText": "   done → 停止",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b41"
		},
		{
			"id": "7B5ujLyJ",
			"type": "rectangle",
			"x": -696,
			"y": -732.45,
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
			"seed": 277599687,
			"version": 2,
			"versionNonce": 69644136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pxtLG4ps"
				},
				{
					"type": "arrow",
					"id": "nMqKfexc"
				},
				{
					"type": "arrow",
					"id": "bVPkj827"
				},
				{
					"type": "arrow",
					"id": "zecP6vbv"
				},
				{
					"type": "arrow",
					"id": "PSSxCBEG"
				},
				{
					"type": "arrow",
					"id": "Xz3GrFbm"
				},
				{
					"type": "arrow",
					"id": "Df2AHMwU"
				},
				{
					"type": "arrow",
					"id": "DeK8BjaZ"
				},
				{
					"type": "arrow",
					"id": "pSq8BzM4"
				},
				{
					"type": "arrow",
					"id": "khxwWcPm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b42"
		},
		{
			"id": "pxtLG4ps",
			"type": "text",
			"x": -676,
			"y": -720.45,
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
			"seed": 451640644,
			"version": 2,
			"versionNonce": 980179736,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q5 字元變位元組並保存",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7B5ujLyJ",
			"originalText": "Q5 字元變位元組並保存",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b43"
		},
		{
			"id": "5m4SYinV",
			"type": "rectangle",
			"x": -1176,
			"y": -1168.9,
			"width": 404,
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
			"seed": 710270933,
			"version": 2,
			"versionNonce": 896303720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YgKitm4j"
				},
				{
					"type": "arrow",
					"id": "bVPkj827"
				},
				{
					"type": "arrow",
					"id": "775iSV7A"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b44"
		},
		{
			"id": "YgKitm4j",
			"type": "text",
			"x": -1162,
			"y": -1159.9,
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
			"seed": 1449685969,
			"version": 2,
			"versionNonce": 123811864,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "ASCII：space 32、\"0\" 48、\"A\" 65、\"a\" 97",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5m4SYinV",
			"originalText": "ASCII：space 32、\"0\" 48、\"A\" 65、\"a\" 97",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b45"
		},
		{
			"id": "EGe2cQbD",
			"type": "rectangle",
			"x": -1580,
			"y": -1165.65,
			"width": 344,
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
			"seed": 576324886,
			"version": 2,
			"versionNonce": 75494760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zPTu5i6b"
				},
				{
					"type": "arrow",
					"id": "775iSV7A"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b46"
		},
		{
			"id": "zPTu5i6b",
			"type": "text",
			"x": -1568,
			"y": -1158.65,
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
			"seed": 436767652,
			"version": 2,
			"versionNonce": 2075292952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 數值 0、字元 \"0\"、代碼 48 是三種角色",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EGe2cQbD",
			"originalText": "⚠ 數值 0、字元 \"0\"、代碼 48 是三種角色",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b47"
		},
		{
			"id": "Uc6SLTXN",
			"type": "rectangle",
			"x": -1209,
			"y": -1023.7,
			"width": 437,
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
			"seed": 1430651139,
			"version": 2,
			"versionNonce": 648874088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Yj2bc7By"
				},
				{
					"type": "arrow",
					"id": "zecP6vbv"
				},
				{
					"type": "arrow",
					"id": "k4KGfwuV"
				},
				{
					"type": "arrow",
					"id": "U58PqwQx"
				},
				{
					"type": "arrow",
					"id": "qrEvjQgu"
				},
				{
					"type": "arrow",
					"id": "VsSqKVsD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b48"
		},
		{
			"id": "Yj2bc7By",
			"type": "text",
			"x": -1195,
			"y": -1014.7,
			"width": 409,
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
			"seed": 960461676,
			"version": 2,
			"versionNonce": 752095768,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Unicode 指定字元（code point）；UTF-8 指定\nbytes",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Uc6SLTXN",
			"originalText": "Unicode 指定字元（code point）；UTF-8 指定\nbytes",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b49"
		},
		{
			"id": "6ayDX3mi",
			"type": "rectangle",
			"x": -1646,
			"y": -1095.6,
			"width": 377,
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
				"zmcS5STN"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1511071170,
			"version": 2,
			"versionNonce": 1203747688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tJwpxyEP"
				},
				{
					"type": "arrow",
					"id": "k4KGfwuV"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4A"
		},
		{
			"id": "tJwpxyEP",
			"type": "text",
			"x": -1634,
			"y": -1088.6,
			"width": 353,
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
				"zmcS5STN"
			],
			"frameId": null,
			"roundness": null,
			"seed": 810250011,
			"version": 2,
			"versionNonce": 1639583512,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"A中\" → 2 個碼位、4 bytes（41 E4 B8 AD）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "6ayDX3mi",
			"originalText": "\"A中\" → 2 個碼位、4 bytes（41 E4 B8 AD）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4B"
		},
		{
			"id": "zRA5fhyA",
			"type": "rectangle",
			"x": -1664,
			"y": -1047.6,
			"width": 395,
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
			"seed": 758433317,
			"version": 2,
			"versionNonce": 973344360,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YYP6hQvA"
				},
				{
					"type": "arrow",
					"id": "U58PqwQx"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4C"
		},
		{
			"id": "YYP6hQvA",
			"type": "text",
			"x": -1652,
			"y": -1040.6,
			"width": 371,
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
			"seed": 838572315,
			"version": 2,
			"versionNonce": 1658350616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "A：1 byte；中：3 bytes；UTF-8 用 1–4 bytes",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zRA5fhyA",
			"originalText": "A：1 byte；中：3 bytes；UTF-8 用 1–4 bytes",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4D"
		},
		{
			"id": "5bidCHGD",
			"type": "rectangle",
			"x": -1551,
			"y": -999.6,
			"width": 282,
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
			"seed": 212481097,
			"version": 2,
			"versionNonce": 642122088,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8q5u39HK"
				},
				{
					"type": "arrow",
					"id": "qrEvjQgu"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4E"
		},
		{
			"id": "8q5u39HK",
			"type": "text",
			"x": -1539,
			"y": -992.6,
			"width": 258,
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
			"seed": 1177538112,
			"version": 2,
			"versionNonce": 1243818264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "encode → bytes；decode → str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5bidCHGD",
			"originalText": "encode → bytes；decode → str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4F"
		},
		{
			"id": "NySmdD8Q",
			"type": "rectangle",
			"x": -1627,
			"y": -932.8,
			"width": 358,
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
				"rEP3DHhN"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1895145098,
			"version": 2,
			"versionNonce": 1003590760,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bH4PWsJt"
				},
				{
					"type": "arrow",
					"id": "VsSqKVsD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4G"
		},
		{
			"id": "bH4PWsJt",
			"type": "text",
			"x": -1615,
			"y": -925.8,
			"width": 334,
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
				"rEP3DHhN"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2096357888,
			"version": 2,
			"versionNonce": 1393444376,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "前兩個 bytes ≠ 前兩個碼位再 encode：\"A中\n\".encode()[:2] → b'A\\xe4'",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NySmdD8Q",
			"originalText": "前兩個 bytes ≠ 前兩個碼位再 encode：\"A中\n\".encode()[:2] → b'A\\xe4'",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4H"
		},
		{
			"id": "nyLHwHQj",
			"type": "rectangle",
			"x": -913,
			"y": -820.05,
			"width": 141,
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
				"iQHC58aC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 239735647,
			"version": 2,
			"versionNonce": 1618134888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tHCxQNZG"
				},
				{
					"type": "arrow",
					"id": "PSSxCBEG"
				},
				{
					"type": "arrow",
					"id": "5hTWpzGD"
				},
				{
					"type": "arrow",
					"id": "WiP3FGtj"
				},
				{
					"type": "arrow",
					"id": "Yy8Pp7g7"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4I"
		},
		{
			"id": "tHCxQNZG",
			"type": "text",
			"x": -899,
			"y": -811.05,
			"width": 113,
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
				"iQHC58aC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 396594542,
			"version": 2,
			"versionNonce": 713933592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "é 的兩種寫法",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nyLHwHQj",
			"originalText": "é 的兩種寫法",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4J"
		},
		{
			"id": "fpgYEqqU",
			"type": "rectangle",
			"x": -1163,
			"y": -864.8,
			"width": 190,
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
			"seed": 1585650711,
			"version": 2,
			"versionNonce": 1618319976,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6dgQSKfV"
				},
				{
					"type": "arrow",
					"id": "5hTWpzGD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4K"
		},
		{
			"id": "6dgQSKfV",
			"type": "text",
			"x": -1151,
			"y": -857.8,
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
			"seed": 1385262626,
			"version": 2,
			"versionNonce": 1058381848,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"é\"：1 碼位、2 bytes",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fpgYEqqU",
			"originalText": "\"é\"：1 碼位、2 bytes",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4L"
		},
		{
			"id": "wB93K76c",
			"type": "rectangle",
			"x": -1166,
			"y": -816.8,
			"width": 193,
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
			"seed": 2124220142,
			"version": 2,
			"versionNonce": 514198888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G243DprA"
				},
				{
					"type": "arrow",
					"id": "WiP3FGtj"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4M"
		},
		{
			"id": "G243DprA",
			"type": "text",
			"x": -1154,
			"y": -809.8,
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
			"seed": 486102894,
			"version": 2,
			"versionNonce": 278519064,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"é\"：2 碼位、3 bytes",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wB93K76c",
			"originalText": "\"é\"：2 碼位、3 bytes",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4N"
		},
		{
			"id": "VyiuRkdd",
			"type": "rectangle",
			"x": -1231,
			"y": -768.8,
			"width": 258,
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
			"seed": 1110314739,
			"version": 2,
			"versionNonce": 1146101864,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EXWDnTvy"
				},
				{
					"type": "arrow",
					"id": "Yy8Pp7g7"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4O"
		},
		{
			"id": "EXWDnTvy",
			"type": "text",
			"x": -1219,
			"y": -761.8,
			"width": 234,
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
			"seed": 1016911292,
			"version": 2,
			"versionNonce": 9337368,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "== → False；len ≠ 看到的字數",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VyiuRkdd",
			"originalText": "== → False；len ≠ 看到的字數",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4P"
		},
		{
			"id": "XvyqeS7Z",
			"type": "rectangle",
			"x": -985,
			"y": -676.05,
			"width": 213,
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
				"TXGJQLZw"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 539908104,
			"version": 2,
			"versionNonce": 1900008296,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CzExKzsV"
				},
				{
					"type": "arrow",
					"id": "Xz3GrFbm"
				},
				{
					"type": "arrow",
					"id": "AwKbFqfU"
				},
				{
					"type": "arrow",
					"id": "NJWbbCWV"
				},
				{
					"type": "arrow",
					"id": "9a3sCaDm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4Q"
		},
		{
			"id": "CzExKzsV",
			"type": "text",
			"x": -971,
			"y": -667.05,
			"width": 185,
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
				"TXGJQLZw"
			],
			"frameId": null,
			"roundness": null,
			"seed": 86492821,
			"version": 2,
			"versionNonce": 568817432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "執行狀態 vs 持久檔案",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XvyqeS7Z",
			"originalText": "執行狀態 vs 持久檔案",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4R"
		},
		{
			"id": "mm2P7EDi",
			"type": "rectangle",
			"x": -1346,
			"y": -720.8,
			"width": 301,
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
			"seed": 1078276936,
			"version": 2,
			"versionNonce": 1807820392,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "BmpgK8au"
				},
				{
					"type": "arrow",
					"id": "AwKbFqfU"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4S"
		},
		{
			"id": "BmpgK8au",
			"type": "text",
			"x": -1334,
			"y": -713.8,
			"width": 277,
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
			"seed": 353609441,
			"version": 2,
			"versionNonce": 152622104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "變數、fields、總和：程式結束就沒了",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mm2P7EDi",
			"originalText": "變數、fields、總和：程式結束就沒了",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4T"
		},
		{
			"id": "sAFCPMZX",
			"type": "rectangle",
			"x": -1462,
			"y": -672.8,
			"width": 417,
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
			"seed": 1360297409,
			"version": 2,
			"versionNonce": 1352669544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kMUpYMC5"
				},
				{
					"type": "arrow",
					"id": "NJWbbCWV"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4U"
		},
		{
			"id": "kMUpYMC5",
			"type": "text",
			"x": -1450,
			"y": -665.8,
			"width": 393,
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
			"seed": 1772093842,
			"version": 2,
			"versionNonce": 471240984,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "存檔的 UTF-8 檔、程式碼、commit 的證據：留下來",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sAFCPMZX",
			"originalText": "存檔的 UTF-8 檔、程式碼、commit 的證據：留下來",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4V"
		},
		{
			"id": "KVzCCBU9",
			"type": "rectangle",
			"x": -1182,
			"y": -624.8,
			"width": 137,
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
			"seed": 1801592503,
			"version": 2,
			"versionNonce": 1126739048,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DETxwDPp"
				},
				{
					"type": "arrow",
					"id": "9a3sCaDm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4W"
		},
		{
			"id": "DETxwDPp",
			"type": "text",
			"x": -1170,
			"y": -617.8,
			"width": 113,
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
			"seed": 655095508,
			"version": 2,
			"versionNonce": 1649716760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "print 不是存檔",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KVzCCBU9",
			"originalText": "print 不是存檔",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4X"
		},
		{
			"id": "K6FxG3Qr",
			"type": "rectangle",
			"x": -877,
			"y": -532.05,
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
			"groupIds": [
				"pWsMS4XY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 471534875,
			"version": 2,
			"versionNonce": 489086824,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "N3qCaNYp"
				},
				{
					"type": "arrow",
					"id": "Df2AHMwU"
				},
				{
					"type": "arrow",
					"id": "qUwdRD6C"
				},
				{
					"type": "arrow",
					"id": "rLmxwxSp"
				},
				{
					"type": "arrow",
					"id": "Tw7m9TMt"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4Y"
		},
		{
			"id": "N3qCaNYp",
			"type": "text",
			"x": -863,
			"y": -523.05,
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
				"pWsMS4XY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 520182560,
			"version": 2,
			"versionNonce": 1422338840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "儲存媒體",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "K6FxG3Qr",
			"originalText": "儲存媒體",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4Z"
		},
		{
			"id": "T86gBdFE",
			"type": "rectangle",
			"x": -1163,
			"y": -576.8,
			"width": 226,
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
			"seed": 1696510158,
			"version": 2,
			"versionNonce": 518435432,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "DFjtiQRC"
				},
				{
					"type": "arrow",
					"id": "qUwdRD6C"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4a"
		},
		{
			"id": "DFjtiQRC",
			"type": "text",
			"x": -1151,
			"y": -569.8,
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
			"seed": 1639844980,
			"version": 2,
			"versionNonce": 769787928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "HDD：旋轉磁碟、磁性記錄",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "T86gBdFE",
			"originalText": "HDD：旋轉磁碟、磁性記錄",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4b"
		},
		{
			"id": "8wfjUSxA",
			"type": "rectangle",
			"x": -1208,
			"y": -528.8,
			"width": 271,
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
			"seed": 922138471,
			"version": 2,
			"versionNonce": 523511144,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rWPCc6GD"
				},
				{
					"type": "arrow",
					"id": "rLmxwxSp"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4c"
		},
		{
			"id": "rWPCc6GD",
			"type": "text",
			"x": -1196,
			"y": -521.8,
			"width": 247,
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
			"seed": 1433713750,
			"version": 2,
			"versionNonce": 966346008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "SSD：非揮發 flash，沒有讀寫頭",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8wfjUSxA",
			"originalText": "SSD：非揮發 flash，沒有讀寫頭",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4d"
		},
		{
			"id": "8vBtbp8A",
			"type": "rectangle",
			"x": -1079,
			"y": -480.8,
			"width": 142,
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
			"seed": 1541132534,
			"version": 2,
			"versionNonce": 995833960,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MUjLZz2k"
				},
				{
					"type": "arrow",
					"id": "Tw7m9TMt"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4e"
		},
		{
			"id": "MUjLZz2k",
			"type": "text",
			"x": -1067,
			"y": -473.8,
			"width": 118,
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
			"seed": 1761310681,
			"version": 2,
			"versionNonce": 627106328,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "光碟：雷射讀取",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8vBtbp8A",
			"originalText": "光碟：雷射讀取",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4f"
		},
		{
			"id": "75qx32fd",
			"type": "rectangle",
			"x": -1224,
			"y": -432.8,
			"width": 452,
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
			"seed": 1661030446,
			"version": 2,
			"versionNonce": 120056680,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8VupSRDV"
				},
				{
					"type": "arrow",
					"id": "DeK8BjaZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4g"
		},
		{
			"id": "8VupSRDV",
			"type": "text",
			"x": -1210,
			"y": -423.8,
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
			"seed": 2023233942,
			"version": 2,
			"versionNonce": 1345117976,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "encoding 回答「哪些 bytes」；storage 回答「存\n在哪」",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "75qx32fd",
			"originalText": "encoding 回答「哪些 bytes」；storage 回答「存\n在哪」",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4h"
		},
		{
			"id": "kZhPc7e5",
			"type": "rectangle",
			"x": -993,
			"y": -355.8,
			"width": 221,
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
			"seed": 1993848778,
			"version": 2,
			"versionNonce": 1021722216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "f567tCgW"
				},
				{
					"type": "arrow",
					"id": "pSq8BzM4"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4i"
		},
		{
			"id": "f567tCgW",
			"type": "text",
			"x": -979,
			"y": -346.8,
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
			"seed": 769299881,
			"version": 2,
			"versionNonce": 443628568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "持久 ≠ 永久，≠ 已備份",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kZhPc7e5",
			"originalText": "持久 ≠ 永久，≠ 已備份",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4j"
		},
		{
			"id": "SNRUf5aH",
			"type": "rectangle",
			"x": -1056,
			"y": -282.5,
			"width": 284,
			"height": 40.5,
			"angle": 0,
			"strokeColor": "#c2255c",
			"backgroundColor": "#fff3bf",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"wygpRUfT"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 277692654,
			"version": 2,
			"versionNonce": 1835151720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fZjfqVuw"
				},
				{
					"type": "arrow",
					"id": "khxwWcPm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4k"
		},
		{
			"id": "fZjfqVuw",
			"type": "text",
			"x": -1042,
			"y": -273.5,
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
				"wygpRUfT"
			],
			"frameId": null,
			"roundness": null,
			"seed": 776486621,
			"version": 2,
			"versionNonce": 908196120,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "★ DRAM 斷電資料消失（T）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SNRUf5aH",
			"originalText": "★ DRAM 斷電資料消失（T）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4l"
		},
		{
			"id": "9UzpSnuX",
			"type": "rectangle",
			"x": -761,
			"y": 191.52,
			"width": 374,
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
			"seed": 1944302085,
			"version": 2,
			"versionNonce": 803718248,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Nspcnf9z"
				},
				{
					"type": "arrow",
					"id": "wAaUa7VN"
				},
				{
					"type": "arrow",
					"id": "i84GKMZz"
				},
				{
					"type": "arrow",
					"id": "cSDwYddJ"
				},
				{
					"type": "arrow",
					"id": "uxbkWPEC"
				},
				{
					"type": "arrow",
					"id": "iwxJu4SH"
				},
				{
					"type": "arrow",
					"id": "4wzTL9nJ"
				},
				{
					"type": "arrow",
					"id": "SMmiC3SE"
				},
				{
					"type": "arrow",
					"id": "UjwwxEzz"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4m"
		},
		{
			"id": "Nspcnf9z",
			"type": "text",
			"x": -741,
			"y": 203.52,
			"width": 334,
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
			"seed": 1439760885,
			"version": 2,
			"versionNonce": 1991448088,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "Q6 AI 修改介面，不偷改規則",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "9UzpSnuX",
			"originalText": "Q6 AI 修改介面，不偷改規則",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4n"
		},
		{
			"id": "4YuBHEFu",
			"type": "rectangle",
			"x": -1303,
			"y": -198,
			"width": 466,
			"height": 85.5,
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
			"seed": 161160836,
			"version": 2,
			"versionNonce": 1380120424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TunWzy4V"
				},
				{
					"type": "arrow",
					"id": "i84GKMZz"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4o"
		},
		{
			"id": "TunWzy4V",
			"type": "text",
			"x": -1289,
			"y": -189,
			"width": 438,
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
			"seed": 216689371,
			"version": 2,
			"versionNonce": 555258648,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Prompt：先比 v0.4／v0.5 契約，只要前端 patch；\n保留大小寫與空白；不要 regex、functions、file\nI/O",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4YuBHEFu",
			"originalText": "Prompt：先比 v0.4／v0.5 契約，只要前端 patch；\n保留大小寫與空白；不要 regex、functions、file\nI/O",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4p"
		},
		{
			"id": "bXKh2pH5",
			"type": "rectangle",
			"x": -1090,
			"y": -98.5,
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
			"seed": 314554627,
			"version": 2,
			"versionNonce": 146786920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "B7J5i2Gk"
				},
				{
					"type": "arrow",
					"id": "cSDwYddJ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4q"
		},
		{
			"id": "B7J5i2Gk",
			"type": "text",
			"x": -1076,
			"y": -89.5,
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
			"seed": 12523886,
			"version": 2,
			"versionNonce": 1002860568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "範例資料是資料，不是指令",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bXKh2pH5",
			"originalText": "範例資料是資料，不是指令",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4r"
		},
		{
			"id": "RVmMMJCY",
			"type": "rectangle",
			"x": -1100,
			"y": 24.75,
			"width": 263,
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
				"UgvpnBJm"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 563343415,
			"version": 2,
			"versionNonce": 506084712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dcEGuYxN"
				},
				{
					"type": "arrow",
					"id": "uxbkWPEC"
				},
				{
					"type": "arrow",
					"id": "NhPnjuYH"
				},
				{
					"type": "arrow",
					"id": "xgQHguqa"
				},
				{
					"type": "arrow",
					"id": "CsdYXCRQ"
				},
				{
					"type": "arrow",
					"id": "ibnmSkRd"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4s"
		},
		{
			"id": "dcEGuYxN",
			"type": "text",
			"x": -1086,
			"y": 33.75,
			"width": 235,
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
				"UgvpnBJm"
			],
			"frameId": null,
			"roundness": null,
			"seed": 496118087,
			"version": 2,
			"versionNonce": 1588636952,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "故意錯誤 candidate 四反例",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RVmMMJCY",
			"originalText": "故意錯誤 candidate 四反例",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4t"
		},
		{
			"id": "tV3vpTr4",
			"type": "rectangle",
			"x": -1499,
			"y": -44,
			"width": 339,
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
			"seed": 457471894,
			"version": 2,
			"versionNonce": 600723560,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Lnisq5Ps"
				},
				{
					"type": "arrow",
					"id": "NhPnjuYH"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4u"
		},
		{
			"id": "Lnisq5Ps",
			"type": "text",
			"x": -1487,
			"y": -37,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 480059690,
			"version": 2,
			"versionNonce": 55265816,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Donegal,1,30 → 誤停（用了 \"DONE\" in）",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tV3vpTr4",
			"originalText": "Donegal,1,30 → 誤停（用了 \"DONE\" in）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4v"
		},
		{
			"id": "MkPYreKg",
			"type": "rectangle",
			"x": -1455,
			"y": 4,
			"width": 295,
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
			"seed": 982342882,
			"version": 2,
			"versionNonce": 561513320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VXvcHpkj"
				},
				{
					"type": "arrow",
					"id": "xgQHguqa"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4w"
		},
		{
			"id": "VXvcHpkj",
			"type": "text",
			"x": -1443,
			"y": 11,
			"width": 271,
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
			"seed": 590791190,
			"version": 2,
			"versionNonce": 1418348312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus East,1,30 → 內部空白被刪",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MkPYreKg",
			"originalText": "Campus East,1,30 → 內部空白被刪",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4x"
		},
		{
			"id": "QZmswNmF",
			"type": "rectangle",
			"x": -1397,
			"y": 52,
			"width": 237,
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
			"seed": 1879767027,
			"version": 2,
			"versionNonce": 1165186664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2EHzUyRU"
				},
				{
					"type": "arrow",
					"id": "CsdYXCRQ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b4y"
		},
		{
			"id": "2EHzUyRU",
			"type": "text",
			"x": -1385,
			"y": 59,
			"width": 213,
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
			"seed": 1115132651,
			"version": 2,
			"versionNonce": 2128716824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "CaMpUs,1,30 → 大小寫被改",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QZmswNmF",
			"originalText": "CaMpUs,1,30 → 大小寫被改",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b4z"
		},
		{
			"id": "pED7Reff",
			"type": "rectangle",
			"x": -1453,
			"y": 100,
			"width": 293,
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
			"seed": 1328239037,
			"version": 2,
			"versionNonce": 344738152,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "E6mPX3Kx"
				},
				{
					"type": "arrow",
					"id": "ibnmSkRd"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b50"
		},
		{
			"id": "E6mPX3Kx",
			"type": "text",
			"x": -1441,
			"y": 107,
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
			"seed": 919876981,
			"version": 2,
			"versionNonce": 4546840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "Campus,1,30.9 → int(float()) 截斷",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pED7Reff",
			"originalText": "Campus,1,30.9 → int(float()) 截斷",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b51"
		},
		{
			"id": "ASnBzMyE",
			"type": "rectangle",
			"x": -942,
			"y": 240.75,
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
				"yXeHpKGD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1860328448,
			"version": 2,
			"versionNonce": 437181544,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "w3Hs3Lhu"
				},
				{
					"type": "arrow",
					"id": "iwxJu4SH"
				},
				{
					"type": "arrow",
					"id": "6LLEn7HL"
				},
				{
					"type": "arrow",
					"id": "4HUVCDur"
				},
				{
					"type": "arrow",
					"id": "AwcVT3Df"
				},
				{
					"type": "arrow",
					"id": "gqWZGTny"
				},
				{
					"type": "arrow",
					"id": "WDMtVHdy"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b52"
		},
		{
			"id": "w3Hs3Lhu",
			"type": "text",
			"x": -928,
			"y": 249.75,
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
				"yXeHpKGD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 733118865,
			"version": 2,
			"versionNonce": 2015985176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "成對測試",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ASnBzMyE",
			"originalText": "成對測試",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b53"
		},
		{
			"id": "vZBmk8eJ",
			"type": "rectangle",
			"x": -1289,
			"y": 148,
			"width": 287,
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
			"seed": 1561375223,
			"version": 2,
			"versionNonce": 398921576,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "qU9FAAPC"
				},
				{
					"type": "arrow",
					"id": "6LLEn7HL"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b54"
		},
		{
			"id": "qU9FAAPC",
			"type": "text",
			"x": -1277,
			"y": 155,
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
			"seed": 875172687,
			"version": 2,
			"versionNonce": 2005007128,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "加欄位邊緣空白 → 標籤與數字不變",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vZBmk8eJ",
			"originalText": "加欄位邊緣空白 → 標籤與數字不變",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b55"
		},
		{
			"id": "CckpTVdB",
			"type": "rectangle",
			"x": -1305,
			"y": 196,
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
			"seed": 896543895,
			"version": 2,
			"versionNonce": 906027624,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "3QVN6U4v"
				},
				{
					"type": "arrow",
					"id": "4HUVCDur"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b56"
		},
		{
			"id": "3QVN6U4v",
			"type": "text",
			"x": -1293,
			"y": 203,
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
			"seed": 279955023,
			"version": 2,
			"versionNonce": 1354946584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "只改大小寫 → 數字不變、保留新拼法",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CckpTVdB",
			"originalText": "只改大小寫 → 數字不變、保留新拼法",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b57"
		},
		{
			"id": "yV874EPH",
			"type": "rectangle",
			"x": -1256,
			"y": 244,
			"width": 254,
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
			"seed": 482934050,
			"version": 2,
			"versionNonce": 864572776,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4XygBBmT"
				},
				{
					"type": "arrow",
					"id": "AwcVT3Df"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b58"
		},
		{
			"id": "4XygBBmT",
			"type": "text",
			"x": -1244,
			"y": 251,
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
			"seed": 1608753214,
			"version": 2,
			"versionNonce": 1742738712,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "插一行無效 → 筆數與總和不變",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "yV874EPH",
			"originalText": "插一行無效 → 筆數與總和不變",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b59"
		},
		{
			"id": "dbSkgR8M",
			"type": "rectangle",
			"x": -1227,
			"y": 292,
			"width": 225,
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
			"seed": 285079863,
			"version": 2,
			"versionNonce": 363423848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "hYyuFN6S"
				},
				{
					"type": "arrow",
					"id": "gqWZGTny"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5A"
		},
		{
			"id": "hYyuFN6S",
			"type": "text",
			"x": -1215,
			"y": 299,
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
			"seed": 2139636143,
			"version": 2,
			"versionNonce": 38646296,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "DONE 當欄位值 → 是資料",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dbSkgR8M",
			"originalText": "DONE 當欄位值 → 是資料",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5B"
		},
		{
			"id": "AMz5FkVf",
			"type": "rectangle",
			"x": -1240,
			"y": 340,
			"width": 238,
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
			"seed": 732519801,
			"version": 2,
			"versionNonce": 1479547752,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iqw5QkfT"
				},
				{
					"type": "arrow",
					"id": "WDMtVHdy"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5C"
		},
		{
			"id": "iqw5QkfT",
			"type": "text",
			"x": -1228,
			"y": 347,
			"width": 214,
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
			"seed": 542734854,
			"version": 2,
			"versionNonce": 385855256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "立刻結束 → 0 筆、不算平均",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "AMz5FkVf",
			"originalText": "立刻結束 → 0 筆、不算平均",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5D"
		},
		{
			"id": "tniZFMYU",
			"type": "rectangle",
			"x": -1293,
			"y": 388,
			"width": 456,
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
			"seed": 264391104,
			"version": 2,
			"versionNonce": 493383272,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6hEJ6SuW"
				},
				{
					"type": "arrow",
					"id": "4wzTL9nJ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5E"
		},
		{
			"id": "6hEJ6SuW",
			"type": "text",
			"x": -1279,
			"y": 397,
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
			"seed": 1306397958,
			"version": 2,
			"versionNonce": 510266392,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "Session oracle：2 筆、16.00 km、75 min、37.50\nmin、12.80 km/h",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tniZFMYU",
			"originalText": "Session oracle：2 筆、16.00 km、75 min、37.50\nmin、12.80 km/h",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5F"
		},
		{
			"id": "BYUvkH8N",
			"type": "rectangle",
			"x": -1289,
			"y": 483.8,
			"width": 452,
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
				"RThbD67S"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1604967852,
			"version": 2,
			"versionNonce": 1579049320,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "tuFqmfEk"
				},
				{
					"type": "arrow",
					"id": "SMmiC3SE"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5G"
		},
		{
			"id": "tuFqmfEk",
			"type": "text",
			"x": -1275,
			"y": 492.8,
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
			"groupIds": [
				"RThbD67S"
			],
			"frameId": null,
			"roundness": null,
			"seed": 913572273,
			"version": 2,
			"versionNonce": 1652607256,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "trip_text.py：STOP／REJECT／ACCEPT 三條\n路徑",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BYUvkH8N",
			"originalText": "trip_text.py：STOP／REJECT／ACCEPT 三條\n路徑",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5H"
		},
		{
			"id": "Qy3pMDRe",
			"type": "rectangle",
			"x": -1252,
			"y": 560.8,
			"width": 415,
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
			"seed": 1476463594,
			"version": 2,
			"versionNonce": 429782120,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kfspEmdz"
				},
				{
					"type": "arrow",
					"id": "UjwwxEzz"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5I"
		},
		{
			"id": "kfspEmdz",
			"type": "text",
			"x": -1238,
			"y": 569.8,
			"width": 387,
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
			"seed": 1099141596,
			"version": 2,
			"versionNonce": 1320674840,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "講義自訂的兩個訊息：Error: empty record.、\nError: double quotes are not supported.",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Qy3pMDRe",
			"originalText": "講義自訂的兩個訊息：Error: empty record.、\nError: double quotes are not supported.",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5J"
		},
		{
			"id": "SKNxh5fQ",
			"type": "rectangle",
			"x": -479,
			"y": 900.75,
			"width": 92,
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
			"seed": 1813207763,
			"version": 2,
			"versionNonce": 95627112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "gqs4Q6F9"
				},
				{
					"type": "arrow",
					"id": "FPsuEaJQ"
				},
				{
					"type": "arrow",
					"id": "mTgDCDx6"
				},
				{
					"type": "arrow",
					"id": "KCS2zkLm"
				},
				{
					"type": "arrow",
					"id": "fScZQXtt"
				},
				{
					"type": "arrow",
					"id": "kt9NzBTM"
				},
				{
					"type": "arrow",
					"id": "pUWbCXkD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5K"
		},
		{
			"id": "gqs4Q6F9",
			"type": "text",
			"x": -459,
			"y": 912.75,
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
			"seed": 1205605780,
			"version": 2,
			"versionNonce": 1073963800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 24,
			"fontFamily": 5,
			"text": "選讀",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SKNxh5fQ",
			"originalText": "選讀",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5L"
		},
		{
			"id": "wELM4z2t",
			"type": "rectangle",
			"x": -977,
			"y": 686.6,
			"width": 422,
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
				"E7wqMsLY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1065102089,
			"version": 2,
			"versionNonce": 1051327080,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pTt3eNMn"
				},
				{
					"type": "arrow",
					"id": "mTgDCDx6"
				},
				{
					"type": "arrow",
					"id": "h6WKhumW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5M"
		},
		{
			"id": "pTt3eNMn",
			"type": "text",
			"x": -963,
			"y": 695.6,
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
			"groupIds": [
				"E7wqMsLY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1737362735,
			"version": 2,
			"versionNonce": 1423392792,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "csv.reader：引號裡的逗號是資料 → ['Campus,\nEast', '12.5', '45']",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wELM4z2t",
			"originalText": "csv.reader：引號裡的逗號是資料 → ['Campus,\nEast', '12.5', '45']",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5N"
		},
		{
			"id": "CTqWarTq",
			"type": "rectangle",
			"x": -1409,
			"y": 710.5,
			"width": 372,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"LZEaBGwx"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 325787837,
			"version": 2,
			"versionNonce": 2001628520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Nj5X6CL2"
				},
				{
					"type": "arrow",
					"id": "h6WKhumW"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5O"
		},
		{
			"id": "Nj5X6CL2",
			"type": "text",
			"x": -1397,
			"y": 717.5,
			"width": 348,
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
				"LZEaBGwx"
			],
			"frameId": null,
			"roundness": null,
			"seed": 896345395,
			"version": 2,
			"versionNonce": 1025998104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "csv 只負責切欄位，不保證距離有限、分鐘為正",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CTqWarTq",
			"originalText": "csv 只負責切欄位，不保證距離有限、分鐘為正",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5P"
		},
		{
			"id": "pFjexcyw",
			"type": "rectangle",
			"x": -1000,
			"y": 782.4,
			"width": 445,
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
				"SkBziZWa"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1069493199,
			"version": 2,
			"versionNonce": 686588008,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8U4kdWwj"
				},
				{
					"type": "arrow",
					"id": "KCS2zkLm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5Q"
		},
		{
			"id": "8U4kdWwj",
			"type": "text",
			"x": -986,
			"y": 791.4,
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
				"SkBziZWa"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1338269383,
			"version": 2,
			"versionNonce": 174594584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "unicodedata.normalize(\"NFC\", ...)：é 兩種寫法比\n較相等",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "pFjexcyw",
			"originalText": "unicodedata.normalize(\"NFC\", ...)：é 兩種寫法比\n較相等",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5R"
		},
		{
			"id": "4Sph2aky",
			"type": "rectangle",
			"x": -994,
			"y": 859.4,
			"width": 439,
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
			"seed": 781984594,
			"version": 2,
			"versionNonce": 1129329512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eRwZ72r2"
				},
				{
					"type": "arrow",
					"id": "fScZQXtt"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5S"
		},
		{
			"id": "eRwZ72r2",
			"type": "text",
			"x": -980,
			"y": 868.4,
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
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1115406366,
			"version": 2,
			"versionNonce": 2139952920,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "open(..., encoding=\"utf-8\")；with 結束自動關檔",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4Sph2aky",
			"originalText": "open(..., encoding=\"utf-8\")；with 結束自動關檔",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5T"
		},
		{
			"id": "LNv378bV",
			"type": "rectangle",
			"x": -697,
			"y": 982.65,
			"width": 142,
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
			"seed": 1987448115,
			"version": 2,
			"versionNonce": 1556448872,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SeRwaFsd"
				},
				{
					"type": "arrow",
					"id": "kt9NzBTM"
				},
				{
					"type": "arrow",
					"id": "x8xSbPVH"
				},
				{
					"type": "arrow",
					"id": "ubmbSrLD"
				},
				{
					"type": "arrow",
					"id": "3psycaCm"
				},
				{
					"type": "arrow",
					"id": "KH3xPPLm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5U"
		},
		{
			"id": "SeRwaFsd",
			"type": "text",
			"x": -683,
			"y": 991.65,
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
			"seed": 1493326250,
			"version": 2,
			"versionNonce": 1628075032,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "方法回傳型態",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LNv378bV",
			"originalText": "方法回傳型態",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5V"
		},
		{
			"id": "52Hdj5xH",
			"type": "rectangle",
			"x": -1049,
			"y": 913.9,
			"width": 292,
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
			"seed": 1322289455,
			"version": 2,
			"versionNonce": 1645771112,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pHvBHu35"
				},
				{
					"type": "arrow",
					"id": "x8xSbPVH"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5W"
		},
		{
			"id": "pHvBHu35",
			"type": "text",
			"x": -1037,
			"y": 920.9,
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
			"seed": 1753410370,
			"version": 2,
			"versionNonce": 1154756888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "in、startswith、endswith → bool",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "52Hdj5xH",
			"originalText": "in、startswith、endswith → bool",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5X"
		},
		{
			"id": "t7mWSiMk",
			"type": "rectangle",
			"x": -970,
			"y": 961.9,
			"width": 213,
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
			"seed": 834819916,
			"version": 2,
			"versionNonce": 1184173160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9eLBXSJ5"
				},
				{
					"type": "arrow",
					"id": "ubmbSrLD"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5Y"
		},
		{
			"id": "9eLBXSJ5",
			"type": "text",
			"x": -958,
			"y": 968.9,
			"width": 189,
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
			"seed": 1328444961,
			"version": 2,
			"versionNonce": 1650347544,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "find、rfind → 位置或 −1",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "t7mWSiMk",
			"originalText": "find、rfind → 位置或 −1",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5Z"
		},
		{
			"id": "7JEwxByx",
			"type": "rectangle",
			"x": -1063,
			"y": 1009.9,
			"width": 306,
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
			"seed": 858587493,
			"version": 2,
			"versionNonce": 872890216,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "iynaA6iV"
				},
				{
					"type": "arrow",
					"id": "3psycaCm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5a"
		},
		{
			"id": "iynaA6iV",
			"type": "text",
			"x": -1051,
			"y": 1016.9,
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
			"seed": 1027290638,
			"version": 2,
			"versionNonce": 1654442776,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "replace、strip、lower、upper → str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7JEwxByx",
			"originalText": "replace、strip、lower、upper → str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5b"
		},
		{
			"id": "Rq9jMR85",
			"type": "rectangle",
			"x": -973,
			"y": 1057.9,
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
			"seed": 1124088230,
			"version": 2,
			"versionNonce": 985338472,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SF2BqxxA"
				},
				{
					"type": "arrow",
					"id": "KH3xPPLm"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5c"
		},
		{
			"id": "SF2BqxxA",
			"type": "text",
			"x": -961,
			"y": 1064.9,
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
			"seed": 919548689,
			"version": 2,
			"versionNonce": 805546008,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "split → list；join → str",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Rq9jMR85",
			"originalText": "split → list；join → str",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5d"
		},
		{
			"id": "XU9PULSn",
			"type": "rectangle",
			"x": -1005,
			"y": 1105.9,
			"width": 450,
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
			"seed": 591871613,
			"version": 2,
			"versionNonce": 24937832,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XjTx2ANb"
				},
				{
					"type": "arrow",
					"id": "pUWbCXkD"
				},
				{
					"type": "arrow",
					"id": "3vWWsN9d"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5e"
		},
		{
			"id": "XjTx2ANb",
			"type": "text",
			"x": -991,
			"y": 1114.9,
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
			"seed": 79231273,
			"version": 2,
			"versionNonce": 1183245592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "⚠ strip(\"km\") 去的是字元集合，不是去掉 \"km\" 字\n尾",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XU9PULSn",
			"originalText": "⚠ strip(\"km\") 去的是字元集合，不是去掉 \"km\" 字\n尾",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5f"
		},
		{
			"id": "5EnZ8WaR",
			"type": "rectangle",
			"x": -1287,
			"y": 1129.8,
			"width": 222,
			"height": 34,
			"angle": 0,
			"strokeColor": "#9c36b5",
			"backgroundColor": "#ffffff",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "dotted",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"EkTA443y"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1768890174,
			"version": 2,
			"versionNonce": 1972869224,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EZDz2xBR"
				},
				{
					"type": "arrow",
					"id": "3vWWsN9d"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5g"
		},
		{
			"id": "EZDz2xBR",
			"type": "text",
			"x": -1275,
			"y": 1136.8,
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
			"groupIds": [
				"EkTA443y"
			],
			"frameId": null,
			"roundness": null,
			"seed": 100834644,
			"version": 2,
			"versionNonce": 60457496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "\"abXba\".strip(\"ab\") → \"X\"",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5EnZ8WaR",
			"originalText": "\"abXba\".strip(\"ab\") → \"X\"",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b5h"
		},
		{
			"id": "5tFTWVqf",
			"type": "rectangle",
			"x": 1198,
			"y": -1538.75,
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
				"jmTfwthc"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 334580195,
			"version": 2,
			"versionNonce": 2060995432,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "FWBRxDqB"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5i"
		},
		{
			"id": "FWBRxDqB",
			"type": "text",
			"x": 1205,
			"y": -1535.75,
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
				"jmTfwthc"
			],
			"frameId": null,
			"roundness": null,
			"seed": 875235111,
			"version": 2,
			"versionNonce": 1983020824,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T056",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5tFTWVqf",
			"originalText": "T056",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5j"
		},
		{
			"id": "RsLGDfAY",
			"type": "rectangle",
			"x": 1405,
			"y": -1163.95,
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
				"dGfTUD9z"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1206220996,
			"version": 2,
			"versionNonce": 462069352,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eGLYwMJX"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5k"
		},
		{
			"id": "eGLYwMJX",
			"type": "text",
			"x": 1412,
			"y": -1160.95,
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
				"dGfTUD9z"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1720459982,
			"version": 2,
			"versionNonce": 784522264,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T084",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RsLGDfAY",
			"originalText": "T084",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5l"
		},
		{
			"id": "jqfp7DL7",
			"type": "rectangle",
			"x": 1077,
			"y": -923.15,
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
				"BRAbXeCU"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1548657638,
			"version": 2,
			"versionNonce": 947556712,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "2iqJsYBe"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5m"
		},
		{
			"id": "2iqJsYBe",
			"type": "text",
			"x": 1084,
			"y": -920.15,
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
				"BRAbXeCU"
			],
			"frameId": null,
			"roundness": null,
			"seed": 614368985,
			"version": 2,
			"versionNonce": 255826200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T049",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "jqfp7DL7",
			"originalText": "T049",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5n"
		},
		{
			"id": "7s8benTd",
			"type": "rectangle",
			"x": 996,
			"y": -821,
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
				"xLCbYxGK"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1729377092,
			"version": 2,
			"versionNonce": 955524200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "MLm8ERKB"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5o"
		},
		{
			"id": "MLm8ERKB",
			"type": "text",
			"x": 1003,
			"y": -818,
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
				"xLCbYxGK"
			],
			"frameId": null,
			"roundness": null,
			"seed": 667385549,
			"version": 2,
			"versionNonce": 454866456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q021",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7s8benTd",
			"originalText": "Q021",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5p"
		},
		{
			"id": "Y7cCqLJw",
			"type": "rectangle",
			"x": 1429,
			"y": -808.35,
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
				"tT9hJXvR"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 962925218,
			"version": 2,
			"versionNonce": 985880424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "84xMVNG4"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5q"
		},
		{
			"id": "84xMVNG4",
			"type": "text",
			"x": 1436,
			"y": -805.35,
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
				"tT9hJXvR"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1248572716,
			"version": 2,
			"versionNonce": 1196307224,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T050",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Y7cCqLJw",
			"originalText": "T050",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5r"
		},
		{
			"id": "vnCeZhJi",
			"type": "rectangle",
			"x": 1243,
			"y": -597.55,
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
				"hB5nVRx6"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 783744873,
			"version": 2,
			"versionNonce": 1110714984,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G538M9gb"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5s"
		},
		{
			"id": "G538M9gb",
			"type": "text",
			"x": 1250,
			"y": -594.55,
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
				"hB5nVRx6"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1920089565,
			"version": 2,
			"versionNonce": 1246236696,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T085",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vnCeZhJi",
			"originalText": "T085",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5t"
		},
		{
			"id": "ZqNau2xU",
			"type": "rectangle",
			"x": 1019,
			"y": -384.75,
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
				"YNsJFqPu"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 553796945,
			"version": 2,
			"versionNonce": 1779604840,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "zwxbUBib"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5u"
		},
		{
			"id": "zwxbUBib",
			"type": "text",
			"x": 1026,
			"y": -381.75,
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
				"YNsJFqPu"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1420103113,
			"version": 2,
			"versionNonce": 1811827992,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T083",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZqNau2xU",
			"originalText": "T083",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5v"
		},
		{
			"id": "5jYp2jY8",
			"type": "rectangle",
			"x": 984,
			"y": -311.45,
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
				"E4s9tMes"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 434284072,
			"version": 2,
			"versionNonce": 329953384,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "VJRNz68P"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5w"
		},
		{
			"id": "VJRNz68P",
			"type": "text",
			"x": 991,
			"y": -308.45,
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
				"E4s9tMes"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1429360493,
			"version": 2,
			"versionNonce": 1441065496,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T081",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5jYp2jY8",
			"originalText": "T081",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5x"
		},
		{
			"id": "hMH6uPuX",
			"type": "rectangle",
			"x": 1050,
			"y": -46.15,
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
				"gKzE4nxH"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 624526879,
			"version": 2,
			"versionNonce": 382231400,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "eC8sLUc8"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b5y"
		},
		{
			"id": "eC8sLUc8",
			"type": "text",
			"x": 1057,
			"y": -43.15,
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
				"gKzE4nxH"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1753972839,
			"version": 2,
			"versionNonce": 1659889432,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T051",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hMH6uPuX",
			"originalText": "T051",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b5z"
		},
		{
			"id": "DP5yfUa9",
			"type": "rectangle",
			"x": 1018,
			"y": 49.65,
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
				"nTuDSzFn"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1365883430,
			"version": 2,
			"versionNonce": 1907865192,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "wyv5PamZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b60"
		},
		{
			"id": "wyv5PamZ",
			"type": "text",
			"x": 1025,
			"y": 52.65,
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
				"nTuDSzFn"
			],
			"frameId": null,
			"roundness": null,
			"seed": 213205344,
			"version": 2,
			"versionNonce": 1871922200,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T052 Q022",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DP5yfUa9",
			"originalText": "T052 Q022",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b61"
		},
		{
			"id": "adbSLwrE",
			"type": "rectangle",
			"x": 1514,
			"y": 145.45,
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
				"u73627NZ"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 373348137,
			"version": 2,
			"versionNonce": 2034542952,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "4VCz4thd"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b62"
		},
		{
			"id": "4VCz4thd",
			"type": "text",
			"x": 1521,
			"y": 148.45,
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
				"u73627NZ"
			],
			"frameId": null,
			"roundness": null,
			"seed": 764158746,
			"version": 2,
			"versionNonce": 700645656,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T100",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "adbSLwrE",
			"originalText": "T100",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b63"
		},
		{
			"id": "ukmgskDa",
			"type": "rectangle",
			"x": 823,
			"y": 234.2,
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
				"sjbNaEXp"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 190806073,
			"version": 2,
			"versionNonce": 146488424,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "dEBf8DLw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b64"
		},
		{
			"id": "dEBf8DLw",
			"type": "text",
			"x": 830,
			"y": 237.2,
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
				"sjbNaEXp"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2006146705,
			"version": 2,
			"versionNonce": 1626545688,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T055 T080",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ukmgskDa",
			"originalText": "T055 T080",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b65"
		},
		{
			"id": "tvJhgVJi",
			"type": "rectangle",
			"x": 790,
			"y": 363.6,
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
				"6LJtDwer"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1766121721,
			"version": 2,
			"versionNonce": 837250920,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "d2eg9iSH"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b66"
		},
		{
			"id": "d2eg9iSH",
			"type": "text",
			"x": 797,
			"y": 366.6,
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
				"6LJtDwer"
			],
			"frameId": null,
			"roundness": null,
			"seed": 179346480,
			"version": 2,
			"versionNonce": 1444387608,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T048",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tvJhgVJi",
			"originalText": "T048",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b67"
		},
		{
			"id": "FtE5y6Rh",
			"type": "rectangle",
			"x": 1087,
			"y": 424.25,
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
				"7KzUyEbk"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 2025422198,
			"version": 2,
			"versionNonce": 1830109800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LNLkw7X6"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b68"
		},
		{
			"id": "LNLkw7X6",
			"type": "text",
			"x": 1094,
			"y": 427.25,
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
				"7KzUyEbk"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1980615096,
			"version": 2,
			"versionNonce": 195328024,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T047",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "FtE5y6Rh",
			"originalText": "T047",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b69"
		},
		{
			"id": "QSENkGPs",
			"type": "rectangle",
			"x": 1117,
			"y": 587.95,
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
				"qpscKJVd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 444347166,
			"version": 2,
			"versionNonce": 1225831784,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "EbPSELrp"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6A"
		},
		{
			"id": "EbPSELrp",
			"type": "text",
			"x": 1124,
			"y": 590.95,
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
				"qpscKJVd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 519266069,
			"version": 2,
			"versionNonce": 361608472,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q023",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QSENkGPs",
			"originalText": "Q023",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6B"
		},
		{
			"id": "tj8iMbsg",
			"type": "rectangle",
			"x": 1484,
			"y": 521.05,
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
				"s6CsVw5h"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1464072493,
			"version": 2,
			"versionNonce": 455460968,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "kMBqVicF"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6C"
		},
		{
			"id": "kMBqVicF",
			"type": "text",
			"x": 1491,
			"y": 524.05,
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
				"s6CsVw5h"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2030876393,
			"version": 2,
			"versionNonce": 1766281752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T053",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tj8iMbsg",
			"originalText": "T053",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6D"
		},
		{
			"id": "nt5aBjGG",
			"type": "rectangle",
			"x": 1552,
			"y": 683.85,
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
				"9hU8SGdd"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1104512580,
			"version": 2,
			"versionNonce": 790657896,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "PQtwBGN7"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6E"
		},
		{
			"id": "PQtwBGN7",
			"type": "text",
			"x": 1559,
			"y": 686.85,
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
				"9hU8SGdd"
			],
			"frameId": null,
			"roundness": null,
			"seed": 982089648,
			"version": 2,
			"versionNonce": 767905560,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T054",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "nt5aBjGG",
			"originalText": "T054",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6F"
		},
		{
			"id": "4QxJzaKS",
			"type": "rectangle",
			"x": 1584,
			"y": 750.65,
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
				"ER8Kasaz"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 410001395,
			"version": 2,
			"versionNonce": 2001522280,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "XjnALU2N"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6G"
		},
		{
			"id": "XjnALU2N",
			"type": "text",
			"x": 1591,
			"y": 753.65,
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
				"ER8Kasaz"
			],
			"frameId": null,
			"roundness": null,
			"seed": 2104520756,
			"version": 2,
			"versionNonce": 192654360,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T082",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4QxJzaKS",
			"originalText": "T082",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6H"
		},
		{
			"id": "MWJBSbtE",
			"type": "rectangle",
			"x": 951,
			"y": 935.4,
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
				"9TSU4gk6"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1284494904,
			"version": 2,
			"versionNonce": 1014415720,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "nGFT7CNX"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6I"
		},
		{
			"id": "nGFT7CNX",
			"type": "text",
			"x": 958,
			"y": 938.4,
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
				"9TSU4gk6"
			],
			"frameId": null,
			"roundness": null,
			"seed": 453361648,
			"version": 2,
			"versionNonce": 2086562072,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q028",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MWJBSbtE",
			"originalText": "Q028",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6J"
		},
		{
			"id": "NRXNCExn",
			"type": "rectangle",
			"x": 1524,
			"y": 1173.45,
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
				"77E8kqML"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 219448712,
			"version": 2,
			"versionNonce": 1307202664,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "rfcXuqbE"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6K"
		},
		{
			"id": "rfcXuqbE",
			"type": "text",
			"x": 1531,
			"y": 1176.45,
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
				"77E8kqML"
			],
			"frameId": null,
			"roundness": null,
			"seed": 728855991,
			"version": 2,
			"versionNonce": 467764760,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T057",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NRXNCExn",
			"originalText": "T057",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6L"
		},
		{
			"id": "ts7HtDb4",
			"type": "rectangle",
			"x": -1353,
			"y": -1114.4,
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
				"zmcS5STN"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 511542127,
			"version": 2,
			"versionNonce": 829654888,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KZZGwGHj"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6M"
		},
		{
			"id": "KZZGwGHj",
			"type": "text",
			"x": -1346,
			"y": -1111.4,
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
				"zmcS5STN"
			],
			"frameId": null,
			"roundness": null,
			"seed": 63044903,
			"version": 2,
			"versionNonce": 1996030744,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T058 Q024",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ts7HtDb4",
			"originalText": "T058 Q024",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6N"
		},
		{
			"id": "M9ET97e7",
			"type": "rectangle",
			"x": -1312,
			"y": -951.6,
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
				"rEP3DHhN"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 688973272,
			"version": 2,
			"versionNonce": 1398692456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "LenGxm7q"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6O"
		},
		{
			"id": "LenGxm7q",
			"type": "text",
			"x": -1305,
			"y": -948.6,
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
				"rEP3DHhN"
			],
			"frameId": null,
			"roundness": null,
			"seed": 714938103,
			"version": 2,
			"versionNonce": 1545134104,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T094",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "M9ET97e7",
			"originalText": "T094",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6P"
		},
		{
			"id": "GUmLc2St",
			"type": "rectangle",
			"x": -815,
			"y": -838.85,
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
				"iQHC58aC"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1974729,
			"version": 2,
			"versionNonce": 913755496,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "bfdiPeNw"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6Q"
		},
		{
			"id": "bfdiPeNw",
			"type": "text",
			"x": -808,
			"y": -835.85,
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
				"iQHC58aC"
			],
			"frameId": null,
			"roundness": null,
			"seed": 79497594,
			"version": 2,
			"versionNonce": 724901144,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q036",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GUmLc2St",
			"originalText": "Q036",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6R"
		},
		{
			"id": "cqCdbmQA",
			"type": "rectangle",
			"x": -856,
			"y": -694.85,
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
				"TXGJQLZw"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1243130893,
			"version": 2,
			"versionNonce": 604561512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "SWSgeHhh"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6S"
		},
		{
			"id": "SWSgeHhh",
			"type": "text",
			"x": -849,
			"y": -691.85,
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
				"TXGJQLZw"
			],
			"frameId": null,
			"roundness": null,
			"seed": 791506035,
			"version": 2,
			"versionNonce": 633453080,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T059 Q002",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "cqCdbmQA",
			"originalText": "T059 Q002",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6T"
		},
		{
			"id": "KkxWVUSn",
			"type": "rectangle",
			"x": -815,
			"y": -550.85,
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
				"pWsMS4XY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 170803097,
			"version": 2,
			"versionNonce": 1541444456,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "jk6TE4GU"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6U"
		},
		{
			"id": "jk6TE4GU",
			"type": "text",
			"x": -808,
			"y": -547.85,
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
				"pWsMS4XY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 425902236,
			"version": 2,
			"versionNonce": 1051899672,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T060",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KkxWVUSn",
			"originalText": "T060",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6V"
		},
		{
			"id": "bmMJKSee",
			"type": "rectangle",
			"x": -815,
			"y": -301.3,
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
				"wygpRUfT"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 8958417,
			"version": 2,
			"versionNonce": 1145693800,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fRkDUcPd"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6W"
		},
		{
			"id": "fRkDUcPd",
			"type": "text",
			"x": -808,
			"y": -298.3,
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
				"wygpRUfT"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1113734882,
			"version": 2,
			"versionNonce": 1786516504,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T002",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "bmMJKSee",
			"originalText": "T002",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6X"
		},
		{
			"id": "GHRSXDZx",
			"type": "rectangle",
			"x": -880,
			"y": 5.95,
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
				"UgvpnBJm"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 40847445,
			"version": 2,
			"versionNonce": 437311848,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Zfq24ZDZ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6Y"
		},
		{
			"id": "Zfq24ZDZ",
			"type": "text",
			"x": -873,
			"y": 8.95,
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
				"UgvpnBJm"
			],
			"frameId": null,
			"roundness": null,
			"seed": 805611528,
			"version": 2,
			"versionNonce": 1863438616,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q038",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GHRSXDZx",
			"originalText": "Q038",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6Z"
		},
		{
			"id": "L4zFcLu4",
			"type": "rectangle",
			"x": -921,
			"y": 221.95,
			"width": 90,
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
				"yXeHpKGD"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1996700559,
			"version": 2,
			"versionNonce": 545352808,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WqpPBqtg"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6a"
		},
		{
			"id": "WqpPBqtg",
			"type": "text",
			"x": -914,
			"y": 224.95,
			"width": 76,
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
				"yXeHpKGD"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1608166066,
			"version": 2,
			"versionNonce": 870837784,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T099 Q034",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "L4zFcLu4",
			"originalText": "T099 Q034",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6b"
		},
		{
			"id": "t49fyBbM",
			"type": "rectangle",
			"x": -880,
			"y": 465,
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
				"RThbD67S"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 151682248,
			"version": 2,
			"versionNonce": 1365745512,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Q3aDUeGJ"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6c"
		},
		{
			"id": "Q3aDUeGJ",
			"type": "text",
			"x": -873,
			"y": 468,
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
				"RThbD67S"
			],
			"frameId": null,
			"roundness": null,
			"seed": 19916944,
			"version": 2,
			"versionNonce": 301099800,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q037",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "t49fyBbM",
			"originalText": "Q037",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6d"
		},
		{
			"id": "hgBzJFBN",
			"type": "rectangle",
			"x": -598,
			"y": 667.8,
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
				"E7wqMsLY"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 1902063165,
			"version": 2,
			"versionNonce": 219116136,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "S9VrCaiL"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6e"
		},
		{
			"id": "S9VrCaiL",
			"type": "text",
			"x": -591,
			"y": 670.8,
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
				"E7wqMsLY"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1105816590,
			"version": 2,
			"versionNonce": 598034456,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "Q039",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hgBzJFBN",
			"originalText": "Q039",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6f"
		},
		{
			"id": "SX2QZWNZ",
			"type": "rectangle",
			"x": -1080,
			"y": 691.7,
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
				"LZEaBGwx"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 462985998,
			"version": 2,
			"versionNonce": 1246029160,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TYyEarq9"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6g"
		},
		{
			"id": "TYyEarq9",
			"type": "text",
			"x": -1073,
			"y": 694.7,
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
				"LZEaBGwx"
			],
			"frameId": null,
			"roundness": null,
			"seed": 784252039,
			"version": 2,
			"versionNonce": 351569176,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T096",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "SX2QZWNZ",
			"originalText": "T096",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6h"
		},
		{
			"id": "MNnpHFzz",
			"type": "rectangle",
			"x": -598,
			"y": 763.6,
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
				"SkBziZWa"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 328103403,
			"version": 2,
			"versionNonce": 1179908200,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Es2ByExj"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6i"
		},
		{
			"id": "Es2ByExj",
			"type": "text",
			"x": -591,
			"y": 766.6,
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
				"SkBziZWa"
			],
			"frameId": null,
			"roundness": null,
			"seed": 757545939,
			"version": 2,
			"versionNonce": 1934893592,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T095",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "MNnpHFzz",
			"originalText": "T095",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6j"
		},
		{
			"id": "RAB5eaPK",
			"type": "rectangle",
			"x": -1108,
			"y": 1111,
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
				"EkTA443y"
			],
			"frameId": null,
			"roundness": {
				"type": 3
			},
			"seed": 204492819,
			"version": 2,
			"versionNonce": 889760616,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "AEeyLgJn"
				}
			],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"index": "b6k"
		},
		{
			"id": "AEeyLgJn",
			"type": "text",
			"x": -1101,
			"y": 1114,
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
				"EkTA443y"
			],
			"frameId": null,
			"roundness": null,
			"seed": 249659109,
			"version": 2,
			"versionNonce": 2109218584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T090",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RAB5eaPK",
			"originalText": "T090",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6l"
		},
		{
			"id": "dThBaD93",
			"type": "text",
			"x": -1664,
			"y": -2091.75,
			"width": 1223,
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
			"seed": 1838540511,
			"version": 2,
			"versionNonce": 1890516584,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 40,
			"fontFamily": 5,
			"text": "PROG1 期中心智圖 5｜Deck 5：程式如何處理並解讀文字（W8）",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "PROG1 期中心智圖 5｜Deck 5：程式如何處理並解讀文字（W8）",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b6m"
		},
		{
			"id": "2dTN7ZUv",
			"type": "text",
			"x": -1664,
			"y": -2029.75,
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
			"seed": 276851174,
			"version": 2,
			"versionNonce": 1955888152,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148488,
			"link": null,
			"locked": false,
			"fontSize": 18,
			"fontFamily": 5,
			"text": "來源：PROG1 Deck 5 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "來源：PROG1 Deck 5 整理（2026-10-16 版）與 PROG1 期中心智圖。標籤是老師 Midterm Practice 例題題號（T＝是非、Q＝問答）；老師說考題不會一模一樣，標籤用來找對應的\n練習題。",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b6n"
		},
		{
			"id": "N9JCSJx7",
			"type": "rectangle",
			"x": -1664,
			"y": -1962.75,
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
			"seed": 1876254670,
			"version": 2,
			"versionNonce": 705884520,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "8JbGetBe"
				}
			],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"index": "b6o"
		},
		{
			"id": "8JbGetBe",
			"type": "text",
			"x": -1650,
			"y": -1953.75,
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
			"seed": 347108129,
			"version": 2,
			"versionNonce": 1776105752,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "★ 考古題考過",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "N9JCSJx7",
			"originalText": "★ 考古題考過",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b6p"
		},
		{
			"id": "7V53HwWt",
			"type": "rectangle",
			"x": -1503,
			"y": -1962.75,
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
			"seed": 259789121,
			"version": 2,
			"versionNonce": 411075688,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "X9RxqDUh"
				}
			],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"index": "b6q"
		},
		{
			"id": "X9RxqDUh",
			"type": "text",
			"x": -1489,
			"y": -1953.75,
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
			"seed": 540784458,
			"version": 2,
			"versionNonce": 285627928,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "⚠ 易錯陷阱",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7V53HwWt",
			"originalText": "⚠ 易錯陷阱",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b6r"
		},
		{
			"id": "UvY8QZMH",
			"type": "rectangle",
			"x": -1359,
			"y": -1962.75,
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
			"seed": 1940611601,
			"version": 2,
			"versionNonce": 700692328,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Sqm9rv7R"
				}
			],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"index": "b6s"
		},
		{
			"id": "Sqm9rv7R",
			"type": "text",
			"x": -1345,
			"y": -1953.75,
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
			"seed": 461480716,
			"version": 2,
			"versionNonce": 251908888,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 5,
			"text": "例題考到、原本心智圖沒有的觀念",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "UvY8QZMH",
			"originalText": "例題考到、原本心智圖沒有的觀念",
			"autoResize": true,
			"lineHeight": 1.25,
			"index": "b6t"
		},
		{
			"id": "ZH22WZut",
			"type": "rectangle",
			"x": -1057,
			"y": -1955.15,
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
			"seed": 99393196,
			"version": 2,
			"versionNonce": 841517672,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CyGLswSY"
				}
			],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"index": "b6u"
		},
		{
			"id": "CyGLswSY",
			"type": "text",
			"x": -1050,
			"y": -1952.15,
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
			"seed": 1915843321,
			"version": 2,
			"versionNonce": 1246343192,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T001 Q001",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ZH22WZut",
			"originalText": "T001 Q001",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6v"
		},
		{
			"id": "8kjkWpGq",
			"type": "text",
			"x": -959,
			"y": -1953.75,
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
			"seed": 1765747693,
			"version": 2,
			"versionNonce": 477822312,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
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
			"index": "b6w"
		},
		{
			"id": "HspMCYSg",
			"type": "rectangle",
			"x": -830,
			"y": -1955.15,
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
			"seed": 266122456,
			"version": 2,
			"versionNonce": 986443032,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WzBTiXPA"
				}
			],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"index": "b6x"
		},
		{
			"id": "WzBTiXPA",
			"type": "text",
			"x": -823,
			"y": -1952.15,
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
			"seed": 803912455,
			"version": 2,
			"versionNonce": 436670568,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
			"link": null,
			"locked": false,
			"fontSize": 14,
			"fontFamily": 3,
			"text": "T089",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HspMCYSg",
			"originalText": "T089",
			"autoResize": true,
			"lineHeight": 1.2,
			"index": "b6y"
		},
		{
			"id": "g3MKzkBW",
			"type": "text",
			"x": -773,
			"y": -1953.75,
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
			"seed": 1364477936,
			"version": 2,
			"versionNonce": 972982808,
			"isDeleted": false,
			"boundElements": [],
			"updated": 1793858148489,
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
			"index": "b6z"
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