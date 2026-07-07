---
title: Concept - MIDAS
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #concept #migraine-scale

---

# MIDAS — Migraine Disability Assessment Questionnaire

---

## What MIDAS Is

The **Migraine Disability Assessment Questionnaire (MIDAS)** is a brief, validated questionnaire used to measure the degree of disability caused by migraine headaches. It quantifies how many days of work, household work, and social activities are impaired by migraine over a 3-month period.

The MIDAS score classifies migraine disability into four grades:
- **Grade I** (0–5): Little or no disability
- **Grade II** (6–10): Mild disability
- **Grade III** (11–20): Moderate disability
- **Grade IV** (21+): Severe disability

---

## MIDAS Questions

The questionnaire asks how many days in the past 3 months:
1. Missed work or school due to headaches
2. Productivity at work or school reduced by half or more
3. Missed household work or chores
4. Productivity in household work reduced by half or more
5. Missed social activities

Days where the person was in bed count as the full 24 hours.

---

## Why MIDAS Matters for AI Medical Scribes

MIDAS is one of the most commonly used **patient-reported outcome measures (PROMs)** in neurology headache clinics. It is often administered at the start of a visit via a paper questionnaire or an EHR-integrated intake form.

**The problem it solves:** Migraine is a episodic condition — the doctor doesn't observe a migraine attack in the office. The MIDAS captures the patient's headache burden over time, enabling the doctor to understand:
- How frequent are the headaches?
- How disabling are they?
- Is the patient deteriorating over months?

**Why Abrige doesn't own this:** Abrige sees only the in-visit conversation. It does not:
- Administer the MIDAS questionnaire before the visit
- Track MIDAS scores longitudinally (was it Grade IV, now Grade II?)
- Alert the doctor if MIDAS is worsening despite treatment
- Correlate MIDAS trends with medication changes

A **pre-visit synthesis tool** could automate MIDAS collection, track the trajectory, and surface: "MIDAS has worsened from Grade II to Grade IV in 3 months — patient has missed 18 work days. Consider medication review."

---

## Related

- [[Concept - UPDRS]]
- [[Concept - EDSS]]
- [[Competitor Teardown - Viz.ai]]
- [[Competitor Teardown - Ceribell]]
