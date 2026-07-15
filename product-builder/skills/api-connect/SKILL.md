---
name: api-connect
description: 快速把外部 API 或 AI（Claude、OpenAI、天氣、地圖等）串進正在做的 prototype。當使用者說「我要加 XX 功能」「串一個 API」「讓它會回饋 / 抓資料 / 呼叫 AI」時使用。負責挑 API、安全放 key、接進去、測通，並用白話解釋。
---

# api-connect — 幫 prototype 串外部 API / AI

## 什麼時候用
使用者 在做 prototype，說出類似的話就啟動：
- 「記錄完給我一句 AI 回饋」
- 「我要抓天氣 / 地圖 / 匯率 / 新聞」
- 「串一個 API」「接 OpenAI / Claude」
- 「讓它會自動 XX」

## 核心原則
- 使用者非工程師。每一步先用白話講「這步在幹嘛、為什麼」，再動手。
- **API key 絕對不寫死在 code 裡**。一律進 `.env`，且 `.env` 要在 `.gitignore`。
- 先做最小可跑版本，通了再加花樣。不要一次串三個 API。
- 卡住先講清楚卡在哪、要 使用者 做什麼（例：去哪申請 key），不腦補假資料。

## 流程

### 1. 搞清楚要什麼
問一句就好：「你想加的功能，具體是輸入什麼 → 輸出什麼？」
例：情緒紀錄 App →「使用者寫完當天心情 → AI 回一句同理的話」。

### 2. 挑 API（幫使用者決定，別丟選擇題）
| 想做的事 | 推薦 | 為什麼 |
|---------|------|--------|
| AI 回饋 / 生成文字 / 分析情緒 | Claude API（Anthropic）| 面試主題相關、品質好 |
| 也可 | OpenAI | 生態成熟 |
| 天氣 | Open-Meteo | 免費、免 key |
| 地圖 / 地點 | Google Maps / Mapbox | 通用 |
| 匯率 / 股價 | 依題目查免費源 | — |

不確定就上網查目前免費、好上手的，直接提一個，不護主。

### 3. 拿 key（如果需要）
- 需要 key 的 API：白話講去哪申請、貼給我，我放進 `.env`。
- 免 key 的（如 Open-Meteo）：直接跳過。

### 4. 安全接進去
- 建 `.env`，寫 `XXX_API_KEY=...`
- 確認 `.gitignore` 有 `.env`（沒有就加）
- 前端專案：key 不能放前端（會被看到）。要走一個小後端 / serverless function 代呼叫。這點務必跟 使用者 講清楚，別把 key 曝在瀏覽器。
- 寫最小串接程式，接上 prototype。

### 5. 測通
- 實際跑一次，給 使用者 看真的有回應。
- 失敗就把錯誤訊息原文貼出來、講白話原因、修。

### 6. 收尾講解
用 3 句話講：串了什麼、key 放哪、之後想改哪裡怎麼改。

## Claude API 起手式（最常用）
若專案有用 Anthropic SDK，套用 `claude-api` skill 的做法：
- 模型預設 `claude-opus-4-8`（或依需求 sonnet/haiku）
- 加 prompt caching
- key 走後端，不進前端

## 安全紅線
- key 進 `.env` + `.gitignore`，永不 commit、永不放前端。
- 不幫任何規避、爆量、攻擊性用途串 API。
