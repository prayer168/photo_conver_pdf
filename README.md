# 圖片批次轉 PDF（A2 直式・無損畫質）

純前端離線工具：批次上傳圖片，**每張圖片各自產生一個 PDF**，畫質與尺寸完全不破壞。

## 特色

- **批次上傳**：拖放或點選，一次多張（JPG / PNG）
- **每張一個 PDF**：各自獨立檔案
- **無損畫質**：直接把原始圖片位元組嵌入 PDF（`embedJpg` / `embedPng`），不經 canvas 重繪、不重新壓縮，與原檔 100% 相同
- **A2 頁面**：直式 420×594mm（另含橫式與邊距選項），圖片等比例置中
- **兩種輸出**：每張個別下載 ＋ 全部打包 ZIP 下載
- **檔名沿用原圖**：`photo1.jpg → photo1.pdf`
- **完全離線**：圖片不上傳，全程在瀏覽器本機處理

## 使用方式

直接開啟 `index.html`（建議 Chrome / Edge），或造訪 GitHub Pages 線上版。

## 技術

[pdf-lib](https://pdf-lib.js.org/) + [JSZip](https://stuk.github.io/jszip/)（皆置於 `lib/`，無 CDN 依賴）。
