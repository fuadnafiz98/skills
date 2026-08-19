# Modes

Each mode is a shape, not a licence to change the facts. The floor in `SKILL.md`
holds in all of them: verdict first, 80 columns, blocks of ten, nothing dropped.

## layer-cake — the default spine

Eyetracking calls this the layer-cake scan: descriptive headings let a reader
take the answer from headings alone.

- A bold lead-in or `##` heading every three to six lines.
- The heading states what the block **concludes**, not what it is about:
  `**Cache was empty**`, never `**About the cache**`.
- Two to four words, front-loaded.
- Reading only the headings, top to bottom, must still answer the question. If
  it does not, the headings are wrong.

## bluf — one question, one answer

- Line one is the whole answer, in one sentence.
- Then only the slabs that apply, each labelled and short: **WHY**, **WHAT
  CHANGED**, **NEXT**, **RISK**.
- No narrative, no chronology of your own work.
- Use for a direct question or a decision. Not for exploratory findings, where
  it flattens things that deserve headings of their own.

## receipts — stack it on anything

- Every claim that came from tool output carries its proof, inline, after an
  arrow: `default is 180s → server log: 180.1s gap`.
- Proof is a measured value, a log line, a `file.py:42`, an exit code. Not a
  restatement of the claim.
- Say plainly when something is **not** verified: `not checked`, `assumed`.
- This is the one add-on that may cost extra words. It always earns them.

## hook-loop — the short-form structure

Hook, payoff, one tease, payoff. Attention comes from an open loop, so the risk
is obvious: never let the loop delay the answer.

- The verdict still comes first, before any hook.
- At most **one** tease per reply, mid-way, on its own line, and it must point
  at something real: `— and the cache was not the culprit —`.
- Pattern interrupt every eight to ten lines: a rule, a heading, a code block, a
  table. Not a new glyph.
- No manufactured tension about work that was trivial. If there is no twist,
  this is the wrong mode.

## patch-notes — for turns that changed things

```
! fixed    epoch rendering as a percentage
+ added    range check on every percent
~ changed  cache write is atomic, per-uid
- removed  slow_floor, slow_types
⚠ known    terminal still folds below 80 cols
```

- One line per change, verb-first, present tense.
- `⚠ known` is not optional when something is left broken, skipped, or
  untested.
- Paths and identifiers as written, never reflowed.

## sparkline — only with real numbers

Two or more comparable numbers, or none of this.

```
unset   ████████████████████ 180.1s
20000   ██                    20.0s
15000   █                     15.1s
```

- Bars scale to the largest value, 20 characters wide at most.
- The number stays in text beside the bar; a bar alone is decoration.
- One row per measurement, units on every row. Never bar a number you did not
  measure.

## quiz — at most once, only when surprising

- One line posing the question the way you actually faced it, then the answer,
  bolded, immediately: `Cache race, or something dumber? **Something dumber.**`
- Never more than one per reply, never on a simple question, never as a way to
  withhold. If the reader could not have guessed wrong, skip it.

## greentext — explicit only

`/output 4chan`. See `greentext.md`.
