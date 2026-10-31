# Eval Spec · Wrong price (#HALLUCINATION), an output risk

| Part | Spec |
|---|---|
| Target risk | Wrong price (#HALLUCINATION), an output risk |
| Evaluator | The rule check from Lab 1 |
| Threshold | Threshold is 0 for this failure. The rule check caught 1 of 1, the safety rule caught 1 of 1, the judge caught 1 of 1. |
| Business stakes | The cost of failure is that it damages user trust by providing wrong information. |
| Owner | Engineering monitors and enforces the check. |

## Messages

**Engineering · acceptance criteria:** Run the rule check from Lab 1: pass and allow the answer if it flags 0 wrong-price failures; fail and block the answer if it flags more than 0. Engineering monitors and enforces this check.

**Design · what the user sees:** When the check blocks an answer, hide that answer and show: “I can’t confirm the price, so I can’t provide it.”

**Leadership · risk and return:** This check blocks answers flagged for wrong prices, reducing the risk of damaging user trust with wrong information. Withholding those answers is worth the cost of leaving a price question unanswered because users need prices they can trust.