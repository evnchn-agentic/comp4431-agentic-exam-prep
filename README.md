# COMP4431 — Agentic Exam Prep

*A multimedia final doesn't ask you to recite what convolution is — it asks you to run a 3×3
kernel over a pixel block by hand, on an image you've never seen. So I built a drill loop that
hunts the errors that bite on *unfamiliar* transforms — dB misread as multiplicative, the
off-by-one at a convolution's edge — and handed the note-transcription to my agents to buy
the hours to actually practise. Here's how that went, rough patches included.*

## What This Is

The full arc of prepping for the **COMP4431 (Multimedia Computing)** open-book final with the
[`agentic-exam-prep`](https://github.com/evnchn-agentic/agentic-exam-prep) loop — a record of
**learning ability** on a subject made of signals and transforms: what a human reaches when
the mechanical parts (note transcription, question generation, drill bookkeeping) go to
agents, and the reclaimed hours go to practice and understanding.

> **"Agentic Evan" = me + my agents.** Long story short.

## The Journey

### Phase 0 — Frame the surface
Grouped the course into its multimedia/DSP modules (image, audio, video, compression) and
ran a diagnostic pass on where my gaps *actually* were. The loop is aimed from the start —
and because the subject is signals and transforms rather than HTTP and the DOM, the *kind* of
error worth hunting is different (Phase 3).

### Phase 1 — Re-tune the drill engine for DSP
The mechanics carried over from COMP4021; the **depth axes were re-designed for the domain**:
the "code-output trace" axis became **algorithm-step trace** ("apply this 3×3 kernel to this
pixel block — what's the centre output?"), kept the **footgun** and **confusion-pair** axes
(lossy vs lossless, RGB vs YCbCr, DFT vs DCT, intra- vs inter-frame), and added
**formula-recall** (Nyquist rate, quantization, kernel math). Each generated set went through
a verifier-agent pass before I drilled it — and I caught my *own* arithmetic slip in a
hand-authored footgun question, flagging it in the answer key rather than burying it.

**Not smooth:** when I asked for a set with answers, an agent tried to *infer* the answers
from raw unverified material instead of transporting the already-curated, self-checked sets.
I shut that down — with verified artifacts in hand, the agent's job is to *carry* what's
checked, not *re-derive* it (re-derivation is expensive and invites fabrication).

### Phase 2 — Targeted revision, not re-reading
The loop graded every attempt by **reasoning quality, not just the letter**:
- *confident-correct* → **graduate** to a flashcard bank;
- *lucky-guess / answer-by-elimination* → **retest** in a fresh shape (letter right, rule not internalized);
- *wrong* → **revamp** against the specific misconception.

### Phase 3 — Predict where the next error hides (DSP failure shapes)
The failure-shape track (Set 0.x) re-tuned for signals: **"operation ≠ in-place"** (a
returns-new vs mutates trap), **"linear vs log-scale leak"** (treating dB as multiplicative — −6 dB is *a quarter* of the
power, not "half, twice"), **"continuous vs discrete-time leak"** (applying continuous-Fourier
intuition to DFT bins),
**off-by-one in border / padding** (convolution edges), and the **lossy/lossless
decision-tree** (JPEG/PNG/GIF/WebP, H.264/ProRes, MP3/FLAC). Catch the *class* of error
before it surfaces on un-drilled material.

### Phase 4 — Agent-authored notes: the time reallocation *(the thesis)*
This is the real point of the whole exercise. Courses often assign note-writing precisely
*because* transcribing is the memorization device. Handing that
transcription to an agent didn't skip the learning — it **reallocated the hours** from
copying material into notes toward *practising*, *understanding*, and *using* the concepts.
The agent freed the human to do the deeper work.

### Phase 5 — The final sprint
Tier-triaged what was actually worth drilling in the last stretch (you drill the right
10–15, not the whole bank), froze the print pack, and ran a drill-then-mark loop into the
exam. **One honest snag:** the agent's first grep of my marked answers undercounted — I'd
added marks *between* its passes, and only "look carefully" surfaced them. Lesson baked in:
re-read fresh, never trust a stale grep of a moving target.

## Why it worked — generalization, not recall

The whole payoff of this loop is **generalization**. The failure-shape track (Phase 3)
doesn't memorize answers — it learns *where a class of error strikes next*, on material it
was never drilled on. That is exactly what a DSP exam tests once it stops asking you to
recite and starts asking you to *apply* a transform to a case you haven't seen. Rote
memorization of practice questions falls apart at that boundary; failure-shape generalization
is built for it. The agentic revision didn't shortcut the understanding — it went **above and
beyond** the usual prep. That's the point of the whole exercise.

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
