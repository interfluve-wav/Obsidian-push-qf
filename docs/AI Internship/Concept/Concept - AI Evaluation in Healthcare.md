---
title: Concept - AI Evaluation in Healthcare
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #concepts

---
title: AI Evaluation in Healthcare
tags: [ai-evaluation, clinical-AI, metrics, WER, MTR, ambient-documentation, ASR, validation]
---

## Definition

AI evaluation in healthcare refers to the structured process of assessing whether AI-generated clinical outputs (notes, transcriptions, diagnoses, alerts) are accurate, safe, and fit for clinical use. Unlike generic AI benchmarks, healthcare AI evaluation requires domain-specific metrics, clinician involvement, staged deployment, and ongoing post-market surveillance — because errors have direct patient safety consequences.

## How It Appears in Sources

### Abridge's 4-Stage Evaluation Pipeline ([[Source - Abridge AI Evaluation Whitepaper]])

**Stage 1: Automated Metrics + Clinician Spot-Checks**
- Automated metrics: WER (word error rate) for ASR, Medical Term Recall (MTR) for ASR, precision/recall of medical concepts for note generation
- Stratified by patient subpopulation (demographics from EHR integration)
- Clinician spot-checks on curated encounter sets: coarse quality signal for subjective dimensions

**Stage 2: Blinded Head-to-Head Trials**
- Software platform presents notes side-by-side (current system vs. candidate)
- Reviewers blinded to which system authored each note
- Anytime-valid sequential hypothesis testing: false-positive-rate-controlled, allows early stopping when results are conclusive
- Adjudicated by licensed clinicians

**Stage 3: Staged Release**
- Alpha release: limited to trained early adopters in frequent contact with Abridge staff
- In-vivo verification on selected cohorts before broader rollout
- Active (comments + star ratings) and passive (edit rate) feedback collected at every stage

**Stage 4: Ongoing Post-Deployment Monitoring**
- Edit-rate tracking: passive, inherently scalable (editing is natural workflow)
- Star ratings: 1–5 within note-editing UI
- Qualitative free-text feedback → blind spot identification
- Language-stratified analyses (requires model-driven language identification proxy)
- [[Source - Abridge Confabulation Elimination Whitepaper|Confabulation elimination]] as a specialized evaluation sub-discipline

### Linked Evidence ([[Source - Abridge AI Evaluation Whitepaper]])
- Tool that surfaces relevant transcript excerpt for each claim in the generated note
- Used by clinicians for verification during editing
- Also used by Abridge's internal audit team for efficiency in quality audits

## Key Metrics in Clinical AI

| Metric | Full Name | What It Measures | Used For |
|--------|-----------|-----------------|----------|
| WER | Word Error Rate | Minimum word edits / reference length | ASR/transcription quality |
| MTR | Medical Term Recall | Fraction of medical terms captured | ASR clinical fidelity |
| Precision | — | Fraction of generated terms that are correct | Note generation quality |
| Recall | — | Fraction of reference terms captured | Note generation completeness |
| CER | Character Error Rate | Character-level edit distance on specific entities (vs. full sentence) | Medical ASR benchmark specificity |
| Confabulation catch rate | — | % of unsupported claims detected by guardrail system | Guardrail/system efficacy |

## Debates / Open Questions

- **What is an acceptable WER in clinical settings?** Generic speech WER benchmarks don't account for medical terminology. Medical WER benchmarks are proprietary and non-standardized across vendors.
- **Inference vs. hallucination:** Where does a "reasonable inference" (e.g., "diabetes" from metformin+HbA1c discussion) become a confabulation requiring flagging? Abridge addresses this with a 5-category support axis, but the boundary remains subjective.
- **Clinician review as backstop vs. reliable safeguard:** If clinicians routinely skip review (time pressure, interface design), the "clinician reviews before EHR entry" safeguard weakens substantially.
- **Internal benchmarks vs. third-party validation:** All Abridge benchmark figures (WER, MTR, confabulation catch rates) are from internal/private benchmarks — no independent replication available.

## Connected To
[[Entity - Abridge]], [[Source - Abridge AI Evaluation Whitepaper]], [[Concept - Hallucination Elimination]]
