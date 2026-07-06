#capstone #ai-internship #neurology #concept #speech-recognition

---

# ASR — Automatic Speech Recognition

---

## What ASR Is

**Automatic Speech Recognition** (ASR) is the technology that converts spoken language into written text. Every time you use a voice assistant, dictate to your phone, or get a transcript from an audio recording, ASR is doing the work.

In healthcare, ASR is the foundational technology that powers ambient AI scribes. The clinical conversation is recorded as audio, the ASR system transcribes it to text, and the AI scribe then processes that text into a structured clinical note.

---

## Why ASR Matters for Medical Scribes

Standard ASR models (like consumer dictation tools) perform poorly on medical conversations because:

- **Medical terminology** — drug names (Levothyroxine, dapagliflozin), disease names (Huntington's, sarcoidosis), procedure names (SPECT CT, polysomnography)
- **Multi-speaker conversations** — distinguishing the doctor from the patient from a caregiver in the same recording
- **Accented English** — non-native speakers, regional accents
- **Background noise** — clinical environments are noisy (monitors, other staff, exam room acoustics)
- **Spontaneous speech** — patients don't speak in clean sentences; they interrupt, backtrack, use colloquialisms

Medical-grade ASR models are fine-tuned on clinical audio to handle these challenges specifically.

---

## ASR Metrics

The two most common ways to measure ASR accuracy:

**WER — Word Error Rate**
The percentage of words incorrectly transcribed. Lower is better. A WER of 10% means 1 in 10 words is wrong.

- Abrige's internal WER: **12.7%** (on their own medical benchmark)
- 24% relative reduction vs. other medical ASR models
- 15% relative improvement on accented English

**CER — Character Error Rate**
The percentage of characters (letters, numbers) incorrectly transcribed. More granular than WER; useful for catching small but clinically significant errors (e.g., "metformin 500" vs. "metformin 50").

- Used in the [[Source - Trelis Medical ASR Benchmarks]] for evaluating medical term accuracy
- [[Concept - AI Evaluation in Healthcare]] has a metrics comparison table

---

## ASR in the Abrige Stack

```
Patient + Clinician Audio
        ↓
  Medical ASR (fine-tuned, Whisper-class)
        ↓
  Timestamped Transcript
        ↓
  LLM → Structured Clinical Note
```

Abrige uses a **custom ASR pipeline fine-tuned on medical vocabulary**, built on a Whisper-class foundation model. Their internal benchmarks show:
- 83% relative reduction in errors on new medications (vs. off-the-shelf models)
- WER 12.7% on clinical conversations
- Medical Term Recall (MTR): **97%**

---

## ASR Landscape (Medical)

Key players in medical ASR:
- **Abrige** — proprietary medical ASR, fine-tuned
- **Whisper (OpenAI)** — open-source base model; fine-tuned versions used by many vendors
- **Nuance DAX** — Dragon Medical One ASR backbone + OpenAI GPT-4
- **DeepScribe** — custom medical ASR
- **Amazon MedicalScribe** — AWS medical transcription service
- **Google Cloud Speech-to-Text Medical** — domain-specific medical ASR API

The [[Source - Trelis Medical ASR Benchmarks]] has comparative WER/CER data across 16 models including Whisper variants, Gemini 2.5 Pro + Scribe, and domain-specific models.

---

## Related

- [[Concept - WER]]
- [[Concept - CER]]
- [[Source - Trelis Medical ASR Benchmarks]]
- [[Concept - AI Evaluation in Healthcare]]
- [[Competitor Teardown - Abrige]]
