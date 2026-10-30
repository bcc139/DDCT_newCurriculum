# Math for CG — Checkpoint Sheets and Rubric

*A worked implementation of the skill-tier checkpoints for a first-year Math for CG course · prepared by Claude for DDCT (KMUTT) · 2026-10-30 · draft for trial*

## 1. Purpose and how this pack is used

A checkpoint is a short, live, unaided task that shows a student can do a **judgment-tier** skill on their own. Passing it unlocks AI use for that skill in later work, with a duty to verify and log every AI result. The checkpoint tests judgment, not arithmetic speed: when a product is defined, which order to multiply in, what a result means geometrically, and how to tell when an answer is wrong. [1]

This pack contains a skill-tier map for the course (section 2), three checkpoints across the semester (section 3), the full transform checkpoint with two versions, answer keys and a rubric (sections 4–7), the not-yet path (section 8), what passing unlocks and the verification log (section 9), a delayed retest item (section 10), and instructor notes (section 11). [2]

## 2. Skill-tier map for the course

| Tier | Skills in this course | How it is assessed |
|---|---|---|
| **Judgment** (do it unaided) | Vector operations and the meaning of the dot product; matrix multiplication and composing transforms (order); homogeneous coordinates; linear interpolation; the half-plane (side-of-line) test | Live checkpoint; passing unlocks AI for that skill |
| **Literacy** (understand, diagnose, fix) | Solving linear systems by elimination; manipulating trig identities; 3D rotation about arbitrary axes; direction cosines; evaluating higher-order curves | Diagnose-and-fix tasks inside normal assignments |
| **Delegate** (use and check) | Large numeric computation; plotting graphs; simplifying long expressions; degree–radian conversion | A line in the process log; spot checks |

[3]

## 3. The three checkpoints at a glance

| Checkpoint | Suggested timing | Skill | Unlocks |
|---|---|---|---|
| **CP1 Vectors** | After the vectors unit (about week 3) | Dot product, angle, projection | AI for vector computation and debugging |
| **CP2 Transforms** (detailed below) | End of the transformations unit, before the midterm (about week 6) | Matrix multiplication, homogeneous coordinates, composition order | AI for matrix computation, transform chains, NumPy and engine APIs |
| **CP3 Side tests and interpolation** | After interpolation (about week 11) | Half-plane test, linear interpolation | AI for geometry utilities and curve code |

[4]

Every checkpoint follows the same four-part structure, so students learn the format once: **A. Compute** (apply), **B. Explain** (understand and analyse), **C. Code** (apply as procedure), **D. Spot the error** (evaluate). Each takes about 25 minutes. [5]

## 4. CP2 Transforms — student sheet, Version A

*Print this page for students. Time: 25 minutes. Allowed: pen, paper, a laptop with Wi-Fi off (or write code on paper). Not allowed: AI tools, internet, notes. Use column vectors: a point is written (x, y, 1), and M·P means M is applied to P.*

**Part A — Compute (about 8 minutes)**

A1. Let A = [[1, 2, 0], [0, 1, 3]] (2×3) and B = [[2, 1], [0, 1], [1, 0]] (3×2). Compute AB.

A2. Is BA defined? If so, what is its size? Compute only the entry in row 2, column 3 of BA.

A3. Write the 3×3 homogeneous matrices R (rotate 90° counter-clockwise about the origin) and T (translate by (2, 0)). Build the matrix M that **rotates first, then translates**. Apply M to the point P = (1, 0).

**Part B — Explain (about 5 minutes)**

B1. Compute N = R·T and apply it to P = (1, 0).

B2. Sketch P, M·P and N·P on a small grid. In at most two sentences, explain why M·P and N·P are different.

**Part C — Code (about 7 minutes)**

C1. Write a function `matmul(A, B)` in Python using plain lists (no NumPy). It must raise an error if the sizes do not match. It must pass:

```python
matmul([[1, 2], [3, 4]], [[5, 6], [7, 8]]) == [[19, 22], [43, 50]]
matmul([[1, 2, 3], [4, 5, 6]], [[1, 2, 3], [4, 5, 6]])   # must raise an error
```

**Part D — Spot the error (about 5 minutes)**

D1. An AI assistant gave this answer:

> "To rotate the unit square with corners (0, 0), (1, 0), (1, 1), (0, 1) by 90° counter-clockwise, use R = [[0, 1], [1, 0]]. Check: (1, 0) → (0, 1), which is correct for a 90° rotation."

Is the AI right? If not, explain the error, give the correct matrix, and describe a better check.

## 5. CP2 Transforms — answer key, Version A

| Item | Expected answer |
|---|---|
| A1 | AB = [[2, 3], [3, 1]] |
| A2 | Yes; BA is 3×3. Row 2, column 3: (0)(0) + (1)(3) = **3** |
| A3 | R = [[0, −1, 0], [1, 0, 0], [0, 0, 1]]; T = [[1, 0, 2], [0, 1, 0], [0, 0, 1]]; **M = T·R** = [[0, −1, 2], [1, 0, 0], [0, 0, 1]]; M·(1, 0, 1) = **(2, 1)** |
| B1 | N = R·T = [[0, −1, 0], [1, 0, 2], [0, 0, 1]]; N·(1, 0, 1) = **(0, 3)** |
| B2 | Matrix multiplication is not commutative. With column vectors the right-most matrix acts first, so N translates P to (3, 0) and then rotates it about the origin to (0, 3), while M rotates P to (0, 1) and then moves it to (2, 1). |
| C1 | See the reference solution below. Any correct approach passes. |
| D1 | **No.** [[0, 1], [1, 0]] is a **reflection across the line y = x**, not a rotation. It sends (0, 1) to (1, 0), whereas a 90° counter-clockwise rotation sends (0, 1) to (−1, 0). Its determinant is −1 (a rotation has +1). Correct matrix: **[[0, −1], [1, 0]]**. A better check uses at least two independent points, or checks det = +1 and that lengths are preserved. A single test point can pass by coincidence. |

[6]

Reference solution for C1:

```python
def matmul(A, B):
    n, m = len(A), len(A[0])
    if len(B) != m:
        raise ValueError("inner dimensions do not match")
    p = len(B[0])
    return [[sum(A[i][k] * B[k][j] for k in range(m)) for j in range(p)]
            for i in range(n)]
```

## 6. CP2 Transforms — Version B (retake)

Same format and timing, different numbers. [7]

| Item | Task | Expected answer |
|---|---|---|
| A1 | A = [[2, 0, 1], [1, 3, 0]], B = [[1, 2], [0, 1], [4, 0]]; compute AB | [[6, 4], [1, 5]] |
| A2 | Is BA defined? Size? Entry in row 1, column 2 | Yes, 3×3; (1)(0) + (2)(3) = **6** |
| A3 | S = uniform scale by 2; T = translate by (0, 3). Build M that **scales first, then translates**, and apply to P = (1, 1) | S = [[2, 0, 0], [0, 2, 0], [0, 0, 1]]; T = [[1, 0, 0], [0, 1, 3], [0, 0, 1]]; M = T·S = [[2, 0, 0], [0, 2, 3], [0, 0, 1]]; M·P = **(2, 5)** |
| B1–B2 | Compute N = S·T, apply to P, sketch, explain | N = [[2, 0, 0], [0, 2, 6], [0, 0, 1]]; N·P = **(2, 8)**: translating first moves P to (1, 4), which the scale then doubles |
| C1 | Same `matmul` task; tests: `matmul([[2, 0], [1, 1]], [[1, 3], [0, 2]]) == [[2, 6], [1, 5]]`, and a 3×2 times a 3×2 must raise an error | Reference solution as above |
| D1 | AI answer: "To scale by 2 and then translate by (0, 3), use M = S·T. For P = (1, 1) the result is (2, 8)." | **Order is wrong.** S·T translates first. Correct: M = T·S, result (2, 5). Quick check: scale (1, 1) to (2, 2), then add (0, 3) to get (2, 5) |

[8]

## 7. Rubric

Each part is marked **Met** or **Not yet**. The checkpoint result is **Pass** or **Not yet**; there is no score. [9]

| Part | Met | Not yet | Bloom level |
|---|---|---|---|
| **A. Compute** | Correct method throughout: rows times columns, size rule, homogeneous form, correct order in A3. One arithmetic slip is allowed if the method is right. | Wrong method (columns times rows, ignored size rule, missing homogeneous coordinate, wrong order in A3), or two or more slips | Apply |
| **B. Explain** | Correct N·P; sketch shows both results; explanation names non-commutativity **and** which transform acts first | Explanation missing, or only says "they are different" without saying why | Understand, analyse |
| **C. Code** | Passes the given test; raises an error on mismatched sizes; no index confusion | Fails the test, or has no size check | Apply (procedural) |
| **D. Spot the error** | Identifies the actual error, explains why it is wrong, gives the correct answer **and** a better check | Misses the error, or accepts the single-point check as sufficient | Evaluate |

[10]

**Pass rule:** all four parts Met. **Marking time:** about five minutes per student. A short "talk me through it" question during marking is allowed when a written answer is unclear, and the spoken answer counts. [11]

### 7.1 Common errors and what they indicate

| Error | What it suggests | Targeted practice |
|---|---|---|
| Multiplying columns by rows | Mechanics not secure | Five small products by hand, checked with a peer |
| Computing a product that is not defined | Size rule not understood | Size-prediction drill before computing |
| Forgetting the third coordinate (w = 1) | Homogeneous form not understood | Rewrite three 2D transforms in 3×3 form |
| Using R·T for "rotate then translate" | Order rule not understood | Sketch-first exercises: draw the result, then pick the order |
| Wrong sign on sine in a rotation | Rotation derivation not secure | Derive R from where (1, 0) and (0, 1) must go |
| Trusting a single test point | Verification habit missing | Find a matrix that passes one test point but is wrong |

[12]

## 8. The not-yet path

A student who gets Not yet receives targeted practice the same week for the part they missed (section 7.1) and retakes Version B, or a further variant, the following week. There is no grade penalty: the student simply continues matrix work without AI until they pass. If a student is still Not yet after two or three attempts, the adviser is informed so support can be arranged. This is a signal, not a failure mark. [13]

Faculty may use AI to generate further variants with different numbers, provided a person checks every answer before use. [14]

## 9. What passing unlocks, and the verification log

After passing CP2, students may use AI for matrix work in later assignments: computing long transform chains, debugging matrix code, learning NumPy or engine APIs, and exploring extensions such as quaternions. One rule stays: **every AI result involving matrices must be checked, and the check logged.** [15]

Accepted checks:
- **Known test point:** apply the matrix to a point whose correct result is known in advance.
- **Two independent points:** one point can pass by coincidence, as Part D shows.
- **Rotation properties:** lengths are preserved, Rᵀ·R = I, det(R) = +1 (−1 means a reflection).
- **Small hand case:** reduce the problem (2D instead of 3D, two transforms instead of five), compute it by hand, and compare. [16]

Verification log template (one line per AI use):

| Date | What AI produced | Check used | Result | Decision |
|---|---|---|---|---|
| e.g. 12 Nov | Camera transform matrix | Test point: origin should map to camera position | Did not match; order was wrong | Asked AI to fix; rechecked; passed |

[17]

Assignments change shape after the unlock. Before: "Compute this composite transform." After: "Build the transform chain that places a camera, a character and its arm in a scene. AI may do the arithmetic, but you choose and justify the order, and show two checks that it is right." [18]

## 10. Delayed retest (6–8 weeks later, inside the midterm or a later quiz)

*"A game object must first rotate 45° about the origin and then move to (5, 0). Which product, T·R or R·T, places it correctly? Without computing the full matrix, explain why, and describe one quick check you would run."* [19]

Expected answer: **T·R**, because with column vectors the right-most matrix acts first, so R rotates and then T translates. A quick check: the point (1, 0) should end at about (5.71, 0.71), that is (5 + cos 45°, sin 45°). Under R·T it would end at about (4.24, 4.24), which is clearly wrong. This item checks whether the skill lasted after AI was unlocked. Record results per student. [20]

## 11. Instructor notes

**Setting.** The checkpoint must be live and in class. Take-home checkpoints can be done with AI and prove nothing. Use paper plus a laptop with Wi-Fi off, or allow code on paper. In a class of about ten, direct observation is enough; no proctoring software is needed. [21]

**Language.** The class is international and taught in English. Mark explanations for correct reasoning, not grammar. Short sentences, labelled sketches and technical terms are enough. [22]

**Framing.** Present the checkpoint as "clearing you to use the tool", not as a test to fear. Show students the rubric and a practice version in advance. Students should know exactly what unlocks AI and how to retake. [23]

**Fuzzy boundaries.** Matrices appear inside shaders, rigs and cameras in later courses. Do not police the boundary tightly. Rely on the verification log and an occasional "talk me through this" question in reviews. [24]

**Evidence.** Keep a simple record per student: attempt dates, result per part, and the delayed retest result. Pass rates and retest results show whether the checkpoint works, and double as learning-outcome evidence for quality assurance. [25]

## Appendix. CP1 and CP3 in brief

| Part | CP1 Vectors | CP3 Side tests and interpolation |
|---|---|---|
| A. Compute | Dot product of (3, 4) and (4, 3), and the cosine of the angle between them: 24 and 24/25 = 0.96 | For the line from A(0, 0) to B(4, 0), which side is P(1, 2)? Cross term (Bx−Ax)(Py−Ay) − (By−Ay)(Px−Ax) = 8 > 0, so P is on the left. Linear interpolation from (0, 0) to (4, 8) at t = 0.25 gives (1, 2) |
| B. Explain | What the sign of a dot product tells a game about whether an enemy is in front of or behind the player | Why linearly interpolating angles from 350° to 10° gives the wrong turn, and what to do instead |
| C. Code | `dot(a, b)` and `normalize(v)` with a zero-length check | `lerp(a, b, t)` and `side(a, b, p)` |
| D. Spot the error | AI projects (3, 4) onto (2, 0) as (12, 0), forgetting to divide by \|b\|². Correct: (6/4)·(2, 0) = (3, 0) | AI writes lerp as A + t·B. For A = (2, 2), B = (4, 4), t = 0.5 it gives (4, 4) instead of (3, 3). Correct: (1 − t)·A + t·B |

[26]
