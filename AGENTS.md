# AGENTS.md — StyleNote

## 1. 專案定位與目標
StyleNote 是繁體中文的韓系日常穿搭知識網站，提供可參考、可拆解、可實際運用的全身穿搭靈感。網站以韓系低彩度配色、柔和簡約、校園休閒、都會俐落及日常穿搭公式為主要內容。AI 每次新增或修改內容前，必須先閱讀本檔案與 README.md，並沿用既有網站架構。

## 2. 技術規範
- 使用 HTML5、CSS3 與原生 JavaScript，不使用前端框架或後端服務。
- 使用繁體中文、UTF-8 編碼及台灣常用詞彙。
- 網站需可部署於 GitHub Pages；所有站內連結與資源路徑使用相對路徑。
- 不新增需要 API Key、登入、付費服務或私人伺服器才能運作的功能。
- 不任意更改既有資料夾結構、檔名或導覽路徑；若有必要，必須同步更新所有引用位置及 README.md。

## 3. 專案結構
- `index.html`：首頁、品牌介紹、精選 OOTD、專題入口及穿搭公式摘要。
- `pages/color-guide.html`：韓系低彩度配色與實際穿搭配色示例。
- `pages/style-guide.html`：柔和簡約、校園休閒、都會俐落及韓系街頭風格。
- `pages/wardrobe.html`：韓系基本款衣櫥、衣物盤點及單品搭配。
- `pages/outfit-formulas.html`：依日常情境拆解全身穿搭公式。
- `css/style.css`：全站共用樣式與響應式版面。
- `js/main.js`：全站共用互動功能。
- `images/ootd/ig-outfit-grid.jpg`：使用者提供之 Instagram 個人檔案截圖裁切素材表。
- `README.md`：專案介紹、檔案結構及 GitHub Pages 部署說明。

## 4. 韓系視覺設計規範
- 背景暖白 `#FAF8F6`；主要文字深灰 `#292729`。
- 強調色灰粉 `#B88E8B`；輔助霧粉 `#F0E9E7`；柔灰邊框 `#E9E2DF`。
- 整體氛圍乾淨、柔和、低彩度、留白充足，接近韓國日常穿搭編輯網站。
- 避免美式大型商業街拍、過度強烈的色彩、過度裝飾、漸層與大量動畫。
- 保持頁首、導覽列、卡片、標題層級及頁尾在各頁一致。
- 桌機版內容置中；手機版需適應 375px 以上寬度，不得產生水平捲動。

## 5. 圖片與 OOTD 素材規範
- 優先使用實際全身穿搭照片；其次為半身搭配、鞋包細節及單品特寫。不可用空衣架、店面或純商品照取代穿搭示範。
- 首頁應呈現多張穿搭照片；各主題頁至少安排 3 張與內容直接相關的圖片或視覺例子。
- `images/ootd/ig-outfit-grid.jpg` 是使用者在課堂作業對話中提供的 Instagram 截圖裁切素材，不得描述為網站原創攝影或自行拍攝。
- 目前圖片素材為 4×4 圖片表，HTML 透過 `.ootd-image` 區塊與 CSS `background-position` 顯示各個裁切格。新增或調整裁切位置時，必須同步檢查 CSS 定位及每張照片是否完整。
- 圖片應保持清晰；不可使用過度壓縮、縮圖放大或含糊的圖片。圖片更換後需實際開啟 GitHub Pages 確認，不可只以 GitHub 上傳成功作為完成依據。
- 每張圖片須提供有意義的替代文字（alt）、圖說及來源說明。使用使用者提供素材時，標示「使用者提供之 Instagram 截圖裁切／穿搭參考」。
- 不可未經授權直接抓取私人帳號內容；新增素材應由使用者提供，或使用可合法使用且可標示來源的圖片。
- 同一頁避免重複使用同一張照片；照片內容須與相鄰文字及穿搭公式相符。

## 6. 內容撰寫規範
- 每頁只使用一個主要 H1，並有清楚導言。
- 主題頁至少包含 3 個有實質內容的 H2 區塊。
- 內容需具體說明單品、版型、配色、比例、場合或搭配公式，避免只有抽象形容詞。
- 穿搭示例盡可能使用「上身＋下身＋鞋款＋配件」拆解，並補充適合情境或替換方式。
- 每個主題頁提供實用提醒及至少 2 個站內延伸連結。
- 文字使用繁體中文與台灣用語，避免不必要的中英混雜。

## 7. AI 新增與修改流程
1. 先閱讀本檔案、README.md 及欲修改的現有頁面。
2. 先確認需求影響哪些頁面、樣式、圖片及導覽連結，再開始修改。
3. 沿用既有頁首、頁尾、共用 CSS、JavaScript 與命名規則。
4. 新增頁面時放在 `pages/`，並同步更新首頁入口、導覽列及 README.md。
5. 新增或更換圖片時，先確認解析度、裁切範圍、來源、alt 與圖說。
6. 修改後檢查桌機與 375px 手機版、圖片載入、文字溢位、所有內部連結及瀏覽器錯誤。
7. 若圖片或頁面尚未在公開網站驗證，不可宣稱部署完成。

## 8. GitHub 與發布規範
- Repository：`PCCC-Pc/stylenote`。
- 使用 `main` 分支，GitHub Pages 從根目錄發布。
- Commit message 應清楚描述修改內容。
- 發布後實際測試首頁及全部四個主題內頁，確認導覽、圖片、相對路徑及手機版顯示。
- 圖片檔名與路徑若有變動，必須同步更新所有 HTML/CSS 引用；不可只改檔名而忽略引用位置。

## Language

When the conversation is in Chinese, write Traditional Chinese as used in Taiwan, with Taiwanese vocabulary and phrasing rather than mainland Chinese terms. Traditional characters alone are not enough: whenever a word has a different everyday form for in Taiwan and in mainland China, especially in software and computing, use the Taiwanese one.

Technical terms with no settled Taiwanese translation stay in English rather than being forced into a translation nobody says.

## Command Output

Command output here is condensed by rtk to save tokens, keeping every signal and dropping costly noise. Treat it as the complete result: run commands normally, and batch related commands into one call to avoid extra turns. Truncated results state their recovery path in their own output — a `[+N hidden: rtk recall <hash>]` marker means `rtk recall <hash>` returns the elided part (`--full` for everything, `--grep` to filter). Re-run a command as `rtk bypass <cmd>` only when its result is unusable: empty output was clearly expected, contradicting its exit code, or garbled.
