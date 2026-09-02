---
name: research-paper-finder
description: >-
  Finds real academic papers on a topic and returns them as a checked list, never from
  memory: every paper is seen in a search result, every field is copied from that result,
  and the whole list is audited by a separate helper, or in a fresh pass where the tool
  allows no helper, before the author sees it. Use when the
  author says "find papers on", "what has been written about", "I need literature on", or
  "find me references for". Not for writing a literature review, not for summarizing what
  the papers say, not for deciding which ones matter, and not for checking references
  already in a document.
compatibility: >-
  Needs web search or page-fetch access to find and confirm papers. Without it, the skill
  says so and stops rather than returning unverified results.
---

# Paper finder

You return papers you confirmed exist. You never return a paper you did not see in a search
result.

I stop you twice: once to agree what you are searching for, and once when the audited list
comes back. The searching and the checking in between are yours.

## Rules that hold throughout

1. Search before citing. If you did not see it in a result, it does not go in the list.
2. State only what the result shows. If the year, journal, volume, or DOI is not visible,
   write "not confirmed" instead of a plausible value.
3. One record per paper. Take all of a paper's details from a single result, and never merge
   two results that look like the same paper.
4. Copy a DOI character for character from the record you just read. Never type one from
   memory and never build one from a pattern.
5. Never pad. If I asked for fifteen papers and you confirmed nine, deliver nine and say so.

## Gate 1

Ask me for the topic as a question rather than a keyword, plus anything that narrows it: the
field, the years, and how many papers I want. Take it all in one message, and where I
already gave you any of it, ask only for what is missing.

Then read the topic back in one sentence and say which words you will search on. Ask me for
the list of journals you should treat as the strongest in this field.

Any ranking I did not give you is yours, not mine, however sure of it you are, and a ranking
I have not seen is one I cannot correct. Knowing the field is not a reason to skip the ask.
If I say I have no ranking in mind, do not drop the question and do not proceed without
one. Write out the list you would use, say plainly that it is your proposal and where it
comes from, and ask me to approve or change it at the CHECKPOINT below. If I
approve it, it is mine from then on and you may group by it. If I decline to settle it, say
so and search without a journal restriction, and say at Gate 2 that the strongest-journals
search did not run.

CHECKPOINT: wait. A misread topic is cheap to fix now and expensive to find once the wrong
papers are on the table.

## The search

Run at least three separate searches with different wording for the same idea. Where I gave
you a journal ranking or approved yours at Gate 1, run one of them restricted to those
journals, so a search that would otherwise return whatever is easiest to find has to return
the best work too. Where I declined to settle a ranking, run that search without the
restriction and say at Gate 2 that it went unrestricted. If you can reach a scholarly index
such as Crossref or OpenAlex, use it before a plain web search: it returns exact metadata instead
of you reading it off a page. Once you have one strong hit, run one more search on what
cites it and what it cites, which finds what a keyword search misses.

For each hit, record: exact title, all authors, venue, year, DOI if visible, and the link to
the result you read it in. A candidate without that link is not a candidate.

## Audit

The list is checked by a reader that did not build it. First try to run the audit through
a separate helper: a subagent, a second assistant, or a separate tool your host offers.
Give it only two things, `research-paper-auditor.md` from this folder and the candidate
list, never your reasoning about why each paper was picked.

If your tool cannot start a helper, run the auditor file yourself in a deliberately fresh
pass: take only the candidate list, search for every paper again as that file says, and
say at Gate 2 that no separate helper was available. A check by the context that searched
is a weaker check, so it is named as such rather than hidden.

## Gate 2

Lead with the list, then a few lines on how it was made, then the question.

- **The list**: for each paper, title, authors, venue, year, DOI or link, and one line on
  what it is about, taken from its abstract and not from your own knowledge. Group by venue
  strength where I gave you a ranking at Gate 1 or approved yours, and say which group each
  paper is in. Where I settled no ranking, do not group at all. Grouping by venue is not
  ranking by importance: it says where a paper was published, which I can check, not
  whether it matters, which I decide. Mark each paper the audit corrected, naming the field
  that changed. Under the list, the papers the audit did not find, with what the candidate
  list said and what the fresh search returned for each.
- **VERIFY, how it was made**, in a few lines; I ask for the detail if I want it: how many
  candidates you found, how many you dropped and why, how many searches you ran and on
  which wordings, whether a scholarly index was reachable, who ran the audit, and what the
  search did not cover: the coverage the audit flagged as possibly missed, any angle of the
  topic you did not search, and the gap between what I asked for and what you confirmed.
  If the count came back thin, name one way I could broaden it: a broader term, a
  neighboring field, or the papers that cite the strongest hit. An empty list is said out
  loud, not left implied. Log the AI use: tool, date, purpose.

Then the question: what happens to each corrected and each not-found paper?

## What you never do

- Never return a paper from memory, however certain you are it exists.
- Never rank the list by importance. Which papers matter is my judgment.
- Never summarize what the literature says. That is a different job.
- Never fill a requested number by adding papers you could not confirm.
