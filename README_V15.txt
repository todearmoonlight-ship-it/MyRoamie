TripBook V15 Universal Alpha
===========================

核心功能
- 多旅程管理：新增、切換、編輯、刪除不同旅行。
- 舊東京 V14 資料相容：首次開啟會以目前東京行程建立第一個旅程，並讀取既有 tokyo-* 本機資料。
- 行程批次匯入：支援 XLSX / XLS / CSV，另可直接貼上 CSV 或 Tab 分隔資料。
- Google Maps：每一筆行程自動產生搜尋連結，每日自動組合路線；可另設定 Google My Maps。
- 城市天氣：依旅程主要城市，或當日行程的「城市」欄位，自動使用 Open-Meteo geocoding + forecast。
- 景點圖片：無照片的行程會自動從 Wikipedia / Wikimedia 搜尋圖片並存入 IndexedDB，成功後可離線查看；卡片保留來源連結。
- 航班 / 住宿 / 交通：可自行新增與編輯。
- 旅遊憑證：PDF / 圖片存在裝置 IndexedDB。
- 記帳：雙幣別、預算、收據照片、免費 Tesseract 快速 OCR。
- 收藏、購物清單、旅行日誌、準備清單、優惠券。
- 每趟旅行可獨立備份 / 匯入。
- PWA / Service Worker 離線快取。

批次行程欄位
必要：日期、時間、行程名稱
可選：地址、城市、簡介、備註、網址、預約網址
支援英文欄名 Date / Time / Title / Location / Address / City / Description / Note / Website / Reservation。

注意
1. Excel 解析器、OCR 第一次使用需有網路下載外部資源；Service Worker 成功快取後，後續可提高離線可用性。
2. 天氣、Google Maps、Wikipedia/Wikimedia 自動圖片需要網路。
3. Wikipedia/Wikimedia 自動圖片成功取得後會下載到本機 IndexedDB，並保留來源頁面連結。
4. Google Maps 每日路線使用公開 URL，不需要 Google Maps API Key；行程太多時只會取前 11 個點建立單一路線。
5. 建議正式旅行前，先在線上開啟一次 APP、Excel 匯入與 OCR，讓必要外部資源完成快取。
