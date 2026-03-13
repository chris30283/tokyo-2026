# 🌸 2026 東京賞櫻之旅 (Tokyo Sakura Trip App)

這是一個專為 **2026 年 3 月東京與箱根賞櫻行** 所打造的「單頁式旅遊手冊 App (Single-file PWA)」。

無需下載、無需登入、無後端伺服器。透過瀏覽器即可運作，並利用 LocalStorage 技術在手機上永久保存你的個人打勾紀錄與記帳資料。

---

## ✨ 核心功能 (Key Features)

### 📅 智慧行程管理

* **5 天 4 夜完整動線**：新宿、箱根（一泊二食）、東京鐵塔、原宿、表參道、上野等詳細規劃。
* **🚦 自動導航 (Smart Highlight)**：App 偵測現在時間，自動將「進行中」的行程標示為粉紅色呼吸燈，打開 App 自動定位到當下行程。
* **備案切換**：Day 2（箱根午餐三選一）與 Day 5（淺草 vs 千鳥之淵賞櫻），視天氣與花況一鍵切換。

### 🧰 實用旅遊工具

* **🚕 給司機看 (Taxi Card)**：一鍵跳出超大字體的日文地址與敬語，解決與日本司機的溝通障礙。
* **🗣️ 手指日文發音**：內建 TTS (Text-to-Speech) 引擎，點擊喇叭按鈕即可用標準日語唸出需求（含餐廳、購物、緊急三大類）。
* **🌐 即時翻譯**：語音輸入（中→日 / 日→中），透過 Gemini API 翻譯後自動 TTS 朗讀，附複製按鈕。
* **🎫 票券收納夾**：集中管理浪漫特快座位、飯店訂單號、YORONIKU 訂位碼、VJW 入境通關連結等，一鍵複製。
* **🗺️ 行李與電梯攻略**：針對攜帶大行李的移動日，提供精準的「電梯入口」與「無障礙路徑」指引。
* **🧳 箱根行李托運**：D2/D3 托運流程完整寫入行程，附官網連結與截止時間提醒。
* **✈️ 航班即時追蹤**：透過 AviationStack API 顯示即時起降狀態、登機門與誤點資訊（需設定 API Key）。
* **🤖 Robot AI 旅遊助理**：Gemini 多輪對話，支援圖片辨識（菜單、告示牌、藥品、地圖），可在旅途中隨時提問。

### 💰 購物與記帳

* **🛍️ 必買清單**：可勾選追蹤戰利品，一鍵分享清單。
* **💸 記帳助手**：快速記錄消費（食／衣／住／行），自動計算總花費並換算台幣，支援編輯與一鍵刪除。
* **📊 分類長條圖**：視覺化各類別花費比例。
* **📤 分享功能**：一鍵將記帳明細複製為文字，方便貼到 Line 群組備份。

### 🌤️ 天氣穿搭建議

* 即時抓取東京天氣（Open-Meteo API），顯示溫度、天氣描述。
* 點擊天氣小卡展開詳細穿搭建議，根據溫度、雨況、風速動態生成。

---

## 🗓️ 行程概覽

| 天 | 日期 | 主題 | 亮點 |
|---|---|---|---|
| D1 | 3/14 (六) | 新宿之夜 | JL0802 抵 NRT → N'EX → 新宿 APA Check-in → 晚餐 |
| D2 | 3/15 (日) | 箱根溫泉 | 浪漫特快 E268 → 湯本行李托運 → 午餐三選一 → 雕刻之森 → 水之音一泊二食 |
| D3 | 3/16 (一) | 海盜船 & 新宿 | 大涌谷 → 海盜船 → 新宿東口逛街（Biju Mam、Lumine Est）→ 大塚居酒屋 |
| D4 | 3/17 (二) | 表參道 & 東京鐵塔 | 明治神宮 → 原宿飾品掃貨（Pocket、Laforet）→ 貓街 → 表參道 → YORONIKU → 東京鐵塔 |
| D5 | 3/18 (三) | 最後一天 | 淺草 or 千鳥之淵賞櫻 → Skyliner → JL0809 返台 |

---

## 📱 如何安裝到手機 (iOS/Android)

為了獲得最佳體驗（全螢幕、無網址列、資料永久儲存），請務必將此網頁加入主畫面。

### iOS (iPhone)

1. 使用 **Safari** 打開網頁。
2. 點擊下方選單中間的 **「分享」** 按鈕（方框向上箭頭）。
3. 往下滑，選擇 **「加入主畫面 (Add to Home Screen)」**。
4. 點擊右上角的「新增」。
5. 桌面上會出現一個櫻花圖示的 App，點開即可使用！

### Android (Chrome)

1. 使用 **Chrome** 打開網頁。
2. 點擊右上角的 **「...」** 選單。
3. 選擇 **「安裝應用程式」** 或 **「加到主畫面」**。

---

## 🔑 API Key 設定（選填）

App 部分功能需要自行申請 API Key，在右上角「⚙️ 設定」中填入：

| 功能 | API | 申請連結 | 費用 |
|------|-----|----------|------|
| AI 對話、圖片辨識、即時翻譯 | Google Gemini API | [aistudio.google.com](https://aistudio.google.com/) | 免費方案 |
| 航班即時追蹤 | AviationStack | [aviationstack.com](https://aviationstack.com/) | 免費方案 |

### Gemini 模型選擇

App 內建三個免費模型一鍵切換：

| 模型 | 免費額度 | 適合場景 |
|------|----------|----------|
| ⚡ Gemini 2.5 Flash | 250 次／天 | 日常對話、圖片辨識（**預設推薦**） |
| 🧠 Gemini 2.5 Pro | 100 次／天 | 複雜問題、深度分析 |
| 🪶 Gemini 2.5 Flash Lite | 1,000 次／天 | 簡單翻譯、高頻對話 |

---

## 🛠️ 技術棧 (Tech Stack)

所有程式碼整合在單一 `tokyo_trip.html` 檔案中，零安裝、零後端。

| 類別 | 技術 |
|------|------|
| Core | HTML5, Vanilla JavaScript |
| Styling | [Tailwind CSS](https://tailwindcss.com/) 3.4.1 (CDN) |
| Reactivity | [Alpine.js](https://alpinejs.dev/) 3.13.3 (CDN) |
| Slider | [Swiper.js](https://swiperjs.com/) v11 (autoHeight 模式) |
| Icons | [Phosphor Icons](https://phosphoricons.com/) |
| Font | Zen Maru Gothic (Google Fonts) |
| Markdown | marked.js |
| AI | Google Gemini API（對話 + Vision 圖片辨識） |
| 天氣 | Open-Meteo API |
| 航班 | AviationStack API |
| 翻譯語音 | 瀏覽器原生 SpeechRecognition + SpeechSynthesis |
| 資料儲存 | Browser LocalStorage（純本地，不上傳） |

---

## ⚠️ 注意事項

1. **資料隱私**：所有資料（勾選狀態、記帳紀錄、API Key）皆儲存於你的手機瀏覽器中，**不會**上傳到任何伺服器。
2. **同步問題**：因為無後端，旅伴的手機資料**不會自動同步**。建議一人負責記帳，或利用「分享」功能互傳文字備份。
3. **iOS Safari 限制**：請務必透過「加入主畫面」的方式使用，若僅在一般網頁模式下瀏覽，Safari 可能會定期清除 LocalStorage 導致紀錄消失。
4. **航班追蹤**：AviationStack 免費方案每月 100 次查詢，旅途期間查詢 2 個航班綽綽有餘。

---

### 🌸 祝旅途愉快！Have a nice trip to Tokyo!
