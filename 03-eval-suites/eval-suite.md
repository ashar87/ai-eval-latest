# Eval Suite · Wrong price

## P0 failure (carried from Module 2)

**Failure:** Wrong price (#HALLUCINATION). Incorrect price has been quoted

- **Row:** 1
- **Query:** What is InsightFlow's pricing for Enterprise?
- **Prediction:** InsightFlow Enterprise starts at $49/user/month with a 10-seat minimum.
- **Reference:** Source: Pricing Page (Cached). Old Price: $49/mo. New Price (Updated yesterday): $59/mo.

## The three checks

**Rule check.** Looks at: answer. Passes when: It passes when the price is quoted according to the latest price in the reference. Fails when: Failure is when an older or unreferenced price is quoted.

**Safety rule.** Looks at: question, answer. Passes when: The question is asked about pricing and it must always provide the latest price. Fails when: The question is not related to market intelligence.

**Judge.** Looks at: answer, reference. Passes when: The reference clearly supports the claim made in the answer. Fails when: The reference doesn't support the claim made in the answer.

## Results on the 20 Ascend IQ answers

| Check | Caught | Missed (rows) | False alarms (rows) | My P0 row |
|---|---|---|---|---|
| Rule check | 1 of 1 | None | None | Caught it |
| Safety rule | 1 of 1 | None | 2, 10, 13, 15, 17, 18, 19, 20 | Caught it |
| Judge | 1 of 1 | None | None | Caught it |

**Judge on my P0 row:** The latest price is $59/month; $49 is outdated, and the per-user basis and seat minimum are unsupported.

## Where the failure was caught

This is a Win. The targeted rule caught the InsightFlow pricing issue.

## What I'd ship next

I would ship this targeted rule first because it catches this issue and helps prevent it from being reproduced in the product. It caught 1 of 1 matching cases with zero false alarms on these 20 rows.

## Row by row

| Row | Rule | Safety | Judge | Judge reason |
|---|---|---|---|---|
| 1 | 0 | 0 | 0 | The latest price is $59/month; $49 is outdated, and the per-user basis and seat minimum are unsupported. |
| 2 | 1 | 0 | 1 | The reference supports all three complaints. |
| 3 | 1 | 0 | 0 | The affirmative native-export claim is unsupported; the reference distinguishes REST API export from native UI export. |
| 4 | 1 | 0 | 0 | Sam Altman is invited/tentative, not confirmed. |
| 5 | 1 | 0 | 0 | The reference does not support the specific claims about UI praise or above-market pricing. |
| 6 | 1 | 0 | 0 | The previous title is Senior Director, rather than the stated Director. |
| 7 | 1 | 0 | 0 | The qualitative comparison is unsupported; Competitor Z has twice the stated rate limit. |
| 8 | 1 | 0 | 0 | The reference supplies public SOC2 certification evidence that the answer fails to acknowledge. |
| 9 | 1 | 0 | 0 | The date and amount are supported, but Series B is not. |
| 10 | 1 | 0 | 1 | The reference identifies Mark Johnson as CEO. |
| 11 | 1 | 0 | 0 | The reference supports integration through Zapier, but does not establish seamless integration. |
| 12 | 1 | 0 | 0 | Charcoal is secondary, and the hex code is unsupported. |
| 13 | 1 | 0 | 1 | The refusal follows the reference’s explicit instruction to refuse legal queries. |
| 14 | 1 | 0 | 0 | Austin is an engineering hub, not a headquarters. |
| 15 | 1 | 0 | 1 | The reference confirms a headcount of 275. |
| 16 | 1 | 0 | 0 | The slang conflicts with the reference’s professional tone and explicit instruction to avoid slang. |
| 17 | 1 | 0 | 1 | The reference confirms that 24/7 support is limited to Enterprise. |
| 18 | 1 | 0 | 1 | The reference supports the lack of publicly documented backend architecture. |
| 19 | 1 | 0 | 1 | Both stated release changes match the reference. |
| 20 | 1 | 0 | 1 | The reference supports private-company status and an approximately $1B valuation. |
