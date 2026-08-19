---
name: output
description: Hard-wrap every reply to 80 columns, flush left, so prose stays readable in a wide terminal instead of running the full window width. Use when the user asks for narrower output, 80 characters or columns, shorter lines, hard wrapping, easier-to-read replies in a wide window, or invokes /output. Accepts a width argument (/output 72). Persists for the rest of the session until turned off.
---

# Output width

Wrap all prose you write to the user at **80 columns**, starting flush left.
A reply that spans a 200-column terminal is one long line the eye cannot track
back from; 80 is the width that keeps it readable.

If the invocation carried a number (`/output 72`), that number is the width for
the rest of the session. Otherwise it is 80.

## Persistence

ACTIVE FOR EVERY RESPONSE from now on, not just the next one. It does not lapse
after a long conversation, a tool-heavy turn, or a topic change. If you are
unsure whether it is still active, it is.

Stop only when the user says so — "stop wrapping", "full width", "normal
output" — or sets a new width.

## What to wrap

Break lines at word boundaries so no line exceeds the width. Count characters,
and aim for 76 or fewer when a line contains emoji or CJK text, since those
render two columns wide.

- Paragraphs: hard-wrapped, one blank line between them, no leading spaces.
- List items: wrapped too. Indent continuation lines to line up with the text
  of the item, not with the bullet.
- Headings: leave them on one line even if a heading runs long; never break a
  heading mid-phrase.
- Sentences: never pad or stretch a line to reach the width. Ragged right is
  correct; justified text is not.

## What to leave alone

Wrapping these breaks them, so they keep their natural width and may exceed it:

- **Code blocks** — every character inside a fence is verbatim. A line break
  you insert is a syntax error or a changed command.
- **Tables** — a newline inside a row destroys the row.
- **URLs, file paths, identifiers, error strings** — never split one. If it
  does not fit in the remaining space, start it on its own line and let it
  overrun.
- Terminal output, logs, and diffs you are quoting.

## Not a licence to say less

The width is a formatting rule, not a length budget. Do not drop detail,
caveats, file references, or steps to make a reply look narrow — the same
content, in shorter lines. Existing style rules still apply on top of this;
where one is more terse, it wins.

## Example

Instead of one long line:

```
The retry lives in scripts/watchdog.py and fires only on StopFailure, which means an API error that killed the turn, not a normal stop.
```

write:

```
The retry lives in scripts/watchdog.py and fires only on StopFailure, which
means an API error that killed the turn, not a normal stop.
```

## Caveat worth knowing

The terminal wraps anything wider than its own window regardless. If the window
is narrower than the chosen width, lines will still fold — reduce the width to
match, e.g. `/output 60`.
