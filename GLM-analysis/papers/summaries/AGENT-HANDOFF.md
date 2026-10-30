# AGENT-HANDOFF — papers-digest pipeline state (for a NEW session)
**Updated:** 2026-10-14 · **PIPELINE COMPLETE** — this file now only covers the papers pipeline. The whole-project state (curriculum scan, industry research, recommendation briefs, pending meetings) lives in **`../../SESSION-HANDOFF.md` — read that first.** Skill: `papers-digest` at `~/.agents/skills/papers-digest/`.

## Mission
Summarize every paper in the 9 folders of `papers/` and extract **concrete, transferable cases** for the DDCT new-curriculum work; produce one HTML summary per folder + a master synthesis (`00-INDEX.html`), with minimum tokens and maximum specificity (numbers, practices, mappings).

## Current state (2026-10-13, late night — ALL PHASES DONE)
- **Phase 2 COMPLETE — 83/83 PDFs converted** to `papers/text/<folder>/<name>.md` (MinerU basic, base64 stripped, verified: 0 leftovers).
- **Phase 3 COMPLETE — all 9 folders digested.** Folders 1–3 (3 agents) + folders 4–9 (6 agents, one batch). Every folder has `<folder>-summary.html` + `<folder>-digest.md` in `papers/summaries/` (18 files, all verified on disk).
- **Phase 4 COMPLETE — `papers/summaries/00-INDEX.html`** built from the 9 digests: 8 convergent patterns, 15-case cross-folder shortlist, scenario coverage map (S0 strong / S4-S5 moderate / S1 partial / S2-S3 thin), gaps, folder index.
- **Known library misses:** 5 🔒 paywalled + 3 🤖 one-clicks (see `../MANIFEST.html`) **plus 1 wrong-source PDF**: `4-design…/2024 A study of students learning experience using AIGC tools in China (DRS).pdf` is actually DRS's 9-page Publication-Ethics statement, not the paper (confirmed via pypdf page inspection; MinerU basic AND advanced both extract only boilerplate). Re-download the real paper, delete the .md, re-run convert + strip, then re-digest folder 4 incrementally with the old digest attached.
- **Stale `.txt` files** from an older cancelled fallback run sit in `text/1-*` … `text/8-*`. They are NOT the pipeline output — agents read only `.md`. Safe to delete if the user approves (left untouched).
- `papers/summaries/` tooling: `report-template.html` (restored 2026-10-13) · `convert_1to3.sh`, `convert_4to9.sh` (reusable incremental MinerU loops) · `strip_b64.py` (strips BOTH markdown and HTML `<img>` base64 forms, `\\?\` long-path safe) · `check_links.py` (verifies every .pdf href in an HTML file, long-path safe — plain `os.path.isfile` gives false misses at ≥260 chars) · `extract_pdfs.py` (old fallback, superseded).
- Sibling context (agents do NOT need it): `../../01-concerns-breakdown.md` … `05-evidence…md`, `../..` project README.
- **Next natural steps (user's call):** present findings to the working group; fix the DRS miss; chase the 8 MANIFEST misses; when new papers land → incremental Phase 1–2 → re-spawn only affected folder agents with old digest attached.

## Phase-3 spawn instructions (for the folders 4–9 run)
Fill `references/agent-prompt-template.md` per folder (counts: 4-design 17 · 5-games 5 · 6-arch 4 · 7-eng 4 · 8-writing 15 · 9-gbl 4):
- `{TXT_DIR}` = `C:\Users\vvora\Downloads\zcode\3D+AI curriculum\KMUTT-DDCT\papers\text\<folder>`; `{FILE_COUNT}` per above.
- **Input-section delta (keep, it matters):** agents read **`.md` files only** — MinerU-converted, base64 already stripped; IGNORE `.txt`/`.short.txt` siblings (stale); budget = full read if ≤45k chars, else chunked read prioritizing abstract/methods/results/discussion; include the explicit per-folder file list so agents never glob.
- Launch the 6 Agent calls (general-purpose) **in one message** for parallelism. Agents write `<folder>-summary.html` + `<folder>-digest.md` into `papers/summaries/` and return only the digest.
- Folder hints (from the original 2026-10-12 handoff):
  - **4-design-and-art-education** — the DD branch core: design-pedagogy meta (N=2,847), China quasi-experiment (3 integration modes), Reflect-AI*, studio studies, animation+vibe-coding. Maps: L2/L3/L4, S1/S4, judgment notebooks. *Reflect-AI not yet in library (🔒 #3 priority).
  - **5-games** — game curriculum proper: jams as AI-learning format, asset-creation practices, GenAI synthesis, MKO autoethnography. Maps: L8, S4 blocks, S5-L3.
  - **6-architecture-studios** — closest studio pedagogy: ethics-embedded studio, AI joins the crit, 15-week studio. Maps: L4, crit redesign.
  - **7-engineering** — course-rebuild cases incl. faculty using AI to design the syllabus. Maps: L7, S0.
  - **8-writing-and-composition** — detection-reliability (61–69%), AI-resilient assessment, feedback-uptake (48–62% ignore AI feedback), MIT cognitive-debt EEG, offloading. Maps: DR23/DR3, 3-zone, tickets/vivas, L5.
  - **9-game-based-learning** — pedagogy category (games teach other subjects): GBL-for-AI-literacy (4-dimension outcomes), MDA framework. Maps: S0 fluency course taught gamefully, S5-L1.

## Phase-2 decision — settled 2026-10-12, executed 2026-10-13
MinerU 4 basic tier (venv + commands at `C:\Users\vvora\Downloads\zcode\pdf-conversion-lab\`): `mineru-kit.exe parse <pdf> -o text/<folder> --tier basic`, incremental on `.md` existence, then strip base64. Full run: 83 papers ≈ 2.5 h CPU (~60–100 s/paper). **Gotchas found in the field:**
- **Windows MAX_PATH:** one folder-4 paper (name ≈157 chars) made MinerU's write fail with a misleading "No such file" *after* successful inference. Workaround: `-o` to a short temp dir (e.g., `~/m_tmp`), then `mv` into place (MSYS handles long paths); Python touching such files needs the `\\?\` prefix (see `strip_b64.py`).
- The skill/REPORT base64 one-liner only removes markdown-style images; MinerU also emits `<img src="data:image…">` inside table HTML — use `strip_b64.py` (both patterns).
- For math-heavy papers you'll implement from, use `--tier advanced`.

## Incremental updates (the recurring-question answer)
Agents are one-shot per run; a completed agent can be resumed **only within the same session** (via its agentId/SendMessage). Across sessions, the folder **digest is the memory**: when new papers land → re-run Phase 1–2 (incremental; scripts above) → spawn that folder's agent again with its old digest attached + "summarize only new files, merge into existing HTML/digest".

## Cross-session notes
- **Conversion decision is time-boxed:** MinerU basic/advanced workflow decided 2026-10-12 (live experiment, `pdf-conversion-lab/REPORT.html`). Scheduled 3-month review fires **2027-01-13**. Don't re-litigate before then; do honor anything newer than REPORT.html.
- **Parallel AutoClaw experiment:** blind converter-vs-summary comparison in `pdf-conversion-lab/autoclaw-kit/`. `RESULTS.md` did not exist as of 2026-10-13 evening — check again next session; it may refine per-paper-type choices but does not block Phase 3.
- **GPU note:** marker/GLM-OCR paths need the dGPU unlocked (not Eco mode) — MinerU CPU paths don't care. Ollama + glm-ocr:latest already installed if ever needed.
- **Quota:** Brave counter last known 347/750 (no searches used in the 2026-10-13 sessions). Plan usage limits blocked agent spawns twice on 2026-10-13 afternoon/evening (weekly/monthly cap; nominal reset 2026-10-19 03:58) but the same 3 spawns succeeded ~18:50 the same day — quota apparently recovered or plan changed. If spawns fail again, wait for the reset rather than retrying repeatedly.

## Token rules (non-negotiable)
Pre-extracted text only (agents never touch PDFs) · reading budget per template · cheat-sheet in prompt (agents never read curriculum files) · digests returned, HTML to disk · no web in digest agents · incremental, never full-index rewrites.
