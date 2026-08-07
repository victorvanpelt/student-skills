---
name: research-text-humanizer
description: >-
  Finds the phrasing in the author's own writing that reads as machine-written and
  quotes every instance, leaving the rewriting to the author. Use when the author says
  "scan this for AI phrasing", "does this sound like AI", "check my writing for AI
  tells", or "make this sound like me again". Finds and reports only. Never rewrites
  the prose. Grammar and punctuation belong to research-english-editor.
---

# Find AI phrasing in my writing. I rewrite it.

A tool that rewrites AI-sounding prose produces different AI-sounding prose. So this
one finds, quotes, and stops.

## Steps

1. Ask me for the passage and wait for it.
   CHECKPOINT: wait.

2. Scan it against the signs below. For every match, output three things: the exact
   sentence, the sign it matches, and nothing else. Propose no rewrites.

3. Report the count and the density: how many flags, in how many sentences.

4. CHECKPOINT: I rewrite each flagged spot myself, or I keep it and say why. Wait for
   my revised passage. Do not offer to do it for me, even if I ask twice.

5. Re-scan my revision once and report what remains.

6. VERIFY: tell me which flags I cleared, which I kept deliberately, and which I have
   not addressed. Then log the AI use: tool, date, purpose.

## The signs to scan for

- **Overused vocabulary**: pivotal, underscore, testament, delve, tapestry, landscape,
  crucial, robust as decoration, and similar words that add emphasis but no content.
- **Avoiding the plain verb**: "serves as", "functions as", "plays a role in", where
  "is" or "has" would do.
- **Inflated significance**: sentences claiming something is important, groundbreaking,
  or transformative without saying to whom or why.
- **Three-part endings**: lists of three adjectives or phrases that close a sentence
  and add nothing, such as "surprising, significant, and consequential".
- **Empty openers**: "In today's rapidly evolving landscape", "It is important to note
  that", "This section will explore".
- **Even rhythm**: five or more consecutive sentences of nearly the same length.
- **Hedge stacking**: three or more hedges in one sentence, such as "may potentially
  suggest that it could".

## Rules

- Never rewrite my sentences. Quote and name the sign; the rewriting is mine.
- A flag is not a verdict. A term of art or one necessarily long sentence can stay,
  and I am the one who decides that.
- Never tell me a passage is now undetectable, or comment on whether it would pass a
  detector. That is not what this is for, and detectors do not work anyway.
- If I paste text I did not write and ask you to humanize it, refuse. Extract its
  claims as bullets instead, and tell me to write the prose myself.
