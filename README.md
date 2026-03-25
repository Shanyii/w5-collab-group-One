# 第五週 Pull Request 協作練習

這是第五週的分組作業，練習完整的 Pull Request 協作流程。
**重點不只是寫程式，而是 PR 描述、Code Review 與回應 review 的過程。**

---

## 基本資料

| 項目        | 填寫           |
| ----------- | -------------- |
| 組別        | 第 1 組       |
| 組員        | 楊姍頤 D1185397，林瑞城 D1123896，黃柏豪 D1249756，沈靖恩 D1321025 |
| GitHub Repo | https://github.com/Shanyii/w5-collab-group-One.git |
| 報告日期    | 2025 / 03 / 25 |

---

## 快速開始

**組長**

1. Fork 該 repo → 命名為 `w5-collab-第X組` → **Create fork**
2. Settings → Branches → Add rule：`main`，勾選 **Require PR + 2 approvals**
3. Settings → Collaborators → 邀請所有組員
4. 把 repo URL 告訴組員

**組員**

```bash
git clone https://github.com/組長帳號/w5-collab-第X組.git
cd w5-collab-第X組
git checkout -b feature/member-a   # 依角色選擇
```

---

## Review Comment 範例

每個 PR 至少需要 **2 位成員 approve** 才能 merge。
Review 時留下有意義的 comment，以下是常見的寫法：

**✅ 肯定 / Approve 常用語**

```
LGTM!
```

```
LGTM! 邏輯很清楚，merge 沒問題 👍
```

```
Ship it! 🚀
```

```
Nice work! 時間戳格式選得很好，HH:MM 簡潔又夠用。
```

```
Looks good to me, 就這樣 merge 吧。
```

**💬 提問或確認意圖**

```
nit: 這個變數名稱可以再清楚一點嗎？（nit = nitpick，小建議，不影響 approve）
```

```
Esc 清空是清空輸入框還是整個對話？PR 描述可以補一下。
```

```
這裡用 querySelectorAll 是有考慮到未來擴充嗎？好奇問一下 😄
```

```
optional: 可以加 localStorage 記住 dark mode 狀態，但不一定要這次做。
```

**🔧 建議修改**

```
nit: `d` 這個變數名不太好懂，建議改成 `chatBox`。
```

```
這裡有重複的程式碼，可以抽成一個 function，會更好維護。
```

```
minor: clearChat 沒有 confirm 視窗，使用者可能會不小心清掉，要不要加個確認？
```

**⚠️ 指出問題（Request changes）**

```
這裡如果輸入是空字串會壞掉，需要先加個判斷再 merge。
```

```
WIP? 這個 function 好像還沒實作完，先確認一下？
```

```
blocking: 這個會影響其他功能，需要修一下才能 merge。
```

---

**常見縮寫對照**

| 縮寫     | 全文               | 意思               |
| -------- | ------------------ | ------------------ |
| LGTM     | Looks Good To Me   | 沒問題，可以 merge |
| nit      | Nitpick            | 小建議，不強制修改 |
| WIP      | Work In Progress   | 還沒做完           |
| PTAL     | Please Take A Look | 請幫我看一下       |
| TBD      | To Be Determined   | 待確認             |
| optional | —                 | 可做可不做的建議   |
| blocking | —                 | 必須修才能 merge   |

> **記住**：review 是討論，不是批判。指出問題時說明原因，建議修改方向，而不是直接否定。

---

## PR 描述規範（每個 PR 都要填）

```markdown
## 做了什麼
- （說明新增或修改了什麼）

## 如何測試
1. （步驟一）
2. （步驟二）

## 截圖
（附上修改後的畫面截圖）
```

---

## 完整協作流程

```
組長：Fork 模板 → 設 Branch Protection → 邀請組員
  ↓
各組員：clone → 建分支 → 完成任務 → push → 開 PR（填完整描述）
  ↓
組長：Review PR → 留 comment → Approve
  ↓
組員：回應 comment → 修改 → re-push
  ↓
組長：Merge（解決 conflict）
  ↓
全組：git pull origin main → 確認成果
```

---

## 一、協作分工

| 組員姓名 | 負責分支 | 主要修改內容 | PR 連結 | 是否完成 |
| -------- | -------- | ------------ | ------- | -------- |
|  楊姍頤  |  `main ` |     修改標題、撰寫README     |    (https://github.com/Shanyii/w5-collab-group-One.git)     | ✅  |
|  林瑞城  | `member-a` |    在 .message 裡加上時間戳 span           |    (https://github.com/Shanyii/w5-collab-group-One/pull/2)     | ✅  |
|  沈靖恩  | `member-b `| 新增對話刪除按鈕 | https://github.com/Shanyii/w5-collab-group-One/tree/mamber-b | ✅ |
|          |          |              |         | ✅ / ❌  |
|      黃柏豪    |  feature/member-d        | 深色模式頁面樣式與切換邏輯             |    https://github.com/Shanyii/w5-collab-group-One/pull/4     | ✅  |

---

## 二、截圖紀錄

### 2-1 PR 列表截圖（必填）

> 截圖：GitHub repo → Pull requests，顯示所有 PR 的狀態（open / merged）

<img width="865" height="277" alt="image" src="https://github.com/user-attachments/assets/79921a26-4717-492f-8977-284e36f58ffa" />
<img width="865" height="229" alt="image" src="https://github.com/user-attachments/assets/632f31a4-1049-4aa1-9839-3a9ddb9323dd" />

---

### 2-2 PR 描述截圖（必填）

> 截圖：其中一個 PR 的描述頁面，顯示完整的「做了什麼 / 如何測試」內容

<img width="865" height="764" alt="image" src="https://github.com/user-attachments/assets/64658d93-42b2-488e-a706-ba4a3c53eef8" />

---

### 2-3 Code Review 截圖（必填）

> 截圖：Files changed 頁面，顯示 inline comment 的留言

<img width="865" height="361" alt="image" src="https://github.com/user-attachments/assets/e686ca4d-8d2c-4773-9af6-f2ca5070a144" />

---

### 2-4 Merge 成功截圖（必填）

> 截圖：某個 PR 頁面顯示「Merged」紫色標籤

<img width="865" height="705" alt="image" src="https://github.com/user-attachments/assets/0a4f176d-5577-4331-b811-e9f77615efb2" />

---

### 2-5 最終成果截圖（必填）

> 截圖：用瀏覽器打開 `index.html`，顯示所有功能整合完成的畫面

與chatbot對話
<img width="865" height="408" alt="image" src="https://github.com/user-attachments/assets/fc638fa2-a0fd-4f0f-bbb7-fa4360411986" />
按下刪除對話後
<img width="865" height="399" alt="image" src="https://github.com/user-attachments/assets/0575525d-811d-47e3-9caa-63dba99c7f44" />

---

## 三、遇到的問題與解決方式

**問題 1：** Git 無法 commit，顯示 "Author identity unknown"

**解決方式：** 使用 `git config user.name` 和 `git config user.email` 設定使用者身份

---

**問題 2：** Git 無法 commit，顯示 "Author identity unknown" 設定 git config user.name 和 git config user.email

解決方式：設定 git config user.name 和 git config user.email

---

## 四、個人心得

> 每位組員各寫 2–3 句，說明這週對 PR / Code Review 的理解或感想

**楊姍頤：** 這周的上課過程交會我更多關於gitnhb的使用方式，還有整理branch的方法。

**林瑞城：** 這的課程非常有趣，讓我可以了解到PR整體的過程，不再只是單人協作而已，了解整體的過程。

**沈靖恩：** 今天的課程讓我更熟悉如何在多人合作時，在專案中建立新分支、pull request，以及了解code review在多人合作之大型專案中的重要。

**黃柏豪：** 這次作業與小組練習不僅讓我更加掌握如何使用 GitBash 和 Github，Pull Request 設定與 Merge 的流程，也讓我理解到 Code Review 與團隊協作的重要性。沒有 Stand-up meeting 即便是小小的團隊協作也是一大挑戰。

---

## 五、自評與互評

| 評分項目 | 分數（1–5） | 說明 |
|---------|-----------|------|
| PR 描述完整度 |5 | 組員都有將進度內的修改如期完成|
| Review comment 品質 |3 | 我們只有意思意思的寫一小部分評論|
| 回應 review 的態度 |5 | 我們當場溝通比較多|
| 最終成果完整度 | 5| 所有進度都有如期完成|

這週覺得最有挑戰的是？

- [ ] 寫 PR 描述
- [ ] 給 Code Review
- [ ] 回應 review 並修改
- [✅ ] 解決 Merge Conflict
- [ ] 其他：＿＿＿

---

*報告由全組共同完成，commit 到 main 後繳交。*
