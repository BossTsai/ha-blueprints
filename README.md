# BossWei – Home Assistant Automation Blueprints

本目錄收錄由 **BossWei（智新科技）** 設計與維護的  
**Home Assistant Automation 藍圖（Blueprints）**。

所有藍圖皆以「實際可用、穩定、安全、可重複套用」為設計原則，  
適合個人家庭、進階玩家與專業部署環境使用。

---

## 📌 共通使用方式（藍圖匯入）

1. 開啟 Home Assistant  
2. 前往：**設定 → 自動化與場景 → 藍圖**
3. 點選右上角 **「匯入藍圖」**
4. 貼上藍圖提供的 **Raw GitHub 連結**
5. 建立自動化並依照畫面選擇對應設備

---

## 📂 目錄結構說明

本資料夾採用「**一個藍圖 = 一個專案資料夾**」的結構：

ha-blueprints/
└─ blueprints/
   └─ automation/
      └─ BossWei/
         ├─ README.md        
         └─ ac_power_on_set_temp/
            ├─ blueprint.yaml
            └─ README.md

設計原則：
	•	每個資料夾代表一個 獨立、完整的藍圖專案
	•	藍圖主檔固定命名為 blueprint.yaml
	•	專案資料夾名稱即為藍圖功能識別名稱
	•	每個藍圖皆附帶獨立 README，說明用途、邏輯與使用情境

🔧 目前提供的藍圖

1️⃣ 冷氣通電後自動校正目標溫度（僅冷氣模式）

📥 一鍵匯入藍圖連結
https://raw.githubusercontent.com/BossTsai/ha-blueprints/main/blueprints/automation/BossWei/ac_power_on_set_temp/blueprint.yaml

Home Assistant → 設定 → 自動化與場景 → 藍圖 → 匯入藍圖

詳細設定說明、欄位解釋與使用範例，請參考該資料夾內的 README.md。

---

⚠️ 注意事項
	•	本目錄內藍圖皆為 Automation Blueprint
	•	藍圖本身不會直接執行，需建立自動化實例後才會生效
	•	不同整合（冷氣、電視）支援能力依設備而異

⸻

👤 作者

BossWei（智新科技）
GitHub：https://github.com/BossTsai￼

⸻

📜 授權

MIT License
可自由使用、修改與散布，請保留原作者資訊。
詳細設定說明、欄位解釋與使用範例，
請參考該資料夾內的 README.md。
