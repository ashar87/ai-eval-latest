# Module 5 · Eval Budget · Ascend IQ

**Quarterly budget cap:** $200,000
**Online eval spend:** $155,000 (2 of at most 3 online evals)

## Budget

| Failure | Trust metric | Risk | Level | Cost |
| --- | --- | :---: | :---: | ---: |
| Data Fabrication | Hallucination Rate | P0 | Online eval | $85,000 |
| Context Specificity | Robustness | P1 | Online eval | $70,000 |
| Overconfident Tone | UX Trust | P1 | Periodic audit | $6,500 |
| Data Bias | Fairness | P2 | Code-based check | $2,750 |
| Slow Answers | Latency | P3 | Code-based check | $1,250 |

## Downgrades

### Periodic audit · Overconfident Tone (UX Trust · P1)
- **Cheaper check:** Check 50 answers weekl, selecting a mixture of random answers and higher-risk responses.
- **Why it’s enough:** It catches overconfidence in the sampled traces but it misses full coverage.

### Code-based check · Data Bias (Fairness · P2)
- **Cheaper check:** Daily. Check the data summarised is from the right region when summarising.
- **Why it’s enough:** It catches data issues on sampled traces but coverage stays an issue. Since this is P2, the risk can be accepted for now.

### Code-based check · Slow Answers (Latency · P3)
- **Cheaper check:** Automatically capture latency on every production request, with threshold alerts and weekly trend reviews.
- **Why it’s enough:** Latency is a deterministic metric that can be measured continuously.
