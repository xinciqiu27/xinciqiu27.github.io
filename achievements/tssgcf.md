---
layout: default
title: TSSGCF
---

# TSSGCF: Textual Similarity-Supervised Graph Collaborative Filtering for Web API Recommendation

## 基本信息

- 论文题目：TSSGCF: Textual Similarity-Supervised Graph Collaborative Filtering for Web API Recommendation
- 会议：The 23rd International Conference on Service-Oriented Computing, ICSOC 2025
- 类别：CCF B 类会议
- 作者身份：第二作者
- 研究方向：Web API Recommendation, Graph Collaborative Filtering, Textual Similarity

---

## 研究背景

Web API 推荐任务旨在根据 Mashup 的功能需求或历史交互信息，为开发者推荐合适的 Web API。

传统推荐方法通常依赖 Mashup 与 Web API 之间的交互信号，但在真实场景中，Mashup 和 Web API 的文本描述中包含了大量功能语义信息。如果能够充分利用这些文本语义信息，就可以更好地建模 Mashup 与 API 之间的匹配关系。

---

## 核心思想

该工作尝试将文本语义相似性引入图协同过滤框架中，使模型不仅学习交互关系，还能受到文本相似性的监督。

整体思路可以概括为：

Mashup / Web API 文本描述  
→ Sentence-BERT 语义编码  
→ 文本相似性建模  
→ 图协同过滤表示学习  
→ Web API 推荐结果

---

## 我的主要贡献

在该工作中，我主要参与了：

- 论文方法框架设计与讨论
- 数据预处理
- 使用 Sentence-BERT 对 Mashup 和 Web API 的文本描述进行编码
- 参与基线模型选择
- 负责其中 5 个基线模型的实现
- 参与主实验超参数调优
- 参与相关工作、实验设置、超参数影响等部分的撰写

---

## 我的收获

通过这个工作，我开始系统理解 Web API 推荐任务的基本流程，包括数据构建、模型设计、基线对比、评价指标和论文写作。同时，我也进一步认识到文本语义信息在服务推荐场景中的重要性。
