# 营销 Agent 的四个类别

*[English version](marketing-agent-classes.md)*

"营销 AI Agent" 这个词在 2025–2026 年被用来指四类**运作方式截然不同**的系统。把它们混在一起会同时产出不可靠的投资判断和产品判断。本文把它们拆成四个**分类（categorical）**——按 agent 在生态中的位置、客户是谁、经济模型是什么来划分——并解释每一类挣的是什么钱、底层跑的是什么技术、LLM 推理在哪些位置有结构性优势。

## 四类如何区分

四个类别是**分类的（categorical），不是有序的（ordinal）**。主要按"agent 在营销生态中坐在哪里"划分。**成熟度（incumbent / scaled / PMF / early）是类内的次级轴**，不是另一种类别。

| Class | 位置 | 谁付钱 | 经济模型 |
|---|---|---|---|
| 1 — Platform-Owned | 嵌在自有流量的广告平面内部 | 广告主（通过广告支出） | 流量自带的利润空间；自动化价值被平台捕获 |
| 2 — Independent | 漂在所有广告平面之上，跨平面操作 | 广告主 | SaaS 或流水抽成 |
| 3 — Conversational | 在 click 之后的对话层 | 业务主（CX / 销售团队） | per-seat 或 per-resolution SaaS |
| 4 — Agent-Mediated | 在新出现的 AI 中介购买层 | 广告主（早期） | 投机性，尚未稳定 |

## Class 1 — Platform-Owned Automation

自主出价、创意选择、受众扩展、节奏控制——这些都内嵌在那些**自己拥有（或聚合了）流量供给的广告平面**里。Agent 作为购买界面的一部分出货，广告主不会把它当成独立产品来部署。底层跑的是**传统 ML**（深度 CTR/CVR 模型、RL 出价器、多臂老虎机），LLM 仅参与创意生成。

这一类内部有两个子型，因为它们的护城河差异很大。

**Class 1a — Walled-Garden 平台**（拥有终端用户注意力）

- Google Performance Max / Smart Bidding
- Meta Advantage+
- Amazon Sponsored / DSP 自动出价
- TikTok Smart+

**Class 1b — 聚合网络型平台**（聚合第三方供给）

- AppLovin（AXON 2.0）—— 聚合移动应用流量
- Moloco —— ML 驱动的广告平台，深耕移动 UA 与零售媒体 DSP；在其细分领域技术声誉与 AppLovin 同档
- Mobvista / Mintegral —— 同样模式，港股上市，强在中国出海移动
- 腾讯广告 —— 嵌在 Tencent 超级 app 矩阵内部的自主排序与出价
- 阿里妈妈 —— 阿里电商平面里的同一模式
- Criteo —— 早期 retargeting 网络，结构上类似
- The Trade Desk —— 边界案例，纯撮合不拥有 supply，但运行逻辑等同于自主购买平面

1a 与 1b 的区分关键在经济结构：**walled garden 端到端拥有用户注意力**，所以自动化创造的价值被平台直接捕获；**聚合网络必须与第三方 publisher 分账**，这压缩了定价权但扩展了覆盖。

Class 1 管理全球数字广告支出的大部分。任何外部 agent 产品的第一个问题是：*你比 Class 1 在购买平面内部自带的自动化强在哪里*。

## Class 2 — Independent Cross-Surface Agents

外部 agent 产品，卖给品牌和代理商；跨多个 Class 1 平面（Google、Meta、TikTok、零售媒体、programmatic）操作但**不拥有任何平面的 supply**。技术底座差异大：**已规模化的玩家通常是混合架构**（传统 ML 做优化 + LLM 做创意）；**早期玩家通常是 LLM 原生**。

**已规模化（有公开 traction 数据）：**

- Albert.ai —— 最早一批自主广告 agent 之一（前身 Adgorithms）。跨 Google / Meta / YouTube 管理。公开案例：Harley-Davidson，流量 5×，月度线索 +2,930%。
- Ryze AI —— 跨 23 国 2,000+ 营销人员，管理 $500M+ 广告支出。公开数据：6 周内达到 3.8× ROAS。
- Jellyfish —— 用 AI bot 替代部分人工媒介团队。M&S 案例：内容交付速度 +80%、成本 -30%。

**有 PMF，尚未规模化：**

- Muze AI —— YC 背景，定位替代月费 $10K–$15K 的代理。85–90% 自主，创意生成 < 2 分钟。已上 Shopify App Store 且有付费客户。

**早期，未验证：**

- Uplane（YC 2026）—— 以"利润"而非"点击"为优化目标的代理替代品；接入 CRM/ERP 学习真正驱动盈利的因子。
- Absurd（YC 2026）—— 全链路 AI 视频广告。Kalshi "Election Day" 单条破百万播放。

当前胜出的是**混合架构**（传统 ML 做核心 + LLM 做创意），这把"纯 LLM 原生 agent"的论点压缩到下文讨论的几个特定杠杆点上。

## Class 3 — Conversational & Service Agents

LLM 原生 agent，运行在**点击之后的对话层**：客服、销售对话、留存沟通。和 Class 1/2 结构性不同——它们**优化的不是 impression，而是对话回合和解决率**。**这是 LLM 推理本身就是核心产品的一类**，不是边缘功能。经济模型像企业 SaaS（per-seat、per-resolution），不像广告抽成。

**已规模化：**

- Sierra —— 创立 7 个季度内达到 $100M ARR；联合创始人 Bret Taylor（前 Salesforce CEO）。

**PMF，正在扩张：**

- Decagon —— 客服 agent；金融科技和消费品牌客户有牵引力。
- Intercom Fin —— Intercom 的自主客服 agent，2023 年起在 Intercom 客户群中部署。
- Cresta —— 实时坐席辅助 + 自主销售/客服 agent。
- Ada —— 客服自动化；这一品类里较早的 LLM 原生转型。
- Cognigy —— 企业级对话 AI 平台，欧洲呼叫中心市场地位强。
- Parloa —— 欧洲呼叫中心对话 AI。

## Class 4 — Agent-Mediated Discovery（前沿）

最新也最投机的一类。Class 1–3 最终都服务**人类终端用户**，而 Class 4 直接面对**那些越来越多代替人做购买决策的 AI agent**——ChatGPT、Claude、Perplexity、垂直购买助理正在成为新的"受众"。这一类内部已经分化出两个子型：

**4a — GEO / AEO 平台**（Generative / Answer Engine Optimization——测量并提升品牌在 LLM 回答中的可见度）：

- Profound —— 跨 ChatGPT、Perplexity、Gemini、Google AI Overviews 跟踪品牌出现与推荐情况；业内公认的品类定义级产品。
- Daydream —— 让品牌目录和内容对 AI 购买 agent 可发现可推荐。
- Scrunch AI —— 分析品牌在主流 answer engine LLM 回答中的呈现状况。

**4b — AI 渠道内广告投放**（在 AI agent surface 上买位）：

- Lapis —— ChatGPT 内的原生广告投放，开拓全新的购买 surface。
- sitefire —— *Agent SEO*：在 schema/feed 层让产品对 AI agent 可读可推荐。

目前没有任何 Class 4 玩家公开规模化数据。论点是结构性的：**当 AI agent 中介越来越多的商业决策，整套 SEO/SEM 逻辑必须重写**。Class 4 就是"下一步"。

## 区分四类的几根轴

| 轴 | Class 1 | Class 2 | Class 3 | Class 4 |
|---|---|---|---|---|
| Agent 操作位置 | 自有广告平面内 | 跨平面，不拥有 | 对话中，post-click | 新的 AI 中介 surface |
| 客户 | 广告主 | 广告主 | 业务主（CX / 销售） | 广告主（早期） |
| 技术底座 | 传统 ML | 混合（ML + LLM） | LLM 原生 | LLM 原生 |
| 经济模型 | 流量利润 | SaaS / 抽成 | 企业 SaaS | 未定 |
| LLM 推理是核心吗 | 否 | 否 | 是 | 是 |

**成熟度是类内的次级轴**——incumbent / scaled / PMF / early——不是新的一类。

## LLM agent 真正的杠杆点在哪

主导的 Class 1 玩家和大部分 Class 2 玩家都跑在传统 ML 上，LLM 限于创意生成。他们优化的循环是**高频、低延迟、数据密集的**，这种回路结构上奖励经典 ML、不奖励 LLM 深度推理。**至今没有任何头部 agent 业务主要构建在 Claude Code 或纯 Claude API 上。**

LLM 推理在三个位置有结构性优势：

1. **策略层**——渠道组合、市场进入决策、品牌定位、跨组合预算分配。这些需要的是商业语境推理，不是逐 impression 优化。聚焦这一层的 Class 2 玩家（Uplane 是最清晰的例子）有可防御的论点。
2. **端到端创意链**——market insight → 创意策略 → 文案/视觉/视频 → A/B 解读 → 迭代——把全链路作为单一闭环跑，而非孤立的生成环节。这是 Class 2 混合架构的护城河所在。
3. **Agent-to-Agent 营销**——整个 Class 4。当 AI agent 中介越来越多购买决策，SEO/SEM 整套逻辑要重写。这个品类几乎全空，LLM 的理解能力是核心武器。

## 为什么 Class 1b 是利润最高的那一格

Class 1b（聚合网络型平台——AppLovin、Mintegral、腾讯广告、阿里妈妈、Criteo）在这个分类里**结构上最赚钱**，三个原因：

1. **流水抽成经济**——它们对穿过自己管道的每一块广告费抽成。**Volume × take-rate** 随整个广告市场线性放大，而不是 per-customer SaaS 定价那种 ARPU 模型。
2. **算法与数据同址**——匹配算法和 first-party programmatic 数据都在同一家公司内部。Class 2 复制不了这一点——它必须从外部接入 Class 1 平面，还要自己带数据。
3. **双边网络效应**——更多 publisher 吸引更多广告主，再吸引更多 publisher——和 Class 1a walled garden 同构的护城河，只是 supply 形态不同。

这就是为什么 AppLovin、Mobvista 这种**几乎不出现在 agent 叙事里**的公司，反而是营销领域里最赚钱的 AI-driven 业务之一。从任何功能性定义上看它们都是 AI 原生。它们只是不把自己包装成 "agent"。

## 中国广告科技生态的视角

中国移动互联网广告市场孕育了非常强势的 Class 1b。Mobvista（Mintegral）是全球性的 Class 1b 玩家。腾讯广告是 Tencent 超级 app 平面里的 Class 1a。阿里妈妈是阿里电商平面里的 Class 1a。字节的广告栈在 TikTok/抖音规模上是同样模式。拼多多的广告系统同理。

**国内的 Class 2（独立的 agent 产品卖给品牌）相对薄弱**，因为 Class 1 平面太强，品牌更倾向于直接在平面内部操作，而非购买外部自动化层。这正好和美国市场倒过来——美国 Class 1a/1b 更碎片化，Class 2 因此有更多空间。"Marketing AI agent" 的叙事——主要是 Class 2/3 的叙事——在跨太平洋传播时不舒服，原因就在这里。

## 综合

四个类别**不是层级关系**。它们是营销生态中的四个不同位置，各自有不同的客户、经济模型、技术、竞争动态。**对建造者来说，正确的问题不是"我属于第几层"，而是"我在哪一类里建造，这一类的经济结构对我的护城河和天花板意味着什么"**。

最值得关注的融合前沿是：Class 3 或 Class 4 的 LLM 原生 agent **获得 first-party 数据访问权，开始以 Class 1 级别的自主性运行**。这种融合尚未发生。
