# 📘 gitlesson — Git 練習 × 偏鄉智慧藥局早期版本

這個 repo 一開始是用來練習 Git 的網頁專案，目前內容是 **偏鄉智慧藥局聯合調度系統** 的早期**純前端**版本。

> 後續完整版本（Node.js + SQLite 後端、疾管署資料 ETL）在 👉 [SmartPharma](https://github.com/Johnnnny0823/SmartPharma)

---

## 💊 專案內容

以桃園市大溪、復興區為場景，串連各家特約藥局的庫存，提供：

- 民眾線上預約慢性病連續處方箋
- 藥局之間的跨店庫存查詢與雙向調撥
- 依天氣（晴天、大雨、颱風）調整偏鄉據點的安全庫存
- 調撥物流進度追蹤

藥品、庫存與金流皆為模擬資料。

---

## 🆚 與 SmartPharma 的差異

| | 本 repo（早期版） | [SmartPharma](https://github.com/Johnnnny0823/SmartPharma)（完整版） |
|---|---|---|
| 資料儲存 | 瀏覽器 `localStorage` | SQLite（透過 Express API） |
| 後端 | 無（另附早期的 `api.jsp` 草稿） | Node.js + Express |
| 疫情資料 | 無 | 疾管署開放資料 ETL + 季節性疾病預測圖 |

---

## 🚀 執行方式

頁面會用 `fetch` 讀取 `mock_nhi_data.json`，直接雙擊 HTML 會被瀏覽器擋下，需要開一個本機伺服器：

```bash
python -m http.server 8000
```

然後打開 http://localhost:8000/index.html 。

---

## 📁 檔案說明

| 檔案 | 說明 |
|---|---|
| `index.html` / `script.js` / `style_final.css` | 前端介面與邏輯 |
| `mock_nhi_data.json` | 模擬藥品與各藥局庫存 |
| `mock_data_generator.js` | 依健保署藥品主檔格式產生模擬資料 |
| `database_schema.sql` | 早期的 MySQL 資料庫設計 |
| `api.jsp` | 早期的 JSP 版 API 草稿 |

---

## 🌱 Git 練習紀錄

這個 repo 的 commit 歷史保留了學習 Git 的過程：從最早的個人網頁練習（多頁 HTML/CSS），到最後換成藥局系統。想看歷史可以用：

```bash
git log --oneline --stat
```
