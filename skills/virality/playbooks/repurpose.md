# Repurpose (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-repurpose` (MIT, same author). Read this when the
user has one long asset (YouTube video, podcast, livestream, newsletter, blog post, client call)
and wants it turned into reels and carousels.

One good long asset holds four to six posts. Most people pull one and throw away the rest.

## Input

A transcript, article, newsletter, script or call summary. For a public video, get the transcript
the same way as step 3 of SKILL.md; otherwise ask the user to paste. Read all of it first. If it
is the user's own video, ask for the file too: a Reel cut from their real footage beats one built
from their words read again. The `edit` master skill does the cutting.

## Extract, do not summarise

Nobody wants the summary. Pull what stands alone:

| pull | what it is |
| --- | --- |
| Claims | every sentence that would start an argument |
| Numbers | every figure, cost, duration, percentage |
| Stories | every moment with a person, a scene and a cost |
| Mechanisms | every "the way this actually works is..." |
| Mistakes | every admission of something that went wrong |
| Lines | every sentence already quotable as is |

List what you found, with counts, before writing anything. Fewer than four items means the asset is
thin and four posts from it will be thin too. Say that.

## Format per extract

- Claim, mistake, story: Reel. They need a voice and a face.
- Mechanism, numbered list: carousel (`playbooks/carousel.md`). They get re-read.
- A quotable line: a story frame, not a post.

## Build the week

Every post stands completely alone. The viewer has not seen the source and never will, so never
"as I said in my latest video". Give each a different formula from `tools/hooks.json`: five posts
with the same hook shape read as a content mill. Strongest claim first, the story midweek, the
mechanism last. With the user's own footage, cut on the sentence, not on the breath.

```
SOURCE: "Why we killed discovery calls" (42 min podcast, 8,900 words)
FOUND   5 claims, 9 numbers, 3 stories, 4 mechanisms, 2 mistakes, 7 quotable lines
TUE  REEL      Negative Command    Stop running discovery calls (use the 14:20 clip)
WED  CAROUSEL  Job B caption       The 4-question form that replaced the call
FRI  REEL      Mid-Sentence Start  "...and he asked for a refund nine days later"
SUN  REEL      The Time Anchor     Six hours a week back, one deleted link
Say "write Tuesday" and I'll draft it.
```

Then draft one at a time through steps 4 to 6 of SKILL.md. Four finished scripts at once all sound
the same, and the user shoots none of them.
