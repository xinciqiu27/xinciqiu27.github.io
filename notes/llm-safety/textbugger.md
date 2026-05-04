---
layout: default
title: TEXTBUGGER 阅读笔记
---

# TEXTBUGGER 阅读笔记

## 论文信息

- 标题：TEXTBUGGER: Generating Adversarial Text Against Real-world Applications
- 方向：Text Adversarial Attack / Model Security

---

## 一句话总结

TEXTBUGGER 研究如何通过对文本进行细微扰动，生成能够欺骗真实文本分类系统的对抗样本。

---

## 核心问题

文本分类模型在面对轻微扰动时可能出现错误预测，例如拼写错误、字符替换、词语替换等都可能影响模型判断。

---

## 核心框架

原始文本  
→ 找到重要词  
→ 生成字符级或词级扰动  
→ 替换关键词  
→ 生成对抗文本  
→ 欺骗目标分类模型

---

## 我的初步理解

TEXTBUGGER 的本质是一个文本对抗攻击框架。它的核心思想是用尽可能小的文本改动，造成模型预测结果的变化，同时尽量保持人类读者对原文含义的理解。

---

## 当前进度

待进一步精读。
