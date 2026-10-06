# 文献错题本

记录日期：2026-10-06。

这些条目来自准备阶段的文献检索，用于提醒哪些假设、比较方式和失败边界值得检查。它们没有决定实验路线，也没有成为本项目已经取得的研究结果。

**当前所有条目均未在本项目中独立复现。** 下表的提醒来自作者报告、理论条件或官方实验检查项；检查建议属于本项目的候选问题。

## 记录纪律

- 分开标记作者报告的问题、本项目独立观察的问题与尚未验证的怀疑。
- 保留来源、版本、任务、假设、判据和适用范围；不同任务的指标与结论不能直接迁移。
- 文献存在不取消研究，也不授予首创性；采用已有方法、代码、数据或推导时引用对应来源。
- 某个结论被本项目反例击穿时，记录反例和条件；不能据此自动推断造假、作者意图或整个领域失效。
- 不按论文中的结论或数值制造预期结果。是否需要复现，由当前研究问题决定。

## 候选提醒

| 来源 | 值得检查的条件或问题 | 本项目候选检查 |
| --- | --- | --- |
| [On the Difficulty of Evaluating Baselines: A Study on Recommender Systems](https://arxiv.org/abs/1905.01395)，2019 | 作者在评分预测基准中报告，基线配置显著影响比较结果。 | 记录调参范围与预算；核对比较对象是否发挥了预期能力。 |
| [A Critical Study on Data Leakage in Recommender System Offline Evaluation](https://arxiv.org/html/2010.11060v4)，2022 版本 | 按用户留最后一次交互，仍可能通过其他用户的未来数据引入时间泄漏。 | 核对预测时刻可用的行为、特征与候选对象；按任务定义数据切分。 |
| [On Sampled Metrics for Item Recommendation](https://research.google/pubs/on-sampled-metrics-for-item-recommendation/)，2020 | 作者研究了抽样排名指标与全量指标的数值及模型相对排名不一致。 | 小规模下对照全量与抽样评测，改变样本量与抽样策略。 |
| [On Sampling Top-K Recommendation Evaluation](https://arxiv.org/html/2106.10621v1)，2021 arXiv 版本 | 作者讨论抽样 HR@k 与映射后的全量 HR@f(k) 的近似关系；截断位置通常不相同。 | 先核对比较命题、指标与映射条件，再检查何时能保持决策比较。 |
| [An Improved Data Stream Summary: The Count-Min Sketch and its Applications](https://www.cs.ox.ac.uk/people/graham.cormode/pubs/papers/cm-full.pdf)，2005 | 非负频率模型下，点查询的加性误差界以总频率为尺度，并依赖哈希假设。 | 分别检查热门与长尾对象、误差分母和选择边界。 |
| [HyperLogLog in Practice: Algorithmic Engineering of a State of the Art Cardinality Estimation Algorithm](https://stefanheule.com/papers/edbt13-hyperloglog.pdf)，2013 | 作者讨论原始估计的小基数偏差、修正与不同基数区间的表现。 | 覆盖空集、小集合、估计器切换附近与大集合，分别记录偏差和波动。 |
| [The Optimizer's Curse: Skepticism and Postdecision Surprise in Decision Analysis](https://pubsonline.informs.org/doi/abs/10.1287/mnsc.1050.0451)，2006 | 文中分析了按不完美价值估计选优造成的选择后高估，即使候选估计本身无偏。 | 区分观测估计误差与选择过程对误差的放大，检查候选范围。 |
| [Categorizing Variants of Goodhart's Law](https://arxiv.org/abs/1803.04585)，2018 首发 | 作者区分代理指标过度优化的不同失效机制。 | 按当前模型确定失效成因，不把所有异常统称为漂移。 |
| [Scaling Laws for Reward Model Overoptimization](https://proceedings.mlr.press/v202/gao23h.html)，2023 | 作者使用合成金标准奖励与代理奖励，研究不同优化方法下的过度优化行为。 | 明确效用是模拟设定；把优化预算作为变量，允许改善、平台与退化等结果。 |
| [Performative Prediction](https://proceedings.mlr.press/v119/perdomo20a.html)，2020 | 决策部署可以影响未来数据分布；收敛结论依赖声明条件。 | 区分外生变化与行动诱导反馈，核对环境更新规则及稳定性条件。 |
| [Outside the Echo Chamber: Optimizing the Performative Risk](https://proceedings.mlr.press/v139/miller21a.html)，2021 | 作者区分反复重训的稳定点与部署后的风险最优性。 | 分别评价稳定、目标收益和反馈后果，不以收敛自动认定决策有效。 |
| [Feedback Loop and Bias Amplification in Recommender Systems](https://arxiv.org/abs/2007.13019)，2020 | 作者在离线模拟中研究反馈环对流行度偏差、多样性与用户表示的影响。 | 核对用户响应模型和群体条件；不把模拟结果直接推广为全部真实用户行为。 |
| [Dynamic Feedback Loops in Recommender Systems: Analyzing Fairness, Popularity Bias, and User Group Disparities](https://link.springer.com/article/10.1007/s10844-026-01025-y)，2026 | 作者在循环模拟中分别分析准确性、流行度校准、长尾曝光及用户群体差异。 | 同时查看总量与分群指标，核对反馈数据生成是否改变评估含义。 |
| [Surrogate Measures and Consistent Surrogates](https://pmc.ncbi.nlm.nih.gov/articles/PMC4221255/)，2013 | 代理终点悖论讨论代理改善、正相关与干预后最终结局变差可以并存的条件。 | 区分观察相关与干预方向；只吸收统计结构，不借此提出医学结论。 |
| [PROXIMA: A Reliability Scoring Framework for Proxy Metrics in Online Controlled Experiments](https://arxiv.org/abs/2604.14352)，2026 预印本 | 正文综合效应相关、方向准确率与分群脆弱性，检查模拟 A/B 决策中的代理可靠性。 | 核对具体版本、oracle 定义与分群判据；项目页和正文的组成口径差异见核对记录。 |
| [Detecting Proxy Gaming in RL and LLM Alignment via Evaluator Stress Tests](https://aclanthology.org/2026.findings-acl.513/)，Findings of ACL 2026 | 作者用受控扰动与语义有效性审查识别评估器被利用的情况，并报告预警结果。 | 核对扰动是否保持语义、效用标签从何而来，以及预警判据适用范围。 |
| [The Preregistration Revolution](https://psychologicalsciences.unimelb.edu.au/__data/assets/pdf_file/0007/2888098/The-preregistration-revolution.pdf)，2018 | 文中区分探索产生假设与验证假设，并讨论迭代使用二者。 | 保留探索身份；正式验证时形成自己的计划与证据要求。 |
| [NeurIPS 2021 Paper Checklist Guidelines](https://neurips.cc/Conferences/2021/PaperInformation/PaperChecklist) | 官方检查项包括假设、边界、复现材料、参数选择、随机性与计算资源。 | 按当前问题记录必要事实，避免用一轮最优运行代表整体结果。 |

抽样评测的两项研究讨论的比较命题并不完全相同。这里保留两者作为条件核对线索，没有认定它们互相否定。

本轮检索确认存在多个相邻研究方向。关于框架重合、当前名称和 PROXIMA 来源口径的进一步边界，见 [相邻研究核对](related-work-review.md)。

## 方法来源

[VeriTrail 证据反馈工作法](https://github.com/NoctilumeDev/VeriTrail/blob/d794731d2402efe98ff572a38cfcf898c22352d7/docs/working-method.md)提供外层问题选择、内层证据资格、首败保留与状态分离的参照。

其 [M7 配对实验合同](https://github.com/NoctilumeDev/VeriTrail/blob/d794731d2402efe98ff572a38cfcf898c22352d7/docs/11-m7-preregistered-paired-analysis.md)明确不做统计显著性与置信区间；[M8 组合实验合同](https://github.com/NoctilumeDev/VeriTrail/blob/d794731d2402efe98ff572a38cfcf898c22352d7/docs/12-m8-preregistered-batch-matrix.md)的种子用于组合顺序。统计分析、数据生成及模型随机性需要本项目另外定义。
