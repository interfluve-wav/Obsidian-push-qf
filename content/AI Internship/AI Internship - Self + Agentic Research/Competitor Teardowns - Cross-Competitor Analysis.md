#capstone #ai-internship #neurology #competitors #cross-comparison

# Competitor Teardowns — Cross-Competitor Analysis

Companion to: [[Competitor Teardown - Abridge]] · [[Competitor Teardown - Viz.ai]] · [[Competitor Teardown - Ceribell]] · [[Competitor Deep-Dive Framework]]

This document consolidates the 3 deep-dive teardowns into a single comparison view, plus the cross-competitor 8-pain-point gap matrix that drives the capstone's "Layer 5" wedge thesis.

---

## TL;DR

The 3 teardowns cover one company per layer of the AI taxonomy: **Abridge** (Layer 1-2 scribe), **Viz.ai** (Layer 3 imaging), **Ceribell** (Layer 4 signals). The cross-competitor gap analysis shows that **all three together cover only 5 of 24 possible pain points (21%)** — and the unowned quadrant is the pre-visit synthesis layer where the doctor walks into the room already briefed on the patient.

---

## 1. Side-by-side: 3 competitors

| Dimension | Abridge | Viz.ai | Ceribell |
|---|---|---|---|
| **Layer (AI taxonomy)** | 1-2 (audio→text + text→note) | 3 (imaging→findings) | 4 (signals→events) |
| **Founded** | 2018 | 2016 | 2014 |
| **HQ** | Pittsburgh, PA | San Francisco, CA + Tel Aviv | Sunnyvale, CA |
| **Total raised** | ~$808M | ~$291.5M | ~$207M IPO + ~$188M pre-IPO = ~$395M |
| **Valuation / market cap** | $5.3B (Series E, Feb 2025) | $1.2B (Series D, 2022) | ~$578M IPO (Oct 2024); public since |
| **Funding stage** | Series E | Series D (mature) | Public (Nasdaq: CBLL) |
| **FY2025 revenue** | Not disclosed (estimate $100M+) | $40M (2023) → ~$100M ARR (2025) | $89.1M (+36% YoY) |
| **Customer count** | 300+ health systems | ~2,000 hospitals, 230M lives | 647 active hospital accounts |
| **Pricing model** | Enterprise, $208–$800/provider/mo (est.) | Enterprise per-hospital, $25k+/yr/hospital (est.) | Headband $688 + monthly subscription |
| **FDA-cleared?** | **No** (positioned as documentation tool) | Yes (50+ cleared algorithms) | Yes (multiple 510(k)s, including 1st delirium monitor) |
| **CMS reimbursement** | None | **First AI ever with NTAP** (up to $1,040/use) | NTAP for electrographic status epilepticus |
| **Key differentiator** | Linked Evidence (click-to-source) | Stroke triage + care coordination (1,700+ hospitals) | Point-of-care EEG headband + Clarity AI (95% sens / 97% spec) |
| **Best-published clinical evidence** | JAMA Network Open (Oct 2025): burnout 51.9% → 38.8% | Door-to-puncture reduction 11–25 min; scoping review of 29 studies | Neurocrit Care 2025: 4.1-day shorter ICU stay, 19h faster time-to-EEG |
| **Where it wins** | Outpatient, multi-specialty, primary care, deep Epic | Acute stroke, ED/IR, large hospitals | ICU/ED seizure detection, status epilepticus, delirium |
| **Where it fails** | No longitudinal chart, no caregiver, no between-visit data, patient not in loop | Only stroke + few other acute conditions; ED only; no outpatient; FDA forbids patient viewing | Acute only; no outpatient; no diagnostic journey; no between-seizure data |
| **Publicly named customers** | Mayo, Cleveland, UPMC, Stanford, Yale, Emory, all 6 UC | 1,700+ hospitals (mostly stroke centers) | UCLA, Stanford, Cleveland Clinic, Mission, UT Southwestern |
| **Key accuracy / clinical claim** | 24% rel. WERR reduction; 15% rel. accent improvement; 81% "easier" workflow | Door-to-puncture 11–25 min faster; LVO sensitivity 78–97% | Sensitivity 95%, Specificity 97%, NPV 99.9% |

---

## 2. What they compute (the 5-layer AI taxonomy mapping)

| Layer | Function | Abridge | Viz.ai | Ceribell |
|---|---|---|---|---|
| 1 | Audio → text | ✅ Yes (Whisper-class ASR) | ❌ No | ❌ No |
| 2 | Text → structured note | ✅ Yes (multi-model LLM + Linked Evidence) | ❌ No | ❌ No |
| 3 | Imaging → findings | ❌ No | ✅ Yes (50+ algorithms: LVO, ASPECTS, CTP, aneurysm) | ❌ No |
| 4 | Signals → events | ❌ No | ❌ No | ✅ Yes (Clarity AI, 95% sens / 97% spec) |
| 5 | Pre-visit synthesis | ❌ **No** | ❌ **No** | ❌ **No** |

**No competitor owns Layer 5.** This is the wedge.

---

## 3. The 8-pain-point gap analysis (cross-competitor matrix)

The 8 pain points come from the patient-research corpus (`Week 1-2 - Reddit Patient Pain Points.md`, 12+ threads).

Scoring: **Yes** = addresses it; **Partial** = partially; **No** = does not address.

| # | Pain point (verbatim from Reddit) | Abridge | Viz.ai | Ceribell | **Total** |
|---|---|---|---|---|---|
| 1 | Doctors attribute symptoms to anxiety/psych rather than "I don't know" | **No** | No | Partial (objective EEG data could reduce psych attribution for seizures) | 0/3 |
| 2 | 13-year diagnostic journeys | **No** | No (only acute stroke) | No (acute only, no diagnostic journey) | 0/3 |
| 3 | 10-minute appointments, no listening | **Partial** (frees doctor from typing) | N/A (ED setting) | N/A (ICU setting) | 0.5/3 |
| 4 | Dismissive comments on ambiguous test results ("good news your EEG was normal!") | **No** | No | Partial (more EEG data) | 0.5/3 |
| 5 | Patients punished for self-advocacy | **No** | No (FDA forbids patient viewing of mobile preview) | No | 0/3 |
| 6 | Doctors don't see the "between visits" (flares, heat intolerance, sleep, between-seizure data) | **No** | No (acute) | No (acute, no between-seizure capture) | 0/3 |
| 7 | Caregivers are the real information source (dementia, stroke, pediatric) | **No** | No | No | **0/3 — cleanest gap** |
| 8 | Medical education gap (neurologists don't know about sub-specialties, don't translate test results for patients) | **Partial** (specialty templates) | No | Partial (objective data) | 1/3 |
| | **Total coverage** | **2/24 (8%)** | **1/24 (4%)** | **1.5/24 (6%)** | **4.5/24 (≈19%)** |

### The cleanest gaps (zero coverage across all 3 incumbents)

| Pain point | Why it's the wedge |
|---|---|
| **#7 Caregivers are the real information source** | For dementia, stroke recovery, pediatric, ALS — the caregiver is the primary data source. None of Abridge, Viz.ai, Ceribell include a caregiver channel. **This is the single biggest unowned feature in the entire AI healthcare landscape.** |
| **#2 13-year diagnostic journeys** | The longitudinal record summary. No incumbent does this. |
| **#6 Between-visits data** | Wearable + symptom log integration. No incumbent does this. |
| **#1 Psych attribution** | The structured symptom timeline that supports the "I don't know" verdict. No incumbent does this. |

These 4 pain points together define the Layer 5 wedge.

---

## 4. Pricing comparison

| Competitor | Pricing model | Per-provider estimate | Per-hospital estimate | Per-scan estimate | CMS reimbursement |
|---|---|---|---|---|---|
| **Abridge** | Per-provider subscription, annual | $208–$800/provider/mo | — | — | None |
| **Viz.ai** | Per-hospital subscription, modular by disease suite | — | $25k+/yr (third-party est., stroke module) | — | **NTAP up to $1,040/Viz LVO use** (first AI ever) |
| **Ceribell** | Hardware (consumable) + monthly subscription | — | $688/headband + subscription | — | NTAP for status epilepticus |

**Key insight:** The only two AI companies with CMS reimbursement (NTAP) are in acute care (stroke, status epilepticus). **Outpatient AI has no reimbursement path** — this is both a barrier and an opportunity. Our Layer 5 wedge would need to either (a) position as productivity software (charge per-provider, no reimbursement), (b) find a way to bill CPT codes for cognitive work the AI does, or (c) target the health-system subscription model.

---

## 5. Clinical evidence quality ranking

| Competitor | Best evidence | Sample | Where published |
|---|---|---|---|
| **Abridge** | 6-health-system prospective study, 30-day pre/post | n=263 | JAMA Network Open (Olson et al., Oct 2025) — peer-reviewed |
| **Abridge** | KUMC pre/post | n=181 | JAMIA Open (Tierney et al., Feb 2025) — peer-reviewed |
| **Ceribell** | Multi-center retrospective | n=859 (estimated) | Neurocritical Care (Desai et al., 2025) — peer-reviewed |
| **Viz.ai** | Scoping review of 29 studies (mixed sponsors) | 29 studies | Medicina (Dorochowicz et al., Mar 2026) — peer-reviewed |
| **Viz.ai** | Door-to-puncture reduction | multiple | Various (mixed quality, some industry-sponsored) |

**Abridge has the strongest clinical evidence among the 3.** The JAMA publication is the single most-cited evidence in the AI scribe space.

---

## 6. Strategic implications for the capstone

### The wedge is Layer 5

After 3 deep-dives, the conclusion is unambiguous: **no incumbent owns the pre-visit synthesis layer**. The wedge is the briefing the doctor sees before walking into the room, pulling together:

1. The longitudinal chart (prior visits, prior specialists, prior workup) — addresses pain point #2
2. The imaging + signals + labs in one view — addresses pain point #4
3. The wearable / between-visit data — addresses pain point #6
4. The caregiver's structured intake (for dementia/stroke/pediatric) — addresses pain point #7
5. The structured symptom timeline that supports the "I don't know, but here's the differential" verdict — addresses pain point #1

### The defensible moat

Building Layer 5 well is hard because it requires:
- A robust chart-integration pipeline (FHIR, Epic, Cerner)
- A specialty-specific prompt library (30+ templates)
- A wearable / device integration layer (Apple Watch, StrivePD, EpiMonitor)
- A HIPAA-compliant caregiver channel
- A multi-agent LLM to combine all of the above (per Sorka et al., 89.2% on neurology boards)

The closest competitor in any single dimension is Abridge (EHR integration, specialty templates, KLAS). But Abridge explicitly does not own the longitudinal synthesis, the caregiver channel, or the between-visit data. **Abridge is the obvious acquisition target for someone who builds Layer 5.**

### The 5 most defensible wedge options for the capstone

| # | Wedge | Defense | Build difficulty |
|---|---|---|---|
| 1 | **Pre-visit synthesis for the chronic migraine patient** (47M US patients, AI market is greenfield) | Headache-specific trajectory, MIDAS scoring, red-flag screening | Medium |
| 2 | **Caregiver-in-the-loop for dementia** (6.5M US patients, 4 geriatric neuro sites) | HIPAA-compliant caregiver channel, behavioral change tracking, MoCA drift | Medium |
| 3 | **Movement disorder wearable-chart synthesis** (1M Parkinson's, UPDRS drift tracking) | Apple Watch Movement Disorders API + chart pull, dyskinesia detection | High (needs wearable) |
| 4 | **EEG-visit synthesis for epilepsy** (3.4M US, 50% of routine EEGs miss focal seizures) | Ceribell/encevis pull + visit note merge, seizure calendar | High (needs EEG integration) |
| 5 | **"I don't know" verdict tool for the undiagnosed** (undiagnosed headache, cognitive decline, "I don't know what's wrong") | Structured symptom timeline, prior workup summary, differential generation | Medium |

**Top recommendation for the 8-week capstone:** #1 (chronic migraine) or #2 (caregiver dementia). Both are tractable in 8 weeks, both have clear unmet need, and both have low incumbent AI competition. Pair #1 with the longitudinal chart-synthesis feature (Layer 5) and you've got the strongest pitch.

---

## 7. The "Big Vision" framing (Week 8 first slide)

> *"No existing neurology AI company owns the pre-visit synthesis layer — the briefing the doctor sees before walking into the room.*
>
> *Abridge owns the audio-to-text pipeline but doesn't pull the longitudinal chart. Viz.ai owns the imaging analysis but doesn't write the visit note. Ceribell owns the EEG signal but doesn't see the between-seizure data. None of them include the caregiver.*
>
> *Our product synthesizes chart + imaging + signals + wearable + caregiver input into a single briefing the neurologist uses to prepare for a visit. The note happens to come out as a side effect."*

This is the Week 8 first slide. It's defended by the 8-pain-point gap analysis above: the 4 pain points with zero coverage across all 3 incumbents.

---

## 8. Quick reference table for the Week 8 deck

| Slide | Content |
|---|---|
| 1 | Big Vision quote (above) |
| 2 | The 5-layer AI taxonomy (Layer 1-5) |
| 3 | 8 patient pain points (from Reddit research) |
| 4 | 3 deep-dive competitor profiles (Abridge, Viz.ai, Ceribell) |
| 5 | 8-pain-point gap matrix (this doc) |
| 6 | The 4 pain points with zero coverage = the wedge |
| 7 | Architecture: how Layer 5 works (RAG over chart + imaging + signals + caregiver) |
| 8 | The thin slice demo (1 feature end-to-end) |
| 9 | Market sizing (TAM/SAM/SOM) |
| 10 | Pricing model |
| 11 | 8-week roadmap (what we built) |
| 12 | Next steps |

---

## Sources

All from the 3 individual teardowns:

- [[Competitor Teardown - Abridge]] — 28 KB, 6 customer quotes, JAMA 6-system study, $5.3B valuation
- [[Competitor Teardown - Viz.ai]] — 57 KB, 11 clinician quotes, NTAP $1,040/use, RapidAI accuracy gap
- [[Competitor Teardown - Ceribell]] — 48 KB, point-of-care EEG headband, 95% sens / 97% spec, $89.1M FY25 revenue

Plus:
- [[Competitor Deep-Dive Framework]] — the 4-step process used for all 3
- [[Week 1-2 - Reddit Patient Pain Points]] — the 8 pain points
- [[Week 1-2 - Research Papers]] — the academic foundation
- [[Week 1 - Neurology Research]] — the 16-competitor map

## Next steps

1. **Week 2 quick-scans** for the remaining 13 competitors (DeepScribe, Suki, Freed, RapidAI, Brainomix, Aidoc, NeuroQuant, Rune Labs, Empatica, Natus, encevis, Piramidal, DeepCura) — 30 min each, ~6 hours total
2. **Friend's first doctor interview** — use the 8-pain-point matrix to validate which pain points are real for the chosen subspecialty
3. **Architecture doc for Layer 5** — sketch the RAG pipeline, multi-agent LLM, caregiver channel, wearable integration
4. **Market sizing** — use the pricing data from these teardowns to build the revenue model
5. **Week 3 training experiment** — pick the subspecialty, download the dataset, run baseline