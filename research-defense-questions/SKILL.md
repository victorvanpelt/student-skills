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
license: CC-BY-4.0
metadata:
  author: Victor van Pelt
  version: 1.1.0
---

# Defense questions

You produce questions. I produce answers. You judge my answers against my thesis. You never
answer a question you asked, even if I ask you to.

I stop you twice: once when you say back what you think I asked, and once when the
question list arrives. Reading the document and building the questions in between are
yours.

## Gate 0: say back what you think I asked

Take the thesis or chapter and whatever I said about it, and ask only for what is missing:
the document, and one sentence saying what I claim it shows. Then, before you build a
single question, write down what you think this job is, in five short parts:

- **My words**, quoted exactly, and today's date.
- **The problem**: what is wrong or missing, as you read it from my words. Include the
  claim my document makes, as you understand it, in one sentence.
- **The result**: what you will hand me, and how we will know it is right.
- **The limits**: what you must not change, and what you must not touch.
- **The open questions**: what you assumed, which parts of the document you will draw
  questions from, any of the seven headings below you expect to be thin and why, and the
  calls only I can make.

Do this yourself. Reading an instruction is judgment, so it never goes to a helper.

CHECKPOINT: wait. Nothing is built until I answer. Twenty-five questions built on a misread
claim are twenty-five questions I have to throw away.

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

Before the list reaches me, a reader that did not build it checks the locators. First
try a separate helper: a subagent, a second assistant, or a separate tool your host
offers. Give it only my document and the question list, and ask it two numbered
questions, answered against the document and fixed by nobody:

1. For each question, is the page, table, or section it names really where that material
   is? Where it is not, say where the material actually is, or say it is nowhere.
2. For each question, can it be answered from the document alone? Where it cannot, quote
   what the question asks for that the document does not carry.

It changes nothing and moves nothing. You do that. A question whose locator is simply
wrong gets the right locator, or comes off the list if there is none. A question the
document cannot answer does **not** come off the list: it moves to a closing section headed
"questions my thesis does not answer", with the reader's line saying what the document does
not carry. That section is the most useful thing in this file. In a defense, the question
your thesis cannot answer is the one the examiner will ask, and deleting it would hide the
exposure rather than prepare you for it. It sits outside the numbered list on purpose, so
it never reaches the answer-judging below, which would only ever return ungrounded and
teach me nothing.

If your tool cannot start a helper, run those two questions yourself in a deliberately
fresh pass and say so at Gate 2.

## Gate 2

Lead with the questions, then a few lines, then the question.

- **The questions**, grouped under the seven headings, each with its locator and its mark.
  Save them as a Markdown file where your tool can write files, and say where it is;
  where it cannot, show them in full.
- **Questions my thesis does not answer**, in their own closing section, unnumbered and
  outside the seven headings, each with the line saying what the document does not carry.
  Say plainly that these are not failures of the list; they are where I am exposed. If the
  section is empty, say so out loud.
- **A few lines on the list**, and I ask for the detail if I want it: how many questions
  under each heading; how many locators the second reader corrected, how many questions it
  moved to the closing section, how many came off entirely for want of any locator, and who
  ran it; and the parts of my document you drew no questions from, and why. An empty list is
  said out loud, not left implied.

Then the question: do these match what I will be asked, and which do I want to answer first?
Do not suggest answers, do not hint, and do not tell me which questions are hard.

CHECKPOINT: wait. Nothing is settled until I answer.

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
