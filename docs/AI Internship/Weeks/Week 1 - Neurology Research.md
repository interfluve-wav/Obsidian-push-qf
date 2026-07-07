---
title: Week 1 - Neurology Research
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology

# Week 1 — Neurology Track Research

Companion to "Planning & Questions.md". Same Week 1/2 framing, neurology lens.

---

## What problem are we solving here?

We're building an AI that prepares a neurologist for a patient visit — pulling together the prior chart, prior imaging, prior signals, and any longitudinal data into a single pre-visit briefing. The ambient AI scribe market (Abridge, DeepScribe, Nuance DAX) has shown that ambient AI works for note-taking. Our wedge is *upstream* of the scribe: the briefing the doctor sees before walking into the room.

The neurology version of this is harder than the general medical version because:

1. The neuro exam is the longest structured exam in medicine (12 cranial nerves, 5 motor, 4 sensory, reflexes, coordination, gait). General scribes collapse it to "neuro exam: grossly intact."
2. Localization (symptoms → lesion → differential → workup) is the intellectual core. A normal scribe doesn't capture it.
3. Patients have longitudinal signal — MS relapses, Parkinson's UPDRS drift, seizure frequency, migraine MIDAS — that needs to be trended, not re-typed each visit.
4. Imaging, EEG, EMG, and labs arrive separately and need to be merged with the note. Scribes only see the transcript; they ignore the rest of the chart.

So the "pre-visit synthesis-for-neuro" wedge has to do three things general scribes don't:
- Capture the neuro exam as discrete data, not a paragraph.
- Combine transcript + prior chart + imaging + EEG reports into one synthesis.
- Track chronic disease trajectory (EDSS, UPDRS, seizure frequency, MIDAS) over time.

---

## Competitors — AI scribes (overlap (general ambient AI market), but with neuro gaps)

Tier 1 — General scribes used by neurologists today, none of them neuro-specific:

- **DeepScribe** — has a specialty module for neurology. Ambient, writes the note into the EHR. Around $400/provider/mo non-EHR, ~$500/provider/mo with EHR write-back. Strongest where it's deployed at health-system scale. Gap: it doesn't synthesize prior MRI/EEG, doesn't track EDSS/UPDRS/MIDAS longitudinally.
- **Abridge** — Epic-integrated, the de facto scribe at large academic systems. Pricing is contract-only, generally $200–$300+/provider/mo. Gap: same — no imaging/EEG merge, no chronic-disease scoring.
- **Nuance DAX Copilot (Microsoft)** — works natively inside Epic/Cerner/athena. ~$369–$600+/provider/mo by tier. Gap: even with full EHR access it does not produce a localization narrative; it's a transcript-to-note engine.
- **Suki** — voice-first, $299–$399/provider/mo. Adds voice commands ("order MRI brain," "schedule EEG") but still doesn't surface imaging findings inside the note.
- **Freed** — $39/$79/$119 per provider/mo (the lowest-friction general scribe). Self-serve, no hospital approval needed. Gap: no neuro templates at all — neuro exam collapses to a single sentence.
- **Nabla** — free up to 30 encounters/mo, then Pro at $119/mo. Used by small/solo practices. Gap: not specialty-tuned.
- **Heidi Health** — Free–$99/mo, multilingual, light templates. No neuro-specific support.
- **DeepCura** — newest entrant, claims full neurology templates and model flexibility (lets you switch the underlying LLM per case). $129/mo. Closest direct competitor to a "neuro-specific" scribe — but it still only sees the transcript.

Tier 2 — Neuro-specific or procedure-specific scribes worth knowing about:
- **ScribePT / ScribeLink** — niche PT/rehab, not relevant.
- **Medwriter** — markets itself to neurologists specifically but is mostly a generic scribe with neuro marketing copy.

What they all share (the gap = our opportunity):
- Transcript in → note out. They do not ingest the prior chart, prior imaging, prior EEG.
- No localization reasoning document.
- No chronic-disease scoring trend.
- No procedure templates for EMG/NCS, EEG interpretation, lumbar puncture, botulinum toxin.

---

## Competitors — Imaging AI for neuro (heavily more crowded than GI)

This is where neuro diverges from the general scribe market — there are deep, well-funded imaging AI companies already.

- **Viz.ai** — LVO (large vessel occlusion) detection on CT/CTA, plus care coordination (notifies the neurointerventionalist on call). Used in 1,700+ hospitals. Recent ESOC data: RapidAI detected 33% more medium-vessel occlusions than Viz.ai — so accuracy gap exists, not just a marketing gap. Door-to-puncture reductions of 11–25 min reported. Pricing: enterprise/contract, no public per-provider number.
- 
- **RapidAI** — perfusion (CTP) + LVO detection. Stronger on MeVO and perfusion volumetrics than Viz.ai in head-to-head studies. Enterprise pricing.
- 
- **Brainomix e-Stroke** — best-in-class on automated ASPECTS scoring on non-contrast CT. Used in nationwide tenders (Hungary just deployed it across every stroke center). Enterprise pricing.
- 
- **[Aidoc]()** — worklist triage + neurovascular algorithms (stroke, hemorrhage, c-spine fracture, aneurysm). Pricing is per-scan via AWS Marketplace: $6/scan for the Starter tier, with enterprise tiers on top. The only public pricing in this space.
- 
- **RapidAI vs. Viz.ai vs. Aidoc vs. Brainomix** — scoping review (Medicina, Mar 2026, 29 studies): all four show high LVO sensitivity (78–97%), but performance on distal/posterior circulation varies, and outputs are not interchangeable. 4 of 29 studies were industry-sponsored — bias risk flagged.

Tumor / volumetric AI:
- **Cortechs NeuroQuant + NeuroQuant MS + NeuroQuant Brain Tumor** — FDA-cleared volumetric brain MRI. Industry standard for MS lesion/brain atrophy tracking and tumor volumetric reporting. Used in research and increasingly clinical.
- **Cercare Medical "Oncology Virtual Expert"** — AI tumor segmentation, 510(k) cleared in 2025.

EEG AI:
- **Ceribell** — point-of-care EEG headband + AI seizure detection in the ICU. Fast FDA-cleared deployment, used at Cleveland Clinic and others.
- **Natus autoSCORE AI** — AI EEG review as an adjunct to human expert reading.
- **encevis (AIT)** — automated EEG analysis (spike/seizure detection), used in European epilepsy centers.
- **Piramidal** — newer, scanning a full 24-hour EEG in seconds; Cleveland Clinic collaboration announced 2025.
- **Neuro Event Labs Nelli** — long-term ambulatory EEG with AI-assisted seizure detection.

Digital biomarkers / wearables (chronic disease):
- **Empatica EpiMonitor** — FDA-cleared wrist-worn seizure detector (generalized tonic-clonic). $399 device + $15.90–$17.40/mo subscription.
- **Rune Labs StrivePD** — Apple Watch-based passive tremor/dyskinesia tracking for Parkinson's, FDA 510(k) cleared (2023). Free for patients.
- **Multiple companies in MS** — using smartphone-based passive tests (Floodlight, MS Performance Test, BeCare MS Link).

What they all share (the gap = our opportunity):
- Imaging AI ends at the radiology report. It does not write the neuro visit note, does not know what the patient said today, does not surface findings in the encounter.
- EEG AI is a separate workflow with its own UI. The neurologist still has to read the impression and merge it into the chart manually.
- Wearables generate streams of biomarker data that nobody puts into the clinic note.

---

## Competitors — Clinical documentation AI (reasoning layer)

- **OpenEvidence** — physicians' #1 most-used clinical AI. Literature-grounded Q&A. Used heavily by neuro for "what's the latest on X?" but it does not write notes or merge with the chart.
- **UpToDate AI / Wolters Kluwer** — guideline lookup, similar pattern.
- **AMBOSS LiSA** — clinical reasoning, more accurate than general LLMs on clinical vignettes.
- **Glass Health** — generates differential + workup plans from a clinical scenario, used by hospitalists.
- **ChatGPT, Claude, Grok, Perplexity** — used informally for drafting patient comms, summarizing guidelines, brainstorming differentials. Physicians report using them weekly but they are not chart-integrated, not HIPAA, not audit-logged.

---

## Pain points — neurologist-specific (from physician surveys and the literature)

The 2025 Physician Sentiment Survey (athenahealth) and the JAMA Network Open AI-summarization study both point the same direction:
- 65% want documentation/scribing support (highest).
- 48% want admin burden relief.
- 43% want clinical decision support.

Neurology-specific amplifications:
- Neurologic exam adds ~6.7 minutes per visit (study subgroup: pain visits) and is the most failure-prone part of general scribe output (it collapses).
- MRI results take 1–2 weeks to return in non-academic settings — patients return to clinic with results no one has reviewed with them.
- EEG impressions are dense, use epilepsy-specific vocab (FREQ, POLY, GTC, interictal discharges, HFO), and take neurologist time to read carefully.
- Chronic disease scoring is repetitive: EDSS at every MS visit, UPDRS at every PD visit, seizure calendar at every epilepsy visit, MIDAS at every migraine visit — currently re-asked every visit.
- Documentation is so heavy that neurologists report burnout above the physician-average baseline.

---

## Possible product pathways (parallel to the general scribe product line)

1. **Transcript + scribe specialist** — neuro-tuned ambient scribe. (This is what DeepCura and Medwriter are trying to do. Lowest barrier to entry, lowest defensibility.)
2. **Imaging + transcript synthesis** — Viz/Aidoc/RapidAI detect the finding, our model writes the clinical correlation and the patient-facing explanation. **High defensibility because the radiologist note and the clinic note are separate today.**
3. **EEG + transcript synthesis** — Ceribell/encevis give the impression, our model merges it with the encounter and proposes med changes. Newer wedge.
4. **Chronic-disease trajectory** — ingest prior visits + wearable stream + structured scores, surface "EDSS has drifted +0.5 over 18 months" or "seizure frequency doubled since last visit" before the doctor even opens the chart. (StrivePD / Empatica own the device, but nobody owns the in-clinic surfacing.)
5. **Multimodal model: MRI + EEG + EHR + transcript → differential + workup** — biggest defensibility, hardest to ship. This is the "pre-visit synthesis-for-neuro" big vision.

The most realistic Week 1 framing: pick pathway 2 (imaging merge) or pathway 5 (multimodal) as the Big Vision, and use pathway 1 (neuro scribe) as the Week 3 Label Studio demonstrator (it's the easiest to label and the easiest to evaluate).

---

## Imaging and signal analysis (the AI building blocks, in plain language)

For pictures (MRI, CT, PET):
- **CNNs** are the default backbone. ResNets and U-Nets are the workhorses.
- **3D CNNs and transformer-based U-Nets** are the current state-of-the-art for brain tumor and stroke-lesion segmentation (handles volumetric MRI natively).
- **Grad-CAM** is the cheapest explainability layer — overlays a heatmap on the MRI showing what the model looked at. Critical for radiologist trust.

For signals (EEG, EMG):
- **1D CNNs + BiLSTM** hybrid is the standard architecture (Frontiers in Neurology 2025 review).
- **CNN-RF hybrid** and **FCNLSTM** show 95–99% accuracy on Bonn/CHB-MIT benchmarks but most haven't been validated in clinical EEG (different preprocessing, different artifact profile).
- **Dynamic Graph Neural Networks** are newer; 99.83% on Bonn single-channel.

For multimodal:
- **EEG + sMRI/fMRI fusion** with attention mechanisms has reported up to ~99% diagnostic accuracy on Parkinson's in some studies (MDPI 2024). Caution: most published numbers are on small datasets; generalization is the open question.
- **Visual Question Answering (VQA)-style multimodal networks** are the closest published architecture to "ask the MRI a question and get an answer in natural language." Worth tracking for the prototype.

For structured EHR data:
- **XGBoost / Random Forests** on longitudinal EHR features for disease-conversion prediction (e.g., mild cognitive impairment → Alzheimer's). Used in pharma-trial enrichment.

For wearables:
- Apple Watch Movement Disorders API (tremor, dyskinesia) → StrivePD pipeline.
- Empatica EDA + accelerometer → generalized tonic-clonic seizure classifier.

---

## Datasets — neurology (parallel to general ambient AI dataset list)

EEG datasets:
- **CHB-MIT** (Children's Hospital Boston MIT scalp EEG) — the most-cited public EEG seizure dataset. 23 subjects, ~844 hours.
- **Freiburg iEEG** (intracranial EEG) — 21 patients, used for seizure detection benchmarking.
- **Bonn University EEG** — single-channel scalp, 5 sets, often the first benchmark for any new EEG model.
- **TUH EEG Corpus** (Temple University Hospital) — large-scale clinical EEG archive, 25,000+ recordings.
- **SCORE-AI dataset** (Nordic multicenter, 30,493 records) — recent, used for the autoSCORE AI product.

MRI / fMRI datasets:
- **OpenNeuro** (Stanford-hosted, BIDS-compliant) — 1,793 public datasets, MRI/PET/MEG/EEG/iEEG. Includes Alzheimer's (ds004504), Parkinson's resting-state EEG (ds002778), motor imagery fMRI+EEG (ds002336), multimodal iEEG-fMRI (PMC8938409).
- **ADNI (Alzheimer's Disease Neuroimaging Initiative)** — gold standard for Alzheimer's MRI/PET/DTI progression.
- **PPMI (Parkinson's Progression Markers Initiative)** — analogous for Parkinson's.
- **MS PATHS / MSBase** — clinical + MRI for MS.
- **Human Connectome Project (HCP)** — high-resolution multimodal brain imaging.
- **UK Biobank** — 500,000+ participants with brain MRI subset, population-scale.

Multimodal:
- **Open multimodal iEEG-fMRI** (PMC8938409, 51 participants) — naturalistic stimulation during intracranial EEG.
- **EEG+fMRI motor imagery** (OpenNeuro ds002336) — canonical multimodal fusion benchmark.

PET:
- **ADNI PET subset** (florbetapir, FDG) — amyloid/tau/metabolic imaging.
- **OpenNeuro PET** (e.g., ds007907 skull bone marrow translocator, chronic pain) — newer, smaller.

Wearable / digital biomarker:
- **Apple Movement Disorders API raw data** — not directly downloadable, but Rune Labs/Apple have published benchmarks.
- **Empatica research datasets** — gated, requires partnership.
- **Multiple sclerosis digital biomarker dataset** (PMC8615428) — review of available sources.

Genomic + behavioral:
- **NIH dbGaP** — for genomics tied to neurological phenotypes.
- **All of Us** (NIH) — includes neurological phenotypes + EHR + wearables for ~1M participants.

---

## Strategy — where this puts us in the broader AI strategy landscape

**The ambient AI scribe market's Week 1 gaps** (the parallel track the team is using for reference): competitor pricing is spread across $39–$600, and no single vendor combines transcript + chart + imaging + signals into a pre-visit synthesis.

Neurology's Week 1 gaps are sharper but the playbook is the same:
- Scribe market is more crowded on price (down to $39/mo with Freed).
- Imaging AI is more crowded and deeper (Viz/RapidAI/Brainomix/Aidoc all clinically deployed).
- EEG AI is fragmented (Ceribell, Natus, encevis, Piramidal — none dominant).
- Wearables are device-side only (StrivePD, EpiMonitor) — no one owns the in-clinic surfacing.

Our wedge = the missing layer between "transcript," "prior chart," "MRI/CT," "EEG/EMG," and "the actual visit note." For neurology the modality surface is wider (imaging + signals + EHR + transcript), and the longitudinal chronic-disease trajectory is a unique layer that no scribe owns.

---

## Open questions for week 2 (your three questions, neurology angle)

1. **Do we go after the neuro-scribe wedge (low risk, low defensibility) or the imaging-merge wedge (higher risk, much higher defensibility)?** This determines which datasets we prioritize in Week 3.
2. **Is the deliverable a working prototype or a blueprint?** For neuro, a blueprint is more realistic given the imaging/signal complexity.
3. **What "big vision" framing matches pre-visit synthesis's?** Candidates:
   - "The neuro consult, fully reconstructed from chart + imaging + EEG + transcript."
   - "Localization, automated: symptoms → lesion → workup, drafted before the neurologist enters the room."
   - "The chronic-neurology dashboard: MS, Parkinson's, epilepsy, migraine — trended across every visit, surfaced in the note."

---

## Sources

Scribes:
- https://www.deepcura.com/resources/best-ai-scribe-for-neurology
- https://www.deepscribe.ai/resources/best-ai-medical-scribes
- https://www.deepscribe.ai/specialties/neurology
- https://glass.health/resources/best-ai-medical-scribe
- https://omnimd.com/blog/best-medical-ai-scribes/
- https://www.marvix.ai/blog/best-ai-scribe-for-neurology

Imaging AI:
- https://pmc.ncbi.nlm.nih.gov/articles/PMC13027882/ (Brainomix/Aidoc/RapidAI/Viz.ai scoping review)
- https://www.viz.ai/
- https://www.rapidai.com/
- https://www.aidoc.com/
- https://www.brainomix.com/stroke/
- https://aws.amazon.com/marketplace/pp/prodview-hmy5pemibugck (Aidoc $6/scan)
- https://radiologybusiness.com/topics/healthcare-management/healthcare-policy/ai-powered-brain-tumor-segmentation-tool-earns-clearance-us
- https://www.cortechs.ai/nq-bt-revolutionizing-neuro-oncology-with-ai-driven-precision/
- https://www.appliedradiology.com/articles/neuroquant-ms-advancing-precision-in-multiple-sclerosis

EEG AI:
- https://www.frontiersin.org/journals/neurology/articles/10.3389/fneur.2025.1615120/full
- https://consultqd.clevelandclinic.org/harnessing-ai-to-bring-real-time-eeg-interpretation-to-the-icu
- https://www.aha.org/aha-center-health-innovation-market-scan/2025-08-26-4-takeaways-cleveland-clinics-new-ai-co-pilot-brain-icu-care
- https://ceribell.com/
- https://natus.com/neuro/autoscore-ai/
- https://encevis.com/research/

Wearables / digital biomarkers:
- https://www.empatica.com/store/epimonitor
- https://www.empatica.com/blog/empatica-epimonitor-epilepsy-monitoring/
- https://www.prnewswire.com/news-releases/rune-labs-secures-fda-clearance-for-parkinsons-disease-monitoring-through-strivepd-ecosystem-on-apple-watch-301566472.html
- https://www.strive.group/

Pain points:
- https://www.athenahealth.com/resources/blog/insights-from-2025-pss
- https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2848785
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11620545/ (neuro exam adds ~6.7 min)
- https://pmc.ncbi.nlm.nih.gov/articles/PMC12372577/

Datasets / multimodal:
- https://openneuro.org/
- https://openneuro.org/datasets/ds002336/versions/2.0.2
- https://openneuro.org/datasets/ds004504/versions/1.0.9
- https://pmc.ncbi.nlm.nih.gov/articles/PMC8938409/
- https://www.mdpi.com/2076-3417/14/9/3883 (PD EEG+MRI)
- https://www.sciencedirect.com/science/article/abs/pii/S1746809425019433 (MRI-EEG CNN attention)
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11968424/