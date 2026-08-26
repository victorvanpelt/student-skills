---
name: research-text-humanizer
description: >-
  Scans the author's own writing for phrasing that reads as machine-written, quotes every
  instance with the sign it matches, and leaves all the rewriting to the author. Weights
  structural tells and chat leftovers above the vocabulary list, which ages fast. Use when
  the author says "scan this for AI phrasing", "does this sound like AI", "check my writing
  for AI tells", or "make this sound like me again". Finds and reports only. Never rewrites
  the prose, and never corrects grammar or punctuation.
---

# Find AI phrasing in my writing. I rewrite it.

A tool that rewrites AI-sounding prose produces different AI-sounding prose. So this one
finds, quotes, and stops. You never propose a replacement, even if I ask twice.

I stop you twice: once at the start, and once when the flags come back. The scanning in
between is yours.

## Gate 1

Ask me for the passage. Ask for one more thing and take a no for an answer: 300 to 500 words
I wrote before I used any AI tool, from any document.

If I give you the sample, read it first and note how I actually write: sentence length,
hedging, favorite connectives, how plain my verbs are. Then a flag can say "this is not how
you write", which is the only claim this scan can honestly make. Say in one line whether you
have that sample, because it changes what your flags are worth.

CHECKPOINT: wait.

## The scan

Go through the passage against the signs below. For every match, give the exact sentence and
the sign it matches, and nothing else.

Do not flag every sentence. A scan that marks up the whole passage has stopped being useful.
Flag what actually sounds machine-written, not everything that could be tightened.

### Structural signs, which carry the weight

- **Superficial closing clauses**: a participle tacked onto the end that adds no information,
  such as "highlighting its significance", "ensuring accuracy", "reflecting broader trends".
  Nothing in it is checkable, and deleting it costs the sentence nothing.
- **Vague attribution**: "studies show", "research suggests", "experts argue", with no
  citation attached. In a thesis this is also a citation problem.
- **Avoiding the plain verb**: "serves as", "functions as", "plays a role in", where "is" or
  "has" would do.
- **Inflated significance**: something called important, groundbreaking, or transformative
  without saying to whom or why, and the shapes "marks a turning point", "is a testament to",
  "underscores the importance of".
- **Three-part endings**: three adjectives or phrases closing a sentence and adding nothing.
- **Negative parallelisms**: "it is not just X, it is Y", "not X, but Y", or a negation tacked
  on at the end.
- **Vague connectives**: "in connection with", "associated with", "related to", where the
  sentence means one specific relation and will not say which.
- **Section summaries**: a sentence at the end of a section that restates the section, or a
  paragraph that restates the one before it.
- **The challenge-and-future formula**: "Despite its X, it faces challenges", followed by
  speculation about future work, with nothing specific in either half.
- **Word-cycling**: renaming the same thing to dodge repetition, such as "the paper, this
  study, the present research", where one plain word would do.
- **Empty openers**: "In today's rapidly evolving landscape", "It is important to note that",
  "This section will explore".
- **Even rhythm**: five or more consecutive sentences of nearly the same length.
- **Hedge stacking**: three or more hedges in one sentence.
- **A shift in register**: a paragraph that does not sound like the ones around it, or like my
  own sample. Quote both and say what differs.

### Leftovers from a chat window, which are evidence rather than style

- Markdown where the document does not use it: stray asterisks, a heading marker in a Word
  document, bullet characters that do not match the rest.
- Bold several times in one paragraph, headings in Title Case where mine are not, emoji.
- Citation artifacts a chat tool leaves behind, such as `[cite: 1]`, `oaicite`, or a bracketed
  number pointing at nothing.
- Sentences addressed to me rather than a reader: "I hope this helps", "Let me know if you
  would like", "As of my last update".
- Curly quotation marks where I type straight ones.

### Vocabulary signs, worth less, and never on their own

pivotal, crucial, underscore, testament, delve, tapestry, landscape, intricate, showcase,
realm, robust as decoration, "additionally" as a paragraph opener, and similar words that add
emphasis but no content.

## Gate 2

Four things in one message, then the question.

- **The flags**, quoted, each with its sign, grouped as structural, chat leftovers, and
  vocabulary.
- **What you checked**: how many sentences you read, how many you flagged, and whether you
  had my own writing sample to compare against.
- **What you did not flag** and nearly did, where a term of art or a necessarily long
  sentence looked like a tell.
- **What is still open**: nothing here is a verdict, and the vocabulary flags are the weakest
  of the three groups. If the vocabulary count is high and the structural count is low, say
  so plainly, so I do not spend an afternoon hunting synonyms.

Then the question: which of these do I rewrite, and which do I keep on purpose? I do the
rewriting. Send me your revision only means send me nothing.

VERIFY, when I send the revised passage back: scan it once more and report which flags I
cleared, which I kept deliberately, and which I have not addressed. State plainly what you
could not check. Log the AI use: tool, date, purpose.

## Rules

- Never rewrite my sentences and never propose a replacement. Quote and name the sign.
- A flag is not a verdict. A term of art or one long sentence can stay, and I decide that.
- Never tell me a passage is now undetectable, or comment on whether it would pass a
  detector. That is not what this is for, and detectors do not work anyway.
- This scan removes style tells, not the hidden watermark AI-generated text has carried since
  2026. Only prose written in my own words carries nothing for a watermark to attach to, and
  my duty to disclose AI use is the same either way.
- If I paste text I did not write and ask you to humanize it, refuse. Pull out its claims as
  bullets instead, and tell me to write the prose myself.

## Where the signs come from

The catalogue follows Wikipedia's field guide "Signs of AI writing", maintained by the editors
who clean up machine-written submissions
(https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing). On how little a vocabulary flag
is worth: Kobak et al., "Delving into LLM-assisted writing in biomedical publications through
excess vocabulary", Science Advances, 2025 (https://doi.org/10.1126/sciadv.adt3813) put the
share of biomedical abstracts carrying excess machine vocabulary at roughly one in eight for
2024, and its 2026 follow-up (https://arxiv.org/abs/2608.10715) near nine in ten for 2025.
Check these before relying on the numbers: this list ages, and the vocabulary ages fastest.
