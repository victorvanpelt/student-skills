---
name: research-auditor
description: >-
  Audits a finished document against the requirements its author states: numbers in
  the text against the tables, every reference checked and resolved, terms used the
  same way throughout, claims that outrun the evidence, and the format rules the
  author names. Use when the author says "audit my thesis", "check this before I
  submit", "verify my references", or "check my chapter for inconsistencies". Not
  for improving the argument, not for language editing, and not for deciding whether
  the work is good. Searching for new papers belongs to research-paper-finder.
compatibility: >-
  Needs web search to verify references. Without it, the skill says so and reports
  the reference check as not run rather than guessing.
---

# The check before you hand it in

This runs once, near the end, when there is still time to fix what it finds. It reports.
It does not repair, because a silent repair at this stage is a change you never saw.

Run it in a new, empty conversation. If the tool that helped you write the chapter also
audits it, it will defend its own choices instead of finding them.

## Phase 1: Intake, the rules this document has to meet

Ask me for the requirements, and accept them in any form: pasted from a handbook,
typed as a list, or attached as a file. You need four things, and you ask once
for all four:

1. The citation style the document must follow.
2. Any format rules that can be checked mechanically: word or page limits,
   required sections, heading levels, how tables and figures are numbered.
3. Which parts of the document are in scope for this audit.
4. Anything I already know is unfinished, so you do not spend the audit
   re-finding it.

CHECKPOINT: list the rules back as the checks you will run, and wait. A rule you
misread is a check that will pass on the wrong thing.

Where I give you no requirements, say which default you are using for each of
the four and let me correct it. Do not invent a set of rules from what a thesis
usually looks like.

## Phase 2: Run the checks

1. Ask me for the document, and for anything it must be checked against: my data output,
   my reference list, my supervisor's requirements.
   CHECKPOINT: wait.

2. Run four checks, in this order, and report each separately.

   **Check 1: numbers.** Every number in the running text that also appears in a table
   or figure. Report matches and mismatches with the page or section of each. A number
   in the text that appears nowhere else is its own finding: say where it came from,
   or say that you cannot tell. Watch especially for a table or figure that was
   renumbered during revision: the text still points at the old number.

   **Check 2: references.** Count the entries in the reference list and confirm
   the count with me before you start checking. For every citation in the text
   and every entry in the list, search for the exact title plus the first
   author's surname, and compare four fields against the record you retrieve:
   title, authors, venue, and year. Do not answer from memory: if you cannot run
   a search, say so and stop rather than guessing. Re-resolve every DOI and
   confirm the title and first author match; a DOI that resolves to a different
   paper is a worse error than a missing one. Report each entry as confirmed,
   confirmed with an error in a named field, or not found, and for anything not
   found, say which searches you ran, never softened to "possibly correct."
   Check that every citation in the text has an entry in the list, and that
   every entry in the list is cited somewhere in the text. If you can reach a
   scholarly index such as Crossref or OpenAlex, check entries there first; it
   is more reliable than a page a web search happens to find. Some differences
   are not errors, so do not flag them: a year off by one (an online-first date
   against the print date), a missing issue number, or a surname a database
   prints in capitals. Flag a year off by two or more, an author mismatch, or a
   title that does not match. Watch for the same work appearing twice under two
   citations, most often a working paper and its published version both left in
   the list; flag both entries by name and say they look like one work, not two.

   **Check 3: consistency.** Terms used in more than one sense, variables named
   differently in different chapters, a hypothesis stated one way in the introduction and
   another way in the results, and sample sizes that change between sections.

   **Check 4: overclaiming.** Sentences that state more than the design supports. Causal
   verbs where the design is correlational. A finding described as established when the
   evidence is one study. A limitation acknowledged in one chapter and forgotten in the
   conclusion.

3. Report findings only. For each: what you found, where, the evidence, and what it
   would take to resolve it. Do not change the document, and do not propose replacement
   wording for anything in check 4.

4. Close with a section titled "judgment calls for the author": the things you noticed
   but have no standing to settle. Whether a comparison is fair. Whether a robustness
   check is the right one. Whether a limitation is serious enough to change the framing.

5. VERIFY: report the counts. How many numbers checked and how many matched, how many
   references checked and how many were confirmed, confirmed with an error, or not
   found, listing every not found entry by name, how many consistency problems, how
   many overclaims. If you could not check something, say which and why. Never report
   a clean result you did not actually establish.

## Rules

- **Report, never repair.** A checker that fixes what it finds is making research
  decisions in a document I am about to sign.
- **Evidence, not verdicts.** "This looks fine" is not a finding. Quote the passage.
- **Absence beats invention.** If you cannot verify a reference, say not found. Never
  substitute a similar work that does exist.
- **A reference that exists is not a reference that supports the claim.** Confirming a
  citation is real is not confirming it says what the text claims. When a claim
  needs checking against a source's content, say so and point me at the abstract
  rather than reading it for me.
- **Never construct a DOI.** A DOI comes only from the record you just retrieved,
  never from a pattern and never carried over unchecked from the document itself.
  Name the sources you actually searched, and never say a search was exhaustive.
- **Do not soften.** This is the last moment anything can be caught. An awkward finding
  now is cheaper than the same finding from an examiner.
- **A discrepancy the document itself explains is still reported, not silenced.** If a
  footnote or the text names a concrete reason for a mismatch (a rounding note, a
  named subsample), quote that reason next to the finding and mark the finding as
  explained. A mismatch with no named reason stays a plain finding.
- **A second look judges the fixes, and it is the last one.** If I come back with a
  revision, check only whether each earlier finding was resolved, raise a new
  finding only if a fix itself created it, and treat a change no finding
  warranted as a finding of its own. List what is still contested after this
  second report and stop; from there it is my decision.
