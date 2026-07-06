#capstone #ai-internship #neurology #competitor #deep-dive #scribe
Related: [[Competitor Deep-Dive Framework]] · [[Week 1 - Neurology Research]] · [[Competitor Teardown - Viz.ai]] · [[Competitor Teardown - Ceribell]]

# Competitor Teardown — Abridge

> **Capstone neurology AI landscape teardown — Abridge (AI medical scribe)**
> Audience: capstone team building the Week 8 AI-in-healthcare landscape map.
> Date: July 2026. Framework: 4-step structured teardown. All quotes verbatim from primary sources.

---

## TL;DR (60-second read)

Abridge is the **most-validated AI medical scribe in the US** — ambient audio → structured clinical note, with deep Epic integration and the trademarked "Linked Evidence" feature that ties every AI-drafted claim to the source transcript. Pittsburgh-based; founded 2018 by Shiv Rao (cardiologist + Wharton MBA). 2025 + 2026 Best in KLAS for ambient AI. **$300M Series E at $5.3B valuation (Feb 2025)**, four months after a $250M Series D. 300+ health systems (including Mayo, Cleveland Clinic, UPMC, Stanford). 

Pricing is enterprise-only, $208–$800/provider/mo per multiple third-party estimates. The JAMA Network Open 6-health-system study (Olson et al., Oct 2025) showed burnout dropped from 51.9% → 38.8% in 30 days — the strongest published clinical evidence for any ambient scribe. 

**What Abridge does NOT own:** the longitudinal pre-visit synthesis (chart + imaging + signals + transcript), caregivers as an information source, between-visit patient data, and the structured chronic-disease scoring layer (UPDRS, EDSS, MIDAS, seizure calendar). The 8-pain-point score: 4 partial, 4 no — the cleanest possible confirmation of the capstone thesis.

---

## Section 1 — Surface scan

### 1.1 One-paragraph company summary

Abridge is the Pittsburgh, PA–based, generative-AI clinical documentation company founded in **2018** by Dr. Shiv Rao, a cardiologist with a Wharton MBA who left UPMC's cardiology practice to build it. The product is an ambient AI scribe: the doctor opens the Abridge app on a phone (iPhone first, Android added 2023), records the patient encounter, and Abridge's LLM stack generates a structured specialty note (SOAP, H&P, neuro H&P, etc.) with timestamped attribution back to the source audio via its "Linked Evidence" feature. The note writes into Epic (deepest integration), Cerner/Oracle Health, and athenahealth via SMART-on-FHIR. Median note generation time has dropped from 76 sec (Jul 2023) to 38 sec (Apr 2024). Abridge is the **2025 and 2026 Best in KLAS winner for ambient AI** (per homepage) and the only ambient AI scribe with a peer-reviewed JAMA Network Open study (Olson et al., Oct 2025, n=263 across 6 health systems). The company is deployed at **300+ health systems** including Mayo Clinic, Cleveland Clinic, UPMC, Stanford, Emory, Yale, and the entire University of California system. Raised **~$808M total** across 5+ rounds: $5M seed → $15M Series A → $40M Series B → $150M Series C (Feb 2024) → $250M Series D (Oct 2024) → $300M Series E (Feb 2025) at a **$5.3B valuation**, led by a16z and Khosla Ventures. Headcount estimated 400+ (LinkedIn).

> Verbatim homepage (https://www.abridge.com/): *"Abridge is recognized as a market leader in ambient AI and earned the 2025 and 2026 Best in KLAS award."*
> Verbatim homepage tagline: *"One intelligence layer connecting health systems, payers, and life sciences organizations. Built by clinicians, for clinicians—trusted by 300+ health systems."*

### 1.2 Headline features list

1. **Ambient clinical conversation capture** — iPhone/iPad/Android app, secure recording with patient consent
2. **Multi-speaker diarization** — separates patient, physician, family members, interpreters
3. **Specialty note generation** — SOAP, H&P, neuro, cardiology, primary care, discharge summary, etc. Per Linked Evidence whitepaper, Abridge supports 30+ specialty templates
4. **"Linked Evidence"** — trademarked feature: highlight any sentence in the AI-drafted note → see + hear the source transcript segment that produced it. Per Abridge's own docs: *"Linked Evidence helps you view the origin of particular AI summaries so you can see the source of truth."* (https://support.abridge.com/hc/en-us/articles/30235128433811-Verify-a-Note-With-Linked-Evidence)
5. **Multilingual** — 15+ languages including Spanish, Mandarin, Portuguese, Arabic
6. **EHR write-back** — bi-directional Epic, Cerner/Oracle, athena via SMART-on-FHIR + ambient dictation
7. **Dot-phrase / smart-phrase integration** — `.hpisec` etc. pull note sections into EHR templates
8. **AI prior-auth / coding suggestions** — suggests E&M level and ICD-10/SNOMED codes from the encounter
9. **Payer and life-sciences intelligence layer** — newer, leverages the same conversation data for downstream use cases

### 1.3 Pricing model

**No public pricing.** Abridge publishes no per-provider number. The model is enterprise SaaS, per-provider subscription, annual contract, scaled by number of providers, health-system size, and which modules are licensed.

**Third-party pricing estimates (snippet only, not official):**
- **Marvix AI review (2026):** *"Reported enterprise estimates commonly range from roughly $200–$800/provider/month."* — https://www.marvix.ai/blog/abridge-pricing-review
- **DeepCura review (2026):** *"Enterprise license: approximately $2,500 per clinician per year (~$208/month); Full implementation: $250-$500 per provider per month, depending on volume."* — https://www.deepcura.com/resources/abridge-ai-review
- **VeroScribe review (2026):** *"Abridge ... Not published (enterprise only) ... Annual Cost per Provider, ~$2,500–$7,200+ per year."* — https://www.veroscribe.com/blog/abridge-review-2026
- **OrbDoc pricing guide (2025):** *"Abridge: Enterprise pricing only"* (https://orbdoc.com/learn/ai-medical-scribe-pricing-guide)

**Conservative estimate: $250–$400/provider/month for typical enterprise deployment, with volume discounts at 1,000+ providers.** The $800 ceiling per Marvix likely includes implementation, training, and add-on modules (coding, prior auth).

### 1.4 Funding to date

| Round | Date | Amount | Valuation | Lead |
|---|---|---|---|---|
| Seed | 2019 | $5M | — | UPMC Enterprises |
| Series A | 2021 | $15M | — | |
| Series B | 2022 | $40M | — | |
| Series C | Feb 2024 | $150M | — | Lightspeed |
| Series D | Oct 2024 | $250M | ~$2.5B | Lightspeed, a16z, Khosla |
| **Series E** | **Feb 2025** | **$300M** | **$5.3B** | **a16z, Khosla** |

**Total raised: ~$808M** (per Crunchbase aggregate, https://news.crunchbase.com/health-wellness-biotech/ai-doctor-note-taking-startup-abridge/)

### 1.4b Key Technical Benchmarks (from Abridge Whitepapers, 2024–2025)

The following data comes from two Abridge whitepapers published in 2024–2025 — [[Source - Abridge AI Evaluation Whitepaper]] and [[Source - Abridge Confabulation Elimination Whitepaper]].

**ASR Performance:**
- Internal medical benchmark WER: **12.7%**
- **24% relative reduction** in WER vs. other medical ASR models (internal benchmark)
- **81–83% relative reduction** in error on new medications vs. off-the-shelf models
- Medical Term Recall (MTR): **97%** (internal benchmark)
- On generic Librispeech benchmark: comparable to Whisper v3 (OpenAI)
- Spanish WER: 3.1% vs. 6.2% English

**Confabulation Elimination (from [[Source - Abridge Confabulation Elimination Whitepaper]], Aug 2025):**
- Abridge proprietary guardrail model: **97% confabulation catch rate**
- GPT-4o (off-the-shelf): **82% confabulation catch rate** (internal benchmark)
- Implication: GPT-4o misses ~6× as many confabulations as Abridge's system
- Training corpus: **50,000+ examples** (open-source hallucination detection + domain-specific clinical scenarios)
- Physician validation: **1,000+ hours** of annotation by board-certified physicians
- Internal benchmark dataset: **10,000+ realistic clinical encounters** with annotated unsupported claims

**Post-Deployment Quality Metrics (May–July 2025, from [[Source - Abridge AI Evaluation Whitepaper]]):**
- Average star rating, English encounters: **4.3/5** (tens of thousands of ratings)
- Spanish encounters: **4.1/5** (improved from 3.7 in February)
- Japanese: **4.4/5**
- Non-English medical term recall: >80% of English recall rate
- Languages with published ratings: English, Spanish, Mandarin (Cantonese + Mandarin), Japanese, Italian, Tagalog, Vietnamese, Arabic, French, Korean, Russian, German, Haitian Creole (28+ total)

**Note Evaluation Framework:**
- 4-stage pipeline: automated metrics → clinician spot-checks → blinded head-to-head trials → staged release → ongoing post-deploy monitoring
- Linked Evidence: every claim in the generated note links to source transcript excerpt (clinician verification)
- Edit-rate tracking: passive signal from clinician edits to AI-drafted notes before EHR signing

Sources:
- [[Source - Abridge AI Evaluation Whitepaper]] (Sept 2024, updated Aug 2025)
- [[Source - Abridge Confabulation Elimination Whitepaper]] (Aug 2025)
- https://news.crunchbase.com/health-wellness-biotech/ai-doctor-note-taking-startup-abridge/
- https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla
- https://www.abridge.com/press-release/series-c-150

### 1.5 Customer base

Per homepage: **300+ health systems**, including (publicly named):
- **Mayo Clinic**
- **Cleveland Clinic**
- **UPMC** (founding partner)
- **Stanford Health Care**
- **Yale New Haven Health**
- **Emory Healthcare**
- **University of California Health** (all 6 academic medical centers)
- **UCHealth**
- **University of Chicago Medicine**
- **Tenet Healthcare**
- **Memorial Hermann**
- **Baptist Health** (KY)
- **Kaiser Permanente** (pilot)

**KUMC (University of Kansas Medical Center)** study: 181 clinicians enrolled, 133 active users, 30 specialties covered (per https://www.abridge.com/blog/kumc-research-studies)

### 1.6 Customer quotes (verbatim)

1. **Abridge homepage (https://www.abridge.com/) — featured customer testimonial:**
   > *"Abridge has fundamentally changed the way I practice medicine. It captures the conversation in a way that's deeply meaningful, and the linked evidence means I trust the note."*

2. **JAMIA Open / KUMC study (Tierney et al., 2025, https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/) — survey post-implementation:**
   - 81% said documentation workflow was easier
   - 77% said it improved patient care through decreased documentation burden
   - 73% said it decreased time spent documenting outside clinical hours
   - 67% said it reduced risk for burnout due to documentation
   - 64% said it increased satisfaction at work

3. **JAMA Network Open / 6 health system study (Olson et al., Oct 2025, https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542):**
   - Pre-implementation burnout: 51.9% (Mini-Z ≥3)
   - 30-day post-implementation burnout: 38.8%
   - 74% lower adjusted odds of burnout (OR 0.26, 95% CI 0.13–0.54, P<.001)
   - ~10.8 minutes saved per workday
   - Neurologist/psychiatrist subgroup: 5.3% of sample, directionally same

4. **Abridge "Pioneering the Science of AI Evaluation" whitepaper (https://www.abridge.com/ai/science-ai-evaluation):**
   > *"We measure performance across the dimensions that matter: correctness, completeness, clinical reasoning, and traceability."*

5. **Abridge "Becoming the Benchmark for Healthcare AI" (https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai):**
   - 24% relative reduction in word error rate on clinical conversations
   - 15% relative improvement in transcription accuracy for accented English

6. **Abridge Linked Evidence docs (https://support.abridge.com/hc/en-us/articles/30235128433811-Verify-a-Note-With-Linked-Evidence):**
   > *"Linked Evidence helps you view the origin of particular AI summaries so you can see the source of truth. When you highlight the relevant auto-generated summary, Abridge displays the corresponding transcript segment and audio clip."*

---

## Section 2 — What they compute

### 2.1 Architecture diagram (text)

```
┌─────────────────────────────────────────────────────────────┐
│  Patient + Clinician Conversation (audio)                   │
└────────────────────────┬────────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────┐
│  Mobile App (iOS / Android) — secure recording              │
│  Patient consent flow (verbal, captured in transcript)      │
└────────────────────────┬────────────────────────────────────┘
                         │  audio upload (HIPAA, encrypted)
                         ▼
┌─────────────────────────────────────────────────────────────┐
│  Abridge Cloud (AWS, HIPAA-compliant)                        │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  Speech recognition (custom ASR, fine-tuned for        │  │
│  │  medical vocab; uses Whisper-class foundation model)   │  │
│  └─────────────────────────┬─────────────────────────────┘  │
│                            ▼                                 │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  Speaker diarization (patient / clinician / family /  │  │
│  │  interpreter)                                         │  │
│  └─────────────────────────┬─────────────────────────────┘  │
│                            ▼                                 │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  LLM layer (multi-model: OpenAI, Anthropic, and       │  │
│  │  proprietary fine-tunes for medical reasoning)        │  │
│  │  - Specialty prompt templates                         │  │
│  │  - Note structure generation (SOAP, H&P, etc.)        │  │
│  │  - ICD-10 / E&M level suggestion                      │  │
│  └─────────────────────────┬─────────────────────────────┘  │
│                            ▼                                 │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  Linked Evidence linker                               │  │
│  │  (every generated sentence → source transcript seg)  │  │
│  └─────────────────────────┬─────────────────────────────┘  │
│                            ▼                                 │
│  ┌───────────────────────────────────────────────────────┐  │
│  │  EHR write-back (SMART-on-FHIR)                       │  │
│  │  Epic / Cerner / athena + dot-phrase injection        │  │
│  └───────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

### 2.2 Per-feature I/O table

| Feature | Input | Compute | Output | Latency | Accuracy (published) |
|---|---|---|---|---|---|
| Ambient audio capture | iOS/Android mic, patient consent | Custom ASR pipeline (Whisper-class) | Timestamped transcript w/ speaker labels | Real-time (transcript) + ~38s (note) | 24% rel. WERR reduction; 15% rel. improvement accented English |
| Note generation | Transcript + specialty template | Multi-model LLM (OpenAI + Anthropic + proprietary) | SOAP/H&P/specialty note | Median 38s (Apr 2024, down from 76s Jul 2023) | KUMC: 81% "easier" workflow; 77% "improved care" |
| Linked Evidence | Generated note + transcript | Sentence-segment alignment | Click-to-source transcript + audio | Instant | Not published as %; Abridge claims it is the "source of truth" |
| Multilingual | Audio in 15+ languages | Multilingual ASR + LLM | Translated + structured note | Same as English | Not published in detail |
| E&M / coding suggestion | Note + transcript | Specialty-specific LLM | E&M level + ICD-10/SNOMED codes | Near-real-time | Not published as %; reduces under-coding (claim) |
| EHR write-back | Final note | SMART-on-FHIR | Note text in EHR note field | Real-time | Not applicable |
| Payer intelligence (newer) | De-identified conversation data | Aggregation LLM | Risk stratification, quality metrics | Batch | Not yet published |

### 2.3 Published evaluations (with verbatim accuracy numbers)

| Study | Year | Sample | Finding | URL |
|---|---|---|---|---|
| Olson et al. (JAMA Network Open, 6 health systems) | Oct 2025 | 263 ambulatory clinicians, 30 days | **Burnout 51.9% → 38.8%** (74% lower adjusted odds). ~10.8 min saved per workday. | https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542 |
| Tierney et al. (JAMIA Open, KUMC) | Feb 2025 | 181 clinicians, 99 post-impl. | **81% said documentation easier; 77% said improved care; 73% said less after-hours work.** | https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/ |
| Abridge "Becoming the Benchmark" | 2024 | Internal eval | **24% relative reduction in WER on clinical conversations; 15% relative improvement on accented English** | https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai |
| Abridge "Pioneering the Science of AI Evaluation" | 2024 | Whitepaper | Correctness, completeness, clinical reasoning, traceability dimensions | https://www.abridge.com/ai/science-ai-evaluation |
| STAT News review | 2026 | Multiple studies | Modest time savings (under 1 min/note in some studies) | https://www.statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/ |

### 2.4 FDA clearances

**Abridge is NOT an FDA-cleared medical device.** It is sold as a "clinical documentation tool" not subject to FDA review (per Abridge's own positioning and multiple KLAS assessments). It generates administrative notes, not clinical decisions. The Linked Evidence feature is positioned as a "traceability" tool for audit, not as a diagnostic aid.

This is a regulatory moat: Abridge can ship features without FDA submission. The Layer 5 pre-visit synthesis wedge may or may not require FDA clearance depending on how the system is positioned.

---

## Section 3 — Pricing & go-to-market

### 3.1 Pricing model summary

| Element | Detail |
|---|---|
| List price | Not public |
| Model | Per-provider subscription, annual contract |
| Estimated range (third-party) | $208–$800/provider/mo |
| Volume discounts | Yes (health-system level, undisclosed) |
| Implementation fee | Often bundled; Marvix suggests $250–$500/provider/mo for full implementation |
| Onboarding | 30–90 days for enterprise |
| Switching costs | HIGH (EHR integration, dot-phrase library, clinician habit) |
| Net revenue retention | Not disclosed |

### 3.2 Sales motion

**Top-down (enterprise sale):** Abridge's GTM is health-system-level. The sales team is organized around IDNs (integrated delivery networks), academic medical centers, and large community health systems. Sales cycle: 6–18 months. Typical buyer: CMIO, CIO, CEO, or designated AI governance committee.

**Champions:** Physicians who adopt first and become internal advocates. Abridge leverages the KUMC + 6-system JAMA publications as enterprise sales collateral.

**Recent pricing/contract signals:**
- Multiple KLAS awards (2025, 2026) drive inbound demand
- Series E ($300M, Feb 2025) at $5.3B valuation signals investor confidence in continued enterprise expansion
- Series E press release (Fierce Healthcare) framed as "scale to meet accelerating demand from health systems"

Sources:
- https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla
- https://www.abridge.com/

### 3.3 Onboarding time

- **Initial pilot (5–20 providers):** 30–60 days
- **Health-system rollout (100+ providers):** 90–180 days (includes EHR integration, dot-phrase library, training)
- **Enterprise-wide (1,000+ providers):** 6–12 months

### 3.4 Switching costs

**Very high.** Once a hospital builds:
- A dot-phrase library mapped to Abridge's output sections
- Clinician habits around reviewing/editing AI-drafted notes
- An EHR integration with the SMART-on-FHIR write-back
- A governance process for ambient AI in the chart

...the cost to switch to a competitor (DeepScribe, Nuance DAX, Suki, Freed, etc.) is non-trivial. Abridge's KLAS awards + JAMA publication make the switching argument harder.

### 3.5 Recent press on pricing or business model

- **Feb 2025 Series E:** $300M at $5.3B valuation, led by a16z and Khosla. Public framing: "scale to meet accelerating demand." (https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla)
- **No public pricing changes announced.**
- **STAT News (Apr 2026):** Reported that "scribes saved clinicians under 1 minute per clinical note" in some studies, suggesting real-world value capture is below the marketing — this could pressure pricing. (https://www.statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/)

---

## Section 4 — Gap analysis (8 patient pain points)

The 8 pain points are from the patient-research corpus in `Week 1-2 - Reddit Patient Pain Points.md`.

| # | Pain point | Coverage | How Abridge addresses it | What's missing |
|---|---|---|---|---|
| 1 | Doctors attribute symptoms to anxiety/psych rather than "I don't know" | **No** | None — Abridge captures the conversation, not the longitudinal chart. The doctor still has to remember the patient's history before walking in. | No pre-visit synthesis of the patient's prior workup, prior specialists seen, prior "anxiety" labels applied. The doctor walks in cold on the prior chart. |
| 2 | 13-year diagnostic journeys | **No** | None — Abridge doesn't summarize the longitudinal record. The note is per-encounter only. | No "this patient has been worked up for X, Y, Z over 13 years; here's what was ruled out and what's still on the table." The "I don't know" verdict isn't supported with a structured longitudinal view. |
| 3 | 10-minute appointments, no listening | **Partial** | The scribe frees the doctor from typing, so they can theoretically look at the patient. The JAMA 6-system study showed 10.8 min saved per workday, not per encounter. | The encounter is still 10 minutes. The scribe doesn't surface "what you didn't get to in the last 3 visits" or "what's the top 1 question to ask today." |
| 4 | Dismissive comments on ambiguous test results ("good news your EEG was normal!") | **No** | None — Abridge doesn't translate test results into patient-friendly language or pre-flag ambiguous results. | No "this EEG is normal but the patient has been seizing daily; the literature says 50% of routine EEGs miss focal seizures, consider a 24-hour ambulatory EEG" alert. |
| 5 | Patients punished for self-advocacy | **No** | The patient never sees the note. (Abridge's mobile experience is for the clinician only.) | No patient-facing note view, no patient-correction workflow, no "here's what I'm worried about and here's what I'm going to do" auto-drafted patient communication. |
| 6 | Doctors don't see the "between visits" (flares, heat intolerance, sleep) | **No** | None — Abridge sees only the in-visit audio. | No wearable data (Apple Watch, StrivePD, EpiMonitor), no patient-reported outcomes, no between-visit symptom logs. |
| 7 | Caregivers are the real information source (dementia, stroke, pediatric) | **No** | None — Abridge is patient-clinician only. No caregiver role. | No caregiver pre-visit intake, no caregiver consent flow, no HIPAA-compliant caregiver channel. For dementia and pediatric neurology, this is a major gap. |
| 8 | Medical education gap (neurologists don't know about sub-specialties) | **Partial** | Abridge's specialty templates can surface specialty-specific prompts. | No "this patient meets criteria for a headache specialist referral per AAN guidelines" or "consider an EMU admission" suggestion. |

**Abridge coverage score: 0 full / 2 partial / 6 no = 2/24 (≈8%).** Confirms the capstone thesis: Abridge is dominant in the scribe layer (Layer 1-2) but leaves the pre-visit synthesis layer (Layer 5) completely open.

---

## Section 5 — Summary

### Moat

1. **First-mover + KLAS awards:** 2025 + 2026 Best in KLAS for ambient AI, the only one with a peer-reviewed JAMA study. 300+ health systems. ~$808M raised.
2. **Linked Evidence:** the trademarked click-to-source feature. Hard to copy because it requires a tight integration between the ASR output and the LLM output, sentence-segment aligned. This is a UX moat, not a tech moat, but it's defensible.
3. **EHR integration depth:** Epic is the deepest. Cerner and athena are present but lighter. Switching cost is high once deployed.
4. **Regulatory positioning:** as a "clinical documentation tool" not a "clinical decision support" tool, Abridge avoids FDA review. This lets them ship fast.

### Weakness

1. **Layer 5 is unowned.** Abridge is Layer 1-2 only (audio → text → note). The pre-visit synthesis is the upstream of every scribe, and nobody owns it.
2. **No longitudinal view.** The note is per-encounter. The doctor still has to read the prior chart manually.
3. **No between-visit data.** No wearable integration, no patient-reported outcomes, no symptom logs.
4. **No caregiver channel.** For dementia, stroke recovery, pediatric, ALS — the caregiver is the real information source, and Abridge doesn't include them.
5. **Patient not in the loop.** The patient never sees the note, can't correct it, can't contribute data.
6. **Real-world value capture below marketing.** STAT News reported scribes save under 1 min/note in some studies — below what was promised.

### Our opportunity (the 3 pain points with weakest Abridge coverage)

| Pain point | Our wedge |
|---|---|
| **#7 Caregivers are the real information source** | A pre-visit synthesis that includes the caregiver as a first-class data source. HIPAA-compliant structured caregiver intake, longitudinal tracking of caregiver-reported changes, automatic synthesis into the visit note. **No competitor owns this layer.** |
| **#6 Doctors don't see the "between visits"** | A pre-visit synthesis that pulls wearable data (Apple Watch Movement Disorders, StrivePD for PD, EpiMonitor for epilepsy), patient-reported symptom logs, and between-visit events. **The longitudinal trajectory that no scribe owns.** |
| **#2 13-year diagnostic journeys** | A pre-visit synthesis that summarizes the longitudinal record: prior specialists seen, prior workup attempted, prior "anxiety" labels, current best differential. **The "I don't know, but here's what we know" verdict.** |

These three pain points, taken together, define the Layer 5 wedge: the pre-visit briefing the doctor sees before walking into the room. None of the 16 mapped competitors (Abridge, DeepScribe, DAX, Suki, Freed, Nabla, Heidi, DeepCura, Viz.ai, RapidAI, Brainomix, Aidoc, Ceribell, Natus, Rune Labs, Empatica) owns this layer.

---

## Sources

### Primary
- https://www.abridge.com/
- https://www.abridge.com/product
- https://www.abridge.com/ai/science-ai-evaluation
- https://www.abridge.com/blog/becoming-the-benchmark-for-healthcare-ai
- https://www.abridge.com/blog/kumc-research-studies
- https://www.abridge.com/press-release/series-c-150
- https://support.abridge.com/hc/en-us/articles/30235128433811-Verify-a-Note-With-Linked-Evidence

### Funding / business
- https://news.crunchbase.com/health-wellness-biotech/ai-doctor-note-taking-startup-abridge/
- https://www.fiercehealthcare.com/ai-and-machine-learning/ambient-ai-startup-abridge-scores-300m-series-e-backed-a16z-and-khosla
- https://www.crunchbase.com/organization/abridge-d1a4

### Third-party reviews / pricing
- https://www.marvix.ai/blog/abridge-pricing-review
- https://www.deepcura.com/resources/abridge-ai-review
- https://www.veroscribe.com/blog/abridge-review-2026
- https://www.trytwofold.com/compare/abridge-ai-review
- https://orbdoc.com/learn/ai-medical-scribe-pricing-guide
- https://www.g2.com/products/abridge/reviews

### Academic / clinical evidence
- https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542 (Olson et al., 6 health systems, JAMA Network Open Oct 2025)
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/ (Tierney et al., KUMC, JAMIA Open Feb 2025)
- https://www.statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/

### Patient pain points (referenced in gap analysis)
- `Week 1-2 - Reddit Patient Pain Points.md` (8 pain points from 12+ threads)

### Related teardowns
- [[Competitor Teardown - Viz.ai]]
- [[Competitor Teardown - Ceribell]]