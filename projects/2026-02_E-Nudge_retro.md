# Project 1: E-Nudge (AI Community Nudge) — Retrospective

## What it was

MS AI School cohort 9 1st project.
A Korean-language hate speech detection system with 3-class
classification (hate / offensive / none), built as a community
moderation tool. BEEP! dataset → pseudo-labeling → 8-model comparison → ComplementNB v4 selected as final
model. Deployed on Azure Web App with FastAPI + Azure SQL DB +
Blob Storage.

## What I actually did

- ML modeling end-to-end (text classifier owner)
- 8-model comparison and selection (CNB v4 final)
- Pseudo-labeling design and execution
- KcELECTRA "dual bottleneck" validation structure
- RAI documentation (Transparency Note + Impact Assessment)
- Market analysis
- Presentation narrative and structure
- Final presentation video produced in Remotion

## What I'm proud of

**Staying inside traditional ML instead of escaping to deep learning.**
"Hate" as a classification target is fundamentally subjective, which
showed up as low model scores. The easy move would have been to jump
to a DL model for a score boost. Instead I researched my way to
pseudo-labeling, kept the project inside our learned scope (and
inside what we could actually deploy), and tied it into the
LLM-as-Judge pattern we'd seen in class — turning a methodology
choice into a presentation arc that landed.

**Recognizing RAI was something we had to own.** I'll admit the
execution came late, in the run-up to the final presentation, and
I'll lean on the excuse that the project itself was RAI-adjacent so
the framing was already there. We didn't get most of it into the
product as features. But documenting the RAI thinking — Transparency
Note, Impact Assessment — let us preserve the meaning of what we'd
built, even where the implementation fell short.

## What I struggled with

**The team drifted into functional silos.** I went in wanting us to
explore and learn together rather than divide by function, and we
held that for a while. But the pressure of shipping pulled us into
role-based work by the end. Holding both feelings here: the regret
of not getting the shared exploration I wanted, and the
acknowledgment that having six people equally deep on every detail
was probably never realistic.

## What I'd do differently

**My imagination for the final output was too small.** I'd push it
further — toward a real integration with an existing live service,
not just a standalone demo. I see that ceiling now, in retrospect.

## What I took away

- The people. People I came to love.
- A pattern of acting strategically — asking for help, taking
  visible credit where it was due, working to build a sense of
  togetherness.
- A re-realization of what happens when ideas and research meet
  each other at the right moment. The compound effect.
