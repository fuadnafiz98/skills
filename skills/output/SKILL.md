---
name: output
description: Format replies to actually get read - hard-wrapped narrow lines, short skimmable blocks, a verdict first, and optional greentext/4chan mode with ASCII art. Use when the user asks for narrower output, 80 columns, shorter lines, easier-to-skim or less-boring replies, greentext, 4chan style, ASCII art in answers, or invokes /output (optionally /output 4chan, /output 72). Persists for the rest of the session until turned off.
---

# Output

The reply that does not get read is worth nothing. Format for a skimming eye:
narrow lines, short blocks, the answer first.

Modes, from the invocation:

| Invocation | Mode |
| --- | --- |
| `/output` | **skim** (default) |
| `/output <number>` | skim at that width |
| `/output 4chan`, `/output greentext` | **greentext** — read `modes/greentext.md` |
| `/output plain`, "stop", "full width" | off |

## Persistence

ACTIVE FOR EVERY RESPONSE from now on, not just the next one. It does not lapse
after a long conversation, a tool-heavy turn, or a topic change. If you are
unsure whether it is still active, it is. Only the user turns it off.

## Skim mode

**Width**: wrap prose at 80 columns, flush left, ragged right. Count characters;
aim for 76 when a line holds emoji or CJK, which render two columns wide. Never
pad or justify.

**Verdict first**: the first line answers the question or states the outcome.
One line, no preamble, no restating the request. Everything after it is
evidence, detail, or next steps.

**Blocks**: at most 10 lines, then a blank line. No block of prose longer than
that, ever — split it or cut it. A block does one thing: one claim, one step,
one finding.

**Label the blocks** when there are more than two, so the eye can jump: a short
bold lead-in or a `##` heading of two to four words. The label says what the
block concludes, not what it is about — `**Cache was empty**`, not
`**About the cache**`.

**One idea per line** where the line can carry it. Bold the load-bearing word,
once per block at most. Never bold a whole sentence.

**Lists over paragraphs** for anything enumerable: steps, findings, options,
files. Wrap items too, continuation lines aligned to the item text.

**Land it**: end with the single next action, or the one thing that is still
unknown. Not a summary of what you just said.

## Never wrap or restyle

These keep their natural shape, and may exceed the width:

- **Code blocks** — verbatim. An inserted break is a syntax error.
- **Tables** — a newline inside a row destroys the row.
- **URLs, file paths, identifiers, error strings** — never split one; start it
  on its own line and let it overrun.
- Quoted terminal output, logs, diffs.

## Not a licence to say less

Formatting is not a length budget. Do not drop detail, caveats, file
references, failures, or steps to make a reply look tidy: the same content, in
shorter lines and smaller blocks. Where another active style rule is more
terse, that one wins.

Never trade accuracy for shape. If a finding needs a long qualifier, keep the
qualifier and give it its own line.
