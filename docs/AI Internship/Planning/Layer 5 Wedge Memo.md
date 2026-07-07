---
title: "Layer 5 Wedge Memo — Pre-Visit Synthesis for Neurology"
updated: 2026-07-07 12:05 EDT
tags: [capstone, ai-internship, neurology, strategy, layer-5, wedge]
---

#capstone #ai-internship #neurology #strategy #wedge

# Layer 5 Wedge Memo

**The pre-visit synthesis layer is unowned. That's the wedge.**

This is a 1-page distillation of [[Competitor Teardowns - Cross-Competitor Analysis]] + [[Neurology Subspecialties Map]] + [[Week 1-2 - Reddit Patient Pain Points]]. Read it first, then go to the source docs for evidence.

---

## The problem in one sentence

Every existing neurology AI company helps the doctor *during* or *after* the visit (scribe the note, flag a stroke, detect a seizure) — but **none of them help the doctor *prepare for* the visit.** The doctor walks into the room without having read the chart, the prior imaging, the between-visit symptoms, or the caregiver's observations.

## The evidence (Layer 5 = 0/3 ownership)

| Layer | What it does | Owned by |
|---|---|---|
| 1 | Audio → text (ASR) | Abridge (Whisper-class) |
| 2 | Text → structured note (LLM) | Abridge (multi-model + Linked Evidence) |
| 3 | Imaging → findings | Viz.ai (50+ 510(k)s, LVO/CTP/ASPECTS) |
| 4 | Signals → events | Ceribell (point-of-care EEG, 95% sens / 97% spec) |
| **5** | **Pre-visit synthesis (chart + imaging + wearable + caregiver → briefing)** | **Nobody** |

Cross-competitor 8-pain-point matrix: Abridge covers 2/24, Viz.ai 1/24, Ceribell 1.5/24 — together **4.5/24 (≈19%)**. The unowned 81% is the wedge.

## The 4 pain points no incumbent addresses (verbatim, from Reddit research)

These are the same 4 pain points that all 3 incumbents score **zero** on. They're the seed of the product spec.

**#2 — 13-year diagnostic journeys.** *"In my case, 13 years of being treated by several providers like my symptoms were in my imagination until an MRI + clinical history confirmed it was MS."* — u/occasional_nomad, r/MultipleSclerosis (73 pts). The chart is the diagnosis; nobody summarizes it.

**#6 — Between-visits data is invisible.** Doctors see what happens in the room, not the flares, the heat intolerance, the sleep, the between-seizure events. Wearable + symptom log + diary data exists but isn't pulled into the visit.

**#7 — Caregiver is the real information source.** *"I type up two notes prior to all appointments. The first one is for the front desk staff... The second is for the doctor."* — dementia caregiver, r/dementia. For dementia, stroke recovery, pediatric, ALS — the caregiver is the primary data source. **No scribe includes a HIPAA-compliant caregiver channel.** Cleanest gap in the entire AI healthcare landscape.

**#1 — Psych attribution as default for "I don't know."** *"It is ok when symptoms are puzzling... to just say, 'I don't know', instead of saying 'this must be an anxiety disorder.' The latter statement destroys trust."* — u/Enginerdus, r/MultipleSclerosis (32 pts). The structured symptom timeline that supports an honest "I don't know" verdict (with a differential) is a product, not a sentence.

## Why it's buildable in 8 weeks

Layer 5 doesn't need novel research. It needs:
- **Chart integration** via FHIR (Epic, Cerner) — both have public APIs
- **A specialty prompt library** — 30+ templates, anchored to the 4 pain points above
- **A wearable integration layer** — Apple Watch Movement Disorders API, EpiMonitor, StrivePD are all documented
- **A caregiver channel** — Twilio + a structured intake form + audit log
- **A multi-agent LLM** — per Sorka et al., 89.2% on neurology boards with off-the-shelf GPT-4 + RAG

The wedge is composition, not research.

## Subspecialty shortlist (from the 31-neurology map)

Total opportunity = Prevalence × Pain × Shortage ÷ (AI maturity × Build difficulty). High totals = most leverage.

| Subspecialty | Total | Why |
|---|---|---|
| **Headache / Migraine** | 25 | 47M US patients, AI greenfield, easiest to build, general-neuro chief complaint |
| **Cognitive / Dementia** | 25 | 6.5M US, only 4 geriatric neuro sites, caregiver-in-the-loop maps directly to pain #7 |
| Movement disorders | 15 | UPDRS drift + wearable data; needs StrivePD/Apple integration |
| Epilepsy | 15 | Ceribell/encevis + visit note merge; harder build |

**Recommended path for 8 weeks:** Headache (transcript-only, fastest to ship) **+** caregiver-in-the-loop as a cross-cutting feature (works for cognitive/dementia, stroke recovery, severe MS). The caregiver channel differentiates from every scribe in the market.

## Why Abridge is the acquisition target, not the competitor

Abridge has the strongest position to build Layer 5 — Epic integration (300+ systems), specialty templates (50+), KLAS-leading — but explicitly does **not** own longitudinal chart synthesis, the caregiver channel, or between-visit data. Their CEO (cardiologist Shiv Rao) frames Abridge as "the most initial wedge into a much larger opportunity" — meaning they know Layer 5 is the next move. The right strategy is to build the Layer 5 thin slice, validate it, and become the obvious Layer 5 tuck-in. (This is positioning for the Week 8 deck, not an exit plan.)

## What this memo is NOT

- **Not** a final subspecialty pick — that's still a team decision; the memo says Headache + Caregiver is the recommended path, not the only path
- **Not** an architecture doc — Layer 5 components are listed but not designed; that's Week 3-4 work
- **Not** the Week 8 deck — this is the strategic anchor the deck is built on; the deck is the *delivery* form
- **Not** a market sizing — TAM/SAM/SOM still needs the pricing data from the 3 teardowns, scoped to the chosen subspecialty

## What to do with this memo

1. **First team meeting:** lead with the "0/3 ownership" table + the 4 unowned pain points. Don't lead with subspecialty — that comes after the wedge is shared.
2. **Friend's first doctor interview:** anchor every question to the 4 pain points. If the doctor doesn't see 1-2 of them, the wedge for that subspecialty is weaker than the map suggests.
3. **Ask Amar/Aditya about GastroNote:** send them this memo + the 1-sentence version ("we're building pre-visit synthesis for neurology — are you already there?"). Their answer shapes whether to compete, partner, or pivot.
4. **Week 3 training experiment:** pick the subspecialty *after* the doctor interview validates the 4 pain points for that condition, not before. Headache is the safest bet, but don't anchor to it.

---

## Sources (clickable)

- [[Competitor Teardowns - Cross-Competitor Analysis]] — the 0/3 Layer 5 evidence, full matrix
- [[Competitor Teardown - Abridge]] — 28KB, 6 customer quotes, JAMA 6-system study
- [[Competitor Teardown - Viz.ai]] — 57KB, 11 clinician quotes, NTAP $1,040/use
- [[Competitor Teardown - Ceribell]] — 48KB, 95% sens / 97% spec
- [[Neurology Subspecialties Map]] — 31 subspecialties, 5-dimension scoring
- [[Week 1-2 - Reddit Patient Pain Points]] — 12+ threads, 4 pain points cited above
- [[Week 1 - Neurology Research]] — 16-competitor landscape
- [[Week 1-2 - Research Papers]] — 34 academic papers tiered

Last updated: 2026-07-07 12:05 EDT
