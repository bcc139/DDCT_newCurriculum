# SESSION-HANDOFF — KMUTT-DDCT curriculum project state
**Updated:** 2026-10-14 (end of the 2026-10-13/14 mega-session) · Read this first. The **papers-pipeline** state
lives separately in `papers/summaries/AGENT-HANDOFF.md` (still accurate — pipeline complete). This file covers
everything else: the curriculum scan, industry/partnership research, the recommendation briefs, and pending actions.

## Mission context
DDCT = KMUTT dual undergrad programs (DD ~50/yr art-track, CT <10/yr tech-track), joint with DigiPen, international,
premium tuition, AI-skeptical students. **All-faculty meeting within October 2026** for the new-curriculum direction —
the deliverables below were built for it. User's stance: "it can be something new and different, but first we have to
know what others do."

## Deliverables (all links verified at write time)

| Artifact | What it is | Status |
|---|---|---|
| `papers/summaries/00-INDEX.html` | 83-paper synthesis: 8 patterns, 15-case shortlist, **prioritized reading list**, scenario map — all with 📄 PDF links (29 verified) | ✅ complete |
| `papers/summaries/*-digest.md` ×9 + `*-summary.html` ×9 | Per-folder digests (agents' returned digests + HTML cards) | ✅ complete |
| `curriculum/` (50 files + README) | World curriculum scan: DigiPen family (3 campuses — no others exist), Thailand ×3, Greater China ×10 (incl. CUC×DigiPen joint program, Tongji Design×AI dual degree, Tsinghua training plan), experience-first programs (NYU IMA, Parsons D&T pathways, USC IYA, UCLA DMA, GaTech CM, Aalto, RCA IED), other languages (JP FR RU DK ES BR EE), **Teaching AI** EdTech book (888 pp. PDF) + `teaching-ai-edtechbooks-digest.md` | ✅ complete |
| `curriculum/industry-partnerships/` (37 artifacts + README) | AI-company × university cases (Tripo/VAST, Deemos/ShanghaiTech, Meshy incl. **Thai classroom case**, Runway×NYU/USC, OpenAI×ASU, NVIDIA DLI) + creative industries (Netflix×Geidai & ×Otis, Salford×BBC/ITV, MVRDV×TU-Delft, Tencent×Tsinghua, LSE×Google, D&AD, Animationsinstitut). **Six partnership models** taxonomy | ✅ complete |
| `curriculum/program-support/` (7 artifacts + README) | Support-stack research: ETC personal-workstation policy, USC publishing label + Summer Bridge, NYU Open Library + tech lending, PlayStation First devkits, d.school coaching | ✅ complete |
| `06-ddct-recommendation-brief.html` | **The meeting deliverable**: constraints→diagnosis→Y1–Y4 architecture (one program, two passports)→six moves→industry stack→support layer→out-of-the-box ideas A–G→risks→reference index. **80 verified local links** | ✅ complete (verify links after any edit: `python check_links_all.py 06-ddct-recommendation-brief.html`) |
| `07-program-support-brief.html` | Beyond-classes supports: staff roles, materials/equipment, organizations, money-as-experience, phased rollout | ✅ complete |
| `2026-10-IPSJ-paper.pdf` (at `3D+AI curriculum/` root, one level up) + `2026-10-IPSJ-author-meeting-questions.md` | Kondo & Sato CT-framework paper (8-element rubric C1–C8, law students, prompt→p5.js art) + prioritized question list | ✅ read & assessed; noted as idea G in 06 |

## Pending actions
1. **Faculty meeting (this month)**: present 06 (primary) + 07; backup depth = 00-INDEX reading list + curriculum/industry READMEs. User may ask for a slide-deck version — none built yet.
2. **Author meeting (~2 weeks, Kondo)**: use `2026-10-IPSJ-author-meeting-questions.md`; lead with the collaboration offer (co-designed prompt-log study at DDCT).
3. **Manual downloads needed** (CLI-hostile hosts): CAMT full structure PDF (`go.camt.cmu.ac.th/.../structure%20and%20study%20plan%20DG%20(62-65).pdf` — broken TLS for CLI) · USC catalogue host · CMU IDeATe (connection reset) · Daegu (JS-shell site, dropped).
4. **Library misses**: folder-4 "DRS 2024 China AIGC" is the wrong source PDF (ethics statement) — re-download, then incremental re-digest folder 4 per `papers/summaries/AGENT-HANDOFF.md`. Plus 5 🔒 paywalled + 3 🤖 one-clicks in MANIFEST.html.
5. **Coverage gaps logged in curriculum/README.md**: Korea (Chung-Ang/KARTS/SKKU), Uppsala/NTNU, Cologne Game Lab, BUAS, USC SCA, NYU ITP grad, DADIU per-semester curricula (learnIT login), Luma/Kaedim/miHoYo/NetEase/Epic/Unity/Disney×CalArts/WPP.

## Conventions & tooling (established this session)
- **Naming**: `Institution - Program/Doc (lang, format).html|.pdf`; CJK in filenames breaks this Git-Bash+Windows-python combo — use ASCII names, note language in the name.
- **Fetch recipe**: curl `-sL --compressed --max-time 30 -A "Mozilla/5.0 ..."`; on failure retry via **webReader MCP** (server-side render; works for JS pages and CLI-blocked hosts; for key articles save the returned markdown as `.md (via webReader)` with source URL noted).
- **Always run downloads with per-fetch timeouts** (a hung host stalls un-timed chains); run long batches in background.
- **Link verification**: `check_links_all.py` (KMUTT-DDCT root) and `papers/summaries/check_links.py` — both `\\?\` long-path safe; plain `os.path.isfile` false-negatives ≥260 chars.
- **PDF→text quick reads**: pypdf via `pdf-conversion-lab/venv-mineru/Scripts/python.exe` (Windows paths only, not `/c/...`).
- **Digest style**: DDCT-mapped (S#/DR#/L# codes), numbers-or-"not reported", ★ = concrete transferable case.

## Quota
- **Brave search counter: 430/750** (as of 2026-10-14; warn user at 750). ~40 requests used across this session's collection rounds.
- Plan usage limits caused two agent-spawn failures on 2026-10-13 (5-hour, then weekly/monthly cap; nominal reset was 2026-10-19) — spawns succeeded same evening. If spawns fail, wait for reset; sub-agents never consumed tokens on rejected spawns.

## Where numbers came from (integrity note)
All cited effect sizes/percentages trace to `papers/text/*.md` (MinerU conversions), the collected artifacts, or the
IPSJ/Teaching-AI PDFs. "Not reported" convention used throughout. MIT cognitive-debt and Gerlich offloading cited
with preprint/correlational caveats in 06 §7.
