# Weekly plan (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-plan` (MIT, same author). Read this when the user
says plan my week, what should I post, content calendar, or "I have nothing to post about".

## Input

Read `~/.claude/virality/audience.md`, `voice.md`, `swipe.md` and `log.md` if they exist. The swipe
file (written from step 2 of SKILL.md) is the user's own evidence about which formulas land in
their niche right now and outranks any default here. The log stops the plan repeating a theme from
the last fortnight. If the audit playbook ran, its STOP and DO MORE lines win over everything.

Missing pieces: ask once, batched, for what they sell and to whom, the 3 or 4 themes they want to
be known for, what actually happened this week (a call, a number, a mistake, a thing they built,
an argument), and 10 accounts worth being visible to.

## What to post

4 to 5 posts a week, at least 3 of them Reels: Reels are the format that reliably reaches
non-followers, carousels go deep with followers, stories are daily and planned separately. Never
two of the same type back to back.

| type | per week | job |
| --- | --- | --- |
| Proof | 1 | something that happened, with a number. Reel |
| Teach | 1 to 2 | one thing the viewer can do today. Reel or carousel |
| Opinion | 1 | a position that could lose followers. Reel |
| Story | every other week | a scene with a cost. Reel |
| Offer | every other week | what you sell, plainly. Carousel or stories |

Each slot gets a theme, the specific angle from this week, the format, and a formula name from
`tools/hooks.json`, varied across the week. An angle, not a topic: "AI" is not a plan, "the
proposal we lost because the draft had an em dash in it" is a Reel.

## When to post

When the audience is awake and not at work: early evening for most consumer audiences, early
morning for business ones, in the audience's timezone. Say it plainly: the hour matters far less
than the first two seconds. If the hooks are not working yet, optimising post times is polishing
the wrong thing.

## The engagement round

20 minutes a day, before posting. A list of 10: 5 reach accounts (comment early, before the thread
is 200 deep), 3 peers of the same size, 2 people who could buy (comment for weeks before any DM,
never pitch in a comment). Hand it to `playbooks/engage.md`.

## Output

```
WEEK OF SEP 15
MON  engage only (20 min)
TUE  7:30pm  REEL      PROOF    The Time Anchor     5-hour proposal to 20 minutes
THU  7:00pm  CAROUSEL  TEACH    Job B caption       the 4-slide clause breakdown
FRI  7:30pm  REEL      OPINION  Negative Command    stop doing discovery calls
SUN  6:00pm  REEL      STORY    Mid-Sentence Start  the refund email
STORIES  daily, 3 to 5 frames, question box Thursday
ENGAGE   5 reach / 3 peers / 2 buyers: ...
Say "write Tuesday" and I'll draft it.
```

Write it to `~/.claude/virality/plan.md`. "Write Tuesday" runs SKILL.md steps 4 to 6 on that slot.
Nothing is scheduled or posted.
