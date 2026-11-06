
| 轉型                       | 結果                      | 要記住的事                        |
| ------------------------ | ----------------------- | ---------------------------- |
| `int(12.9)`              | `12`                    | Float → int **向零截斷**，不是四捨五入。 |
| `int("12.5")`            | `ValueError`            | 這段文字不是 int() 能解析的整數格式。       |
| `int(-1.7)`              | `-1`                    | 向零截斷（truncate toward zero）。  |
| `round(2.5), round(3.5)` | `2, 4`                  | 精確中間值採靠偶數的捨入（tie to even）。   |
| `-7 // 3`                | `-3`                    | 地板除法                         |
| `10**3**5**7`            | `10 ** (3 ** (5 ** 7))` | 右結合                          |
| `-3**2`                  | `-9`                    |                              |

> [!example] 範例：display, result, and statement are different
> ```python
> result = print("Hello")
> print(result)
> value = 12.345
> label = f"{value:.2f}"
> print(label)
> print(type(label))
> ```

> [!solution]- 輸出
> ```text
> Hello
> None
> 12.35
> <class 'str'>
> ```
> 第一個 Hello 是 print 的顯示效果；`result` 收到的是該函式呼叫的回傳值 `None`。`print()` returns `None`. An assignment statement has no expression result; it does not "return None." f-string 的結果是字串，所以 `label` 不是已經被四捨五入的數值變數。