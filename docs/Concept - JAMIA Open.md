---
title: "Concept — JAMIA Open"
draft: false
tags:
  - concept
  - ai-internship
  - neurology
  - clinical-trial-design
description: "JAMIA Open: health informatics journal, and the Tierney et al. KUMC study methodology caveats."
---

# JAMIA Open — Journal / Study Design Concept

---

## What JAMIA Open Is

**JAMIA Open** (*Journal of the American Medical Informatics Association Open*) is a peer-reviewed, open-access journal published by the BMJ Group in partnership with the American Medical Informatics Association (AMIA). It focuses on applied health informatics research — the science of how information technology is used in healthcare delivery.

It is considered a **credible, peer-reviewed source** for clinical informatics research, including quality improvement studies on digital health tools like AI scribes.

---

## Why JAMIA Open Is Relevant Here

The **Tierney et al. study** (2025) was published in JAMIA Open. This is the KUMC quality improvement study that provides the 81% / 77% / 73% / 67% / 64% satisfaction figures for Abridge.

While JAMIA Open is not as high-impact as JAMA, it is a **specialty informatics journal** — its peer reviewers are domain experts in health informatics, making the methodology more likely to be scrutinized for informatics-specific concerns (study design, measurement validity, bias).

---

## Important Study Design Notes

The Tierney et al. KUMC study has several methodological nuances worth understanding:

**1. Quality improvement study, not an RCT**
It was designed as an internal quality improvement initiative, not a randomized controlled trial. This means:
- No randomized assignment
- No control group
- Results are observational/directional, not causal

**2. Non-identical pre/post surveys**
The pre-implementation survey (8 items) and post-implementation survey (11 items) had different questions. Only **2 items were directly comparable**:
- "I find my current documentation workflow easy to use" → "Abridge has made my documentation workflow easy to use"
- "I usually complete the note before the next patient visit" → "With Abridge, I could complete the note before the next patient visit"

The 81%, 77%, 73%, etc. figures come from **post-implementation survey responses only** — the percentage of respondents who agreed or strongly agreed with each statement after using Abridge. They are not computed pre/post changes.

**3. Selection bias**
Early adopters of AI documentation tools may have been more favorable toward technology and less burned out at baseline — limiting generalizability.

**4. Single institution**
KUMC is one institution — academic, Midwestern, early adopter culture.

---

## The 2 Statistically Computed Pre/Post Comparisons

These are the only two findings with computed statistical comparisons:

| Finding | Result |
|---|---|
| Documentation workflow easy to use | 6.91× higher odds post-intervention (P<.001) |
| Note completed before next patient | 4.95× higher odds post-intervention (P<.001) |

---

> [!info]- Related
> [[Concept - KUMC]] · [[Concept - JAMA Network Open]] · [[Concept - Mini-Z Burnout Scale]] · [[Abridge|Abridge Teardown]]
