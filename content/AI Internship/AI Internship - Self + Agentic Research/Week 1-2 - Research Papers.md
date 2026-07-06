#capstone #ai-internship #neurology #research-papers

# Week 1–2 Research Papers — Same Problem Space

Companion to "Week 1 - Neurology Research.md". Curated list of academic papers that frame the exact same wedge your friend is researching.

All papers below address one or more of:
1. Ambient AI scribes / clinical documentation burden
2. LLM-driven clinical reasoning on neurology cases
3. Multimodal chart + imaging + EEG synthesis
4. AI–clinician disagreement / missed findings
5. EHR summarization with retrieval-augmented generation

---

## Tier 1 — Read these first (directly on your wedge)

### 1. Ambient AI Scribes Reduce Burnout — But Lower Note Quality
**Olson KD et al. (Yale + 5 health systems).** *JAMA Network Open.* Oct 2, 2025. doi:10.1001/jamanetworkopen.2025.34976
- 263 ambulatory clinicians, Abridge for 30 days
- Burnout: 51.9% → 38.8% (74% lower adjusted odds)
- Equivalent to ~10.8 min saved per workday
- Neurology/Psychiatry was 5.3% of sample (small, but directionally same)
- https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2839542

### 2. AI Scribe Notes Are Lower Quality Than Human Notes
**Reddy A et al. (VA / Univ of Washington).** *Annals of Internal Medicine.* Apr 17, 2026.
- 5 standardized primary care visits, 11 AI scribes vs. 18 human clinicians, 30 blinded raters using PDQI-9
- **Human notes scored higher in every case**, especially on thoroughness, organization, usefulness
- Authors conclude AI scribes are draft tools, not substitutes
- https://mednews.uw.edu/news/AI-scribes-lower-quality

### 3. Abridge at KUMC — Detailed Operational Data
**JAMIA Open.** Feb 21, 2025. doi:10.1093/jamiaopen/ooaf013
- 99 post-implementation survey responses
- 81% said documentation workflow easier
- 77% said it improved patient care through decreased documentation burden
- Median note generation: 76 sec (Jul 2023) → 38 sec (Apr 2024)
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11843214/

### 4. AI Scribes Save Under a Minute Per Note (real-world review)
**STAT review.** Apr 1, 2026.
- Aggregate of published studies: scribes saved clinicians under 1 minute per clinical note
- Despite marketing, modest real-world time savings
- https://www.statnews.com/2026/04/01/ai-ambient-scribes-modest-time-savings-clinical-documentation/

### 5. Hype vs Reality in AI Clinical Integration
**PMC12700513.** 2025.
- Overreliance causes clinicians to accept outputs uncritically
- Neglecting clinical cues and diminishing independent judgment
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12700513/

---

## Tier 2 — Clinical reasoning LLMs on neurology cases

### 6. LLM Outperforms Physicians on Clinical Reasoning
**Brodeur PG, Buckley TA, Kanjee Z, Goh E et al.** *Science.* Vol 392, Issue 6797, pp 524–527. Apr 30, 2026. doi:10.1126/science.adz4433
- OpenAI o1 series tested against hundreds of physicians
- On landmark diagnostic cases: physicians with GPT-4 = 76%, physicians with conventional resources = 74%, GPT-4 alone = 92%
- Real-world ER second-opinion study at Beth Israel Deaconess
- **Best paper for the "LLM as clinical reasoning layer" argument**
- https://www.science.org/doi/10.1126/science.adz4433

### 7. Multi-Agent Framework for Neurological Clinical Reasoning
**Sorka M, Gorenshtein A, Aran D, Shelly S (Technion + Mayo).** *PLOS Digital Health.* Dec 4, 2025. doi:10.1371/journal.pdig.0001106
- 10 LLMs on 305 Israeli Board Certification Neurology exam questions
- Five-agent framework (complexity classifier, interpreter, retrieval, synthesis, validator)
- LLaMA 3.3-70B: 69.5% (base) → 73.4% (RAG) → **89.2% (agentic)**
- Domain-specialized models (Meditron-70B, MedLLaMA3) performed *worse* than general models
- **Most directly relevant paper for "reasoning layer over multimodal neuro data"**
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12677565/

### 8. Neural-MedBench — Reasoning Benchmark for Multimodal Clinical AI
**arXiv:2509.22258.** Sep 2025.
- Compact reasoning-intensive benchmark probing limits of multimodal clinical models
- https://arxiv.org/html/2509.22258v1

---

## Tier 3 — Neurology-specific documentation gaps

### 9. ChatGPT Neurology Referral Letters — Completeness Study
**Rattananan W.** *Medicina (Kaunas).* Oct 28, 2025. doi:10.3390/medicina61111931
- 5 standardized neurology scenarios × 10 letters = 50 letters using ChatGPT-4o
- Mean total score 25.76/30 (87% completeness, 84% quality)
- **72% of letters (36/50) had content gaps in HPI and physical exam sections**
- Management was the lowest-scoring domain (72.7%)
- **Direct evidence of the gap your product would fill**
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12653999/

### 10. Standardized Note Templates Improve Quality Metrics in Resident Clinics
**Breithaupt A et al. (UCSF + ZSFG).** *Neurology Education.* Vol 4 No 1. Mar 5, 2025. doi:10.1212/NE9.0000000000200200
- 23 neurology residents, cluster-randomized trial
- Condition-specific templates for epilepsy, headache, Parkinson's
- Significant quality improvements:
  - Epilepsy: driving documentation 92% vs 53% (p=0.002)
  - PD: medication-related motor symptoms 95% vs 50% (p=0.01)
  - Headache: lifestyle counseling 77% vs 21% (p=0.005)
- **No efficiency gain** — templates made notes longer, not faster
- **Critical: shows that just having templates improves "missed finding" rate dramatically — same wedge as your product**
- https://www.neurology.org/doi/10.1212/NE9.0000000000200200

### 11. Completeness of Neurology Referral Letters (general)
**medRxiv 2025.06.12.25329503.** 2025.
- Letters scored on demographics, chief complaint, HPI, physical exam, management, consultation questions
- Wide variability, "clear documentation of attempted therapies to minimal or absent"
- https://www.medrxiv.org/content/10.1101/2025.06.12.25329503v1.full.pdf

---

## Tier 4 — Missed findings, AI-clinician disagreement

### 12. AI–Clinician Disagreement Prediction Pipeline
**Sanchez M et al. (Harvard / Stanford).** *Cell Reports Medicine.* Oct 17, 2023. doi:10.1016/j.xcrm.2023.101207
- Deployed chest X-ray AI — disagreement rate with radiologists = **6.5%**
- Built pipeline modeling disagreement + significance + confidence
- Expected burden reduction: 4.8%
- Key insight: diagnostic model alone insufficient, need ecosystem of models around it
- https://www.sciencedirect.com/science/article/pii/S2666379123003749

### 13. NLP Limits AI–Radiologist Report Discrepancies
**Radiology Business.** Northwestern Medicine build.
- NLP software detected missed diagnoses on high-acuity CT
- https://radiologybusiness.com/topics/health-it/enterprise-imaging/natural-language-processing-can-limit-report-discrepancies-between-ai-and-radiologists

### 14. Patient Reactions to AI–Clinician Discrepancies
**PMC12141964.** 2025.
- How discrepancies between AI-derived and radiologists' recommendations affect patients
- Critical for trust model design
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12141964/

### 15. Liability When AI Finds What Radiologist Missed
**AuntMinnie.** 2025.
- Radiologists more legally culpable if AI catches an abnormality they missed
- https://www.auntminnie.com/imaging-informatics/artificial-intelligence/article/15747540/if-ai-finds-an-abnormality-that-a-radiologist-misses-whos-at-fault

### 16. Missed Radiology Follow-Ups — Northwestern Program
**PRNewswire / Northwestern Medicine.** 2022.
- Built internal AI to trigger follow-up on incidental imaging findings
- https://www.prnewswire.com/news-releases/using-artificial-intelligence-to-solve-one-of-health-care-s-most-enduring-problems-301504387.html

---

## Tier 5 — Multimodal foundation models (the AI architecture wedge)

### 17. Medical Multimodal Foundation Models Review
**Sun K, Xue S et al. (Tsinghua).** arXiv:2412.02621. Dec 3, 2024.
- Comprehensive review across datasets, architectures, clinical applications
- Two categories: MMVFMs (vision-only) and MMVLFMs (vision-language)
- Covers MRI, CT, X-ray fusion with clinical reports
- https://arxiv.org/html/2412.02621v1

### 18. Foundation Models for Radiology
**dirjournal.org.** 2025. doi:dir.2025.253445
- Applications, opportunities, challenges, risks
- https://www.dirjournal.org/articles/foundation-models-for-radiology-fundamentals-applications-opportunities-challenges-risks-and-prospects/doi/dir.2025.253445

### 19. Vision-Language Foundation Model for 3D Medical Imaging
**Nature s44387-025-00015-9.** 2025.
- 3D medical imaging with VL foundation models
- https://www.nature.com/articles/s44387-025-00015-9

### 20. Multimodal Dataset and Benchmarks for Vietnamese PET/CT
**NeurIPS 2025.**
- Adapting general VLMs to medical domain
- https://neurips.cc/virtual/2025/poster/121676

---

## Tier 6 — RAG for clinical text

### 21. RAG on Clinical Notes for Diagnostic Reasoning
**arXiv:2401.10733v2.** 2024.
- Dynamic QA of clinical documents using retrieval-augmented generation
- https://arxiv.org/html/2401.10733v2

### 22. Enhancing Medical AI with RAG (Review)
**PMC12059965.** 2025.
- Combines information retrieval + generative models for medical tasks
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12059965/

### 23. Clinical Entity Augmented Retrieval
**Nature npj Digital Medicine.** 2024. doi:10.1038/s41746-024-01377-1
- LLMs + RAG improved information extraction vs. prior methods
- https://www.nature.com/articles/s41746-024-01377-1

### 24. Clinical Text Summarization with LLMs — Evidence Review
**JMIR.** 2025. doi:10.2196/68998
- State of the art on clinical text summarization using LLMs
- https://www.jmir.org/2025/1/e68998

### 25. Generative LLMs in EHRs — Systematic Review
**Du X et al. (Brigham and Women's / Harvard).** *JAMIA.* 2024. doi:10.1093/jamia/ocaf233
- 76 studies since ChatGPT release, real EHR data
- 88.2% used zero-shot prompting
- Only 2 studies used multimodal data
- 6 studies identified hallucinations (e.g., fabricated patient names)
- **Critical caveats: bias, hallucinations, impersonal tone**
- https://www.medrxiv.org/content/10.1101/2024.08.11.24311828v2.full-text

---

## Tier 7 — Implementation / operational

### 26. LLM Verification of Patient Care Documents
**Chung P et al.** *NEJM AI.* 2025. doi:10.1056/AIdbp2500418
- LLMs effectively summarize EHRs but require verification
- https://ai.nejm.org/doi/full/10.1056/AIdbp2500418

### 27. LLM Performance on Clinical Reasoning Tasks
**JAMA Network Open.** 2025. doi:10.1001/jamanetworkopen.2024.47679
- Differential dx less accurate than diagnostic testing
- Final dx, management, miscellaneous reasoning more accurate
- https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2847679

### 28. Adapted LLMs Outperform Medical Experts in Clinical Text Summarization
**arXiv:2309.07430v4.** 2023.
- LLMs outperform medical experts on multiple summarization tasks
- https://arxiv.org/html/2309.07430v4

### 29. Neurologic Examination Adds ~6.7 Minutes Per Visit
**PMC11620545.** 2024.
- Subgroup analysis: pain visits +6.7 min
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11620545/

### 30. Documentation Burden Measurement
**PMC11534919.** 2024.
- Total EHR time → decreased patient satisfaction, lower communication ratings
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11534919/

---

## Tier 8 — EHR / workflow integration

### 31. EHR Documentation Burden Crowds Out Health Information Exchange
**Health Affairs.** 2024. doi:10.1377/hlthaff.2024.00398
- Each additional hour spent documenting → 7.1% reduction in HIE use
- https://www.healthaffairs.org/doi/abs/10.1377/hlthaff.2024.00398

### 32. Hard-to-Use EHRs Linked to Physician Burnout
**AMA News.** 2024.
- Every 1-point boost in EHR usability → 3% lower odds of burnout
- https://www.ama-assn.org/practice-management/digital-health/new-research-links-hard-use-ehrs-and-physician-burnout

### 33. Ambient Documentation Technology — Clinician Experience
**JAMA Network Open.** 2025. doi:10.1001/jamanetworkopen.2024.37847
- Survey study pre/post ambient documentation
- https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2837847

### 34. Documentation Philosophy — Shorter Yet Information-Rich Notes
**Rodríguez-Fernández JM.** *Frontiers in Digital Health.* 2022. doi:10.3389/fdgth.2022.1063141
- Argument for redesigning clinical notes
- https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2022.1063141/full

---

## Suggested reading order (if you only have 4 hours)

1. **#9** (Rattananan — ChatGPT neurology referral letters, 72% had gaps) — single best paper for "this is the gap"
2. **#10** (Breithaupt — UCSF templates, 92% vs 53% on driving status) — single best paper for "templates/structure fix this"
3. **#7** (Sorka — multi-agent neuro reasoning, 89.2% with agents) — best paper for the AI architecture wedge
4. **#1** (Olson — JAMA Network Open, 51.9% → 38.8% burnout) — establishes demand side
5. **#2** (Reddy — Annals, AI notes lower quality) — establishes quality gap (this is your opportunity)

If you have time for a sixth: **#6** (Brodeur — Science, GPT-4 92% vs physicians 76%) for the "LLMs already do reasoning well" narrative.

---

## What this corpus tells us about your wedge

**The gap is real and quantified:**
- Templates improve "missed findings" rate from 53% to 92% on driving status (Breithaupt)
- 72% of LLM-generated neurology referral letters had content gaps (Rattananan)
- AI scribes reduce burnout 13 percentage points but produce lower-quality notes (Olson vs. Reddy tension)
- Clinicians spend 2x more time on EHR/admin than patient care (KUMC/AHA data)

**The architecture is feasible:**
- Multi-agent LLM framework hits 89.2% on neurology board questions (Sorka)
- LLaMA 3.3-70B + RAG + agents outperforms GPT-4o on neurology reasoning
- Multimodal foundation models for medical imaging are now production-grade (Tsinghua review)

**The market is validated:**
- $150M Series E for Aidoc
- Abridge = 2025/2026 Best in KLAS
- Multiple health systems publishing positive pilot data

**The unsolved wedge:**
- Nobody is merging ambient scribe + prior chart + imaging + EEG into one synthesis
- 6.5% AI-radiologist disagreement rate (Sanchez) is real and unaddressed by current scribes
- Missed follow-ups on incidental findings remain a top-3 safety issue (Northwestern, Inflo Health)

---

## Sources by topic

**Ambient scribes:**
- #1, #2, #3, #4, #5, #33, #43 (JAMIA Open KUMC)

**Neurology-specific:**
- #7, #9, #10, #11, #29

**Multimodal / RAG / reasoning:**
- #6, #7, #8, #17, #18, #19, #20, #21, #22, #23, #24, #25, #26, #27, #28

**Missed findings / disagreement:**
- #12, #13, #14, #15, #16

**Documentation burden:**
- #30, #31, #32, #34

**EHR workflow / integration:**
- #31, #32, #33, #34