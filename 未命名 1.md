# Phase 2：Template + Properties

### ① 這一階段要解決什麼

Phase 1 決定了「一筆交易 = 一篇筆記」，這階段要把每篇交易筆記的「固定欄位」訂下來，也就是設計 Properties（筆記最上面一小塊結構化資料）。有了固定欄位，之後查詢、加總、做 Dashboard 才有東西可以抓。同時做一個 Template（範本），讓你以後新增交易不用每次重打欄位名稱，才有機會做到 10-20 秒記一筆。

### ② 今天要做什麼

1. 確認 `記帳/交易` 資料夾已建立
2. 設定 → 核心外掛（Core plugins）→ 開啟「範本」（Templates），並指定範本資料夾，例如 `範本`
3. 在範本資料夾新增一篇筆記，命名為 `交易範本`
4. 貼上下面③的內容，測試新增第一筆交易

### ③ 直接貼上的內容

把新筆記切到「原始碼模式」（右上角 ... 選單，或 Ctrl/Cmd+E），在最上面貼上：

```yaml
---
date: {{date}}
type: 支出
category: 
account: 
amount: 0
note: 
---
```

貼完切回一般檢視，就會變成可編輯的 Properties 區塊。

**欄位說明**：

- `date`：交易日期，`{{date}}` 會自動帶入今天
- `type`：收入／支出／轉帳，先預設支出（最常用，省打字）
- `category`：分類，先留空——Phase 3 一起定義固定清單
- `account`：帳戶／支付方式，先留空
- `amount`：金額，永遠填正數就好
- `note`：備註，選填

之後要記一筆：在 `記帳/交易` 新增筆記（檔名不用想，用預設的就好，以後都靠 Properties 找資料，不是靠檔名），指令面板（Ctrl/Cmd+P）打 "Insert template" 插入範本，改掉 type/category/account/amount 即可。

### ④ 怎麼確認成功

新筆記上方出現灰底區塊，列著 date、type、category、account、amount、note 六個可編輯欄位。點每個欄位左邊的小圖示，確認 `date` 是「日期」類型、`amount` 是「數字」類型（其餘保持文字即可）。

### ⑤ 常見錯誤

- `amount` 沒設成數字類型：之後加總會出錯或加不起來
- 貼 YAML 時漏掉頭尾的 `---`：Properties 不會出現
- Templates 外掛沒開啟：指令面板找不到 Insert template
- 範本資料夾設定錯：插入時看不到剛存的範本

---

完成後跟我說，我們就進 **Phase 3：收入 / 支出 / 帳戶整理**。