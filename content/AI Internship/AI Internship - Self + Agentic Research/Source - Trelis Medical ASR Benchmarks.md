#capstone #ai-internship #neurology #sources

---
title: "Best Medical Transcription (ASR) Models" — Trelis Research
source_type: blog_post
date_ingested: 2026-07-01
url: https://trelis.substack.com/p/best-medical-transcription-asr-models
original_date: April 9, 2026
author: Ronan (Trelis Research)
tags: [ASR, speech-recognition, medical-transcription, benchmarks, Whisper, Gemini, Scribe, Speechmatics, Trelis]
---

## Summary

Trelis Research (April 9, 2026) benchmarks 16 proprietary and open-source ASR models across 3 custom medical benchmarks. Key finding: Google's proprietary model and Eleven Labs' Scribe v2 lead; Whisper Large V3 is the best general-purpose open-source model. Domain-specific fine-tuning (MultiMed ST) shows poor generalization to accented speech and recent terminology. All 3 datasets are public on Hugging Face under `Trelis Medical`.

## The 3 Benchmarks

**MultiMed Hard** — 50 hardest rows from YouTube medical content (MultiMed dataset). Entity CER (character error rate on medical terms only, not full sentence). Difficulty selected via median CER across Whisper Large, Canary, and Voxtral Mini.

**EKA Hard** — 50 hardest rows from Indian-accented English (EKA dataset, medical students reading prepared scripts with pharmaceutical + Indian-market medical terms). Tests generalization beyond American English.

**Medical Terms 2025** — 50 synthetic examples of terms newly appearing in 2025 FDA/EMA/WHO sources. Tests model knowledge of recent medical terminology (near/after many models' training cutoffs). Generated via LLM → Kokoro TTS.

## Model Performance

### MultiMed Hard (YouTube medical content)
| Model | Entity CER | Notes |
|---|---|---|
| Scribe v2 (Eleven Labs) | **13.4%** | Best overall |
| Gemini 2.5 Pro | High | |
| Ursa 2 Enhanced (Speechmatics) | High | |
| Whisper Large V3 | High | Top open-source |
| Nova V3 | High | |
| Whisper Large Turbo | Lower | |
| Whisper Small | Lower | |
| Parakeet Universal 3 Pro (AssemblyAI) | Lower | |
| Canary (Nvidia) | Lower | |
| Whisper 3 (Fireworks) | Lower | |
| Voxtral | Low | |
| Med ASR (Google open source) | Low | Near Whisper Tiny |
| Whisper Tiny / Base | Lowest | |

**Key:** MultiMed ST (fine-tuned on MultiMed training set) performed well on this benchmark (in-distribution) but dropped significantly on EKA Hard (out-of-distribution), scoring similarly to Whisper Small.

### EKA Hard (Indian-accented English)
| Model | Notes |
|---|---|
| Gemini 2.5 Pro | Lowest entity CER |
| Scribe v2 | Close second |
| Parakeet | Notably better here than on MultiMed |
| Speechmatics Ursa | |
| Universal 3 Pro (AssemblyAI) | |
| Nova 3 | |
| Whisper Large V3 / Turbo | Very close |

### Medical Terms 2025 (recent terminology)
| Model | Notes |
|---|---|
| Gemini 2.5 Pro | Best |
| Scribe v2 | Close second |
| Universal 3 Pro | |
| Whisper Large V3 (Fireworks + direct) | |
| Canary Turbo | |

Speechmatics models ranked lower on this benchmark. Google open-source Med ASR performed below even Whisper Tiny — significantly underperforming Google's proprietary model.

## Key Findings

1. **Google proprietary >> Google open-source Med ASR.** Google's proprietary ASR leads; the open-source Med ASR ranks near the bottom, close to Whisper Tiny. This is a significant gap within the same organization.

2. **Domain-specific fine-tuning generalizes poorly.** MultiMed ST (fine-tuned on MultiMed training data) scored well on in-distribution test data but fell to Whisper Small–level on Indian-accented speech and recent terms. Domain-specific training ≠ generalizable medical ASR.

3. **Whisper Large V3 is the best general open-source model.** Despite being older, Whisper Large V3 generalizes well across all 3 medical benchmarks. A strong foundation for custom fine-tuning rather than training from scratch.

4. **Best models achieve 10–20% entity CER on hardest cases.** On easy/general cases, error rates are much lower. These benchmarks specifically selected the hardest 50 rows — they differentiate models, not represent typical performance.

5. **Eleven Labs Scribe v2 is the top proprietary model for medical ASR.** Scribe v2 leads MultiMed Hard at 13.4% entity CER and is competitive on the other two benchmarks.

6. **Accented speech remains a challenge.** Gemini 2.5 Pro leads on EKA Hard (Indian-accented), demonstrating superior accent robustness.

## How to Access

All 3 datasets + full prediction results per model per benchmark are on Hugging Face under the **Trelis Medical** collection: search "Trelis medical" on huggingface.co.

## Connected Pages

[[Entity - Abridge]], [[Source - Abridge AI Evaluation Whitepaper]], [[Concept - AI Evaluation in Healthcare]]
