---
course: [PROG1]
semester: "115-1"
chapter: ["1", "2", "3", "4", "5"]
tags: [programming, exam, needs-review]
source:
  - "圖片_251107_143342_260925_102707.PDF（考古題 A：Midterm I，年份不明）"
  - "圖片 2_251107_142435_260925_102851.PDF（考古題 B：Fall 2021 Midterm I 與手寫參考答案）"
created: 2026-10-16
up: "[[PROG1 Index]]"
format: "global 1.0"
---
> [!info] Coverage
> 兩份舊版課程的期中考 Midterm I：考古題 A（年份不明，7 題、110 分）與考古題 B（Fall 2021，8 題、105 分，附手寫參考答案）。題目照抄，解答與說明都是 Claude 寫的，程式都用 Python 3.13 跑過。對應的講義在 [[PROG1 Deck 1 整理]]、[[PROG1 Deck 2 整理]]、[[PROG1 Deck 3 整理]]、[[PROG1 Deck 4 整理]]、[[PROG1 Deck 5 整理]]。

> [!warning] Claude 提醒：這兩份考古題怎麼用
> - 兩份都是舊版課程的 Midterm I：考古題 B 封面寫 Fall 2021（3 頁、8 題、105 分），考古題 A 封面沒有年份（3 頁、7 題、110 分）。今年教材改成 AI-PBL 版的 Deck 1–5，題型可能改變；但兩份的結構很一致：第 1 題是電腦概念是非題（A 51 分、B 45 分），其餘幾乎都是「寫出螢幕輸出」的程式追蹤題（A 59 分、B 45 分），B 另有改語法錯誤 10 分、寫出兩位老師名字 5 分。
> - 考古題 A 卷上的紅筆與藍筆答案是別人寫的，不是官方答案，其中有幾題是錯的（下面逐題標出）。考古題 B 第 4 頁是 2021 年的手寫參考答案。
> - 每一題的程式都用 Python 3.13 實際跑過；是非題附判斷理由與新講義的位置。考卷是 LaTeX 排版，引號印成 ” ”，這裡照 Python 寫成直引號 `"`。

## 考點對照表

| 考點 | 考古題 A | 考古題 B | 新講義位置 | 新講義有教？ |
| --- | --- | --- | --- | --- |
| 指令集、RISC／CISC（ARM） | 1(a)(b)(f) | 1(a)(b)(e) | [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式\|D1-Q5]]（不同 architecture 有不同 instruction set） | 部分 |
| L1／L2 cache 大小與速度 | 1(c)(d) | 1(c) | [[PROG1 Deck 4 整理#D4 電腦基礎：向後跳躍與記憶體區域性\|D4 電腦基礎]]（只講 cache 概念） | 部分 |
| 時脈（GHz）與效能 | 1(e) | 1(d) | — | 沒教 |
| DRAM 斷電資料消失 | 1(g) | 1(f) | [[PROG1 Deck 1 整理#D1-Q2 電腦實際上在做什麼\|D1-Q2]]、[[PROG1 Deck 5 整理#D5-Q5 字元如何變成位元組並被保存\|D5-Q5]] | 有 |
| system software | 1(h) | 1(g) | — | 沒教 |
| statement 以換行分隔 | 1(i) | 1(h) | [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式\|D1-Q5]]（statement 的定義） | 部分 |
| 0／1、byte、bits 需要 interpretation | 1(j)–(n) | 1(i)–(l) | [[PROG1 Deck 1 整理#D1-Q3 電腦如何表示資訊\|D1-Q3]]、[[PROG1 Deck 2 整理#D2 電腦基礎：位元如何表示整數\|D2 電腦基礎]] | 有 |
| interpreter 與 machine language | 1(o) | 1(m) | [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式\|D1-Q5]] | 有，但說法和舊答案不同 |
| Python 跨平台 | 1(p) | 1(n) | — | 沒教 |
| logic error 與 IDE | 1(q) | 1(o) | [[PROG1 Deck 1 整理#D1-Q6 如果 AI 可以寫 code，為什麼還要學 Programming\|D1-Q6]] | 有 |
| `print()` 回傳 None、`end=` | Q2 | Q2 | [[PROG1 Deck 2 整理#D2 選讀：容易混淆的精確規則\|D2 選讀]]（None）；`end=` 沒教 | 部分 |
| 字串 × 整數、字串 + 字串 | Q2 | Q2 | [[PROG1 Deck 1 整理#D1-Q3 電腦如何表示資訊\|D1-Q3]]、[[PROG1 Deck 5 整理#D5-Q1 文字的意義從哪裡來\|D5-Q1]] | 有 |
| 位元運算 `^`、`\|`、`<<` | Q3 | Q3 | [[PROG1 Deck 3 整理#D3-Q2 多個條件如何一起工作\|D3-Q2]] 只提 `&`、`\|`、`~` 是位元運算 | 沒教 |
| for + range + 同時指派 | Q4 | Q4 | [[PROG1 Deck 4 整理#D4-Q2 for 如何逐項處理資料\|D4-Q2]]；同時指派沒教 | 部分 |
| for + while True + break、`/`、`%`、`sep=` | Q5 | Q5 | [[PROG1 Deck 4 整理#D4-Q4 不知道次數時，如何決定何時停止\|D4-Q4]]、[[PROG1 Deck 2 整理#D2-Q5 如何把數量關係寫成運算式\|D2-Q5]]；`sep=` 沒教 | 部分 |
| 一直乘 2 直到超過 | Q6 | Q6 | [[PROG1 Deck 4 整理#D4-Q4 不知道次數時，如何決定何時停止\|D4-Q4]] | 有 |
| if／elif／else + break（Fibonacci） | Q7 | Q7 | [[PROG1 Deck 3 整理#D3-Q4 超過兩種結果時，如何分類\|D3-Q4]]、[[PROG1 Deck 4 整理#D4-Q5 停止、略過與繼續前進有何不同\|D4-Q5]] | 有 |
| 改正語法錯誤 | — | Q7 | [[PROG1 Deck 1 整理#D1-Q6 如果 AI 可以寫 code，為什麼還要學 Programming\|D1-Q6]]、[[PROG1 Deck 3 整理#D3-Q3 條件如何選擇要執行的程式\|D3-Q3]] | 有 |
| 授課老師名字 | — | Q8 | — | — |

## 新講義沒教的舊考點

> [!tip] Claude 補充：指令集、RISC 與 CISC
> - **Instruction set（ISA）**：一種 CPU 看得懂的全部 machine instructions。不同處理單元可以有不同指令集（x86、ARM、RISC-V；GPU 也有自己的指令集），所以「Different processing units can have different instruction sets」是 T。
> - **RISC**（Reduced Instruction Set Computer）：指令少而簡單、長度固定，運算只在 register 上做，記憶體只用 load／store 存取。ARM、RISC-V 都是 RISC。
> - **CISC**（Complex Instruction Set Computer）：指令多、功能複雜、長度可變，一條指令可以直接操作記憶體。x86 是 CISC 的代表。
> - 所以「ARM follows the RISC design philosophy」是 T，「ARM follows the CISC design philosophy」是 F。
> - **同一個指令集，效能可以不同**：指令集只規定「有哪些指令」，不規定「怎麼做出來」。同樣是 x86 或 ARM，不同晶片的核心數、cache、時脈、內部設計（microarchitecture）都不同，所以「same instruction set can have different computing performance」是 T。

> [!tip] Claude 補充：時脈不等於效能
> 時脈（clock rate，例如 3.8 GHz）是每秒幾個 clock cycle；效能大致取決於「每個 cycle 能完成多少指令（IPC）× 時脈 × 核心數」，還有 cache 與記憶體速度。一顆 3.8 GHz 的舊 CPU 可能比 2.6 GHz 的新 CPU 慢。所以「3.8 GHz should have better performance」是 F，「3.8 GHz is possibly worse」是 T。

> [!tip] Claude 補充：記憶體階層，L1 小而快
> 越靠近 CPU 核心越小、越快、每 byte 越貴：register → L1 cache → L2 cache → L3 cache → RAM（DRAM）→ SSD／HDD。L1 每個核心一份、最小最快；L2 較大較慢；L3 通常更大，由多個核心共用。所以「L1 is smaller than L2」T、「L1 is faster than L2」T、「L1 is larger than L2」F。cache 與 RAM 是揮發性（volatile）記憶體，斷電資料就消失，所以「DRAM 的資料斷電後消失」是 T；SSD／HDD 是非揮發性（nonvolatile），斷電後仍保留。

> [!tip] Claude 補充：system software 與 application software
> **System software** 管理硬體、提供平台給其他程式用：作業系統（OS）本身、驅動程式（device drivers）、系統工具（utility programs）。**Application software** 幫使用者完成日常工作：瀏覽器、文書處理、遊戲。作業系統通常會附帶一些應用程式（例如 Windows 的記事本、小算盤），它們是作業系統「提供」的，卻是 application software。所以「Any software provided by your operating system is a system software」F；「A software provided by your operating system can be not a system software」T。

> [!tip] Claude 補充：Python 的 statement 與換行；跨平台
> - Python 用**換行**結束一個 statement（不像 C／Java 用 `;`），所以「The statements in Python are separated using the newline symbol」在 2021 參考答案是 T（考古題 A 卷上紅筆也寫 T）。細節：同一行也能用 `;` 放兩個簡單 statement，括號內的 expression 可以跨行，但考題要的是 T。
> - Python 程式能在 Windows、macOS、Linux 上跑，是因為**每個平台都有為它編譯的 Python interpreter**，不是「所有平台都有一模一樣的 interpreter」（不同 CPU 需要不同的 machine code，見 [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式|D1-Q5 Python 如何執行我們的程式]]）。所以那題是 F。

> [!tip] Claude 補充：`print()` 的 `sep=` 與 `end=`
> `print(值1, 值2, ..., sep=" ", end="\n")`：`sep` 是值與值之間放的字串（預設一個空白），`end` 是全部印完後補上的字串（預設換行）。`print()` 本身回傳 `None`。
> ```python
> print("A", "B", "C")
> print("A", "B", "C", sep="")
> print("A", "B", "C", sep="-")
> print("no newline", end="")
> print("!", end=".")
> print()
> x = print("inner", end=" ")
> print(x)
> ```
> ```text
> A B C
> ABC
> A-B-C
> no newline!.
> inner None
> ```
> （Claude 執行）`print(print(...))` 的順序：Python 先算外層 `print` 的引數，也就是先**執行**內層 `print`（內容先上螢幕），拿到它的回傳值 `None`，外層再把 `None` 印出來，最後接上外層的 `end`。

> [!tip] Claude 補充：位元運算 `&`、`|`、`^`、`~`、`<<`、`>>`
> 把整數寫成二進位，逐位運算（新講義 [[PROG1 Deck 3 整理#D3-Q2 多個條件如何一起工作|D3-Q2 多個條件如何一起工作]] 只說這組不是邏輯運算）：
>
> | 運算 | 意思 | 例子（1 = `0001`，10 = `1010`） |
> | --- | --- | --- |
> | `a & b` | AND：兩位都是 1 才是 1 | `1 & 10` = `0000` = 0 |
> | `a \| b` | OR：任一位是 1 就是 1 | `1 \| 10` = `1011` = 11 |
> | `a ^ b` | XOR：兩位不同才是 1 | `1 ^ 10` = `1011` = 11 |
> | `~a` | 每位反轉；對 Python int 等於 `-a - 1` | `~5` = −6 |
> | `a << n` | 左移 n 位，等於乘 $2^{n}$ | `1 << 10` = 1024 |
> | `a >> n` | 右移 n 位，等於 `a // 2**n` | `1024 >> 3` = 128 |
>
> ```python
> a = 1
> b = 10
> print(bin(a), bin(b))
> print(a & b, a | b, a ^ b)
> print(a << 10, 1024 >> 3)
> print(~5)
> print(2 ^ 3, 2 ** 3)
> ```
> ```text
> 0b1 0b1010
> 0 11 11
> 1024 128
> -6
> 1 8
> ```
> （Claude 執行）最後一行最重要：`2 ^ 3` 是 1（XOR），`2 ** 3` 才是 8。Python 的次方是 `**`（[[PROG1 Deck 2 整理#D2-Q5 如何把數量關係寫成運算式|D2-Q5 如何把數量關係寫成運算式]]）。

> [!tip] Claude 補充：同時指派 `a, b = b, a + b`
> 右邊**先全部用舊值算完**，再一起指派給左邊。拆成兩行就不一樣了：
> ```python
> a, b = 2, 3
> a, b = b, a + b
> print(a, b)
>
> a, b = 2, 3
> a = b
> b = a + b
> print(a, b)
> ```
> ```text
> 3 5
> 3 6
> ```
> （Claude 執行）第二段的 `b = a + b` 用到的是已經被改成 3 的 a。考古題 A4、A7、B4、B7 都靠這個規則：`a, b = b, a + b` 每做一次就往後走一個 Fibonacci 數。

## 考古題 A：Midterm I（年份不明）

封面：This exam contains 3 pages (including this cover page) and 7 questions. Total of points is 110.（Q1 51、Q2 5、Q3 8、Q4 10、Q5 12、Q6 12、Q7 12）

### A1 是非題（51 分）

> [!question] A1
> [True or False] Please answer the following questions with **T** for True and **F** for False:
> - (a) (3 points) Different processing units can have different instruction sets for their own purposes.
> - (b) (3 points) A CPU with the ARM instruction set follows the RISC design philosophy.
> - (c) (3 points) Generally, the size of the L1 cache is smaller than that of the L2 cache.
> - (d) (3 points) Generally, the access speed of the L1 cache is faster than that of the L2 cache.
> - (e) (3 points) The computing performance of a CPU running at 3.8 Ghz is possibly worse than that of a CPU running at 2.6 Ghz.
> - (f) (3 points) The processing units having the same instruction set can have different computing performance.
> - (g) (3 points) The data stored in the DRAM disappears after the power of the computer is switched off.
> - (h) (3 points) A software provided by your operating system can be not a system software.
> - (i) (3 points) The statements in Python are separated using the newline symbol.
> - (j) (3 points) All data in a computer is stored using sequences of 0s and 1s.
> - (k) (3 points) A one byte data means that it is stored using 8==(?)== 8 bits.
> - (l) (3 points) Any number stored in a computer can be represented using 8 bits without information loss.
> - (m) (3 points) Given a byte storing a sequence of 0s and 1s, we can interpret its meaning without other information.
> - (n) (3 points) Numbers and characters are stored in the computer as 0s and 1s, but the images and the music are not.
> - (o) (3 points) A python interpreter translates the high-level language to the machine language before the program can be executed.
> - (p) (3 points) A software written using python can be executed in different platforms because all of these platforms have exactly the same python interpreter.
> - (q) (3 points) Most of the logic errors can be directly identified by the python IDE, such as pycharm.

> [!solution]- Claude 解答：A1
> | 題 | 答案 | 卷上紅筆 | 理由 |
> | --- | --- | --- | --- |
> | (a) | T | T | 不同 architecture 有不同 instruction set（D1-Q5） |
> | (b) | T | T | ARM 是 RISC（2021 B1(b)「ARM follows CISC」答 F） |
> | (c) | T | T | L1 最小 |
> | (d) | T | T | L1 最快 |
> | (e) | **T** | F ✗ | 效能不只看時脈；2021 B1(d)「3.8 GHz should have better performance」答 F，兩題必須相反 |
> | (f) | T | T | 同指令集、不同實作（2021 B1(e) 答 T） |
> | (g) | T | T | DRAM 是揮發性記憶體（2021 B1(f) 答 T） |
> | (h) | **T** | F ✗ | OS 附帶的程式可以是應用軟體；2021 B1(g)「Any software provided by your OS is a system software」答 F，兩題必須相反 |
> | (i) | T | T | 2021 B1(h) 答 T |
> | (j) | T | T | 所有資料最後都是 0／1（D1-Q3） |
> | (k) | **T** | F ✗ | 1 byte = 8 bits（D2 電腦基礎） |
> | (l) | F | F | 8 bits 只有 256 種圖樣（2021 B1(j) 答 F） |
> | (m) | F | F | 要知道寬度與 encoding（2021 B1(k) 答 F） |
> | (n) | F | F | 圖片、音樂也是 0／1（2021 B1(l) 答 F） |
> | (o) | 有爭議 | T | 2021 B1(m) 參考答案給 T；新講義 D1-Q5 的說法會判 F（見下） |
> | (p) | F | F | 每個平台有自己的 interpreter（2021 B1(n) 答 F） |
> | (q) | F | F | logic error 通常不會報錯（D1-Q6；2021 B1(o) 答 F） |
>
> **(o) 為什麼有爭議**：舊課程把 interpreter 說成「把每一行 high-level 翻成 machine language 再執行」，所以 2021 參考答案給 T。新講義 [[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式|D1-Q5 Python 如何執行我們的程式]] 則明寫 CPython 先把 source 編譯成 bytecode，而「Python bytecode 不是 CPU native machine code」，照這個說法應判 F。W2 補課影片（Interpreter and Compiler）看的時候留意老師採哪一種說法；今年若再出這題，考前問老師或助教最保險。

### A2 print 裡的 print（5 分）

> [!question] A2
> (5 points) Please write down the content in the screen written by the following code:
> ```python
> a = "3"
> b = 5
> print(print(a*b,end=""),end = ".")
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 33333None.
> ```
> `a*b` 是 `"3" * 5` → `"33333"`（字串重複，[[PROG1 Deck 5 整理#D5-Q1 文字的意義從哪裡來|D5-Q1 文字的意義從哪裡來]]）；內層 `print` 先印 `33333`，`end=""` 不換行，回傳 `None`；外層印出 `None`，再接 `end="."`。卷上藍筆寫「33333.」，漏了 `None`。

### A3 位元運算（8 分）

> [!question] A3
> (8 points) Please write down the content in the screen written by the following code:
> ```python
> a = 1
> b = 10
> print(a^10,end = ",")
> print(a|b,end = ".")
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 11,11.
> ```
> 1 = `0001`、10 = `1010`。`^` 是 XOR，`0001 ^ 1010 = 1011` = 11；`|` 是 OR，也得 `1011` = 11。兩個 `print` 都不換行，`end` 分別補上 `,` 和 `.`。`^` 不是次方，見 [[#新講義沒教的舊考點]]。

### A4 for 迴圈與同時指派（10 分）

> [!question] A4
> (10 points) Please write down the content in the screen written by the following code:
> ```python
> a = 1
> b = 1
> for i in range(5):
>     a,b = a+b, a*b
> print(b,end = "")
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 330
> ```
> | 迴圈後 | a | b |
> | --- | --- | --- |
> | 開始 | 1 | 1 |
> | i = 0 | 2 | 1 |
> | i = 1 | 3 | 2 |
> | i = 2 | 5 | 6 |
> | i = 3 | 11 | 30 |
> | i = 4 | 41 | 330 |
>
> 每一輪右邊都用**舊的** a、b 算：`a+b` 和 `a*b` 同時算完才指派。`print` 在迴圈外，只印最後的 b。卷上藍筆答案看起來是 350，旁邊鉛筆追蹤得到 330；正確是 330。

### A5 質因數分解（12 分）

> [!question] A5
> (12 points) Please write down the content in the screen written by the following code:
> ```python
> Num = 1024
> CurNum = Num
> for i in range(2,Num):
>     count = 0
>     while True:
>         if CurNum % i == 0:
>             count = count +1
>             CurNum = CurNum/i
>         else:
>             break
>     if count != 0:
>         print(i,count,sep="")
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 210
> ```
> 這是在求 Num 的質因數分解：對每個 i，while 迴圈數 i 能整除 CurNum 幾次。$1024 = 2^{10}$：i = 2 時整除 10 次，CurNum 變成 1.0（`/` 讓它變 float：512.0、256.0……），`print(2, 10, sep="")` 印出 `210`。之後 `1.0 % i` 都不是 0，count 都是 0，不再印任何東西。陷阱是 `sep=""`：2 和 10 中間沒有空白。卷上答案 210 正確。

### A6 一直乘 2（12 分）

> [!question] A6
> (12 points) Please write down the content in the screen written by the following code:
> ```python
> Num =99864
> i = 2
> while True:
>     if i*2 > Num:
>         print(i)
>         break
>     else:
>         i = i*2
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 65536
> ```
> i 從 2 開始一直乘 2，直到「再乘一次就超過 Num」才印出：也就是不超過 Num 的最大 2 的次方。$2^{16} = 65536 \le 99864$，$2^{17} = 131072 > 99864$。卷上答案正確。

### A7 Fibonacci 找 index（12 分）

> [!question] A7
> (12 points) Please write down the content in the screen written by the following code:
> ```python
> Num = 6765
> index = 2
> a = 1
> b = 1
> while True:
>     if b == Num:
>         print(index)
>         break
>     elif b> Num:
>         print(-1)
>         break
>     else:
>         a, b = b, a+b
>         index = index +1
> ```

> [!solution]- Claude 解答（Python 驗證）
> ```text
> 20
> ```
> `a, b = b, a+b` 每次往後走一個 Fibonacci 數，index 跟著加 1：index 2 時 b = 1（第 2 項），index 3 時 b = 2，……，b 依序是 1, 2, 3, 5, 8, 13, …；6765 是第 20 項，所以印 20。若 Num 不是 Fibonacci 數，b 會跳過它，走 `elif b> Num` 印 −1。卷上答案 20 正確（紅筆是逐步追蹤）。

## 考古題 B：Fall 2021 Midterm I

封面：Computer Programming, Fall 2021, Midterm I. This exam contains 3 pages (including this cover page) and 8 questions. Total of points is 105.（Q1 45、Q2 5、Q3 8、Q4 8、Q5 12、Q6 12、Q7 10、Q8 5）

### B1 是非題（45 分）

> [!question] B1
> [True or False] Please answer the following questions with **T** for True and **F** for False:
> - (a) (3 points) Different processing units can have different instruction sets for their own purposes.
> - (b) (3 points) A CPU with the ARM instruction set follows the CISC design philosophy.
> - (c) (3 points) Generally, the size of the L1 cache is larger than that of the L2 cache.
> - (d) (3 points) A CPU running at 3.8 Ghz should have better computing performance compare to the CPU running at 2.6 Ghz.
> - (e) (3 points) The processing units having the same instruction set can have different computing performance.
> - (f) (3 points) The data stored in the DRAM disappears after the power of the computer is switched off.
> - (g) (3 points) Any software provided by your operating system is a system software.
> - (h) (3 points) The statements in Python are separated using the newline symbol.
> - (i) (3 points) All data in a computer is stored using sequences of 0s and 1s.
> - (j) (3 points) Any number stored in a computer uses 8 bits.
> - (k) (3 points) Given a byte storing a sequence of 0s and 1s, we can interpret its meaning without other information.
> - (l) (3 points) Numbers and characters are stored in the computer as 0s and 1s, but the images and the music are not.
> - (m) (3 points) A python interpreter translates the high-level language to the machine language before the program can be executed.
> - (n) (3 points) A software written using python can be executed in different platforms because all of these platforms have exactly the same python interpreter.
> - (o) (3 points) Most of the logic errors can be directly identified by the python IDE, such as pycharm.

> [!solution]- Claude 解答：B1（2021 手寫參考答案：TFFFT TFTTF FFTFF）
> | 題 | 參考答案 | Claude 判斷 | 理由 |
> | --- | --- | --- | --- |
> | (a) | T | T | 不同處理單元可有不同指令集 |
> | (b) | F | F | ARM 是 RISC，不是 CISC |
> | (c) | F | F | L1 比 L2 小 |
> | (d) | F | F | 效能不只看時脈 |
> | (e) | T | T | 同指令集、不同實作 |
> | (f) | T | T | DRAM 斷電資料消失 |
> | (g) | F | F | OS 也會附帶應用軟體 |
> | (h) | T | T | Python 以換行結束 statement |
> | (i) | T | T | 所有資料都是 0／1 |
> | (j) | F | F | 數字可用多個 bytes；Python int 不是固定 8 bits |
> | (k) | F | F | 需要知道 encoding |
> | (l) | F | F | 圖片、音樂也是 0／1 |
> | (m) | T | 有爭議 | 新講義說 bytecode 不是 machine code，會判 F（見 A1 的 (o)） |
> | (n) | F | F | 每個平台有自己的 interpreter |
> | (o) | F | F | logic error 通常不會被 IDE 抓到 |

### B2 print 裡的 print（5 分）

> [!question] B2
> (5 points) Please write down the content in the screen written by the following code:
> ```python
> a = "3"
> b = "5"
> print(print(a+b,end=""),end = ".")
> ```

> [!solution]- Claude 解答（Python 驗證，與參考答案一致）
> ```text
> 35None.
> ```
> `"3" + "5"` 是字串串接得 `"35"`；內層 `print` 印 `35` 不換行並回傳 `None`，外層印 `None` 再接 `.`。

### B3 位元運算（8 分）

> [!question] B3
> (8 points) Please write down the content in the screen written by the following code:
> ```python
> a = 1
> b = 10
> print(a<<10,end = ",")
> print(a^b,end = ".")
> ```

> [!solution]- Claude 解答（Python 驗證，與參考答案一致）
> ```text
> 1024,11.
> ```
> `1 << 10` 是把 1 左移 10 位，等於 $2^{10} = 1024$；`1 ^ 10` 是 XOR，`0001 ^ 1010 = 1011` = 11。

### B4 Fibonacci for 迴圈（8 分）

> [!question] B4
> (8 points) Please write down the content in the screen written by the following code:
> ```python
> a = 1
> b = 1
> for i in range(10):
>     a,b = b, a+b
> print(b,end ="")
> ```

> [!solution]- Claude 解答（Python 驗證，與參考答案一致）
> ```text
> 144
> ```
> (a, b) 依序：(1, 1) → (1, 2) → (2, 3) → (3, 5) → (5, 8) → (8, 13) → (13, 21) → (21, 34) → (34, 55) → (55, 89) → (89, 144)。`range(10)` 跑 10 次，最後 b = 144。

### B5 質因數分解（12 分）

> [!question] B5
> (12 points) Please write down the content in the screen written by the following code:
> ```python
> Num = 2056
> CurNum = Num
> for i in range(2,Num):
>     count = 0
>     while True:
>         if CurNum % i == 0:
>             count = count +1
>             CurNum = CurNum/i
>         else:
>             break
>     if count != 0:
>         print(i,count,sep=" ")
> ```

> [!solution]- Claude 解答（Python 驗證，與參考答案一致）
> ```text
> 2 3
> 257 1
> ```
> $2056 = 2^{3} \times 257$，257 是質數。i = 2 時整除 3 次（CurNum 變 257.0）；i = 257 時整除 1 次。和 A5 只差在 Num 與 `sep=" "`（中間有空白）。

### B6 一直乘 2（12 分）

> [!question] B6
> (12 points) Please write down the content in the screen written by the following code:
> ```python
> Num =15431543
> i = 2
> while True:
>     if i*2 > Num:
>         print(i)
>         break
>     else:
>         i = i*2
> ```

> [!solution]- Claude 解答（Python 驗證，與參考答案一致）
> ```text
> 8388608
> ```
> $2^{23} = 8388608 \le 15431543$，$2^{24} = 16777216 > 15431543$。

### B7 改正三個語法錯誤（10 分）

> [!question] B7
> (10 points) There are three syntax errors in the following program. Correct them and write down the program without these syntax errors.
> ```python
> Num = 6765
> index = 2
> a = 1
> b = 1
> while true:
>     if b = Num:
>         print(index)
>         break
>     elif b> Num:
>         print(-1)
>         break
>   else:
>         a, b = b, a+b
>         index = index +1
> ```

> [!solution]- Claude 解答（與參考答案一致）
> ```python
> Num = 6765
> index = 2
> a = 1
> b = 1
> while True:
>     if b == Num:
>         print(index)
>         break
>     elif b> Num:
>         print(-1)
>         break
>     else:
>         a, b = b, a+b
>         index = index +1
> ```
> 三個錯：`true` → `True`；`if b = Num` → `if b == Num`；`else:` 對齊 `if`／`elif`。改好後執行印出 `20`（就是 A7）。Python 3.13 實際報的錯（Claude 執行）：
> - `if b = Num:` → `SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?`
> - `else:` 縮排 → `IndentationError: unindent does not match any outer indentation level`（IndentationError 是 SyntaxError 的一種）
> - `while true:` → 其實不是 syntax error：`true` 只是一個沒定義的名稱，要等執行到那一行才出 `NameError: name 'true' is not defined`。考題把它算成 syntax error，照改就好。
>
> Python 執行前會先 parse 整個檔案，只要有 syntax error，整支程式一行都不會跑（[[PROG1 Deck 1 整理#D1-Q5 Python 如何執行我們的程式|D1-Q5 Python 如何執行我們的程式]]：A syntax error prevents that script from starting）。

### B8 授課老師（5 分）

> [!question] B8
> (5 points) Please write down the names of the two professors lecturing this course.

> [!solution]- Claude 解答
> 寫出當年兩位授課老師的中文全名；參考答案註明「有錯字不計分，對 1 個 2 分」。今年 Deck 的署名是 Guan-Ju Peng @ AM, NCHU。

> [!todo] Transcription check
> - 考古題 A 1(k)：「using」後面第一個字元被紅筆劃掉，最佳判讀是印刷時重複的「8」（標成 ==(?)==）；不影響題意（1 byte = 8 bits）。
> - 考古題 B7：掃描上 `else:` 比 `if`／`elif` 往左、比 `while` 往右，確切空白數看不出來，抄寫時用兩個空白；任何不對齊的位置都是同一個 IndentationError。
