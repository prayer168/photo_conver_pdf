# 圖片批次轉 PDF（A1/A2/A3・多格式・無損畫質）

純前端離線工具：批次上傳圖片，**每張圖片各自產生一個 PDF**，畫質與尺寸完全不破壞。

## 特色

- **批次上傳**：拖放或點選，一次多張（JPG / PNG / HEIC / WebP / AVIF / GIF / BMP）
- **每張一個 PDF**：各自獨立檔案
- **無損畫質**：JPG / PNG 直接把原始圖片位元組嵌入 PDF（`embedJpg` / `embedPng`），不經 canvas 重繪、不重新壓縮，與原檔 100% 相同
- **更多格式**：WebP / AVIF / GIF / BMP 由瀏覽器解碼後以 PNG 無損重新封裝再嵌入，像素資料不變
- **HEIC 支援**：iPhone 照片可直接轉。PDF 容器本身不支援 HEIC、瀏覽器也無法直接保留它，所以 HEIC 必須先解碼再轉成高品質 JPEG（用最高品質 0.95，視覺上近乎無損）才能嵌入
- **可選紙張**：A1 / A2 / A3，直式或橫式，圖片等比例置中（另含邊距選項）
- **兩種輸出**：每張個別下載 ＋ 全部打包 ZIP 下載
- **檔名沿用原圖**：`photo1.jpg → photo1.pdf`
- **完全離線**：圖片不上傳，全程在瀏覽器本機處理

## 使用方式

直接開啟 `index.html`（建議 Chrome / Edge），或造訪 GitHub Pages 線上版。

## 技術

[pdf-lib](https://pdf-lib.js.org/) + [JSZip](https://stuk.github.io/jszip/) + [heic2any](https://github.com/alexcorvi/heic2any)（皆置於 `lib/`，無 CDN 依賴）。

---

設計者：陳賢宗（黑熊老師）
