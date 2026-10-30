# Evidence File — AI-in-Curriculum Integration Across Academic Branches
**For:** DDCT curriculum working group · **Question:** what do papers, case studies, and faculty reflections from CS, design, games, architecture, engineering, writing, and business actually report — concretely — when AI is integrated into curricula? What worked, what didn't, and what results exist?
**Method:** 14 targeted searches (papers via ACM/Springer/Elsevier/arXiv/MDPI/Frontiers + teaching-center cases + practitioner blogs), 2026-10-12. All links archived in `../references.md` (session 11).
**Companions:** `01-concerns-breakdown.md` · `02-curriculum-scenarios.md` · `03-direction-first-curriculum.md` · `04-social-science-counterweight.md`

---

## 1. The big picture first — meta-analyses (do students learn better with GenAI?)

| Study | Finding |
|---|---|
| **Ma et al. 2025, *J. Computer Assisted Learning* (Wiley)** — meta-analysis of GAI impact on learning outcomes | Positive overall: pooled effect **g ≈ 0.86 for achievement**, **≈ 0.80 for motivation** (cognitive, competency, affective dimensions) |
| **Systematic review & meta-analysis, *Learning and Individual Differences* (2025)** | Large effects in **language skills, academic achievement, affect-motivation**; only **medium effect on higher-order thinking** — the gap that matters most for design education |
| **Meta-analysis of 59 experiments / 29 sources on higher-order thinking (PMC)** | GenAI can support HOT, but effects are moderated by *how* it is instructionalized — mechanisms and moderators matter more than access |
| **Experimental-studies meta-analysis (PBL/IBL moderation)** | In problem-based learning, **upper-secondary students gained more than tertiary**; chatbots with **dual conversational + resource roles** outperformed single-role designs |

**Honest counterweight (single studies):** an **ICSE-SEET 2024 CS1 experiment** found ChatGPT gave *no significant performance gain* on assignment-style tasks — and students **largely stopped exploring other educational resources** once using it; a quasi-experimental high-school study found assistance "may not yield substantive benefits and may diminish flow, self-efficacy, and achievement"; a counterbalanced CS1 study (2025) is measuring exactly where quality vs. understanding diverge. **Pattern: pedagogically *aligned* AI helps; raw access is neutral-to-harmful.**

## 2. Computer science — the deepest evidence base

### ★ Harvard CS50's Duck Debugger (the flagship concrete case, with numbers)
- **What:** CS50.ai — a GPT-4-based "rubber duck debugger" built atop Azure OpenAI, deliberately prompted/fine-tuned to **lead students toward answers rather than spoil them** ("ChatGPT itself is all too willing to provide outright answers").
- **Results:** **201k students/teachers have generated ~35k prompts/day — ~9.4 million prompts total**; students described it as "a personal tutor," saying raw ChatGPT "would have definitely detracted from learning" (SIGCSE TS 2024 paper, Liu, Zenke, Malan et al.); a 2025 follow-up ("Improving AI in CS50: Leveraging Human Feedback") had teaching fellows grade **1,309 response pairs** before/after the Duck's introduction to keep quality rising.
- **Lesson for DDCT:** the tool's *pedagogical alignment* (tutor-not-answerer) is the design variable — exactly the "brief → draft → critique" discipline of our AI-as-junior-staff loop.
- Links: paper https://cs.harvard.edu/malan/publications/fp0627-liu.pdf · SIGCSE 2024 https://dl.acm.org/doi/10.1145/3626252.3630938 · usage stats https://cs50.harvard.edu/x/2025/notes/ai/ · tool docs https://cs50.readthedocs.io/cs50.ai/

### The SIGCSE/ITiCSE literature
- **Becker et al. 2023, "Programming Is Hard — Or at Least It Used to Be"** — the foundational paper reframing code-generating AI as *educational opportunity*, not just integrity threat (cited across SIGCSE 2026).
- **SIGCSE 2025: "Understanding the Impact of Using GenAI Tools in a Database Course"** — moving from perceptions to measured behavior in a real course.
- **Instructor/student gap:** engineering-education studies find **students report higher familiarity and engagement with GenAI than their instructors** — faculty development is the bottleneck, not student readiness.

## 3. Assessment frameworks that achieved scale (directly reusable)

### ★ The AI Assessment Scale (AIAS — Perkins, Furze, Roe et al.)
- **What:** a five-level scale — **No AI → AI Planning → AI Collaboration → Full AI → AI Exploration** — for declaring and designing the role of AI *per assessment task*.
- **Adoption results:** used by **250+ schools and universities worldwide, translated into 16 languages**, featured in **UNESCO digital week**, promoted by Australia's **TEQSA** for assessment transparency; revised framework paper arXiv:2412.09029; full JUTLP 2025 history paper.
- **DDCT relevance:** this is the published, globally-adopted version of the 3-zone policy in `02-curriculum-scenarios.md §6` — adopt/reference it rather than inventing local language from scratch (instant credibility with committees).
- Links: https://aiassessmentscale.com/ · https://arxiv.org/abs/2412.09029 · Iowa CTL explainer: https://teaching.center.uiowa.edu/ai-assessment-scale-reflecting-ai-assignment-design

### ★ Mollick & Mollick — "Assigning AI: Seven Approaches for Students, with Prompts" (2023)
- Seven pedagogical roles with ready prompts: **AI-tutor (knowledge), AI-coach (metacognition), AI-mentor (ongoing feedback), AI-teammate (collaboration), AI-tool (performance), AI-simulator (practice), AI-student (reverse-check understanding)**.
- The practical bridge from policy to assignment design; basis of **Wharton Online's Coursera course "AI in Education" built in collaboration with OpenAI** (Nov 2024) — an institutional-scale faculty-training precedent (OpenAI's education VP publicly framing Wharton as the lighthouse case).
- Links: https://arxiv.org/abs/2306.10052 · Coursera course: https://www.coursera.org/learn/wharton-ai-in-education-leveraging-chatgpt-for-teaching · launch: https://news.wharton.upenn.edu/press-releases/2024/11/wharton-online-launches-ai-in-education-leveraging-chatgpt-for-teaching-developed-in-collaboration-with-openai/

## 4. Art & design education (the DDCT home branch)

| Study | What was done | Result / reflection |
|---|---|---|
| ★ **Reflect-AI (Springer chapter, 2025/26)** | 4-week in-situ deployment in **undergraduate design studios**: an "Anticipate–Interrogate–Act" micro-cycle embedded into each AI interaction; compared baseline AI vs. structured reflection vs. +counterfactual prompts vs. +peer audit | Reframed AI use **from idea generation to reflective co-creation** — students articulated intent, inspected outputs, justified decisions. The closest published validation of our judgment-notebook design |
| ★ **China quasi-experiment (ETRD, 2026)** | Three conditions in university design courses: **traditional / chatbot-assisted / fully-integrated AIGC** | Integration *mode* changed outcomes in product performance, **self-efficacy, and role clarity** — "not whether AI is used, but how it is instructionally integrated" |
| **Design-ideation study (ScienceDirect, 2024)** | AIGC in ideation tasks | **Significant self-efficacy gains across skill levels**; but receptivity varied by student ability — heterogeneity is real |
| **Frontiers in Education (2026)** | Mixed-methods on **reconfiguring graphic design education** | Proposes human-agency + adaptive-curriculum framework; documents curriculum-level reorganisation needs (expertise, pedagogy, assessment, governance) |
| **MDPI *Computers* 14(4) (2025)** | 10 art students, composition task **traditional vs. GenAI**, observed | Micro-scale but concrete behavioral comparison |
| **DRS 2024 (China)** | Qualitative, **9 bachelor design students** using AIGC in projects | Learning-experience impacts documented (motivation, dependency tensions) |
| **TAM+TPACK empirical study (Sustainability, 2025)** | Chinese design courses | Extracts **integration patterns**: introduction methods, instructional role positioning, task types, assessment criteria |
| **Visual-design courses (T&F, 2025; Weinan Normal + Dong-A)** | Course-level AIGC integration | Documents philosophy/model change in visual design teaching |
| **Generative art as pedagogical tool (art schools)** | Curriculum-mapping scheme | Argues assessment must be **longitudinal/process-based, not artifact-points** — matches our growth-rate assessment |
| **Lindenwood faculty paper (Hutson & Cotroneo)** | Prompt engineering + iterative process in art curriculum | Student-ranked usefulness of integration ways |

## 5. Games (the DDCT-specific branch)

- ★ **NVIDIA GenAI game-jam case study (CVPR 2025 workshop, Spjut)**: a several-day jam building *Plunderwater: Sunken Treasure* with heavy GenAI use — an honest "what worked / what needs improvement" reflection from inside the process (even the title came from GenAI suggestions). https://openaccess.thecvf.com/content/CVPR2025W/CV2/papers/Spjut_A_Generative_AI_Game_Jam_Case_Study_from_October_2024_CVPRW_2025_paper.pdf
- **DiGRA jam study — GenAI in game asset creation**: survey of jam participants (n=37): **64.9% used Bing/DALL-E, 51.4% ChatGPT**, 32.4% multi-tool — baseline data on what students actually reach for unprompted. https://dl.digra.org/index.php/dl/article/download/2438/2431/2467
- **arXiv 2509.11898 — qualitative synthesis of GenAI in game development** (10 studies across education/practice/indie/jams): themes of creativity, efficiency, **ethics and authorship** — the reflection base for our theory spine.
- ★ **"Generative AI as a More Knowledgeable Other" (MDPI *Applied Sciences*)** — an **autoethnography by a game-design teacher** integrating GenAI as scaffolding "MKO": the kind of first-person faculty reflection the user asked for.
- **"Materializing the abstract: understanding AI by game jamming" (Frontiers in Comp Sci, 2022)** — argues jam formats are *uniquely suited* to learning AI as a **design material**: direct validation of block/jam formats in Scenarios 4–5.

## 6. Architecture studios (closest cousin to DDCT's studio pedagogy)

- ★ **MDPI *Buildings* (2025): "Teaching with AI in Architecture: Embedding Technical Skills and Ethical Reflection in a Core Design Studio"** — dual-module framework (AI skills + AI ethics) in the core studio. **Key result from student feedback: students preferred ethics *embedded* in the studio rather than taught as separate instruction; engagement was phase-dependent and tool-sensitive; modular AI education proved scalable**; integration raised digital adaptability and strategic thinking while surfacing authorship/bias/accountability reflection.
- **15-week integrated studio study (J. Asian Architecture & Building Eng., 2026)** — process-oriented pedagogies for AI's "creative unpredictability": tracks design thinking, creativity, self-reflection over a full studio (same length as a DDCT semester).
- **"Reflection in co-action: AI joins the crit" (IJTDE, 2026)** — reframes studio "learning by doing" as **"learning by co-doing"** with AI present in critique.

## 7. Engineering

- **ASEE (chemical engineering): rebuilding Thermodynamics / Material & Energy Balances / Kinetics *with* AI** — students critique AI-generated answers in structured settings; **faculty also used AI to design the syllabus, materials, assessments** → "roadmap for AI-driven course redesigns" and evidence on how perceptions evolve.
- **Mechanical engineering (J. STEM Ed. Research, 2026)** — GenAI-redefined problem generation with measured learning outcomes.
- **Cross-cutting finding:** instructor adoption trails student adoption (gap studies) — echoing our UNESCO faculty-ladder recommendation.

## 8. Writing & composition (the integrity-stress-test branch)

- ★ **Frontiers in Education (2026): AI-assisted revision assignment design** — two consecutive assignments where students **draft without AI, then revise with AI, then reflect**; analysis of how students select/use tools from their own reflective responses. A clean, concrete assignment template transferable to design crits.
- **First-year writing framework (ScienceDirect, 2024)** — affordances/limitations + directed reflection (warns courses "underutilized directed reflection").
- **Kennesaw State ENGL1101 pilot** — AI-integrated composition structure across two sections, with teacher-research **reflective journal** capturing decision points.
- **Cornell teaching case studies** — students account for AI use via **instructor conferences + written reflections** tied to their own projects.
- **University of Delaware** — a first-year writing course redesigned to *teach* AI use critically (profiled as a faculty transformation story).
- **General-education course study (PMC)** — where AI was **explicitly permitted**, qualitative analysis of documented reflections showed uses from ideation → revision → structural refinement; permission + documentation yields rich data, not chaos.

## 9. Institutional & faculty-development cases

- ★ **Indiana Wesleyan University "Faculty Course Refresh Institute" (EDUCAUSE Review, Mar 2026)** — a structured institute moving faculty from "whether" to "how" of AI use; the concrete template for DDCT's UNESCO-ladder faculty program.
- **NIU CITL: "Before you ban, require, or ignore AI: a reflection framework for faculty"** — starting question is *what role should AI play in this learning activity*, not "how do I add AI."
- **FeedbackFruits practitioner guide** — process-visibility moves that survive AI: **outline-before-final, brief self-reflection, documented AI use (tools + prompts + outputs), peer-review stage** — "meaningful evidence of engagement without dramatically increasing grading burden" (= our disclosure + dossier design).
- **Faculty Focus (Clark, 2026): "AI didn't break assessment: it exposed what was already broken"** — the reflection framing our Assessment Guidelines already assume.

## 10. Synthesis — eight evidence-backed lessons for the DDCT scenarios

| # | Evidence lesson | Source anchors | DDCT mapping |
|---|---|---|---|
| L1 | **Aligned AI beats raw AI**: tutor-styled CS50 Duck (9.4M prompts, "personal tutor") vs. null-to-negative CS1 results and displaced help-seeking | §1–2 | AI-as-junior-staff loop's BRIEF→CRITIQUE discipline; avoid "just let them use ChatGPT" integration |
| L2 | **Integration mode is the variable**, not use itself (traditional vs chatbot vs integrated conditions → different outcomes) | §4 China quasi-exp | The 3-zone policy *per assignment*, borrowed from AIAS (250+ institutions, 16 languages) |
| L3 | **Reflection scaffolds are the strongest lever**: Reflect-AI's Anticipate–Interrogate–Act; AIAS's task redesign; Frontiers' draft-then-revise-then-reflect | §3–4, §8 | Judgment notebooks + tickets (03-direction-first) now have published validation |
| L4 | **Embed ethics inside the studio** — students preferred it; separate modules rated worse | §6 architecture | Ethics thread design in Scenario 0; Brake·Anchor·Engine spine (04) |
| L5 | **Process visibility beats surveillance** — documented AI use, outlines, reflections, peer stages | §9 | Disclosure forms + making-of dossiers (DR16/DR23) |
| L6 | **Overall effects positive (g≈0.86 achievement) but HOT only medium; heterogeneity by student ability** — protect fundamentals and differentiate | §1, §4 | AI-off craft core; growth-rate assessment; blind taste tests |
| L7 | **Faculty readiness is the bottleneck** (student>instructor adoption; IWU institute model) | §2, §7, §9 | UNESCO teacher ladder + Course-Refresh-Institute copy in Phase 1 |
| L8 | **Jam/block formats are validated AI-learning media** (NVIDIA case, DiGRA baseline, "AI as design material") | §5 | Tool-sprint blocks (S0), Atelier blocks (S4), Academy L2 |

**One-line takeaway:** the literature has moved from *should we* to *how* — and the "how" that works (aligned roles, disclosed zones, reflection scaffolds, embedded ethics, process evidence) is precisely the architecture already designed in files 01–04; this file supplies the citations to defend each element to a committee.

---

## 11. 2026 additions — post-2024 refresh (added 2026-10-12)

Per faculty decision, the **fetch-priority list in `papers/MANIFEST.md` now excludes 2024 papers** (too old for AI's pace); 2024 evidence above remains cited for historical grounding. New sweep (all 2025–2026; ✅ = PDF in `papers/`):

**Design & animation (the DDCT branch keeps deepening)**
- ✅ **"Effectiveness of generative AI in higher education design pedagogy: a meta-analysis of usage modes" (*IJTDE*, 2026)** — PRISMA synthesis of **27 controlled studies, N = 2,847 (2023–2026)**: the first *design-pedagogy-specific* meta-analysis; usage modes (how AI is integrated) are the analytical axis — i.e., the meta-analytic version of our L2. https://link.springer.com/article/10.1007/s10798-026-10122-6
- ✅ **Double Diamond + GAI in design learning (Frontiers in Psychology, 2026)** — structured design-thinking strategy guiding GAI use → design achievement, creative self-efficacy, problem-solving: theory-structured AI use beats unstructured use. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1847432/full
- ✅ **GAI for innovative thinking in animation teaching (Scientific Reports, 2025)** — animation-teaching strategies under GAI. https://www.nature.com/articles/s41598-025-03805-y
- ✅ **Collaborative creation framework for experimental animation pedagogy — GAI + *vibe coding* (Frontiers in Psychology, 2026)** — the first pedagogy paper to formalize vibe coding in animation studios. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1940505/full
- ✅ **GenAI in creative education: baseline-linked evidence (Frontiers in Psychology, 2026)** — 133 art students, **prior-performance-linked** final assessments + authorship perceptions — assessment design directly relevant to our growth-rate approach. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1956939/abstract
- ✅ (user-contributed) **Undergraduate architecture design studios in transition — critical review (2026)** and **"Rewriting the curriculum: a systematic review of generative AI-driven pedagogical change and emerging systems of learning in higher education (2026)"** — both added directly to the papers library.
- ✅ **Customized GAI in visual communication design education — engagement & emotions (MDPI Sustainability, 2026)** — user-retrieved, in library. https://www.mdpi.com/2071-1050/17/22/9963
- ✅ **Creative Problem Solving + GenAI in animation storytelling — sustainability competencies (MDPI Sustainability, 2026)** — user-retrieved, in library. https://doi.org/10.3390/su18083858
- ✅ **Impact of GenAI on student creativity in art & design — meta-analysis (J. Curriculum Studies Research, 2026)** — user-retrieved, in library. https://curriculumstudies.org/index.php/CS/article/view/1108
- **Evaluating creativity in GenAI outputs — dimensions & cross-national differences among art/design students (Creativity Research Journal, 2026)** 🔒 https://www.tandfonline.com/doi/full/10.1080/10400419.2026.2729228
- ✅ **GenAI in higher art education — systematic review of tools, pedagogies, practices (SN Computer Science, 2026)** — user-retrieved, in library. https://link.springer.com/article/10.1007/s42979-026-04788-x
- **GenAI in STEAM education — review of 21 empirical studies (Education Sciences, 2026)** 🤖 https://doi.org/10.3390/educsci16071012
- ✅ **GAI interaction & output quality → university learning outcomes (Scientific Reports, 2025)** — technology-mediated model linking *interaction quality* to outcomes. https://www.nature.com/articles/s41598-025-08697-6

**AI literacy (the fluency-course evidence)**
- ✅ **AI-literacy interventions — three-level meta-analysis of 59 studies (Learning and Individual Differences, 2026)** — user-retrieved, in library; the citation for Scenario 0's AI-Fluency core. https://www.sciencedirect.com/science/article/pii/S1747938X26000527
- ✅ **A discipline-agnostic AI literacy course for academic research — architecture, pedagogy, implementation (arXiv, 2026)** — a real course (BSTA 495/395) with pre/post outcome evidence from its Spring 2026 first offering. https://arxiv.org/html/2604.27225
- **AI literacy → engagement, with psychological capital as mediator (Frontiers in Psychology, 2026)** 🤖 https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1892204/full

**Games — game curriculum proper (making & studying games)**
(No new 2026 entries this round; the §5 base above plus the library's jam/synthesis/autoethnography papers remain the core.)

**Game-based learning & gamification — a distinct category (faculty correction, 2026-10-12)**
*GBL/gamification uses games or game mechanics to teach other subjects — it is a pedagogy, not game curriculum. Kept for DDCT because it evidences (a) teaching the AI-Fluency course gamefully (Scenario 0 / Academy L1) and (b) the educational-games market niche. Filed under `papers/9-game-based-learning/`.*
- ✅ **AI-supported game-based learning — systematic review (Behavioral Sciences, 2026)** — user-retrieved, in library (folder 9). https://doi.org/10.3390/bs16071050
- ✅ **AI-enhanced MDA framework for educational game design (Research in Learning Technology, 2026)** — user-retrieved; filed in folder 9. https://journal.alt.ac.uk/index.php/rlt/article/view/3746
- **Gamified AI-supported environments — systematic review & meta-analysis (Frontiers in Education, 2026)** 🤖 https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2026.1754080/full
- ✅ **Game-based learning for asynchronous AI-literacy — cognitive/behavioural/affective/ethical outcomes (European J. of Education, 2026)** — user-retrieved, in library (folder 9). https://onlinelibrary.wiley.com/doi/10.1111/ejed.70658

**Computer science — game programming, engines & AI-assisted coding (folder-2 expansion, 2026-10-12)**
- ✅ **How AI assistance impacts the formation of coding skills (Anthropic RCT — Shen & Tamkin, 2026)** — the *skill-formation* experiment: over-reliance on AI assistance measurably harms skill development — the strongest published evidence yet for our AI-off craft core / "taste before tools" (DR3, L1). https://www.anthropic.com/research/AI-assistance-coding-skills · arXiv:2601.20245
- ✅ **Effects of GitHub Copilot on computing students in brownfield coding tasks (ICER 2025)** — realistic *legacy-code* tasks: effectiveness, efficiency, and process effects; documents students' "one-shot prompting then debug" behavior. https://dl.acm.org/doi/full/10.1145/3702652.3744219 · arXiv:2506.10051
- ✅ **Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency (2026)** — *writing skill predicts vibe-coding performance* and prompt quality is the mechanism — empirical backing for the direction-first thesis (tickets/critique writing as programming training). arXiv:2603.14133
- ✅ **Vibe coding with preservice teachers (Frontiers in Psychology, 2026)** — pre/post pilot: programming self-efficacy and intentions to use GenAI. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1957111/full
- ✅ **Vibe coding before the trend (2026)** — four student cohorts (ICT/marketing/journalism) doing vibe-coding challenges before it was named. arXiv:2605.07751
- ✅ **Large Language Models in Computer Science Education — systematic literature review (SIGCSE TS 2025)** — the branch's map paper (CC-BY). https://dl.acm.org/doi/10.1145/3641554.3701863 · author preprint: https://lsiddiqsunny.github.io/public/sigcse_ts25-preprint.pdf
- ✅ **A Survey of LLM-Based Applications in Programming Education (2025)** — automation vs. human-oversight balance across 2021–2025 systems. arXiv:2510.03719
- ✅ **Adoption of AI-coding assistants in programming education — extended TAM (J. Computers in Education, 2025)** — trust + learning motivation as adoption drivers. https://link.springer.com/article/10.1007/s40692-025-00375-w
- ✅ **Teaching computer game development with Unity engine — a case study (CEUR, 2023)** — the rare engine-teaching case study (pre-GenAI baseline; kept as the Unity-pedagogy anchor). https://ceur-ws.org/Vol-3482/paper330.pdf
- 🔒 **How Generative AI Influences Learning Outcomes in Programming Education: A Three-level Bayesian Meta-analysis (Educational Psychology Review, 2026)** — the programming-specific meta resolving "inconsistent evidence" — new #2 priority. https://link.springer.com/article/10.1007/s10648-026-10211-x
- 🤖 **Influence of AI Tools on Learning Outcomes in Computer Programming — meta-analysis (Computers, 2025)**: https://www.mdpi.com/2073-431X/14/5/185 · **Does generative AI help in learning programming (Computers and Education Open, 2025)**: https://www.sciencedirect.com/science/article/pii/S2451958825000570 · **Scoping review of vibe coding & AI-assisted programming in university computing education (2026)**: https://www.mdpi.com/3042-8130/2/4/34
- 🔒 lower priority: GenAI-in-game-development bibliometric (ACM AIVRID 2025): https://dl.acm.org/doi/10.1145/3777730.3777843 · vibe coding + flow theory model (J&amp;MC Educator 2026): https://doi.org/10.1177/10776958251407389
- *(Non-paper engine resource:* Epic's "Player to Creator" curriculum guide, LEGO Fortnite → Unreal Engine: https://dev.epicgames.com/community/learning/courses/lXx/player-to-creator-curriculum-guide-from-lego-fortnite-to-unreal-engine/MZ1r/player-to-creator-curriculum-guide-unreal-engine-for-game-development *)*

**Writing & composition — integrity + AI-assisted pedagogy (folder-8 expansion, 2026-10-12)**
*The user's two questions — how to stop AI-ghostwritten submissions, and how to encourage good AI-assisted writing — now have a direct evidence base:*

**Stopping AI submissions — detection does NOT work; redesign does:**
- ✅ **"Who wrote this?" — reliability of GPTZero, Pangram, Copyleaks, Turnitin (Int'l J. Educational Integrity, 2026)** — four tools × four text types (human / AI / hybrid / "humanised" AI): detectors are unreliable, especially on hybrid and humanised text. https://link.springer.com/article/10.1007/s40979-026-00226-w
- ✅ **Evaluating accuracy and reliability of AI content detectors (IJEI, 2026)** — companion study; reported overall accuracies as low as **61% (Turnitin) / 69% (Originality.ai)** on mixed texts. https://link.springer.com/article/10.1007/s40979-026-00213-1
- ✅ **Designing AI-resilient assessment — four-pillar framework (Frontiers in AI, 2026)** — the constructive alternative: redesign for process, presence, and oral evidence rather than police text. https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2026.1841682/full
- ✅ **Reimagining writing assessment for the AI era — systematic review of 19 studies (Frontiers in Psychology, 2026)** — students face "functional failure" distinguishing AI-as-tool vs AI-as-substitute *without pedagogical scaffolding*; faculty feel underprepared. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1809174/full
- 🤖 MDPI *Information* — effectiveness & ethics of detection tools: https://www.mdpi.com/2078-2489/16/10/905 · T&F *Teaching in Higher Education* — practice-based equitable redesign framework: https://www.tandfonline.com/doi/full/10.1080/13562517.2026.2670362

**Encouraging good AI-assisted writing — feedback design is the lever:**
- ✅ **AI-mediated feedback improves revisions — RCT with FeedbackWriter in a large undergrad course (2026)** — structured AI feedback *integrated into the course* outperforms conventional feedback on revision quality. arXiv:2602.16820
- ✅ **Revising with AI (Frontiers in Education, 2026)** — **48–62% of learners don't use the AI feedback they're given** — the uptake problem is bigger than the quality problem. https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2026.1702406/full
- ✅ **"Stop perfecting the feedback, start supporting the uptake" (Frontiers in Education, 2026)** — the position paper version of that finding: design for *use* of feedback, not better feedback. https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2026.1737037/full
- ✅ **Grammarly-RCT for EFL writing (Discover Education, 2025)** — 60 postgrads: AI feedback improved proficiency, revision frequency, and quality. https://link.springer.com/article/10.1007/s44217-025-00602-7
- 🤖 **"Generative AI offers more, but students revise less"** (IJETHE 2026) — the cautionary title-finding: more AI feedback ≠ more revision. https://doi.org/10.1186/s41239-026-00579-9

**Why the AI-off zones matter (cognition evidence):**
- ✅ **MIT Media Lab — "Your Brain on ChatGPT": cognitive debt in essay writing (2025)** — EEG across 32 regions: LLM group showed **lowest brain engagement and underperformance at neural, linguistic, behavioral levels**, with cumulative "cognitive debt" across sessions. https://www.media.mit.edu/publications/your-brain-on-chatgpt/ · arXiv:2506.08872
- ✅ **Cognitive offloading through digital tools vs critical thinking, persistence, depth (Frontiers in Psychology, 2026)** — the mechanism study. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2026.1781101/full
- 🤖 Gerlich (Societies 2025) — the N=666 cognitive-offloading/critical-thinking study: https://www.mdpi.com/2075-4698/15/1/6 · JISE narratives of offloading: https://www.ojed.org/jise/article/view/10565
- 🤖 JoWR special issue — empirical studies of writing & GenAI intro (Anson & Cole): https://www.jowr.org/jowr/article/view/2120

**Faculty & assessment**
- ✅ **Reframing faculty development for digital transformation and GenAI (PMC, 2026)** — user-retrieved, in library. https://pmc.ncbi.nlm.nih.gov/articles/PMC13377356/
- ✅ **Redesigning teaching, learning & assessment — constructive alignment under GenAI (Education Sciences, 2026)** — user-retrieved, in library. https://doi.org/10.3390/educsci16091507
- ✅ **GenAI in higher education — systematic review of empirical uses, outcomes, risks (Computers and Education: AI, 2026)** — user-retrieved, in library. https://www.sciencedirect.com/science/article/pii/S2666374026000130
