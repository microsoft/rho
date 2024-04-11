

<h1 align="center">
<img src="./docs/static/images/rho_logo.png" width="100" alt="rho-logo" />
<br>
Rho-1: Not All Tokens Are What You Need
</h1>

<div align="center">

![](https://img.shields.io/badge/Model-Release%20Soon-blue)
![](https://img.shields.io/badge/Code%20License-MIT-green)

</div>

<p align="center">
  <a href="https://microsoft.github.io/rho/rho-1.pdf"><b>[📜 Paper]</b></a> •
  <!-- <a href="https://arxiv.org/abs/TODO"><b>[📜 Paper]</b></a> • -->
  <!-- <a href="https://huggingface.co/TODO"><b>[🤗 HF Models]</b></a> • -->
  <a href="https://github.com/microsoft/rho"><b>[🐱 GitHub]</b></a>
  <!-- <a href="https://twitter.com/TODO"><b>[🐦 Twitter]</b></a> -->
</p>

<p align="center">
    <img src="./docs/static/images/acc_vs_tokens_1b_7b.png" width="1000">
        <br>
    <em>Figure 1: Rho-1 is trained with Selective Language Modeling (SLM). SLM improves average few-shot accuracy on GSM8k and MATH by over 16%, achieving the baseline performance 5-10x faster.</em>
</p>


## 🔥 News

<!-- - [2024/04/12] 🔥🔥🔥 Rho-Math-v0.1 models released at [🤗 HuggingFace](https://huggingface.co/TODO)! -->
- [2024/04/11] Rho-1 paper and repo released.
- [2024/04/11] 🔥🔥🔥 Rho-1-1B is the first 1B LLM that achieves over 40% accuracy on MATH dataset.


## 💡 Introduction

Rho-1 employs Selective Language Modeling (SLM), which selectively trains on clean and useful tokens that aligned with the desired distribution.

- When continual pretraining on 15B OpenWebMath corpus, Rho-1 yields an absolute improvement in few-shot accuracy of up to 30% in 9 math tasks.
- After fine-tuning, Rho-1 1B and 7B achieved state-of-the-art results of 40.6\% and 51.8\% on MATH dataset, respectively — matching DeepSeekMath with only 3\% of the pretraining tokens.

### Selective Lanugage Modeling (SLM)

<p align="center">
    <img src="./docs/static/images/example.png" width="1000">
        <br>
    <em>Figure 2:
    <b>Upper:</b> Even an extensively filtered pretraining corpus contains token-level noise.
    <b>Left:</b> Previous Causal Language Modeling (CLM) trains on all tokens.
    <b>Right:</b> Our proposed Selective Language Modeling (SLM) selectively applies loss on those useful and clean tokens.</em>
</p>

<p align="center">
    <img src="./docs/static/images/pipeline.png" width="1000">
        <br>
    <em>Figure 3: <b>The pipeline of Selective Language Modeling.</b>
    SLM optimizes language model performance by concentrating on valuable, clean tokens during pre-training.
    It involves three steps:
    (Step 1) Initially, train a reference model on high-quality data.
    (Step 2) Then, score each token's loss in a corpus using the reference model.
    (Step 3) Finally, train the language model selectively on tokens that show higher excess loss compared to the reference loss.</em>
</p>



## 🚀 Quick Start

Code and models will be release within the next few days. Stay tuned!


## 🍀 Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.


## ☕️ Citation

If you find this repository helpful, please consider citing our paper:
```
arXiv on hold, update soon.
```


## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=microsoft/rho&type=Date)](https://star-history.com/#microsoft/rho&Date)