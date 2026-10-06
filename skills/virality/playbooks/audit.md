# Audit (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-audit` (MIT, same author). Read this when the user
pastes their insights or past posts and asks what's working, why something flopped, or to audit
their content.

The only honest evidence of what works for an account is that account. Every rule in this skill is
a prior; the user's last 30 posts are the data.

## Input

Whatever they have: per-post insights (views, reach, interactions, watch time, saves, shares,
follows, non-follower share of reach), retention graphs for the best and worst recent reels (worth
more than everything else together), or just posts with view counts. Also read
`~/.claude/virality/log.md`, which records the formula each shipped script used.

Normalize view counts the same way as step 2: `tools/collect.py` then `tools/swipe.py`, with the
user's own handle as the only creator, gives the outlier multiple per post.

## What to measure

Raw views mostly measure follower count. Compute these and show the working:

| metric | how | tells you |
| --- | --- | --- |
| Outlier multiple | views / the account's median | a real hit or a normal day |
| Non-follower reach | % of reach from non-followers | whether it travelled |
| Hold at 3s | still watching at 3s / started | the hook's grade |
| Average watch time | from insights | whether the middle worked |
| Sends per reach | shares / reach | the strongest signal you can earn |
| Follows per reach | follows / reach | whether the profile converted |

Rank by outlier multiple and sends per reach. 4,000 views with 90 sends beat 60,000 with 11.

## Find the pattern

Top five against bottom five, and be willing to say something the user will not like:

- Hold at 3 seconds first. If top and bottom differ there, it is the hook and nothing else.
- Formula (from the log or `tools/hookscore.py` on each first line), format, length band
  (under 15s, 15 to 30, 30 to 60, over 60), theme, whether they replied in the first hour.
- Day and time last, and only if nothing else separates them. It is almost never the cause.

State each finding as a claim with its evidence and the sample size. 30 posts show a pattern;
6 do not, and saying so beats inventing one.

## The distinction that saves months

Views and no follows is a profile problem: go to `playbooks/profile.md`. No views is a hook
problem: back to steps 5 and 6 of SKILL.md. Separate the two before recommending anything.

## Output

```
AUDIT  ·  31 posts  ·  Jun 12 to Sep 5  ·  median views 4,100
TOP 5 BY OUTLIER MULTIPLE
  18.2x  Contrarian Flip   74,600 views  62% non-follower  hold@3s 71%  128 sends
  ...
BOTTOM 5
   0.3x  The List           1,200 views   9% non-follower  hold@3s 31%    2 sends
WHAT THE DATA SAYS
1. Hold at 3 seconds is the whole story: top five 66%, bottom five 33%.
2. Posts where you were the one who looked bad: 8.1x vs 0.9x for the rest. n=5.
3. Day of week shows nothing. Stop optimising it.
STOP: tool listicles.   DO MORE: a cost you paid, with the number.
```

Then feed it forward: the plan playbook builds next week on it, and step 2 filters the swipe file
to the formulas that work for this account.
