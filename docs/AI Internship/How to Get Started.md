---
title: "How to Get Started — AI Internship Onboarding & First 4 Weeks"
updated: 2026-07-07 12:24 EDT
tags: [capstone, ai-internship, neurology, onboarding, getting-started]
---

#capstone #ai-internship #neurology #onboarding

# How to Get Started

**For: anyone joining the AI Internship capstone** (including future-you if you step away for a few weeks). This is the single document that tells you where we are, what we've decided, what's unblocked, and what to do this week. Read it before anything else in the vault.

---

## Where we are (as of 2026-07-07)

**Stage:** Pre-Week 2. Week 1-2 research is done and validated. Week 2+ work (doctor interview, subspecialty pick, technical feasibility) is blocked on a meeting that hasn't happened yet with the rest of the team.

**Decided:**
- **Scope:** neurology only. No gastro, no GI. (Source: [[Competitor Teardowns - Cross-Competitor Analysis]], [[Neurology Subspecialties Map]].)
- **Strategic frame:** Layer 5 (pre-visit synthesis) is the wedge. No incumbent owns it. (Source: [[Layer 5 Wedge Memo]].)
- **Recommended 8-week path:** Headache / Migraine as the primary condition + caregiver-in-the-loop as a cross-cutting feature. (Source: [[Layer 5 Wedge Memo]], [[Neurology Subspecialties Map]].)
- **Vault is published:** https://research.intern.suhaaschitturi.com — 86 pages, validated, dated.

**Unblocked, in priority order:**
1. **Validation audit** (done 2026-07-07; HIGH-severity fixes applied). See `Validation/Validation Report 2026-07-07.md`.
2. **Competitor quick-scans** for the 13 lighter competitors (DeepScribe, Suki, Freed, RapidAI, Brainomix, Aidoc, NeuroQuant, Rune Labs, Empatica, Natus, encevis, Piramidal, DeepCura) — independent of subspecialty.
3. **Doctor interview intake template** (the script for the friend's first interview) — no decision needed.
4. **Quartz polish** (page title, hero text, favicon) — 10 min.

**Still blocked:**
- Subspecialty decision (team meeting not yet scheduled)
- Doctor interview scheduling (friend's side)
- GPT-4 / API access confirmation
- GastroNote context (Amar/Aditya haven't responded)
- Week 3+ training experiments (waiting on dataset choice)

---

## The 4 documents that matter most

If you read only 4 things, read these, in this order:

1. **`Planning/Layer 5 Wedge Memo.md`** — the strategic anchor. 1 page, 5-line argument. Read first.
2. **`Competitors/Competitor Teardowns - Cross-Competitor Analysis.md`** — the 0/3 ownership evidence, full 8-pain-point matrix, the 3 deep-dive summaries. Read second.
3. **`Planning/Neurology Subspecialties Map.md`** — the 31 subspecialties, 5-dimension scoring, top 5 candidates. Read third.
4. **`Sources/Week 1-2 - Reddit Patient Pain Points.md`** — the 8 patient pain points, verbatim from Reddit. The reason the wedge exists. Read fourth.

**Don't read in this order** the raw teardowns (Abridge / Viz.ai / Ceribell) until you have the frame. They're 30-50KB each and overwhelming without context. Skim the cross-competitor doc first, then dive into the individual teardowns for the company you care about.

---

## How to actually start (the next 4 weeks)

### Week 2 (current — finish by Sun 2026-07-13)

Goal: get the team meeting scheduled, get the doctor interview scheduled, finish competitor quick-scans.

- [ ] **Send the wedge memo** to Amar / Aditya / team. Subject line: "Pre-visit synthesis layer for neurology — feedback wanted by Friday." This is the single ask that unblocks the most.
- [ ] **Build the doctor interview intake template** (1 page, 15-min interview, anchored to the 4 unowned pain points in the wedge memo). Lives in `Planning/Doctor Interview Intake.md`.
- [ ] **Run competitor quick-scans** for the 4 highest-leverage players (DeepScribe, Suki, Aidoc, RapidAI). 30 min each, 2h total. Output: 4 short teardowns in `Competitors/`. Independent of subspecialty decision.
- [ ] **Schedule the team meeting** — even a 30-min sync to align on the wedge memo and the Headache + Caregiver recommendation. Without this, Weeks 3-8 stall.

### Week 3 (start 2026-07-14, after team meeting)

Goal: pick the subspecialty, run the first doctor interview, choose the dataset.

- [ ] **Pick subspecialty** in the team meeting. Default = Headache + Caregiver (the recommended path). Override only with strong counter-evidence.
- [ ] **Run friend's first doctor interview** using the intake template. Capture: which of the 4 pain points (#1 psych attribution, #2 13-year journeys, #6 between-visits, #7 caregivers) the doctor has personally seen.
- [ ] **Pick the dataset** based on subspecialty. Defaults: Headache → MIMIC-IV demo + synthetic migraine diary; Dementia → ADNI; Epilepsy → CHB-MIT EEG. Decision matrix in `Planning/Dataset Choice.md` (to be written).
- [ ] **Set up Label Studio** if the team has bandwidth. Otherwise defer to Week 4.

### Week 4 (start 2026-07-21)

Goal: market sizing + imaging AI landscape + first technical artifact.

- [ ] **Market sizing** for the chosen subspecialty (TAM / SAM / SOM). Use the pricing data from the 3 teardowns.
- [ ] **Imaging AI landscape** teardowns (RapidAI, Brainomix, Aidoc, NeuroQuant) — only if subspecialty is movement disorders, MS, or stroke. Skip for headache / dementia.
- [ ] **First baseline model** (CNN/RNN on chosen dataset) — only if the technical team has cycles.
- [ ] **Friday Demo #1** to the team — even if it's just "we have data loaded."

### Week 5-6 (start 2026-07-28)

Goal: 3 tracks running in parallel (Business / Clinical / AI). This is where the capstone shifts from research to build.

- [ ] Business track: market opportunity report, revenue model, pricing model
- [ ] Clinical track: subspecialty-specific workflow map, doctor interview synthesis
- [ ] AI track: prototype architecture (Layer 5 = RAG + multi-agent LLM + caregiver channel + wearable), first end-to-end demo

### Week 7-8 (start 2026-08-11)

Goal: deliverables check + final presentation.

- [ ] Cross-check all 3 tracks
- [ ] Build the Week 8 deck (see slide outline in `Competitor Teardowns - Cross-Competitor Analysis.md` §8)
- [ ] Record a thin-slice demo (the Layer 5 prototype, even if it's a static screenshot + 30-sec Loom)

---

## How decisions get made

The team is small and async. Default decision flow:

1. **Surface the decision** in the relevant doc (e.g., "Subspecialty: Headache + Caregiver" in `Planning/Neurology Subspecialties Map.md`)
2. **Wait 48 hours** for pushback in team chat
3. **If no pushback**, the recommendation in the doc becomes the decision
4. **If pushback**, schedule a 30-min sync; default to the doc's recommendation if no consensus

**Decisions that need the whole team:**
- Subspecialty pick
- Pricing model
- Final deck contents
- Anything that goes to Amar / Prasad / external

**Decisions any single person can make:**
- Which competitor to teardown next
- Which dataset to download
- Which concept page to write next
- Doc formatting, tags, structure

---

## How the vault is organized

```
AI Internship/
├── index.md                            (vault hub)
├── Competitors/                        (3 deep-dive teardowns + 2 quick-scans + framework + entity + cross-analysis)
├── Concept/                            (17 concept pages: WER, ASR, EHR, scales, organizations)
├── Sources/                            (whitepapers, papers, Reddit, Becker's profile, Trelis benchmarks)
├── Planning/                           (wedge memo, subspecialties map, todo, cadence, planning)
├── Weeks/                              (week-by-week logs)
├── Log/                                (wiki-log)
└── Validation/                         (audit reports — NEW 2026-07-07)
```

**Tag schema** (used in YAML frontmatter): `capstone`, `ai-internship`, `neurology`, plus per-doc tags (e.g., `scribe`, `patient-research`, `wedge`).

**Naming:** `Concept - ASR.md`, `Competitor Teardown - Abridge.md`, `Source - Becker's Abridge Profile.md`. Spaces in filenames are fine; Quartz slugifies them to triple-dash on the published site.

**Frontmatter on every file:** `title`, `updated` (YYYY-MM-DD HH:MM TZ). The `updated` field tracks when the file was last touched.

---

## How the publish pipeline works

1. Edit files in the local Obsidian vault at `~/Documents (On My Mac)/Obsidian.md/Main Sync Vault/AI Internship/`
2. Mirror to repo: `rsync -av --delete "VAULT/" "~/Documents/GitHub/Obsidian-push-qf/docs/AI Internship/"` (use `--delete` so deletions propagate)
3. Commit: `cd ~/Documents/GitHub/Obsidian-push-qf && git add "docs/AI Internship/" && git commit -m "..." && git push origin v5`
4. GitHub Actions runs `pages-deploy.yml`, which calls `npx quartz build -d "docs/AI Internship"` (note: **quote the path** — the space breaks the build otherwise)
5. ~1-2 min later, the change is live at https://research.intern.suhaaschitturi.com

**Custom domain:** research.intern.suhaaschitturi.com → CNAME → interfluve-wav.github.io (DNS-only on Cloudflare, HTTPS enforced by GitHub).

**Verification after push:** `curl -o /dev/null -w "%{http_code}\n" -L https://research.intern.suhaaschitturi.com/<slug>` should return 200.

---

## Common pitfalls (learned the hard way)

- **Don't anchor on subspecialty first.** Anchor on the wedge (Layer 5) first; the subspecialty is the *application* of the wedge. Picking subspecialty before sharing the wedge memo leads to the team picking based on the wrong criteria.
- **Don't skip the validation pass.** Pre-Week 8, run a 30-min audit of every claim in the published site. We just did this and found 4 HIGH-severity errors that would have been caught in any investor / press call. `Validation/Validation Report 2026-07-07.md` is the template.
- **Don't trust third-party pricing.** Abridge's pricing is enterprise-only and not published; the $208-$800/provider/mo range comes from review sites, not the company. State it as "estimated."
- **Reddit upvote counts are timestamps.** Don't cite "73 pts" as a verified figure. Either re-pull on a fixed date or replace with "top-voted comment."
- **GitHub Pages build path needs quotes** in the workflow if it contains spaces. We hit this once; the fix is `-d "docs/AI Internship"`.
- **The "5 geriatric neuro sites" claim is unverified.** It's load-bearing for the dementia wedge but not confirmed. Re-check against the UCNS fellowship directory before Week 8.

---

## What to read if you only have 5 minutes

1. The TL;DR section of the [[Layer 5 Wedge Memo]] (2 min)
2. The "5-layer AI taxonomy mapping" table in [[Competitor Teardowns - Cross-Competitor Analysis]] (1 min)
3. The "Top 5 to consider" table in [[Neurology Subspecialties Map]] (1 min)
4. Skim the 8 pain points in [[Sources/Week 1-2 - Reddit Patient Pain Points]] (1 min)

After 5 minutes, you should be able to answer:
- What is the wedge? (Pre-visit synthesis; Layer 5; no incumbent owns it.)
- Why neurology? (Highest social-impact subspecialties, doctor shortage, patient pain.)
- What's the recommended subspecialty? (Headache + caregiver-in-the-loop.)
- What are the 4 unowned pain points? (13-year journeys, between-visits data, caregivers, "I don't know" verdict.)

If you can't, ping me — the docs need a re-write.

---

## What to read if you have 30 minutes

Add:
- The full [[Layer 5 Wedge Memo]] (7 min)
- The full cross-competitor analysis (10 min)
- The full subspecialties map (8 min)
- Skim the Abridge teardown (5 min)

---

## What to read if you have 2 hours

Add the full Abridge, Viz.ai, and Ceribell teardowns, the concept pages for WER / ASR / SMART-on-FHIR, and the Reddit pain points corpus. You should be ready to defend the wedge and the subspecialty pick in any conversation.

---

*This document is the single source of truth for "how do I get up to speed on the AI Internship capstone." If anything in it is wrong or stale, edit it. The whole point is that the next person (or future-you) can read one document and be productive in 30 minutes.*
