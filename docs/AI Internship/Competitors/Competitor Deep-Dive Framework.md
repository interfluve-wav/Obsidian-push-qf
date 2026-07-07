---
title: Competitor Deep-Dive Framework
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #competitors


How to research competitors in the neurology AI space — what to look for, what they compute, how to compare them.

Companion to "Week 1 - Neurology Research.md" (16-competitor initial map) and "Neurology Subspecialties Map.md" (subspecialty focus decision).

---

## Why deep-dives matter (vs. just listing competitors)

Listing competitors is research theater. A deep-dive answers four questions:

1. **What do they actually compute?** (not "they do AI" — what features, what inputs, what outputs)
2. **What's their technical architecture?** (cloud vs. on-prem, foundation model vs. custom, etc.)
3. **How are they priced and sold?** (B2B vs. B2C, per-provider vs. per-scan, etc.)
4. **What do they not do that we could?** (the gap = our opportunity)

The "what they compute" question is the most important. It tells you exactly which layer of the stack they own.

---

## The 4-step deep-dive process

For each competitor, work through these 4 steps. Set a 2-3 hour budget per company.

### Step 1: Surface scan (30 min)
- Company website: product page, features list, demo video
- Pricing page: do they publish or hide?
- G2 / KLAS / Capterra reviews: 10-20 most-recent reviews
- LinkedIn: headcount growth, recent hires (especially engineers vs. sales)
- Crunchbase: funding, investors, last round
- News: press releases, conference talks, FDA clearances
- YouTube: product demo, KLAS summit talks

**What to capture:**
- One-paragraph company summary (what they do, in plain English)
- Headline features list (3-7 items)
- Pricing model (and your estimate if hidden)
- Funding to date
- Year founded
- Customer count (if disclosed)
- 3 customer quotes (from reviews)

### Step 2: "What do they compute" deep read (60 min)
This is the heart of the deep-dive. For each feature the company offers, answer:
- **Input:** what data goes in (transcript, prior note, lab values, MRI, etc.)
- **Compute:** what model/algorithm processes it (foundation LLM, fine-tuned classifier, custom CNN, etc.)
- **Output:** what the doctor/patient sees (note draft, alert, summary, score, etc.)
- **Latency:** is it real-time, near-real-time, or batch?
- **Accuracy/eval:** do they publish any accuracy numbers, validation studies, or third-party evals?

**Sources for "what they compute":**
- Their engineering blog (most don't have one — that's a red flag)
- Published papers (Abridge and DeepScribe both have validation papers; find them)
- FDA 510(k) summary (the public "substantial equivalence" document lists exactly what the device measures)
- Patents (Google Patents, Lens.org — surprisingly informative)
- Whitepapers they publish
- Conference talks (CHIME, HIMSS, AES, AAN)
- Job postings (the tools they use show up in job reqs)
- GitHub (rare for health AI, but some do open-source components)

**What to capture:**
- Architecture diagram (sketch it)
- Per-feature I/O table
- List of all published evaluation results (accuracy, sensitivity, specificity, etc.)
- List of all FDA clearances (with 510(k) number)

### Step 3: Pricing & go-to-market (30 min)
- Direct: per provider/mo, per encounter, per hospital site, per scan
- If hidden: estimate from job postings, KLAS data, public customer references
- Sales motion: top-down (enterprise CIO) vs. bottom-up (individual doctor signs up)
- Onboarding time: days? weeks? months?
- Switching costs: how locked-in is the customer?
- Net revenue retention: do they publish? (most don't)
- Recent pricing changes: any rumors of increases?

**What to capture:**
- Pricing model + your estimate
- Sales motion description
- Onboarding time
- Switching cost assessment
- Recent press on pricing or business model changes

### Step 4: Gap analysis (30 min)
For each of the 8 patient pain points (from "Week 1-2 - Reddit Patient Pain Points.md"), answer:
- Does the competitor fix this? (Yes / Partially / No)
- How do they fix it? (one sentence)
- What do they not fix? (one sentence)

**The 8 pain points to score each competitor on:**
1. Doctors attribute symptoms to anxiety/psych rather than "I don't know"
2. 13-year diagnostic journeys
3. 10-minute appointments, no listening
4. Dismissive comments on ambiguous test results
5. Patients punished for self-advocacy
6. Doctors don't see the "between visits"
7. Caregivers are the real information source
8. Medical education gap

**What to capture:**
- A scored matrix: competitor × pain point (Yes/Partial/No + one-sentence how)
- The 2-3 pain points where no competitor has any coverage
- The 1 pain point where this competitor has unique coverage (their moat)

---

## What competitors compute (taxonomy of the 5 layers)

Every neurology AI company fits into one or more of these 5 layers. Use this as your mental model.

### Layer 1: Audio capture → text (the "ears")
- Examples: Abridge, DeepScribe, Nuance DAX, Freed, Nabla
- **Compute:** speaker diarization, medical ASR, sentence segmentation
- **Inputs:** ambient audio, microphone
- **Outputs:** timestamped transcript, optionally with speaker labels
- **What they own:** the audio → text pipeline
- **What they don't:** clinical reasoning, chart integration, longitudinal data

### Layer 2: Text → structured clinical note (the "writer")
- Examples: same as above, plus DeepCura
- **Compute:** LLM (OpenAI, Anthropic, Google, or proprietary) with specialty prompts
- **Inputs:** transcript, sometimes prior note
- **Outputs:** SOAP note, specialty note (H&P, neuro exam, etc.)
- **What they own:** the prompt engineering + LLM routing
- **What they don't:** the prior chart, the imaging, the EEG, the home data

### Layer 3: Imaging → findings (the "eyes")
- Examples: Viz.ai, RapidAI, Brainomix, Aidoc, NeuroQuant, Cercare
- **Compute:** 3D CNNs, transformer U-Nets, foundation vision models
- **Inputs:** DICOM MRI/CT/CTA, sometimes clinical context
- **Outputs:** LVO detection, ASPECTS, perfusion volumes, lesion segmentation
- **What they own:** the imaging AI model + FDA-cleared indication
- **What they don't:** the clinic note, the patient conversation, the longitudinal trajectory

### Layer 4: Signals → events (the "nervous system")
- Examples: Ceribell, Natus, encevis, Piramidal, Neuro Event Labs, Empatica, Rune Labs, Apple Movement Disorders
- **Compute:** 1D CNNs, RNNs, GNNs on time-series
- **Inputs:** EEG (scalp or intracranial), EMG, accelerometer, EDA, ECG
- **Outputs:** seizure detection, event annotation, wearable stream analytics
- **What they own:** the signal processing + clinical event detection
- **What they don't:** the in-clinic synthesis, the chart integration

### Layer 5: Pre-visit synthesis (the "briefing")
- **Examples: literally nobody owns this layer**
- **Compute:** RAG over chart + imaging + signals + transcript, multi-agent LLM
- **Inputs:** the full longitudinal record
- **Outputs:** "this is who this patient is, what they came in for, what's been missed"
- **This is the wedge**

The vendors that own Layer 1-2 are not Layer 5. The vendors that own Layer 3-4 are not Layer 5. **Nobody is Layer 5.** That's us.

---

## The "what do they compute" output template

For each competitor, fill this in:

```
COMPETITOR: [name]
URL: [homepage]
FOUNDED: [year]
FUNDING: [$X, last round YYYY]
CUSTOMERS: [# estimated]
PRICING: [$X/provider/mo OR enterprise quote OR free]

WHAT THEY COMPUTE:
  Layer 1 (audio→text): [yes/no, which model]
  Layer 2 (text→note): [yes/no, which model, what templates]
  Layer 3 (imaging): [yes/no, which modality, what indication]
  Layer 4 (signals): [yes/no, which modality, what events]
  Layer 5 (pre-visit synthesis): [yes/no]

FDA CLEARANCES: [list with 510(k) numbers]
PUBLISHED EVALS: [list with links]

PAIN POINTS ADDRESSED (out of 8):
  1. Anxiety/psych attribution: [Yes/Partial/No] — [how]
  2. 13-year diagnostic journeys: [Yes/Partial/No] — [how]
  3. 10-min appointments: [Yes/Partial/No] — [how]
  4. Dismissive test result comments: [Yes/Partial/No] — [how]
  5. Patients punished for self-advocacy: [Yes/Partial/No] — [how]
  6. Doctors don't see between-visit data: [Yes/Partial/No] — [how]
  7. Caregivers are real info source: [Yes/Partial/No] — [how]
  8. Medical education gap: [Yes/Partial/No] — [how]

MOAT: [what they uniquely do that nobody else can easily copy]
WEAKNESS: [what's clearly missing from their product]

GAPS THAT ARE OUR OPPORTUNITY:
  - [pain point X] — they don't address this, nobody does
  - [pain point Y] — they address it but poorly
```

Save this to a file called `Competitor Teardown - {name}.md` in the AI Internship folder, or as a single `Competitor Teardowns.md` with all 16 companies.

---

## The 3 deep-dive targets for Week 2

You don't have time to deep-dive all 16. Pick 3 — one per category (scribe, imaging, signals).

### Scribe: pick Abridge
- Why: most-validated (published papers, KLAS awards, 6 health system JAMA study)
- Most likely to be the incumbent everyone compares against
- Public financials, multiple press cycles, clear pricing model
- 2025 Best in KLAS, $200M+ funding

### Imaging: pick Viz.ai
- Why: most-cited neurology AI company
- Clear technical architecture (LVO detection on CTA)
- 1,700+ hospitals = clear adoption signal
- Door-to-puncture metric is the canonical outcome measure
- $100M+ funding

### Signals: pick Ceribell
- Why: most-clinically-deployed EEG AI in the US
- Hardware + software wedge (clearer than pure-software plays)
- Cleveland Clinic collaboration
- Clear point-of-care positioning (vs. lab-based EEG)
- Multiple published studies

For each, follow the 4-step process above. Allocate 2-3 hours each.

---

## What about competitors we don't deep-dive?

For the other 13 (DeepScribe, Nuance DAX, Suki, Freed, Nabla, Heidi Health, DeepCura, RapidAI, Brainomix, Aidoc, NeuroQuant, Cercare, Rune Labs StrivePD, Empatica EpiMonitor, Natus autoSCORE, encevis, Neuro Event Labs, Piramidal):

- Do the 30-min surface scan (Step 1) only
- Fill in the "what they compute" template
- Score on the 8 pain points
- Save to a single "Competitor Quick Scans.md" doc

The deep-dive is where you win. The surface scan is for the slide deck.

---

## Where to find the "what they compute" information

| Source | What it tells you | How to access |
|---|---|---|
| Company engineering blog | Architecture, models used | google "[company] engineering blog" |
| Published validation papers | Accuracy, methodology | PubMed, Google Scholar, company site |
| FDA 510(k) database | Cleared indications, performance | https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfpmn/pmn.cfm |
| Patents | Architecture, claims | https://patents.google.com/, Lens.org |
| Job postings | Tech stack, models, tools | LinkedIn, company careers page |
| GitHub | Open source components | github.com |
| Conference talks (HIMSS, CHIME, AAN, AES) | Architecture, customer stories | YouTube, conference proceedings |
| Whitepapers / case studies | Customer outcomes, deployment | Company site, KLAS Research |
| Hacker News / r/MachineLearning | Technical discussion, criticism | search "[company] reddit" |
| Healthcare AI news (STAT, MedCity, FierceHealthcare) | Funding, partnerships, criticism | news sites |

---

## Common competitor research mistakes

- **Mistake 1: reading only the website.** Companies may not be completely honest on their websites. Validate with third-party sources.
- **Mistake 2: confusing "AI" with "actually works."** Many AI companies have beautiful demos and 5 paying customers. Look for adoption signals (KLAS, G2, public customer counts)
- **Mistake 3: ignoring what they don't do.** The gap is the opportunity. Spend at time to deep-dive on analyzing the opportunity gap.
- **Mistake 4: not pricing the competitor.** If you can't estimate their price, you can't estimate their market.
- **Mistake 5: reading the same competitor's pitch deck twice.** Read 3 different sources on each company.
- **Mistake 6: skipping the FDA database.** 510(k) summaries are the most objective source on what an AI device actually does. Every clinical AI company has one.
- **Mistake 7: comparing on features, not on outcomes.** "They have templates" is a feature. "Templates improve missed-finding rate from 53% to 92%" is an outcome. Outcomes are what you need.

---

## After Week 2: how to use these teardowns

The teardowns are inputs to:
- The 5-force competitive analysis (in Week 5-6 business track)
- The market sizing model (in Week 4 business track)
- The "why we're different" slide (in Week 8 presentation)
- The pricing model (in Week 5-6 business track)
- The "Big Vision" framing (in Week 8 presentation)

You will reference these teardowns in every subsequent week. Make them good.

---

## The "Big Vision" framing, validated

After deep-diving 3 competitors, the pre-visit synthesis (Layer 5) framing should sharpen into something like:

> "No existing neurology AI company owns the **pre-visit synthesis layer** — the briefing the doctor sees before walking into the room. Scribes (Abridge, DeepScribe) own the audio-to-text pipeline but don't pull the chart. Imaging AI (Viz.ai, RapidAI) own the imaging analysis but don't write the visit note. Wearables (Rune Labs, Empatica) own the data stream but don't surface findings in the encounter. **Nobody combines them into a single synthesis the neurologist uses to prepare for a visit.** That's the wedge."

This framing should be on the first slide of your Week 8 deck.

---

## Deliverables (to be saved in AI Internship folder)

| File | What it contains |
|---|---|
| `Competitor Teardowns.md` | 3 deep-dives (Abridge, Viz.ai, Ceribell) + 13 quick scans |
| `Competitor Comparison Matrix.md` | Cross-competitor comparison on the 8 pain points |
| `Competitor Pricing Model.md` | All 16 competitor prices (or estimates) + your pricing model |
| `Competitor Architecture Diagrams.md` | Sketches of each competitor's technical architecture |
| `What Competitors Compute.md` | Layer 1-5 mapping for each competitor |

Allocate Week 2 to these. Aim for completion by end of Week 2.

---

## One more thing: read the actual users

For each top 3 competitor, read 10-20 actual user reviews on G2, KLAS, or Capterra. Capture verbatim quotes — these are the *real* feature gaps, not the ones you imagined.

User reviews tell you:
- What the marketing claims
- What the product actually does
- What users are frustrated with
- What users want next

This is the closest you can get to "voice of customer" without running your own survey.

---

## Sources for competitor research

- Company websites (16 listed in "Week 1 - Neurology Research.md")
- FDA 510(k) database: https://www.accessdata.fda.gov/scripts/cdrh/cfdocs/cfpmn/pmn.cfm
- KLAS Research: https://klasresearch.com/
- G2: https://www.g2.com/
- Capterra: https://www.capterra.com/
- Crunchbase: https://www.crunchbase.com/
- LinkedIn: company pages
- Google Patents: https://patents.google.com/
- PubMed: https://pubmed.ncbi.nlm.nih.gov/
- arXiv: https://arxiv.org/
- STAT News: https://www.statnews.com/
- MedCity News: https://medcitynews.com/
- FierceHealthcare: https://www.fiercehealthcare.com/