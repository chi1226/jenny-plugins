# design-flow

雙鑽石設計流程 plugin —— 把一套完整的產品設計方法論裝進 Claude。

*A double-diamond design process toolkit for Claude: 28 skills covering user research, problem definition, ideation, and delivery. Skills are written in Traditional Chinese.*

由 [Jenny Liu](https://jenny-liu.framer.website/)（UIUX / Product Designer）打造，涵蓋從使用者研究到交付驗證的 28 個 skill，以雙鑽石（Double Diamond）為總框架，每個階段的產出可以一棒接一棒往下傳。

## 安裝

```bash
claude plugin marketplace add chi1226/jenny-plugins
claude plugin install design-flow@jenny-plugins
```

## 使用方式

不知道從哪開始？直接下：

```
/design-flow:next 我有一堆訪談逐字稿，不知道下一步
```

它會判斷你在流程的哪一格，告訴你下一步該用哪個 skill。

## Skill 地圖

### 流程導覽（Meta）
| Skill | 用途 |
|---|---|
| design-router | 判斷你在雙鑽石哪一格、指路下一步 |
| project-brief | 一個專案填一次脈絡，其他 skill 直接引用 |
| double-diamond | 把專案拆成雙鑽石四階段的可執行活動 |

### 探索（發散 1）— 使用者研究
interview-guide（訪談大綱）→ interview-review（檢查引導性）→ affinity-synthesis（洞察歸納）；persona-build、context-scenario 補足使用者理解。

### 定義（收斂 1）— 問題定義
jtbd-write → jtbd-to-hmw / job-story → job-story-review → problem-statement → ps-critique → hmw-generate → hmw-review。每一步都有對應的生成與品質檢查。

### 發展（發散 2）— 設計發想
ideation（Crazy 8s / SCAMPER）、competitor-scan（競品探索）、ia-userflow（資訊架構）、ui-stack（五狀態清單）、mental-model-gap（心智模型缺口）。

### 交付（收斂 2）— 驗證與交付
design-critique（結構化評論）、usability-test、ux-flow-friction（摩擦點）、a11y-check（WCAG 2.1 AA）、error-message（UX 文案）、taste-train（視覺一致性）、design-spec（工程交付規格）。

## 設計原則

- **不腦補**：所有 skill 的輸入欄位留空，資訊不足會先問，不假造任何產品脈絡。
- **一棒接一棒**：上一個 skill 的產出就是下一個的輸入，skill 之間用 [[wiki 連結]] 互相引用。
- **生成 + 檢查成對**：關鍵產出（訪談題目、Job Story、PS、HMW）都有對應的 review/critique skill 把關品質。

## 連接器（選用）

plugin 附 `.mcp.json` 範例，接上 Figma（讀設計稿）與 Notion（存研究資料）。第一次使用會跳出授權，不需要可以直接刪掉這個檔案。

## 版本

- v0.2.0（2026-07-15）：skill 通用化（移除個人稱呼）、雙語 description、.mcp.json 連接器範例
- v0.1.0（2026-07-15）：初版，28 個 skill + /design-flow:next
