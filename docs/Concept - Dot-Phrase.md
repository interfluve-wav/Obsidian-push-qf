---
title: "Concept — Dot-Phrase"
draft: false
tags:
  - concept
  - ai-internship
  - neurology
  - EHR-helper
description: "Dot-phrase: EHR documentation shortcuts, how they work in the Abridge workflow, and why they create switching costs."
---

# Dot-Phrase — EHR Documentation Shortcut

---

## What a Dot-Phrase Is

A **dot-phrase** (also called a smart-phrase or dot-word) is a short text shortcut that automatically expands into a longer, pre-formatted block of clinical text within an electronic health record (EHR) system.

- **Typed:** `.hpisec`
- **Expands to:** the History of Present Illness section template with standard headings and prompts

Dot-phrases are one of the most widely used time-saving tools in clinical documentation. They are especially common in:
- Emergency medicine
- Primary care
- Specialty clinics with high patient volume

---

## How Dot-Phrases Work in the Abridge Workflow

In the KUMC study of Abridge's implementation, dot-phrases are the mechanism by which Abridge-drafted notes are inserted into the Epic EHR:

1. Abridge generates the clinical note (SOAP format, H&P format, etc.)
2. The clinician reviews and edits the Abridge draft in the Abridge web editor
3. The clinician types a dot-phrase (e.g., `.hpisec`, `.assessment`) in Epic
4. The dot-phrase pulls the corresponding Abridge-drafted section into the Epic note template
5. The clinician signs the note in Epic

```
Clinician types in Epic:  .hpisec
        ↓
Epic expands:  [Abridge-drafted HPI section]
        ↓
Clinician signs the note
```

---

## Common Dot-Phrases

| Dot-Phrase | Expands to |
|---|---|
| `.hpisec` | History of Present Illness section |
| `.meds` | Current medications section |
| `.pe` | Physical exam section |
| `.assessment` | Assessment and plan section |
| `.ap` | Assessment and plan (shorter) |
| `.cc` | Chief complaint |

Each clinician or health system can customize their dot-phrase library — this is why **switching AI scribes is hard**: the dot-phrase library is built around a specific vendor's note section structure.

---

## Dot-Phrases as a Switching Cost

This is a key competitive dynamic: once a health system builds a dot-phrase library mapped to Abridge's note sections, switching to a competitor requires rebuilding that library from scratch.

**Example:** If a physician is used to typing `.hpisec` to pull the HPI from Abridge, and they switch to a competitor whose note sections are structured differently, they need to:
- Learn new dot-phrase codes
- Remap their entire workflow
- Retrain their muscle memory
- Potentially rebuild templates in Epic

This is a significant **behavioral switching cost** on top of the technical switching cost.

---

> [!info]- Related
> [[Concept - Epic]] · [[Concept - SMART-on-FHIR]] · [[Abridge|Abridge Teardown]]
