# Carousel (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-carousel` (MIT, same author). Read this when the
user says carousel, slides, swipe post, or has a list-shaped or step-shaped idea that would die
as a single image.

A swipe is an interaction and a scroll is not, so carousels hold attention longer than anything
else on the grid. Instagram can also re-show a carousel from a later slide to someone who skipped
it, so slide 2 has to stand on its own.

## Carousel or Reel

Carousel when the idea has sequence and gets re-read: steps, a framework with parts, a before and
after, a list worth screenshotting. Reel when it has motion, a face, or a payoff that has to be
seen happening. One claim is neither: write it as a Reel (SKILL.md step 4 onward) and say so.

## Structure

6 to 10 slides. The cap is 20, and 20 is a book nobody finishes. Under 5 and the swipe never starts.

```
1        COVER   the hook, 6 words or fewer, legible at grid thumbnail size, one line of promise under it
2        STAKE   why this matters, one sentence. It is a second cover, so it cannot be setup
3..N     ONE IDEA PER SLIDE: a 3 to 7 word headline, at most 25 words under it
N+1      RECAP   the whole thing as a list. The screenshot slide
LAST     CTA     one action: save, comment a keyword, or follow
```

Pick the cover from `tools/hooks.json` like any hook (`on_screen` lines are already six words or
fewer) and run it through `tools/hookscore.py`.

## Slide rules

- The cover is most of the result. Six words, big.
- Build at 1080x1350 (4:5) and keep cover text clear of the outer 120 px on every side, so the
  grid crop never matters.
- Number the slides (3/8). People finish what they can see the end of.
- No slide is a paragraph. Over 25 words, split it.
- The recap slide is the one that gets sent. Sends are the strongest signal you can earn, so it
  must read with no context.
- The handle small in a bottom corner of every slide. Screenshots travel without you.
- Alt text on the cover at minimum.

## Files

1080x1350, JPEG or PNG, up to 20 items. Build as HTML, one `<section>` per slide with
`width:1080px; height:1350px; page-break-after: always`, one accent colour, type no smaller than
32 px. Render with headless Chrome or whatever HTML-to-image the user has. If the project has a
brand or design system, use it. For anything more designed than that, the `build` master skill
covers the design pass.

## Output

Slide copy first, as a numbered list the user can edit in ten seconds, then the caption (Job B in
`playbooks/caption.md`). Humanize both. Render files only after the user approves the copy.

```
CAROUSEL  ·  8 slides
1  COVER   THE $18,000 CLAUSE
           One line I now put in every contract.
2  STAKE   I approved the work. They asked for the money back nine days later.
3          WHAT IT SAYS
           Payment on delivery, not on approval.
...
7  RECAP   All four lines, in order.
8  CTA     Comment CONTRACT and I'll send the full clause.
Caption: Job B, hook in line 1, one ask, 3 tags.
```

Nothing is uploaded. The user posts it.
