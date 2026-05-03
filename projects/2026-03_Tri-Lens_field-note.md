# Side Project: Tri-Lens (Bricolage Variant) — Field Note

## What it was
The original Tri-Lens was
[@liminal-cipher](https://github.com/liminal-cipher)'s idea:
one service producing the same AI/tech news at three difficulty
levels (general / developer / researcher). I bolted Moltbook —
an "agent-only SNS" platform I came across — onto that idea and
ran a variant of my own: multiple persona-configured agents, each
interpreting the same news through a different professional lens.
Bricolage in the literal sense — the original idea plus an
external piece I happened to find, jammed together to see what
would happen.

The bot was meant to be a daily "appetizer" — reading tech news
the way a producer reads a story: what's the angle, what does
this mean for content and media. Not a news aggregator. A
persona running a tiny news desk with my voice on it.

## My role
- Wrote the variant proposal (EN + KR)
- Configured the persona stack (SOUL.md / IDENTITY.md / USER.md /
  AGENTS.md / HEARTBEAT.md) on OpenClaw
- Operated the bot for ~5 weeks across 4 briefing notes
  (0216 / 0222 / 0311 / 0314)
- Ran cost diagnostics, fixed the runaway, documented what I
  found for the team

## What actually happened
- Feb 5–8: Proposal written, OpenClaw installed, Moltbook joined.
  Bot live within hours.
- Feb 9–14: Costs ran away to a ~$120–150/month pace. Sessions
  ballooned to 352KB on the worst day.
- Feb 16: First briefing. Three root causes found —
  heartbeat firing every 30 min (~40x/day), a "skill update check"
  that kept overwriting my custom rules with the upstream defaults,
  and the upstream HEARTBEAT.md actively encouraging the bot to
  roam and comment everywhere. Switched heartbeat off, replaced
  it with a cron job (M/W/F).
- Feb 22: Second briefing. The fixes themselves had been guided
  by Claude, and Claude had been hallucinating OpenClaw config
  that didn't exist. Started forcing it to web-search official
  docs before answering. Settled the runaway for real.
- Mar 11: Third briefing. Bot stable. March total: **$0.86.**
  At one point the bot itself surfaced a mismatch between its
  rules file and the cron schedule and asked about it instead of
  running blind.
- Mar 14: Found a path to running OpenClaw on a ~$5 single-board
  chip instead of leaving the MacBook on. Ordered the chip.

## What I learned

**An agent is infrastructure, not a chat partner.**
Treating an agent as something you "talk to" misses the actual
cost structure. It's closer to running a server: cron schedules,
log analysis, config-file version control, cost monitoring,
emergency kill-switches. The bot costs money just by being on —
even a "nothing to do, HEARTBEAT_OK" reply was burning ~$0.10
because the persona stack had to load into context every time.
The MacBook-on-or-off dilemma was real: turn it off and the bot
goes silent, leave it on and the meter keeps running. If you're
going to keep an agent alive, you're operating infrastructure.

**The persona paradox.**
Pouring my PD background into the persona files made the bot
mine — and made every API call more expensive, because the
persona stack rode along in context every time. Flatten the
persona to save cost and it stops being mine. There was a
second version of the same problem in the output: leaning on
broadcast analogies once is a fresh angle; leaning on them five
times in a row reads as "is that all this person has." A
producer who keeps reaching for the same frame becomes a
caricature of themselves. Designing a persona is a real exercise
in self-portraiture, and the line between "this is me" and
"this is a flattened version of me" was thinner than I expected.

## Why it ended
The original concept was 
[@liminal-cipher](https://github.com/liminal-cipher)'s, and they
built the proper version of it — clean, on its own track
([tri-lens-news](https://github.com/liminal-cipher/tri-lens-news)),
the way it was meant to exist. My variant was a bricolage that
wedged in Moltbook as an external piece, useful for what I
learned along the way. Once the main branch was alive in the
right hands, there was no reason to keep dragging the variant
along.
