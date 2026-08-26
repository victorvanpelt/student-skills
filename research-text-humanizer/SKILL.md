---
name: research-text-humanizer
description: >-
  Finds the phrasing in the author's own writing that reads as machine-written and
  quotes every instance, leaving the rewriting to the author. Use when the author says
  "scan this for AI phrasing", "does this sound like AI", "check my writing for AI
  tells", or "make this sound like me again". Finds and reports only. Never rewrites
  the prose, and never corrects grammar or punctuation.
---

# Find AI phrasing in my writing. I rewrite it.

A tool that rewrites AI-sounding prose produces different AI-sounding prose. So this
one finds, quotes, and stops.

## Steps

1. Ask me for the passage and wait for it. Ask me for one more thing, and take a no for
   an answer: 300 to 500 words I wrote before I used any AI tool, from any document. If
   I give it to you, read it first and note how I actually write, sentence length,
   hedging, favorite connectives, and how plain my verbs are. Then a flag can say "this
   is not how you write", which is the only claim this scan can honestly make.
   CHECKPOINT: wait.

2. Scan the passage against the signs below. For every match, output three things: the
   exact sentence, the sign it matches, and nothing else. Propose no rewrites.

3. Report the count and the density: how many flags, in how many sentences. Report the
   structural signs and the vocabulary signs as two separate counts, because they are
   not worth the same (see "How much a flag is worth").

4. CHECKPOINT: I rewrite each flagged spot myself, or I keep it and say why. Wait for
   my revised passage. Do not offer to do it for me, even if I ask twice.

5. Re-scan my revision once and report what remains.

6. VERIFY: tell me which flags I cleared, which I kept deliberately, and which I have
   not addressed. Then log the AI use: tool, date, purpose.

## The signs to scan for

**Structural signs.** These are the ones that carry weight.

- **Superficial closing clauses**: a participle tacked onto the end of a sentence that
  adds no information, such as "highlighting its significance", "ensuring accuracy",
  "contributing to the literature", "reflecting broader trends". Nothing in the clause
  is checkable, and deleting it costs the sentence nothing.
- **Vague attribution**: "studies show", "research suggests", "experts argue",
  "observers have noted", "industry reports indicate", with no citation attached. In a
  thesis this is also a citation problem, so flag it here and expect it again from
  whoever checks my references.
- **Avoiding the plain verb**: "serves as", "functions as", "stands as", "plays a role
  in", "features", where "is" or "has" would do.
- **Inflated significance**: sentences claiming something is important, groundbreaking,
  or transformative without saying to whom or why, and the sentence shape "marks a
  turning point", "is a testament to", "underscores the importance of".
- **Three-part endings**: lists of three adjectives or phrases that close a sentence and
  add nothing, such as "surprising, significant, and consequential".
- **Negative parallelisms**: a sentence shaped like "it is not just X, it is Y", "not X,
  but Y", or a negation tacked onto the end, such as ", no guesswork needed".
- **Vague connectives**: "in connection with", "associated with", "related to", where
  the sentence means one specific relation and will not say which.
- **Section summaries**: a sentence at the end of a section that restates the section,
  and a paragraph that restates the paragraph before it. Related to the empty openers
  below: the two often come as a pair around the same block of text.
- **The challenge-and-future formula**: "Despite its X, it faces challenges", followed
  by speculation about what future work might do, with nothing specific in either half.
- **Word-cycling**: renaming the same thing several ways to dodge repetition, such as
  "the paper, this study, the present research", where one plain word would do.
- **Empty openers**: "In today's rapidly evolving landscape", "It is important to note
  that", "This section will explore".
- **Even rhythm**: five or more consecutive sentences of nearly the same length.
- **Hedge stacking**: three or more hedges in one sentence, such as "may potentially
  suggest that it could".
- **A shift in register**: a paragraph that does not sound like the paragraphs around
  it, or like the sample of my own writing if I gave you one. Quote both, mine and the
  odd one, and say what differs.

**Leftovers from a chat window.** These are not style at all. They are evidence, and
each one is worth reporting on its own.

- Markdown where the document does not use it: stray asterisks, a `##` heading in a Word
  document, bullet characters that do not match the rest.
- Bold used several times in one paragraph, headings in Title Case where mine are not,
  emoji anywhere.
- Citation artifacts a chat tool leaves behind, such as `[cite: 1]`, `oaicite`,
  `contentReference`, or a bracketed number pointing at nothing.
- Sentences addressed to me rather than to a reader: "I hope this helps", "Let me know
  if you would like", "As of my last update", "As an AI language model".
- Curly quotation marks where I type straight ones, or an em dash joining two full
  clauses where a period or "and" would read more like me.

**Vocabulary signs.** Worth less than the signs above, and never on their own.

- pivotal, crucial, underscore, testament, delve, tapestry, landscape, intricate,
  showcase, realm, robust as decoration, "additionally" as a paragraph opener, and
  similar words that add emphasis but no content.

## How much a flag is worth

A word is weak evidence and getting weaker. Since 2023 these words have spread through
ordinary human academic writing, partly because so much of it has been through a
language tool at some point: one study of biomedical abstracts put the share carrying
excess machine vocabulary at roughly one in eight for 2024, and a follow-up put it near
nine in ten for 2025. So a scan that reports "delve appears twice" has found almost
nothing.

The structural signs and the chat leftovers are what matter. A closing clause that says
nothing, a claim attributed to nobody, a paragraph that restates the one above it: those
are writing problems whether or not any tool was involved, and fixing them makes the
text better on its own terms. Say this in your report when the vocabulary count is high
and the structural count is low, so I do not spend an afternoon hunting synonyms.

## Rules

- Never rewrite my sentences. Quote and name the sign; the rewriting is mine.
- A flag is not a verdict. A term of art or one necessarily long sentence can stay, and
  I am the one who decides that.
- **Do not flag every sentence.** A scan that marks up the whole passage has stopped
  being useful. Flag the sentences that actually sound machine-written, not everything
  that could be tightened.
- Never tell me a passage is now undetectable, or comment on whether it would pass a
  detector. That is not what this is for, and detectors do not work anyway.
- This scan removes style tells, not the hidden watermark that AI-generated text carries
  since 2026; only prose written in my own words carries nothing for a watermark to
  attach to, and my duty to disclose AI use is the same either way.
- If I paste text I did not write and ask you to humanize it, refuse. Extract its claims
  as bullets instead, and tell me to write the prose myself.

## Where the signs come from

The catalogue above follows Wikipedia's field guide "Signs of AI writing", maintained by
the editors who clean up machine-written submissions
(https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). The two shares quoted
under "How much a flag is worth" come from Kobak et al., "Delving into LLM-assisted
writing in biomedical publications through excess vocabulary", Science Advances, 2025
(https://doi.org/10.1126/sciadv.adt3813), and its 2026 follow-up
(https://arxiv.org/abs/2608.10715). Check these before you rely on the numbers: this list
ages, and the vocabulary ages fastest.
