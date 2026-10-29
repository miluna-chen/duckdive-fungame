# 浪人潛越 Duck Dive Trainer

WAVESLOW 浪漫衝浪教學的潛越訓練小遊戲。以第一視角迎向白浪花，依序抓準三個時機：下潛、踢板尾、拉板上浮。

## 網址

- GitHub Pages：https://miluna-chen.github.io/duckdive-fungame/
- LINE LIFF：https://liff.line.me/你的LIFF_ID（設定完成後）

## 檔案

- `index.html`：整個遊戲（畫面、音效、Logo 都在這一個檔案裡），可直接當 LIFF 的 Endpoint URL。

## 設定 LIFF ID

1. 在 LINE Developers Console 的 LINE Login channel 新增 LIFF app，Endpoint URL 填上面的 GitHub Pages 網址，Size 選 Full，打開 Share target picker。
2. 打開 `index.html`，搜尋 `YOUR_LIFF_ID`，換成拿到的 LIFF ID，commit 後 GitHub Pages 會自動更新。

沒有填 LIFF ID 時，遊戲一樣能在一般瀏覽器玩，只是不會出現「分享成績給朋友」按鈕。
