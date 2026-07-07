---
title: Concept - UPDRS
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #concept #parkinsons-scale

---

# UPDRS — Unified Parkinson's Disease Rating Scale

---

## What UPDRS Is

The **Unified Parkinson's Disease Rating Scale (UPDRS)** is the gold-standard clinical assessment tool for measuring the severity of Parkinson's disease (PD) symptoms. It is used in both clinical practice and clinical trials to track disease progression and treatment response over time.

The UPDRS has four parts:
- **Part I** — Mentation, behavior, and mood (e.g., cognitive impairment, depression, hallucinations)
- **Part II** — Activities of daily living (e.g., speech, handwriting, walking, tremor)
- **Part III** — Motor examination (e.g., bradykinesia, rigidity, tremor, gait)
- **Part IV** — Motor complications (e.g., dyskinesias, motor fluctuations, "off" episodes)

Each part is scored on a scale, and the total score ranges from 0 (no impairment) to 199 (severe impairment).

---

## Why UPDRS Matters for AI Medical Scribes

The UPDRS is a **longitudinal disease severity score** — it must be administered in person by a neurologist and takes 15–30 minutes. No AI scribe can automate this.

However, the UPDRS is exactly the kind of structured, time-series data that a pre-visit synthesis system should pull together and present to the doctor before the appointment. A patient's UPDRS trajectory over the last 5 visits tells a clinically meaningful story:
- Is the patient declining despite treatment?
- Are dyskinesias getting worse?
- Is the patient spending more time in the "off" state?

**Why Abrige doesn't own this:** Abrige captures the encounter-level note. It does not aggregate UPDRS scores across visits, compute the trajectory, or surface a trend alert. This is a gap in the chronic disease monitoring layer — exactly the space a pre-visit synthesis tool could fill.

---

## UPDRS in Neurology Practice

In movement disorder neurology (a subspecialty of neurology), the UPDRS is:
- Used at every visit for PD patients
- Required in most PD clinical trials
- The basis for ON/OFF motor fluctuation tracking
- A key input for deep brain stimulation (DBS) candidacy decisions

**Key scale scores:**
- 0–10: Mild/no impairment
- 11–20: Mild-moderate
- 21–30: Moderate
- 31–60: Moderate-severe
- 61+: Severe

---

## Related

- [[Competitor Teardown - Ceribell]]
- [[Competitor Teardown - Viz.ai]]
- [[Concept - EDSS]]
- [[Concept - MIDAS]]
