# 冷氣通電後自動校正目標溫度（僅冷氣模式）

此 Blueprint 用於：冷氣電源由 off → on 後，若目前模式為 `cool` 且目標溫度不是指定值，則自動修正為指定溫度。

**版本：v1.0.1**  
- 修正 Blueprint 在 HA 建立自動化時出現的 template 語法錯誤

---

## ✅ 功能
- 以「電源開關」狀態 off→on 作為觸發
- 只在 `hvac_mode == cool` 時動作
- 若目前設定溫度 ≠ 目標溫度 → 自動設為目標溫度
- 可設定「通電後同步延遲」避免剛開機狀態未同步

---

## 🔧 Inputs（建立自動化時可選）
- 冷氣電源開關（switch）
- 冷氣本體（climate）
- 目標溫度（number）
- 同步延遲秒數（number）

---

## 🔗 一鍵匯入連結（Raw）
https://raw.githubusercontent.com/BossTsai/ha-blueprints/main/blueprints/automation/BossWei/ac_power_on_set_temp/blueprint.yaml

---

## 🧪 使用範例
- 客廳冷氣：目標 27℃
- 主臥冷氣：目標 26℃

（建立自動化時選對應的 switch / climate / 溫度即可）
