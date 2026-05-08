# Wiki Schema

## Domain
基于深度学习的分子图生成方法研究（Molecular Graph Generation via Deep Learning）

博士研究方向，涵盖分子图表示学习、生成模型（VAE/GAN/扩散模型/自回归）、
药物分子设计、逆合成分析、分子性质预测等相关内容。

## Conventions
- File names: lowercase, hyphens, no spaces（如 `molecular-diffusion-models.md`）
- Every wiki page starts with YAML frontmatter（见下方模板）
- Use `[[wikilinks]]` to link between pages（每页至少 2 个出链）
- 更新页面时，务必更新 `updated` 日期
- 每个新页面必须添加到 `index.md` 对应的分区
- 每次操作必须追加到 `log.md`
- **溯源标记：** 在综合 3+ 来源的页面上，使用 `^[raw/articles/source-file.md]` 标注段落来源，方便追溯
- **修改 raw/ 下的文件时** 需要重新计算 sha256 并更新 frontmatter
- **中英混用：** 页面内容建议英文术语保留原文（如 VAE、GNN），解释部分用中文，方便日后国际交流

## Frontmatter
```yaml
---
title: 页面标题（中文）
title_en: Page Title in English
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary | paper-note
tags: [from taxonomy below]
sources: [raw/papers/paper-name.md]
confidence: high | medium | low
contested: true
contradictions: [other-page-slug]
---
```

`confidence` 和 `contested` 可选。`confidence: low` 的页面会在 lint 报告中标记出来，
防止弱证据被固化。

### raw/ Frontmatter
```yaml
---
source_url: https://arxiv.org/abs/xxxx.xxxxx
ingested: YYYY-MM-DD
sha256: <hex digest of body>
---
```

`sha256` 用于后续重新摄入时检测内容是否变更。

## Tag Taxonomy

### Models & Architectures
- `model`: 具体模型名称
- `vae`: 变分自编码器相关
- `vqvae`: VQ-VAE / 向量量化
- `gan`: 生成对抗网络
- `diffusion`: 扩散模型
- `autoregressive`: 自回归模型
- `flow`: 归一化流
- `transformer`: Transformer 架构
- `gnn`: 图神经网络
- `rl`: 强化学习

### Tasks & Methods
- `molecule-generation`: 分子生成
- `language-modeling`: 语言建模
- `de-novo`: 从头药物设计
- `inverse-synthesis`: 逆合成分析
- `property-prediction`: 性质预测
- `conformation-generation`: 构象生成
- `optimization`: 优化方法
- `representation-learning`: 表示学习

### Data & Evaluation
- `dataset`: 数据集（QM9、ZINC、ChEMBL、PubChem 等）
- `benchmark`: 基准测试
- `metric`: 评价指标
- `molecular-dynamics`: 分子动力学

### People & Orgs
- `person`: 研究者
- `lab`: 实验室/课题组
- `conference`: 会议（NeurIPS、ICML、ICLR、AAAI 等）
- `journal`: 期刊

### Meta
- `comparison`: 对比分析
- `agi`: 通用人工智能 / AGI 理论
- `cognitive-science`: 认知科学
- `review`: 综述
- `timeline`: 时间线
- `open-question`: 开放问题
- `tool`: 工具/代码库

Rule: 每个新标签必须先加到此处才能使用，防止标签泛滥。

## Page Thresholds
- **创建页面：** 某个实体/概念出现在 2+ 来源中，或是 1 个来源的核心内容
- **追加到已有页面：** 当来源提到已有页面覆盖的内容
- **不要创建页面：** 仅仅顺带一提、次要细节、超出领域范围
- **拆分页面：** 超过 ~200 行时拆分为子主题，并互相链接
- **归档页面：** 内容完全被取代时，移到 `_archive/`，从 index 中移除

## Entity Pages
一个页面 = 一个实体（模型/人物/数据集/工具等）。包含：
- 概述 / 是什么
- 关键事实和日期
- 与其他实体的关系（[[wikilinks]]）
- 来源引用

## Concept Pages
一个页面 = 一个概念/方法。包含：
- 定义/解释
- 当前认知状态
- 开放问题或争议
- 相关概念（[[wikilinks]]）

## Comparison Pages
并排对比分析。包含：
- 对比什么及原因
- 对比维度（优先用表格）
- 结论或综合判断
- 来源

## Update Policy
当新信息与现有内容冲突时：
1. 比较日期——新来源通常优于旧来源
2. 如果确实矛盾，标注两种说法及其日期和来源
3. 在 frontmatter 标记矛盾：`contradictions: [page-name]`
4. 在 lint 报告中标记供用户审阅
