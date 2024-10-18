---
title: Home
layout: home
nav_order: 1
---

<!-- # ***OpenR***
{: .no_toc } -->

<h1>
  <span style="font-size: 40px;font-weight: bold;font-style: italic;"> OpenR</span>
  <span style="font-size: 20px;"> - An Open Source Framework for Advanced
Reasoning with LLMs</span>
</h1>

<!-- An Open Source Framework for Advanced
Reasoning with LLMs
{: .fs-6 .fw-300 } -->

[![GitHub contributors](https://img.shields.io/github/contributors/openreasoner/openr)][contributors-url]
[![arXiv](https://img.shields.io/badge/ArXiv-2410.09671-b31b1b.svg)](https://arxiv.org/pdf/2410.09671)
![GitHub License](https://img.shields.io/github/license/openreasoner/openr)
[![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/openreasoner/openr)][issues-url]
[![GitHub forks](https://img.shields.io/github/forks/openreasoner/openr)][forks-url]
[![GitHub Repo stars](https://img.shields.io/github/stars/openreasoner/openr)][stars-url]
[![HuggingFace Dataset](https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=000)](https://huggingface.co/openreasoner)
[![X](https://img.shields.io/badge/openreasoner-%23000000.svg?logo=X&logoColor=white)](#https://x.com/openreasoner)


<!-- 
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url] -->

<p align='center'>
<img src="./assets/images/openr_logo.png" alt="Description" width="200" />
<p align="center">
    <a href="https://arxiv.org/pdf/2410.09671">Paper</a>
    ·
    <a href="https://github.com/openreasoner/openr/blob/main/reports/Tutorial-LLM-Reasoning-Wang.pdf">Tutorial</a>
    ·
    <a href="https://github.com/openreasoner/openr/">Code</a>
    ·
    <a href="https://openreasoner.github.io/">Docs</a>
    ·
    <a href="https://huggingface.co/datasets/openreasoner/MATH-APS">Data</a>
    ·
    <a href="https://huggingface.co/openreasoner/Math-psa">Model</a>
    ·
    <a href="https://github.com/openreasoner/openr/issues">Issue</a>
    <!-- · -->
    <!-- <a href="https://medium.com/p/xxxxxx">Blog (Pytorch)</a> -->
    <!-- · -->
    <!-- <a href="https://nips.cc/virtual/xxxxx">Video</a> -->
  </p>
</p>

<p align="center">
    <a href="./docs/get-start.html" class="btn btn-primary fs-5 mb-4 mb-md-0 mr-2">Get started now</a>
    <a href="https://github.com/openreasoner/openr" class="btn fs-5 mb-4 mb-md-0">View it on GitHub</a>
</p>

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---



## 🚀 News and Updates

<span style="color: #555; font-weight: bold;">[11/10/2024]</span> Our paper is on <span style="color: #007acc;" > [**Arxiv**](https://arxiv.org/abs/2410.09671)</span> !

<span style="color: #555; font-weight: bold;">[11/10/2024]</span> <span style="color: #007acc;">*OpenR* has been released!</span>


## Key Features

<!-- <ul style="list-style-type: none; padding: 0;">
    <li><strong>✅ Test-time Computation</strong></li>
    <li><strong>✅ Test-time Scaling Law</strong></li>
    <li><strong>✅ Process-supervision Data Release</strong></li>
    <li><strong>✅ Support Online RL Training</strong></li>
    <li><strong>✅ Support both Generative and Discriminative PRM Training</strong></li>
    <li><strong>✅ Support Multiple Search Strategies</strong></li>
</ul> -->

<div style="display: flex; align-items: center;">
<ul style="list-style-type: none; padding: 0;">
    <li><strong>✅ Process-supervision Data Release</strong></li>
    <li><strong>✅ Online RL Training</strong></li>
    <li><strong>✅ Generative and Discriminative PRM Training</strong></li>
    <li><strong>✅ Multiple Search Strategies</strong></li>
    <li><strong>✅ Test-time Computation</strong></li>
    <li><strong>✅ Test-time Scaling Law</strong></li>
</ul>
    <img src="./assets/images/logo_text.png" alt="Description" style="width: 300px; margin-left: 50px; float: right;">
</div>

## What is *OpenR*?

> ***OpenR*** is an open-source framework that integrates **search**, **reinforcement learning** and **process supervision** to improve **reasoning** in Large Language Models.




OpenAI o1 has demonstrated that leveraging reinforcement learning to inherently
integrate reasoning steps during inference can greatly improve a model’s reasoning abilities. 

We attribute these enhanced reasoning capabilities to the integration of **search**, **reinforcement learning**, and **process supervision**, which collectively drive the development of ***OpenR***.


Our work is the first to provide an open-source framework demonstrating how the effective utilization of these techniques enables LLMs to achieve advanced reasoning capabilities, 



## What Can *OpenR* Do?

> We believe the ability of reasoning can be improved by the following:

<img src="./assets/images/code_framework.png" width="800px" height="600px" />

<!-- OpenReasoner is an open-source framework designed to enhance reasoning capabilities in Large Language Models (LLMs) by focusing on three key pathways: -->

- **Data Acquisition**: This pathway emphasizes the critical role of high-quality, diverse datasets in training LLMs. It includes data collection for both model pre-training and fine-tuning, with a specific focus on **reasoning** process, which are central to *OpenR*'s objectives. Given the significant costs associated with human annotation of reasoning data, **we offer an automated pipeline that extracts reasoning steps from outcome labels**, reducing manual effort while ensuring the collection of valuable reasoning information.

- **Training**: This pathway centers around training strategies that enhance the reasoning capabilities of LLMs, from the perspective of both generative models and reward models. *OpenR* provide toolkits such as **online reinforcement learning** to train LLMs as the proposer, and methods to learn **Process-supervision Reward Models** (PRMs) as the verifier.

- **Inference**: This pathway focuses on the scaling law at test-time, enabling LLM to give refined outputs through ways of generation or searching. *OpenR* allows us to **select among various search algorithms**—such as *beam search*, *best-of-N selection*, and others—each with unique advantages depending on the quality of the process reward models.



## How to *OpenR*?

In the documentation, we provide some runnable code example as well as detailed usage of some key modules in the framework.

<ul>
  <li><a href="./docs/get-start.html">Quick Start</a> contains some ready-to-run code examples that can give you a head start on <strong><em>OpenR</em></strong>.</li>
  <li><a href="./docs/usage/index.html">Usage</a> discuss details of key modules in the codebase.</li>
  <li><a href="./docs/datasets.html">Datasets</a> give you a sense of how we use data in our experiments.</li>
</ul>

To any interested in making ***OpenR*** better, there are still improvements that need to be done. We welcome any form of contribution and feel free to have a look at our [contribution guidance](https://github.com/openreasoner/openr/blob/main/CONTRIBUTING.md).


## Citing *OpenR*

To cite this project in publications:

```text
@article{wang2024openr,
  title={OpenR: An Open Source Framework for Advanced Reasoning with Large Language Models},
  author={Wang, Jun and Fang, Meng and Wan, Ziyu and Wen, Muning and Zhu, Jiachen and Liu, Anjie and Gong, Ziqin and Song, Yan and Chen, Lei and Ni, Lionel M and others},
  journal={arXiv preprint arXiv:2410.09671},
  year={2024}
}
```


<!-- MARKDOWN LINKS & IMAGES -->

<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/openreasoner/openr.svg?style=for-the-badge
[contributors-url]: https://github.com/openreasoner/openr/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/openreasoner/openr.svg?style=for-the-badge
[forks-url]: https://github.com/openreasoner/openr/network/members
[stars-shield]: https://img.shields.io/github/stars/openreasoner/openr.svg?style=for-the-badge
[stars-url]: https://github.com/openreasoner/openr/stargazers
[issues-shield]: https://img.shields.io/github/issues/openreasoner/openr.svg?style=for-the-badge
[issues-url]: https://github.com/openreasoner/openr/issues

[license-shield]: https://img.shields.io/github/license/openreasoner/openr.svg?style=for-the-badge
[license-url]: https://github.com/openreasoner/openr/blob/main/LICENSE.txt