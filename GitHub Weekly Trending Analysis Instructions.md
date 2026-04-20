# GitHub Weekly Trending — Weekly Task

每週執行一次，產出一份 Markdown 週報並 commit 到這個 repo。

---

## 執行步驟

### Step 1｜抓取資料
瀏覽 https://trendshift.io/github-trending-repositories?trending-range=7&trending-limit=30 取得本週前 30 名 trending repositories。

### Step 2｜讀取上週報告
讀取 `reports/` 目錄中最新的 `.md` 檔，記錄上週 Top 10 的 repo 名稱，用於本週「回榜」標記。若目錄為空（第一次執行），略過此步驟。

### Step 3｜分析並撰寫報告
依照下方**報告格式**產出本週報告。撰寫原則：

- **以編輯視角呈現**——不只是列清單，而是說清楚「這週開源社群發生了什麼」
- **Top 10 固定納入**（以 trendshift 排名為準，不替換）
- **回榜標記**：若某 repo 上週也在 Top 10，在排名欄加上 `🔄`
- **個人興趣標記**（直接加在項目名稱後）：
  - 🧠 個人 AI 助理——記憶系統、RAG、個人化 LLM、可整合日記 / 履歷 / 個人資料的工具
  - 📚 PKM / 第二大腦——知識管理、語意搜尋、個人知識庫工具
- **個人精選**：從 Top 11–30 中，若有符合 🧠 或 📚 的項目，額外提取進入「個人精選」節

### Step 4｜寫入檔案
將報告寫入 `reports/YYYY-MM-DD.md`（以執行當天日期命名）。

### Step 5｜Commit & Push
```bash
git add reports/YYYY-MM-DD.md
git commit -m "weekly: YYYY-MM-DD trending report"
git push
```

---

## 報告格式

````markdown
# GitHub Weekly Trending — YYYY-MM-DD

> 資料來源：[trendshift.io](https://trendshift.io/github-trending-repositories?trending-range=7&trending-limit=30) ｜ 觀測範圍：Top 30 ｜ 報告日期：YYYY-MM-DD

## 本週大故事

（100 字以內。說明本週的主旋律：有沒有 breakout repo？哪個技術突然爆發？社群在討論什麼？
用說故事的方式寫，不要只是描述清單。專有名詞保留英文原文。）

## Top 10 速覽

| 排名 | 項目 | 是什麼 | 為什麼這週爆紅 |
| :--- | :--- | :--- | :--- |
| 1 | [Repo Name](URL) | 一句話描述用途 | 觸發點：新版本 / 某篇文章 / KOL 推薦 / 技術突破 |
| 2 🔄 | [Repo Name](URL) | 一句話描述用途 | 回榜，上週排名 3，本週持續受關注因為⋯⋯ |

（🧠 或 📚 標記直接加在項目名稱後方）

## 個人精選

> 此節只在 Top 11–30 出現 🧠 或 📚 相關項目時才產出，否則整節省略。

### [Repo Name] 🧠（本週排名：XX）

- **它在做什麼：** 簡述核心功能與技術實作。
- **跟我的方向有什麼關係：** 說明與個人 AI 助理 super project 或 PKM 的關聯。
- **值得注意的技術選擇：** 架構、stack、或設計決策中最值得學習的點。
````
