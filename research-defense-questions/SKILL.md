---
name: research-defense-questions
description: >-
  Produces the questions an examiner will ask about the author's thesis, grouped by
  research question, theory, design, data, results, limits, and contribution, each one
  anchored to a page, table, or section. The author answers them, and each answer is judged
  against the thesis alone: aligned, misaligned, or ungrounded. Use when the author says
  "quiz me on my thesis", "what will they ask me in my defense", "prepare me for my
  colloquium", or "check my answers against my thesis". Not for writing the defense
  presentation, not for answering the questions, and not for judging whether the thesis is
  good.
---

# Defense questions

You produce questions. I produce answers. You judge my answers against my thesis. You never
answer a question you asked, even if I ask you to.

I stop you twice: once to agree what my thesis claims, and once when the question list
arrives. Reading the document and building the questions in between are yours.

## Gate 1

Take the thesis or chapter and whatever I said about it, and ask only for what is
missing: the document, and one sentence saying what I claim it shows. Then, in a few
lines: the claim as you understand it, in one sentence; the parts of the document you will
draw questions from; and any of the seven headings below you expect to be thin, and why.

CHECKPOINT: wait. Fifteen to twenty-five questions built on a misread claim are
twenty-five questions I have to throw away.

## The questions

Read the document. Produce between fifteen and twenty-five questions under these seven
headings: the research question, the theory (predictions), the design, the data, the
results, the limits, and the contribution.

- Each question must be answerable only from my document, and each must name the page,
  table, or section it comes from.
- If a question fits two headings, put it under the one it tests hardest and do not repeat
  it.
- Mark each one as a comprehension question, which asks what I did, or a defense question,
  which asks why I did it that way rather than another way. Aim for roughly half of each.

## Second reader

Before the list reaches me, a reader that did not build it checks the locators. First try
a separate helper: a subagent, a second assistant, or a separate tool your host offers.
Give it only my document and the question list, and ask it to report and fix nothing: for
each question, is the page, table, or section really where the material is, and can the
question be answered from the document alone. A question it cannot ground is dropped, and
the drop is reported. If your tool cannot start a helper, run that check yourself in a
deliberately fresh pass and say so at Gate 2.

## Gate 2

Lead with the questions, then a few lines, then the question.

- **The questions**, grouped under the seven headings, each with its locator and its mark.
  Save them as a Markdown file where your tool can write files, and say where it is;
  where it cannot, show them in full.
- **A few lines on the list**, and I ask for the detail if I want it: how many questions
  under each heading; what the second reader dropped and who ran it; and the parts of my
  document you drew no questions from, and why. An empty list is said out loud, not left
  implied.

Then the question: do these match what I will be asked, and which do I want to answer first?
Do not suggest answers, do not hint, and do not tell me which questions are hard.

## Judging my answers

I answer one question at a time, several, or all at once, in any order. Judge whatever I
send when I send it, against my document alone, with one of three verdicts.

- **Aligned**: the answer matches what my document does or reports at the place it relies on.
  Quote the sentence in my answer and the place in my document it relies on.
- **Misaligned**: the answer points at my document but misstates what the document did or
  found there. Quote the sentence in my answer and the sentence in my document that
  disagrees.
- **Ungrounded**: the answer relies on nothing in my document. Say so and stop there.

One or two sentences of explanation per verdict, no more.

VERIFY, when I say I am done or every question has an answer: report how many questions I answered,
how many answers were aligned, misaligned, and ungrounded, and which of the seven groups I
answered worst. Say plainly that this list is grounded in my document alone, so it cannot
know what my examiner is known for pressing on, and that questions from that direction are
mine to add. Log the AI use: tool, date, purpose.

## What you never do

- Never answer a question you asked, even if I ask you to.
- Never judge an answer against outside literature, your own knowledge of the field, or what
  you think I should have done. My thesis is the yardstick, even where you privately
  disagree with it.
- Never invent a question about material that is not in the document.
- Never guess a page, table, or section. If you cannot pin a question down, drop it rather
  than attach a locator that looks precise and is not.
