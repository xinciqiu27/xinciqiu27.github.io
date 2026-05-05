---
layout: default
title: Web API Recommendation 学习笔记
---

# Web API Recommendation 学习笔记

本栏目用于整理我在 Web API / Cloud API 推荐方向及其相关方法文献中的阅读笔记。主要记录论文的大致思路以及我的小思考。

---

## 论文阅读笔记

### Web API / Cloud API 推荐主线

- [Function-guided ELDA 阅读笔记](function-guided-elda.html)
- [BERT-based Web API Recommendation 阅读笔记](cloudcom-bert-webapi.html)
- [CECL 阅读笔记](cecl.html)
- [LSFL 阅读笔记](lsfl.html)
- [LMSR 阅读笔记](lmsr.html)
- [Spherical Hashing 隐私保护 API 推荐阅读笔记](spherical-hashing-api.html)
- [高阶互补云 API 推荐阅读笔记](personalized-tensor-factorization.html)
- [FCRL 阅读笔记](fcrl.html)
- [LACL 阅读笔记](lacl.html)
- [MGCL 阅读笔记](mgcl.html)
- [MDCL 阅读笔记](mdcl.html)

### 相关推荐方法与背景文献

- [GLSCL 阅读笔记](glscl.html)
- [SRA-CL 阅读笔记](sra-cl.html)
- [SLGGCL 阅读笔记](slggcl.html)
- [QRPM 阅读笔记](qrpm.html)

---

## 当前理解

这一方向的演化脉络已经比较清晰：早期方法主要依赖关键词、主题模型和协同过滤；中期开始强化图结构、对比学习与互补关系建模；最新工作则越来越强调 LLM 对需求语义补全、推荐上下文预测、多视角关系融合和冷启动鲁棒性的作用。

我目前的一个直观判断是：真正拉开效果差距的，不只是“用了更强的模型”，而是能否同时处理三件事：
- 新需求描述本身的语义稀疏性
- Mashup / API 之间的多粒度协同关系
- 冷启动场景下缺少历史调用数据的问题
