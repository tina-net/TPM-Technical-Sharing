# 📦 AI Infrastructure and Operations Fundamentals (Coursera)

This note summarizes key concepts from the Coursera course on AI Infrastructure and Operations, including MLOps workflows, containerization, and model lifecycle management.

本筆記整理自 Coursera 課程，涵蓋 MLOps 架構、Docker/Kubernetes 部署、模型維運管理等重點，並從 TPM 角度補充跨部門實作思維。

---

## 📚 Covered Topics
- 🔹 MLOps vs DevOps
- 🔹 Container + Orchestration (Docker / Kubernetes)
- 🔹 Resource Scaling & Monitoring
- 🔹 Model Deployment Pipelines

# 📦 AI Infrastructure and Operations Fundamentals (Coursera)

This is a bilingual summary note for the course **"AI Infrastructure and Operations Fundamentals"** on Coursera. It focuses on MLOps architecture, container orchestration, model lifecycle, and monitoring practices—all from a TPM’s perspective.

---

## 📘 Course Overview 課程概覽

- English: This course introduces key concepts in managing the infrastructure that supports AI systems. It includes topics like containerization, resource management, monitoring, and the MLOps lifecycle.
- 中文：這堂課程介紹支撐 AI 系統背後的基礎架構管理概念，包括容器化、資源配置、監控，以及 MLOps 模型生命週期。

---

## 🧱 Key Concepts 主要概念

### 1. MLOps Lifecycle | 機器學習營運生命週期
- Model training → validation → deployment → monitoring → retraining
- 模型訓練 → 驗證 → 部署 → 監控 → 再訓練
- TPM Insight：需協調 Data/ML/IT 團隊，掌握切換點與依賴關係。

### 2. Containerization & Orchestration | 容器化與編排
- Docker for packaging models / Kubernetes for orchestrating scalable inference services
- 使用 Docker 封裝模型、Kubernetes 負責大規模自動部署
- TPM Insight：資源可視化與負載調度是專案穩定性的關鍵

### 3. Model Deployment Patterns | 模型部署策略
- A/B testing, Canary deployments, Shadow testing
- A/B 測試、金絲雀發布、影子測試
- TPM Insight：需與 QA 團隊協調測試版本切換與 rollback 流程

### 4. Infrastructure Monitoring | 資源監控
- GPU utilization, latency, throughput, error rate
- GPU 使用率、推論延遲、效能吞吐量、錯誤率監控
- TPM Insight：建立 SLO/SLI/SLA 追蹤儀表板，協助跨 BU 設定期望值

### 5. Scaling & Optimization | 擴展與優化策略
- Autoscaling services via K8s; load balancing; resource throttling
- 透過 K8s 自動擴展、負載平衡、限制資源使用峰值
- TPM Insight：需預估模型熱點與高峰時段部署需求

---

## 🔄 TPM Responsibilities in AI Infra 專案經理的關鍵職能

- Collaborate with ML/DL, DevOps, and SRE teams to ensure smooth model rollout  
  與 ML/DL、DevOps、SRE 團隊協作以確保部署順利  
- Track infrastructure KPIs and deployment health status  
  跟蹤基礎設施 KPI 與部署健康狀態  
- Facilitate post-deployment review & retraining alignment  
  推動部署後的回顧與重新訓練調整

---

## 📌 Summary

This course offers TPMs foundational knowledge to communicate effectively with engineering teams and to lead AI infrastructure projects involving model delivery, scalability, and performance monitoring.

本課程有助於 TPM 打通 AI 架構與工程團隊的語言隔閡，並建立管理模型部署與監控指標的全貌視角。

---

