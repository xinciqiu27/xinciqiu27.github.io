---
layout: default
title: Multi-Modal Complementary Web API Recommendation
---

# Multi-Modal Complementary Web API Recommendation with Attentive Context Modeling

## 基本信息

- 论文题目：Multi-Modal Complementary Web API Recommendation with Attentive Context Modeling
- 会议：2026 29th International Conference on Computer Supported Cooperative Work in Design, CSCWD 2026
- 类别：CCF C 类会议
- 作者身份：第一作者
- 研究方向：Web API Recommendation, Multi-Modal Recommendation, Complementary Recommendation

---

## 研究背景

在真实的软件开发过程中，开发者往往不会只调用一个 Web API，而是会组合多个 API 来完成复杂功能。

因此，推荐系统不仅需要推荐“相似”的 API，也需要推荐能够与已有 API 形成互补关系的 API。

---

## 核心问题

该工作关注的问题是：

给定开发者已经选择的一组 Web API，如何推荐新的、具有互补价值的 Web API？

这不同于传统的单一 API 推荐，因为模型需要理解：

- 已选 API 组合的上下文
- 候选 API 与已有 API 之间的互补关系
- 多模态信息对推荐结果的影响

---

## 核心方法

该工作主要包括：

- 构建互补式 Web API 推荐任务
- 根据 Web API 共现关系设计正负样本
- 建模 Web API 的多模态信息
- 设计候选感知的注意力机制
- 根据已选 API 组合动态调整候选 API 表示

---

## 实验结果

最终模型在 Recall@10 和 MRR 指标上相较最强基线分别提升：

- Recall@10：5.01%
- MRR：2.78%

---

## 我的主要贡献

作为第一作者，我主要负责：

- 互补推荐任务建模
- 正负样本构建
- 基于 Web API 共现关系的样本设计
- 候选感知注意力机制设计
- 实验设计与结果分析
- 论文主要内容撰写

---

## 我的收获

这个工作让我从论文参与者转变为更主动的研究设计者。我开始学习如何提出问题、定义任务、设计模型结构，并围绕实验结果证明方法的有效性。
