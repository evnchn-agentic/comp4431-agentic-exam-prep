# Illustrative drill sample (self-authored — NOT course content)

> These questions are **hand-authored on general multimedia/DSP concepts** to show the
> *format* of the drill loop. They are **not** from COMP4431, its question bank, or any exam.
> The "Your answer / Thinking" line is where reasoning gets written down — it's what the
> loop grades on (reasoning quality, not just the letter; see Phase 2 in the README).

## Q1 🔄 [retest] sampling — the Nyquist trap

A signal contains frequencies up to 8 kHz. To reconstruct it without aliasing, the sampling
rate must be at least:

A) 4 kHz
B) 8 kHz
C) 16 kHz
D) 32 kHz

**Your answer:** ___    **Thinking:** ___________________________________________

---

## Q2 🔄 [revamp] off-by-one in the border (a DSP failure-shape)

You convolve a 5×5 image with a 3×3 kernel using **"valid"** (no padding) mode. The output
dimensions are:

A) 5×5
B) 4×4
C) 3×3
D) 7×7

**Your answer:** ___    **Thinking:** ___________________________________________

---

## Answers

**Q1 — C (16 kHz).** Nyquist: sample at ≥ 2× the highest frequency. *Failure-shape:
formula-recall — the factor is 2, and it's the *highest* frequency, not the bandwidth name.*

**Q2 — C (3×3).** "valid" convolution shrinks each axis by `(kernel − 1)`: 5 − (3−1) = 3.
*Failure-shape: off-by-one in border/padding — the exact trap the Set 0.x track in Phase 3
extrapolates across the course's spatial operations.*
