---
layout: default
title: 学习笔记
page_style: landing
description: Web API Recommendation 与 LLM Safety 学习记录。
---

<section class="hero-banner">
  <p class="eyebrow">Research Notebook</p>
  <h1>学习笔记</h1>
  <p class="lead">这里用于持续记录我的学习过程，包括论文阅读笔记、概念理解、研究问题整理以及阶段性学习总结。当前内容主要沿着两条主线展开。</p>
</section>

<section class="section-block">
  <div class="section-header">
    <p class="eyebrow">Themes</p>
    <h2>两条长期学习主线</h2>
  </div>
  <div class="cards-grid cards-grid--split">
    <article class="content-card">
      <span class="paper-card__meta">Theme 01</span>
      <h3><a href="{{ '/notes/web-api-recommendation/' | relative_url }}">Web API Recommendation</a></h3>
      <p>这是我本科阶段主要参与研究的方向，重点关注 Web API 推荐、服务计算、图协同过滤、多模态推荐和互补推荐等问题。</p>
      <ul class="bullet-list">
        <li>任务定义与数据建模</li>
        <li>文本语义与图结构表示</li>
        <li>多模态与互补推荐方法</li>
      </ul>
      <div class="topic-actions">
        <a class="button button--secondary" href="{{ '/notes/web-api-recommendation/' | relative_url }}">查看主题页</a>
      </div>
    </article>
    <article class="content-card">
      <span class="paper-card__meta">Theme 02</span>
      <h3><a href="{{ '/notes/llm-safety/' | relative_url }}">LLM Safety / Trustworthy AI</a></h3>
      <p>这是我近期开始系统学习的新方向，主要关注大语言模型安全、对抗攻击、防御机制、可信推理与多智能体可靠性等内容。</p>
      <ul class="bullet-list">
        <li>诈骗文本与模型诱导</li>
        <li>文本与多模态对抗攻击</li>
        <li>安全评测与可靠推理</li>
      </ul>
      <div class="topic-actions">
        <a class="button button--secondary" href="{{ '/notes/llm-safety/' | relative_url }}">查看主题页</a>
      </div>
    </article>
  </div>
</section>

<section class="section-block">
  <div class="section-header">
    <p class="eyebrow">Current Notes</p>
    <h2>当前已整理内容</h2>
  </div>
  <div class="cards-grid cards-grid--split">
    <article class="content-card">
      <h3>Web API Recommendation</h3>
      <p>该部分正在持续整理中，后续将逐步补充从基础任务定义到方法演进的系统化笔记。</p>
      <ul class="note-links">
        <li><a href="{{ '/notes/web-api-recommendation/' | relative_url }}">Web API 推荐任务介绍与主题入口</a></li>
        <li><a href="{{ '/achievements/tssgcf.html' | relative_url }}">TSSGCF 相关成果回看</a></li>
        <li><a href="{{ '/achievements/mmc-webapi.html' | relative_url }}">互补式 Web API 推荐相关成果回看</a></li>
      </ul>
    </article>
    <article class="content-card">
      <h3>LLM Safety / Trustworthy AI</h3>
      <p>目前已经开始积累若干篇典型论文的阅读笔记，作为后续专题学习和问题总结的基础。</p>
      <ul class="note-links">
        <li><a href="{{ '/notes/llm-safety/fraudshield.html' | relative_url }}">FraudShield 阅读笔记</a></li>
        <li><a href="{{ '/notes/llm-safety/textbugger.html' | relative_url }}">TEXTBUGGER 阅读笔记</a></li>
        <li><a href="{{ '/notes/llm-safety/multipun.html' | relative_url }}">MULTIPUN 阅读笔记</a></li>
        <li><a href="{{ '/notes/llm-safety/manbench.html' | relative_url }}">MANBENCH 阅读笔记</a></li>
      </ul>
    </article>
  </div>
</section>

<section class="section-block section-block--two-column">
  <article class="content-card">
    <div class="section-header section-header--compact">
      <p class="eyebrow">Next</p>
      <h2>后续更新计划</h2>
    </div>
    <ul class="timeline-list">
      <li>补充 Web API 推荐方向的基础概念与方法脉络。</li>
      <li>继续扩展 LLM Safety 方向论文精读与问题整理。</li>
      <li>沉淀重要概念解释、研究问题总结和论文框架拆解。</li>
    </ul>
  </article>
  <article class="content-card accent-card">
    <div class="section-header section-header--compact">
      <p class="eyebrow">Why Notes</p>
      <h2>这部分内容的目标</h2>
    </div>
    <p>我希望这些笔记不仅服务于“记住论文内容”，也能帮助我逐步形成自己的研究视角：知道哪些问题值得继续追、哪些方法有局限、哪些概念需要重新理解。</p>
  </article>
</section>
