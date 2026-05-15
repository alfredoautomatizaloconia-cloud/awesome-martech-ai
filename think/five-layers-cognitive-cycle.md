# The Five Layers as a Cognitive Cycle

*[中文版 / Chinese version](five-layers-cognitive-cycle.zh.md)*

The five layers of the Martech AI Stack are not an arbitrary slicing. They decompose a single cycle — *data → action → feedback* — into stages that can be independently owned, optimized, and reasoned about. Each layer answers a different epistemic question.

| Layer | The question it answers | What it produces | One-word essence |
|---|---|---|---|
| **Data** | Who is the user? What happened? | Queryable factual records | Facts |
| **Intelligence** | What can we infer or predict? | Scores, probabilities, embeddings, causal effects | Beliefs |
| **Decision** | What action should we take? | Concrete per-decision recommendations | Choices |
| **Activation** | How do we get the action in front of the user? | Delivered impressions, messages, prompts | Actions |
| **Measurement** | Did it work? How should we update our beliefs? | Causal effect estimates, feedback into the loop | Truth |

## Layer by layer

### 1. Data Layer — "Facts"

Answers *what happened, who is who*. It records and does not judge.

- **Owns:** identity graph, event stream, consent state, clean rooms
- **Verbs:** collect, identify, resolve, govern
- **Typical outputs:** "User X viewed page Y at time T"; "cookie Z and login ID X are the same person"
- **Failure modes:** identity inconsistency, broken event taxonomy, missing consent metadata. Every layer above is poisoned when this layer fails.

### 2. Intelligence Layer — "Beliefs"

Turns facts into structured inferences about the future or about unobserved state.

- **Owns:** supervised ML (CTR/CVR/LTV), causal models (uplift, DiD), RL policies, embeddings, foundation models
- **Verbs:** predict, estimate, embed, infer
- **Typical outputs:** "User X has 0.73 conversion probability"; "Creative A lifts response by 1.2× over B"; "This cohort is push-sensitive but email-insensitive"
- **Failure modes:** overfitting historical data, missing regime shifts, optimizing the wrong target (using prediction where causation is needed)

### 3. Decision Layer — "Choices"

Maps beliefs to specific actions. This is the leap from *what we know* to *what we do*.

- **Owns:** bidding policies, NBA policies, budget allocation, audience selection
- **Verbs:** choose, bid, allocate, target
- **Typical outputs:** "Bid $0.43 on this impression"; "Send promo X to cohort Y on Tuesday 9am"; "Allocate 35% of this quarter's budget to Meta"
- **Failure modes:** greedy optimization, no counterfactual reasoning, missing exploration, mismatched decision granularity vs. objective

### 4. Activation Layer — "Actions"

Physically delivers decisions to users. This layer does not optimize — it executes.

- **Owns:** paid media surfaces, CRM, push, email, in-app prompts, conversational channels
- **Verbs:** serve, send, render, converse
- **Typical outputs:** ad impressions actually served, push notifications actually sent, conversational responses actually rendered
- **Failure modes:** delivery failures, latency, channel constraints not respected, creative rendering errors

### 5. Measurement Layer — "Truth"

Decides whether actions actually produced the causal effect we wanted, and feeds the result back to Intelligence.

- **Owns:** A/B platforms, incrementality tests, MMM, attribution, switchback, synthetic control
- **Verbs:** experiment, measure, attribute, backtest
- **Typical outputs:** "Treatment ROAS = 2.3 vs control 1.8, p<0.01"; "MMM shows Meta saturating beyond $5M"; "Net lift of this push is ~0.2pp"
- **Failure modes:** confounding, attribution illusions, p-hacking, missing counterfactuals, treating correlation as causation

## Why five layers, not three or seven

The slicing is not arbitrary. Each boundary corresponds to a conceptual distinction that should not be collapsed:

| Boundary | What it separates | Cost of collapsing |
|---|---|---|
| Data ↔ Intelligence | Facts vs. beliefs | Model predictions get stored as facts in the CDP, poisoning every downstream layer |
| Intelligence ↔ Decision | Prediction vs. action | A CTR predictor used directly as a bidding policy — the canonical early-ML mistake |
| Decision ↔ Activation | Choosing vs. executing | Delivery failures blamed on strategy, or strategy failures blamed on delivery |
| Activation ↔ Measurement | Doing vs. knowing-it-worked | "I shipped it, so it must have worked" — the source of all attribution illusions |

Each layer has its own domain experts, its own KPIs, and its own failure modes. Decoupling them is what allows one team to optimize a single layer without contaminating another.

## The cycle

```
       ┌───────────── Measurement ──────────────┐
       │           (truth feedback)              │
       ↓                                         │
   Intelligence ←──── Data ──────                │
       │           (facts supply)                │
       ↓                                         │
    Decision ──────→ Activation ─────────────────┘
    (choose action)  (execute action → new facts)
```

**Measurement flows back to both Intelligence (updating beliefs) and Data (producing new experimental facts).** This is the essence of the closed loop. A system without Measurement is not a Martech AI system — it is a one-way emitter.

---

*Companion to [`three-tier-marketing-agents.md`](three-tier-marketing-agents.md). Both essays inform the Cross-Layer Domain Views table in the [main README](../README.md).*
