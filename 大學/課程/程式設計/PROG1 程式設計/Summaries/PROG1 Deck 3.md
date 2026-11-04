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

