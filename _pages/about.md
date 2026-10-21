---
permalink: /
title: 
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% include base_path %}

**I'm Zelin He, a final-year Ph.D. candidate at Penn State working on end-to-end LLM agent training and development.**

My work centers on co-optimizing the harness (memory, skills, context compression, middleware) with the policy (SFT, RL, on-policy distillation), for real-world performance that generalizes, at minimal training cost and with efficient inference.

This line runs through two consecutive projects at AWS AI Labs, on context injection and on skill optimization with RL training ([ReSkill](https://github.com/amazon-science/reskill)), to my recent work at LinkedIn, where I built both the training infrastructure and the method for RL with a data-driven, evolving harness. Applications range from coding, web shopping and scientific discovery to industrial end-to-end agentic search. I'm advised by Dr. [Runze Li](https://runzelipsu.github.io/) and work with Dr. [Ying Sun](https://ysunac.github.io/) (EECS).

<h2 id="experience">Experience</h2>

<div class="xp">

<div class="xp-entry">
  <div class="xp-when">May 2026 – now
    <span class="xp-logo sq"><img src="{{ base_path }}/images/logos/linkedin.svg" alt="LinkedIn"></span>
    <span class="xp-team">Agentic Modeling &amp; Foundation Team</span></div>
  <div class="xp-what">
    <h3>Training infrastructure and recursive harness optimization</h3>
    <p class="xp-role">AI/ML Engineer Intern</p>
    <p>The harness decides what an agent sees of its own history and what guidance it gets. It is usually hand-written and frozen during RL. My work treats it as something the system learns.</p>
    <ul>
      <li>Built a harness-transparent LLM gateway between agent applications and model serving. It records every model call as one token-level trace for SFT and RL, and is deployed for LinkedIn's production post-training.</li>
      <li>CoHarness-RL recasts the harness as programs over a typed state, with a compression program that builds the context and a steering program that gives advice when behavior drifts. Candidates are proposed from trajectories and replayed over past ones before adoption.</li>
      <li>Beat memory, skill, prompt and harness-evolution baselines by 5 to 12% on held-out CodeSearch, with compression close to frontier-model compaction at over 100x fewer teacher calls.</li>
    </ul>
    <div class="xp-links"><span class="venue">Under review</span><span class="soon">Paper coming soon</span></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/coharness.png" alt="A raw transcript passes through compression and steering programs to produce an updated transcript"><figcaption>CoHarness-RL treats the harness as compression and steering programs over the interaction state.</figcaption></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-when">Feb – May 2026
    <span class="xp-logo fill"><img src="{{ base_path }}/images/logos/aws.svg" alt="AWS"></span>
    <span class="xp-team">Model Customization</span></div>
  <div class="xp-what">
    <h3>ReSkill <span class="xp-tag">Skills that evolve with the policy</span></h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>A skill creator diagnoses failures from past experience and proposes trigger-based skill edits. Each new version has to win a counterfactual A/B test inside GRPO's rollout groups before it is adopted.</li>
      <li>Thompson sampling with an adaptive discount decides which skill version to use as the policy keeps changing.</li>
      <li>+14.5% over the GRPO baseline, against +8.6% for the strongest of eight baselines, with the largest gains on unseen tasks.</li>
      <li>Also shipped a five-stage multi-agent workflow built on Strands, at 98% accuracy and 5x labeler speed across 50+ facility launches.</li>
    </ul>
    <div class="xp-links"><span class="venue">Under review</span><a href="https://amazon-science.github.io/reskill/">Project page</a><a href="https://arxiv.org/abs/2606.01619">Paper</a><a href="https://github.com/amazon-science/reskill">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/reskill.jpg" alt="ReSkill overview"><figcaption>ReSkill reconciles skill creation with policy optimization.</figcaption></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-when">May – Sept 2025
    <span class="xp-logo fill"><img src="{{ base_path }}/images/logos/aws.svg" alt="AWS"></span>
    <span class="xp-team">AutoML (AutoGluon)</span></div>
  <div class="xp-what">
    <h3>SenTSR-Bench <span class="xp-tag">Thinking with injected knowledge</span></h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>Built a benchmark for diagnostic reasoning on production sensor data, with a VLM-driven synthetic-data pipeline that scales training data 260x.</li>
      <li>A small time-series model, trained with SFT and RL, writes its analysis straight into a frozen reasoning model's thinking, reaching +11.2% accuracy over Claude 3.7 and Qwen3.</li>
      <li>Piloted the system with 5x faster inference than comparable commercial model APIs.</li>
    </ul>
    <div class="xp-links"><span class="venue">AISTATS 2026</span><a href="https://arxiv.org/abs/2602.19455">Paper</a><a href="https://github.com/ZLHe0/SenTSR-Bench">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/sentsr.png" alt="Knowledge injection from a time-series LM into a reasoning LM"><figcaption>Knowledge injection, and the RL loop that hones the specialist's thinking traces.</figcaption></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-when">May – Aug 2024
    <span class="xp-logo"><img src="{{ base_path }}/images/logos/amazon.svg" alt="Amazon"></span>
    <span class="xp-team">IntelliHub</span></div>
  <div class="xp-what">
    <h3>VLM4TS <span class="xp-tag">Vision-language models for anomaly detection</span></h3>
    <p class="xp-role">Applied Scientist Intern</p>
    <ul>
      <li>A lightweight Vision Transformer screens sensor data and a vision-language model verifies the flagged windows, lifting F1 by 24.6% at 36x lower token cost.</li>
      <li>Evaluated on 130 assets at Amazon fulfillment centers and three public benchmarks.</li>
    </ul>
    <div class="xp-links"><span class="venue">AAAI 2026 Oral</span><a href="https://arxiv.org/pdf/2506.06836">Paper</a><a href="https://github.com/ZLHe0/VLM4TS">Code</a></div>
    <figure class="xp-fig"><img src="{{ base_path }}/images/work/vlm4ts.jpg" alt="VLM4TS pipeline with anomaly scores and a performance comparison"><figcaption>Visual screening, then visual reasoning.</figcaption></figure>
  </div>
</div>

<div class="xp-entry">
  <div class="xp-when">Aug 2022 – now
    <span class="xp-logo"><img src="{{ base_path }}/images/logos/pennstate.svg" alt="Penn State"></span>
    <span class="xp-team">Statistics, with EECS</span></div>
  <div class="xp-what">
    <h3>Statistical machine learning</h3>
    <p class="xp-role">Graduate Researcher</p>
    <p>Transfer learning that stays robust under covariate shift, personalized federated learning with minimax guarantees, and a power-calibrated framework for tuning LLM watermarks.</p>
    <div class="xp-links"><span class="venue">ICML 2026</span><span class="venue">ICML 2025</span><span class="venue">AISTATS 2024</span><span class="venue">JMLR</span></div>
  </div>
</div>

</div>

<h2 id="papers">Selected Papers</h2>

- ReSkill: Reconciling Skill Creation with Policy Optimization in Agentic RL (under review) [[Website](https://amazon-science.github.io/reskill/)] [[Paper](https://arxiv.org/abs/2606.01619)] [[Code](https://github.com/amazon-science/reskill)]
  - **Zelin He**, Haotian Lin, Boran Han, Wei Zhu, Haoyang Fang, Bernie Wang, Xuan Zhu, Runze Li, Matthew Reimherr
- CoHarness-RL: Recasting Harnesses as Learnable and Evolving Programs for Agentic RL (under review, coming soon)
- Beyond Heuristic Tuning: Power-Calibrated LLM Watermarking [[Paper](https://arxiv.org/abs/2607.05694)]
  - Xiaopu Wang, **Zelin He**, Chengyuan Liu, Runze Li
  - *International Conference on Machine Learning (ICML), 2026*
- Harnessing Vision-Language Models for Time Series Anomaly Detection [[Paper](https://arxiv.org/pdf/2506.06836)] [[Code](https://github.com/ZLHe0/VLM4TS)]
  - **Zelin He**, Sarah Alnegheimish, Matthew Reimherr
  - *AAAI Conference on Artificial Intelligence (AAAI), 2026* <span style="color:blue">(Oral)</span>
- SenTSR-Bench: Thinking with Injected Knowledge for Time-Series Reasoning [[Paper](https://arxiv.org/abs/2602.19455)] [[Code](https://github.com/ZLHe0/SenTSR-Bench)]
  - **Zelin He**, Boran Han, Xiyuan Zhang, Shuai Zhang, Haotian Lin, Qi Zhu, Haoyang Fang, Danielle C. Maddix, Abdul Fatir Ansari, Akash Chandrayan, Abhinav Pradhan, Bernie Wang, Matthew Reimherr
  - *International Conference on Artificial Intelligence and Statistics (AISTATS), 2026*
- Understanding the Statistical Accuracy-Communication Trade-off in Personalized Federated Learning with Minimax Guarantees [[Paper](https://arxiv.org/abs/2410.08934)] [[Code](https://github.com/ZLHe0/fedprox-bilevel)]
  - Xin Yu\*, **Zelin He\***, Ying Sun, Lingzhou Xue, Runze Li
  - *International Conference on Machine Learning (ICML), 2025*

<details markdown="1">
<summary>More papers</summary>

- M<sup>2</sup>AD: Multi-Sensor Multi-System Anomaly Detection through Global Scoring and Calibrated Thresholding
  - Sarah Alnegheimish, **Zelin He**, Matthew Reimherr, Akash Chandrayan, Abhinav Pradhan, Luca D'Angelo
  - *International Conference on Artificial Intelligence and Statistics (AISTATS), 2025*
- TransFusion: Covariate-Shift Robust Transfer Learning for High-Dimensional Regression [[Paper](https://proceedings.mlr.press/v238/he24a.html)] [[Code](https://github.com/ZLHe0/TransFusion)]
  - **Zelin He**, Ying Sun, Runze Li
  - *International Conference on Artificial Intelligence and Statistics (AISTATS), 2024*
- High-dimensional Parameter Transfer With Fused-Regularizer
  - **Zelin He**, Ying Sun, Jingyuan Liu, Runze Li
  - *Journal of Machine Learning Research (JMLR)*
- Weakly-supervised Multi-sensor Anomaly Detection with Time-series Foundation Models
  - **Zelin He**, Matthew Reimherr, Sarah Alnegheimish, Akash Chandrayan
  - *NeurIPS 2024 TSALM Workshop*
- AdaTrans: Feature-wise and Sample-wise Adaptive Transfer Learning for High-dimensional Regression (preprint) [[Paper](https://arxiv.org/abs/2403.13565)] [[Slides](files/trans-slides.pdf)] [[Poster](files/trans-poster.pdf)]
  - **Zelin He**, Ying Sun, Jingyuan Liu, Runze Li

</details>

Full list on [Google Scholar](https://scholar.google.com/citations?user=cqhRdPoAAAAJ&hl=en). \* equal contribution.

<h2 id="chat">Let's chat</h2>

<div class="chat-note">
<p>I'm always glad to talk about agents, reinforcement learning and post-training. If something here connects with what you're working on, send me a note at <span class="mail">zelinhe0@outlook.com</span>.</p>
</div>

## Education
- Ph.D. in Statistics, Pennsylvania State University, 2022 – Dec 2026
- B.S. in Statistics, Beijing Normal University, 2018 – 2022

## Honors
- University Graduate Fellowship, 2023
- Early Pass of the Doctoral Theory Qualifying Exam, 2022
- Paul M. Doty Distinguished Graduate Fellowship, 2022
- Verne M. Willaman Distinguished Graduate Fellowship in Science, 2022
- National Scholarship, 2021

## Reviewing
ICML, ICLR, NeurIPS, JASA, TNNLS, JCGS
