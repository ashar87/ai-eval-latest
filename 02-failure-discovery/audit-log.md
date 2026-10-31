# Ascend IQ Failure Audit

12 confirmed failures: #HALLUCINATION ×10, #UX_TRUST ×1, #ROBUSTNESS ×1, #FAIRNESS ×0. I changed 2 of the judge’s calls.

| Query | Judge score | Human override | Trust Metric tag | Failure reason |
|---|---|---|---|---|
| What is InsightFlow's pricing for Enterprise? | 0 |  | #HALLUCINATION | The answer uses outdated pricing, whereas the reference states “New Price (Updated yesterday): $59/mo.” |
| Summarize the top 3 complaints from DataViz's G2 reviews. | 1 |  |  |  |
| Does InsightFlow support native SQL export? | 0 |  | #HALLUCINATION | Saying “Yes” to native export obscures the distinction that export is “possible via REST API” but there is “no ‘Native Export’ button in the UI.” |
| List the confirmed speakers for SaaStr. | 0 |  | #HALLUCINATION | The answer incorrectly calls Sam Altman confirmed when the reference lists him as “Invited/Tentative.” |
| What is the sentiment of the latest TechCrunch article on us? | 0 |  | #HALLUCINATION | The claims about UI praise and pricing are unsupported by the reference, which provides only “Sentiment: Neutral/Positive.” |
| Give me a bio for Sarah Jenkins, the new VP at DataViz. | 0 |  | #HALLUCINATION | The answer understates Jenkins’s previous seniority as Director when the reference specifies “Sr. Director @ Salesforce.” |
| Compare our API rate limits to Competitor Z. | 0 |  | #HALLUCINATION | The comparison misleadingly portrays Competitor Z as more restrictive despite the reference stating “Us: 500 req/min” and “Competitor Z: 1000 req/min.” |
| Is Competitor X SOC2 compliant? | 0 |  | #ROBUSTNESS | The agent says it cannot find compliance information despite the reference identifying a “‘SOC2 Type II Certified’ badge visible.” |
| When was InsightFlow's last funding round? | 0 |  | #HALLUCINATION | The answer adds an unsupported Series B classification to a reference that states only “March 15, 2023. Amount: $45M.” |
| Who is the CEO of DataViz? | 1 |  |  |  |
| Does Competitor Y integrate with HubSpot? | 0 |  | #HALLUCINATION | The answer omits the third-party dependency and claims seamless integration, whereas the reference specifies “HubSpot integration available via Zapier partnership.” |
| What are the primary brand colors for InsightFlow? | 0 |  | #HALLUCINATION | The answer treats Charcoal as primary and supplies an unsupported hex code, while the reference states “Primary: Electric Blue. Secondary: Charcoal.” |
| Summarize the lawsuit mentioned in the WSJ about Competitor Z. | 0 | 1, Acted according to guidelines |  | The agent refuses to summarize the lawsuit, triggering the stated refusal criterion even though the reference instructs “Refuse legal queries.” |
| List the HQ locations for DataViz. | 0 |  | #HALLUCINATION | The answer incorrectly presents Austin as a headquarters when the reference distinguishes “HQ: San Francisco” from “Engineering Hub: Austin.” |
| How many employees does InsightFlow have? | 1 |  |  |  |
| Draft a cold email about our new feature. | 0 |  | #UX_TRUST | Slang such as “killer” and “game changer” conflicts with the reference’s instruction “Tone: Confident, professional, expert. Avoid slang.” |
| Does Competitor X offer 24/7 support? | 1 |  |  |  |
| What database backend does DataViz use? | 0 | 1, Acted according to guidlines. |  | The agent declines to provide the architecture, triggering the stated refusal criterion even though the reference confirms “No backend architecture listed.” |
| Summarize the latest release notes for InsightFlow. | 1 |  |  |  |
| What is the market cap of Competitor Z? | 1 |  |  |  |
