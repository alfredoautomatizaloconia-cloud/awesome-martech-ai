# Three Tiers of Marketing Agents — and the Fourth Player Most Frameworks Miss

> *A working framework for the 2025–2026 marketing-agent landscape — followed by the player class the framework leaves out, and why ignoring it gives a misleading picture of where the money actually is.*

<div align="center">
<img src="../assets/three-tiers-marketing-agents.jpg" alt="Three Tiers of Marketing Agents" width="780">
</div>

## 1. The problem this framework solves

"Marketing AI Agent" has become a catch-all term used across at least four very different species:

- The automation already running inside Google Ads and Meta Ads.
- Standalone agent products sold to brands and agencies.
- The programmatic infrastructure that brokers ads between publishers and advertisers.
- A new class of LLM-native agents from the YC-2026 cohort.

Conflating them produces bad investment theses and bad product theses. The three-tier framework below separates them. Section 6 then adds the *fourth* class — the programmatic infrastructure layer — which is the most profitable of all and the one most "marketing agent" coverage silently omits.

## 2. Tier 1 — Platform-Native AI (the incumbents who already ate the market)

These do not call themselves agents, but functionally they are: autonomous bidding, automatic creative assembly, audience discovery, budget pacing, surface allocation. They already manage the majority of global digital ad spend.

- **Google Performance Max / Smart Bidding** — Cross-channel automated campaign type; the de facto agent inside Google Ads.
- **Meta Advantage+** — Automated audience, creative, and placement decisions across Meta surfaces.
- **Amazon Sponsored Brands / DSP Automated Bidding** — Amazon's equivalent on retail media.
- **TikTok Smart+** — TikTok's answer to PMax/Advantage+.

For any agent startup, the first question is unavoidable: *what do you do that Google and Meta do not already do inside the buying surface itself?* This is the ceiling of Tier 2.

## 3. Tier 2 — Vertical Agents with Real Traction

The shortlist of agent products with disclosed scale, customers, or revenue.

- **Albert.ai** — The longest-running autonomous ad agent. Cross-channel autonomous management across Google, Meta, YouTube. Harley-Davidson reported a 5× traffic increase and 2,930% monthly lead lift after deployment — one of the few brand-scale validated cases.
- **Ryze AI** — Manages over $500M in ad spend across 2,000+ marketers in 23 countries, covering Google, Meta, Microsoft, LinkedIn, TikTok, Pinterest, and Amazon PPC. Customers report 3.8× ROAS within 6 weeks. The hardest disclosed scale numbers in this tier.
- **Muze AI** — YC-backed; positioned to replace $10K–$15K/month agency retainers. 85–90% autonomous; video and image generation in under 2 minutes; auto-detects creative fatigue. On the Shopify App Store with paying customers, still early.
- **Jellyfish** — Agency that replaced parts of its human media-buying team with AI bots. 65% reduction in campaign launch time. Drove 80% faster content delivery and 30% cost reduction for M&S.
- **Sierra** — Conversational service agents; $100M ARR in 7 quarters after founding by ex-Salesforce CEO Bret Taylor. The clearest existing proof that a vertical agent business can scale, and the cleanest example of an agent that is *not* an ad agent.

## 4. Tier 3 — YC 2026 Cohort: Interesting Angles, Unproven Outcomes

- **Uplane** — Replaces marketing agencies; generates hundreds of ad creatives with matching landing pages, connects to CRM and ERP to learn what drives *profit*, not just clicks.
- **Lapis** — Native ad placement inside ChatGPT (a new channel), generating creative from existing brand assets across ChatGPT, Meta, and Google.
- **sitefire** — *Agent SEO*: helps brands get discovered and recommended *by* AI agents. A new paradigm — buying placement in front of AI agents, not humans.
- **Absurd** — Full-stack AI video advertising. Kalshi's "Election Day" spot exceeded a million views.

## 5. Where LLM Agents actually have leverage

Notably, none of these are built on Claude Code or pure Claude API. The reason is structural: ad optimization is a high-frequency, low-latency, data-dense loop — real-time bidding data → multivariate testing → conversion attribution → next-iteration policy — and that loop rewards traditional ML (gradient boosting, multi-armed bandits, RL) far more than deep LLM reasoning. Existing winners are hybrid: traditional AdTech + ML + LLM only for creative generation.

But LLMs do have three high-leverage points where reasoning is the bottleneck:

1. **Strategy layer, not execution layer.** Bid optimization belongs to Google/Meta. But *should we enter this market, how should the brand be positioned, how should budget split across channels* — these require business-context reasoning, which is exactly where LLMs beat traditional ML.
2. **End-to-end creative chain.** Most tools generate ad creatives. The real pain is the full chain: market insight → creative strategy → copy/visual/video → A/B reading → iterative refinement. LLMs are the only architecture that can run this loop coherently.
3. **Agent-to-Agent marketing.** As consumers route purchase decisions through ChatGPT, Claude, and vertical buying agents, the entire SEO/SEM logic must be rewritten. Making your product legible and recommendable *to AI agents* is a new, largely empty category — and here, LLM understanding is the core weapon.

**Bottom line for Tiers 1–3:** Digital advertising's agent transition is real, but most winners today are not LLM-native. The pure LLM-Agent opportunity is not in optimizing execution — it is in **strategy reasoning** and **Agent-to-Agent marketing**, the two high grounds still unoccupied.

---

## 6. The Fourth Player — Programmatic Infrastructure (the layer most frameworks miss)

The three-tier framework asks: *which agent product should a brand buy?* It is a **buyer-side product map**.

It deliberately leaves out a parallel rail that is at least as economically significant: the **programmatic ad infrastructure**. These companies are not products you "deploy" as a brand — they are the pipes through which ad inventory flows from publisher to advertiser. They are also, increasingly, **autonomous ML systems** at platform scale. Many of them are spectacularly profitable.

The honest version of the framework is two-dimensional:

```
                                     ┌──────────────────────────────────────────┐
                                     │       WHO IS THE CUSTOMER?               │
                                     │                                          │
                                     │   Brand / Advertiser   Publisher /       │
                                     │       Marketer            Network        │
              ┌──────────────────────┼──────────────────────────────────────────┤
              │ Incumbent platform   │  Tier 1:                Tier 4:          │
              │ (autonomous ML       │  Google PMax            AppLovin AXON    │
              │  inside the buying   │  Meta Advantage+        Mobvista /       │
              │  or selling surface) │  Amazon DSP auto        Mintegral        │
              │                      │  TikTok Smart+          Tencent Ads      │
              │                      │                          Criteo · TTD     │
              ├──────────────────────┼──────────────────────────────────────────┤
              │ Newer / external     │  Tier 2:                (rare — mostly   │
              │ agent product        │  Albert · Ryze          consumed by      │
              │                      │  Muze · Jellyfish        Tier 4 players) │
              │                      │  Sierra                                  │
              │ ┌─ + LLM-native bet ─┤  Tier 3:                                 │
              │ │                    │  Uplane · Lapis                          │
              │ │                    │  sitefire · Absurd                       │
              └─┴────────────────────┴──────────────────────────────────────────┘
```

**Tier 4 — Programmatic Infrastructure** sits inside the supply chain, not on top of it. Examples by market:

- **AppLovin (AXON 2.0)** — The single clearest example. AppLovin's AXON is an autonomous ML targeting and bidding system serving mobile app advertisers across its owned-and-operated ad network. After AXON 2.0 shipped in 2023, AppLovin's revenue and stock both roughly 10×'d — not because of any LLM, but because a *better autonomous ML model in the buying-surface chokepoint* changes the entire economics of mobile UA.
- **Mobvista / Mintegral** — Hong Kong-listed; one of the largest programmatic ad networks serving Chinese mobile-app outbound, plus global SSP/DSP infrastructure. Operates the same ML-driven targeting/bidding role as AppLovin in adjacent markets.
- **Tencent Ads (腾讯广告)** — Operates the ad surface across WeChat, Tencent Video, news, and games — one of the largest ad businesses in the Chinese-language internet. Internally an extremely sophisticated ranking/bidding ML stack; externally a managed ad-buying product where the autonomy lives inside Tencent's surface, much like Meta Advantage+ is autonomy living inside Meta.
- **The Trade Desk (TTD)** — The dominant independent DSP outside the walled gardens.
- **Criteo** — The original retargeting DSP; still a meaningful programmatic player.
- **AppsFlyer / Adjust / Kochava** — Measurement (MMPs) rather than autonomy, but they own the attribution layer that makes Tier 4 economically legible.

### 6.1 Why Tier 4 is the most profitable layer in Martech

There are three structural reasons:

1. **They sit on a take-rate, not a license.** A SaaS agent product (Tier 2/3) earns $X per seat or per campaign. A programmatic network earns a percentage of every dollar of ad spend that passes through it. Volume × take-rate scales linearly with the entire ad market.
2. **They control both the matching algorithm and the data.** Unlike Tier 2 agents — which must integrate with the platforms above them and the brand's data below — Tier 4 owns the buying surface. The model is trained on first-party programmatic data the rest of the market cannot replicate.
3. **They are protected by network effects on both sides.** More publishers attract more advertisers attract more publishers. This is structurally similar to the moat under Tier 1, just on the supply side.

This is why "boring" companies like AppLovin or Mobvista — companies that almost no "AI marketing" thinkpiece talks about — are some of the most profitable AI-driven businesses in marketing. They are AI-native by every reasonable definition. They just do not market themselves as "agents."

### 6.2 So are Tier 4 players "marketing agents"?

By a strict definition — *systems that autonomously decide which ads to serve to which user at which price, with minimal human-in-the-loop* — **yes, they are**. AppLovin AXON, Mintegral's bidder, and the Tencent ad ranking system all meet that bar. They are operationally indistinguishable from Tier 1 in everything except *whose surface they live on*.

By the colloquial 2025 definition of "agent" — *LLM-driven, tool-using, planning-and-acting system that a marketer can talk to* — **no**. Tier 4 is overwhelmingly traditional ML (deep CTR/CVR models, two-tower retrieval, RL bidders), with LLMs limited to creative generation tasks at the edges.

This is exactly the same definitional split that exists in Tier 1. Performance Max is autonomous; it is not an "LLM agent." Both are valid framings depending on what question you are asking.

### 6.3 Why this matters for builders

For anyone building in Martech AI in 2026, the Tier 4 lens reorganizes the opportunity landscape:

- **If your edge is "better autonomous ML at scale,"** you are competing with Tier 1 and Tier 4 incumbents. The bar is harder than it looks, because the incumbents have the data flywheel. You need a wedge — a vertical (retail media, CTV, gaming UA, B2B) or a structural shift (post-cookie, retail-media fragmentation, AI-agent buyers) — that the incumbents are not optimizing for.
- **If your edge is "LLM reasoning over the marketing decision,"** you are in Tier 2/3 territory. Compete on strategy reasoning, creative chains, or Agent-to-Agent marketing. Do *not* compete with PMax or AppLovin on bidding execution — they have years of head-start and a data moat.
- **If your edge is "I sit on a chokepoint in the supply chain,"** you might be building Tier 4. This is the rarest and most defensible position. It usually requires owning a publisher network, an SDK install base, or an irreplaceable measurement layer. Hard to start from zero in 2026, but adjacent verticals (CTV, retail media on long-tail e-commerce, AI-agent-mediated commerce) still have open space.

### 6.4 Where the Chinese ad-tech ecosystem fits

The Chinese mobile-internet ad market produced an unusually strong Tier 4. Mobvista (with Mintegral) and ByteDance's ad stack are global Tier 4 players; Tencent Ads is Tier 4 inside the Tencent superapp surface; Alibaba Mama (阿里妈妈) is Tier 4 inside Alibaba's e-commerce surface; Pinduoduo's ad system is the same pattern. Domestic Tier 2/3 (independent agent products sold to brands) is comparatively thin, because the Tier 4 surfaces are so dominant that brands prefer to operate inside them rather than buy external automation layers.

This is the inverse of the US picture, where Tier 4 is more fragmented and Tier 2/3 has more room. It is one reason "marketing AI agent" narratives travel awkwardly across the Pacific — the framework is implicitly written about the US market, where the Tier 4 vacuum leaves more space for external products.

## 7. Synthesis

The original three-tier framework is correct for a specific question — *which agent product should a brand evaluate buying right now?* — and within that question, the LLM leverage points (strategy, creative chain, Agent-to-Agent) are the right places to look.

But if the question shifts to *where is the money in AI-driven marketing*, the answer has always been Tier 1 and Tier 4. AppLovin's AXON is not part of the LLM agent narrative, yet it is one of the most successful AI-driven business stories of the last three years. Any honest map of Martech AI has to put both rails on the same page.

The interesting frontier is the place where the two rails will eventually converge: **LLM-native agents that gain access to first-party data and become Tier 4-class autonomy operators in their own right**, rather than thin clients on top of someone else's surface. That convergence has not happened yet. When it does, the framework above will need a fifth box.

---

*Original analysis for [awesome-martech-ai](https://github.com/leoncuhk/awesome-martech-ai). Comments and corrections welcome via PR.*
