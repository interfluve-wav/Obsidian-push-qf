---
title: "Concept — WER (Word Error Rate)"
draft: false
tags:
  - concept
  - ai-internship
  - neurology
  - evaluation-metric
description: "WER: the standard ASR accuracy metric, what 12.7% means in practice, and why WER alone isn't enough for medical AI evaluation."
---

# WER — Word Error Rate

---

## What WER Is

**Word Error Rate (WER)** is the standard industry metric for measuring how accurately a speech recognition system transcribes spoken words into text. It is expressed as a percentage — lower is better.

**WER = (Substitutions + Deletions + Insertions) / Total Words**

Where:
- **Substitution** — a word was transcribed as a different word ("aspirin" → "aspiran")
- **Deletion** — a word was missed entirely ("patient takes aspirin daily" → "patient takes daily")
- **Insertion** — a word was added that wasn't spoken ("patient takes aspirin" → "patient takes V aspirin")

---

## Why WER Is Important for Medical AI

In clinical documentation, a WER of 10% sounds acceptable in casual terms. But consider what 10% means in practice:

- A 10-minute conversation at ~150 words per minute = ~1,500 words
- 10% WER = **150 words transcribed incorrectly**
- One wrong drug name, one wrong dosage, one wrong body part — any of these could be clinically significant

For medical ASR, the target WER is generally **below 5–10%** on clinical conversations, with best-in-class systems hitting **8–13%** on in-domain medical benchmarks.

Abridge reports a WER of **12.7%** on their internal medical benchmark — meaning roughly 1 in 8 words is wrong in their transcription. This sounds high, but the comparison is against other medical ASR systems, where Abridge achieves a **24% relative reduction** in WER.

---

## WER vs. Other Metrics

| Metric | What it measures | Best for |
|---|---|---|
| **WER** | Word-level accuracy | Overall transcription quality |
| **CER** | Character-level accuracy | Medical terms, drug names, dosages |
| **MTR** | Medical Term Recall | Whether critical medical terms are captured correctly |
| **Accuracy** | Correct words / total words | General performance (inverse of WER) |

Abridge reports both WER and **MTR (Medical Term Recall) of 97%** — meaning 97% of medical terms are correctly recalled/transcribed, even when the broader WER is 12.7%.

This distinction matters: WER captures all errors equally, while MTR focuses on whether the clinically important terms (medications, diagnoses, procedures) made it through.

---

## WER in the Abridge Benchmarks

From the Abridge AI Evaluation Whitepaper and Abridge Confabulation Elimination Whitepaper:

- Abridge internal WER on clinical conversations: **12.7%**
- 24% relative reduction vs. other medical ASR models
- 83% relative reduction in error on new medications specifically
- 15% relative improvement on accented English

The **83% reduction on new medications** is striking — it means Abridge's medical fine-tuning specifically improved accuracy on medication names, which are often the most clinically consequential transcription errors.

---

## Limitations of WER

WER treats all words as equally important. A substitution of "ibuprofen" → "iron" is clinically catastrophic; a substitution of "a" → "the" is irrelevant. WER cannot distinguish between these cases.

For medical AI evaluation, WER should be paired with:
- [[Concept - CER]] — character-level accuracy for medication dosages, lab values
- [[Concept - MTR (Medical Term Recall)]] — Medical Term Recall specifically for clinically critical vocabulary
- Human clinician review of generated notes

---

> [!info]- Related
> [[Concept - ASR]] · [[Concept - CER]] · [[Abridge|Abridge Teardown]]
