# DDCT New Curriculum — Ideas, Options and Alternatives (v2)

*A response to the GLM analysis of sample curricula and papers · prepared by Claude for Varunyu (DDCT, KMUTT) · v2, 2026-10-30 · working draft for discussion*

**What changed from v1.** v2 follows a faculty discussion and is deliberately leaner and more frank. It narrows the core to real-time 3D and animation, with breadth delivered through projects. It replaces the four-year maker thread with physical computing plus outsourced fabrication. It moves humanities into DDCT's own versions of general-education (GE) courses. It drops cybersecurity as a curriculum component. It delivers breadth through project "clinics" taught by guest experts. It cuts partnerships to fewer, deeper ones and explains shared blocks. It adds a staffing model for permanent and guest lecturers and a "what to drop" exercise. [1]

## 0. How to read this document

**Basis.** I read GLM's briefs 01–05, the recommendation briefs 06 and 07, SESSION-HANDOFF, the IPSJ question list, the three READMEs (curriculum, industry-partnerships, program-support), the nine paper digests and the Teaching-AI digest. I also checked one headline number against its source paper (section 2.3). I did not read the raw web snapshots, the full paper texts (apart from that one), the HTML summary cards, the visual guides, MANIFEST.html or AGENT-HANDOFF.md. [2]

**Labels.** **[Package]** marks a point that comes from GLM's files. **[Outside]** marks a point from general learning-science or education knowledge that is not in the package. **[My view]** marks my own judgment. **[Hypothesis]** marks something to test before it drives decisions. I have tried to say plainly where I disagree, including with the faculty's own ideas. [3]

## 1. Summary

1. **Subtract before adding.** Every idea on the table adds content. The most common failure of curriculum redesigns is adding without removing, so the faculty meeting should start with what the program will stop teaching (section 13). [4]
2. **A narrow, deep core and breadth through projects.** Teach real-time 3D and animation explicitly and deeply. Let application domains (heritage, products, health, installations, networking, security) arrive through projects, supported by short clinics. [5]
3. **Protect judgment skills, not every skill.** Classify skills into three tiers (judgment, literacy, delegate), and put live checkpoints only on judgment skills. Retopology, UV unwrapping and similar skills become literacy: understand, diagnose and fix, not master. [6]
4. **Design differently by craft.** Art-leaning (DD) students tend to be skeptical of AI in their own craft; tech-leaning (CT) students tend to take shortcuts. Both tend to shortcut the other's craft. Mixed studios let each group guard its own craft. [7]
5. **Physical computing over fabrication.** Microcontroller and sensor work gives honest physical feedback at low maintenance cost and naturally carries networking and IoT security. Outsource or borrow 3D printing and fabrication. [8]
6. **Humanities through DDCT's own GE versions**, negotiated with the university, so meaning and critique gain a home without adding credits. [9]
7. **Fewer, deeper partnerships.** Two or three partnerships with named people and recurring activities, plus shared blocks with other universities to give small cohorts teams and peers. [10]
8. **Use guest experts for depth, permanent faculty for continuity.** Guests teach clinics, studios and special topics; permanent faculty own the core, the checkpoints and the culture. [11]
9. **Culture outweighs structure.** No checkpoint system works unless the faculty agree to hold students to a common standard. [12]

## 2. The GLM package: what to keep and what to adjust

### 2.1 What it does well

**[Package]** The package covers the AI-in-education evidence (83 papers across nine branches), a world scan of programs, six partnership models and a support layer for small cohorts. It supplies an AI-policy grammar (three zones, mapped to the published AI Assessment Scale), a four-pillar assessment kit with vivas, and an architecture (06 §2: one program, two passports). These remain useful foundations. [13]

### 2.2 The diagnosis needs both student profiles

**[My view]** GLM designs around "AI-skeptical students". The faculty's experience is that DDCT has both kinds: art-leaning students tend to be skeptical, tech-leaning students tend to take shortcuts. Skeptics need agency (a legitimate AI-free route, co-authored policy, AI as an object of critique). Shortcut-takers need friction (unaided work before AI, grade weights that reward craft) and visible consequences (vivas, failed builds, missed performance budgets, live demos). GLM's design mostly addresses the first group. Section 4 develops this. [14]

### 2.3 Evidence strength, and numbers worth tightening

**[Package, partly checked]** Most of the evidence comes from writing and computer-science courses, usually with small samples and often self-report. GLM's digests say there is no experimental evidence yet for generative image, video or 3D pipelines in art schools. The curriculum should therefore be treated as a hypothesis and measured with delayed unaided tests, not satisfaction surveys. [15]

| Item in the package | What I found | Action |
|---|---|---|
| Brief 06 §1: chatbot arm had the worst self-efficacy, "η²p=.285" | Checked against the source ANCOVA table: .285 is the effect of condition on **design performance** (F(2,95)=18.94). The effect on **self-efficacy** is η²p=.122 (F(2,95)=6.58, p=.002). The chatbot arm was still lower than both fully integrated AI (diff 5.31, p=.009) and traditional teaching (diff 5.50, p=.006); fully integrated AI vs traditional did not differ (p=1.0). | Correct brief 06 before presenting. |
| Lehigh AI-literacy course: attribution d=+2.40 | Self-reported, single cohort (n=26), no control. | Cite as a blueprint, not an effect size. |
| Skill-formation RCT: AI access cut learning 17% (d=0.738, n=52) | Strong direct evidence, but written by Anthropic researchers. | Use it, and say who wrote it. |
| Klapproth retention figures (57.5% vs 68.5%) | Secondary citation inside a framework paper. | Check the primary source before quoting. |
| MIT "cognitive debt"; Gerlich offloading | Preprint and correlational; Wang 2026 finds no direct harm after mediators. | Use "brain first, AI second" as a design principle, not as proven causal. |
| Brief 06 links | About 80 relative links point at local PDFs and web snapshots. | They will not resolve in the repo copy. |

[16]

## 3. Design principles for v2

**[My view]** Five principles shape the rest of this document. First, **depth before breadth**: a small program earns credibility through depth in one area, here real-time 3D and animation, which is also where DigiPen's credibility lies. Second, **protect judgment, delegate the rest**: the skills worth protecting are those that let a graduate judge and direct work. Third, **subtract before adding**: every addition needs a matching removal. Fourth, **structure follows staffing**: anything that needs a technician, a specialist or ongoing maintenance must name who does it before it starts. Fifth, **culture over structure**: studio hours, critique norms and consistent standards matter more than any policy document. [17]

## 4. Student profiles: the craft decides, not only the student

**[My view]** Students tend to be skeptical about AI in their own craft and willing to shortcut other people's. An art student who refuses AI images may let AI write their Python or solve their math. A tech student who leans on AI for code may accept AI-generated art without noticing what is wrong with it, because they lack a trained eye. If this holds, "DD equals skeptic, CT equals shortcut-taker" is only half the picture. **[Hypothesis]** It should be checked with a per-student survey early in the term, asking why students use or avoid AI, together with a short unaided task to compare what they say with what they can do. [18]

| Student and domain | Main risk | Design response |
|---|---|---|
| DD in art craft | Disengagement if AI is forced | Agency: AI-free route allowed, co-authored policy, critique of AI output |
| DD in math, code and writing | Quiet shortcuts in the subjects they find hardest | Friction: the same checkpoints and vivas as everyone, framed as protecting them |
| CT in code and systems | Delegating and not learning | Friction plus measurable consequences: from-scratch tasks, explain-your-code, performance budgets, live debugging |
| CT in art and visual judgment | Accepting poor AI art uncritically | Build taste: critique practice, art-direction feedback from DD peers |

[19]

**[My view]** Mixed DD+CT studios turn this into a strength. When a CT student brings AI-generated art, the DD art director critiques it. When a DD student brings AI-written code, the CT tech director asks them to explain it. Each group's instinct becomes a quality gate for the other, and each has a respected role. These are tendencies, not types, and the exceptions often matter most. [20]

## 5. Checkpoints that stay light but useful

### 5.1 Three tiers of skill

**[My view]** Not every skill deserves a checkpoint. Classify each skill in the core into one of three tiers, and put live checkpoints only on the first. [21]

| Tier | Definition | Examples | What students must show | Checkpoint |
|---|---|---|---|---|
| **Judgment** | Skills a graduate needs in order to judge, direct and fix work | Drawing and observation, form, motion principles, math for CG, programming fundamentals, debugging, reading code, composition | Do it unaided, live | Short live checkpoint that unlocks AI for that skill |
| **Literacy** | Skills a graduate must understand well enough to diagnose and fix, but need not master | Retopology, UV unwrapping, rigging setup, LOD generation, boilerplate code, render settings | Explain the principle; diagnose a bad example (often an AI output); fix one case | Diagnose-and-fix task inside an existing assignment, no separate exam |
| **Delegate** | Skills that tools will do; knowing they exist is enough | Batch conversions, routine file and format work, simple asset variations | Use the tool appropriately and check the result | None |

[22]

**[My view]** The literacy tier matches the faculty's view on retopology and UV unwrapping. Students learn what the skill is, why it matters and how to solve it in principle, so they can use and correct the tools, but they do not spend weeks producing it by hand. A good literacy task is: "here is an AI-generated model; find the topology and UV problems, explain why each matters for deformation or texturing, and fix the worst one." [23]

### 5.2 Rules that keep checkpoints from becoming bureaucracy

**[My view]** Seven rules keep the system light. Each course has at most two or three checkpoints. A checkpoint takes under 30 minutes and is embedded in an assignment that already exists. Results are pass or not-yet, with retakes. The instructor or teaching assistant marks it with a one-page rubric. Every checkpoint must change a decision (it unlocks something or triggers support); if it changes nothing, cut it. Guest lecturers get a template and use the same rules. The faculty review the list once a year and delete checkpoints that no longer earn their place. [24]

### 5.3 What each stakeholder gets

| Stakeholder | What they need | What the checkpoint system gives |
|---|---|---|
| Students | Clear, fair rules and a path forward | Know exactly what unlocks AI; retakes; no hidden penalty |
| Permanent faculty | Low workload | Few checkpoints, embedded in existing work, one-page rubrics |
| Guest lecturers | A simple frame to follow | A template and the same tiers |
| Program and quality assurance | Evidence that learning outcomes are met | Pass records per skill double as outcome evidence |
| Employers and partners | Confidence that graduates can actually do the work | Verified judgment skills alongside the portfolio |

[25]

## 6. Scope: a narrow, deep core with breadth through projects

**[My view]** "Digital experience" is too broad for a program of this size, and Silpakorn already uses the name. The core should be real-time 3D and animation: modeling and materials, motion and animation principles, rigging and animation basics, engine work and scripting, math for CG, visual design and drawing, and game design fundamentals. DD students go deeper on the art side and CT students on the engineering side, sharing the same foundations. [26]

**Is this "learning by doing"?** Partly. Breadth through projects is learning by doing, but the core should not be. **[Outside]** Research on minimally guided learning, summarised by Kirschner, Sweller and Clark (2006), finds that novices learn less from pure discovery than from explicit instruction with guided practice. Students learn what a project forces them to learn and avoid what is hard. So the split should be: **the core is taught explicitly, with deliberate practice and checkpoints; breadth is applied through projects, with just-in-time support (section 9).** [27]

**[My view]** Breadth then comes from application domains, not new skill sets: heritage and museum experiences, product visualisation, health and training simulations, installations, multiplayer and networked play, physical controllers. A student can go deep in real-time 3D and still graduate with a portfolio that reaches well beyond games. [28]

## 7. Making: physical computing first, fabrication on demand

**[My view]** A full fabrication lab needs equipment, maintenance, safety oversight and a technician; without a technician it decays. Physical computing is a better first investment. Microcontroller kits (Arduino or ESP32-class boards) and sensors are cheap, can be issued per student or per team, and need little maintenance beyond consumables. [29]

**[My view]** Physical computing also solves two other problems. It carries networking naturally, since Wi-Fi boards talking to a game engine teach protocols, latency and client-server design in context. It carries security naturally too, since connected devices invite discussion of authentication, exposure and safe defaults. Typical projects include custom game controllers, interactive installations, kinetic or animatronic props, and sensors that drive real-time 3D scenes. A Year 3 block or elective, taught by a guest from the maker community or KMUTT's engineering side, is a realistic start. [30]

**[My view]** For 3D printing and fabrication, use KMUTT facilities or print services when a project needs them, and keep one small "print-fail clinic" inside a modeling course: students print a model (including AI-generated meshes), diagnose why it fails, and fix it. **[Hypothesis]** This makes topology and geometry quality concrete; measure print success rates over the term. Expand to an in-house lab only if demand is proven and a technician is funded. [31]

## 8. Humanities through DDCT's own GE versions

**[My view]** Using DDCT-specific versions of KMUTT's general-education courses is a strong idea: it gives humanities and social science a home without adding credits, which removes the biggest structural objection. The courses must still meet the university's GE learning outcomes and any national standard, so check those during negotiation. [32]

| GE area (to be matched to KMUTT outcomes) | Possible DDCT version | Focus |
|---|---|---|
| Social sciences | Play and Society | How games and media shape culture and behaviour; playtesting as light ethnography |
| Humanities and culture | Thai Culture in Interactive Media | Folklore, heritage and soft power in games and animation (a gap no program in GLM's scan fills) |
| Law, ethics, citizenship | Ethics, IP and Law for Creators | Copyright, AI-generated content, disclosure, contracts, labour |
| Communication | Pitching and Presenting Creative Work | Pitch with live Q&A, critique writing, presenting to international audiences |
| Digital and AI literacy | Thinking with AI | How generative models work, verifying output, documenting AI use |

[33]

**[My view]** Two frank cautions. First, these courses succeed or fail on the teacher. A weak version will confirm students' suspicion that humanities are filler, so it is better to delay a course than to run it without the right person. Guest scholars and practitioners can teach them under DDCT policy. Second, consider opening some of them to other KMUTT students. Mixing with other disciplines is valuable, and it also markets the program. [34]

## 9. Breadth through projects, done properly

**[My view]** The current model, where students work mostly alone in project courses with advisers as checkpoints, has two weaknesses. Breadth depends on what each adviser happens to know, and solo work teaches little about teams or project management. Five changes make project-based breadth reliable without adding many courses. [35]

**1. Just-in-time clinics.** Keep a menu of short modules (roughly 3–6 hours each) taught by guest experts: multiplayer networking, performance profiling, shaders, physical computing, IoT security basics, data and cloud deployment, pitching. Run a clinic when enough current projects need it, for example when three or more projects need multiplayer. [36]

**2. Competency cards.** Each clinic comes with a one-page checklist of what a project must demonstrate (for networking: a working client-server build, handling of lag or disconnects, a short explanation of the design). The adviser checks the card at a milestone. This keeps breadth verifiable without exams. [37]

**3. Technical reviews at milestones.** At key milestones, a guest reviewer runs an industry-style design review covering architecture, performance and security. Students defend their decisions, which doubles as an oral defence. [38]

**4. A flexible course shell.** A variable-topic "Special Topics" course lets the program add lecture series each term to match what projects need, without a curriculum revision. This is GLM's "slow layer, fast layer" idea in practice. [39]

**5. At least one team project per year.** Mixed DD+CT teams with rotating producer and tech-director roles. Project management is learned by doing it, getting it wrong and reflecting, not in a lecture. [40]

| Topic | Decision | How it is delivered |
|---|---|---|
| Optimization | **Core** | Taught in the core; a performance budget is required in every real-time project |
| Pitching and presenting | **Core** | DDCT GE course plus a pitch with Q&A at milestones |
| Networking | Project-driven | Clinic plus competency card; arises in multiplayer and physical-computing projects |
| Security | Literacy only | One AI-and-data-hygiene session for all; IoT and game-security clinic when projects need it; not a curriculum component |
| Project and team management | Learned by doing | Rotating roles in team projects, retrospectives |
| Business basics | Optional | Clinic for students heading to freelance or self-publishing |

[41]

## 10. Partnerships: fewer and deeper

**[My view]** Partnerships cost faculty time to maintain, and many university agreements become dead paper. Two or three real partnerships, each with a named person on both sides and a recurring activity, are worth more than ten agreements. Likely candidates are DigiPen (keep and deepen; GLM's list of what to request still applies), one or two Thai studios that need juniors, and one or two universities for shared blocks. [42]

**[My view]** Be realistic about AI companies. They want users, data and visibility far more than they want to shape education. Their free education programs are worth joining for access, but curriculum should not be built around tools that change every six months. Any agreement should include academic freedom (students may critique the partner's tools), terms for student work (not used for training without consent), no exclusivity, and an exit. [43]

### 10.1 What a shared block is

**[My view]** A shared block is a short, intensive unit, typically two to four weeks, that two or more universities run together. Students from each institution enrol through a course at their own university, work in mixed teams on a common brief, and are taught by lecturers contributed by each partner. Each university grades its own students against a rubric agreed in advance. **[Package]** GLM's model is DADIU in Denmark, where students from several universities combine into production teams; GLM's idea C suggests DDCT do this with Silpakorn ICT, CMU CAMT and Walailak. [44]

| Element | How it works |
|---|---|
| Credit | Each university maps the block onto an existing course shell (a special-topics or studio course), so no new approval is needed |
| Timing | A window that fits all calendars, often between terms or in summer |
| Location | Rotating host, or online preparation plus an on-site intensive week |
| Teaching | Each partner contributes one lecturer; guest experts can join |
| Brief | One shared brief, ideally from a real client or industry partner |
| Assessment | A common rubric; each university grades its own students |

[45]

**[My view]** For DDCT the benefits are concrete: CT's small cohort gets enough people for real teams, students meet peers with different skills, faculty share teaching load, and a national network forms at low cost. The challenges are calendar alignment, travel cost, credit mapping and language (DDCT teaches in English, partners may teach in Thai). An online or hybrid version with DigiPen Singapore or another international partner is a possible variant. [46]

## 11. Teaching staff model: permanent and guest

**[My view]** Guest and invited lecturers make much of this feasible, but they suit some jobs better than others. Guests are strong at depth and currency: clinics, special topics, technical reviews, industry briefs, DDCT GE courses with the right scholar, and co-teaching studios. They are weaker at continuity: owning a core course over years, running checkpoints consistently, advising, and carrying program culture. [47]

| Role | Best held by | Why |
|---|---|---|
| Core courses and checkpoints | Permanent faculty | Consistency across years; standards |
| Advising and culture | Permanent faculty | Relationships and continuity |
| Clinics and special topics | Guests | Current expertise; flexible timing |
| Technical reviews and juries | Guests and industry | Credibility; industry standards |
| Co-taught studios | Permanent faculty plus a guest | Combines continuity and expertise |
| DDCT GE courses | Guest scholars or practitioners, under DDCT policy | Brings expertise the core faculty may lack |

[48]

**[My view]** Two practical points. A short onboarding pack for guests (the AI policy, the skill tiers, the checkpoint template, the assessment rubric) keeps independent classes aligned. Pairing each guest with a permanent faculty contact avoids classes drifting away from program standards. [49]

## 12. Putting it together

| Thread | Year 1 | Year 2 | Year 3 | Year 4 |
|---|---|---|---|---|
| **Core craft** (judgment-tier checkpoints) | Drawing, form, math for CG, programming | Modeling, animation, engine work; literacy tasks (retopology, UVs); AI-first rebuild studio | Specialisation; AI control techniques; optimization budgets | Mastery viva |
| **Studies** (DDCT GE versions) | Thinking with AI; Play and Society | Ethics, IP and Law for Creators | Thai Culture in Interactive Media | Published critique or postmortem |
| **Making** | Hand prototypes inside studios | Print-fail clinic (via services) | Physical-computing block or elective | Optional physical component in capstone |
| **Breadth** (project-driven) | — | First team project; clinics as needed | Clinics and competency cards; shared block | Technical reviews in capstone |
| **Practice** | Team basics; first public show | Rotating roles; pitch with Q&A | Real client brief | Industry-mentored capstone and expo |

[50]

## 13. What to drop

**[My view]** Before agreeing any addition, ask each course owner to answer four questions. Which topics in this course are now delegate-tier and can be cut to a short demonstration? Which production skills can move from mastery to literacy? Which assignments test output that AI can now produce, and should become diagnose-and-fix or viva tasks? Which electives have low enrolment and could become clinics? The time recovered is what pays for physical computing, clinics and team projects. [51]

## 14. First 12 months: low-cost pilots

| Pilot | Where | Cost | Evidence to collect | Go / no-go signal |
|---|---|---|---|---|
| Per-student AI-use and attitude survey, plus student-authored AI policy | Start of next term | Very low | Which profile dominates in which domain | Informs everything else |
| Skill-tier classification of the core | Faculty workshop | Low | A tier for each core skill | Agreement across course owners |
| Checkpoints in one or two foundation courses | Math for CG; drawing or programming | Low | Pass rates; delayed unaided retest at 6–8 weeks | Retest results hold or improve |
| Literacy-tier diagnose-and-fix task | A modeling course | Low | Diagnosis quality | Students can explain and fix common faults |
| One just-in-time clinic with a competency card | A project course | Low (one guest) | Card completion; project quality | Advisers find it useful; students apply it |
| Physical-computing mini-block | Year 3 elective or project course | Low to medium (kits) | Projects completed; networking and security learned | Demand and outcomes justify a full block |
| GE negotiation | University level | Time | Which GE slots DDCT may run | At least one DDCT GE version approved |
| One shared-block conversation | One Thai partner university | Time | Calendar and credit fit | A joint pilot agreed |

[52]

## 15. Risks and open questions

**Risks.** Faculty workload remains the main constraint. Guest lecturers can drift from program standards without onboarding. DigiPen credit structures may limit changes. GE negotiation may be slow or restrictive. Shared blocks depend on calendars and money. The evidence for 3D and animation specifically is thin. Policy alone will not change student work habits: culture does. [53]

**Open questions.** How much flexibility does the DigiPen agreement leave? Which GE slots can DDCT run, and under what outcome requirements? Which KMUTT facilities (fabrication, electronics) can DDCT students use? Do DD and CT share first-year courses? What is the budget for guests, kits and clinics? Which partner universities are realistic for a first shared block? [54]

## 16. Decisions to put to the faculty meeting

1. Narrow the core to real-time 3D and animation, with breadth through projects. [55]
2. Run the "what to drop" exercise in every core course before adding anything. [56]
3. Adopt the three skill tiers and the checkpoint rules, and pilot checkpoints in one or two foundation courses. [57]
4. Start physical computing as a Year 3 pilot; use services for fabrication. [58]
5. Open GE negotiations with the university for DDCT versions. [59]
6. Adopt clinics, competency cards and a Special Topics shell for project-driven breadth; drop cybersecurity as a curriculum component. [60]
7. Choose two or three partnerships to deepen, and open one shared-block conversation. [61]
8. Agree a guest-lecturer onboarding pack and a faculty contact for each guest. [62]

## Appendix A. Evidence register

Strength is my rough rating from the package's own descriptions. "Checked" means I verified the figure against the primary paper text. [63]

| Claim | Where in the package | Strength | Caveat |
|---|---|---|---|
| Guided AI beats raw AI | Digest 1 (Yang 2025, n=153); digest 4 (Li & Chen 2026, n=100, **checked**) | Moderate | Small samples; different disciplines |
| AI access reduced skill formation by 17% unless used for inquiry | Digest 2 (Shen & Tamkin 2026, n=52) | Moderate | Authored by Anthropic researchers; one task type |
| Permissive homework is safe with AI-free checks and oral defence | Digest 1 (Kosar 2024, n=182) | Moderate | One CS course |
| Guardrailed tutor: 88% accuracy vs 48% | Digest 2 (CS50) | Moderate | Accuracy, not learning outcome |
| Bias-corrected pooled effect about 0.32 (raw 0.804) | Digest 1 (Chen & Cheung 2025) | Moderate | Heterogeneous studies |
| Embedded ethics preferred over a separate module | Digest 6 (Zhejiang, n=70) | Weak | Preference, not outcomes |
| Per-stage AI gating: 20.90 vs 18.65 vs 16.13 | Digest 4 (Song & Xu 2026) | Moderate | Gating by stage, not by skill |
| AI detectors 61–69% accurate | Digest 8 | Moderate | Text only |
| Unaided-first then AI-later preserves recall | Digest 8 (MIT preprint) | Weak | Preprint, small crossover group |
| Lehigh AI-literacy course gains | Digest 3 | Weak | Self-report, single cohort |
| Minimal guidance is less effective for novices | Outside the package (Kirschner, Sweller & Clark 2006) | Moderate | General learning science, not AI-specific |

## Appendix B. The GLM-analysis folder

The `GLM-analysis` folder holds GLM's analysis documents only: briefs 01–07, SESSION-HANDOFF, the IPSJ question list, the visual guides, the READMEs, the Teaching-AI digest, and the paper index, manifest, digests and summary cards. It excludes raw web-page snapshots, downloaded PDFs and full paper texts, which are large and may carry third-party copyright, so relative links to those files will not resolve. [64]
