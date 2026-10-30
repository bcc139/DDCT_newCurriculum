# DDCT New Curriculum — Ideas, Options and Alternatives

*A response to the GLM analysis of sample curricula and papers · prepared by Claude for Varunyu (DDCT, KMUTT) · 2026-10-30 · working draft for discussion*

## 0. How to read this document

**Basis.** I read GLM's briefs 01–05, the two recommendation briefs (06 and 07, converted to text), SESSION-HANDOFF, the IPSJ author-meeting question list, the three READMEs (curriculum, industry-partnerships, program-support), all nine paper digests, and the Teaching-AI digest. I also checked one headline number against the source paper (section 2.3). I did not read the raw web-page snapshots, the full paper texts (apart from that one), the HTML summary cards, the three visual guides, MANIFEST.html or AGENT-HANDOFF.md. Everything I attribute to "the package" is therefore GLM's reading of its sources, not my independent check. [1]

**Labels.** I use three labels. **[Package]** means the point comes from GLM's files. **[My view]** means my own judgment. **[Hypothesis]** means a guess that should be tested or validated by interviews before it drives decisions. Your six ideas are mostly outside what GLM analysed, so a large share of sections 3.2–3.6 is [My view] or [Hypothesis]. [2]

## 1. Summary

1. **Keep GLM's AI-pedagogy core**: aligned (tutor-like) AI over raw access, unaided work first, process-plus-oral-defence assessment, and a local-model lab. It is the best-evidenced part of the package. [3]
2. **Change how AI is unlocked**: from "AI-off in Year 1" to a skill-by-skill unlock, where a short live unaided checkpoint opens AI for that skill. This targets your real problem (students taking quick routes) better than a calendar rule does. [4]
3. **Position the program as "digital experience"**: real-time, spatial and physical interactive experiences built with production-level craft. Organise it as three project-based studio lines (Play, Motion and Story, Space and Object) without changing the DD and CT degree names yet. [5]
4. **Make "digital to physical" a yearly thread**: hand prototypes, 3D printing and casting, physical computing, and a produced edition in Year 4. Physical failure is feedback a student cannot talk their way around. [6]
5. **Treat humanities as the reason the product is good**, not only a counterweight to AI. Embed critics and scholars in studios, keep one named course per year, and use games-as-arguments projects to make it fun. [7]
6. **Teach optimization, networking, security and soft skills through shipped projects**, not stand-alone courses. Optimization has the strongest tie to craft. Pitching doubles as an oral defence. [8]
7. **Build partnerships in tiers and name what each partner gets**, extend beyond games and animation (including AI companies), and protect academic freedom so students can critique partners' tools. [9]

## 2. The GLM package: what to keep and what to adjust

### 2.1 What it does well

**[Package]** The package covers four things thoroughly: the AI-in-education evidence (83 papers across nine branches), a world scan of programs, six models of industry partnership, and a support layer for small cohorts (07). It also supplies a usable AI-policy grammar (three zones, mapped to the published AI Assessment Scale), a four-pillar assessment kit with vivas, and a concrete architecture (06 §2: one program, two passports). I would present these largely as they are. [10]

### 2.2 The diagnosis may be pointing at the wrong students

**[My view]** GLM's design is built around "AI-skeptical students" whose resistance protects their identity (SESSION-HANDOFF; concern A8). Your project brief describes the opposite problem: comfortable students who lean toward easy and quick solutions. The two groups need different designs. Skeptics need agency and a legitimate AI-free space. Shortcut-takers need friction, visible consequences and public stakes. The three-zone policy handles both, but the motivational design differs, and most of GLM's persuasion tools (co-authored policy, honouring "creative sovereignty") address the first group. [11]

**[My view]** A short anonymous survey of what your students actually do with AI, and how they feel about it, would settle which problem dominates. The DiGRA game-jam survey in folder 5 (19 questions) is a reusable starting instrument. Both profiles probably exist in one cohort, so the survey should split the cohort, not average it. [12]

### 2.3 Evidence strength, and numbers worth tightening

**[Package, partly checked]** Most of the evidence comes from writing and computer-science courses, usually with small samples and often self-report. GLM's own digests say there is no experimental evidence yet for generative image, video or 3D pipelines in art schools. So the sensible stance is to treat the new curriculum as a hypothesis and instrument it, with delayed unaided tests rather than satisfaction surveys. [13]

| Item in the package | What I found | Action |
|---|---|---|
| Brief 06 §1: chatbot arm had the worst self-efficacy, "η²p=.285" | I checked the source paper's ANCOVA table. .285 is the effect of teaching condition on **design performance** (F(2,95)=18.94). The effect on **self-efficacy** is η²p=.122 (F(2,95)=6.58, p=.002). The chatbot arm was still significantly lower than both the fully integrated AI arm (diff 5.31, p=.009) and traditional teaching (diff 5.50, p=.006). Fully integrated AI vs traditional was no different on self-efficacy (p=1.0). | Correct the figure in brief 06 before presenting. |
| Lehigh AI-literacy course: attribution d=+2.40 | Self-reported, single cohort (n=26), no control. | Cite as a course blueprint, not as an effect benchmark. |
| Anthropic skill-formation RCT: AI access cut learning 17% (d=0.738, n=52) | Strong direct evidence for protecting foundations, but written by Anthropic researchers. | Use it, and say who wrote it. |
| Klapproth retention figures (57.5% vs 68.5%) | Secondary citation inside a framework paper. | Check the primary source before quoting. |
| MIT "cognitive debt" and Gerlich offloading | Preprint and correlational respectively; Wang 2026 finds no direct harm after mediators. | Adopt "brain first, AI second" as a design principle, not as proven causal. |
| Brief 06 links | About 80 relative links point at local PDFs and web snapshots. | They will not work in the repo copy; see the GLM-analysis README. |

[14]

### 2.4 Where the package is thin against your six ideas

**[My view]** Maker work, security, networking, optimization and soft skills have almost no coverage; the only relevant item is a Thai lecturer's classroom case (sketch to AI 3D model to 3D print). Humanities are covered well (04), but framed as a brake on AI. The scope question ("digital experience") is raised in the world scan (NYU IMA, RCA, Aalto, Silpakorn aiDEX) and in 06 §1, but the architecture that follows is still organised around DD and CT as game and animation degrees. Partnerships are mapped mostly to games, animation and AI vendors. [15]

## 3. Your six ideas, one by one

### 3.1 Learn better with AI without being de-skilled

**[Package]** The evidence converges on four design rules. First, aligned AI helps and raw access is neutral to harmful: the CS50 tutor reached 88% curricular accuracy against 48% for a generic chatbot, while a quasi-experiment found the ad-hoc chatbot arm worse than traditional teaching on self-efficacy. Second, sequence matters: unaided first, AI second, and close every AI phase with unaided work. Third, grade process and judgment: a Maribor course (n=182) saw no outcome differences when it combined AI-resistant tasks, AI-free in-lab extensions and oral defence. Fourth, detection software is not a defence (reported accuracy 61–69%), so redesign assessment instead. [16]

**[My view]** I would keep all four, and change one mechanism. GLM keeps Year 1 AI-off. For students inclined to shortcuts, a calendar rule invites waiting it out. A better lever is a **skill-by-skill unlock ledger**: each foundational skill has a short, live, unaided checkpoint, and passing it unlocks AI for that skill in later briefs. Some examples: [17]

| Skill | Unaided checkpoint (short, live, repeatable) | What it unlocks |
|---|---|---|
| 2D/3D transforms (Math for CG) | Derive and apply a rotation or change of axes by hand, then code it | AI for debugging and generating variants |
| Observational drawing | 20-minute timed drawing in class | AI for mood and reference exploration (not final art) |
| Modeling | Block out and clean up a simple prop in two hours | AI-assisted concepting and texturing |
| Programming | Implement a small algorithm from scratch | AI for scaffolding and refactoring |
| Animation | Pose-to-pose cycle without motion assist | AI motion assist and cleanup |

**[My view]** Checkpoints should be pass / not-yet, retakeable, and framed as "you are cleared to use this tool", not as a penalty. A student who is not yet cleared keeps working in the AI-free zone with tutor support. The risks are stigma, administrative load and gaming; small cohorts make it feasible, and the ledger can stay private to the student and adviser. This is untested. GLM's closest evidence is the per-stage gating sheet (achievement 20.90 vs 18.65 for AI-only vs 16.13 traditional), which gates by design stage, not by skill. [18]

**[My view]** Three supporting practices fit this. The first is an **AI-first, rebuild-by-hand** studio in Year 2: students receive an AI-generated asset or scene and must evaluate, repair and rebuild it, which trains judgment once basics exist. The second is **grade weighting that prices unaided craft above AI polish**: the UC Davis pattern (80% unaided draft, 10% AI revision, 10% reflection) is a template. The third is an **attempt-first "studio duck" tutor** over DDCT course content (the CS50 pattern), so help-seeking does not default to a generic chatbot. [19]

**[Package]** The Teaching-AI syllabi add useful details to borrow: tools withheld until the second half of a course while critical literacy comes first (UCF "Art of AI"), students drawing their anticipated and actual workflow and discussing the gap (BAU Barcelona), pre-AI work then a graded validation log (SFSU), students writing the course AI policy (Hamline), and screening previous students' work every session. [20]

**[My view]** Policy cannot carry the whole load for shortcut-seeking students. Their problem is partly motivational, so the curriculum should make effort visible and rewarded: public shows, live demos, physical artefacts, and peer-visible progress on hard practice. That is one reason the maker thread (3.3) matters for your first idea as well as your third. [21]

### 3.2 Scope: "digital experience" rather than 3D CG and game development

**[My view]** I would adopt the broader frame, with a spine so that it does not become a grab-bag. A working definition: *interactive, real-time, spatial or physical experiences that are designed and engineered with production-level craft.* That covers games, animation, XR, installations, interactive products, simulations and generative media. **[Package]** GLM's 06 reaches a similar conclusion (nobody owns the junction between game-first programs such as DigiPen, Georgia Tech and U-tad, and experience-first programs such as NYU IMA, RCA IED and Aalto New Media). Silpakorn's new "AI for Digital Experience Technology" degree already uses the naming from the ICT and AI side, so DDCT's distinct claim can be craft, making and meaning. [22]

| Option | What changes | DigiPen / approvals | Risk | My take |
|---|---|---|---|---|
| A. Widen outcomes only | Keep DD and CT; add electives and briefs beyond games and animation | Low | Weak signal to the market | Minimum viable |
| B. Three studio lines inside the current degrees | **Play** (games), **Motion and Story** (animation, film), **Space and Object** (XR, installations, physical computing, fabrication). Lines are project communities, not tracks. | Low to medium | Needs enough students per line | **Recommended now** |
| C. Rename the program ("Digital Experience") | New identity and degree names | High | Approval cost, DigiPen alignment | Defer; revisit after two cohorts of B |

[23]

**[My view]** With about 50 DD and fewer than 10 CT students a year (06), the lines must stay informal, so that no cohort is split below a workable team size. The Parsons pathways model, where students route through pathways inside one studio system, is the precedent GLM cites. [24]

### 3.3 More concrete, real-world making

**[My view]** I strongly agree, and I would make "digital to physical" a thread that runs through all four years, not a single elective. [25]

| Year | Making brief (examples) | What it teaches |
|---|---|---|
| 1 | Hand and clay sculpt, paper engineering, cardboard prototype of a game or interface | Form, scale, iteration without a screen |
| 2 | **Print-fail clinic** (print an AI-generated or student mesh, diagnose, repair); laser-cut game components; mold and cast from own model | Watertight geometry, wall thickness, tolerance, topology |
| 3 | Microcontrollers and sensors: a custom controller, an interactive installation, an animatronic or kinetic prop | Hardware-software interaction, networking, power, fault finding |
| 4 | A **produced edition**: board game, art toy, installation or exhibition, with a small budget and a public show | Production, cost, packaging, audience |

[26]

**[My view]** Procedural modeling is a natural bridge. Geometry made with Houdini VEX or Blender Python has to be valid to print, which turns abstract mesh quality into an observable pass or fail. **[Package]** The Thai classroom case (sketch to AI 3D to print) is a good entry point, but I would make the failure the lesson: AI meshes often fail to print, and students must work out why and repair them. **[Hypothesis]** I expect this to push students back into topology fundamentals; that is untested and worth measuring (print success rate over time). [27]

**[My view]** Cheap extensions include tabletop games and card games (systems design without a screen, which also feeds section 3.4), stop-motion and puppet work for animation principles, and a physical-computing controller for any Year 3 game. Equipment can be staged in tiers. Tier 0 is a print service plus hand tools and borrowed equipment. Tier 1 adds a few desktop printers, access to a laser cutter and an electronics bench. Tier 2 adds resin printing, vacuum forming, CNC or mocap. Resin and laser work need ventilation and safety training. Before budgeting, find out what KMUTT's engineering and fabrication units already have. **[Package]** The 07 brief also suggests a Thai cultural asset archive (scans, textures, motifs), modelled on the RISD Nature Lab, which would double as making material. [28]

### 3.4 Social science and humanities for human touch and depth

**[Package]** GLM's 04 argues that RPI-style critical game design makes the degree about the questions AI cannot answer, and structures the idea as Brake (what AI should not do), Anchor (what it cannot do) and Engine (making AI useful). It lists strong course-level precedents (RPI seminars, Tampere's four perspectives, Uppsala, XJTLU's AI-and-society modules, UC Irvine's queer and feminist game studies, Michigan State's Indigenous game design) and a verified gap: no Thai or Southeast Asian games-studies course appears anywhere in its catalog. [29]

**[My view]** I would reframe it. The package sells the humanities as a counterweight to AI. Your framing is stronger: when anyone can produce a game, what makes a game good in detail, technically, aesthetically and intellectually, is meaning, audience and craft. Present it that way to faculty and students; it also avoids positioning the humanities against the students who like AI. [30]

| Option | Description | Evidence / precedent | Cost |
|---|---|---|---|
| A. Seminar spine | Named theory courses each year, RPI or Tampere style | Strong precedents at graduate level | Needs dedicated staff |
| B. Embedded co-teaching | A humanities or social-science scholar sits in studio critiques and co-designs briefs | Zhejiang architecture study (n=70): students preferred embedded ethics 65.7% to 28.6% for a separate module | Needs cross-faculty partnership |
| C. Hybrid | One named course per year plus embedded critics | Combines both | **Recommended** |

[31]

**[My view]** Ways to make it fun and concrete: a **Games as Arguments** studio where each team's game must make a claim, be playtested by outsiders and be defended before a jury; tabletop games about local issues (smog, flooding, platform work); design fiction; playtests run as light ethnography; published critiques and postmortems; and a "kill-criteria tribunal" where teams argue for cancelling a project. Thai-specific courses fill the gap noted above (Thai games and soft power, folklore and heritage in interactive media, a sociology of the Thai creative workforce). I would drop GLM's fixed 1:1 "balance rule" between AI-production and studies credits, since nothing in the evidence supports a particular ratio. Embedded assessment of arguments does more. [32]

**[Package]** GLM names two failure modes worth keeping: ethics-washing (grade defended arguments, not attendance) and critique-only programs that leave graduates unable to make things (USC's caution). Staffing is the practical issue: KMUTT is a technology university, so plan a partnership with liberal-arts or social-science units, joint appointments, and practitioner adjuncts. [33]

### 3.5 Learning outside the core: security, networking, optimization, soft skills

**[My view]** Your test, that each item needs a specific purpose for the student's future career, is the right one. I would teach all of them through shipped projects, not stand-alone courses, and rank them by how closely they tie to craft: [34]

| Topic | Career purpose | Craft link | Delivered as | Priority |
|---|---|---|---|---|
| **Optimization** | Performance is a hiring filter in real-time work; running models locally depends on it | Highest: frame-time budgets, profiling, level of detail, memory; also model quantization for the local-model lab | Year 2 sprint, then a budget requirement in every real-time project | 1 |
| **Networking** | Multiplayer, live services, IoT and installations | Medium | Year 2 basics, Year 3 multiplayer or physical-computing project | 2 |
| **Security** | Cheating and account abuse, IP leaks, safe use of AI tools with client data | Medium | Three-week "break each other's builds" block plus threat modelling; AI-use security (data leakage, prompt injection, NDA-safe local models, content provenance) at literacy level | 3 |
| **Team and project management** | Every studio and freelance path | High if roles are real | Rotating producer and tech-director roles in mixed DD+CT studios; retrospectives; scope cuts | embedded |
| **Pitching and presentation** | Funding, clients, hiring, international teams | High | A pitch with live Q&A at every milestone, which doubles as an oral defence (AI-resistant assessment) | embedded |
| **Client and business basics** | Freelance and self-funded creators | Medium | GLM's venture layer: pricing, contracts, publishing, income portfolio | embedded |

[35]

**[My view]** Breadth competes with craft time, which is the opposite of what the first idea needs. Two controls help. First, cap the total: offer a "second spine" that each student chooses (Systems, Production and Business, or Studies) on top of the shared core, so no one takes everything. Second, require every cross-discipline item to end in a shipped artifact with an oral defence. Cohort size also matters: CT's fewer than 10 students a year could make Systems the natural CT emphasis, while DD students need security and networking only at literacy level. **[Package]** GLM's idea A (every CT student runs a production cell staffed by DD students) is a good vehicle for the Practice items above. [36]

### 3.6 Partnerships beyond DigiPen

**[Package]** GLM identified six partnership models: curriculum embedding, ambassador or access programs, spinouts, co-location, company-run institutes, and industry-owned credentials. It suggests applying this semester to the free vendor programs (Meshy education plan, Tripo ambassador program, Runway educators, NVIDIA DLI teaching kits), adding Netflix×Geidai-style masterclasses and D&AD real briefs this year, and negotiating a Tencent×Tsinghua-style co-built module structurally. It also suggests reconsidering the DigiPen deal along the CUC axis (DigiPen blueprint, local delivery, dual credential), though accreditation locks may resist that. I agree with all of it. [37]

**[My view]** I would add four cautions and extensions. First, vendor programs are cheap but create lock-in and sit awkwardly with a critical-studies spine. Take the access, keep open-weight local models as the core, and write an **academic-freedom clause** into any agreement so students and faculty can critique a partner's tools. Second, agree terms for student work (not used for model training without consent), non-exclusivity and exit. Third, state what each partner receives, because partnerships last when both sides gain. Fourth, widen the sector list. [38]

| Partner type | What they might get | What DDCT asks | Entry offer |
|---|---|---|---|
| AI companies | **[Hypothesis]** Human evaluation and taste (judging model output), character and agent interaction design, 3D and synthetic data, student feedback on tools | Tool access, briefs, mentors, co-supervised capstones | Student ambassadors; a structured tool-evaluation sprint |
| Games and animation studios | Pipeline-ready juniors, prototypes | Briefs, masterclasses, internships | Real-brief studios; an industry day |
| Product, toy and maker firms | Concepts, short-run prototypes, designer-toy and edition ideas | Fabrication access, mentors | Joint "produced edition" briefs |
| Museums, heritage and tourism | Interactive and spatial content | Real clients, cultural material | Heritage XR or exhibition projects |
| Manufacturing, health and simulation | Visualization and digital twins | Real data, domain mentors | Applied capstones |
| Other universities | Shared blocks fill small cohorts | Cross-enrolment, joint teams | Three-week blocks with Silpakorn, CMU CAMT and Walailak (GLM idea C); exchange with DigiPen Singapore, CityU Hong Kong SCM, Aalto and Tokyo Geidai |

[39]

**[My view]** Three-week blocks suit exchange well, because a visiting student can join a complete unit. Your cohorts are small and international, which is an asset for joint studios across institutions. DigiPen remains the anchor, and GLM's list of things to request from it (the CS 394/594 course design, the BS in AI degree map, portfolio-policy language, the Singapore Attach-and-Train template) is worth pursuing in parallel. [40]

## 4. Putting it together

**[My view]** I would build on GLM's "one program, two passports" architecture (06 §2): DD and CT remain separate named degrees, but run as one vertical studio system with mixed teams. Your ideas add five threads that run across the four years: [41]

| Thread | Year 1 | Year 2 | Year 3 | Year 4 |
|---|---|---|---|---|
| **Craft** (AI unlocked by unaided checkpoints) | Drawing, form, math, programming | Modeling, animation, engine craft; AI-first rebuild studio | Specialisation; AI control techniques (LoRA, ControlNet-class, local models) | Mastery viva |
| **Make** | Hand, clay, paper, cardboard | 3D print, laser cut, casting; print-fail clinic | Microcontrollers, controllers, installations | Produced edition and exhibition |
| **Studies** | Play and culture seminar | Critics embedded in studios | Games as Arguments studio; playtest research | Published critique or postmortem |
| **Systems** | Programming, math | Profiling and optimization sprint; networking basics | Multiplayer or IoT; security block; local-model lab | Tech direction of a capstone |
| **Practice** | Team basics; first public show | Rotating roles; pitch with Q&A | Real client brief; project management | Industry-mentored capstone; expo |

[42]

**[My view]** DD would lean toward Craft, Make and Studies, and CT toward Systems, with both sharing Practice. The three AI zones from GLM then apply thread by thread: Year 1 Craft and Make stay mostly AI-free; Year 2 studios are AI-disclosed with the unlock ledger; Year 3 includes AI-required production routes and an AI-augmented option; Year 4 closes with a viva for every student. Every year ends with at least one public show. [43]

## 5. A first 12 months: low-cost pilots

**[My view]** GLM's own risk list (06 §7) says faculty load is the real constraint, so I would start with pilots inside existing courses and measure them, instead of launching a redesign. [44]

| Pilot | Where it fits | Cost | Evidence to collect | Go / no-go signal |
|---|---|---|---|---|
| Student AI-use and attitude survey, plus student-authored AI policy | Start of next term | Very low | Which student profile dominates | Informs everything else |
| Unlock ledger in one or two foundation courses | A math or programming course; drawing | Low | Checkpoint pass rate and time; a delayed unaided retest at 6–8 weeks | Retest scores hold or improve vs a comparison group |
| Print-fail clinic | A modeling course, with borrowed or serviced printing | Low | Print success rate over the term; quality of diagnosis reports | Success rate rises and reports show topology understanding |
| Embedded critic in one studio | A Year 2 or 3 studio | Low to medium | Student and faculty feedback; quality of critique writing | Students prefer it to a separate module |
| Optimization sprint | A real-time project | Low | Frame-time results against budget | Budgets met without AI-only fixes |
| Pitch-as-viva at milestones | Any studio | Very low | Defence scores; agreement with process logs | Reliable separation of understanding levels |
| Partner applications and one masterclass | Whole program | Very low | Access granted; partner interest | At least one partner agrees to a brief |

[45]

**[My view]** Track a small set of indicators from day one: unaided checkpoint pass rates, delayed retention scores, shipped public works per student, viva scores, print success rate, student AI-use and attitude changes, partner engagements, and, once graduates exist, role titles at 6 and 18 months. [46]

## 6. Risks and open questions

**Risks.** Faculty workload is the main one, since every idea costs staff time. Accreditation and DigiPen credit structures may limit changes to the core. Studio lines can fragment very small cohorts. Maker spaces carry cost and safety obligations. Humanities staffing depends on cross-faculty agreements. Vendor lock-in and conflicts of interest are possible. Skill gates can create stigma or admin burden. Breadth can crowd out craft. The evidence for 3D and animation specifically is thin. Finally, policy alone will not fix students' motivation for effortful practice. [47]

**Questions I could not answer from the files.** How much flexibility does the DigiPen agreement leave in credits and course content? What makerspace and fabrication facilities does KMUTT already have? Do DD and CT share first-year courses today? Which humanities or social-science units could partner? What is the budget range for equipment and for the two staff hires in 07? Are the student cohorts mostly shortcut-takers, skeptics, or both? [48]

## 7. Decisions to put to the faculty meeting

1. Adopt the frame: "digital experience" as the positioning, with studio lines (option B) now and renaming deferred. [49]
2. Approve the AI-use survey and the student-authored AI policy as first steps. [50]
3. Pilot the unlock ledger in one or two foundation courses, with a delayed unaided retest. [51]
4. Approve a "digital to physical" thread, with Tier 0 resources in year one and a facilities survey of KMUTT. [52]
5. Agree the embedded-critic model for humanities and begin conversations with partner units. [53]
6. Choose which Systems and Practice items become required, and which belong to the optional second spine. [54]
7. Authorise partnership applications and the academic-freedom and student-work terms for any agreement. [55]

## Appendix A. Evidence register

Strength is my rough rating of how far the evidence supports a decision, from the package's own descriptions. "Checked" means I verified the figure against the primary paper text. [56]

| Claim | Where in the package | Strength | Caveat |
|---|---|---|---|
| Guided AI beats raw AI | Digest 1 (Yang 2025, n=153); digest 4 (Li & Chen 2026, n=100, **checked**) | Moderate | Small samples; different disciplines |
| AI access reduced skill formation by 17% unless used for inquiry | Digest 2 (Shen & Tamkin 2026, n=52) | Moderate | Authored by Anthropic researchers; one task type |
| Permissive homework is safe with AI-free checks and oral defence | Digest 1 (Kosar 2024, n=182) | Moderate | CS course, one institution |
| Guardrailed tutor: 88% accuracy vs 48% | Digest 2 (CS50) | Moderate | Accuracy, not learning outcome |
| Bias-corrected pooled effect about 0.32 (raw 0.804) | Digest 1 (Chen & Cheung 2025) | Moderate | Meta-analysis of heterogeneous studies |
| Embedded ethics preferred over separate module | Digest 6 (Zhejiang, n=70) | Weak | Survey preference, not outcomes |
| Per-stage AI gating: 20.90 vs 18.65 vs 16.13 | Digest 4 (Song & Xu 2026, n=120 per arm) | Moderate | Gating by stage, not by skill |
| AI detectors 61–69% accurate | Digest 8 | Moderate | Text only; nothing on 3D or visual work |
| Unaided-first then AI-later preserves recall | Digest 8 (MIT preprint) | Weak | Preprint, small crossover group |
| Lehigh AI-literacy course gains | Digest 3 | Weak | Self-report, single cohort |

## Appendix B. Files in the GLM-analysis folder

The `GLM-analysis` folder holds GLM's analysis documents only: briefs 01–07, SESSION-HANDOFF, the IPSJ question list, the three visual guides, the three READMEs, the Teaching-AI digest, and the paper index, manifest, nine digests and nine summary cards. It excludes the raw web-page snapshots, the downloaded PDFs and the full paper texts, which are large and may carry third-party copyright. Relative links inside those documents that pointed at excluded files will not resolve. [57]
