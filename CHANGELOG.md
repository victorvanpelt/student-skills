# Changelog

Every skill folder carries its own version in the `metadata.version` field of its
`SKILL.md`. This file records what changed in each release, so a skill copied earlier
can be compared against the current one.

## 1.0.1, 2026-09-08

- **research-english-editor**: `compatibility` added to the frontmatter. The skill needs a host
  that can write Word tracked changes into a .docx, and said so only in its body text, where a
  host program reading the frontmatter could not see it.
- **README**: the plain-text route no longer tells you to open a second chat and paste the work
  in. Every skill already handles a missing helper itself, by running the same check in a fresh
  pass and saying that is what it did. The README now says that, so the README and the ten
  skills give one answer instead of two.

## 1.0.0, 2026-09-08

First versioned release. All ten skills and the bundled `research-paper-auditor`.

Changed in this release:

- **research-document-reviewer**: the defender pass moved out of the helper and into the
  skill itself, as a deliberately separate pass, with four refutation questions and a kill
  log shown at Gate 2. Deciding whether a comment survives is a judgment, and a helper
  that kills a real concern removes the comment the author most needed.
- **research-document-auditor**: the second reader now answers four numbered questions and
  compares each severity against the three definitions the skill states, instead of judging
  whether a severity is fair. Adjusting a severity is the skill's call, reported at Gate 2.
- **research-proposal-drafter**: the audit split into two passes. A helper checks that the
  references resolve, that their form is right, that citations and list entries match, and
  that the checkable facts hold. Claim support, academic English, and AI slop moved to a
  separate pass by the skill, because judging how a draft reads is not a lookup. The helper
  no longer proposes replacement wording outside a corrected reference entry.
- **research-defense-questions**: the second reader reports an ungrounded question and
  changes nothing. The skill does the dropping and reports every drop at Gate 2.
- **Nine skills**: the second stop is now marked with CHECKPOINT, so both promised stops
  are labelled. research-english-editor is unchanged here: it designs one stop and says so.
- **Every skill**: `license` and `metadata.version` added to the frontmatter.
- **Repository**: LICENSE file added (CC BY 4.0).
