# Four Classes of Marketing Agents

The term "Marketing AI Agent" is applied loosely in 2025–2026 to four operationally distinct kinds of system. Conflating them produces bad investment theses and bad product theses. This essay separates them into four **categorical classes** — not a linear hierarchy of Tier 1/2/3/4 — and explains where each makes money, what technology it actually runs on, and where LLM reasoning has structural leverage.

## Why categorical, not tiered

An earlier version of this analysis used a "Tier 1 / Tier 2 / Tier 3 / Tier 4" structure. Numbered tiers imply a linear hierarchy — Tier 1 is bigger or more important than Tier 4 — which misrepresents the actual market. The real distinctions among marketing-agent classes are **categorical**: *where the agent operates in the ecosystem*, *who its customer is*, and *what its economic model looks like*. Maturity (incumbent / scaled / PMF / early) is a secondary axis that varies *within* each class.

The four classes below are distinguished primarily by where the agent sits:

| Class | Position | Who pays | Economic model |
|---|---|---|---|
| 1 — Platform-Owned | Inside an ad surface that owns supply | Advertiser (via ad spend) | Margin on inventory; automation value captured by platform |
| 2 — Independent | Outside any single surface, operating across them | Advertiser | SaaS or share of spend |
| 3 — Conversational | In the post-click conversation | End-business (CX / sales) | Per-seat or per-resolution SaaS |
| 4 — Agent-Mediated | In a new AI-buying-agent surface | Advertiser (frontier) | Speculative |

## Class 1 — Platform-Owned Automation

Autonomous bidding, creative selection, audience expansion, and pacing built into ad surfaces that own (or aggregate) their own supply. The agent ships as part of the buying interface; advertisers do not deploy it as a separate product. Built on traditional ML (deep CTR/CVR models, RL bidders, multi-armed bandits); LLMs are limited to creative generation.

Two sub-types are worth distinguishing because their economic moats differ.

**1a — Walled-Garden Platforms (own end-user attention)**

- Google Performance Max / Smart Bidding
- Meta Advantage+
- Amazon Sponsored / DSP Automated Bidding
- TikTok Smart+

**1b — Aggregator-Network Platforms (aggregate third-party supply)**

- AppLovin (AXON 2.0) — aggregates mobile-app inventory
- Mobvista / Mintegral — same pattern, HK-listed, strong in Chinese outbound
- Tencent Ads — autonomous ranking and bidding inside Tencent's superapp surface
- Alibaba Mama — the same inside Alibaba's e-commerce surface
- Criteo — historically a retargeting network; structurally similar
- The Trade Desk — borderline; pure matcher without owned supply, but operates with the same autonomous-buying-surface logic

The distinction matters: walled gardens own user attention end-to-end, so the value of the automation accrues to the platform; aggregator networks must split value with third-party publishers, which limits pricing power but extends reach.

Class 1 manages the majority of global digital ad spend. The first question any external agent product must answer is *what does it do that Class 1 does not already do inside the buying surface*.

## Class 2 — Independent Cross-Surface Agents

External agent products sold to brands and agencies, operating across multiple Class 1 surfaces (Google, Meta, TikTok, retail media, programmatic) without owning supply. Tech substrate varies — scaled players are typically hybrid (traditional ML for optimization + LLM for creative); early players are typically LLM-native.

**Scaled (disclosed traction):**

- Albert.ai — one of the earliest autonomous ad agents (originally Adgorithms). Cross-surface management across Google, Meta, YouTube. Disclosed case: Harley-Davidson, 5× traffic, 2,930% monthly lead lift.
- Ryze AI — $500M+ ad spend managed across 2,000+ marketers in 23 countries; reported 3.8× ROAS within 6 weeks.
- Jellyfish — agency that replaced parts of human media-buying with AI. M&S case: 80% faster content delivery, 30% cost reduction.

**Product-market fit, not yet scaled:**

- Muze AI — YC-backed; agency-replacement positioning for Shopify SMBs; 85–90% autonomous; under 2-minute creative generation.

**Early, unproven:**

- Uplane (YC 2026) — profit-aware agency replacement; connects to CRM and ERP to optimize on profit, not clicks.
- Absurd (YC 2026) — full-stack AI video advertising. Kalshi's "Election Day" spot exceeded a million views.

The hybrid pattern (traditional ML core + LLM creative) is currently the winning configuration at scale, which constrains the LLM-native thesis to specific leverage points discussed below.

## Class 3 — Conversational & Service Agents

LLM-native agents operating in the post-click conversation: customer support, sales conversations, retention dialogue. Structurally different from Classes 1 and 2 because they do not optimize impressions — they optimize conversation turns and resolution outcomes. This is the class where LLM reasoning is the core product, not a peripheral feature.

**Scaled:**

- Sierra — $100M ARR within 7 quarters of founding; co-founded by Bret Taylor (ex-Salesforce CEO). The clearest existing proof that a marketing-adjacent agent business can scale through LLM reasoning alone.

**Product-market fit, scaling:**

- Decagon — AI agents for customer support; significant fintech and consumer-brand traction.
- Cresta — real-time agent assist plus autonomous sales/support agents.
- Ada — customer service automation; an early LLM-native pivot in the category.
- Parloa — European conversational AI for contact centers.

Economics resemble enterprise SaaS (per-seat, per-resolution) rather than ad take-rate.

## Class 4 — Agent-Mediated Discovery (Frontier)

The newest and most speculative class. Whereas Classes 1–3 all ultimately serve human end-users, Class 4 targets the AI agents that increasingly mediate human purchase decisions. ChatGPT, Claude, Perplexity, and vertical buying agents are becoming the audience.

- sitefire — *Agent SEO*: making products legible and recommendable to AI agents.
- Lapis — ad placement inside ChatGPT (cross-listed from Class 2 because it pioneers a new surface).

No disclosed scale exists yet. The thesis is structural: as AI agents intermediate more commerce decisions, the entire SEO/SEM stack must be rewritten. Class 4 is what comes next.

## The axes that distinguish the four classes

| Axis | Class 1 | Class 2 | Class 3 | Class 4 |
|---|---|---|---|---|
| Where the agent operates | Inside an owned ad surface | Across surfaces, owns none | In conversation, post-click | In new AI-mediated surfaces |
| Customer | Advertiser | Advertiser | End-business (CX / sales) | Advertiser (early) |
| Tech substrate | Traditional ML | Hybrid (ML + LLM) | LLM-native | LLM-native |
| Economics | Inventory margin | SaaS / % of spend | Enterprise SaaS | TBD |
| Is LLM reasoning core? | No | No | Yes | Yes |

Maturity is a secondary axis *within* each class — incumbent, scaled, PMF, early — not a separate class.

## Where LLM agents actually have leverage

The dominant Class 1 winners and most Class 2 winners are built on traditional ML, with LLMs limited to creative generation. The optimization loop they run is high-frequency, low-latency, and data-dense, which rewards classical ML over LLM reasoning. None of the major agent businesses to date are built primarily on Claude Code or pure Claude API.

LLM reasoning is structurally advantaged in three places:

1. **Strategy layer** — channel mix, market-entry decisions, brand positioning, budget allocation across portfolios. Business-context reasoning rather than per-impression optimization. Class 2 players targeting this layer (Uplane is the clearest example) have a defensible thesis.
2. **End-to-end creative chain** — market insight → creative strategy → copy/visual/video → A/B reading → iterative refinement, run coherently as a single loop. This is where Class 2 hybrids hold their position.
3. **Agent-to-Agent marketing** — Class 4 in its entirety. As AI agents intermediate more buying decisions, the SEO/SEM stack must be rewritten. The category is largely empty and LLM understanding is the core weapon.

## Why Class 1b is the most profitable corner

Class 1b (aggregator-network platforms — AppLovin, Mintegral, Tencent Ads, Alibaba Mama, Criteo) is structurally the most profitable position in this taxonomy, for three reasons:

1. **Take-rate economics.** They earn a percentage of every ad dollar flowing through their pipes. Volume × take-rate scales with the entire ad market, not with per-customer SaaS pricing.
2. **Co-located algorithm and data.** Both the matching algorithm and the first-party programmatic data live inside the same company. Class 2 cannot replicate this — it must integrate with Class 1 surfaces from the outside and bring its own data.
3. **Two-sided network effects.** More publishers attract more advertisers attract more publishers — the same structural moat as Class 1a walled gardens, in a different supply form.

This is why companies like AppLovin and Mobvista — companies that rarely appear in agent-narrative coverage — are some of the most profitable AI-driven businesses in marketing. They are AI-native by every reasonable functional definition. They simply do not market themselves as agents.

## The Chinese ad-tech ecosystem

The Chinese mobile-internet ad market produced an unusually strong Class 1b. Mobvista (with Mintegral) is a global Class 1b player. Tencent Ads is Class 1a inside the Tencent superapp surface. Alibaba Mama is Class 1a inside Alibaba's e-commerce surface. ByteDance's ad stack is the same pattern at TikTok/Douyin scale. Pinduoduo's ad system follows the same logic.

Domestic Class 2 (independent agent products sold to brands) is comparatively thin, because the Class 1 surfaces are so dominant that brands prefer to operate inside them rather than buy external automation. This is the inverse of the US picture, where Class 1a and 1b are more fragmented and Class 2 has more room. "Marketing AI agent" narratives — which are largely Class 2/3 narratives — travel awkwardly across the Pacific for this reason.

## Synthesis

The four classes are not in a hierarchy. They are four different positions in the marketing ecosystem, with different customers, economics, technologies, and competitive dynamics. The right question for a builder is not *which tier do I belong to*; it is *which class am I building in, and what does that class's economic structure imply about my moat and my ceiling*.

The interesting convergence frontier is the point where Class 3 or Class 4 LLM-native agents gain access to first-party data and start operating with Class 1-level autonomy. That convergence has not yet happened. When it does, the taxonomy will need a fifth class.

---

*Original analysis for [awesome-martech-ai](https://github.com/leoncuhk/awesome-martech-ai). Companion to [`five-layers-cognitive-cycle.md`](five-layers-cognitive-cycle.md). Comments and corrections welcome via PR.*
