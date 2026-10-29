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

## 點擊追蹤

### 來源連結
在 LIFF 網址後面加 `?src=名稱`，就能分辨玩家從哪裡點進來：

| 用在哪裡 | 連結 |
|---|---|
| LINE 圖文選單 | https://liff.line.me/2012274845-HP96ecgc?src=line_richmenu |
| LINE 群發訊息 | https://liff.line.me/2012274845-HP96ecgc?src=line_message |
| IG 限動 | https://liff.line.me/2012274845-HP96ecgc?src=ig_story |
| Facebook | https://liff.line.me/2012274845-HP96ecgc?src=facebook |

### Google Analytics 4
`index.html` 裡的 `const GA_ID = ''` 填入 GA4 評估 ID（G- 開頭）後開始追蹤，留空則不追蹤。會送出的事件：

- `page_view`：打開遊戲（附 `src` 來源、`opened_in` 是在 LINE 裡還是一般瀏覽器）
- `level_select`：切換關卡（`level`）
- `game_start`：開始一局（`level`，重玩時多一個 `retry`）
- `game_result`：一局結束（`level`、`result`、`grade`、`cause`）
- `share_click`：按「分享成績給朋友」

不會送出玩家的 LINE 名稱或 ID。要在 GA4 報表裡用 `src`、`level`、`grade` 分組，需先在 GA4 管理 → 自訂定義 → 建立「事件範圍」的自訂維度。
