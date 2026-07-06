#capstone #ai-internship #neurology #subspecialties

# Neurology Subspecialties Map

All 31 neurology subspecialty fellowships per AAN/ACGME/UCNS, with prevalence, AI maturity, opportunity assessment, and recommended wedge.

This is the *first* decision you make as a team: which subspecialty to focus on for 8 weeks. Use this map to narrow from "neurology" to 1-2 specific conditions.

---

## How to read this map

Each subspecialty is scored on 5 dimensions (1-5 scale, 5 = best):

| Dimension | What it measures |
|---|---|
| **US prevalence** | How many patients (1=rare <100K, 5=>10M) |
| **AI maturity** | How saturated the AI market is (1=greenfield, 5=fully saturated) |
| **Pain severity** | Patient-reported pain intensity per Reddit research |
| **Doctor shortage** | How underserved the subspecialty is (5=most undersupplied) |
| **Build difficulty** | How hard for us to ship in 8 weeks (1=trivial, 5=needs imaging+signals+EHR) |

**Total opportunity = Prevalence × Pain × Shortage ÷ (AI maturity × Build difficulty)**

A high total = the most leverage.

---

## The 31 subspecialties (ACGME + UCNS accredited + non-accredited)

### Tier 1 — Highest opportunity (recommended starting points)

| Subspecialty | Sites | US prevalence | AI maturity | Pain | Shortage | Build | Total | Wedge |
|---|---|---|---|---|---|---|---|---|
| **Headache / Migraine** | 41 UCNS | 47M (2nd highest DALY globally) | 1 (greenfield) | 5 (massive dismissal) | 5 (3,700 needed vs. 500) | 1 (transcript-only) | **25** | Scribe + pre-visit synthesis, no imaging layer |
| **Movement disorders (PD, ET, dystonia)** | 48 | 1M Parkinson's, 7M ET | 2 (StrivePD, Cala Health) | 5 (UPDRS drift, dyskinesia) | 4 (4,000+ wait lists per Reddit) | 3 (chart + wearable) | **15** | Trajectory tracking + wearable merge |
| **Epilepsy** | 77 ACGME | 3.4M US, 50M global | 2 (Ceribell, encevis) | 5 (EEG dismissal = gaslighting) | 3 | 3 (chart + EEG) | **15** | EEG-visit synthesis, seizure calendar |
| **Multiple sclerosis** | 20 | 1M US | 3 (NeuroQuant, multiple DMTs) | 5 (13-year diagnostic journeys) | 3 | 2 (chart + MRI) | **10** | Trajectory + lesion tracking |
| **Cognitive / Behavioral / Dementia** | 35 (BNNP), 4 (geriatric) | 6.5M Alzheimer's, 100K FTD | 2 (Cortechs) | 5 (caregiver pain, 4-year diagnostic) | 5 (only 4 geriatric neuro sites) | 2 (chart + caregiver) | **25** | Caregiver-in-the-loop, longitudinal |

### Tier 2 — Solid opportunities

| Subspecialty | Sites | US prevalence | AI maturity | Pain | Shortage | Build | Total | Wedge |
|---|---|---|---|---|---|---|---|---|
| **Vascular neurology / Stroke** | 99 ACGME | 800K strokes/yr, 7M survivors | 5 (Viz, RapidAI, Brainomix, Aidoc all 510k'd) | 4 | 3 | 5 (imaging + workflow) | **3** | Saturated — skip unless you have a fresh angle |
| **Neuromuscular** | 49 | 200K ALS, 200K+ others | 1 | 4 | 4 | 3 (chart + EMG) | **8** | Niche, but underserved |
| **Neurocritical care** | 70 (UCNS+ACGME) | (ICU subset) | 2 (Ceribell, Piramidal) | 4 | 3 | 4 (real-time signals) | **6** | Real-time ICU EEG, hard to ship |
| **Sleep medicine** | 84 | 70M sleep disorder sufferers | 1 (mostly dental devices) | 3 | 2 | 2 (chart + sleep study) | **6** | Big market but not "neurology" in the AI sense |
| **Pain medicine** | 104 | 50M chronic pain | 1 | 4 | 3 | 1 (chart only) | **12** | Generalist, less neuro-specific |
| **Clinical neurophysiology** | 89 | (EMG/EEG labs) | 1 | 3 | 3 | 3 (chart + signals) | **3** | Technical, narrow |
| **Neuro-oncology** | 34 | 25K primary brain tumors/yr, 200K+ metastatic | 3 (Cercare, NeuroQuant) | 5 (high mortality) | 3 | 4 (chart + MRI + path) | **8** | High-stakes, hard wedge |
| **Autonomic disorders** | 5 UCNS | rare | 1 | 4 | 5 (only 5 sites) | 2 (chart + vitals) | **8** | Very niche but underserved |
| **Neuroimmunology** | (under MS) | (under MS) | 3 | 5 | 3 | 3 (chart + MRI + labs) | **8** | Overlap with MS |

### Tier 3 — Lower opportunity for our 8 weeks

| Subspecialty | Sites | Why lower |
|---|---|---|
| Endovascular Surgical Neuroradiology | 2 ACGME | Pure stroke, saturated |
| Neuroimaging / Neuroradiology | 5 UCNS | Imaging AI is mature, hard to differentiate |
| Brain Injury Medicine | 1 ACGME | Too small |
| Clinical Neuromuscular Pathology | 5 UCNS | Pathology, not clinical |
| Neural Repair and Rehabilitation | 0 UCNS | Doesn't exist as fellowship |
| Neurohospitalist | 2 | Acute care, hard wedge |
| Balance Disorders, Neuropharmacology, Neurogenetics, etc. | 0 | Too small |

---

## Three conditions worth zooming into

### 1. Headache / Migraine (Total: 25)

**Why this is the strongest starting point:**
- 47M US patients — biggest prevalence of any neuro condition
- 3,700 headache specialists needed vs. 500 currently → severe shortage
- 70% of migraine patients are undiagnosed or under-treated
- Reddit research shows massive patient pain: "brushed off," "yelled at," "told to drink water"
- Most chief complaint in general neurology visits (general neuro is mostly headache)
- AI market is greenfield (no major incumbent)
- Easiest to build: transcript-driven, no imaging needed
- Reimbursement: high (Headache is one of the most common reasons for neuro referral)

**Patient pain (verbatim from Reddit research):**
- "10-minute appointment, told to take vitamins, drink more water"
- "Overheard my neurologist laugh at my appointment when I asked for a headache specialist"
- "She literally told you to look at your scans then got annoyed that you had looked at your scans"
- 15+ data points per headache visit (onset, location, quality, severity, frequency, aura, triggers, alleviating factors, etc.)

**The wedge:**
- Pre-visit synthesis: pull prior visit data, MIDAS scores, abortive/preventive response, red flag screening
- Generate the "structured headache note" (the 15+ data points)
- Surface "this patient is on tier 3 preventives and still has 12 headache days/month — what next?"
- Trigger specialist referral automatically when criteria met

**Competitors to study:**
- DeepCura ($129/mo, claims neuro templates) — closest direct competitor
- Abridge, DeepScribe — generic, no headache templates
- Mayo Clinic, Cleveland Clinic — academic headache programs, no AI

**Risk:** No device data, no imaging, no signals — wedge is mostly software. Lower defensibility than movement disorders or epilepsy.

### 2. Movement disorders (Total: 15)

**Why this is strong:**
- 1M Parkinson's patients, 7M essential tremor
- UPDRS scoring is required at every visit (manual, time-consuming, error-prone)
- Apple Watch Movement Disorders API gives tremor/dyskinesia stream
- Rune Labs StrivePD owns the device side but not the in-clinic synthesis
- Patient pain: caregiver burden, off-time, dyskinesia side effects, no real-time medication adjustment

**Patient pain (verbatim from Reddit research):**
- "Mom, 82, new neurologist thinks she doesn't have Parkinson's. This is after 13 years of treatment."
- "From living independently, driving, shopping to 24/7 care, can't walk, can't use the bathroom, can't feed herself"
- "The diagnosis of parkinson's is still very much a subjective process of ruling out very bad brain conditions first, then finding the medicine that relieves parkinson's symptoms. There is no definitive test that proves a person has parkinson's disease."

**The wedge:**
- Pre-visit synthesis: pull UPDRS, medication response, wearable tremor/dyskinesia data
- Generate the "movement disorder visit note" with quantitative trajectory
- Surface "UPDRS has drifted +0.5 over 18 months, medication wearing off increasing — consider DBS eval"
- In-clinic: capture the UPDRS exam as discrete data (tremor, rigidity, bradykinesia, postural stability)

**Competitors to study:**
- Rune Labs StrivePD — owns wearable
- Apple Movement Disorders API — owns tremor/dyskinesia capture
- Medtronic, Abbott, Boston Scientific — own DBS
- Cala Health — owns non-invasive stim for ET
- NeuroQuant — owns MRI volumetrics

**Risk:** Need to integrate with wearable APIs (StrivePD has, Apple Watch does). Higher build difficulty than headache.

### 3. Cognitive / Dementia (Total: 25)

**Why this is the highest social-impact play:**
- 6.5M Alzheimer's patients in US, projected to 13M by 2050
- Only 4 geriatric neurology fellowship sites in the whole US
- Caregiver is the real information source (per Reddit research)
- 4-year average diagnostic journey, often misdiagnosed
- 75% of dementia caregivers report high stress
- HIPAA makes caregiver information flow awkward
- AAN workforce report explicitly calls this the most undersupplied subspecialty

**Patient pain (verbatim from Reddit research):**
- "I type up two notes prior to all appointments. The first one is for the front desk staff... The second is for the doctor."
- "Sit yourself behind her so the doctor can see you. That way you can nod to confirm or shake your head if it's not true and she will never know."
- "Dementia falls into geriatric specialties! THESE are the doctors that have the knowledge and tools to deal with dementia." (her internist was useless)
- "My mom proceeded to wreak complete havoc on the drive home. Hitting my dad, trying to pull the steering wheel..."

**The wedge:**
- Caregiver-in-the-loop: structured intake for the caregiver (the one who knows the patient)
- Pre-visit synthesis: prior MMSE/MoCA scores, behavioral changes, ADL/IADL drift
- Generate the "dementia visit note" with cognitive trajectory
- Surface "MMSE dropped 4 points in 18 months, behavioral changes in last 3 months, consider medication adjustment"
- Side benefit: HIPAA-compliant caregiver communication channel

**Competitors to study:**
- Cortechs NeuroQuant (volumetric MRI)
- Cognito Therapeutics (sensory stimulation)
- Eli Lilly / Eisai (Lecanemab, Donanemab — but these are drugs, not software)
- Most memory clinics use paper-based caregiver intake

**Risk:** Long sales cycle (geriatric clinics, memory care centers), FDA considerations if you touch any clinical decision support.

---

## The recommended path: 2-subset focus

If you want maximum leverage in 8 weeks, focus on:

**Subset 1 (primary): Headache / Migraine**
- Easiest to build
- Largest patient pool
- Greenfield AI market
- Direct overlap with what your friend is researching (general neuro chief complaint is mostly headache)

**Subset 2 (cross-cutting feature): Caregiver-in-the-loop**
- Works for cognitive/dementia, stroke recovery, ALS, severe MS
- Differentiates from every scribe in the market (none of them include the caregiver)
- Maps to the highest pain point in the Reddit research
- HIPAA-compliant structured communication channel is a defensible product feature

**Why not just movement disorders or just MS?** They're solid but narrower, and your friend is interviewing general neurologists who see mostly headache. Headache gets you the most doctor-interview data and the most patient-side data (47M patients).

---

## Quick-reference scoring table

| Subspecialty | Prevalence | AI maturity (1=greenfield, 5=saturated) | Pain | Shortage | Build | Total |
|---|---|---|---|---|---|---|
| Headache/Migraine | 5 | 1 | 5 | 5 | 1 | **25** |
| Cognitive/Dementia | 4 | 2 | 5 | 5 | 2 | **25** |
| Movement disorders | 4 | 2 | 5 | 4 | 3 | **15** |
| Epilepsy | 3 | 2 | 5 | 3 | 3 | **15** |
| Multiple sclerosis | 3 | 3 | 5 | 3 | 2 | **10** |
| Pain medicine | 4 | 1 | 4 | 3 | 1 | **12** |
| Neuromuscular | 2 | 1 | 4 | 4 | 3 | **8** |
| Autonomic | 1 | 1 | 4 | 5 | 2 | **8** |
| Neuro-oncology | 2 | 3 | 5 | 3 | 4 | **8** |
| Neurocritical | 2 | 2 | 4 | 3 | 4 | **6** |
| Sleep | 4 | 1 | 3 | 2 | 2 | **6** |
| Stroke / Vascular | 4 | 5 | 4 | 3 | 5 | **3** |
| Clinical neurophysiology | 2 | 1 | 3 | 3 | 3 | **3** |

**Top 5 to consider:** Headache, Cognitive/Dementia, Movement disorders, Epilepsy, MS.

**Bottom line:** skip stroke, skip clinical neurophysiology, skip anything where AI maturity is 4 or 5 (saturated). The highest-leverage moves are in conditions with greenfield AI markets and severe doctor shortages.

---

## How this maps to your 8-week plan

| Week | Headache track | Dementia track | Movement disorders track |
|---|---|---|---|
| 1 | Map 20-30 competitors (mostly scribe) | Map 20-30 competitors (Cortechs, Cognito) | Map 20-30 competitors (Rune, Apple, Medtronic) |
| 2 | Doctor interviews (general neurologists, headache specialists) | Doctor interviews (geriatric neuro, memory clinics) | Doctor interviews (movement disorder specialists) |
| 3 | Label Studio on headache transcript data | Label Studio on caregiver intake data | Label Studio on UPDRS scoring data |
| 4 | Pain point survey (Migraine Impact, MIDAS) | Caregiver burden survey (Zarit Burden Interview) | UPDRS / MDS-UPDRS scoring review |
| 5-6 | Pre-visit synthesis architecture | Caregiver-in-the-loop architecture | Wearable + chart synthesis architecture |
| 7 | Deliverables check | Deliverables check | Deliverables check |
| 8 | Demo: headache note generation + red flag screening | Demo: caregiver note → clinical summary | Demo: wearable data + chart → UPDRS drift alert |

---

## Sources

- AAN fellowship directory: https://www.aan.com/Fellowship
- ABMS subspecialty certificates: https://www.abms.org/member-boards/specialty-subspecialty-certificates/
- Sarva et al., BMC Medical Education 2021 (PMC7891131): status of neurology fellowships
- AAN Workforce Task Force Report (Neurology 2013, 2017, 2021): 19% shortage by 2025
- Industry payments in neurology (PMC7458713): which subspecialties get pharma $$
- Burden of disease: Global Burden of Disease study 2019, via AAN
- Singer Lab NeuroTech list: https://singer.gatech.edu/neurotech-list/
- AAN 2021 compensation report: https://www.aan.com/siteassets/home-page/tools-and-resources/practicing-neurologist--administrators/benchmarking-data/neurology-compensation--productivity/21_ncp_report.pdf
- AAN shortage report (NeurologyLive coverage): https://www.neurologylive.com/view/the-grave-threat-posed-by-the-shortage-of-neurologists
- mdedge: https://mdedge.com/neurology/article/58501/health-policy/neurology-shortfall-worsen-2025