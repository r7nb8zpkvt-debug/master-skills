# Caption (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-caption` (MIT, same author). Read this when the
user wants the caption for a Reel, carousel or photo, or asks about hashtags.

```bash
python3 tools/caption.py caption.txt
python3 tools/caption.py caption.txt --keywords "client proposals,agency pricing"
```

It prints the caption the way the feed does: the first 125 characters in a box, everything else
behind "... more". Read that box before anything else. Exit 0 is READY, 1 is REVIEW or FIX,
2 is bad input.

## Decide which job the caption has

**Job A: the video already hooked them.** A Reel carries its own hook, spoken and on screen. The
caption is not a second hook; competing with the video loses both. Line 1 is the ask (the
comment keyword from the script), then the context that makes the ask make sense, then the words
people search. This is the default for anything step 6 of SKILL.md produced.

**Job B: the caption is the content.** A photo, a single image, a carousel whose cover has
already spent its six words. Line 1 is the hook and works like a Reel hook: concrete, short, cut
at a cliff rather than mid-clause.

Say which job you are writing and why.

## Shape

```
Line 1   125 visible characters. Job A: the ask, plainly. Job B: the hook.
         Never a greeting, a hashtag, or an emoji as the first character.
Body     2 to 6 short paragraphs, a blank line between each. The search terms live here.
Ask      one. Comment a keyword, save it, or DM. One.
Tags     up to five, on their own line at the bottom, or none.
```

The limit is 2,200 characters and almost nothing needs it. A caption that earns the tap and then
delivers 600 characters beats one that delivers 1,800.

## Hashtags and search

- Instagram capped hashtags at five per post on 18 December 2025, down from thirty. They are topic
  labels, not a reach lever. `caption.py` fails anything over five.
- `#viral`, `#fyp`, `#explorepage`, `#foryou` describe nothing. Cut them.
- Search reads the caption text. The phrase the user wants to be found for goes in as a phrase a
  person would type, inside a normal sentence ("client proposals" in line 3), not as a tag. Ask
  for two or three terms and pass them with `--keywords`.

## Rules

- No link in the caption. It is not clickable. Bio, DM, or a first comment (say so in the receipt).
- One ask. `caption.py` counts them.
- A keyword people can type: one word, no spaces, no emoji, and said out loud in the video.
  `Comment CONTRACT` works; `Comment "the contract guide"` does not.
- Emoji as punctuation, not decoration. The linter warns above 4 per 100 characters.
- Write alt text for carousels and photos. Screen readers and Instagram both read it.

## Loop

1. Decide Job A or B and say which.
2. Draft it, then `tools/humanize.py` it. Captions are short, so slop is louder here.
3. `tools/caption.py` with the search terms. Fix every FAIL; decide every WARN out loud.
4. Print the copy-ready block, then:

```
CAPTION READY
job:        A, the reel carries the hook
visible:    118 of 125 characters before the cut
ask:        one, comment CONTRACT
hashtags:   3
search:     "client proposals" in line 3, "agency pricing" in line 5
linter:     READY
```

Nothing is posted. The user pastes it.
