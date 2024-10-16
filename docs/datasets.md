---
title: Datasets
nav_order: 4.6
---

# Datasets
{: .no_toc}

> ***OpenR*** utilizes multiple datasets on math problems.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## 🧮 MATH

> ***OpenR*** use [MATH](https://github.com/openreasoner/openr/tree/main/envs/MATH) dataset [[Hendrycks et al., 2021]](https://arxiv.org/abs/2103.03874) for data augmentation. 

***OpenR*** augments the data by automatically generating synthetic samples using automated methods such as [OmegaPRM](https://arxiv.org/abs/2406.06592). This approach reduces the reliance
on expensive human annotations, enabling more scalable data collection. The data-processing code can be found at [`openr/data`](https://github.com/openreasoner/openr/tree/main/data).

## 🎲 MATH-APS

> MATH-APS is the MATH dataset processed by OmegaPRM. 

MATH-APS contains the *question, process* and *label* for each reasoning process. In the process, the solution is divided into multiple steps, each separated by a special step token (`\n\n\n\n\n`), marking the end of each step where the PRM can make predictions. The label is a classification of the entire process, with each step labelled as either `+` or `-` based on the correctness of the solution. MATH-APS scores steps with values between 0 and 1, so we label steps whose score is greater than 0.5
as positive and others negative.

We have released MATH-APS on [huggingface](https://huggingface.co/datasets/openreasoner/MATH-APS).


## 🔢 PRM800K

> The original dataset can be found in [this GitHub repo](https://github.com/openai/prm800k). 

<!-- ### Step tag
{: .no_toc}

We use `\n\n\n\n\n` as the step tag, which is appended to each step.

### For binary classification
{: .no_toc}

PRM800K has three labels: `good`, `neutral`, and `bad`, but we regard PRM training as a binary
classification problem. Hence, we treat steps labelled `neutral` or `good` in PRM800K as positive
ones and those labelled `bad` as negative ones.

### Multiple candidates for each step
{: .no_toc}

Each step may contain one or more completions in the original PRM800K. We include all the possible
combinations of these candidates in the training data. -->

<!-- ## ♟️ MATH-APS

>*OpenR* use automated methods such as OmegaPRM to synthesize a new dataset named *MATH-APS*.

This dataset was collected by us following the procedure introduced [here]({% link
docs/usage/data.md %}).

### For binary classification
{: .no_toc}

MATH-APS scores steps with values between 0 and 1, so we label steps whose score is greater than 0.5
as positive and others negative. -->

## 🧩 Math-Shepherd

> The original dataset can be found in [this Hugging Face dataset
repo](https://huggingface.co/datasets/peiyi9979/Math-Shepherd). It was used to train the
[Math-Shepherd](http://arxiv.org/abs/2312.08935) PRM.



## Integrated Datasets for PRM Training

The PRM is trained through supervised fine-tuning on an LLM, with the correct/incorrect
distinction serving as the classification label. We train a PRM named *Math-psa* using datasets such as `PRM800K`, `Math-Shepherd`, and our `MATH-APS` dataset. For detailed integration please refer to [openr/prm/code](https://github.com/openreasoner/openr/tree/main/prm/code).