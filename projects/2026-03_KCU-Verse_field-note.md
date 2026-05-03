# Side Project: KCU Verse — Field Note (Dropped)

## What it was
A YouTube content pipeline plan: classify K-pop lyrics by TOPIK
proficiency levels, regroup them by theme and emotion, and turn the
output into textbook-style learning playlists for the KCU channel.
Target was the ~40M Korean learners worldwide who use K-pop as a
study gateway. Competitive gap was specific — no existing service
offered TOPIK-graded K-pop lyric content in Hangul (LingoClip used
romanization only).

## My role
Tech PM bridging the content team and the AI engineer.
- Authored the one-pager and the extended technical roadmap
  (4-phase pipeline: lyrics ingest → NLP classification →
  playlist composition → LLM-generated study assets → video
  assembly → YouTube publish)
- Researched datasets (EX3exp Kpop-lyric-dataset 25,696 songs,
  TOPIK/NIKL vocabulary lists) and copyright considerations
  (KOMCA licensing, 2022 Korean Supreme Court precedent on NLP
  corpus use, YouTube Content ID risk)
- Mapped the morphology + sentiment + topic stack
  (KoNLPy, KoBERT/KcELECTRA) and the LLM/image-gen layer
- Ran kickoff meetings with the PO, the AI engineer, and the
  KCU channel team

## How far we got
- Phase 1 (planning shared with PO and AI Dev): done
- Phase 2 (extended planning doc): done
- Phase 3 (KCU team review): Go decision reached, then a
  channel-direction shift was announced
- Phase 4 (offline kickoff, March 1): done
- After that: dropped

## Why it stopped
The collaborating channel was pivoting its content identity, and
the new direction didn't have room for music-as-automated-output as
part of the worldview. I'd designed the project specifically because
the AI engineer joining us was interested in NLP and was a
multilingual learner herself — using lyrics as a study tool felt
like a meaningful build for both of us. Adapting to the new
direction would have meant restarting the planning from scratch.

I also made a call I'd reconsider now: I didn't push the
conversation further with the channel side. I've spent enough years
in content to know that pivots and zigzags are normal — what looked
like inconsistency was a struggling channel chasing virality and
algorithm fit. But I worried the AI engineer would read this work as loss
of direction rather than the working reality of media, and I cut
the discussion to protect her motivation. In hindsight I could
have kept the door open longer.

## What I take away
- The hard ceiling on a PM working without internal authority on
  the partner side. I felt it clearly here.
- A real picture of what a non-slop AI output pipeline looks like.
  Choosing playlists as the bridge between NLP, content, and
  generation — instead of churning out the kind of output you'd
  call AI slop — let me imagine wider, more legitimate ways AI
  can plug into existing media work. That mental model stays
  with me even though the project didn't ship.
