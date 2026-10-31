# Module 4 · Launch Strategy · Ascend IQ Copilot

## 4.0 Release Criteria

| Gate | Failure | Metric | Threshold | Dataset | Method | Runs at |
|---|---|---|---|---|---|---|
| Hard | Row 1 Hallucination: The answer quotes the old price as current | % of answers with qrong price | 0% | Ascend IQ golden set | Code-based check | Staging |
| Soft | Row 17 · Tone: slang detected | % of answers with slang.  | Less than 1%. | Ascend IQ golden set | LLM judge | Staging |
| Advisory | Row 3 · Latency: exceeded the maximum response time | Average latency | Less than 3s. | Ascend IQ golden set | Code-based check | Staging |

## CI Gate Request for Engineering

- **Hard gate · Row 1 Hallucination: The answer quotes the old price as current.** Check: the code-based check, run on the Ascend IQ golden set at Staging. Measures: % of answers with qrong price. Passes when: 0%. On a fail: block the merge.
- **Soft gate · Row 17 · Tone: slang detected.** Check: the LLM judge, run on the Ascend IQ golden set at Staging. Measures: % of answers with slang. . Passes when: Less than 1%.. On a fail: pause the release until the PM signs off on an override.
- **Advisory gate · Row 3 · Latency: exceeded the maximum response time.** Check: the code-based check, run on the Ascend IQ golden set at Staging. Measures: Average latency. Passes when: Less than 3s.. On a fail: post a warning, and don't block.

## Mitigation Plan · Soft Gate

If our Soft gate fails (i.e., slang is detected), I recommend delaying the launch. The issue can be damage the reputation and delay will give us some time to bring the % below the threshold.
