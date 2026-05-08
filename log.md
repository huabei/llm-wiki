# Wiki Log

> 操作时间线。只追加不改写。
> 格式：`## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete
> 超过 500 条时轮转：重命名为 log-YYYY.md，重新开始。

## [2026-04-28] create | Wiki 初始化
- 创建者：华北（中南大学，博二）
- 方向：基于深度学习的分子图生成
- 结构：SCHEMA.md, index.md, log.md + raw/, entities/, concepts/, comparisons/, queries/
- Git 仓库已初始化

## [2026-04-28] create | Jakub M. Tomczak 实体页 + 博客概念页
- 创建 `entities/jakub-m-tomczak.md` — 作者生平、学术背景、代表著作
- 创建 `concepts/deep-generative-modeling-blog.md` — 博客系列完整目录、特点分析、与分子图生成研究的关联
- 更新 `index.md` — 添加两条新条目
- 双向链接：`[[jakub-m-tomczak]]` ↔ `[[deep-generative-modeling-blog]]`
- 博客中共有 19+ 篇博文，覆盖生成模型的全部主流范式

## [2026-05-04] create | 语言作为 VQVAE 系统概念页（含修正与讨论记录）
- 创建 `concepts/language-as-vqvae.md` — 语言 VQVAE 认知框架
- 核心框架为华北原始想法，标记 `^[原始]` 归属
- 小北的阐释/外推标记 `^[讨论]`，首次整理时对模仿学习的误解已标注修正记录
- 删除强行关联分子生成的内容
- 更新 `SCHEMA.md` — 新增标签：vqvae, language-modeling, agi, cognitive-science
- 更新 `index.md` — 添加 `[[language-as-vqvae]]` 到 Concepts 分区

## [2026-05-05] update | 新增编码-重建对比学习模型框架
- 华北提出模型框架：x → encoder → z → decoder → x' → encoder → z'，z 与 z' 做对比学习
- 原文添加至「原始文本」章节
- 「整理版本」新增「编码-重建对比学习框架」小节，包含生物映射、框架特性、与已有工作的联系、技术挑战
- 更新 `updated` 日期
