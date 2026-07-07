---
title: Concept - Cerner and athenahealth
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #concept #EHR

---

# Cerner and athenahealth — Electronic Health Record Systems

---

## Cerner (now Oracle Health)

**Cerner** was the second-largest US hospital EHR system before its acquisition by Oracle in 2022. It is now officially branded **Oracle Health**. Cerner holds approximately 20–25% of the US hospital EHR market, primarily in community hospitals and mid-sized health systems.

**Cerner's AI strategy:** Cerner/Oracle has been slower to embed generative AI than Epic. Historically, Cerner was known for its HealtheDataLab (machine learning) and has more recently begun integrating LLM-based clinical documentation tools.

**Abridge's Cerner integration** is described as lighter than Epic — Abrige writes notes back via SMART-on-FHIR, but the depth of workflow automation is not as deep. Cerner's legacy architecture (Millennium platform) has made deep integration harder for third-party vendors.

---

## athenahealth

**athenahealth** (often stylized as athenahealth or just athena) is a cloud-based EHR platform for outpatient/ambulatory practices, used primarily by physician groups, independent practices, and mid-sized medical groups. It holds approximately 8–10% of the US outpatient EHR market.

**athenahealth's strengths:**
- Cloud-first architecture (unlike Cerner's legacy on-prem systems)
- Strong in ambulatory and specialty care
- Built-in revenue cycle management (RCM)

**Abridge's athenahealth integration** uses SMART-on-FHIR for note write-back, similar to Cerner. Ambulatory practices using athenahealth can deploy Abrige without switching EHRs.

---

## Why Both Matter for the AI Scribe Landscape

Together, Epic, Cerner/Oracle Health, and athenahealth cover approximately **60–70% of the US hospital and outpatient EHR market**. Any serious AI medical scribe must integrate with all three.

| EHR | Market segment | Abrige integration depth | Abrige write-back |
|---|---|---|---|
| **Epic** | Large hospital systems, academic medical centers | Deepest | Dot-phrase + SMART-on-FHIR |
| **Cerner / Oracle Health** | Mid-sized hospitals, community systems | Lighter | SMART-on-FHIR |
| **athenahealth** | Ambulatory / outpatient practices | Moderate | SMART-on-FHIR |

**Nuance DAX (Microsoft)** has a different competitive position — it is natively embedded within the Epic workflow via a Microsoft/Epic partnership, giving it a structural advantage within Epic accounts where that partnership is active.

---

## Related

- [[Concept - Epic]]
- [[Concept - SMART-on-FHIR]]
- [[Concept - Dot-Phrase]]
- [[Competitor Teardown - Abrige]]
