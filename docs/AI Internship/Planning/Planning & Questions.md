---
title: Planning & Questions
updated: 2026-07-07 11:46 EDT
---

**

Planning:

- Week 1 - Research, learn more about GastroNote, capstone, and clinical domain. 
    
- Week 2 - Deeper research, talk with doctors, understand the data, learn about competitor weaknesses/strengths & how that can help with our product, competitive landscape mappingWeek 3 - Use Label Studio, run first training experiment 
    
- Week 4 - Look through market data, Doctor pain point surveys, Imaging AI landscape.
    
- Week 5+6 - Focus on the 3 tracks individually. Analyze findings. Business: market opportunity report & revenue model analysis. Neuro: clinical workflow map. AI: prototype architecture.
    
- Week 7 - Ensure we have checked expected deliverables
    
- Week 8 - Focus on presentation
    

  

Questions We Have:

- What exactly is [Gastro.ai](http://gastro.ai/)? Can we see the product if available? We want context and possibly a demo.
    
- Regarding the three aspects (3 different paths), how do we want to work (more divided or more collaborative)?
    
- For technical feasibility (may connect to other tracks), what should the end product look like? Is it research with a blueprint of technical details or simply research of what should be used?
    
- For weeks 3-5, the roadmap mentions Friday Demos. What are Friday Demos?
    
- In weeks 1-2, it mentions using GPT4. What should we use GPT4 for in those weeks?
    
- How should we focus on the “Big Vision” throughout the weeks?
    
- Are we making a working product by the end or are we developing a blueprint of a possible product?
    

  

1. Market & Strategy
    
2. Clinical Domain Expert
    
3. Technical Feasibility
    

  

Points Mentioned

- How will research be done with all three tracks
    
- Prioritize some tracks over others in some weeks/days (esp in research)
    

  
  

Week 1 Notes: 

- What is [gastro.ai](http://gastro.ai/)? Demo? 
    

- Ai specifically for gastroenterology that can read everyone's previous record for a patient and create a patient context, merges this with a transcript of the conversation and flags info that the doctor missed, and helps with overlooked care and billing. 
    

- Find competitors (10-15): features/pricing/strengths/gaps
    

- Current ai scribes: Abridge, DeepScribe, Suki, Microsoft Copilot/Nuance, Freed, Nabla, Heidi Health, Nuance DAX, DeepCura
    

- Links: [https://glass.health/resources/best-ai-medical-scribe](https://glass.health/resources/best-ai-medical-scribe), [https://engage.klasresearch.com/blog/the-rise-of-ambient-speech-technology-in-healthcare/6427/?utm_source=chatgpt.com](https://engage.klasresearch.com/blog/the-rise-of-ambient-speech-technology-in-healthcare/6427/?utm_source=chatgpt.com), [https://www.deepcura.com/resources/compare/best-ai-medical-scribes?utm_source=chatgpt.com](https://www.deepcura.com/resources/compare/best-ai-medical-scribes?utm_source=chatgpt.com), look through company sites
    
- Abridge/DeepScribe/Nabla: good at automatically generating notes from hearing patient/doctor convos & are used by large hospitals, but mostly focused on note taking and doesn’t combine this with previous patient charts or imaging results, Nabla is used more for smaller practices
    

- Abridge: no official public pricing but around $200/300+/provider/month
    
- DeepScribe: around $400/provider/month (non EHR integrated) or $500/provider/month (EHR integrated)
    
- Nabla: free for up to 30 consultations/month, $119/month (pro), custom pricing based on tailored ai models & workflows (enterprise)
    

- Suki: generates notes efficiency + lets doctors use voice commands to save time (ie. order this, schedule this), but again only helps with notes
    

- $299/month or $399/month per user for deeper EHR integration + more features
    

- Microsoft Copilot/Nuance: easier because works well with microsoft /epic products so can use the same system but still doesn’t combine patient charts.
    

- roughly $369–$600+/provider/month depending on volume tier and contract terms 
    

- Freed: most simple, easy for doctors to learn to use, and doesn’t need hospital approval
    

- $39/month (starter), $79/month (core), $119/month (premier), per provider
    

- Current medical imaging ai: Aidoc, [Viz.ai](http://viz.ai/), AZmed Rayvolve, [Qure.ai](http://qure.ai/) (specifically neurology), PathAI
    

- Their official websites have the most info on specifics
    
- Aidoc: strengths are finds abnormalities on scans quickly but only does imaging interpretation, not much after that for patient notes
    
- [Viz.ai](http://viz.ai/): detects strokes and can figure out which specialists should be involved but looks only at certain diseases not full workflow
    
- [Qure.ai](http://qure.ai/): can screen many X rays and CT scans but also just focused on finding abnormalities through scans
    
- Overall good but limited in that they mainly only help with imaging interpretation but nothing after to help doctor with the patient
    

- Current clinical documentation ai: OpenEvidence, UpToDate AI.
    

- OpenEvidence is mainly used
    
- ChatGPT, Claude, Grok, Perplexity are general AIs that are good for documentation
    
- Used for drafting patient communications, summarizing guidelines, and brainstorming
    
- For the best clinical accuracy, specialized models of AMBOSS LiSA, Gemini, Glass Health
    

- For analysis of pictures, CNNs (Convolutional neural network) will be used.
    

- Grad-CAM has shown that it could help with analyzing images by giving gradience to images (more on that later)
    
- ResNets or U-Nets can be used for precise segmentation of stroke lesions and brain tumors.
    
- Look into Multimodal Liver Segmentation, which looks at MRI and CT scans on livers to identify conditions and severity as well
    

- Uses deep learning architectures, such as 3D CNNs, U-Net variants, and transformers, to fuse features across modalities for enhanced boundary detection and lesion identification
    

- MRI, CT, PET, and EEG signals can be analyzed by CNNs
    
- A multimodal CNN that can be looked on is Visual Question Answering (VQA)
    

- Research current pain points: What do doctors need the most help with in the process, what takes the most time, what information gets missed? How can this AI help?
    

- Link: 
    

- [The 10 AI Tools Doctors Actually Use Daily (Ranked by Real Physicians)](https://www.offcall.com/learn/articles/the-10-ai-tools-doctors-actually-use-daily-ranked-by-real-physicians)
    
- [2025 Physicians AI report](https://2025-physicians-ai-report.offcall.com/)
    

- Survey priorities are unambiguous:
    

- 65% want documentation and scribing support
    
- 48% want administrative burden relief
    
- 43% want clinical decision support
    

- Possible pathway:
    

- We can focus on using separate models for separate roles
    

- Ex: a model can be used for scribing and documentation and another for clinical decision etc.
    

- For neurology, some AI’s score better in analyzing some data better than others, so we may need to utilize more than one LLM to get the best results from the data.
    

- Existing gastroenterology data: [Databases for Gastrointestinal Clinical and Public Health Research: Have Database, Will Research - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC10286872/)
    
- Existing neurology data: 
    

- [OpenNeuro](https://openneuro.org/)
    
- [Neuroscience Data](https://libguides.brown.edu/neuroscience/data) (from Brown University)
    

- Try to combine data into one or look into each datasets and pick out good ones
    

- Focus on these image datasets: brain wave tests (EEG), MRI, CT scans, PET scans, and EMG
    
- For computational research, datasets include neuroimaging (structural and functional), genomic data, and behavioral metrics.
    

- Imaging and Signal Analysis Deep learning models, particularly Convolutional Neural Networks (CNNs) and ResNets, analyze MRI and CT scans
    
- For functional data, algorithms process EEG signals
    
- Multimodal approaches that fuse EEG and MRI data have demonstrated superior diagnostic accuracy (up to 99% in some studies) compared to single-modality models by capturing both structural and functional deficits. 
    
- Electronic Health Record (EHR) Mining Machine Learning algorithms (e.g., XGBoost, Random Forests) scan longitudinal EHRs to predict disease conversion years before clinical diagnosis.
    
- There are Digital Biomarkers and Wearables AI that quantify severity continuously using digital biomarkers from smartphones and wearables. We can use data from this as well to determine severity.
    





**