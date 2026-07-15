---
name: roadmap-prioritize
description: 功能優先級與 roadmap。把一堆想做的功能用 RICE / MoSCoW 排出優先序，整理成 Now / Next / Later roadmap，並說明每個取捨。當使用者說「排優先級」「哪個先做」「roadmap」「功能太多不知道先做哪個」時使用。功能清單未填先問，不腦補。
---

# 功能優先級與 Roadmap

## 輸入（使用者會填，空白先問）
- 功能 / 想法清單：［____］
- 這階段的目標：［例：MVP 上線 / 求職作品完成 / 驗證某假設，有的話引用 [[mvp-plan]]］
- 資源限制：［一個人 / 每週幾小時 / 截止日］

## Task
1. **RICE 打分**，每個功能：
   - **R**each：多少使用者會碰到（或對作品集/目標的觸及）
   - **I**mpact：碰到的人受多大影響（3 巨大 / 2 高 / 1 中 / 0.5 低）
   - **C**onfidence：對上面兩項的把握（100% / 80% / 50%）
   - **E**ffort：要花多少工（人週或相對大小）
   - 分數 = R × I × C ÷ E
2. **MoSCoW 交叉檢查**：Must / Should / Could / Won't（this time）。RICE 分數高但其實是 Could 的，通常代表低估了 Effort 或高估了 Reach，挑出來討論。
3. **整理成 Now / Next / Later**：
   - Now：現在就動工（1–3 項，不能多）
   - Next：Now 做完接著做
   - Later：值得做但不是現在，寫一句「什麼條件成立才升級」
   - Won't：明確說不做，跟 [[prd-write]] 的 Non-Goals 呼應

## 原則
- Now 超過 3 項就不叫優先級，逼自己砍。
- 每個取捨寫一句理由，之後回頭看才知道當時為什麼這樣排。
- 分數是輔助不是聖旨——排完問一句「直覺同意嗎？」，不同意就找出哪個估錯。

## Output
RICE 表 + Now/Next/Later roadmap + 每項一句理由 + Won't 清單。
