---
name: research-feedback-reviser
description: >-
  Turns supervisor comments, seminar feedback, referee reports, or marker notes into a
  numbered list of separate requests, says what each one asks of the author's document, then
  drafts the smallest change that meets each one and has the drafts checked in a fresh pass.
  Hands back the drafts, the alternatives it did not take, the items it could not draft, and
  a one-line-per-item record for the next supervision meeting, for the author to accept or
  reject one at a time. Use when the author says "my supervisor sent comments", "work through
  this feedback", "help me respond to these notes", or "revise my chapter from this
  feedback". Not for deciding whether the feedback is right; that is the author's call.
license: CC-BY-4.0
compatibility: >-
  Needs web search to confirm any new reference a draft adds. Without it, the skill says so
  and adds no new reference.
metadata:
  author: Victor van Pelt
  version: 1.1.0
---

# Work through feedback without losing control of it

Feedback arrives as prose. Prose hides how many separate things are being asked for, which
of them conflict, and how big each one really is. You take it apart, draft the smallest
change that meets each piece, and hand me the drafts. Nothing enters my document before I
say so.

I stop you twice: once when you say back what you think I asked, and once when the drafted
changes come back. Everything between is yours. Deciding once, with drafts in front of me,
beats deciding twice, once in the abstract and once again on the page.

## Gate 0: say back what you think I asked

Before you plan anything, write down what you think this job is, in five short parts:

- **My words**, quoted exactly, and today's date.
- **The problem**: what is wrong or missing, as you read it from my words.
- **The result**: what you will hand me, and how we will know it is right.
- **The limits**: what you must not change, and what you must not touch.
- **The open questions**: what you assumed, and the calls only I can make.

Do this yourself. Reading an instruction is judgment, so it never goes to a helper.

CHECKPOINT: wait. Nothing is planned until I answer. This is the cheapest correction I will
ever make. The same correction after the drafts exist is not cheap.

## Intake, one round

Take whatever I gave you and ask only for what is missing, in one message: the feedback, the
document it refers to, what the document is, and who wrote the feedback. Who wrote it changes
what a sensible response looks like: a supervisor's comment is close to binding, a seminar
attendee's is advice. Ask once, then work.

## Take the feedback apart

**Split it.** One comment can contain three requests, and an aside can contain a fourth.
Number them and quote the exact words behind each, naming the source where there is more than
one, so I can see where it came from.

**Say what each one asks of my document.** One sentence, in my document's own terms (this
section, this claim, this table), never a restatement of the comment.

**Classify each one.**

- **Mechanical**: a typo, a wrong number, a missing citation. No judgment needed.
- **Presentational**: reorder, shorten, clarify. My call, low stakes.
- **Substantive**: a claim, an interpretation, a method choice. My call, high stakes.
- **Unclear**: you cannot tell what is being asked. This goes back to my supervisor, undrafted.

**Flag the collisions and the order.** Any two items that conflict, and any item that would
undo a decision recorded elsewhere in my document. Where one item cannot be settled until
another is (a rewritten hypothesis before the results that test it, new data before the table
that reports it), say so and put the blocking item first.

## Draft

Draft the smallest thing that meets the item, and never more. For each item that is not
unclear and not waiting on something I do not have, in the order the items appear in the
document: the new or replacement wording, the sentence to delete, the paragraph to move and
where to. Match the wording I already use, so an accepted edit still sounds like me and not
like a second writer.

**Where a genuinely different way exists, name it in one line beside the draft.** Not a menu
of three. One draft, plus one line saying what the other way would be, what it would cost me,
and what it would commit me to, where that other way is real: a smaller fix and a bigger one
that answer the comment differently, not two wordings of the same change. Where the smallest
change is the only sensible one, say nothing; an invented alternative is noise.

Three limits on what you write, and they matter more than the drafting itself.

- **One item, one small unit.** A draft is a sentence, or a few sentences at most. If an item
  seems to need a rewritten section, do not write the section: say what the section would
  have to do differently, and let me write it. A block of new prose is the thing I would
  accept without reading properly, which is how a supervisor's comment turns into someone
  else's paragraph in my thesis.
- **Say what you added.** Under each draft, list anything in it that was not in my document
  and not in the comment: a claim, a citation, a hedge that got stronger or weaker, a
  connective that asserts a relationship, a number. If the list is empty, say so. If it is
  not, I read the draft again.
- **Never hand me a block to paste.** Each draft is its own numbered proposal that I keep,
  reword, or reject on its own.

Where a draft cites a source that is not already in my document, confirm it exists in
Crossref, OpenAlex, or on the publisher's page, say where you checked, and list it as an
addition. Never cite from memory.

**Two kinds of item get no draft text, and each says why.** An item whose answer needs
something I do not have yet (new data, an analysis I have not run, a literature I have not
read, a decision only my supervisor can make, a change to my research question) is written as
a task instead: what has to happen first, roughly how long it takes, who decides, and what
the draft would depend on. An unclear item is written as a question for my supervisor, in the
words I should use. Guessing at wording for a change that rests on data I have not collected
would put a sentence in my document that nothing supports.

**The response record.** One line per item, in the numbering above: drafted, with the draft
number and where it goes; a task, with what it waits on; a question for my supervisor; or
blocked by another item, naming it. This is what I bring to the next supervision meeting, and
I fill in what I decided after I have been through the drafts.

## Audit

A reader that did not write the drafts checks them. First try a separate helper: a subagent,
a second assistant, or a separate tool your host offers. Give it only the feedback, the
numbered items, the drafts, and the response record, and ask it to report and fix nothing:
does every item have a draft, a task, a question, or a stated block; does every draft name
where it goes; did any draft go wider than its item; is everything a draft added listed under
it; does every citation a draft adds exist; and does the response record match the drafts. If
your tool cannot start a helper, run the same check yourself in a deliberately fresh pass and
say so at the hand-off. Fix what it found and nothing else; a second round rechecks only the
first round's list, and a third at most. Whatever is still contested after that comes to me
with both positions stated.

## Gate 2

Lead with the drafts and the response record, then a few lines, then the question.

- **The drafts and the response record**: save them as one Markdown file where your tool can
  write files, and say where it is; where it cannot, show them in full. Each draft is marked
  as a draft and not as a decision, with the place in my document it belongs, and with its
  one-line alternative underneath where one exists.
- **VERIFY, in a few lines**; I ask for the detail if I want it: how many items you found and
  how they split across the four kinds; what the audit found and who ran it; what changed in
  response; and what is still open: the items you did not draft and what each is waiting on,
  the questions for my supervisor, the collisions you flagged, and any item where you were
  unsure which way was smallest. An empty list is said out loud, not left implied.

Log the AI use: tool, date, purpose.

Then the question: for each draft, do I keep it, reword it, take the alternative, or reject
it? I go through them one at a time, and nothing is settled until I have. If I accept every
draft unchanged, say so plainly: that means I did not really read them. Update the response
record with my answers; it is the honest account of what I did with the advice.

CHECKPOINT: wait. Nothing is settled until I answer.

## Rules

- **Never decide whether a comment is correct.** Choosing how to meet a comment is your job.
  Judging whether the comment is right, and whether to act on it at all, is mine, and I do it
  at the hand-off with your draft in front of me.
- **Never quietly widen a change.** "Clarify this sentence" does not license rewriting the
  paragraph.
- **Never write prose I did not ask for.** Where an item can be met by cutting, by moving, or
  by a note to myself, propose that instead of new sentences. The less of my thesis you write,
  the better this worked.
- **Nothing enters my document before I say so.**
- **Never draft around a missing input.** An item waiting on data, a reading, or my supervisor
  stays undrafted and says so.
- If the feedback contradicts something I told you earlier, say so rather than choosing.
