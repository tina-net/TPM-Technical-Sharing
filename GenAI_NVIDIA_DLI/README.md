# 🤖 NVIDIA DLI: Generative AI Explained

This note covers the fundamentals of LLMs and generative AI, including Transformer architecture, inference workflow, and prompt engineering. Diagrams included.

本筆記以中英文整理 LLM 與 Transformer 架構原理，搭配推論流程圖、Prompt 設計示意，強化 TPM 對生成式 AI 架構的理解與溝通能力。

---

## 🔍 Key Topics
- 🔸 Transformer 架構與 Self-Attention
- 🔸 LLM 推論流程（ChatGPT 類模型）
- 🔸 Prompt Engineering 概念與應用情境

- # 🤖 NVIDIA DLI: Generative AI Explained | 中英筆記整理

This is a bilingual summary of the NVIDIA Deep Learning Institute (DLI) course "Generative AI Explained." It introduces the architecture of generative models, especially transformers and large language models (LLMs), with visual workflows and core concepts suitable for TPMs.

---

## 📘 Course Overview 課程概覽

- English: This course provides a high-level explanation of how generative AI models like ChatGPT work, covering transformer architecture, tokenization, and inference logic.
- 中文：本課程以高階角度解釋生成式 AI 的運作方式，重點介紹 Transformer 架構、Token 化機制與推論邏輯。

---

## 🔍 Key Concepts 核心概念

### 1. What is Generative AI? | 什麼是生成式 AI？
- Models that create content (text, image, audio) instead of just classifying or predicting.
- 生成式 AI 模型可產出文本、圖片、音訊等，不僅限於分類或預測。

### 2. Transformer Architecture | Transformer 架構解析
- Key elements: Self-Attention, Positional Encoding, Multi-Head Attention
- 核心組件：自注意力機制、位置編碼、多頭注意力
- TPM Insight：有助於理解 LLM 的運作與部署資源需求。

### 3. Large Language Models (LLMs) | 大型語言模型
- Trained on massive datasets using encoder-decoder or decoder-only structures
- 基於巨量語料訓練，可採用 Encoder-Decoder 或 Decoder-only 結構
- 示例：GPT、LLaMA、Gemini

### 4. Prompt Engineering | 提示設計
- Crafting inputs to steer model output effectively
- 精準設計 Prompt 可引導模型產出更符合需求的結果
- TPM Insight：影響產品推論階段的 UX 與可控性

### 5. Inference Pipeline | 推論流程簡介
- Tokenize input → Run through Transformer layers → Generate tokens → Detokenize output
- 輸入文字 Token 化 → 經 Transformer 層運算 → 產生下個 Token → 解碼還原為文字

---

## ✨ TPM Perspective | 專案經理的視角

- Understand model size and compute demand when scoping infrastructure  
  控制 LLM 部署的 GPU 資源預算  
- Collaborate with R&D and infra teams to integrate inference endpoints  
  與軟體、基礎設施專案合作  
- Plan for prompt quality testing & edge case validation  
  前端使用者 prompt 測試與問題距離診斷

---

## 📌 Summary

This course equips TPMs with foundational understanding of how generative models function internally, helping them better plan infrastructure, explain capabilities to stakeholders, and improve coordination in deployment projects.

本課程可幫助 TPM 建立生成式模型的基本理解，進而在規劃資源、跨部門溝通與推論部署中發揮更大影響力。

---

