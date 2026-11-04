但成功轉成 float 也還不夠，因為 float 能表示無窮大和 NaN：

> [!example] 範例：A number can be non-finite
> ```python
> import math
> print(math.isfinite(12.5))
> print(math.isfinite(0.0))
> print(math.isfinite(float("inf")))
> print(math.isfinite(float("nan")))
> ```

> [!solution]- 輸出
> ```text
> True
> True
> False
> False
> ```
> `math.isfinite()` 讓「距離必須有限」變成可以執行的檢查；只檢查負數不能完整排除非有限數。Conversion success does not guarantee a meaningful distance. 這個工具仍以一般課堂大小的輸入為範圍，不是保證所有極端有限數的後續算術都不會發生問題。


> [!example] 範例：Do these require the same thing?
> ```python
> valid = False
> duration_min = 60
> print(valid and duration_min <= 30 or duration_min == 60)
> print(valid and (duration_min <= 30 or duration_min == 60))
> ```

> [!solution]- 輸出
> ```text
> True
> False
> ```
> `and` 的優先序高於 `or`，所以第一行的最後一項可以繞過 `valid`；第二行要求 `valid` 成立後，括號裡的任何選項才有用。寫出括號並把句子讀出來（Read a complex condition aloud），確認它真的符合需求。


> [!failure] 故意錯誤的範例：every option needs its own comparison
> Prepared misconception example — this condition is not what it looks like.
> ```python
> duration_min = 45
> print(duration_min == 30 or 60)
> print((duration_min == 30) or (duration_min == 60))
> ```

> [!solution]- 輸出與分析
> ```text
> 60
> False
> ```
> 第一行不是「時間等於 30 或等於 60」的縮寫，而是把比較結果與數字 60 做 `or`。比較為假時，運算式得到 `60`；60 在 `if` 中被視為真（The number 60 is truthy; it is not an abbreviation for `duration_min == 60`）。因此它放在 `if` 裡會總是選到真分支，但不能不精確地說它「永遠回傳布林值 True」。

