# 🐾 芝麻歷險記 (Sesame's Adventure)

**《芝麻歷險記》（Sesame's Adventure）** 是一款運行於瀏覽器的療癒系 3D 浮島探索與慢活養成網頁遊戲，基於 [Three.js](https://threejs.org/)（WebGL r160）與原生 [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) 打造。全專案採用零依賴打包的單一檔案架構（`index.html`），支援電腦與手機雙端自適應排版、中英雙語自動識別，以及瀏覽器自動存檔。

* **線上遊玩網址**：[https://sesameworld.pages.dev](https://www.google.com/search?q=https://sesameworld.pages.dev)
* **GitHub 儲存庫**：`sesame-game`

## ✨ 遊戲特色 (Core Features)

* **霍比特草皮圓門花屋與 1:1 實體藤籃儲物櫃**：主角藍貓「芝麻」誕生於西側向陽草坡的霍比特風格花屋前，屋內設有圓拱灰泥壁龕與 24 個手工藤編竹籃；玩家存入的任何蘑菇、野菜、河魚、特產與料理，都會在室內藤籃中 1:1 即時生成對應數量與造型的 3D 實體模型。
* **可穿戴與隨地暫放的 3D 小書包**：門口配有專屬立體貓咪小書包，背起後隨身行囊容量由 4 格擴充至 20 格，並可隨時按 `B` 鍵（或手機版快捷鍵）在草地上放下或重新背起。
* **無縫室內外過肩跟隨視角**：可直接推門走入「🏠 貓咪收納花屋」、「🍵 暖陽玻璃茶屋（水車藤蔓溫室）」與「📚 星光樹根書屋」，鏡頭會自動平滑鑽入挑高室內空間並切換廣角視野，呈現木樑、壁爐、彩繪玻璃花窗與吊燈細節。
* **四季感動態自然景觀與五大時段光影**：整座浮島（半徑 `R = 64`）覆蓋隨風擺動的立體長草海、觸碰會飄散傘狀種子的蒲公英、雙層焦散（Caustics）清澈溪流與瀑布，並提供「🌅 清晨、🌤️ 白晝、☀️ 正午、🌇 黃昏、🌙 星夜」五大純境時段切換與流星許願互動。
* **豐富的採集、溪流垂釣與 9 道 3D 料理食譜**：收錄 5 款森林野菇、3 款鮮嫩野菜、香草與野花，溪流中有 5 種 3D 小魚即時擺尾游動並主動游向浮標咬鉤；收集食材後可至「🍳 森林料理亭」組合烹調 9 道精緻料理，出爐後會直接在料理亭餐桌上以 3D 擺盤展示。
* **5 位動物夥伴心願委託與私房特產交換**：與小藍鳥啾啾（Pip）、長耳兔團團（Clover）、紅松鼠果果（Hazel）、刺蝟主廚栗子（Chestnut）及小青蛙呱呱（Puddle）聊天送禮，接取左側「🐾 夥伴心願單」任務，或拿日常收穫交換 6 款夥伴專屬私房好物。
* **程序化合成療癒配樂與自然環境音**：完全不依賴外部音訊檔案，透過 [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) 即時合成毛氈鋼琴、八音盒拇指琴（Kalimba）、木吉他豎琴分解和弦、微風風鈴與林間鳥鳴／夜蟲聲。
* **中英雙語自動切換與無感自動存檔**：根據玩家瀏覽器語系（`navigator.languages`）自動呈現繁體中文或英文介面（亦可點擊底部選單 `🌐 EN / 中文` 一鍵切換），並透過瀏覽器 `localStorage` 即時自動保存所有物品、食譜、好感度與角色座標。

## 🎮 操作指南 (Controls)

| 操作項目 | 電腦網頁版 (Desktop) | 手機觸控版 (Mobile) |
| :--- | :--- | :--- |
| **角色移動** | `W` `A` `S` `D` 或 `↑` `↓` `←` `→`（按住 `Shift` 小跑） | 左下角虛擬搖桿拖曳 |
| **旋轉視角 / 縮放** | 滑鼠左鍵拖曳旋轉、滾輪縮放（或按住 `Ctrl` + 方向鍵原地轉向） | 畫面右側單指滑動旋轉、雙指捏合縮放 |
| **場景互動 / 採集 / 釣魚** | 靠近目標按 `E` 鍵（咬鉤時按 `Space` 或 `E` 拉竿） | 靠近目標點擊右下角橘色「🐾 互動」膠囊鈕 |
| **背起 / 放下小書包** | 按 `B` 鍵（或點擊底部「🎒 行囊」選單） | 點擊右下角「🎒 書包」快捷鍵 |
| **跳躍 / 坐下深呼吸** | 按 `Space` 跳躍、按 `X` 在長草叢中坐下休息 | 點擊右下角「跳」按鈕、底部「🌿 療癒」選單坐下 |
| **背包 / 食譜 / 設定** | `I` 開啟背包、`C` 開啟食譜、`T` 或 `Esc` 開啟設定 | 點擊畫面底部四分類折疊式膠囊收納塢 |
| **自然微互動** | 點擊草地激起微風波浪、點擊夜空召喚許願流星 | 輕觸草地擴散微風波浪、輕觸天空召喚流星 |

## 🗺️ 浮島地標與特產一覽 (Island Landmarks & Specialties)

| 地標 / 夥伴 | 位置區域 | 核心互動與專屬特產 |
| :--- | :--- | :--- |
| **🏠 貓咪收納花屋 (Cat Burrow)** | 西側向陽草坡 | 24 格 1:1 實體 3D 藤籃儲物櫃、門口領取 20 格小書包 |
| **🍳 森林料理亭 (Kitchen Pavilion)** | 中央偏東廣場 | 大灶台 2～3 食材自由組合烹飪、餐桌 3D 料理展示與品嚐 |
| **🍵 暖陽玻璃茶屋 (Glass Tea House)** | 西南側石路旁 | 12 葉旋轉大水車、繁花藤蔓溫室室內空間、長耳兔團團「🍵 晨露花房茶葉」 |
| **📚 星光樹根書屋 (Starlight Library)** | 北側古樹林緣 | 吉卜力風三體塊木瓦書屋、彩繪玻璃花窗、紅松鼠果果「🌰 蜜香甜栗／🌲 琥珀松果仁」 |
| **🎡 暮色大風車 (Sunset Windmill)** | 東北高地山丘 | 巨型四葉帆布風車觀景台、遠眺環島雲海與迷你浮島群 |
| **🌸 櫻花許願亭 (Blossom Pavilion)** | 西南櫻花台地 | 六角飛簷許願清泉池、花瓣隨風飄舞與流星許願加成 |
| **⛩️ 螢光古樹遺跡 (Glow-Shroom Ruins)** | 西北秘境菇林 | 古老石拱門與發光符文方尖碑、盛產夜光「✨ 發光菇」與「🔮 紫晶星傘菇」 |
| **🌉 瀑布木棧道 (Waterfall Pier)** | 東南河口深潭 | 溪流垂釣熱點、小青蛙呱呱「🐚 溪谷珍珠貝」與小藍鳥啾啾「🍓 雲島星果／🍯 暖陽花蜜」 |

## ⚡ 技術架構與手機端溫控省電設計 (Architecture & Thermal Optimization)

1. **零建置單一檔案架構（Zero-Build Single HTML）**：所有 HTML 結構、響應式 CSS 樣式、SVG 手繪圖示、GLSL 頂點／片段著色器（長草風浪與河水雙層焦散）及遊戲邏輯均封裝於單一 `index.html` 中，並透過標準 ES Module Import Map 由 [jsDelivr CDN](https://www.jsdelivr.com/) 載入 Three.js r160。
2. **手機端智慧溫控鎖幀（Adaptive Thermal Frame Pacing）**：針對高更新率手機螢幕（90Hz / 120Hz），在移動與互動時自動鎖定於流暢的 `45 FPS`，當玩家靜止欣賞風景或開啟介面面板超過 3.5 秒時自動降頻至 `28 FPS`，大幅降低行動裝置 GPU 發熱與耗電。
3. **行動端渲染管線最佳化**：在行動裝置上自動關閉高耗能硬體 MSAA 抗鋸齒、動態調整 Retina 像素倍率上限、每 2 幀交錯更新陰影貼圖與風帶幾何，並在切換背景分頁或鎖屏時自動暫停渲染與掛起 `AudioContext`。

## 🚀 部署方式與安全設定 (Deployment & Security)

本專案可直接部署於 [Cloudflare Pages](https://pages.cloudflare.com/) 或 GitHub Pages，無需任何編譯指令：

* **建置設定（Build Settings）**：
  * **Framework preset**：`None`
  * **Build command**：留空（不需填寫）
  * **Build output directory**：`/`
* **HTTP 安全標頭（`_headers`）**：建議於儲存庫根目錄與 `index.html` 同級位置放置 [Cloudflare Pages 自訂標頭檔 `_headers`](https://developers.cloudflare.com/pages/configuration/headers/)，以啟用防盜嵌（`X-Frame-Options: DENY`）與內容安全政策（CSP）：

```text
/*
  X-Frame-Options: DENY
  X-Content-Type-Options: nosniff
  Referrer-Policy: strict-origin-when-cross-origin
  Permissions-Policy: camera=(), microphone=(), geolocation=(), payment=(), usb=()
  Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
  Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net; style-src 'self' 'unsafe-inline'; img-src 'self' data: blob:; media-src 'self' data: blob:; connect-src 'self' https://cdn.jsdelivr.net; worker-src 'self' blob:; frame-ancestors 'none'; base-uri 'self'; form-action 'self';
```
