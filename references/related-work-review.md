# 相邻研究核对

核对日期：2026-10-06。状态：准备阶段文献核对；没有进行算法实验或独立复现。

## 1. 核对结论的强度

已找到代理优化、决策诱导分布变化、推荐反馈环、代理终点悖论及代理可靠性审查的原始论文或发布页面。

本记录只确认资料存在及其声明的研究范围。论文报告的效果、理论条件和代码行为尚未由本项目独立验证。

本轮是有范围的网页检索，不是系统综述。没有认定“完整统一框架不存在”“该交叉问题无人研究”或“漂移算法具有首创性”。完整问题的相似性还需要比较输入、模型、观测权限、判据、反馈规则和可识别边界。

## 2. 与研究问题的关系

| 相邻线索 | 已核对的原始来源 | 本项目阅读时保留的边界 |
| --- | --- | --- |
| Goodhart 分类 | [Categorizing Variants of Goodhart's Law](https://arxiv.org/abs/1803.04585) | 分类是候选解释工具，不代表所有代理优化均有害。 |
| 奖励模型过度优化 | [Scaling Laws for Reward Model Overoptimization](https://proceedings.mlr.press/v202/gao23h.html) | 使用合成金标准奖励；不能把金标准模型直接等同于现实效用。 |
| 决策改变未来分布 | [Performative Prediction](https://proceedings.mlr.press/v119/perdomo20a.html) | 部署诱导分布变化与目标定义改变需分别记录；收敛条件不能省略。 |
| 稳定点与风险最优性 | [Outside the Echo Chamber](https://proceedings.mlr.press/v139/miller21a.html) | 稳定、最优和目标有效性需要分别评价。 |
| 推荐反馈与偏差放大 | [2020 离线模拟研究](https://arxiv.org/abs/2007.13019)、[2026 动态反馈研究](https://link.springer.com/article/10.1007/s10844-026-01025-y) | 用户响应与新数据生成规则是模型前提；群体结论不从平均指标自动取得。 |
| 代理终点悖论 | [Surrogate Measures and Consistent Surrogates](https://pmc.ncbi.nlm.nih.gov/articles/PMC4221255/) | 观察相关与干预效果之间需要因果条件；这里只作为跨领域统计线索。 |
| A/B 代理可靠性审查 | [PROXIMA arXiv v1 正文](https://arxiv.org/html/2604.14352v1) | 它检查定义的模拟决策和 oracle；具体组成与项目介绍须分别核对。 |
| 评估器被利用与预警 | [Evaluator Stress Test](https://aclanthology.org/2026.findings-acl.513/) | 原始发布页列为 Findings of ACL 2026；预警效果是作者报告，不能自动推广。 |

## 3. PROXIMA 的来源口径差异

[作者项目页](https://avinash-amudala.com/projects/proxima)将组成描述为方向一致性、秩保持与分群脆弱性；[arXiv 摘要页](https://arxiv.org/abs/2604.14352)和 [v1 正文](https://arxiv.org/html/2604.14352v1)列为归一化效应相关、方向准确率和分群脆弱率。

v1 正文第 3.3 节的相关项采用实验效应的 Pearson 相关。这里保留两种表述及来源，没有把它们合成为同一个已经核定的公式，也没有解释差异的原因。

此外，v1 正文第 5.4 节表 6 与正文说明：在报告的两个数据集上，PROXIMA 和 correlation-only 选择同一顶级代理，取得相同决策胜率。作者所述的其他诊断优势，需与这个胜率事实分开理解。

因此，项目介绍中的秩保持表述、综合分数的诊断作用以及决策质量改善，不可以直接互相替代。后续只有当前研究问题需要时，才核对 PDF、代码与具体实验。

## 4. 名称记录

已找到两个名称相近而机制不同的工作：

- [DRIFT: Learning from Abundant User Dissatisfaction in Real-World Preference Learning](https://arxiv.org/abs/2510.02341)，使用用户不满意信号进行偏好训练。
- [Drift: Decoding-time Personalized Alignments with Implicit User Preferences](https://arxiv.org/abs/2502.14289)，研究解码时个性化对齐。

这说明名称存在重合，不构成对本项目名称的唯一性核查或机制等价证明。

本项目已商定名称继续为“漂移算法 / Drift Algorithm”。公开首次引用时同时写出 AlgorithmResearchLab 与研究定义；不借用其他工作的大写缩写展开，不因文献命名自动更名。

## 5. 使用方式

这些资料进入错题本，提供值得核对的条件、反例与已有贡献。路线仍从具体算法的单体、条件变化与耦合观察中推进。

本记录没有启动首个实验、制定固定功能清单、承诺检测能力或要求复刻任一论文流程。
