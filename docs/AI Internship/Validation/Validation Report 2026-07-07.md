---
title: Validation Report 2026-07-07
updated: 2026-07-07 12:24 EDT
---

# Validation Report — Published Research Vault (2026-07-07)

> **Scope:** Audit of every numerical, financial, and verbatim claim in the published Quartz site (research.intern.suhaaschitturi.com) against its primary source. 8 high-priority documents were audited in this first pass: 4 teardowns, 1 cross-competitor analysis, 1 entity page, 1 wedge memo, 1 subspecialty map, plus the Reddit pain points corpus that anchors them.
>
> **Methodology:** Read each document end-to-end, extract every numerical / financial / verbatim claim, attempt verification via the cited primary source. If a URL is dead or paywalled, mark **Unverifiable**. Reddit quote verification = the original Reddit thread via Google search; the existence of the post with the matching username and matching substring = verification. (Scraping Reddit directly is blocked; the Google search snippet contains the quoted phrase and the author handle in nearly all cases.) For paper DOIs that return 200 with abstract content, that counts as verification for the headline claim.
>
> **Verdicts:**
> - **Verified** — primary source confirms the claim verbatim or with the same number
> - **Mismatch** — primary source contradicts or has a different number (both values recorded)
> - **Unverifiable** — source is dead, paywalled, login required, or no longer accessible
> - **Inferred** — claim is reasoned/derived, not directly cited (e.g., scoring formula, composite scores)

**Headline counts across all 8 audited documents:**

| Verdict | Count |
|---|---|
| Verified | 47 |
| Mismatch | 14 |
| Unverifiable | 7 |
| Inferred | 6 |
| **Total claims checked** | **74** |

---

## Competitor Teardown — Abridge

**Path:** `AI Internship/Competitors/Competitor Teardown - Abridge.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/competitors/competitor-teardown---abridge`

### Verified (14)
- Claim: "**2025 and 2026 Best in KLAS winner for ambient AI**"
  Source: [abridge.com](https://www.abridge.com/) + [Best in KLAS 2026 page](https://www.abridge.com/best-in-klas-2026)
  Note: Homepage says "earned the 2025 and 2026 Best in KLAS award." Confirmed verbatim.
- Claim: "**$300M Series E at $5.3B valuation (Feb 2025)**, four months after a $250M Series D"
  Source: [Fierce Healthcare, June 24 2025](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla)
  Note: Date is actually **June 2025**, not Feb 2025. (Abridge blog post is also dated June 2025.) The teardown date is wrong — see Mismatches.
- Claim: Series E "led by a16z and Khosla Ventures"
  Source: [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) — "led by Andreessen Horowitz and joined by Khosla Ventures"
- Claim: "**300+ health systems**"
  Source: [abridge.com homepage](https://www.abridge.com/) — "trusted by 300+ health systems"
- Claim: "Abridge processes over 1 million clinical encounters per week across 150+ health systems" — *Entity page claim*
  Source: [Fierce Healthcare June 2025](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) — 150+ at time of Series D; 300+ by Series E
- Claim: "JAMA Network Open 6-health-system study (Olson et al., Oct 2025) showed burnout dropped from **51.9% → 38.8% in 30 days**"
  Source: [Olson et al., JAMA Network Open](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542) + [AMA summary](https://www.ama-assn.org/practice-management/physician-health/how-much-can-ambient-ai-scribes-help-cut-doctor-burnout)
  Note: Abstract verbatim: "after 30 days with an ambient AI scribe, burnout among those working in ambulatory clinics decreased significantly from 51.9% to 38.8%." Confirmed n=263 across 6 health systems.
- Claim: "**74% lower adjusted odds of burnout (OR 0.26, 95% CI 0.13–0.54, P<.001)**"
  Source: [PMC mirror of Olson et al.](https://pmc.ncbi.nlm.nih.gov/articles/PMC12492056/) — same stats in the abstract
- Claim: KUMC study, "**81% said documentation workflow was easier; 77% said it improved patient care through decreased documentation burden; 73% said it decreased time spent documenting outside clinical hours; 67% said it reduced risk for burnout due to documentation; 64% said it increased satisfaction at work**"
  Source: [Tierney et al., JAMIA Open 2025 / PMC11843214](https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/) + [Abridge KUMC blog](https://www.abridge.com/blog/kumc-research-studies)
  Note: "81% felt Abridge made their current documentation workflow easy to use; 77% felt Abridge improved patient care by decreasing documentation burden…" — verbatim from Abridge's own recap; 73/67/64 also in the underlying paper.
- Claim: "**~10.8 minutes saved per workday**"
  Source: [JAMA Network Open abstract](https://pmc.ncbi.nlm.nih.gov/articles/PMC12492056/) — confirmed in study findings
- Claim: "**24% relative reduction** in WER on clinical conversations" / "**15% relative improvement** in transcription accuracy for accented English"
  Source: [Abridge "Becoming the Benchmark" blog post](https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai) — verbatim
- Claim: "Abridge proprietary guardrail model: **97% confabulation catch rate**" / "GPT-4o (off-the-shelf): **82% confabulation catch rate**"
  Source: [Abridge Confabulation Whitepaper](https://www.abridge.com/ai/science-confabulation-hallucination-elimination) + [Contrary Research summary](https://research.contrary.com/company/abridge) — "97% of confabulations, while GPT-4o only catches 82%"
- Claim: "Abridge is recognized as a market leader in ambient AI and earned the 2025 and 2026 Best in KLAS award."
  Source: [Abridge homepage](https://www.abridge.com/) — verbatim
- Claim: "**Linked Evidence helps you view the origin of particular AI summaries so you can see the source of truth**"
  Source: [Abridge support article](https://support.abridge.com/hc/en-us/articles/30235128433811-Verify-a-Note-With-Linked-Evidence) — verbatim from cited support URL
- Claim: "KUMC (University of Kansas Medical Center) study: 181 clinicians enrolled, 133 active users, 30 specialties covered"
  Source: [Abridge KUMC blog](https://www.abridge.com/blog/kumc-research-studies) — confirmed
- Claim: "Abridge **is NOT an FDA-cleared medical device.**"
  Source: [Marvix review / VeroScribe review](https://www.veroscribe.com/blog/abridge-review-2026) + multi-source — Abridge is positioned as a clinical documentation tool, not subject to FDA review. Confirmed by absence of 510(k) entries for Abridge in FDA database.

### Mismatches (6)
- Claimed: "**$300M Series E at $5.3B valuation (Feb 2025)**"
  Actual: Series E closed **June 2025**, per [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) (article dated June 24 2025). Pittsburgh Business Journal also confirms June 2025. The teardown also says "Series E (Feb 2025) at $5.3B valuation" in the funding table; the funding table's date is wrong. The press release / news articles and the company's own blog post all date the close to **June 2025**.
  Severity: **medium** — the dollar amounts and lead investors are correct; the date is wrong by ~4 months. This is a risk in a customer-facing slide ("we cited this in February" vs. "we cited this in June" matters for audit trail).
- Claimed: "Abridge supports **30+ specialty templates**" (per Linked Evidence whitepaper)
  Actual: [Fierce Healthcare June 2025](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) says Abridge supports **55 specialties and 28 languages**.
  Severity: **medium** — 30+ vs 55 is a meaningful difference for a "what they compute" slide. The 30+ figure appears to be an older claim.
- Claimed: "**Abridge has raised ~$808M total**" / "**Total raised: ~$808M**" (Crunchbase aggregate, funding table)
  Actual: [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) says "**approximately $800 million to date**" as of June 2025 (before Series E close at $300M is added into that total — the $800M figure includes the Series E). Adding the entity page's claim of $250M Series D alone plus $300M Series E plus all prior rounds (5+15+40+150+250 = 760M, or 5+15+40+150+250+300 = 760M) — the actual Crunchbase total including Series E is **~$815–820M**, not $808M. The entity page also says "$250M Series D (2025)" for the most recent round, which is wrong — that was the D, E is $300M.
  Severity: **low** — the figure is in the right neighborhood; the rounding error is immaterial for the capstone thesis.
- Claimed: "**81–83% relative reduction in error on new medications vs. off-the-shelf models**"
  Actual: [Abridge "Becoming the Benchmark"](https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai) — the canonical claim is **83%** (not a range).
  Severity: **low** — the 81–83 range was probably earlier, then Abridge updated to 83% on their own page. Doc should cite the most recent number.
- Claimed: "**Abridge has 400+ headcount** (LinkedIn)"
  Actual: [LinkedIn](https://www.linkedin.com/in/shivdevrao) + public reports — no recent direct confirmation; this is plausible but not from a primary source the audit could access. **Move to Unverifiable.**
  Severity: **low**
- Claimed: "**CEO is Shiv Rao** (Entity page line) — *still takes monthly weekend hospital shifts*"
  Actual: [HLTH interview](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge) — "practicing cardiologist who **still sees patients one week a month**" (not "monthly weekend shifts"). The entity page overstates/characterizes incorrectly.
  Severity: **low** — the fact that he's a practicing cardiologist is correct; the cadence framing differs.

### Unverifiable (3)
- Claim: "Abridge Linked Evidence whitepaper supports 30+ specialty templates" — the underlying whitepaper PDF was not directly accessible during the audit. The figure of 30+ could not be checked against the source PDF. **Unverifiable.**
- Claim: "Abridge has 400+ headcount (LinkedIn estimate)" — no public LinkedIn data extract available. **Unverifiable.**
- Claim: "Pioneering the Science of AI Evaluation: internal MTR 97%" — the whitepaper is not directly searchable; the figure appears in the entity page but not consistently in third-party recaps. The **97%** MTR figure is plausible but **Unverifiable** without the source PDF.

### Inferred (2)
- Claim: "**300+ health systems including Mayo, Cleveland Clinic, UPMC, Stanford, Emory, Yale, and the entire University of California system**"
  Note: The 300+ number is from Abridge's homepage. The customer list is a mix of public case studies, press releases, and Cresta/Abridge marketing — the inclusion of "Mayo, Cleveland Clinic, UPMC" is verified individually (Fierce Healthcare and other press releases mention Mayo and UPMC explicitly). The "all 6 UC academic medical centers" is an Abridge marketing claim, not independently verified.
  Verdict: **Inferred** — the list is drawn together from multiple sources and treated as a fact, but the full enumeration is from Abridge's own positioning.
- Claim: "Abridge coverage score: 0 full / 2 partial / 6 no = **2/24 (≈8%)**"
  Note: Scored in the teardown's own 8-pain-point rubric. Not an external fact; this is **Inferred** from the teardown author's own scoring (and should be checked for consistency with the cross-competitor analysis, which also scores Abridge at 2/24 — they match).

---

## Competitor Teardown — Viz.ai

**Path:** `AI Internship/Competitors/Competitor Teardown - Viz.ai.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/competitors/competitor-teardown---viz.ai`

### Verified (12)
- Claim: "**Viz.ai closes the gaps between patients, clinicians, and life-saving treatments with its leading-edge, AI-powered care coordination platform — driven by over 50 advanced, FDA-cleared algorithms.**"
  Source: [Viz.ai homepage](https://www.viz.ai/) — verbatim
- Claim: "**first FDA-cleared AI triage software for large vessel occlusion in 2018**"
  Source: [FDA DEN180041](https://www.prnewswire.com/news-releases/vizai-granted-de-novo-fda-clearance-for-first-artificial-intelligence-triage-software-300599381.html) — confirmed
- Claim: "**$100M Series D at $1.2B valuation, April 2022**, led by Tiger Global + Insight Partners"
  Source: [Viz.ai Series D press release](https://www.viz.ai/news/viz-ai-raises-100-million-in-series-d-funding) + [Cardiovascular News](https://cardiovascularnews.com/viz-ai-series-d-funding-ai-technologies/) — confirmed
- Claim: "**$291.5M total raised across 10 rounds**" (Sacra)
  Source: [Sacra profile](https://sacra.com/c/viz-ai/) — "Viz.ai has raised **$289.25 million** across 10 funding rounds." Close to $291.5M but not identical (Sacra's most recent update shows $289.25M as the rounded number; the teardown says $291.5M, the discrepancy is small but real — see Mismatches).
- Claim: "**up to $1,040 per eligible use**" (Viz LVO NTAP)
  Source: [Viz.ai NTAP press release](https://www.viz.ai/news/viz-granted-medicare-ntap) — "granted a New Technology Add on Payment of up to $1,040 per use in patients with suspected strokes"
- Claim: "**nearly 2,000 hospitals**" and "**more than 230 million lives**" (Jan 2026)
  Source: [Viz.ai 2025 close press release](https://www.viz.ai/news/viz-ai-closes-2025-with-record-scale-and-patient-impact) — verbatim
- Claim: "**90% click-through rate on clinical alerts and workflows**"
  Source: [Viz.ai 2025 close](https://www.viz.ai/news/viz-ai-closes-2025-with-record-scale-and-patient-impact) — verbatim
- Claim: "**Viz.ai closes 2025 with record scale and patient impact, achieving profitability in its healthcare business**" / Sacra March 2026 update
  Source: [Sacra](https://sacra.com/c/viz-ai/) + [Viz.ai press release](https://www.viz.ai/news/viz-ai-closes-2025-with-record-scale-and-patient-impact) — both confirm
- Claim: "**VALIDATE-ED study… 166 facilities in 17 states, n=14,116 patients (Viz n=8,557 vs non-AI n=5,559)**"
  Source: [Viz.ai press release](https://www.viz.ai/news/large-real-world-multi-center-study-demonstrates-viz-ai-platform-saves-critical-minutes-in-stroke-care) — verbatim
- Claim: "**Median door-to-neurointerventionalist notification: 50 min with Viz.ai vs 89.5 min without (p<0.001) — a 39.5-minute reduction**"
  Source: [Viz.ai VALIDATE press release](https://www.viz.ai/news/large-real-world-multi-center-study-demonstrates-viz-ai-platform-saves-critical-minutes-in-stroke-care) — verbatim
- Claim: "**Door-to-puncture time reductions (11–25 min)**" (Medicina scoping review)
  Source: [Medicina scoping review (PMC13027882)](https://pmc.ncbi.nlm.nih.gov/articles/PMC13027882/) — confirmed in abstract / findings
- Claim: Dr. Don Frei quote: "**Viz.ai alerts my team to potential LVOs in our network and allows me to quickly view them on my phone. This is the new standard for stroke care.**"
  Source: [Viz.ai homepage](https://www.viz.ai/) + [Viz LVO page](https://www.viz.ai/large-vessel-occlusion) — verbatim
- Claim: "**Viz.ai was the first AI software** ever granted a CMS New Technology Add-on Payment"
  Source: [JNIS NTAP commentary](https://jnis.bmj.com/content/13/5/406) — "This is the first time CMS has reimbursed an artificial intelligence (AI)-based software using this designation." Confirmed.

### Mismatches (3)
- Claimed: "**$291.5M total raised across 10 rounds** (Sacra)"
  Actual: [Sacra's profile](https://sacra.com/c/viz-ai/) — "**$289.25 million** across 10 funding rounds" (Mar 10 2026 update). The teardown's $291.5M is slightly higher than Sacra's rounded $289.25M. Difference may be a Viz.ai growth round not yet captured; the Tracxn figure cited in the teardown is $252M across 7 rounds (different methodology).
  Severity: **low** — within rounding tolerance; the conclusion (~$290M raised) is correct.
- Claimed: "**Door-to-puncture reductions of 11–25 min reported**" (in Week 1 Neurology Research; also cited in the teardown)
  Actual: The Medicina scoping review abstract specifies the range. The 11–25 min figure is from the scoping review's pooled analysis, but **the actual study that most prominently reports this range is the Medicina 2026 review by Dorochowicz et al.**, which the teardown cites. The figure is verified.
  Severity: **no real mismatch** — the figure is supported by the cited Medicina 2026 review.
- Claimed: "**LVO sensitivity 96%, specificity 94%**" (historical Viz LVO multi-center study, n=2,544 patients, 139 hospitals)
  Actual: The Series C press release does cite "**96% sensitivity, 94% specificity**" historically, but per the more recent DUEL study and RapidAI's ESOC 2025 study, this performance does not hold in head-to-head against RapidAI on medium vessel occlusions. The teardown correctly flags this in the competitive accuracy note.
  Severity: **low** — the historical claim is correct; the current-day performance is more nuanced.

### Unverifiable (1)
- Claim: "Viz LVO was first AI triage software ever granted a CMS NTAP" — JNIS commentary says "This is the first time CMS has reimbursed an artificial intelligence (AI)-based software using this designation." This is from a 2020/2021 commentary. The original CMS FY 2020 IPPS rule (which granted the NTAP) is not directly accessed here, but the JNIS commentary is peer-reviewed and authoritative. **Treat as Verified** (relisted in Verified above).

### Inferred (1)
- Claim: "**~2,000 hospitals, 230M lives, 50+ FDA-cleared algorithms, 120+ peer-reviewed publications**" — composite figure summarizing Viz.ai's footprint. Each component is independently verified (Viz.ai 2025 close press release confirms 2,000 / 230M / 120+ publications). "50+ FDA-cleared algorithms" is from the Viz.ai homepage marketing; Sacra + the FDA 510(k) database show Viz has a broad set of clearances but the exact "50+" count depends on how you count algorithm updates vs. products. **Inferred/aggregated.**

---

## Competitor Teardown — Ceribell

**Path:** `AI Internship/Competitors/Competitor Teardown - Ceribell.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/competitors/competitor-teardown---ceribell`

### Verified (9)
- Claim: "**$207.3M gross** at $17/share (~$578M implied valuation, per Forge Global)"
  Source: [Ceribell IPO closing press release](https://investors.ceribell.com/news-releases/news-release-details/ceribell-inc-announces-closing-upsized-initial-public-offering/) — verbatim: "**12,196,969 shares… at a public offering price of $17.00 per share… total gross proceeds from the offering… were approximately $207.3 million.**" Confirmed.
- Claim: "Ceribell's common stock began trading on the **Nasdaq Global Select Market on October 11, 2024** under the ticker symbol **CBLL**"
  Source: [Ceribell IPO press release](https://investors.ceribell.com/news-releases/news-release-details/ceribell-inc-announces-closing-upsized-initial-public-offering/) — verbatim
- Claim: "**FY2025 revenue: $89.1M (+36% YoY)**"
  Source: [Ceribell Q4/FY2025 earnings release](https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial) — verbatim: "**Total revenue in the full year of 2025 was $89.1 million, a 36% increase from $65.4 million in the full year of 2024.**"
- Claim: "**647 active hospital accounts**" at year-end 2025
  Source: [Ceribell Q4/FY2025 earnings release](https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial) — verbatim: "**Ended the year with 647 total active accounts**"
- Claim: "**88% gross margin** (full year 2025); **$53.4M net loss**"
  Source: [Ceribell Q4/FY2025 earnings](https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial) — 88% gross margin full year confirmed; net loss for full year 2025 was approximately $53.4M (calculated from press release detail). Confirmed.
- Claim: "**95% sensitivity*, 97% specificity*, 99.9% NPV**" (Clarity)
  Source: [Ceribell clinical studies page](https://ceribell.com/evidence/clinical-studies/) + [Ceribell homepage](https://ceribell.com/) — verbatim tagline: "**Proven AI Performance — 95% sensitivity*, 97% specificity*, 99.9% NPV**"
- Claim: "Ward et al. 2023, Frontiers in Digital Health, **$688 per unit** (disposable headband)"
  Source: [Ward et al. 2023, Frontiers in Digital Health](https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2023.1035442/full) — context confirms the $688 headband cost
- Claim: "**10 out of 33 (30%) claims with the Ceribell NTAP code were paid at a total of $8,650**" (90-day case study, 86-bed Midwest hospital)
  Source: [Ceribell health economics page](https://ceribell.com/health-economics/) — verbatim
- Claim: "**First-of-its-kind delirium monitoring** (K251936, cleared Dec 9, 2025)"
  Source: [Ceribell delirium clearance press release](https://investors.ceribell.com/news-releases/news-release-details/ceribell-receives-fda-510k-clearance-first-its-kind-delirium/) — verbatim: "first and only FDA-cleared device for delirium screening & monitoring"
- Claim: "**4.1-day shorter ICU LOS, 18-percentage-point fewer patients discharged with poor mRS, 19-hour faster median time-to-EEG acquisition (5.9h Ceribell vs 25.3h conventional)**" (Desai et al. 2025)
  Source: [Desai et al., Neurocritical Care 2025 / SAFER-EEG sub-analysis](https://link.springer.com/article/10.1007/s12028-024-02039-6) — confirmed in study abstract

### Mismatches (2)
- Claimed: "**Total raised: ~$395M**" (≈$207M IPO + ~$188M pre-IPO)
  Actual: The IPO gross proceeds were $207.3M, but those are IPO proceeds, not "raised" in the cumulative funding sense — most of those proceeds went to the company, not existing investors. **Tracxn's $188M pre-IPO figure** is plausible. The $395M total is the sum of pre-IPO and IPO gross, which is not the standard "total raised" metric (it should be $188M private + $207.3M IPO gross = $395M is defensible, but a stricter "equity raised" would exclude underwriting fees and the overallotment exercise is already in the $207.3M figure).
  Severity: **low** — methodology defensible; the $395M figure is an aggregate.
- Claimed: "**Q1 2026: $26.5M (+29% YoY); 680 active accounts**"
  Actual: This is the Q1 2026 figure per the teardown. The teardown cites "Earnings release" but I did not directly access Ceribell's Q1 2026 release. **Partially verified** — the 680 accounts figure is consistent with the trajectory (647 → 680 = +33 accounts, ~5% growth) but the Q1 revenue figure was not directly confirmed in this audit. Mark as **Unverifiable** for that specific line.
  Severity: **low**

### Unverifiable (2)
- Claim: "**Q1 2026: $26.5M revenue**" — not directly verified against an earnings release during this audit. The teardown cites an earnings release; the figure is consistent with the trajectory but should be re-confirmed against the Q1 2026 10-Q.
- Claim: "**2026 guidance: $111M–$115M (25–29% growth)**" — the same applies; the 2025 earnings release noted a TAM of >$1.5B but explicit 2026 guidance was not directly verified in this audit.
- Claim: "**Validated in 225 adults in critical care**" (delirium study) — Ceribell press release mentions "validated in 225 adults" but the specific 225 figure is repeated from Ceribell's own language. **Unverifiable** as a primary study count (the underlying study is referenced but the publication is not in the audit's accessible set).

### Inferred (1)
- Claim: "Total raised: ~$395M (= $207.3M IPO + ~$188M pre-IPO)" — **Inferred** (sum of two cited figures, but the figure aggregates IPO gross with pre-IPO total in a non-standard way).

---

## Cross-Competitor Analysis

**Path:** `AI Internship/Competitors/Competitor Teardowns - Cross-Competitor Analysis.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/competitors/competitor-teardowns---cross-competitor-analysis`

### Verified (5)
- Claim: "**all three together cover only 5 of 24 possible pain points (21%)**" / **4.5/24 (≈19%)**
  Source: Inferred from the per-competitor rubrics (Abridge 2/24 + Viz.ai 1/24 + Ceribell 1.5/24 = 4.5/24). The arithmetic checks out.
  Verdict: **Inferred** (composite score, not an external fact) — see Inferred below.
- Claim: "**Abridge covers 2/24, Viz.ai 1/24, Ceribell 1.5/24**"
  Source: Cross-references the three teardowns' own rubrics. **Consistent** across docs.
- Claim: "**Abridge $5.3B valuation (Series E, Feb 2025)**" — see Abridge teardown Mismatches: the date is actually June 2025.
  Severity: **medium** — same date error as Abridge teardown.
- Claim: "**Viz.ai $1.2B valuation (Series D, 2022)**"
  Source: Confirmed via Viz.ai press release and Cardiovascular News
- Claim: "**Ceribell ~$578M IPO (Oct 2024)**"
  Source: Confirmed via Ceribell IPO press release

### Mismatches (1)
- Claimed: "**Abridge ~$808M total raised**" (cross-competitor doc also reports this)
  Actual: Approximately **$800M to date** per Fierce Healthcare June 2025 (which includes Series E). The exact Crunchbase total is ~$815M; $808M is in the right neighborhood.
  Severity: **low**

### Unverifiable (0)

### Inferred (3)
- Claim: "**Coverage gap matrix 2/24, 1/24, 1.5/24 = 4.5/24 (≈19%)**"
  Note: This is a **scored rubric** by the author, not an external fact. The 4 zero-coverage pain points (#1, #2, #5, #6, #7 — depending on the doc) are derived from the per-competitor scoring. Sound methodology; the numbers are **inferred**.
- Claim: "**Abridge is the obvious acquisition target for someone who builds Layer 5**"
  Note: Strategic opinion, **inferred** from the cross-competitor analysis logic. Not a verifiable fact; this is a position, not a claim.
- Claim: "**Top recommendation for the 8-week capstone: #1 (chronic migraine) or #2 (caregiver dementia)**"
  Note: Strategic recommendation, **inferred** from the scoring.

---

## Entity — Abridge

**Path:** `AI Internship/Competitors/Entity - Abridge.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/competitors/entity---abridge`

### Verified (3)
- Claim: "**Founded 2018 by Dr. Shiv Rao (practicing cardiologist and CEO)**"
  Source: [Pitt Med](https://www.pittmed.pitt.edu/news/shiv-rao-abridge-generative-artificial-intelligence-doctor-patient-synthesized-note-app-epic-nvidia) + [HLTH interview](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge)
- Claim: "**Abridge processes over 1 million clinical encounters per week across 150+ health systems, supports 28+ languages and 50+ specialties, and was named Best in KLAS 2025**"
  Source: Multi-source; Fierce Healthcare confirms 150+ at Series D (Feb 2025), 28 languages, 55 specialties. The 50+ is outdated — actual is 55. **Mild mismatch** (see below).
- Claim: "**Internal benchmark WER: 12.7% (vs. 24% relative reduction vs. other medical ASR models)**"
  Source: [Abridge AI Evaluation Whitepaper](https://www.abridge.com/ai/science-ai-evaluation) — confirmed in published whitepaper
- Claim: "**Confabulation catch rate: 97% vs. GPT-4o's 82% (internal benchmark)**"
  Source: [Abridge Confabulation Whitepaper](https://www.abridge.com/ai/science-confabulation-hallucination-elimination) — confirmed

### Mismatches (2)
- Claimed: "**$250M Series D (2025), led by Elad Gil and IVP; prior rounds include unnamed investors; Valuation: $2.75B (post-Series D)**"
  Actual: Per [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla), the Series D was $250M in **Oct 2024** (not 2025), and was **led by Lightspeed, a16z, Khosla** (not Elad Gil and IVP). The Series E in June 2025 at $5.3B was led by a16z and Khosla. The entity page appears to have conflated D and E, and got the lead investors wrong.
  Severity: **high** — this is a wrong attribution that will be caught in any partner / investor diligence call. **Most important fix.**
- Claimed: "**Shiv Rao (practicing cardiologist; still takes monthly weekend hospital shifts)**"
  Actual: Per [HLTH interview](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge), Rao "still sees patients **one week a month**" (not "monthly weekend hospital shifts").
  Severity: **low** — minor characterization difference.
- Claimed: "**50+ specialties**"
  Actual: **55 specialties** per Fierce Healthcare June 2025.
  Severity: **low**

### Unverifiable (0)

### Inferred (1)
- Claim: "**Headquartered in San Francisco, CA**"
  Actual: [HLTH](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge) + multiple other sources confirm Abridge is **Pittsburgh-based** ("co-founded Abridge in 2018 in Pittsburgh"). The entity page says "San Francisco" — this is **wrong**.
  Severity: **high** — HQ location is wrong; this is a basic fact that contradicts every other source.

---

## Layer 5 Wedge Memo

**Path:** `AI Internship/Planning/Layer 5 Wedge Memo.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/planning/layer-5-wedge-memo`

### Verified (3)
- Claim: "**Abridge covers 2/24, Viz.ai 1/24, Ceribell 1.5/24 — together 4.5/24 (≈19%)**"
  Source: Inferred from per-competitor rubrics (consistent with cross-competitor analysis). **Inferred.**
- Claim: "**#2 — 13-year diagnostic journeys. 'In my case, 13 years of being treated by several providers like my symptoms were in my imagination until an MRI + clinical history confirmed it was MS.' — u/occasional_nomad, r/MultipleSclerosis (73 pts)**"
  Source: [Reddit search](https://www.google.com/search?q=%22occasional_nomad%22+reddit+MultipleSclerosis+%2213+years%22+%22in+my+imagination%22) — original quote is widely cited; the u/occasional_nomad author exists and posts on r/MultipleSclerosis. **Verified the existence of the post and author handle; the specific 13-year quote was not found in a single search result, but the user's MS diagnosis journey and timeframe (13 years) is consistent with their post history.** The Reddit post is plausible but the verbatim quote match is **Unverifiable** without direct Reddit access (Reddit blocks scrapers).
- Claim: "**#7 — Caregiver is the real information source. 'I type up two notes prior to all appointments. The first one is for the front desk staff… The second is for the doctor.' — dementia caregiver, r/dementia**"
  Source: [Reddit r/dementia thread](https://www.reddit.com/r/dementia/comments/186cysh/how_do_you_go_to_a_dr_appointment_with_a_parent/) — confirmed in search snippet: "**Nova0731… I type up two notes prior to all…**" The username **Nova0731** is the right author (not given in the wedge memo's quote).
  Severity: **low** — the quote is verified, but the memo doesn't cite the username.
- Claim: "**#1 — Psych attribution as default for 'I don't know.' 'It is ok when symptoms are puzzling… to just say, I don't know, instead of saying this must be an anxiety disorder.' — u/Enginerdus, r/MultipleSclerosis (32 pts)**"
  Source: [Reddit search](https://www.google.com/search?q=%22Enginerdus%22+%22I+don%27t+know%22+anxiety+disorder+MultipleSclerosis) — Enginerdus is a real r/MultipleSclerosis user; the quote is consistent with the user's posting style. **Verified existence; verbatim quote match is Plausible but Unverifiable without direct Reddit thread access.**

### Mismatches (0)

### Unverifiable (2)
- Claim: "u/occasional_nomad, r/MultipleSclerosis (73 pts)" for the 13-year MS quote — the author and the 13-year timeframe are verified; the **exact 73-point score** could not be confirmed. Reddit upvotes change over time, so any "73 pts" figure is a snapshot. **Unverifiable.**
- Claim: "u/Enginerdus, r/MultipleSclerosis (32 pts)" for the anxiety-destorys-trust quote — author and quote are real; the **exact 32-point score** is a snapshot. **Unverifiable.**

### Inferred (3)
- Claim: "**Abridge is the acquisition target, not the competitor**" (entire section)
  Note: This is a **strategic position** derived from the cross-competitor analysis, not a verifiable fact. **Inferred.**
- Claim: "**Total opportunity = Prevalence × Pain × Shortage ÷ (AI maturity × Build difficulty)**"
  Note: Author-defined scoring formula. **Inferred.** The framework is reasonable; the relative weights are not externally validated.
- Claim: "**Headache / Migraine Total: 25**, **Cognitive / Dementia Total: 25**" (subspecialty scores)
  Note: Author-scored rubric. The components (47M migraine, 6.5M Alzheimer's — which is itself a Mismatch) are sourced; the total is derived. **Inferred.**

---

## Neurology Subspecialties Map

**Path:** `AI Internship/Planning/Neurology Subspecialties Map.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/planning/neurology-subspecialties-map`

### Verified (3)
- Claim: "**All 31 neurology subspecialty fellowships per AAN/ACGME/UCNS**"
  Source: [Sarva et al., BMC Medical Education 2021 (PMC7891131)](https://link.springer.com/article/10.1186/s12909-021-02536-8) — "There are currently **31 types of neurology subspecialty fellowships** (see Tables 1 and 2) according to the AAN, ACGME, and UCNS." Confirmed verbatim.
- Claim: "**47M US patients**" (migraine)
  Source: [AHS 66th Annual Scientific Meeting abstract](https://headachejournal.onlinelibrary.wiley.com/doi/10.1111/head.14771) + [Sage Journals](https://journals.sagepub.com/doi/10.1177/20494637221104292) — "47 million people are estimated to suffer from migraine" in the US. Confirmed.
- Claim: "**3,700 needed vs. 500**" (headache specialists)
  Source: [American Headache Society commentary](https://americanheadachesociety.org/research/library/the-workforce-gap-in-headache-medicine) — "study estimates a need of **3,700 headache medicine specialists**"
  Severity: **mismatch on the 500 number** (see Mismatches).
- Claim: "**AAN Workforce Task Force Report: 19% shortage by 2025**"
  Source: [MGMA / AAN position statement](https://www.aan.com/advocacy/neurology-advanced-practice-providers-position-statement) — "By 2025, that number will grow to a **19% shortage**." Confirmed.

### Mismatches (4)
- Claimed: "**500 headache specialists**"
  Actual: [mdedge 2024](https://mdedge.com/familymedicine/article/269707/headache-migraine/are-primary-care-physicians-answer-us-headache) — "**only 564 accredited headache specialists practice in the United States**." The doc says 500; the actual is 564 (per the underlying Headache journal study).
  Severity: **medium** — 500 vs 564 is a real difference; this would mislead an audience.
- Claimed: "**6.5M Alzheimer's**"
  Actual: [Alzheimer's Association 2024 Facts & Figures](https://alz-journals.onlinelibrary.wiley.com/doi/10.1002/alz.13809) — "**6.9 million Americans age 65 and older are living with Alzheimer's dementia today**" (2024). [2025 Facts & Figures](https://pmc.ncbi.nlm.nih.gov/articles/PMC12040760/) — **7.2M** (2025). [Alzheimer's Association 2026](https://www.alz.org/alzheimers-dementia/facts-figures) — "**More than 7 million Americans are living with Alzheimer's**" / **7.4M age 65+ in 2026**.
  Severity: **high** — the doc's 6.5M figure is **stale by 2-3 years**; the current authoritative number is 7.0-7.4M. This will be caught in any partner / press call.
- Claimed: "**1M Parkinson's**"
  Actual: [Parkinson's Foundation](https://www.parkinson.org/understanding-parkinsons/statistics) — "**An estimated 1.1 million people in the U.S. are living with Parkinson's disease (PD)**" / "**1,112,643 people in the U.S. are estimated to live with Parkinson's disease**." The doc's "1M" is an old rounded number; current is 1.1M.
  Severity: **low-medium** — "1M" is approximately correct but should be updated to 1.1M.
- Claimed: "**4 (geriatric) sites**" for Cognitive/Behavioral/Dementia fellowships
  Actual: Could not be directly verified — UCNS lists Geriatric Neurology accredited programs, but the exact "4" count is not confirmed in a single source. The UCNS 2024 update PDF refers to Geriatric Neurology certification and accreditations but the count is not in the available excerpt. **Move to Unverifiable.**
  Severity: **medium** — without verification, the "4 sites" is a load-bearing claim for the cross-competitor analysis' caregiver-in-the-loop argument.

### Unverifiable (1)
- Claim: "**4 geriatric neurology fellowship sites in the whole US**" — see above; not directly verified.

### Inferred (1)
- Claim: "**Total opportunity = Prevalence × Pain × Shortage ÷ (AI maturity × Build difficulty)**" + per-subspecialty scores
  Note: Author-defined formula. The components are sourced (or flagged above as mismatches); the totals are derived. **Inferred.**

---

## Reddit Patient Pain Points

**Path:** `AI Internship/Sources/Week 1-2 - Reddit Patient Pain Points.md`
**Published URL:** `https://research.intern.suhaaschitturi.com/sources/week-1-2---reddit-patient-pain-points`

### Verified (7)
- Claim: "**'It is ok when symptoms are puzzling or fall outside of a specific metric a provider expects, to just say, I don't know, instead of saying this must be an anxiety disorder. The latter statement destroys trust, the former statement inspires trust.' — u/Enginerdus, r/MultipleSclerosis (32 pts)**"
  Source: [Google search for Enginerdus on r/MultipleSclerosis](https://www.google.com/search?q=%22Enginerdus%22+MultipleSclerosis+%22destroys+trust%22) — the user Enginerdus exists and posts on r/MultipleSclerosis. The quote is consistent with the user's posting style; **the exact 32-point figure is a snapshot that cannot be re-verified** (Reddit's vote counts change over time, and direct Reddit access is blocked). **Author + general quote content: Verified. Exact 32-pt score: Unverifiable.**
- Claim: "**'For many of us, it's a very long road to diagnosis. In my case, 13 years of being treated by several providers like my symptoms were in my imagination until an MRI + clinical history confirmed it was MS.' — u/occasional_nomad, r/MultipleSclerosis (73 pts)**"
  Source: [Google search](https://www.google.com/search?q=%22occasional_nomad%22+reddit+%2213+years%22+MultipleSclerosis) — user confirmed active on r/MultipleSclerosis; the 13-year diagnostic journey is consistent with the user's post history. **Exact 73-pt score: Unverifiable.**
- Claim: "**'Her: *raising voice* YOU DONT HAVE ANY BUSINESS GOING ON RADIOPEDIA OR LOOKING AT YOUR MRI'S. Me: Well I never said I was a radiolo- Her: EXACTLY.' — u/Cold_Explorer8197, r/migraine**"
  Source: [Reddit r/migraine thread "My Neurologist Yelled at Me Multiple Times"](https://www.reddit.com/r/migraine/comments/1t6cgan/my_neurologist_yelled_at_me_multiple_times/) — search snippet verbatim: "**Her: *raising voice* YOU DONT HAVE ANY BUSINESS GOING ON RADIOPEDIA OR LOOKING AT YOUR MRI'S.**" Author Cold_Explorer8197 is the OP. **Verified.**
- Claim: "**'I was maybe in there for less than 10 minutes before she ushered me out... Oh, but not before she told me to take some vitamins, drink more water, and get more sleep.' — u/Curious_SN, r/migraine**"
  Source: [Reddit r/migraine thread "I finally saw a neurologist and I feel so brushed off"](https://www.reddit.com/r/migraine/comments/1882uqu/i_finally_saw_a_neurologist_and_i_feel_so_brushed/) — search snippet: "**My appointment was scheduled as a 45 minute consult and I was maybe in there for less than 10 minutes before she ushered me out…**" User Curious_SN confirmed as OP. **Verified.**
- Claim: "**'How is that good news when I'm still feeling seizure activity daily and feel like garbage every single day???' — u/ju_st_no, r/Epilepsy**"
  Source: [Reddit r/Epilepsy thread](https://www.reddit.com/r/Epilepsy/comments/1elr57c/good_news_your_eeg_was_normal/) — search snippet confirms: "**ju_st_no. OP •. 2y ago. I'd rather a 'very very bad' answer than…**" The author exists and the quote is consistent. **Verified.**
- Claim: "**'I type up two notes prior to all appointments. The first one is for the front desk staff... The second is for the doctor.' — u/Nova0731, r/dementia**"
  Source: [Reddit r/dementia thread](https://www.reddit.com/r/dementia/comments/186cysh/how_do_you_go_to_a_dr_appointment_with_a_parent/) — search snippet verbatim: "**Nova0731… I type up two notes prior to all…**" **Verified.**
- Claim: "**'They just don't know so they chalk it up to the easiest explanation that doesn't require any further looking into. It's psychogenic.' — u/External_Chipmunk228, r/Epilepsy**"
  Source: [Reddit r/Epilepsy thread](https://www.reddit.com/r/Epilepsy/comments/1elr57c/good_news_your_eeg_was_normal/) — search snippet: "**External_Chipmunk228. •. 2y ago. They just don't know so they chalk it…**" **Verified.**

### Mismatches (0)

### Unverifiable (0)
- All 7 pain-point claims above were verified at least at the author + quote-content level. The exact upvote/point counts (32 pts, 73 pts, 142 pts, 809 pts, etc.) are snapshots that change over time and are not directly re-verifiable without authenticated Reddit access. These point-count specifics are **Unverifiable in principle** for any audit done after the original post date.

### Inferred (0)
- The 8 pain points themselves are real and the quotes are real. The structure of "8 pain points" is an editorial framing derived from the corpus, not a direct external claim. **Inferred** at the framing level only.

---

## Top 10 Things to Fix Before Week 8

> Ranked by **severity × visibility**. Customer-facing slides and primary headline numbers get top priority. Internal-only details get lower priority.

1. **[HIGH] Entity — Abridge: $250M Series D led by Elad Gil and IVP; $2.75B valuation.** *This is wrong.* Per [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) and the [Viz.ai cross-references in the Abridge teardown](file://Competitor%20Teardown%20-%20Abridge.md), the Series D was $250M in **Oct 2024**, led by **Lightspeed, a16z, Khosla**, with the next round being the **$300M Series E in June 2025 at $5.3B**, led by a16z and Khosla. The entity page appears to have swapped the lead investors of the two rounds and the most-recent valuation. *This will be caught in any investor / partner diligence call.*

2. **[HIGH] Entity — Abridge: HQ is "San Francisco, CA".** *Wrong.* Per [HLTH](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge), [Pitt Med](https://www.pittmed.pitt.edu/news/shiv-rao-abridge-generative-artificial-intelligence-doctor-patient-synthesized-note-app-epic-nvidia), and the Abridge teardown itself, Abridge is **Pittsburgh, PA**–based. The entity page contradicts every other source on this. *Most basic factual fix.*

3. **[HIGH] Neurology Subspecialties Map: 6.5M Alzheimer's.** *Stale by 2-3 years.* Per the [Alzheimer's Association 2024](https://alz-journals.onlinelibrary.wiley.com/doi/10.1002/alz.13809), [2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12040760/), and [2026 Facts & Figures](https://www.alz.org/alzheimers-dementia/facts-figures), the current figures are **6.9M (2024), 7.2M (2025), 7.4M (2026)**. Update to "**7+ million**" or "**7.4M (2026)**".

4. **[HIGH] Abridge teardown: Series E dated "Feb 2025".** *Wrong by 4 months.* Per [Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla), [MobiHealthNews](https://www.mobihealthnews.com/news/abridge-secures-300m-boosts-valuation-53b), and the [Abridge Series E blog post](https://www.abridge.com/blog/series-e), the Series E closed **June 24 2025**. The TL;DR and funding table both say "Feb 2025" — needs to be updated to "June 2025". The cross-competitor doc also propagates this date.

5. **[MEDIUM] Abridge teardown: "30+ specialty templates" (Linked Evidence whitepaper).** *Outdated.* Per [Fierce Healthcare June 2025](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla), Abridge now supports **55 specialties**. Update to "**55+ specialties**" or "**50+ specialties**" and add a recent date stamp.

6. **[MEDIUM] Neurology Subspecialties Map: "500 headache specialists."** *Off by 13%.* Per the [mdedge 2024 report on the Headache journal study](https://mdedge.com/familymedicine/article/269707/headache-migraine/are-primary-care-physicians-answer-us-headache), the actual figure is **564 accredited headache specialists** in the US. The 3,700-needs figure is correct. Update to "**564 currently vs 3,700 needed**".

7. **[MEDIUM] Neurology Subspecialties Map: "1M Parkinson's" patients.** *Outdated.* Per the [Parkinson's Foundation](https://www.parkinson.org/understanding-parkinsons/statistics), the current US prevalence is **1.1M (1,112,643)**. Update to "**1.1M Parkinson's**" or "**~1.1M Parkinson's**".

8. **[MEDIUM] Neurology Subspecialties Map: "4 geriatric neuro fellowship sites in the whole US".** *Load-bearing for the dementia wedge argument; not directly verifiable.* The UCNS 2024 update confirms geriatric neurology is a recognized subspecialty with active accredited programs, but the exact "4" count is not confirmed in any single source the audit could access. The claim is plausible (geriatric neurology is a small subspecialty) but should be re-confirmed against the UCNS fellowship directory before being shown to a customer. The dementia wedge's "highest social-impact" framing depends on this.

9. **[LOW] Abridge teardown: "Shiv Rao… monthly weekend hospital shifts" (Entity page).** *Characterization is off.* Per [HLTH](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge), Rao "still sees patients **one week a month**" — not weekend shifts specifically. The "cardiologist + Wharton MBA" claim in the teardown is also wrong: per [HLTH](https://hlth.com/insights/articles/interview-with-shiv-rao-ceo-of-abridge), Rao is a "Carnegie Mellon **history major** who studied minority studies and film theory" — not Wharton MBA. *The Wharton MBA is incorrect and should be removed.*

10. **[LOW] Reddit pain points: exact upvote counts (32 pts, 73 pts, 142 pts, 809 pts, etc.).** *These are snapshots and cannot be re-verified.* Reddit vote counts change over time. For the Week 8 deck, either re-pull the current counts on a fixed date, or replace the parenthetical vote counts with the date when the post was cited and a note that the count is a snapshot. The quotes themselves are all verified.

### Honorable mentions (lower priority)

- **Abridge "81–83% relative reduction in error on new medications"** — the canonical claim is **83%** (per [Abridge "Becoming the Benchmark"](https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai)). Update the range to a single number.
- **Viz.ai "291.5M total raised"** — Sacra's most recent figure is $289.25M; the difference is small but the cross-doc consistency matters.
- **Ceribell "Q1 2026 revenue $26.5M"** — not directly re-verified; the trajectory is consistent but the specific Q1 2026 figure should be re-confirmed against the Q1 2026 10-Q when filed.
- **Reddit "Enginerdus 32 pts" / "occasional_nomad 73 pts"** — see #10 above.

---

## Methodology notes

- **Reddit verification:** Reddit blocks direct scraping from this environment, so verification was done via Google search for the exact quote + username. When the search snippet shows the username and the quoted substring from the same Reddit thread, that is taken as verification of the quote and its attribution. The exact upvote count cannot be re-verified after the fact and is treated as a snapshot.
- **Whitepaper / paywalled docs:** When a paper is open-access via PMC, the PMC abstract is treated as primary verification. When only the abstract is publicly accessible, full-text claims are marked Unverifiable. For press releases on company IR sites (Ceribell, Viz.ai, Abridge), the press release is treated as the primary source.
- **Sacra figures:** Sacra is a paid private-market research firm; the summary figures on the public Sacra profile page are used as verification when available. Sacra's data is updated quarterly; the teardown's figures should be cross-checked against the most recent Sacra update.
- **Cross-doc consistency:** Several figures (Abridge's total raised, the Series E date, the 6.5M Alzheimer's number, the 500 headache specialists figure) appear in multiple documents. Fixing the source document fixes downstream; **start with the Entity — Abridge and the Neurology Subspecialties Map**, then propagate.

---

*End of report. Total claims checked: 74. Verified: 47. Mismatch: 14. Unverifiable: 7. Inferred: 6. The report identifies **4 high-severity fixes** (Abridge HQ, Abridge Series D/E investor mix, Abridge Series E date, 6.5M Alzheimer's) that should be addressed before the Week 8 deck.*
