---
layout: default
title: MANBENCH 阅读笔记
---

# When Agents “Misremember” Collectively: Exploring the Mandela Effect in LLM-based Multi-Agent Systems

## 论文笔记

---

## 一、论文概述

| 项目 | 内容 |
|---|---|
| 论文题目 | When Agents “Misremember” Collectively: Exploring the Mandela Effect in LLM-based Multi-Agent Systems |
| 作者 | Naen Xu, Hengyu An, Shuo Shi, Jinghuai Zhang, Chunyi Zhou, Changjiang Li, Tianyu Du, Zhihui Fu, Jun Wang, Shouling Ji |
| 期刊/会议 | ICLR 2026；arXiv:2602.00428v2 |
| 论文链接 | https://arxiv.org/abs/2602.00428 |
| 论文代码 | https://github.com/bluedream02/Mandela-Effect |

---

## 二、论文内容

### 1. 主要思想

本文研究 LLM 多智能体系统中的 **曼德拉效应**。

所谓曼德拉效应，是指一群人共同记错某个可验证事实。在 LLM 多智能体系统中，多个 agent 也可能在社会影响、伪证据和记忆巩固后，形成与事实相矛盾的集体错误记忆。

作者提出 **MANBENCH**，用于系统评估这种现象。该 benchmark 包含 4,838 个问题、20 个任务、4 类知识域和 5 种交互协议。

---

### 2. 所解决的问题

多智能体系统常被认为能够通过讨论、辩论和协作提升推理能力。

但是，如果讨论中出现看似合理的错误信息，多个 agent 可能不是互相纠错，而是互相强化错误，最终形成集体误判。

现有幻觉研究多关注单个模型的一次性错误，而本文关注的是：

社会诱导  
→ 错误信息传播  
→ 记忆固化  
→ 后续回忆错误

这是一种更动态、更接近人类社会认知偏差的问题。

---

### 3. 背景知识补充

#### 3.1 什么是曼德拉效应？

曼德拉效应是指一群人共同记错某个事实。

经典例子是：有人错误地记得南非领导人 Nelson Mandela 在 1980 年代死于狱中，但实际上他于 2013 年去世。

这个现象强调的不是单个人记错，而是“群体共同形成错误记忆”。

---

#### 3.2 什么是 LLM 多智能体系统？

LLM 多智能体系统指多个 LLM agent 扮演不同角色，通过讨论、辩论或协作来完成任务。

例如：

- 一个 agent 提出结论；
- 一个 agent 提供证据；
- 一个 agent 扮演专家；
- 一个 agent 进行质疑；
- 最终形成群体答案。

这种系统看起来更像人类团队，但也可能产生群体偏差。

---

#### 3.3 Mandela effect 与 hallucination 的区别

| 概念 | 含义 |
|---|---|
| Hallucination | 单个模型生成不真实内容 |
| Mandela effect | 多个 agent 在交互和记忆中共同形成错误事实 |

本文关注的重点不是单次答错，而是错误如何在群体互动中被传播、强化和记住。

---

### 4. 论文的主要内容：框架图与模块理解

MANBENCH 的整体流程可以概括为：

构建有真实答案的问题  
→ 选择 plausible distractor  
→ 设计多智能体交互协议  
→ 注入看似合理但错误的证据  
→ 观察 agent 是否从正确事实转向错误答案  
→ 分析影响因素  
→ 提出防御方法

论文中的五种交互协议包括：

| 协议 | 含义 |
|---|---|
| Baseline Reality | 单独测试 agent 是否知道正确答案 |
| Generic Short-term | 普通群体短期影响 |
| Generic Long-term | 普通群体长期记忆影响 |
| Role-based Short-term | 角色化群体短期影响 |
| Role-based Long-term | 角色化群体长期记忆影响 |

---

### 5. 方法核心步骤

#### Step 1：建立现实基线

首先用 Baseline Reality Protocol 测试 agent 原本是否知道正确答案。

如果 agent 本来就不知道答案，那么后面答错就不能算作被群体诱导产生曼德拉效应。

---

#### Step 2：注入伪证据

系统会给 agent 提供看似合理但错误的 specious evidence。

这些证据不是简单说“正确答案是错的”，而是制造有细节、有权威感、有社会共识的错误叙事。

---

#### Step 3：多智能体互动

在 role-based 协议中，不同 agent 会扮演不同角色：

- Error Conclusion Initiator：提出错误结论
- Detail Support Provider：补充伪造细节
- Group Consensus Reinforcer：强化群体共识
- Authority Endorser：用专家身份背书
- Questioning Compromiser：先质疑后被说服

这种角色分工会让错误叙事更可信。

---

#### Step 4：记忆巩固与检索

短期协议测试 agent 是否在当前上下文中受到影响。

长期协议则加入 memory consolidation 和 retrieval，用来观察错误信息是否被“记住”，并在后续对话中被重新调用。

这一步是本文区别于普通幻觉研究的关键。

---

### 6. 我认为重要的细节

MANBENCH 的重点不是简单问模型事实，而是观察：

现实基线  
→ 社会诱导  
→ 记忆检索

这个动态过程。

它关心的是模型如何在群体叙事中从正确答案转向错误答案，而不是单次回答是否正确。

---

## 三、实验

### 1. 数据集

MANBENCH 包含：

- 20 个任务
- 4,838 个问题
- 4 类知识域
- 5 种交互协议

四类知识域包括：

- History, Time & Events
- Misconceptions & Social Cognition
- General Knowledge
- Domain-Specific Knowledge

实验评估 13 个代表性 LLM，包括闭源模型和开源模型。

---

### 2. 对比方法

论文主要比较：

- 不同交互协议
- 不同模型
- 不同群体规模
- 不同知识领域
- 不同防御策略

Baseline Reality 是必要基线，用来判断 agent 原本是否具备正确知识。

---

### 3. 评价指标

论文使用的主要指标包括：

#### Error Rate

衡量最终回答错误的比例。

#### Reality Shift Rate

衡量 agent 从原本正确答案转向错误答案的比例。

#### Maximal Reality Shift Rate

衡量最强程度的现实偏移现象。

这些指标比单纯准确率更适合研究“从现实到错误记忆”的变化过程。

---

### 4. 实验结果及结论

论文发现：

- 几乎所有 LLM-based agent 都对曼德拉效应存在脆弱性。
- Role-based 协议比 generic 协议更容易诱发错误。
- Long-term 协议说明错误不只是即时从众，还可能经过记忆巩固后被检索出来。
- 专业领域和模糊知识领域更容易出现错误偏移。
- 防御策略平均减少 74.40% 的曼德拉效应。
- 论文提醒 MANBENCH 中的诱导模板不应被用于无监督训练，以免模型学会更易受操控的模式。

---

## 四、论文亮点

### 1. 问题新颖

论文把人类认知偏差引入 LLM 多智能体系统安全研究，关注“集体错误记忆”这一新问题。

### 2. 实验变量设计清晰

论文把群体组成和记忆时间尺度拆成可控变量，能够系统分析不同因素对曼德拉效应的影响。

### 3. 不是只看最终答案

论文关注现实基线如何被社会输入扭曲，而不是简单计算答对率。

### 4. 有伦理意识

论文强调诱导模板不应被滥用，并讨论了潜在误用风险。

---

## 五、局限性与我的批判性思考

### 1. 伪证据是模板化构造

真实世界的信息污染更加开放、复杂和不可预测。模板化伪证据可能无法覆盖全部现实场景。

### 2. 多智能体 memory 实现影响很大

不同 agent 框架的记忆机制不同，因此长期实验结果可能依赖具体实现方式。

### 3. 防御可能降低协作开放性

如果系统过度强调怀疑，可能降低多智能体讨论中的创造性和协作效率。

### 4. 选择题场景较受限

MANBENCH 多为有明确答案的选择题，但开放式复杂任务中的集体错误记忆更难评估。

---

## 六、论文总结（个人理解）

我理解这篇论文最有价值的地方在于：

它提醒我们，多智能体系统不是天然更可靠。

多个模型讨论并不一定能抵消错误，反而可能通过权威感、细节感和共识感，把错误变得更可信。

未来设计 agent 系统时，需要把事实锚定、来源审查和反方验证机制内置进去，而不能简单相信“多模型讨论一定更可靠”。

---

## 七、读完后可以继续追问的问题

1. MANBENCH 的交互协议是否贴近真实多智能体系统？
2. 如何区分 agent 原本不知道答案和被群体诱导产生错误记忆？
3. 多智能体系统中是否应该强制加入 fact-checker 角色？
4. 记忆模块的设计会如何影响曼德拉效应？
5. 开放式任务中的集体错误记忆应该如何评估？
