---
title: Deep Generative Modeling Blog
title_en: Deep Generative Modeling Blog (jmtomczak.github.io)
created: 2026-04-28
updated: 2026-04-28
type: concept
tags: [review, generative-models, blog, tutorial, deep-learning]
sources: []
confidence: high
---

# Deep Generative Modeling Blog

> 作者：[[jakub-m-tomczak|Jakub M. Tomczak]]
> 地址：[jmtomczak.github.io](https://jmtomczak.github.io/)

## 简介

这是 Jakub M. Tomczak 的个人技术博客，内容以**深度生成模型**为主线，从最基础的概率论出发，系统性地覆盖了生成式深度学习的所有主流范式。每一篇都兼具数学严谨性和代码可读性，被社区誉为"深度学习生成模型最好的入门系列之一"。

博客系列与他的著作《Deep Generative Modeling》（Springer 出版）相辅相成，但博客更侧重于**直观理解**和**推导过程**，而书更侧重完整体系。

## 博文目录

### 基础篇
| # | 标题 | 内容概要 |
|---|------|---------|
| 1 | [Introduction](https://jmtomczak.github.io/blog/1/1_introduction.html) | 为什么需要生成模型？三大流派总览：ARM、Flow、LVM |
| 2 | [Autoregressive Models](https://jmtomczak.github.io/blog/2/2_ARM.html) | 自回归模型核心思想：概率链式法则分解 |
| 3 | [Flow-based Models](https://jmtomczak.github.io/blog/3/3_flows.html) | 归一化流：可逆变换下的密度估计 |
| 4 | [VAE](https://jmtomczak.github.io/blog/4/4_VAE.html) | 变分自编码器：ELBO、重参数化技巧 |
| 5 | [Improved Density Flow (IDF)](https://jmtomczak.github.io/blog/5/5_IDF.html) | 改进的密度流模型 |
| 6 | [Hybrid Models](https://jmtomczak.github.io/blog/6/6_hybrid.html) | 混合模型：结合不同生成范式 |
| 7 | [VAE Priors](https://jmtomczak.github.io/blog/7/7_priors.html) | VAE 先验的重要性——被忽视的关键组件 |

### 进阶篇
| # | 标题 | 内容概要 |
|---|------|---------|
| 8 | [Neural Compression](https://jmtomczak.github.io/blog/8/8_neural_compression.html) | 生成模型与神经压缩的深层联系 |
| 9 | [Hierarchical LVMs (Part 1)](https://jmtomczak.github.io/blog/9/9_hierarchical_lvm_p1.html) | 层次化潜变量模型 |
| 10 | [Diffusion-based DGMs (Part 2)](https://jmtomczak.github.io/blog/10/10_ddgms_lvm_p2.html) | 扩散模型（DDGM / DDPM） |
| 11 | [Energy-Based Models](https://jmtomczak.github.io/blog/11/11_energy_based_models.html) | 能量模型与 Langevin 动力学 |
| 12 | [GANs](https://jmtomczak.github.io/blog/12/12_gans.html) | 生成对抗网络 |
| 15 | [ARMs × Transformers](https://jmtomczak.github.io/blog/15/15_transformers.html) | Transformer 参数化的自回归模型 |
| 16 | [Score Matching](https://jmtomczak.github.io/blog/16/16_score_matching.html) | 基于分数的模型：Score Matching 方法 |
| 17 | [Score-based GMs (SDEs/ODEs)](https://jmtomczak.github.io/blog/17/17_sbgms.html) | 基于分数的生成模型与 SDE/ODE 框架 |
| 18 | [Flow Matching](https://jmtomczak.github.io/blog/18/18_fm.html) | 流匹配——用 ODE 做生成 |
| 19 | [Mixture Models](https://jmtomczak.github.io/blog/19/19_mog_pcs.html) | 混合模型视角下的生成建模 |

### 前沿篇
| # | 标题 | 内容概要 |
|---|------|---------|
| 21 | [GenAISys](https://jmtomczak.github.io/blog/21/21_genaisys.html) | 生成式 AI 系统：将生成模块组合为完整 AI 系统 |

> 注：#13、#14、#20 暂未确认对应的公开博文。

## 博客特点

1. **系统性极强**：不是零散的博文，而是一个精心设计的课程，前后呼应、层层递进
2. **数学与直觉并重**：每个模型既给出完整推导，又讲清楚直觉
3. **统一视角**：始终强调生成式建模是 AI 理解世界、表达不确定性的核心工具，而不仅是数据生成器
4. **代码配套**：博客常引用配套 [GitHub 仓库](https://github.com/jmtomczak/intro_dgm) 中的实现

## 与分子图生成研究的关联

Tomczak 的博客直接覆盖了当前分子图生成的**全部主流技术路线**：

- [[vae|VAE]] → 分子图 VAE（如 GraphVAE、JT-VAE）
- [[flow-based-models|Flow-based Models]] → 分子图上的归一化流
- [[diffusion-models|Diffusion Models]] → 分子图扩散模型（如 DiGress、MDM）
- [[score-matching|Score Matching]] → 基于分数的分子生成
- [[flow-matching|Flow Matching]] → 分子构象生成的流匹配方法
- [[energy-based-models|EBM]] → 基于能量的分子建模

推荐从 **#4 VAE** → **#10 扩散模型** → **#18 Flow Matching** 这条路径开始，与当前分子图生成的研究热点高度吻合。
