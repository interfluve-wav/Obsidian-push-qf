#capstone #ai-internship #neurology #concept #ms-scale

---

# EDSS — Expanded Disability Status Scale

---

## What EDSS Is

The **Expanded Disability Status Scale (EDSS)** is the gold-standard clinical assessment tool for quantifying disability severity in **multiple sclerosis (MS)**. Developed by Kurtzke in 1983, it remains the most widely used MS disability measurement in both clinical practice and clinical trials.

The EDSS scores range from 0 (no disability) to 10 (death due to MS), in 0.5-point increments. The scale is based on a neurological examination across eight functional systems:
- Visual
- Brainstem
- Pyramidal
- Cerebellar
- Sensory
- Bowel and bladder
- Cerebral/Mental
- Other

A patient's EDSS score is determined by the highest rating in any functional system plus ambulation status.

---

## Key EDSS Milestones

| EDSS Score | Clinical Meaning |
|---|---|
| 0.0 | No neurological abnormalities |
| 1.0–2.5 | Minimal disability, fully ambulatory |
| 3.0–4.5 | Moderate disability, still fully ambulatory |
| 5.0–5.5 | Disability severe enough to impair daily activities; may need a cane |
| 6.0–6.5 | Requires walking assistance (cane, crutch, walker) |
| 7.0–7.5 | Wheelchair-bound |
| 8.0–9.5 | Bed-bound |
| 10.0 | Death due to MS |

---

## Why EDSS Matters for AI Medical Scribes

Like [[Concept - UPDRS|UPDRS]] for Parkinson's, the EDSS is a **longitudinal disease severity tracker** that sits outside the encounter-level note. The EDSS score from the last visit, and the trajectory over 6–12 months, tells the neurologist whether the patient is stable, improving, or declining — and whether to escalate treatment.

**Why Abrige doesn't own this:** An ambient scribe captures the conversation and drafts the note. It does not:
- Prompt the neurologist to administer the EDSS
- Store and track EDSS scores across visits
- Compute whether the patient's EDSS has changed by 0.5 or more points (the clinically meaningful threshold)
- Flag a patient for MS disease-modifying therapy escalation

A **pre-visit synthesis** layer could do exactly this — pull the last 5 EDSS scores, compute the trajectory, and surface: "Patient's EDSS has increased by 1.5 points in 8 months — discuss escalation."

---

## Related

- [[Concept - UPDRS]]
- [[Concept - MIDAS]]
- [[Competitor Teardown - Viz.ai]]
- [[Competitor Teardown - Ceribell]]
