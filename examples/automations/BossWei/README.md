# Examples – Automations (BossWei)

本資料夾收錄 **BossWei 實際使用、已驗證可正常運作** 的
Home Assistant 自動化範例，主要作為：

- 個人技術紀錄
- 邏輯設計參考
- 未來重構或 Blueprint 化的基礎

⚠️ 注意：
此資料夾內的自動化 **多半使用固定 entity_id**，  
不保證可直接套用到其他人的 Home Assistant 環境。

---

## 🎬 Netflix – 客廳情境自動化

**檔案：**
netflix_livingroom.yaml

### 功能說明
當 `input_boolean.netflix_livingroom` 被開啟時，會依序執行：

1. 若客廳電視為關機或狀態不可用，先開啟電視電源
2. 等待電視狀態恢復可用（避免剛開機尚未初始化）
3. 若目前來源不是 Netflix，則切換至 Netflix
4. 動作完成後，自動將 `input_boolean` 關閉，避免重複觸發

---

### 使用到的實體（依作者環境）
- TV：
  - `media_player.lg_webos_tv_55tg`
- TV 電源：
  - `switch.ac_d73126_2`
- 觸發開關：
  - `input_boolean.netflix_livingroom`

---

### 適合使用情境
- 客廳影音一鍵啟動
- 實體按鈕 / Dashboard 按鈕觸發
- 當作日後 Blueprint 化的範例邏輯

---

### 未來規劃
- 將此自動化重構為 Blueprint（支援選擇 TV / Source）
- 延伸支援 YouTube / HDMI / Game Console
