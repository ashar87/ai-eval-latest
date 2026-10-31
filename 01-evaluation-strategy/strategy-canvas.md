# AI Evaluation Strategy Canvas

> Repo file `ai-evals/01-evaluation-strategy/strategy-canvas.md` (the repo is your submission).

## 1. Product Strategy, The Context

**Who it's for:** VP-level strategists and product leaders at Fortune 500 companies who pay upward of $50,000 a year for verified market intelligence.

**What they use it for:** Asking plain-language questions, like “Compare the pricing models of Stripe and Adyen,” and getting answers in seconds instead of digging through the platform.

**What's at stake:** Engagement is dropping, Q4 retention is at risk, and the CPO wants Ascend IQ live for the top 50 enterprise accounts next month. One poor answer to the wrong client can do lasting damage to the relationship.

## 2. Measurements, The Execution

**User promise.** For VP-level strategists and product leaders at Fortune 500 companies, Ascend IQ promises answers where every factual claim is supported by a verified source, so they can make confident strategic decisions.

**Top 3 trust metrics:**
- **Hallucination Rate**, % of outputs that are confidently false or fabricated.
- **Robustness**, Coherence on messy, adversarial, out-of-scope inputs.
- **UX Trust**, Subjective predictability and consistency over time.

**Why these three:** Hallucination Rate: fabricated claims could lead leaders to make expensive, incorrect decisions.
UX Trust: a predictable, consistent experience gives users confidence in the output.
Robustness: busy product leaders may ask messy questions, and Ascend IQ still needs to handle them reliably.

## 3. Strategic Trade-Offs, The Cost

### Trade-off 1 · Hallucination Rate ↔ UX Trust
We prioritise reducing hallucinations over giving a decisive answer because leaders could make expensive decisions based on unsupported claims. Clearly admitting uncertainty should build trust over time.

### Trade-off 2 · Hallucination Rate ↔ Robustness
We prioritise reducing hallucinations over answering every messy question immediately because guessing a leader’s intent could produce misleading advice. When ambiguity affects accuracy, Ascend IQ should ask a brief clarifying question.

---
_Generated from the AI Evaluation Strategy Canvas, M1 lab tool, AI Evals Certification._