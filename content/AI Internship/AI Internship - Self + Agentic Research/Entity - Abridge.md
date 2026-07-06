#capstone #ai-internship #neurology #competitors #entities

---
title: Abridge
entity_type: organization
tags: [abridge, ambient-ai, clinical-documentation, AI-scribe, healthcare-AI, unicorn]
---

## Overview

Abridge is a San Francisco–based clinical AI company founded in 2018 by Dr. Shiv Rao (practicing cardiologist and CEO). The company builds ambient AI documentation systems that listen to clinical conversations in real time and generate structured medical notes (SOAP notes and specialty formats) for physician review and EHR entry. As of 2025, Abridge processes over 1 million clinical encounters per week across 150+ health systems, supports 28+ languages and 50+ specialties, and was named Best in KLAS 2025.

## Key Facts

- **Founded:** 2018
- **Headquarters:** San Francisco, CA
- **CEO:** Shiv Rao, MD (practicing cardiologist; still takes monthly weekend hospital shifts)
- **CTO / Chief Science Officer:** Zachary C. Lipton, PhD (also associate professor at Carnegie Mellon University)
- **COO:** Julia Chou (former Google)
- **CFO:** Sagar Sanghvi (former CFO of Instacart)
- **CPO:** Mario Queiroz (former Google)
- **General Counsel:** Tim Hwang (former Google)
- **CCO:** Brian Wilson (healthcare veteran)
- **Funding:** $250M Series D (2025), led by Elad Gil and IVP; prior rounds include unnamed investors
- **Valuation:** $2.75B (post-Series D)
- **2025 KLAS:** Best in KLAS winner (clinical documentation)
- **Scale:** 100+ health systems; 1M+ encounters/week; 28+ languages; 50+ specialties
- **Notable customers:** Mayo Clinic, Johns Hopkins Medicine, Duke Health, Memorial Sloan Kettering, UNC Health, Christus Health, UChicago Medicine, Endeavor Health, Inova Health System, Akron Children's

## Technical Architecture (Layer 1 + 2)

Abridge owns **Layer 1 (audio→text)** and **Layer 2 (text→note)** of the 5-layer AI taxonomy — the ambient documentation pipeline.

**Layer 1 — ASR:**
- Proprietary medically tailored ASR model
- Performs speaker diarization and timestamp alignment
- Internal benchmark WER: 12.7% (vs. 24% relative reduction vs. other medical ASR models)
- 81–83% relative reduction in error on new medications vs. off-the-shelf models
- On generic speech: comparable to Whisper v3 (OpenAI)
- Medical Term Recall: 97% (internal benchmark)

**Layer 2 — Note Generation:**
- LLM-based pipeline: transcript → drafted clinical note
- Draws reasonable inferences from clinical context
- Post-generation guardrails: proprietary hallucination/confabulation detection + self-correction (trained on 50,000+ examples; validated with 1,000+ physician hours)
- Confabulation catch rate: 97% vs. GPT-4o's 82% (internal benchmark)
- Linked Evidence: surfaces transcript segment supporting each note claim for clinician verification
- All notes reviewed by clinician before EHR entry

**Multilingual:** 28+ languages; Spanish WER 3.1% vs. 6.2% English; >80% of English medical term recall rate in non-English note generation

**Layer 3–5:** None (Abridge does not own imaging AI, signals/EEG AI, or pre-visit synthesis)

## Evaluation Process

Abridge has a published 4-stage evaluation pipeline:
1. Automated metrics (WER, MTR, precision/recall on medical concepts) + clinician spot-checks
2. Blinded head-to-head trials with licensed clinician adjudicators (anytime-valid sequential hypothesis testing)
3. Staged release (alpha early adopters → broader rollout)
4. Ongoing post-deployment: edit-rate tracking + star ratings (4.3/5 English average) + qualitative feedback

See: [[Source - Abridge AI Evaluation Whitepaper]], [[Source - Abridge Confabulation Elimination Whitepaper]]

## Products

- **Physician ambient documentation:** real-time audio → SOAP note, specialty notes; 50+ specialties
- **Nurse ambient documentation (pilot with Mayo Clinic + Epic):** discrete forms/flow sheets format (vs. narrative); in development as of summer 2024
- **Linked Evidence:** clinician-facing transcript-to-claim linking for verification
- **Enterprise integration:** Epic-first strategy (DeepEpic partnership), also integrated with other major EHRs

## Pricing

Not publicly disclosed. Estimated from framework: enterprise per-provider/per-month (typical for AI scribe category: ~$200–400/provider/month). KLAS data and Inova contract details would provide concrete figures.

## Competitive Position

Abridge is the **incumbent in AI clinical documentation** — most validated (published papers, KLAS awards, 6-health-system JAMA study), most funded ($250M Series D), highest valuation ($2.75B). Primary competitors: DeepScribe, Nuance DAX (Microsoft), Suki, Nabla, Freed, Numa (formerly Healthsparq's ambient), Heidi Health.

Abridge does **not** address Layer 5 (pre-visit synthesis). The gap between visits, caregiver context, and longitudinal chart synthesis is unoccupied — this is the opportunity space.

- [[Source - Trelis Medical ASR Benchmarks]] — 16-model benchmark on 3 custom medical ASR datasets (MultiMed Hard, EKA Hard, Medical Terms 2025). Gemini 2.5 Pro + Scribe v2 lead; Whisper Large V3 best open-source; Google open-source Med ASR near Whisper Tiny. MultiMed ST fine-tuning generalizes poorly (April 2026)

## Role in Research

Abridge is the **reference competitor** for the AI scribe layer. Its evaluation methodology (blinded trials, staged release, post-deploy monitoring) is the most rigorous published in the space. Its confabulation taxonomy provides a useful framework for thinking about hallucination severity in any LLM-generated clinical text. Its nurse expansion is a forward indicator of where ambient documentation is heading.

Sources: [[Source - Abridge AI Evaluation Whitepaper]], [[Source - Abridge Confabulation Elimination Whitepaper]], [[Source - Becker's Abridge Profile]], [[Source - Trelis Medical ASR Benchmarks]], [[Competitor Teardown - Abridge]]
