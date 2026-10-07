# Profile score (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-profile` (MIT, same author). Read this when the
user asks to fix their bio, score or optimise their profile, or "why don't people follow me". Also
go here when the audit shows high non-follower reach and few follows: that is a profile problem,
not a hook problem.

The profile is a decision screen, reached from one reel. It has about three seconds to answer: is
there more of that here, and is it for me.

## Input

Ask the user to paste or screenshot the name field, handle, bio, where the link goes, highlight
names, what is pinned, and the first nine grid covers. A screenshot of the top of the profile and
the first two grid rows is enough for a first pass. Never log in for them.

## Score it

Read `playbooks/profile-rubric.json`: twelve items, 100 points, each with what full marks looks like
and how it usually fails. Score every item, show the table, give the total. Most first passes land
in the 30s and 40s; a generous score is useless.

```
PROFILE SCORE  38/100
  name field       2/12   name only, no words anyone searches
  bio first line   3/12   three nouns and a coffee emoji
  pinned three     0/10   nothing pinned
  highlights       2/8    "Random", "Life", "2023"
  ...
```

## Rewrite in order of points lost

The user has to go and change each field, so do not rewrite everything at once.

1. **Name field** (30 characters, the bold line, not the handle). Instagram search matches it.
   `{Name} | {what you do, in searched words}`. Give three options.
2. **Bio line one.** Who it is for and what changes for them. Not a job title, not a pipe list of
   identities. The rest of the 150 characters carries one piece of proof or one plain offer, using
   the proof bank from `audience.md`. Never invent a number.
3. **Pinned three.** Best proof, clearest explanation of the offer, best introduction to the
   person. Four taps, highest leverage on the page.
4. **Highlights.** Four to six, named for buyer questions: Pricing, Results, How it works, About.
5. **Link.** One destination that matches the bio's promise. Two is already a menu.
6. **Grid covers.** Chosen, not frame one. Four words of cover text makes the grid readable at a
   glance; `tools/title.py --cover` checks cover text.

## Output

Score table, then each rewrite as a copy-ready block in fix-first order, humanized. Re-score and
show the delta honestly: if it reaches 84, say 84 and name what the rest needs (usually a grid, a
story habit and a pinned post that does not exist yet). Nothing is saved to Instagram; the user
edits each field.
