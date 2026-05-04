---
layout: default
title: MULTIPUN 阅读笔记
---

# MULTIPUN 阅读笔记

## 论文信息

- 标题：“I See What You Did There”: Can Large Vision-Language Models Understand Multimodal Puns?
- 方向：Multimodal Understanding / VLM Evaluation / Trustworthy AI

---

## 一句话总结

MULTIPUN 构建了一个用于评估视觉语言模型是否真正理解多模态双关语的 benchmark。

---

## 核心问题

多模态双关语需要模型同时理解图像、文字和隐含语义。现有 VLM 可能只是表面匹配幽默模式，而不是真正理解双关结构。

---

## 核心框架

双关词对生成  
→ 正样本构造  
→ 负样本构造  
→ 设计检测、定位和解释任务  
→ 评估 VLM 的多模态幽默理解能力

---

## 我的初步理解

这篇文章不是单纯提出一个模型，而是构建一个更严格的评测基准，用来考察视觉语言模型是否具备细粒度的跨模态语义理解能力。

---

## 当前进度

待进一步精读。
