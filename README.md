# COMP4431 — Agentic Exam Prep

*Preparing for an open-book Multimedia Computing final as **"Agentic Evan"** (me + my
agents): the same targeted-revision drill loop and agent-authored notes — re-tuned from
web programming to image / audio / video DSP — trading transcription time for practice,
understanding, and using the concepts.*

## What This Is

A worked record of prepping for the **COMP4431 (Multimedia Computing)** open-book final
using the [`agentic-exam-prep`](https://github.com/evnchn-agentic/agentic-exam-prep)
workflow — the sibling arc to
[COMP4021](https://github.com/evnchn-agentic/comp4021-agentic-exam-prep).

It is **not** an "an AI aced a course" story. It's a showcase of **learning ability** — what
becomes possible when a human hands the *mechanical* parts (note transcription, question
generation, drill bookkeeping) to agents and spends the reclaimed hours on practice,
understanding, and use.

> **"Agentic Evan" = me + my agents.** Long story short.

## The Journey

### Phase 0 — Frame the surface
Grouped the course into its multimedia/DSP modules (image, audio, video, compression) and
ran a diagnostic pass on where my gaps *actually* were. Same aimed loop as COMP4021 — but
the subject matter is signals and transforms, not HTTP and the DOM, so the *kind* of error
to hunt is different (see Phase 3).

### Phase 1 — Re-tune the drill engine for DSP
COMP4021 built its question banks from scratch; here the arc started from a **pre-existing
question bank** as the source pool and **re-designed the depth axes for the domain**: the
"code-output trace" axis became **algorithm-step trace** ("apply this 3×3 kernel to this
pixel block — what's the centre output?"), kept the **footgun** and **confusion-pair** axes
(lossy vs lossless, RGB vs YCbCr, DFT vs DCT, intra- vs inter-frame), and added
**formula-recall** (Nyquist rate, quantization, kernel math). Each generated set still went
through a verifier-agent pass before I drilled it.

### Phase 2 — Targeted revision, not re-reading
The loop graded every attempt by **reasoning quality, not just the letter**:
- *confident-correct* → **graduate** to a flashcard bank;
- *lucky-guess / answer-by-elimination* → **retest** in a fresh shape (letter right, rule not internalized);
- *wrong* → **revamp** against the specific misconception.

### Phase 3 — Predict where the next error hides (DSP failure shapes)
The failure-shape track (Set 0.x) re-tuned for signals: **"operation ≠ in-place"** (a
returns-new vs mutates trap), **"linear vs log-scale leak"** (treating dB as multiplicative),
**"continuous vs discrete-time leak"** (applying continuous-Fourier intuition to DFT bins),
**off-by-one in border / padding** (convolution edges), and the **lossy/lossless
decision-tree** (JPEG/PNG/GIF/WebP, H.264/ProRes, MP3/FLAC). Catch the *class* of error
before it surfaces on un-drilled material.

### Phase 4 — Agent-authored notes: the time reallocation *(the thesis)*
Same thesis as the sibling arc, and the real point of both. Courses often assign
note-writing precisely *because* transcribing is the memorization device. Handing that
transcription to an agent didn't skip the learning — it **reallocated the hours** from
copying material into notes toward *practising*, *understanding*, and *using* the concepts.
The agent freed the human to do the deeper work.

### Phase 5 — The final sprint
Tier-triaged what was actually worth drilling in the last stretch (you drill the right
10–15, not the whole bank), froze the print pack, and ran a drill-then-mark loop into the
exam.

## What's deliberately NOT here

- **No course materials** — no slides, lecture notes, the source question bank, or real exam
  questions. The proprietary content stays off this repo. The instructor is not named.
- The **illustrative drill sample**
  ([`sample-drill-illustrative.md`](sample-drill-illustrative.md)) is *self-authored on
  general multimedia/DSP concepts* to show the format — it is not course content.

## The reusable engine

This arc runs on the **[`agentic-exam-prep`](https://github.com/evnchn-agentic/agentic-exam-prep)**
skill — the methodology, course-agnostic. This repo and its
[COMP4021 sibling](https://github.com/evnchn-agentic/comp4021-agentic-exam-prep) are two
applications of it: one on web programming, one on DSP — showing the loop re-tunes to a
domain by swapping its depth axes and failure-shape catalogue, not its mechanics.
