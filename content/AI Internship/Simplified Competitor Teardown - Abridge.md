#capstone #ai-internship #neurology #competitor

---

# Abridge — Simplified Competitor Teardown

---

## What Abridge Actually Is

Abridge sits in the room with the doctor and patient, records the conversation, and writes the clinical note. That's it. It's a scribe — a very good one.

The doctor opens the app on their phone, the patient consents verbally, and Abridge generates a structured note (SOAP, H&P, neuro H&P, whatever the specialty needs)[^1] with every sentence traceable back to the audio via its "Linked Evidence" feature. The note drops into Epic (deepest), Cerner, or athenahealth via SMART-on-FHIR.[^2]

Founded 2018 by Dr. Shiv Rao — a cardiologist who left UPMC to build this. Pittsburgh-based. Raised ~$800M,[^3] most recently $300M Series E at $5.3B (Feb 2025). Deployed at 300+ health systems including Mayo, Cleveland Clinic, Stanford, UPMC, Emory, Yale, and all six UC medical centers. The only ambient AI scribe with a peer-reviewed JAMA Network Open[^4] study. Back-to-back Best in KLAS[^5] (2025 and 2026).

---

## The Numbers That Matter

**Money:**
- ~$800M raised total[^3]
- Series E: $300M at $5.3B (Feb 2025) — just four months after a $250M Series D
- Estimated pricing: $250–$400/provider/month (third-party estimates; Abridge doesn't publish prices)

**Scale:**
- 300+ health systems
- 1M+ encounters processed per week (per whitepaper)
- 28+ languages[^6]

**Clinical outcomes:**
- Physician burnout dropped from **51.9% → 38.8%** in 30 days — measured using the Mini-Z burnout scale[^7] (JAMA Network Open, 263 clinicians across 6 health systems, Oct 2025)
- ~10.8 minutes saved per workday
- 81% of clinicians said documentation got easier; 73% spent less time documenting after hours[^8] (KUMC study, 181 clinicians, JAMIA Open)[^9]
- 4.3/5 star rating in English, 4.1/5 Spanish, 4.4/5 Japanese (tens of thousands of ratings, May–Jul 2025)

**Technical benchmarks (internal, from Abridge whitepapers):**
- WER[^10]: 12.7% — 24% better than other medical ASR[^11] models
- Medical Term Recall (MTR): 97%
- Confabulation catch rate: **97%** (vs. GPT-4o at 82% — off-the-shelf models miss ~6× more)

---

## What It Does Well

**The core product is strong:**

1. **Ambient capture** — records the visit, handles patient consent, works on iOS/Android
2. **Multi-speaker separation** — patient, doctor, family members, interpreters all labeled
3. **Linked Evidence** — the trademarked feature: click any sentence in the note, see the exact audio clip and transcript snippet that produced it. This is their main trust-builder with clinicians
4. **Specialty depth** — 30+ specialty templates including neuro, cardiology, primary care, discharge summary
5. **EHR write-back** — drops notes directly into Epic[^12] (deepest), Cerner/Oracle, athena via SMART-on-FHIR[^2]
6. **Speed** — median note generation dropped from 76 sec (mid-2023) to 38 sec (mid-2024)[^13]
7. **Multilingual** — 28+ languages; Spanish, Mandarin, Japanese, Arabic, etc.
8. **No FDA clearance needed** — positioned as documentation software, not clinical decision support. They ship fast[^14]

---

## The Real Gaps — Where Abridge Leaves Space

This is the important part. Abridge is dominant in what it does. But here's what it doesn't do:

**Gap 1 — The doctor still walks into the room cold**
Abridge sees the conversation. It does not see the chart. The doctor still has to read the prior visits, the last neurology note, the imaging results from six months ago. No longitudinal synthesis.

**Gap 2 — No pre-visit briefing**
Nothing surfaces what happened in the last three visits, what was ruled out, what the top question is for today. The doctor gets no briefing before the room.

**Gap 3 — No between-visit data**
No wearables. No symptom logs. No Apple Watch seizure data, no StrivePD for Parkinson's, no EpiMonitor epilepsy data. Abridge only knows what happened inside the room.

**Gap 4 — No caregiver channel**
For dementia, stroke recovery, pediatric neurology, ALS — the caregiver is often the primary information source. Abridge has no mechanism for caregivers to contribute. No intake form, no consent flow, no HIPAA-compliant caregiver portal.

**Gap 5 — The patient never sees the note**
There's no patient-facing view. No way for patients to read, correct, or add to what was documented. The note is between the doctor and the system.

**Gap 6 — No structured chronic-disease scoring**
No automatic UPDRS[^15] (Parkinson's), no EDSS[^16] (MS), no MIDAS[^17] (migraine), no seizure calendar tracking. The longitudinal progression of a chronic neurological condition is invisible to Abridge.

---

## The 8-Point Patient Pain Point Score

*(How well does Abridge address the 8 patient pain points from the research corpus?)*

| # | Pain Point | Abridge Covers It? |
|---|---|---|
| 1 | Doctor dismisses symptoms as anxiety | **No** — sees only today's room, not the history |
| 2 | 13-year diagnostic journey | **No** — per-visit note only, no longitudinal summary |
| 3 | 10-minute appointments | **Partial** — saves 10 min/day, not per encounter |
| 4 | Doctor says EEG was "normal" when it isn't | **No** — no ambiguous-result flagging or patient translation |
| 5 | Patients punished for self-advocacy | **No** — patient never sees the note |
| 6 | Doctor doesn't see between-visit data | **No** — only in-room audio |
| 7 | Caregivers are the real info source | **No** — no caregiver role at all |
| 8 | Medical education gaps (referrals, guidelines) | **Partial** — specialty templates help, no guideline alerts |

**Score: 0 full / 2 partial / 6 no. Abridge covers roughly 8% of the patient pain points.**

This is a clean signal. The entire gap maps to one unoccupied layer: **the pre-visit synthesis**.

---

## What This Means For Us

Abridge owns the in-room documentation layer. It is the best-in-class incumbent and is not going away. The switching cost once a health system deploys Abridge — dot-phrase[^18] library, EHR integration, clinician habits, JAMA publications as sales collateral — is very high.

The open space is **before the room**. The pre-visit briefing: pulling the chart, the imaging, the wearables, the caregiver intake, the between-visit symptom logs, and synthesizing all of it into one structured briefing the doctor sees before walking in.

Nobody owns that layer. Not Abridge. Not DeepScribe. Not Nuance DAX. Not Suki. Not any of the 16 competitors in the landscape.

**Our wedge: pre-visit synthesis. Caregiver-in-the-loop. Longitudinal chronic-disease tracking.**

The three strongest openings:
- **Dementia / caregivers** — no competitor has a caregiver intake + synthesis layer
- **Epilepsy wearables** — EpiMonitor, Apple Watch seizure data, between-seizure logs
- **Headache / migraine** — longitudinal MIDAS[^17] score tracking, trigger identification, pre-visit migraine diary synthesis

---

## The One Nuance Worth Knowing

Abridge's 2026 STAT News article reported scribes save clinicians **under 1 minute per clinical note** in some studies. A separate study (1,800 clinicians, 5 academic medical centers, 2023–2025) found more meaningful savings: 16 minutes per 8-hour shift. Even so — the real value may be less about time savings and more about burnout reduction. The Mini-Z burnout numbers[^7] (51.9% → 38.8%) are the most clinically meaningful data point.

---

## Bottom Line

| | |
|---|---|
| **What Abridge is** | Best-in-class ambient scribe, in-room only |
| **What it's not** | Pre-visit synthesis, longitudinal tracker, caregiver tool |
| **Threat to us** | Low — different layer entirely |
| **Opportunity** | Own the pre-visit briefing layer that Abridge doesn't touch |

---

## Key Sources

- [jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542) — Olson et al., JAMA Network Open, Oct 2025
- [pmc.ncbi.nlm.nih.gov/articles/PMC11843214/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/) — Tierney et al., KUMC, JAMIA Open, Feb 2025
- [statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/](https://www.statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/) — STAT News, Apr 2026
- [news.crunchbase.com/health-wellness-biotech/ai-doctor-note-taking-startup-abridge/](https://news.crunchbase.com/health-wellness-biotech/ai-doctor-note-taking-startup-abridge/) — funding history
- [fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla](https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla) — Series E
- [abridge.com](https://www.abridge.com/) — company homepage
- [[Source - Abridge AI Evaluation Whitepaper]]
- [[Source - Abridge Confabulation Elimination Whitepaper]]
- [[Source - Becker's Abridge Profile]]
- [[Source - Trelis Medical ASR Benchmarks]]

---

## Footnotes

[^1]: **SOAP, H&P, neuro H&P** — Standard clinical note formats. SOAP = Subjective, Objective, Assessment, Plan (the most common US clinical note structure). H&P = History and Physical (admission note format). Neuro H&P = neurology-specific H&P with neurological exam components. Abridge supports 30+ specialty templates.

[^2]: **SMART-on-FHIR** — An open interoperability standard that lets third-party healthcare apps read from and write to electronic health record systems. SMART creates an app-store model for EHRs; FHIR is the data format standard (Fast Healthcare Interoperability Resources). Abridge uses SMART-on-FHIR to read patient schedules and write clinical notes back into Epic, Cerner, and athenahealth. See [[Concept - SMART-on-FHIR]].

[^3]: **~$800M total raised** — Per FierceHealthcare (Jun 2025): "The company has raised approximately $800 million to date." The doc previously said ~$808M; the primary source uses ~$800M, so that is the correct figure.

[^4]: **JAMA Network Open** — A peer-reviewed, open-access medical journal published by the American Medical Association (AMA). High-impact (JAMA family ~20+ impact factor). The Olson et al. study here is notable as the only peer-reviewed, multi-health-system study showing statistically significant burnout reduction from an ambient AI scribe. Note: one co-author (Tina Shah) is an Abridge employee — disclosed transparently. See [[Concept - JAMA Network Open]].

[^5]: **KLAS / Best in KLAS** — KLAS Research is an independent healthcare IT rating firm that collects provider-submitted performance data on software vendors. Their annual "Best in KLAS" awards are widely used in healthcare IT purchasing. Abridge won Best in KLAS for Ambient AI in both 2025 and 2026. See [[Concept - KLAS]].

[^6]: **28+ languages** — Abridge supports 28 languages including English, Spanish, Mandarin (Cantonese + Mandarin), Japanese, Italian, Tagalog, Vietnamese, Arabic, French, Korean, Russian, German, Haitian Creole, Bulgarian, Catalan, Czech, Danish, Dutch, Finnish, Hindi, Hungarian, Indonesian, Polish, Portuguese, Romanian, Turkish, and Ukrainian (per the AI Evaluation whitepaper).

[^7]: **Mini-Z burnout scale** — The Mini-Z is a single-question validated physician burnout assessment tool developed by the AMA and Mayo Clinic. A score of 3+ on the 5-point scale indicates burnout. The Olson et al. study used Mini-Z as the primary burnout measurement, reporting pre-implementation 51.9% burnout (Mini-Z ≥3) dropping to 38.8% at 30 days — OR 0.26, P<.001. See [[Concept - Mini-Z Burnout Scale]].

[^8]: **KUMC percentages — methodology note** — The 81%, 77%, 73%, 67%, 64% figures come from the post-implementation survey only (percentage of respondents who agreed/strongly agreed after using Abridge), not statistically computed pre/post comparisons. The Tierney et al. study was a quality improvement initiative with non-identical pre/post surveys — only 2 items were directly comparable. These figures should be read as satisfaction/direction rates, not measured changes. See [[AI Internship/Concept - KUMC]] and [[Concept - JAMIA Open]].

[^9]: **KUMC (University of Kansas Medical Center)** — The University of Kansas Medical Center, based in Kansas City, KS. One of the earliest Abridge adopters in the US; conducted the Tierney et al. quality improvement study. A credible academic source, though the study was a single-institution quality improvement initiative, not an RCT. See [[AI Internship/Concept - KUMC]].

[^10]: **WER (Word Error Rate)** — The standard metric for ASR accuracy. The percentage of words incorrectly transcribed. Lower is better. WER = (Substitutions + Deletions + Insertions) / Total Words. Abridge reports 12.7% WER on their internal medical benchmark — meaning roughly 1 in 8 words is wrong. The 24% relative reduction means Abridge is 24% better than other medical ASR systems tested. See [[Concept - WER]].

[^11]: **ASR (Automatic Speech Recognition)** — The technology that converts spoken audio into written text. Medical ASR is fine-tuned on clinical vocabulary (drug names, disease names, procedures), accented English, multi-speaker conversations, and clinical noise environments. Standard consumer ASR performs poorly on medical conversations. Abridge uses a custom medical ASR pipeline fine-tuned on Whisper-class architecture. See [[Concept - ASR]].

[^12]: **Epic** — The dominant US hospital EHR system (~30–40% hospital market share). Abridge's deepest integration. Epic integration via SMART-on-FHIR allows Abridge to read patient schedules and write notes directly into Epic. This deep integration is a significant switching cost — once a health system builds its dot-phrase library and training around Abridge in Epic, moving to a competitor requires rebuilding all of that. See [[Concept - Epic]].

[^13]: **76 sec → 38 sec note generation** — Confirmed in the Tierney et al. KUMC paper: "median draft note generation time at our institution was 76 seconds in July 2023 and improved to 38 seconds by April 2024." This is KUMC-specific data, not Abridge's company-wide average.

[^14]: **No FDA clearance** — Abridge is regulated as clinical documentation software, not a medical device or clinical decision support (CDS) tool. FDA regulates CDS software that supports clinical decisions; administrative documentation tools are outside FDA's scope. This allows Abridge to ship features faster than if it were an FDA-cleared device. Competitors building diagnostic or treatment-support features may require FDA clearance.

[^15]: **UPDRS (Unified Parkinson's Disease Rating Scale)** — The gold-standard clinical assessment for Parkinson's disease severity. Covers motor function, activities of daily living, and complications. Administered by a neurologist at each visit. A pre-visit synthesis tool could track UPDRS scores longitudinally and surface disease progression. Abridge does not administer or track UPDRS scores. See [[Concept - UPDRS]].

[^16]: **EDSS (Expanded Disability Status Scale)** — The gold-standard disability measurement for multiple sclerosis (MS), scored 0–10. Tracks neurological impairment across 8 functional systems. Abridge does not track EDSS scores longitudinally. See [[Concept - EDSS]].

[^17]: **MIDAS (Migraine Disability Assessment)** — A patient-reported questionnaire scoring migraine disability over 3 months (Grade I–IV). MIDAS tracks headache frequency and disability; a pre-visit synthesis tool could administer this automatically before the visit and track trajectory. Abridge does not administer or track MIDAS scores. See [[Concept - MIDAS]].

[^18]: **Dot-phrase** — A text shortcut in an EHR that expands into a longer pre-formatted clinical text block. For example, typing `.hpisec` pulls in the History of Present Illness section. Each health system customizes its dot-phrase library; Abridge's note sections map to specific dot-phrases. Once a physician's dot-phrase library is built around Abridge's section structure, switching vendors requires rebuilding the entire library — a significant switching cost. See [[Concept - Dot-Phrase]].

---

*Related: [[Competitor Teardown - Viz.ai]] · [[Competitor Teardown - Ceribell]] · [[Competitor Teardowns - Cross-Competitor Analysis]]*
