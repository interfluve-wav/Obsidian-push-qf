---
title: wiki-log
updated: 2026-07-07 11:46 EDT
---

#capstone #ai-internship #neurology #log

---

# AI Internship — Vault Wiki Log

---

## 2026-07-03 — Session 4 (This Session)

**Ingested / created:**
- Simplified Competitor Teardown - Abridge (reformatted + validated + footnotes + backlinks)
- Simplified Competitor Teardown - Abridge validated against primary sources; two minor corrections: ~$800M (not ~$808M) and KUMC % methodology note added
- Concept pages: KUMC, JAMA Network Open, ASR, WER, JAMIA Open, Epic, Cerner and athenahealth, SMART-on-FHIR, KLAS, Dot-Phrase, UPDRS, EDSS, MIDAS, Mini-Z Burnout Scale, IDN

**Validation findings:**
- All major claims in the teardown verified against primary sources
- ~$800M funding total confirmed vs ~$808M (FierceHealthcare primary source uses ~$800M)
- KUMC percentages are post-implementation survey responses, not pre/post comparisons — methodology caveat documented

---

## 2026-07-01 — Session 3

**Rebuilt AI Internship/ vault from scratch — neurology-only scope.**
All gastro/GI content removed. No gastro references anywhere in the vault.

**Ingested:**
- Competitor Teardown - Abridge (validated, full 30,283 chars)
- Source - Trelis Medical ASR Benchmarks (3 custom datasets on HuggingFace, 16-model results)
- Entity - Abridge (updated with Trelis ASR benchmark data)
- Concept - AI Evaluation in Healthcare (updated with CER metric from Trelis)
- Index and wiki-log rebuilt for the new vault

---

## 2026-06 — Sessions 1–2

**Initial vault creation. Scope: AI in neurology, AI medical scribes, competitor landscape.**

## 2026-07-07 — Session 5 (This Session)

**Reorganized vault into subfolders and prepared for republish.**

### Reorganization
Split the flat `AI Internship - Self + Agentic Research/` folder (24 loose files) plus the sibling `Concept/` folder (15 files) into 6 dedicated subfolders:

| Subfolder | Contents | File count |
|---|---|---|
| `Sources/` | Whitepapers, papers, articles, Reddit pain point threads, research paper index | 5 |
| `Competitors/` | Abridge / Viz.ai / Ceribell teardowns, entity pages, cross-competitor analysis, deep-dive framework | 7 |
| `Concept/` | Frameworks, metrics (WER/CER/MTR), EHR concepts, healthcare orgs, clinical scales (UPDRS/EDSS/MIDAS/Mini-Z) | 17 |
| `Weeks/` | Week 1 logs, 26 June meeting summary | 2 |
| `Planning/` | Planning.md, Planning & Questions, Todo, Cadence Notes, Wireframes, Subspecialties Map | 6 |
| `Log/` | This wiki-log | 1 |

Plus a root `index.md` hub and one `index.md` per subfolder (7 indexes total).

### Deduplication
Removed 3 duplicate concept files that had copies in both `Concept/` (canonical) and `AI Internship - Self + Agentic Research/Concept - *.md` (stale): AI Evaluation in Healthcare, Confabulation Elimination, KUMC. Kept canonical versions only.

### Date/Time Stamping
All 45 markdown files now carry a YAML `updated: 2026-07-07 11:46 EDT` field in frontmatter (or prepended header for files that previously had no frontmatter). Stamping is part of the reorganization commit, not a per-edit log.

### Publishing pipeline (interfluve-wav/Obsidian-push-qf, branch v5)
- Discovered the build workflow uses `npx quartz build -d docs` (not `content/`)
- Repo was in a half-finished migration state with uncommitted destructive changes to `docs/`; stashed those, restored clean working tree
- Mirrored the reorganized vault into `docs/AI Internship/` via rsync
- Updated `.github/workflows/pages-deploy.yml`: `-d docs` → `-d docs/AI Internship` (so the publish path matches the vault layout)
- Custom domain: `research.intern.suhaaschitturi.com` (CNAME committed, DNS-only on Cloudflare, HTTPS enforced)
- Site status: HTTP 200 reachable, but previous deploy rendered the default Quartz welcome page because the build dir was stale; this commit should produce the first real AI Internship render

### Blocked / Open
- None new this session. Old blockers still apply: subspecialty decision, doctor interview scheduling, GPT-4 API access confirmation.
