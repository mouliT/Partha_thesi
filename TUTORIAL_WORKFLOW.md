# Partha — Chapter 2 Tutorial Workflow (Feynman-First)

This folder is used to write a LaTeX tutorial based on `Chapter_2.pdf`.
The workflow is intentionally incremental: we write, review, and lock one small
unit at a time.

## Ground Rules (non-negotiable)

1) One section/subsection at a time
- I will only write *one* section (or one subsection) per iteration.
- You review and explicitly approve (“green signal”).
- Only after approval will I proceed to the next section/subsection.

2) Feynman-first explanation style
- Start from elementary B.Tech concepts (phasors, KCL/KVL, power balance, PWM timing).
- Build physical intuition first (WHY), then mechanics (WHAT/HOW), then math.
- The reader should be able to re-derive the final equations from first principles.

3) Figure-first, then equation (visual → variables → math)
- We do not introduce an equation before we point to the relevant figure/diagram
  and name the variables in plain language.
- Every figure that is used must be shown and explained where it first matters.

4) Notation must match the original PDF
- Variable names, phase labels (RYB/UVW), and terms (ASPI/SSPI, ASP/SSP, 1N/2N,
  CMV, etc.) must match `Chapter_2.pdf`.
- If we add helper notation, it must expand to the exact original symbols.

5) No forward references that compile as ??
- Do not use `\ref{...}` to labels that do not exist yet.
- If a later section is not written, refer to it in plain text without `\ref`.

6) No “assumed” details
- If a statement depends on a specific figure, table, or equation in the PDF,
  we verify it from the extracted assets (or from the PDF) before writing.

## Output Files

- Tutorial LaTeX file: `Chapter_2_Tutorial.tex`
- Extracted figures: `figures/Parth_ch2_Fig2_*.png`
- Figure context index: `figures/Parth_ch2_context.md`

## Lesson Structure

We split Chapter 2 into lessons to control cognitive load. Default is **5 lessons**:

1) Lesson 1: What is being compared? (winding configs + evaluation metrics)
2) Lesson 2: Torque ripple (harmonics, cancellation in ASP/SSP)
3) Lesson 3: DC bus voltage requirement (phasor derivations)
4) Lesson 4: DC bus capacitor requirement (3rd-harmonic + switching ripple models)
5) Lesson 5: CMV + interleaving + fault tolerance + efficiency + conclusions

If you want **4 lessons**, we can merge Lessons 2 and 3.

## Review Gates (how we confirm understanding)

At the end of each section/subsection we will include a short checkpoint prompt:
"Explain in your own words: what problem did we solve, what assumptions were used,
and what equation/figure is the key result?"
