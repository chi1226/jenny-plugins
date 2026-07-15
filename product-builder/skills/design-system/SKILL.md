---
name: design-system
description: 生成設計系統。依視覺定位產出設計 tokens（色彩、字級、間距、圓角）與基礎元件（按鈕、輸入框、卡片…）規格，供 Figma 或前端共用。當使用者說「建設計系統」「design token」「元件庫」「統一樣式」時使用。定位未填先問，不腦補任何產品。
---

# 生成設計系統（Design System）

## 輸入（使用者會填，空白先問，或引用 [[project-brief]]）
- 產品 / 品牌定位：［____］
- 已定的視覺方向（色/字/風格，可選）：［____］
- 用途：［Figma / 前端 code / 兩者］

## Task
1. **設計 Tokens**
   - 色彩：主色、輔色、語意色（成功/警告/錯誤）、中性灰階，含明暗。
   - 字級：階層（H1…body…caption）+ 行高。
   - 間距：一致的 spacing scale（如 4/8/12/16…）。
   - 圓角、陰影、邊框。
2. **基礎元件規格**：按鈕（各狀態/尺寸）、輸入框、卡片、標籤等，標出用 token。
3. **輸出格式**：
   - 給前端 → CSS 變數 / Tailwind config。
   - 給 Figma → 變數與元件建議（可接 [[figma-design]]）。

## 原則
- 每個決策連回品牌定位，可引用 [[taste-train]] 驗證一致性。
- token 先於元件、元件先於畫面；[[ui-generate]] / [[figma-design]] 直接吃這套。
