# Comments, replies and DMs (Instagram)

From Jakeschincariol/instagram-agent-skill `/ig-comment`, `/ig-reply` and `/ig-dm` (MIT, same
author). Read this when the user wants a comment on someone else's post, replies for the thread
under their own post, or a DM. Everything here is written, humanized with `tools/humanize.py`, and
handed over. The user posts and sends every word. Never automate comments, replies or outreach
DMs, and never drive a browser to publish: it breaks Instagram's Terms of Use and gets accounts
action-blocked.

## Comments on other people's posts

A comment near the top of a reel with 40,000 views is seen by more people than most accounts' own
posts. A generic one is worse than none: it marks the account as a pod account to the one person
whose opinion mattered, the creator. Input is the pasted post or a screenshot; never scrape.

Pick a type by what the post is, never type 1 by default:

| # | type | when |
| --- | --- | --- |
| 1 | Add a datum | the claim can be supported with a number |
| 2 | The missing case | right but incomplete: "This holds until..." |
| 3 | Respectful disagree | name the agreement, then the fork |
| 4 | Extend one line | quote the good line, build on it |
| 5 | The real question | the post skipped the hard part |
| 6 | The receipt | you have done the thing, two sentences on what happened |
| 7 | The correction | a factual error. Right, brief, kind, sure |
| 8 | The reframe | right facts, wrong frame |
| 9 | The one-liner | under 10 words, funny or true |

One to three sentences, one idea. Never open with "Great post", "Love this", "So true", an emoji
or the creator's name and an exclamation mark. Never restate the reel. Never pitch. Early beats
clever: the first hour is when a comment gets carried. Give two options of different types, and
say which you would post and why. Batch mode: 5 to 10 pasted posts, one comment each, and note in
`~/.claude/virality/log.md` who was commented on this week so it does not become the same three
accounts every day.

## Replies under the user's own post

Sort first and say the counts:

| bucket | what it is | what it gets |
| --- | --- | --- |
| KEYWORD | the word the post asked for | the promised thing |
| LEAD | someone describing the problem the user solves | a real answer in public, then a door |
| SUBSTANCE | adds data, disagrees, extends | the longest reply on the thread |
| QUESTION | a question many people have | a reply, and often a Reel |
| SUPPORT | "great post", a tag, an emoji | a like and 3 to 8 words at most |
| NOISE | spam, bait, bad faith | nothing |

Write in that order and stop when the value stops. Answer the actual question in the reply rather
than sending people to DMs. Use their name once, no exclamation mark. Match their length. To a
critic: concede the true part in their words, then hold the line, once. To a hater: nothing, and
hide it if abusive. A QUESTION with real demand behind it (likes on the comment) becomes a Reel
replying to that comment: hand it to step 4 of SKILL.md with The Question formula and their words
verbatim as the hook.

## DMs

Only three kinds are worth writing. Reply to a raised hand (they commented the keyword, answered a
poll, replied to a story): most of the value. The warm approach to someone the user has genuinely
been commenting on for weeks. A collab or brand pitch with a reason it is them. Cold DMs to
strangers are the lowest-yield use of the hour; say so, offer two weeks of commenting instead, and
write it only if they still want it.

Before writing, get who, the trigger (the actual reason to message today), and what the user
wants. No trigger, no message.

**Keyword delivery** sends the thing first, ungated:

```
{name}, here it is: {the thing or the link}.
{one line on how to use it}
{one question they can answer in four words}
```

"Before I send it, what do you do?" is a bait and switch and it is remembered. Keyword auto-replies
through Instagram's own tools or an approved partner are fine; bulk DMs to people who did not
interact are not.

**Warm first message:** 2 to 4 sentences, reference the specific thing in their words, give before
asking, one small ask, no link or calendar in message one, no voice note to a stranger.

**Collab pitch:** four lines: what you have watched them do, the idea, what they get, what you need.

**Follow-ups: two.** +4 days with something new (never "just bumping this"), +10 days to close the
loop and say you will stop. Then stop.

Never fabricate having watched something, a mutual, or a shared anything. Output the message, its
character count, and the follow-ups with their send days.
