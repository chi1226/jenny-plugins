# product-builder

從想法到能點的產品 —— vibe coding 生產包。

*From idea to clickable product: PRD, prioritization, design system, real front-end screens, motion, and API integration. Skills are written in Traditional Chinese.*

由 [Jenny Liu](https://jenny-liu.framer.website/) 打造。10 個 skill 串成一條生產線：定義（PRD、優先級）→ 設計（設計系統、規格、狀態清單）→ 產出（真前端、Figma 稿）→ 打磨（動效、串 API）。

## 安裝

```bash
claude plugin marketplace add chi1226/jenny-plugins
claude plugin install product-builder@jenny-plugins
```

## 使用方式

```
/product-builder:build 我想做一個記帳 App 的週報功能
```

會依進度引導走完整條生產線，也可以直接叫個別 skill。

## Skill 一覽

| 階段 | Skill | 用途 |
|---|---|---|
| 定義 | prd-write | 產品層級 PRD：問題、Goals/Non-Goals、成功指標、驗收條件 |
| 定義 | roadmap-prioritize | RICE + MoSCoW 排優先級，產出 Now/Next/Later |
| 設計 | design-system | 生成設計 tokens（色彩、字級、間距）與基礎元件規格 |
| 設計 | design-spec | 畫面層級規格：結構、狀態、行為、邊界情況 + vibe coding prompt |
| 設計 | ui-stack | 一頁的五種狀態清單（Blank/Loading/Partial/Error/Ideal） |
| 產出 | ui-generate | 描述 → 能在瀏覽器點的 HTML/React 畫面 |
| 產出 | figma-design | 描述 → 可編輯的 Figma 設計稿（需 Figma MCP） |
| 打磨 | motion-design | 把「Q 彈／優雅／俐落」翻成 easing 和時長參數並實作 |
| 打磨 | api-connect | 把外部 API 或 AI 串進 prototype |
| 風格 | design-material-3 | Material 3 風格系統參考（tokens、元件樣式） |

## 設計原則

- **不腦補**：所有輸入欄位留空，資訊不足先問。
- **PRD 先於畫面**：先回答為什麼做、做到哪，再談長怎樣。
- **產出是真的**：ui-generate 生出來的是能點的網頁，不是示意圖。
