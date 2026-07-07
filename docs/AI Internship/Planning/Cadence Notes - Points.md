---
title: Cadence Notes - Points
updated: 2026-07-07 11:46 EDT
---

# Cadence Notes / Points

#capstone #ai-internship #neurology

> Short doc for team syncs — questions to raise, decisions needed, problems faced + solutions. Updated after each cadence meeting.

---

## Questions to Ask / Decisions Needed

- [ ] **Which subspecialty to focus on?** (Headache/Migraine vs Cognitive/Dementia vs Epilepsy vs Movement Disorders) — friend is interviewing doctors, user is doing competitor research. Need to align on ONE before Week 3.
- [ ] **What exactly is GastroNote / what did the other track build?** Context needed: demo? Product page? We need to know what "the parallel track" actually is before deciding how to differentiate.
- [ ] **What does "working product" mean for Week 8?** Blueprint only? Thin-slice demo? MVP? The team needs to align on deliverable scope before Week 3.
- [ ] **Friday Demos — what's the format?** Who attends? How long? Are they internal or with doctors/friends?
- [ ] **GPT-4 access — do we have it?** Week 1/2 research notes mention using GPT-4. Do we have API keys? Should we use Claude or MiniMax instead?
- [ ] **Doctor interviews — how many? Which specialties?** Friend is doing interviews. What questions are we asking? Is there an intake template?
- [ ] **Label Studio — who sets it up?** Week 3 mentions running the first training experiment. Who handles the ML infrastructure?
- [ ] **Data access — do we have real neurologist data?** The plan mentions OpenNeuro, CHB-MIT EEG, ADNI. Are those accessible? Any IRB issues?
- [ ] **What is the "Big Vision" we commit to?** The pre-visit synthesis layer is the technical wedge. But what's the 1-sentence product vision for the Week 8 deck?

---

## Problems Faced / Solutions

| Problem | Status | Solution |
|---|---|---|
| Reddit scraping blocked by JS challenge | Solved (partial) | Headless browser via delegate_task subagent; 11/19 threads extracted |
| GastroNote references in planning docs | Solved | Patched all 4 docs; original Planning & Questions.md left untouched (user-owned) |
| Abridge subagent didn't save file | Solved | Wrote the Abridge teardown directly using data from 4 web searches |
| Model switching mid-session (MiniMax / moa / minimax-oauth) | Ongoing | Active model confirmed: MiniMax-M2.7 via minimax-oauth |
| Doctor interview intake template | Not started | Need to build — suggested template in Week 1 research notes |
| 13 quick-scan competitor teardowns | Not started | ~6 hours of parallel subagent work; low priority until subspecialty chosen |
| CHB-MIT EEG dataset download | Not started | Needs to be set up before Week 3 training experiment |
| Label Studio setup | Not started | Needs ML infra owner before Week 3 |

---

## Agenda Template for Weekly Sync

```
1. Progress since last sync (5 min)
   - What did we finish?
   - What didn't we finish?

2. Decisions needed today (10 min)
   - Subspecialty choice
   - Deliverable scope for Week 8
   - Friday Demo format

3. Blockers (5 min)
   - Data access?
   - API keys?
   - Doctor interviews scheduled?

4. Next week priorities (5 min)
   - Who owns what?
```

---

## Open Threads (Low Priority but Worth Revisiting)

- **Bonk is still in active development** — Bonk engineering work is separate from this capstone. Keep separate.
- **EchoDubBot / Oracle VPS** — not relevant to capstone.
- **Memory consolidation reminder** — MEMORY.md is at 94% capacity. After Week 2, consolidate to make room for new capstone learnings.
