# MAT188 — Standards-Based Grading (SBG): overview & resources

This is the front door to the MAT188 standards-based grading materials. It
explains how the approach works and links to the two companion projects: the
**grading system** (open) and the **tutorial worksheets** (shared with
colleagues on request).

MAT188 is a first-year Linear Algebra course (~1000 students) at the
University of Toronto. These materials are by Camelia Karimianpour and
collaborators; see *License & credit* below.

---

## How SBG design and grading works

**The idea.** Instead of accumulating points on assignments, students are
assessed against a fixed list of explicit **learning standards** — short
"I can …" statements, one skill each. A standard is either *demonstrated* or
not yet, and students get **repeated opportunities** to demonstrate each one.
Only *eventual* mastery matters: demonstrating a standard once, anywhere, is
enough, so a strong later attempt erases an earlier miss.

**The standards.** Each standard has a key like `ch3-CON-subspacecheck` and is
classified by type — **computational (COM)**, **conceptual (CON)**,
**visual/geometry (VG)**, and **writing (WRIT)** — and by chapter. They live in
a single source list and are pulled by key wherever they appear, so the wording
is identical in every place a student meets them.

**How standards reach students (the design).** One standards bank feeds three
channels:

- **Pre-class readings** — each opens with the standards it targets.
- **Tutorial worksheets** — each lists the standards it covers, and every
  question is labelled with the standard(s) it assesses.
- **Gateway Exams** — there are supervised computer-based tests, each question measures performance on a specific standard.
- **Exam-prep / review packages** — drawn from the same labelled question bank.

Assessment happens across several modalities, each with its own reattempt
design: semi-supervised **group tutorials** (with a graded resubmission round),
unsupervised **online homework** (WeBWorK, multiple attempts), and supervised
**gateway quizzes** (a practice round plus two supervised attempts).

**How grading works (the pipeline).** Every gradeable item on every assessment
gets a **score key** (e.g. `ww1-2`, `tut3-2-1`, `ex1-2-1`). A **lookup table**
says, for each standard and each modality, which score keys demonstrate that
standard and how many must be correct. A small Python pipeline then reads the
raw exports from each platform, applies those rules per student, and produces a
per-student **progress report** showing which standards each student has
demonstrated so far. Because it always takes the best evidence across *all*
attempts, adding a resubmission can only add demonstrations, never remove them.

For a fuller treatment, see the grading kit's `docs/01-standards-based-grading.md`
(what SBG is, with references) and `docs/02-the-mat188-implementation.md` (the
real course this is based on).

---

## The resources

### 1. The grading system — `sbg-grading-kit` (open)

A self-contained, runnable kit that turns platform exports into per-student
standards-mastery reports: the standards list, the question→standard lookup
table, converters for WeBWorK and Gradescope-style exports, the evaluator, and
HTML/PDF report generators — with 30 synthetic students so it runs out of the
box.

- Code & docs: https://github.com/camelia-k-p/sbg-grading-kit
- Run it in your browser (no install): https://colab.research.google.com/github/camelia-k-p/sbg-grading-kit/blob/main/colab/sbg_pipeline.ipynb

### 2. The tutorial worksheets — `mat188-worksheets` (private repo + Overleaf link)

The LaTeX project that builds the tutorial worksheets from a central, labelled
question bank, plus viewers for the full standards list and question bank.
Because it contains **worked solutions and grading rubrics**, the full source is
kept in a **private GitHub repository** (master/backup), and a trimmed version
(no exams, homework archives, or work-in-progress) is shared through an
**unlisted, view-only Overleaf link** that anyone with the link can open and
copy:

- Overleaf (view & copy your own): **https://www.overleaf.com/read/sywwsntxhmgx#6b2c15**
- Private repo (invited collaborators): https://github.com/camelia-k-p/mat188-worksheets

Open the Overleaf link to read the worksheets, then use **Copy Project** to make
your own editable copy.

---

## License & credit

Course design, learning standards, and writing: **Camelia Karimianpour**
(University of Toronto), lead author. Pre-class readings are co-authored with
Geoff McGregor, Arthur Chan, Vardan Papyan, and Shai Cohen; the analysis
pipeline is by Simeon Wong; the LaTeX system is by Samuel P. Dumas. The inquiry-based structure of the course and structur of the questions used in tutorials are heavily inspired by MATH217 worksheets at Universiy of Michigan. 

Code is released under the **MIT License**; teaching content under
**CC BY-NC-SA 4.0** (non-commercial, share-alike, with attribution). See each
repository's `LICENSE` files for specifics.

## Acknowledgements

The inquiry-based structure of this course, and the design of the tutorial
questions, are **adapted from** the inquiry-based **Math 217 (Linear Algebra)**
worksheets at the **University of Michigan**. The original Math 217 worksheets are
© University of Michigan Mathematics Department and are licensed under
**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0)**.
Some questions in MAT188 tutorial adn lecture materials here are an adaptation — modified and extended for
MAT188 — and are released under the same CC BY-NC-SA 4.0 license. With gratitude
to the Math 217 instructors and the Michigan IBL community.

- Michigan Inquiry-Based Learning: https://sites.lsa.umich.edu/ibl/
