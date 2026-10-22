---
permalink: /
title: 
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% include base_path %}

**I'm Zelin He. I work on end-to-end LLM agent training and development.**

My work centers on co-optimizing the harness (memory, skills, context compression, middleware) with the policy (SFT, RL, on-policy distillation), for real-world performance that generalizes, at minimal training cost and with efficient inference.

This line runs through two projects at AWS AI Labs, on context injection and on [skill optimization with RL training](https://github.com/amazon-science/reskill), to my recent work at LinkedIn AMF, where I built both the training infrastructure and the method for RL with a data-driven, evolving harness. Applications range from coding, web shopping and scientific discovery to industrial end-to-end agentic search.

<h2 id="experience">Experience</h2>

<div class="xp">

<div class="xp-entry">
  <div class="xp-org">
    <span class="xp-logo sq"><img src="{{ base_path }}/images/logos/linkedin.svg" alt="LinkedIn"></span>
    <span class="xp-team">Agentic Modeling &amp; Foundation Team</span>
    <span class="xp-lead">led by <a href="https://code-terminator.github.io/">Shiyu Chang</a></span>
    <span class="xp-time">May 2026 – now</span></div>
  <div class="xp-what">
    <h3>Training infrastructure and recursive harness optimization</h3>
    <p class="xp-role">AI/ML Engineer Intern</p>
    
    <ul>
      <li>Recast the harness as configurable programs an LLM learns from experience, on harness-agnostic infrastructure that faithfully traces every model call for training and inference.</li>
      <li>Evolving with the model in RL, it steps in only where the model can't improve alone, beating strong baselines by 5 to 12% on coding and nearing frontier-model compaction at a fraction of the cost.</li>
    </ul>
    <div class="xp-links"><span class="soon">Paper coming soon</span></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/coharness_infra.png" alt="Harness optimization, a rollout service with gateway nodes and an inference engine, and policy optimization with a trainer"></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-org">
    <span class="xp-logo fill"><img src="{{ base_path }}/images/logos/aws.svg" alt="AWS"></span>
    <span class="xp-team">AWS AI Labs<br>(Model Customization)</span>
    <span class="xp-lead">led by <a href="https://www.ischool.berkeley.edu/people/jennifer-zhu">Jennifer Zhu</a></span>
    <span class="xp-time">Feb – May 2026</span></div>
  <div class="xp-what">
    <h3>Skill and policy co-evolution in agentic RL</h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>Brings end-to-end skill creation into RL, writing skills from agent failures and A/B testing versions within GRPO's rollout groups, where Thompson Sampling keeps winners at no extra rollout cost.</li>
      <li>Beats strong RL baselines in all five domains by 5.6 points on average (1.3 to 15.8), and by up to 21.9 on out-of-domain tasks.</li>
    </ul>
    <div class="xp-links"><a href="https://arxiv.org/abs/2606.01619">Paper</a><a href="https://github.com/amazon-science/reskill">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/reskill_pipeline.png" alt="ReSkill pipeline with within-group skill testing, the skill creator, and adaptive Thompson Sampling"></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-org">
    <span class="xp-logo fill"><img src="{{ base_path }}/images/logos/aws.svg" alt="AWS"></span>
    <span class="xp-team">AWS AI Labs<br>(AutoML)</span>
    <span class="xp-lead">led by <a href="https://www.mit.edu/~ywang02/">Bernie Wang</a></span>
    <span class="xp-time">May – Sept 2025</span></div>
  <div class="xp-what">
    <h3>Injecting fine-tuned expert knowledge into frontier reasoning</h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>Pairs a frozen frontier model with a small fine-tuned domain expert by writing the expert's analysis into the frontier model's thinking, so it builds on that evidence or corrects it.</li>
      <li>RL trains the expert to write analysis worth injecting, without human annotation, beating either model alone by 8 to 26%.</li>
    </ul>
    <div class="xp-links"><a href="https://arxiv.org/abs/2602.19455">Paper</a><a href="https://github.com/ZLHe0/SenTSR-Bench">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/sentsr.png" alt="Knowledge injection from a time-series LM into a reasoning LM"></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-org">
    <span class="xp-logo"><img src="{{ base_path }}/images/logos/amazon.svg" alt="Amazon"></span>
    <span class="xp-team">IntelliHub</span>
    <span class="xp-lead">led by <a href="https://mreimherr.github.io/">Matthew Reimherr</a></span>
    <span class="xp-time">May – Aug 2024</span></div>
  <div class="xp-what">
    <h3>Visual screening and VLM reasoning for anomaly detection</h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>A zero-shot two-stage pipeline, where a lightweight vision encoder screens the full signal in seconds on CPU and a VLM verifies only the flagged candidates in long-range context.</li>
      <li>Lifts F1 by 24.6% over the best trained baseline on 11 benchmarks, with 36x fewer tokens than language-model methods.</li>
    </ul>
    <div class="xp-links"><a href="https://arxiv.org/pdf/2506.06836">Paper</a><a href="https://github.com/ZLHe0/VLM4TS">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/vlm4ts.jpg" alt="VLM4TS pipeline with anomaly scores and a performance comparison"></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-org">
    <span class="xp-logo"><img src="{{ base_path }}/images/logos/pennstate.svg" alt="Penn State"></span>
    <span class="xp-team">Statistics, with EECS</span>
    <span class="xp-time">Aug 2022 – now</span></div>
  <div class="xp-what">
    <h3>Statistical machine learning</h3>
    <p class="xp-role">Graduate Researcher</p>
    <p>Transfer learning that stays robust under covariate shift, personalized federated learning with minimax guarantees, and a power-calibrated framework for tuning LLM watermarks.</p>
  </div>
</div>

</div>

<h2 id="papers">Selected Papers</h2>

<div class="pubs">
<div class="pub">
  <div class="pub-title">ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Haotian Lin, Boran Han, Wei Zhu, Haoyang Fang, and 4 more</div>
  <div class="pub-venue">Under review</div>
  <div class="xp-links"><a href="https://amazon-science.github.io/reskill/">Project page</a><a href="https://arxiv.org/abs/2606.01619">Paper</a><a href="https://github.com/amazon-science/reskill">Code</a></div>
</div>
<div class="pub">
  <div class="pub-title">CoHarness-RL: Recasting Harnesses as Learnable and Evolving Programs for Agentic RL</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Siyu Zhu, Jacob Helwig, Yujian Liu, Li An, and 3 more</div>
  <div class="pub-venue">Under review</div>
  <div class="xp-links"><span class="soon">Paper coming soon</span></div>
</div>
<div class="pub">
  <div class="pub-title">Beyond Heuristic Tuning: Power-Calibrated LLM Watermarking</div>
  <div class="pub-authors">Xiaopu Wang, <strong>Zelin He</strong>, Chengyuan Liu, Runze Li</div>
  <div class="pub-venue"><strong>ICML</strong> 2026</div>
  <div class="xp-links"><a href="https://arxiv.org/abs/2607.05694">Paper</a></div>
</div>
<div class="pub">
  <div class="pub-title">Harnessing Vision-Language Models for Time Series Anomaly Detection</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Sarah Alnegheimish, Matthew Reimherr</div>
  <div class="pub-venue"><strong>AAAI</strong> 2026, <strong class="oral">Oral</strong></div>
  <div class="xp-links"><a href="https://arxiv.org/pdf/2506.06836">Paper</a><a href="https://github.com/ZLHe0/VLM4TS">Code</a></div>
</div>
<div class="pub">
  <div class="pub-title">SenTSR-Bench: Thinking with Injected Knowledge for Time-Series Reasoning</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Boran Han, Xiyuan Zhang, Shuai Zhang, Haotian Lin, and 8 more</div>
  <div class="pub-venue"><strong>AISTATS</strong> 2026</div>
  <div class="xp-links"><a href="https://arxiv.org/abs/2602.19455">Paper</a><a href="https://github.com/ZLHe0/SenTSR-Bench">Code</a></div>
</div>
<div class="pub">
  <div class="pub-title">Understanding the Statistical Accuracy-Communication Trade-off in Personalized Federated Learning with Minimax Guarantees</div>
  <div class="pub-authors">Xin Yu*, <strong>Zelin He*</strong>, Ying Sun, Lingzhou Xue, Runze Li</div>
  <div class="pub-venue"><strong>ICML</strong> 2025</div>
  <div class="xp-links"><a href="https://arxiv.org/abs/2410.08934">Paper</a><a href="https://github.com/ZLHe0/fedprox-bilevel">Code</a></div>
</div>
<div class="pub">
  <div class="pub-title">M<sup>2</sup>AD: Multi-Sensor Multi-System Anomaly Detection through Global Scoring and Calibrated Thresholding</div>
  <div class="pub-authors">Sarah Alnegheimish, <strong>Zelin He</strong>, Matthew Reimherr, Akash Chandrayan, Abhinav Pradhan, Luca D'Angelo</div>
  <div class="pub-venue"><strong>AISTATS</strong> 2025</div>
</div>
<div class="pub">
  <div class="pub-title">TransFusion: Covariate-Shift Robust Transfer Learning for High-Dimensional Regression</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Ying Sun, Runze Li</div>
  <div class="pub-venue"><strong>AISTATS</strong> 2024</div>
  <div class="xp-links"><a href="https://proceedings.mlr.press/v238/he24a.html">Paper</a><a href="https://github.com/ZLHe0/TransFusion">Code</a></div>
</div>
</div>

<details class="pub-more">
<summary>More papers</summary>
<div class="pubs">
<div class="pub">
  <div class="pub-title">High-dimensional Parameter Transfer With Fused-Regularizer</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Ying Sun, Jingyuan Liu, Runze Li</div>
  <div class="pub-venue"><strong>JMLR</strong></div>
</div>
<div class="pub">
  <div class="pub-title">Weakly-supervised Multi-sensor Anomaly Detection with Time-series Foundation Models</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Matthew Reimherr, Sarah Alnegheimish, Akash Chandrayan</div>
  <div class="pub-venue"><strong>NeurIPS</strong> 2024 TSALM Workshop</div>
</div>
<div class="pub">
  <div class="pub-title">AdaTrans: Feature-wise and Sample-wise Adaptive Transfer Learning for High-dimensional Regression</div>
  <div class="pub-authors"><strong>Zelin He</strong>, Ying Sun, Jingyuan Liu, Runze Li</div>
  <div class="pub-venue">Preprint</div>
  <div class="xp-links"><a href="https://arxiv.org/abs/2403.13565">Paper</a><a href="{{ base_path }}/files/trans-slides.pdf">Slides</a><a href="{{ base_path }}/files/trans-poster.pdf">Poster</a></div>
</div>
</div>
</details>

<p class="pub-note">* equal contribution.</p>

<h2 id="chat">Let's chat</h2>

<div class="chat-note">
<p>I'm always thrilled to connect, whether it's about a new collaboration, a team building something ambitious, or just swapping notes on what you're working on. Say hello at <span class="mail">zelinhe0@gmail.com</span>!</p>
</div>
