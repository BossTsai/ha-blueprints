# Netflix – 客廳情境自動化

本專案為 **BossWei 實際使用並驗證可正常運作** 的 Home Assistant 自動化情境，
用於一鍵啟動客廳 Netflix（必要時自動開機並切換來源）。

---

## 🎯 功能說明

當 `input_boolean.netflix_livingroom` 由 off → on 時：

1. 若客廳電視為關機或狀態不可用，先開啟電視電源
2. 等待電視狀態恢復可用
3. 若目前來源不是 Netflix，切換來源至 Netflix
4. 動作完成後，自動將 input_boolean 關閉，避免重複觸發

---

## 🧩 使用到的實體（依作者環境）

- TV：`media_player.lg_webos_tv_55tg`
- TV 電源：`switch.ac_d73126_2`
- 觸發開關：`input_boolean.netflix_livingroom`

---

## 📂 檔案

- `automation.yaml`：Home Assistant Automation（可直接使用）

---

## 📝 備註

- 此為「實戰範例」，entity_id 為固定值
- 主要用途：技術紀錄 / 邏輯參考 / 未來 Blueprint 化的基礎
