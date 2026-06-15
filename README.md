# Vito · 個人簡歷 — LUXKEY International

金曜石國際（LUXKEY International）短影音策略顧問 Vito 的單頁個人簡歷 / 品牌簡介。

採用 LUXKEY 設計系統：vermillion × teal 高對比、cream 紙感、ink 為底的編輯風格色塊版面。

## 檔案結構

| 檔案 | 說明 |
| --- | --- |
| `Vito - 個人簡歷.html` | 主要頁面（互動版，含可拖曳填圖的 `<image-slot>`） |
| `Vito - 個人簡歷-print.html` | 列印 / PDF 輸出版本 |
| `colors_and_type.css` | LUXKEY 設計系統的色彩與字體 tokens（單一真實來源） |
| `image-slot.js` | `<image-slot>` 自訂元素：使用者可拖放圖片，並透過 sidecar 持久化 |
| `.image-slots.state.json` | 已填入圖片的持久化資料（base64 WebP） |

## 線上瀏覽

本專案透過 GitHub Actions 自動部署到 GitHub Pages。每次推送到 `main` 都會重新發佈：

> https://vitokok-lab.github.io/Resume/

`index.html` 即為主簡歷頁面;`.nojekyll` 確保 `.image-slots.state.json` 等檔案會被原樣發佈,讓嵌入的圖片正常顯示(線上為唯讀,無法再拖曳更換)。

## 本地預覽

由於 `image-slot.js` 透過 `fetch()` 讀取 `.image-slots.state.json`，請以 HTTP 伺服器開啟，避免 `file://` 的 CORS 限制：

```bash
python3 -m http.server 8000
# 開啟 http://localhost:8000/Vito%20-%20個人簡歷.html
```

## 頁面區塊

主視覺 Banner → Hero → 資本市場思維 → 我在做什麼 → 核心案例 → FLYWHEEL 方法論 → 實際成績 → 合作方式 → 精選案例 → 服務項目 → 顧問資歷 → 團隊分工 → CTA 聯絡 → Footer。
