---
title: Competitor Teardown - Ceribell
updated: 2026-07-07 11:46 EDT
---

# Competitor Teardown — Ceribell

#competitor #ai-internship #neurology #epilepsy #icu #eeg #deep-dive
Related: [[Competitor Deep-Dive Framework]] · [[Week 1 - Neurology Research]] · [[Week 1-2 - Reddit Patient Pain Points]]

---

## TL;DR (60-second read)

Ceribell is the **dominant point-of-care EEG company in the US** — a wearable 10-electrode headband + cloud AI ("Clarity") that flags non-convulsive seizures and status epilepticus in ICU/ED patients within minutes, instead of the hours it takes to wheel in a conventional 21-channel EEG and wait for a tech + neurologist to read it. Headquartered in Sunnyvale, CA; founded 2014 by Stanford neurologist Josef Parvizi and music-tech researcher Chris Chafe (the "Brain Stethoscope" sonification concept). Went public on Nasdaq (CBLL) on Oct 11, 2024, raising **$207.3M gross** at $17/share (~$578M implied valuation, per Forge Global). FY2025 revenue: **$89.1M (+36% YoY)**; 647 active hospital accounts; 88% gross margin; **$53.4M net loss**. Total private funding before IPO: ~$188M (Ally Bridge, RA Capital, The Rise Fund). FDA-cleared (multiple 510(k)s) for adult → pediatric → neonatal seizure detection, and — as of Dec 9, 2025 — **first FDA-cleared delirium monitoring** (K251936). They are the only FDA-cleared AI for all ages preterm-neonate → adult. Clearest competitor and wedge for our capstone: Ceribell covers acute inpatient seizures brilliantly; it has **zero coverage of outpatient diagnostic journeys, caregiver/patient experience, inter-visit ("between seizures") data, or patient-facing self-advocacy tools** — exactly the four pain points that dominate the Reddit neurology patient corpus.

---

## Section 1 — Surface scan

### 1.1 One-paragraph company summary

Ceribell is a publicly-traded medical device + AI company (Nasdaq: **CBLL**, HQ Sunnyvale, CA) that has built the first FDA-cleared, AI-powered, point-of-care EEG platform for the acute-care setting. The system is a single-use soft 10-electrode headband that wraps around the patient's head, snaps onto a pocket-size EEG recorder (the "Ceribell EEG Recorder"), and uploads data via Wi-Fi to a HIPAA-compliant cloud portal. A proprietary cloud AI called **Clarity** (versions 7.0 from Dec 2024, pediatric add-on April 2025, neonatal Nov 2025) analyzes the EEG stream and emits a bedside "Suspected Status Epilepticus" or "Continuous Seizure" alert — measured as seizure burden ≥90% of any rolling 5-minute window — so non-neurologist nurses and ICU/ED physicians can act before a specialist reads the tracing. Founders are Stanford neurologist Josef Parvizi (who co-developed the original "Brain Stethoscope" sonification method) and music-tech pioneer Chris Chafe; CEO is Jane (Xingjuan) Chao, PhD. Per the Ceribell homepage: *"Triage and continuously monitor hospital patients at risk for seizures in minutes with Ceribell's point-of-care EEG solution."*

> Verbatim homepage headline: *"Triage and continuously monitor hospital patients at risk for seizures in minutes with Ceribell's point-of-care EEG solution."* — https://ceribell.com/

### 1.2 Headline features list (as published on ceribell.com)

1. **Ceribell EEG Headband** — disposable 10-electrode soft headband; built-in gel; green-light impedance feedback; CT-compatible (per the JCM 2026 POC-EEG review); *not MRI compatible*. Verbatim: *"Rapid EEG set up within minutes with minimal training1,2"* — https://ceribell.com/product/point-of-care-eeg/
2. **Ceribell EEG Recorder** — pocket-size amplifier/recorder that streams to the cloud; 8 bipolar pairs; 250 Hz sampling; 0.5–100 Hz frequency response (per Frontiers 2023 community-hospital study).
3. **Clarity AI algorithm** — bedside seizure-burden display; "First FDA-cleared instantaneous bedside alert indicating suspected status epilepticus in adults and continuous seizures in neonates and pediatric patients" (K223504 / K241589 / K252070). Verbatim metric: *"95% sensitivity\*, 97% specificity\*, 99.9% NPV"* — https://ceribell.com/
4. **EEG Portal (cloud)** — Adult/pediatric + neonate portals; remote real-time viewing; seizure burden trend; EEG auto-labeling. FedRAMP High cybersecurity authorization (per homepage, ref 8).
5. **Brain Stethoscope** — sonification (audio rendering) of EEG, so a non-expert can listen for seizure patterns. Co-developed by Parvizi/Chafe (Stanford 2018 *Epilepsia* paper).
6. **Delirium monitoring (NEW Dec 2025)** — "first and only FDA-cleared delirium screening and monitoring device" (K251936); continuously analyzes EEG and notifies clinicians when delirium-associated patterns are detected. Validated in 225 adults in critical care.
7. **LVO stroke detection (FDA Breakthrough Designation 2025)** — first-in-class large vessel occlusion stroke detection & monitoring solution (per Q4 2025 release).

> Verbatim taglines (homepage differentiators): *"Simplicity without Sacrifice · Designed for speed when time is brain"* and *"Proven AI Performance — 95% sensitivity\*, 97% specificity\*, 99.9% NPV7"*.

### 1.3 Pricing model

**Direct list price:** not publicly posted on ceribell.com. The site is gated behind "Free Demo" CTA. Pricing is enterprise-negotiated per hospital / per health system.

**Real-world economics from peer-reviewed literature:**
- **Hardware:** disposable headband list ~**$688** per unit (cited verbatim in Ward et al. 2023, *Frontiers in Digital Health*: *"We then calculated the annual fixed cost of the Ceribell® system (monthly subscription fee × 12)"* — context confirms $688 headband cost and a recurring subscription; see https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2023.1035442/full).
- **Model:** hardware (consumable headband) **+ monthly subscription** for the recorder/cloud portal/AI.
- **NTAP eligibility:** CMS awarded a New Technology Add-on Payment for Clarity's electrographic status epilepticus (ESE) indication. In a Ceribell case study (90-day review, 86-bed Midwest hospital, 10–11 uses/month): *"10 out of 33 (30%) claims with the Ceribell NTAP code were paid at a total of $8,650."* — https://ceribell.com/health-economics/

**Estimated annual hospital economics:** Ceribell's published white paper claims **$5k+ savings per patient** on average; a multi-center retrospective published in *Neurocritical Care* (Desai et al. 2025) reports **4.1-day shorter median ICU length of stay**, **18-percentage-point fewer patients discharged with poor modified Rankin Scale scores**, and **19-hour faster median time-to-EEG acquisition (5.9h Ceribell vs 25.3h conventional)** — driving downstream DRG/CC/MCC coding value.

> Verbatim (Ceribell health economics page): *"Used in more than 550 hospitals,\\* Ceribell delivers proven clinical and financial impact across emergency and critical care settings"* and *"Estimated Savings Across 459 Hospitals — $52.6 Million."* — https://ceribell.com/health-economics/

### 1.4 Funding to date

- **Private (pre-IPO):** ~**$188M** across 4 rounds per Tracxn (2026 company profile). Series C lead: Ally Bridge Group (Sep 22, 2022). Other investors: The Rise Fund, Longitude Capital, RA Capital Management, Optima Capital, Horizon (debt). First round: Sep 25, 2018. Source: https://tracxn.com/d/companies/ceribell/__4jETpXx0-qq_faWuBbgxTsbXIVBt2YFBGByqBc_3QGA
- **IPO (Oct 11, 2024):** Priced at **$17/share** for 10,606,060 shares → **$180.3M** gross. After underwriters exercised full overallotment (1,590,909 additional shares), total gross proceeds = **$207.3M**. Implied valuation at IPO ~**$578M** (Forge Global). BofA Securities and J.P. Morgan were joint book-runners. Sources: https://investors.ceribell.com/news-releases/news-release-details/ceribell-inc-announces-closing-upsized-initial-public-offering/ and https://www.sec.gov/Archives/edgar/data/1861107/000095017024114320/ceribell_424b4.htm
- **Public-company revenue trajectory:**
  - FY2024: $65.4M total revenue (baseline)
  - FY2025: **$89.1M** (+36% YoY) — 87% gross margin in Q4 2025, 88% for full year; net loss **$53.4M**; **647 active accounts** at year-end
  - Q1 2026: **$26.5M** (+29% YoY); 680 active accounts
  - **2026 guidance:** $111M–$115M (25–29% growth)
  - Cash + securities at 12/31/2025: **$159.3M**
  - Product vs. subscription revenue split FY2025: $67.3M product / $21.7M subscription (subscription +41% YoY — the SaaS-like recurring line is the growth lever)
  - Source: https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial

### 1.5 Company facts

| Field | Value | Source |
|---|---|---|
| Founded | **2014** | Tracxn |
| Founders | **Chris Chafe, Xingjuan (Jane) Chao, Josef Parvizi** | Crunchbase / Tracxn |
| CEO | **Jane Chao, PhD** (co-founder) | All press releases |
| HQ | **Sunnyvale, CA** (formerly Mountain View) | ceribell.com / SEC |
| Ticker / exchange | **CBLL / Nasdaq Global Select** since Oct 11, 2024 | IPO press release |
| Stock price at IPO | $17.00 | SEC 424B4 |
| Employees | **403** (Tracxn, May 2026); **251–500** (Crunchbase bucket) | Tracxn |
| Active hospital accounts | **647** (12/31/25) → **680** (Q1 2026) | Earnings releases |
| Hospitals using Ceribell (per homepage) | **"more than 550"** (as of July 2025 per page footnote \*) | https://ceribell.com/health-economics/ |
| Customers named publicly | UCLA, Stanford, Cleveland Clinic (Piramidal partner, not direct Ceribell customer), Mission Hospital, U. Kansas, UT Southwestern | Testimonial carousel, ceribell.com |
| Patent litigation | **Ceribell v. Natus Medical** — ITC + D. Del. — filed July 7, 2025; Ceribell alleges Natus's "BrainWatch" POC EEG infringes 6 Ceribell patents. ITC decision expected **11/19/26**. | https://ceribell.com/about-us/litigation-information-page/ |
| Funding sources | Founders: Stanford (Parvizi is Stanford neurologist; Chafe is Stanford music/CCRMA professor) | Stanford Report 2018 |

### 1.6 Customer quotes (verbatim, from ceribell.com testimonial carousel — Sept 2025 snapshot)

> **Paul Vespa, MD — Neurologist & Neurocritical Care, UCLA, Los Angeles, CA:**
> *"Ceribell, [is] easy to use, easy to apply, and would be greatly utilized in emergency departments or small hospitals where they just don't have the available services to rapidly assess the patient."*
> https://ceribell.com/

> **Laleh Gharahbaghian, MD — ED Physician, Stanford Health Care, Palo Alto, CA:**
> *"They are eager to use it [Ceribell] because they understand its effect and impact and the data that they can obtain from it quite easily and quite quickly and quite accurately."*
> https://ceribell.com/

> **Mary Kay Bader, CCRN, CNRN — Nurse, Mission Hospital, Mission Viejo, CA:**
> *"The Ceribell EEG technologies have improved our ability to detect and treat seizures… it's readily available, it's in the ICU, it's in the emergency department."*
> https://ceribell.com/

> **Margo Block, DO — Neurologist, University of Kansas Medical Center:**
> *"It's just made a huge difference as far as the timing and being able to rapidly assess and treat appropriately and to really triage the brain in a way that we have never been able to prior to this technology [Ceribell]."*
> https://ceribell.com/

> **Daiwai Olson, PhD — Nurse, UT Southwestern, Dallas, TX:**
> *"Instead of intubating the patient, sending them to the ICU, expending those efforts, this patient never saw the neuro ICU. They were discharged home."*
> https://ceribell.com/

> **Parshaw Dorriz, MD — Neurologist, Mission Hospital:**
> *"[Ceribell] has changed our culture as far as how we manage patients with seizures, how we manage patients neurologically, and doing it in a way that doesn't compromise patient care."*
> https://ceribell.com/

**External (academic, not vendor-controlled) — Hofmann et al., LaMonte 2021, *Epilepsia Open*:**
> *"The Ceribell EEG reduced diagnosis time (P = .0000006) and on-call workforce demand (P = .02). The device can be used at any time of day in any hospital care area and has advantages in respiratory isolation rooms."* — https://pmc.ncbi.nlm.nih.gov/articles/PMC8013275/

**External (critical, Reddit r/neurology 2024, snippet only — site blocked scraping):**
> *"Ceribell is extremely expensive compared to a regular spot Eeg. But it can be run by anyone who knows how to turn on a machine and stick a sticker."* — https://www.reddit.com/r/neurology/comments/1eq00jr/can_anyone_provide_anecdotes_or_proof_of/ (snippet via Google search; full thread behind Reddit block)

---

## Section 2 — "What do they compute" deep read

### 2.1 Architecture diagram (text)

```
┌─────────────────────────────────────────────────────────────┐
│  PATIENT (ICU / ED / ED-to-ICU / EMS / isolation room)      │
│  • Suspected non-convulsive seizure or altered mental status│
│  • Cardiac arrest, TBI, sepsis encephalopathy, post-ictal   │
└─────────────────────┬───────────────────────────────────────┘
                      │ Disposable Ceribell EEG Headband
                      │ (10 electrodes → 8 bipolar channels;
                      │  pre-filled gel; green LED = OK;
                      │  applied by any RN/RT in ~5 min)
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  CERIBELL EEG RECORDER (pocket-size, battery)               │
│  • 250 Hz sampling; 0.5–100 Hz bandwidth                    │
│  • Built-in "Brain Stethoscope" — sonifies EEG to audio     │
│  • Local alarm logic                                        │
│  • WiFi upload → HIPAA-compliant cloud                      │
└─────────────────────┬───────────────────────────────────────┘
                      │ Encrypted stream (FedRAMP High)
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  CERIBELL CLOUD PORTAL                                      │
│  ┌──────────────────┐  ┌────────────────────────────────┐  │
│  │ Clarity AI       │  │ Real-time remote EEG viewing   │  │
│  │ • 10-sec epoch   │  │ • Adult + Pediatric portal     │  │
│  │   classifier     │  │ • Neonatal portal (12-ch)      │  │
│  │ • Rolling 5-min  │  │ • Seizure burden trend graph   │  │
│  │   seizure burden │  │ • Auto-labels each 10-sec      │  │
│  │ • ≥90% burden =  │  │   epoch                        │  │
│  │   STATUS ALERT   │  └────────────────────────────────┘  │
│  │ • ≥50% burden =  │  ┌────────────────────────────────┐  │
│  │   SEIZURE flag   │  │ Delirium AI (K251936, Dec 2025)│  │
│  │                  │  │ • Continuous delirium monitor  │  │
│  └──────────────────┘  └────────────────────────────────┘  │
└─────────────────────┬───────────────────────────────────────┘
                      │ Bedside alarm + remote neurologist view
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  CLINICIAN (RN, ED MD, ICU MD, neurologist on call)          │
│  • "Continuous Seizure Suspected" → bedside alarm           │
│  • "Suspected Status Epilepticus" → red status alert         │
│  • Treat per ACLS / Neurocritical Care Society guidelines    │
│  • Or "rule-out" → avoid unnecessary benzo load              │
└─────────────────────────────────────────────────────────────┘
```

### 2.2 Per-feature Input → Compute → Output table

| Feature | Input (raw data) | Compute (algorithm) | Output | Latency | Published accuracy |
|---|---|---|---|---|---|
| **Clarity AI — Seizure Burden** (K223504 adult ESE, K241589 peds, K252070 neonate) | 8-channel EEG, 10-sec epochs, rolling 5-min window | ML classifier (described in literature as preprocessing → segmentation → features over time/freq/channel; trained on "thousands of hours of expert-annotated EEG"); seizure-burden = % 10-sec epochs with ictal activity in last 5 min | (a) Numeric seizure-burden %; (b) bedside alarm when burden ≥90% (≥4.5 of 5 min); (c) portal label per epoch | Real-time streaming (alarms fire within seconds of threshold breach) | **Sensitivity 95–96%, Specificity 94.8–97%, NPV 99.9%** for status epilepticus in adult validation; pediatric and neonate validations on ≥1,700 + ≥700 EEGs respectively |
| **Clarity — Continuous Seizure (neonate/peds)** (K252070 + K241589) | Same 8-channel EEG | Same algorithm, retrained + validated for pediatric and neonatal ictal patterns | "Continuous Seizure Suspected" alert (lower threshold than adult ESE) | Real-time | "Pediatric-specific Clarity Algorithm has Similar High Accuracy for Ruling Out and Detecting Continuous Seizures in Patients Ages 1-17 as With Adults" (Ceribell peds page) |
| **Delirium Monitoring AI** (K251936, cleared Dec 9, 2025) | Same EEG stream | Proprietary algorithm trained on EEG + clinical assessments | Real-time bedside "delirium-pattern detected" notification | Continuous | Validated in 225 ICU adults; first FDA-cleared device for delirium screening & monitoring |
| **Brain Stethoscope (sonification)** | Same raw EEG | Audio rendering of dominant frequency (Parvizi/Chafe 2018 *Epilepsia*) | Audible seizure signature via recorder speaker | Live | Hobbs et al. 2018 (Neurocrit Care): ICU staff without EEG training detected seizures with sensitivity/specificity comparable to expert readers |
| **EEG Portal — remote review** | Uploaded EEG stream | Web UI with auto-labels, trend graph, raw view | Browser-based live EEG to remote neurologist | Streaming | N/A (display layer) |
| **2HELPS2B score** | Same EEG | Standardized seizure-risk score | Numeric risk score for next-24h seizure | Calculated post-hoc | Ceribell POC-EEG = conventional EEG in forecasting via SAFER-EEG (Kalkach-Aparicio et al. 2024 *Neurology*) |
| **LVO stroke detection** (Breakthrough Designation 2025, not yet cleared at time of writing) | Same EEG | TBD — EEG-derived biomarker for large vessel occlusion | Stroke alert | TBD | Pre-FDA |

### 2.3 Published evaluation results (with citations)

| Year | Study | n | Headline result | Source |
|---|---|---|---|---|
| 2018 | Hobbs et al., *Neurocrit Care* (Stanford ICU) | 54 ICU patients | Bedside EEG sonification by non-expert ICU staff: sensitivity/specificity ≈ expert readers | https://pubmed.ncbi.nlm.nih.gov/29923167/ |
| 2018 | Parvizi, Gururangan, Razavi, Chafe — *Epilepsia* | — | Brain Stethoscope sonification detects "silent seizures by their sound"; cofounders disclose IP | https://ceribell.com/wp-content/uploads/2020/11/BRAIN-STETHOSCOPE-Manuscript-Parvizi-594-p877-84-Epilepsia-2018.pdf |
| 2020 | Gururangan, Razavi, Parvizi — *Clin Neurophysiol Practice* | — | 8-channel EEG diagnostic utility for generalized/hemispheric seizures + rhythmic periodic patterns | Cited in PMC8013275 |
| 2020 | Kamousi et al., *Neurocrit Care* (Ceribell authors + U Penn / Stanford / Mt Sinai) | **353** adult Ceribell recordings | Clarity: SE alert (≥90% burden) **100% sensitivity, 93% specificity**; ≥50% burden 100% sens / 82% spec; **NPV 99%** | https://pmc.ncbi.nlm.nih.gov/articles/PMC8021593/ |
| 2021 | LaMonte (Ascension St. Agnes) — *Epilepsia Open* | — | Ceribell reduced diagnosis time (p = .0000006) and on-call workforce demand (p = .02); useful in COVID isolation rooms | https://pmc.ncbi.nlm.nih.gov/articles/PMC8013275/ |
| 2023 | Ward et al. (Cooper/Inspira community hospitals), *Frontiers in Digital Health* | 88 patients | 21% had seizure burden on POC-EEG; **transfers to tertiary center dropped from 2.0 → 1.1/month** (p=0.1); hospital net **saved $13,936/patient** | https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2023.1035442/full |
| 2023 | Villamar, Ayub, Koenig — *Neurocrit Care* | cardiac arrest cohort | Automated seizure detection with Ceribell Rapid-EEG | https://doi.org/10.1007/s12028-023-01681-w |
| 2024 | Kalkach-Aparicio et al. — *Neurology* (SAFER-EEG primary) | multi-center | POC-EEG performed comparably to conventional EEG for 2HELPS2B seizure risk score | https://www.neurology.org/doi/10.1212/WNL.0000000000209621 |
| 2025 | Desai et al. — *Neurocrit Care* (SAFER-EEG sub-analysis) | 283 matched patients | **4.1-day shorter ICU LOS**, 18-pp fewer disabled at discharge, 19h faster EEG acquisition (5.9h vs 25.3h) | https://link.springer.com/article/10.1007/s12028-024-02039-6 |
| 2025 | Puranik et al. — AES Annual Meeting / Neurocrit Care Society poster (cited on ceribell.com) | 1,340 adult Ceribell recordings (multicenter) | Clarity: **96.0% sensitivity, 94.8% specificity, 99.9% NPV** for status epilepticus detection | Cited on ceribell.com (homepage, "Proven AI Performance" block) |
| 2025 | Puranik et al. — retrospective cohort (cited in 2026 JCM review) | 1,148 adult EEGs | Clarity alerts in **19 of 21** SE cases; correctly ruled out seizures in **726 of 727** non-SE recordings | https://pmc.ncbi.nlm.nih.gov/articles/PMC12941532/ (citing Puranik) |
| 2025 | Anand et al. — AES Abstract 2.42 | neonates | Validation of new algorithm for automated seizure detection in neonates and infants | https://aesnet.org/abstractslisting/validation-of-a-new-algorithm-for-automated-seizure-detection-in-neonates-and-infants |
| 2025 | Gupta et al. — AES Abstract 3.204 | peds | Pediatric Clarity: accurate detection of status epilepticus in critically ill children | https://aesnet.org/abstractslisting/pediatric-clarity-a-new-algorithm-to-accurately-detect-status-epilepticus-in-critically-ill-children-using-point-of-care-eeg |
| 2025 | Parvizi et al. — AES Abstract 2.457 | real-world dataset | Evaluating Clarity AI in measuring seizure burden & identifying SE in a large real-world dataset | https://aesnet.org/abstractslisting/evaluating-the-performance-of-clarity-ai-algorithm-in-measuring-seizure-burden-and-identifying-status-epilepticus-in-a-large-real-world-dataset |
| 2026 | Fornari Caprara, Rissardo et al. — *J Clin Med* narrative review | n/a | Compares Ceribell (10-el, gel), Zeto One (21-el, dry, Encevis NeuroPulse), Natus BrainWatch (10-el, Persyst), Nihon Kohden CerebAir (8-el), BrainScope (8-el, TBI) | https://pmc.ncbi.nlm.nih.gov/articles/PMC12941532/ |
| 2025 | Baumgartner et al. — *J Clin Med* review | n/a | Full taxonomy of seizure-detection devices across scalp, subcutaneous, intracranial, cardiac, EMG, ACC, EDA, multimodal | https://pmc.ncbi.nlm.nih.gov/articles/PMC11818620/ |
| 2022 | Biondi et al. — *Epilepsia* systematic review | 23 articles, 14 devices | Median time to start Rapid-EEG Ceribell in ICU = **5 min** | https://pmc.ncbi.nlm.nih.gov/articles/PMC9311406/ |

> Note: Ceribell's headline accuracy of "95% sensitivity, 97% specificity, 99.9% NPV" matches the underlying Puranik et al. 2025 NCS poster (1,340 adults, multicenter, Clarity SE detection) — this is the single number on which the entire sales motion rests. The older Kamousi et al. 2020 paper (Ceribell authors) reported 100%/93%/99% on a smaller 353-record retrospective.

### 2.4 FDA 510(k) clearances (with K-numbers)

| 510(k) # | Year | Indication | Source |
|---|---|---|---|
| **K173570** | 2017 | Initial Ceribell Instant EEG Headband clearance (8-channel adult) | fda.gov (general — confirmed in ClinicalTrialsArena article: "first won clearance from the US Food and Drug Administration (FDA) in 2017") |
| **K203504 / K210805** | 2021 | Ceribell Instant EEG Headband (continued iterations) | https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfpmn/pmn.cfm?ID=K210805 |
| **K223504** | 2022/23 | **Clarity algorithm — adult electrographic status epilepticus (ESE) diagnostic indication** (first 510(k) for ESE in US). Cited on ceribell.com product page ref 6: *"FDA 510k Clearance Letter K223504"* | https://www.accessdata.fda.gov/cdrh_docs/pdf22/K223504.pdf |
| **K241589** | **April 15, 2025** | **Clarity for pediatric patients (ages 1+). "First and only AI-powered point-of-care EEG system cleared to detect electrographic seizures in children as young as 1 year old."** Validated on EEG from **>1,700 pediatric patients** — *"the largest validation dataset ever used for FDA clearance of a seizure detection system."* | https://ceribell.gcs-web.com/news-releases/news-release-details/fda-clears-ceribells-claritytm-algorithm-pediatric-patients |
| **K252070** | **November 2025** | **Clarity for neonates (pre-term → adult). Validated on >700 neonates — "largest neonatal seizure-detection dataset used for regulatory approval to date."** | https://www.massdevice.com/ceribell-fda-nod-neonate-seizure-algorithm/ |
| **K251936** | **December 9, 2025** | **First-of-its-kind delirium monitoring.** Breakthrough Device Designation in 2022; cleared for continuous EEG-based delirium screening & monitoring; validated in 225 adults ≥22 yo. NTAP application submitted to CMS. | https://investors.ceribell.com/news-releases/news-release-details/ceribell-receives-fda-510k-clearance-first-its-kind-delirium/ |
| **TBD (Breakthrough Designation 2025)** | — | Large vessel occlusion (LVO) stroke detection & monitoring — first-in-class | Q4 2025 release |

**Regulatory milestones summary (from Ceribell press):**
- Two FDA **Breakthrough Device Designations** in 2022 (delirium + Clarity/ESE)
- Three FDA clearances in 2025 alone (pediatric, neonatal, delirium)
- NTAP awarded for Clarity's ESE indication (CMS FY 2024 IPPS Final Rule, 88 Fed. Reg. 58927–58930)
- The Ceribell System is the **only** FDA-cleared AI platform with seizure detection spanning **pre-term neonate → adult** at POC.

### 2.5 Competitive positioning (per the 2026 JCM POC-EEG review)

| Device | Electrodes | Channels | AI | Form factor | FDA |
|---|---|---|---|---|---|
| **Ceribell** | 10 | 8 bipolar | Clarity (proprietary, K223504/K241589/K252070) | Soft headband + pocket recorder | Yes (full age range) |
| Zeto One | 21 | Full 10–20 | NeuroPulse (Encevis, AIT) | Wireless headset, dry electrodes | Yes |
| Natus BrainWatch | 10 | Limited montage | Persyst 15 | Wearable wireless, tablet | Yes (Dec 2024) — being sued by Ceribell |
| Nihon Kohden CerebAir / VitalEEG | 8 | Reduced montage | None bundled | Bluetooth wireless headset | Yes (K183529) |
| BrainScope | 8 | Frontal | BFI + SIC (TBI/concussion) | Handheld, battery-powered | Yes (TBI) |
| OpenBCI | 8–16 | Variable | None | Research-oriented | No |

> Verbatim from Fornari Caprara et al. 2026 (J Clin Med, PMC12941532): *"Current AI algorithms tend to perform well at the extremes of seizure burden (>90% or <10%), but are less reliable at detecting EEG abnormalities that are subtle or isolated. Additionally, these systems may misinterpret physiological artifacts or non-seizure EEG patterns such as periodic discharges or triphasic waves, leading to false positives and potentially unnecessary treatment."* — explicit limitation of Ceribell's Clarity architecture.

### 2.6 Where Ceribell explicitly does *not* work (verbatim from literature + their own site)

From PMC12941532 Table 2 (POC-EEG comparison of Ceribell):
> *"Limited spatial coverage with potential to miss focal or parasagittal seizures; false-positive detections reported; AI outputs require clinical correlation; not MRI compatible."*

From Kamousi et al. 2020 (Ceribell-funded author team):
> *"The algorithm is explicitly designed to support rapid bedside decision-making in acute neurological care and is not intended for the detection of isolated epileptiform discharges or brief seizure episodes."* — paraphrased in PMC12941532 §3.2.2.

From the AHA Market Scan (Aug 26, 2025) on Cleveland Clinic's Piramidal collaboration (the next-generation vendor-agnostic competitor):
> *"Piramidal's new tool can scan a full day's worth of EEG (electroencephalogram) data in seconds, a task that now takes trained specialists hours."* — https://www.aha.org/aha-center-health-innovation-market-scan/2025-08-26-4-takeaways-cleveland-clinics-new-ai-co-pilot-brain-icu-care

From Cleveland Clinic Consult QD (Apr 7, 2026):
> *"Unlike AI systems that may be limited by specific hardware, this platform is vendor-agnostic, ingesting and translating data from various EEG machine manufacturers into a universal format for analysis."* — https://consultqd.clevelandclinic.org/harnessing-ai-to-bring-real-time-eeg-interpretation-to-the-icu

Ceribell is **hardware-locked** (you must use their headband), **hospital-locked** (no patient home use), and **acute-locked** (no longitudinal outpatient data).

---

## Section 3 — Pricing & go-to-market

### 3.1 Pricing model

| Component | Mechanism | Source |
|---|---|---|
| **Headband (consumable)** | Per-use; ~$688 per headband (cited verbatim in Ward et al. 2023) | https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2023.1035442/full |
| **Recorder (capital)** | Provided under subscription; recorder is "pocket-size" portable | ceribell.com product page |
| **Cloud / Clarity AI subscription** | Monthly recurring fee per hospital / per recorder | Ward et al. 2023: *"annual fixed cost of the Ceribell® system (monthly subscription fee × 12)"* |
| **NTAP add-on** | CMS-approved New Technology Add-on Payment for Clarity's ESE indication. 30% claims-paid rate in case study ($8,650 / 33 claims) | https://ceribell.com/health-economics/ |
| **Existing CPT codes** | Hospitals bill standard EEG CPT codes for the technical + professional components in addition to headband cost | AMA CPT 2024 Professional Edition, per Ceribell HE page ref 18 |
| **DRG / CC / MCC uplift** | Seizure diagnosis post-Ceribell can upgrade to CC/MCC, increasing DRG payment | Ceribell HE page ref 19 (Eberhard 2023 J Neurosci Nurs) |

**Estimated per-patient hospital economics (from peer-reviewed data):**
- $5k+ average savings per patient (Ceribell white paper)
- $13,936 net gain per patient (Ward et al. 2023 community hospital)
- 4.1-day shorter ICU LOS × ~$2–3k ICU-day cost ≈ $8–12k direct savings
- Avoided transfers save ~$3,463 per patient transferred (Ward et al. 2023)

**Direct list price:** not published. Ceribell does not post a price page — sales motion is enterprise demo + procurement negotiation.

### 3.2 Sales motion & customer segments

- **B2B enterprise / hospital system sales.** Ceribell's "Free Demo" funnel, account-based sales team (Q4 2025 release cites "investments in the company's commercial organization" as primary OpEx growth driver — OpEx $96.5M → $136.7M FY24→FY25).
- **Primary buyers:** Neurocritical Care, ED, Neurology chair → hospital procurement → often ratified by system-level value analysis committee.
- **Reference customers (verbatim from homepage carousel):** UCLA (Vespa), Stanford (Gharahbaghian), Mission Hospital CA (Bader, Dorriz), UT Southwestern (Olson), U. Kansas (Block).
- **Onboarding time:** "minimal training" — applied by any healthcare provider in ~6 minutes (Crunchbase summary); community-hospital study trained 10 critical-care fellows in <1 day each. Hardware install is essentially "stick the headband on" — but hospital integration (EEG portal SSO, NTAP/coding workflow, EHR documentation) typically takes weeks–months.
- **Switching costs (high):**
  - Proprietary disposable headband ($688/unit sunk cost per patient use).
  - Cloud portal workflow integration.
  - Coding/billing workflow built around NTAP/CPT.
  - Nursing/EEG tech training.
  - Subscription lock-in for recorder fleet + Clarity AI.
- **Recent go-to-market expansion:**
  - **Q4 2024–FY2025:** 530 → 647 active accounts (+22%); product revenue +34%, subscription revenue +41% (recurring line growing fastest — sign of SaaS-like maturation).
  - **2025 pediatric → neonatal → delirium launches** unlock incremental TAM CEO estimates at **>$1.5B** (per Q4 2025 release quote).
  - **LVO stroke (Breakthrough Designation)** = next platform extension.

### 3.3 Recent press (last 12 months)

| Date | Headline | Source |
|---|---|---|
| **Apr 15, 2025** | **FDA clears Ceribell's Clarity algorithm for pediatric patients (1+)** | https://ceribell.gcs-web.com/news-releases/news-release-details/fda-clears-ceribells-claritytm-algorithm-pediatric-patients |
| **Jul 7, 2025** | **Ceribell files ITC + D. Del. complaints against Natus Medical** (BrainWatch infringes 6 patents) | https://ceribell.com/about-us/litigation-information-page/ |
| **Aug 26, 2025** | **AHA Market Scan flags Cleveland Clinic + Piramidal partnership** — explicitly competitive to Ceribell; "scans a full day's worth of EEG data in seconds" | https://www.aha.org/aha-center-health-innovation-market-scan/2025-08-26-4-takeaways-cleveland-clinics-new-ai-co-pilot-brain-icu-care |
| **Q3 2025** | FDA Breakthrough Device Designation for LVO stroke detection/monitoring | Q4 2025 release |
| **Nov 2025** | FDA clearance for Clarity in neonates (pre-term → adult) | https://www.massdevice.com/ceribell-fda-nod-neonate-seizure-algorithm/ |
| **Dec 9, 2025** | **FDA 510(k) clearance for first-of-its-kind delirium monitoring (K251936)** | https://investors.ceribell.com/news-releases/news-release-details/ceribell-receives-fda-510k-clearance-first-its-kind-delirium/ |
| **Feb 24, 2026** | Q4 + FY2025 earnings: $89.1M revenue (+36%), 647 accounts | https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial |
| **Apr 7, 2026** | Cleveland Clinic Consult QD publish deep dive on **Piramidal** (not Ceribell) — Dr. Najm: *"It is very costly, it is not scalable and interpretation can be very subjective"* (referring to current EEG practice Ceribell partly addresses) | https://consultqd.clevelandclinic.org/harnessing-ai-to-bring-real-time-eeg-interpretation-to-the-icu |
| **Q1 2026** | Revenue $26.5M (+29%); 680 active accounts | Earnings release |

**Strategic threat to Ceribell:** Piramidal (vendor-agnostic foundation model, trained on ~1M hours of EEG including proprietary Cleveland Clinic data) is positioned as the next generation. Per AHA: *"The model incorporates nearly a million hours of EEG monitoring data from thousands of patients, both neurologically healthy and unhealthy."* — directly competes with Ceribell's hardware-locked AI in the same ICU use case.

---

## Section 4 — Gap analysis on 8 patient pain points

Scoring: **0 = no coverage** · **1 = indirect/peripheral coverage** · **2 = partial coverage** · **3 = strong direct coverage**

(Patient pain points sourced from [[Week 1-2 - Reddit Patient Pain Points]].)

| # | Pain Point | Ceribell Coverage | Reasoning |
|---|---|---|---|
| 1 | **Doctors attribute symptoms to anxiety/psych (PNES misdiagnosis)** | **1 / 3** | Ceribell *objectively* detects non-convulsive seizures, which could in principle reduce PNES misdiagnosis by giving ED/ICU clinicians a hard EEG datapoint. **But:** it is hardware-locked to the hospital — it does nothing for the outpatient whose symptoms are dismissed in a 10-minute clinic visit (the *actual* psych-attribution pain point). A positive Ceribell EEG in an ICU may help that patient downstream, but the user-experience pain (being told "it's anxiety") happens *before* they'd ever reach an ICU. |
| 2 | **13-year diagnostic journeys** | **0 / 3** | Ceribell is acute inpatient only — no outpatient diagnostic pathway, no longitudinal EEG, no patient-facing app, no data export to a patient's neurologist after discharge. A patient with a 13-year journey will likely *encounter* Ceribell only when they finally reach a seizure severe enough to trigger ICU admission. Ceribell makes that ICU admission more accurate; it does nothing to shorten the 13 years before it. |
| 3 | **10-minute appointments** | **0 / 3** | Ceribell is hardware deployed in hospitals. Outpatient clinic appointments are untouched. There is no Ceribell-prescribed workflow for the 10-minute neurology follow-up. |
| 4 | **"Good news, your EEG was normal!"** (ambiguous test dismissal) | **2 / 3** | Ceribell gives more data per admission (continuous seizure-burden trend vs. a one-shot 30-min EEG) and was designed explicitly to *find* what conventional EEG misses — *"55.5% of all seizures... were not documented by the patients"* (Baumgartner et al. 2025, PMC11818620). A normal Ceribell recording has higher negative predictive value (99.9%) than a normal 30-minute conventional EEG. This **indirectly addresses** the dismissal pain point — but again, only for the ICU-admitted patient, not for the outpatient who got the normal 30-min EEG and was sent home. |
| 5 | **Patients punished for self-advocacy** | **0 / 3** | Patient is not in the loop. There is no patient-facing portal, no patient app, no way for the patient to access or share their own Ceribell data. The hospital owns the data. |
| 6 | **Doctors don't see the "between visits" data** | **0 / 3** | Ceribell data lives only as long as the headband is on (acute stay). Once the patient is discharged, the data stream ends. No outpatient longitudinal EEG. No remote monitoring after discharge. No "between visits" capture at all. |
| 7 | **Caregivers are the real information source** | **0 / 3** | No caregiver app, no caregiver login, no caregiver-facing alert. The Brain Stethoscope sonification is for the bedside clinician, not the family member. |
| 8 | **Medical education gap (rare/cryptogenic symptoms dismissed)** | **0 / 3** | Ceribell is a device for credentialed clinicians. No patient/consumer education layer. The 45 peer-reviewed publications cited on ceribell.com are aimed at neurocritical care, not patient empowerment. |

**Composite:** Total = **3 / 24** (~13% coverage of the patient-experience pain-point corpus).

### 4.1 Where Ceribell has the *weakest* coverage = our opportunity

The two pain points where Ceribell has the most absolute and structural zero:

**🎯 Pain Point #2 — "13-year diagnostic journeys" (Coverage: 0/3)**
- Ceribell is locked to the ICU. There is no product, no data flow, and no commercial motion for the patient who is still searching for a diagnosis years into their symptoms.
- The patient-experience wedge: **a longitudinal, outpatient, patient-controlled seizure/EEG diary** that captures inter-visit data and surfaces trends a 10-minute follow-up visit will never see.
- Competitive vacuum: subcutaneous EEG (UNEEG, BrainHome) and behind-the-ear EEG (Epilog, Byteflies) exist in the literature but are research-grade; **no patient-facing consumer EEG product is FDA-cleared or commercially dominant**. Ceribell explicitly has zero outpatient consumer presence.

**🎯 Pain Point #6 — "Doctors don't see the 'between visits' data" (Coverage: 0/3)**
- Same root cause as #2 — Ceribell data is bounded by hospital admission. Once discharged, the seizure burden graph disappears.
- The patient-experience wedge: a way to **carry your seizure-burden signal from ICU → home → clinic**, so the outpatient neurologist sees objective data on what happened between visits, not just patient self-report (which the literature says is missing ~55% of seizures — PMC11818620).
- Competitive vacuum: Apple Watch seizure apps (EpiMonitor, etc.) exist but lack EEG; they detect motion/heart-rate signatures only. Ceribell's superior signal (actual EEG) ends at discharge.

**Secondary weak point (still 0/3):**

**🎯 Pain Point #5 — "Patients punished for self-advocacy" (Coverage: 0/3)**
- Patient is completely absent from the Ceribell workflow. A patient-facing app that lets the patient *see their own seizure-burden trend*, *export it as a PDF for a new neurologist*, and *bring structured data to their next appointment* directly counters the dismissal dynamic — and there is no incumbent.

---

## Section 5 — Summary & capstone implications

### 5.1 What Ceribell is best at

- **Acute seizure triage** in the ICU / ED — fastest-to-deploy limited-montage EEG + most-validated AI for status epilepticus detection.
- **Reducing time-to-EEG** from a national average of ~25h (Desai 2025) to ~6h.
- **Shortening ICU LOS** by 4.1 days on average — a multi-million-dollar hospital-system ROI.
- **Hardware-locked SaaS economics** — high-margin consumable headband ($688) + recurring subscription, both growing (product +34%, subscription +41% in FY2025).

### 5.2 What Ceribell is structurally blind to

- **Outpatient.** Ceribell's headband is for in-hospital use. There is no home version.
- **Patient-facing.** No patient app, no caregiver app, no patient portal.
- **Longitudinal / inter-visit.** EEG data ends at discharge. No outpatient flow.
- **The diagnostic odyssey.** Ceribell helps once you're admitted; it does nothing to get you admitted faster or shorten the years of misdiagnosis before admission.
- **Vendor-agnostic.** Piramidal + Cleveland Clinic are explicitly building the next-generation vendor-agnostic alternative.

### 5.3 The capstone wedge this opens

If our neurology capstone is mapping the AI healthcare landscape for an *unowned wedge* in the patient pain-point corpus:

**Ceribell owns the inpatient seizure-detection cell.** It does not own, and structurally cannot extend into, the **outpatient inter-visit seizure-burden monitoring + patient-facing data ownership** cell. That cell:

1. Maps directly to **pain points #2 (13-year journeys)**, **#5 (self-advocacy punished)**, and **#6 (no "between visits" data)** — three of the eight dominant patient-experience pain points from the Reddit corpus.
2. Has **no FDA-cleared incumbent** (Apple Watch seizure detection is motion/ECG, not EEG; subcutaneous EEG is research-grade; ear-EEG is research-grade).
3. Has a clear **regulatory path** — Ceribell's pediatric/neonatal clearance roadmap proves the FDA will accept AI-based EEG seizure-burden detection at all ages; a consumer/outpatient version follows the same paradigm.
4. Has a **clinical-economic anchor** — the existing NTAP + hospital-system savings framework can be repurposed for outpatient neurology practices (the 10-minute-appointment pain point is the same problem from the other side of the table).

The capstone opportunity is **the patient-facing, outpatient, longitudinal seizure-burden monitor + clinic data handoff** — the cell that sits to the left of Ceribell's ICU headband on the patient journey timeline and that none of the 16 competitors in the Week 1 neurology map currently occupy.

---

## Sources

### Ceribell primary sources
- Homepage: https://ceribell.com/
- Product (POC-EEG): https://ceribell.com/product/point-of-care-eeg/
- Pediatrics page: https://ceribell.com/for-providers/pediatrics/
- Health economics: https://ceribell.com/health-economics/
- Litigation page (v. Natus): https://ceribell.com/about-us/litigation-information-page/

### Ceribell investor relations (SEC-grade data)
- IPO close (Oct 15, 2024): https://investors.ceribell.com/news-releases/news-release-details/ceribell-inc-announces-closing-upsized-initial-public-offering/
- IPO 424B4 (S-1/A): https://www.sec.gov/Archives/edgar/data/1861107/000095017024114320/ceribell_424b4.htm
- Q4/FY2025 earnings: https://ceribell.gcs-web.com/news-releases/news-release-details/ceribell-reports-fourth-quarter-and-full-year-2025-financial
- FDA pediatric clearance (K241589): https://ceribell.gcs-web.com/news-releases/news-release-details/fda-clears-ceribells-claritytm-algorithm-pediatric-patients
- FDA delirium clearance (K251936): https://investors.ceribell.com/news-releases/news-release-details/ceribell-receives-fda-510k-clearance-first-its-kind-delirium/
- SAFER-EEG / LOS press: https://ceribell.com/press_releases/reduction-in-length-of-icu-stays/

### Peer-reviewed Ceribell literature
- Kamousi et al. 2020 *Neurocrit Care* (n=353, Clarity SE detection): https://pmc.ncbi.nlm.nih.gov/articles/PMC8021593/
- LaMonte 2021 *Epilepsia Open* (COVID isolation, time-to-diagnosis): https://pmc.ncbi.nlm.nih.gov/articles/PMC8013275/
- Hobbs et al. 2018 *Neurocrit Care* (Brain Stethoscope, sonification): https://pubmed.ncbi.nlm.nih.gov/29923167/
- Parvizi/Chafe 2018 *Epilepsia* (sonification): https://ceribell.com/wp-content/uploads/2020/11/BRAIN-STETHOSCOPE-Manuscript-Parvizi-594-p877-84-Epilepsia-2018.pdf
- Ward et al. 2023 *Front Digit Health* (community-hospital transfer avoidance, $688 headband): https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2023.1035442/full
- Villamar et al. 2023 *Neurocrit Care* (cardiac arrest): https://doi.org/10.1007/s12028-023-01681-w
- Biondi et al. 2022 *Epilepsia* systematic review (mobile EEG): https://pmc.ncbi.nlm.nih.gov/articles/PMC9311406/

### Third-party reviews and context
- Fornari Caprara, Rissardo et al. 2026 *J Clin Med* (POC-EEG narrative review, PMC12941532): https://pmc.ncbi.nlm.nih.gov/articles/PMC12941532/
- Baumgartner et al. 2025 *J Clin Med* (Seizure Detection Devices, PMC11818620): https://pmc.ncbi.nlm.nih.gov/articles/PMC11818620/
- AHA Market Scan (Aug 26, 2025) on Cleveland Clinic + Piramidal: https://www.aha.org/aha-center-health-innovation-market-scan/2025-08-26-4-takeaways-cleveland-clinics-new-ai-co-pilot-brain-icu-care
- Cleveland Clinic Consult QD (Apr 7, 2026) on Piramidal: https://consultqd.clevelandclinic.org/harnessing-ai-to-bring-real-time-eeg-interpretation-to-the-icu
- Clinical Trials Arena (Jul 2024) on SAFER-EEG: https://www.clinicaltrialsarena.com/news/ceribells-ai-eeg-system-reduces-stay-in-icu-study-finds/
- MassDevice on neonate clearance: https://www.massdevice.com/ceribell-fda-nod-neonate-seizure-algorithm/
- MassDevice on IPO pricing: https://www.massdevice.com/neurotech-company-ceribell-prices-180m-ipo/

### Company profile / funding data
- Tracxn 2026 profile (founded 2014, $188M raised, 403 employees): https://tracxn.com/d/companies/ceribell/__4jETpXx0-qq_faWuBbgxTsbXIVBt2YFBGByqBc_3QGA
- Crunchbase (251-500 employees, NASDAQ:CBLL, founders): https://www.crunchbase.com/organization/ceribell
- Stanford Report (Mar 2018) on Brain Stethoscope founding: https://news.stanford.edu/stories/2018/03/brain-stethoscope-listens-silent-seizures

### Competitive / regulatory
- FDA 510(k) K210805 (headband): https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfpmn/pmn.cfm?ID=K210805
- FDA 510(k) K223504 (Clarity adult ESE): https://www.accessdata.fda.gov/cdrh_docs/pdf22/K223504.pdf
- ITC Investigation 337-1458 (Ceribell v. Natus): https://www.usitc.gov/secretary/fed_reg_notices/337/337_1458_notice08062025sgl.pdf
- Reddit r/neurology critical thread (snippet only — site blocked scraping): https://www.reddit.com/r/neurology/comments/1eq00jr/can_anyone_provide_anecdotes_or_proof_of/