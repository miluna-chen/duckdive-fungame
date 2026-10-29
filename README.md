# 浪人潛越 Duck Dive Trainer

WAVESLOW 浪漫衝浪教學的潛越訓練小遊戲。以第一視角迎向白浪花，依序抓準三個時機：下潛、踢板尾、拉板上浮。

## 網址

- GitHub Pages：https://miluna-chen.github.io/duckdive-fungame/
- LINE LIFF：https://liff.line.me/2012274845-HP96ecgc

## 檔案

- `index.html`：整個遊戲（畫面、音效、Logo 都在這一個檔案裡），可直接當 LIFF 的 Endpoint URL。

## 設定 LIFF ID

1. 在 LINE Developers Console 的 LINE Login channel 新增 LIFF app，Endpoint URL 填上面的 GitHub Pages 網址，Size 選 Full，打開 Share target picker。
2. LIFF ID 寫在 `index.html` 的 `const LIFF_ID`，目前是 `2012274845-HP96ecgc`。換 LIFF app 時改這一行，commit 後 GitHub Pages 會自動更新。

在一般瀏覽器開也能玩，只是不會出現「分享成績給朋友」按鈕（這個按鈕只在 LINE 裡出現）。
