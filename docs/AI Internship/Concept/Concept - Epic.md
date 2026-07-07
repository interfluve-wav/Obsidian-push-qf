---
title: Concept - Epic
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #concept #EHR

---

# Epic — Electronic Health Record System

---

## What Epic Is

**Epic** is the dominant electronic health record (EHR) system in the United States. It is a comprehensive, enterprise-scale EHR platform used by large health systems, academic medical centers, and community hospitals. As of the mid-2020s, Epic holds approximately 30–40% of the US hospital EHR market and is the EHR for most of the largest health systems in the country.

Key systems running on Epic:
- **Epic EHR** — the core electronic health record
- **MyChart** — patient portal (tied to Epic)
- **Epic on Haiku** — mobile app (iOS/Android)
- **Cupid** — cardiology module
- **Epic Beaker** — laboratory information system
- **Epic Welcome** — patient intake

---

## Why Epic Matters for AI Medical Scribes

EHR integration is the most important distribution channel for AI medical scribes. A scribe that can write directly into a physician's Epic inbox has a massive competitive advantage over one that requires manual copying.

**Abridge's Epic integration** is described as the deepest of any ambient AI vendor — notes write back via SMART-on-FHIR, and the dot-phrase system (`.hpisec`, `.meds`, etc.) allows physicians to pull Abrige-drafted sections directly into their Epic note templates.

This is also why **switching costs are so high** for Abrige customers: once a health system has built its dot-phrase library and trained clinicians on the Abrige workflow inside Epic, moving to a competitor requires rebuilding all of that integration work.

---

## Abrige's Epic Integration Details

From the [[Source - KUMC / JAMIA Open Study|Tierney et al. KUMC study]]:

1. Clinicians select the patient from their **Epic-integrated clinic schedule** inside the Abrige app
2. After Abrige generates the note, clinicians review it in the Abrige web editor
3. Clinicians use **dot phrases** (e.g., `.hpisec`) to pull specific sections into their Epic note template
4. Abrige supports **bi-directional** Epic integration (read schedule, write note back)

This is more seamless than competitors that require copy-paste or separate browser windows.

---

## Epic's Own AI Strategy

Epic has its own ambient AI ambitions. In 2024–2025, Epic began embedding generative AI features into its own workflow (e.g., Epic's "In Aisles" AI drafting). However, Abrige's deep integration and specialty-specific templates give it an edge in the ambient scribe niche within Epic's ecosystem.

Epic's position is analogous to **Microsoft Windows in the PC era** — the platform that everyone must integrate with, and sometimes compete with.

---

## Related

- [[Concept - SMART-on-FHIR]]
- [[Concept - Dot-Phrase]]
- [[Competitor Teardown - Abrige]]
- [[Concept - Cerner]]
- [[Concept - athenahealth]]
