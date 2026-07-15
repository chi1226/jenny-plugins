# Jenny Plugins

設計師做的 Claude plugin 市集 —— 把一套完整的產品設計方法論裝進 Claude。

由 [Jenny Liu](https://jenny-liu.framer.website/)（UIUX / Product Designer）打造與維護。每個 plugin 是一組面向真實設計工作流的 skill，全部繁體中文、全部遵守「資訊不足先問、絕不腦補」原則。

*Claude plugins by a product designer: a complete design methodology (double diamond), a vibe-coding pipeline, and a job-hunting toolkit. Skills are written in Traditional Chinese.*

## Plugin 一覽

| Plugin | 內容 | Skill 數 |
|---|---|---|
| **[design-flow](./design-flow)** | 雙鑽石設計流程：研究 → 定義 → 發想 → 交付，含流程導覽員 design-router | 28 |
| **[product-builder](./product-builder)** | 從想法到能點的產品：PRD、設計系統、生成前端、動效、串 API | 10 |
| **[job-hunt-designer](./job-hunt-designer)** | 設計師求職：case study 敘事、專案簡報、模擬面試 | 3 |

## 安裝

```bash
# 加入市集
claude plugin marketplace add chi1226/jenny-plugins

# 安裝 plugin
claude plugin install design-flow@jenny-plugins
```

裝好後直接下 `/design-flow:next 我卡在不知道怎麼開始` 試試。

## 這套 skill 的特色

- **有流程觀**：不是零散的 prompt 集合，上一個 skill 的產出就是下一個的輸入
- **生成與檢查成對**：訪談題目、Job Story、Problem Statement、HMW 都有對應的 review skill 把關
- **不腦補**：所有輸入欄位留空，缺資訊會先問，不假造任何產品脈絡
