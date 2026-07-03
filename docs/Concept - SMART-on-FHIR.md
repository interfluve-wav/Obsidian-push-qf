---
title: "Concept — SMART-on-FHIR"
draft: false
tags:
  - concept
  - ai-internship
  - neurology
  - interoperability-standard
description: "SMART-on-FHIR: the open EHR integration standard that enables third-party apps like Abridge to read schedules and write clinical notes."
---

# SMART-on-FHIR — EHR Integration Standard

---

## What SMART-on-FHIR Is

**SMART-on-FHIR** is an open standard that allows third-party healthcare software applications to securely access and interact with electronic health record (EHR) systems. It combines two standards:

- **SMART** — Substitutable Medical Applications, Reusable Technologies
- **FHIR** — Fast Healthcare Interoperability Resources (a modern data format standard from HL7)

Think of it as "the app store model for healthcare software" — SMART-on-FHIR creates a standardized way for apps to read from and write to EHRs without requiring custom integration work for each system.

---

## Why It Matters for AI Medical Scribes

Before SMART-on-FHIR, integrating with an EHR required:
- A bespoke integration with each EHR vendor (Epic, Cerner, athenahealth, etc.)
- Hospital IT teams to build and maintain custom connections
- Significant cost and time (often 6–18 months of integration work)

SMART-on-FHIR changes this by providing a **standardized API layer** that works across EHR systems. Once an app is certified as SMART-on-FHIR compliant, any hospital running a compatible EHR can install it without custom integration work.

For AI medical scribes, SMART-on-FHIR enables:
- **Reading patient schedules** from the EHR (to know which patient is being seen)
- **Writing clinical notes** back into the EHR (to deliver the AI-drafted note)
- **Reading patient context** (relevant history, medications, problem list)

---

## SMART-on-FHIR in the Abridge Workflow

```
1. Clinician opens Abridge app
        ↓
2. Abridge reads patient schedule from Epic (via SMART-on-FHIR)
        ↓
3. Clinician records the patient encounter
        ↓
4. Abridge generates the clinical note
        ↓
5. Abridge writes the note back to Epic (via SMART-on-FHIR)
        ↓
6. Clinician uses dot-phrases (.hpisec, .meds, etc.) to pull
   sections into the Epic note template
```

This is the integration architecture behind Abridge's EHR write-back capability.

---

## FHIR Resources — What Gets Exchanged

FHIR organizes healthcare data into "resources" — standardized data structures for things like:
- `Patient` — demographics
- `Encounter` — a clinical visit
- `Observation` — a clinical finding or measurement
- `Condition` — a diagnosis or health concern
- `MedicationStatement` — a medication being taken
- `DiagnosticReport` — lab or imaging results
- `DocumentReference` — a clinical document (like an AI-drafted note)

A SMART-on-FHIR app can read and write any of these resources via a standard REST API.

---

## The Competitive Moat of Deep EHR Integration

The depth of SMART-on-FHIR integration varies significantly by vendor:

| Vendor | SMART-on-FHIR depth | Notes |
|---|---|---|
| **Abridge** | Deep — reads schedule, writes notes, supports dot-phrases | Considered deepest ambient AI integration |
| **Nuance DAX** | Deep within Epic (via Microsoft/Epic partnership) | Uses Dragon Medical One + GPT-4 |
| **DeepScribe** | Moderate | Focused on outpatient/ambulatory |
| **Suki** | Moderate | Lightweight, faster implementation |
| **Freed** | Light | Self-serve, minimal EHR integration |

The deeper the SMART-on-FHIR integration, the higher the **switching cost** for a health system — because the dot-phrase library, training, and clinical workflows are all built around that specific vendor's integration.

---

> [!info]- Related
> [[Concept - Epic]] · [[Concept - Cerner and athenahealth]] · [[Concept - Dot-Phrase]] · [[Abridge|Abridge Teardown]]
