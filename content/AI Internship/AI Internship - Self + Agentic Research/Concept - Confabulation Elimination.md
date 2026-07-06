#capstone #ai-internship #neurology #concepts

---
title: Confabulation Elimination
tags: [confabulation, hallucination, factuality, guardrails, LLM, clinical-AI, Abridge]
---

## Definition

Confabulation elimination (as defined by Abridge) is the systematic reduction of unsupported factual claims in AI-generated clinical documentation to near-zero. Unlike the generic term "hallucination," confabulation elimination distinguishes among multiple claim types (reasonable inference, questionable inference, unmentioned, contradiction) and severity levels (major, moderate, minimal) to enable targeted detection and correction. The goal is not to eliminate all inference, but to eliminate unsubstantiated extrapolation that could harm patient care.

## How It Appears in Sources

### Abridge's 2-Axis Taxonomy ([[Source - Abridge Confabulation Elimination Whitepaper]])

**Axis 1: Support** (degree of transcript substantiation)
1. **Directly Supported:** precise match with transcript, no deviations
2. **Circumstantially Supported / Reasonable Inference:** logically follows, most clinicians would agree
3. **Circumstantially Supported / Questionable Inference:** plausible but other interpretations equally plausible
4. **Unmentioned:** neither stated nor inferable; most clinicians would agree no transcript support
5. **Contradiction:** directly conflicts with transcript

**Axis 2: Severity** (only for unsupported claims)
- **Major:** most clinicians agree would likely negatively impact care and/or cause substantial harm if uncorrected
- **Moderate:** some negative impact plausible but unlikely to cause substantial harm
- **Minimal:** little to no impact on care, even if uncorrected

### Example: "Prozac vs. Lexapro" Correction
- Patient: "Prozac I think?" → "Actually wait, no, not Prozac, it's Lexapro, sorry"
- Draft note incorrectly: "Patient has been taking **Prozac** for depression for the last two years"
- System detects confabulation: contradicts self-correction in transcript
- System corrects: "Patient has been taking **Lexapro** for depression for the last two years"
- Linked Evidence surfaces the transcript excerpt for clinician verification

### Guardrail Architecture ([[Source - Abridge Confabulation Elimination Whitepaper]])
1. **Detection LM:** proprietary task-specific model, 50,000+ training examples (open-source hallucination detection + domain-specific clinical scenarios), trained with 1,000+ physician annotation hours
2. **Self-correction system:** takes detected claim + reasoning → chooses: correct to align with context / delete entirely / false alarm (keep)
3. **Clinician review backstop:** all notes reviewed before EHR entry

**Benchmark result:** Abridge catches 97% of confabulations; GPT-4o catches 82% (6× more missed). Internal benchmark on 10,000+ realistic encounters.

## Why "Confabulation" vs. "Hallucination"

Abridge deliberately avoids "hallucination" because it implies a black-and-white phenomenon. In clinical documentation, many unsupported claims exist on a spectrum — from reasonable inference (clinically appropriate) to unsubstantiated extrapolation (potentially harmful). Treating all as equal obscures the nuance needed to build precise detection systems and misleads clinical users about what they're dealing with.

## Debates / Open Questions

- **The inference boundary is contested:** Not all clinicians agree on where reasonable inference ends and unsubstantiated extrapolation begins. This limits inter-rater reliability on the "Questionable Inference" category.
- **Severity is also subjective:** "Most clinicians would agree" is the standard for Major vs. Moderate classification — but clinical disagreement on edge cases is common.
- **Clinician review dependency:** The system is positioned as near-elimination, but if review is superficial (time pressure), the actual error rate entering the EHR is unknown.
- **Internal benchmarks:** The 97% vs. 82% figures are from Abridge's private benchmark — no independent replication. The "6× more missed" framing is from Abridge's own marketing.
- **Broader industry:** Abridge's taxonomy is proprietary; no industry standard for hallucination/confabulation classification exists in clinical AI yet.

## Connected To
[[Entity - Abridge]], [[Source - Abridge Confabulation Elimination Whitepaper]], [[Concept - AI Evaluation in Healthcare]]
