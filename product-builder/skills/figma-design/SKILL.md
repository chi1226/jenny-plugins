---
name: figma-design
description: 生成 Figma 設計稿。把畫面描述或 design-spec 用 claude.ai Figma 工具產出可編輯的 Figma 設計。當使用者說「生 Figma」「做成設計稿」「畫到 Figma」「設計這個畫面」時使用。畫面資訊未填先問，不腦補任何產品。
---

# 生成 Figma 設計稿

## 輸入（使用者會填，空白先問，或引用 [[project-brief]] / [[design-spec]] / [[ui-stack]]）
- 產品 / 畫面：［____］
- 主要內容與階層：［____］
- 視覺定位 / 既有設計系統（可選）：［____］

## 流程
1. **釐清**：缺的先問，不腦補。確認要幾個畫面、有無既有 design system 要沿用。
2. **走 Figma skill**：使用 claude.ai Figma 工具。呼叫 use_figma 前**務必先跑對應的 Figma skill**（figma-generate-design 等），照它的規範走。
3. **生成**：把畫面產進 Figma，結構用 auto-layout、可編輯，不是一張平圖。
4. **回報**：給 使用者 檔案連結/截圖確認，不對就改。

## 原則
- 有既有設計系統就沿用其 token/元件，不另造。
- 設計師工作流優先：圖層命名清楚、可交接。
- 要變真前端用 [[ui-generate]]；要建元件庫用 [[design-system]]。
