# student-skills

This repository contains simple skills that students writing a thesis or a research paper can use and develop further into skill workflows. A skill is a written procedure your AI tool follows when your request or task matches it. Each of these skills does a single job by automating the boring stuff and keeping you in the loop for the important stuff. Each skill is a single folder you can copy anywhere; the folders follow the commonly-accepted [Agent Skills](https://agentskills.io) standard, so any capable tool can read them. Please note that these skills are bare-bone "starter" skills that serve as examples and starting points. Please use and modify them as you see fit.

## Skills as workflows

Each skill in this repo captures a particular workflow. It tries to automate the boring work that can be forgotten, while handing the important decisions and input to you. Every skill takes what you already gave it and asks only for what is missing, has its output checked by a second reader (a separate helper where your AI tool can start one, or the same assistant in a fresh pass where it cannot), and then hands you the output first, with the checks in a few lines and one question. You always get a stop at the end. Nothing is settled until you answer.

Whether you also get a stop at the *start* depends on the job, and each skill says which it is. Five of them say back what they understood your request to be, in five short parts, and wait before doing anything: the proposal drafter, the document reviewer, the feedback reviser, the analysis coder, and the defense questions. Those jobs all rest on reading what you asked for, so a misreading wastes the whole run and is cheap to fix in one line at the start. The other five do not stop, because their work runs against something fixed that already exists: your own bullets, your own tables and reference list, a search result, or a printed list of rules. There is nothing there to misread, so a stop would cost you a wait and buy nothing. Those five are the document auditor, the English editor, the paper finder, the section drafter, and the text humanizer. Each still asks for what it cannot start without, and that ask is not a gate.

Everything a skill needs is written in its folder; the only thing your AI tool has to do is import the folder's contents.

**On journal rankings.** The paper finder asks you which journals count as strongest in your field, and asks for your supervisor's or department's list first, because that is the one your thesis is actually judged against. If you have none, it offers the Financial Times 50 as a starting point. The FT50 is a public list of fifty journals the *Financial Times* uses to rank business schools. It is one list among several, it leans toward business and economics, and plenty of good work appears outside it. Approve it, change it, or tell the skill to search without any journal restriction.

## The skills

- **research-proposal-drafter**: Asks the three Kinney questions (what you want to find out, why it matters and to whom, how you will find out), drafts a short proposal from your preliminary answers, finds and checks the references the argument needs, names the three changes that would most improve it, runs an audit through a separate helper where your tool allows one, and hands you the proposal as a Markdown file with those three comments for your final pass.
- **research-paper-finder**: Searches for papers on your topic, confirms every candidate against a second search, and drops what it cannot confirm rather than padding the list. Checks itself for the obvious miss before it hands over. Ships with **research-paper-auditor** in its `references/` folder, an independent field-by-field existence check on the results.
- **research-analysis-coder**: Gives you the code that computes a result based on data, never the result itself, so every number comes from a script you can run again.
- **research-section-drafter**: Turns your own bullets into sentences, one or two per bullet, and reports every claim, hedge, and magnitude it added. It hands you the sentences to adopt one at a time, never a finished paragraph to paste.
- **research-english-editor**: Copy-edits any academic document you wrote for grammar, spelling, punctuation, and US academic style, and hands it back with every change marked and numbered, so you reject the ones you do not want.
- **research-text-humanizer**: Quotes the phrasing in your text that reads as machine-written and leaves the rewriting to you, weighting the structural tells above the word list, which ages fast.
- **research-document-reviewer**: Reads any document you wrote (thesis, chapter, proposal, paper, essay) and writes a referee-style review, three main comments and up to twenty minor ones, each anchored to a quoted sentence, without rewriting a word.
- **research-feedback-reviser**: Splits supervisor comments, referee reports, or seminar notes into separate items, says what each one asks of your document, then drafts the smallest change that meets each one and lists anything it added. Items waiting on data you do not have, and items nobody can interpret, get a task or a question for your supervisor instead of invented wording. You keep, reword, or reject each draft at the end, and it keeps a one-line record per item for your next supervision meeting.
- **research-document-auditor**: Audits any finished document (thesis, chapter, proposal, paper, essay) against the rules you give it: every reference checked, resolved, and in APA 7 with a working DOI link, every claim and checkable fact against a source, numbers and statistics against the tables, terms used consistently, claims against evidence. Every finding carries a severity.
- **research-defense-questions**: Produces the questions your examiner will ask, grouped by research question, theory, design, data, results, limits, and contribution, then checks whether your own answers point at anything in your document. Questions your thesis cannot answer are kept in a section of their own rather than dropped, because those are the ones you most need to see coming.

## Installation instructions

First get the files: clone the repository with git, or download it as a zip from GitHub (Code > Download ZIP) and unpack it. Every skill is one self-contained folder. You can either copy all of them or only the ones you want.

**In the Claude app (web or desktop):**

1. Zip one skill folder, with the folder itself as the top level inside the zip.
2. In Claude's settings, you can upload the zip in the skills section.
3. To use, start the task in any chat. If Claude answers without using the skill, name it explicitly (e.g., "use research-paper-finder").

**In a CLI (a tool that runs in your terminal, such as Claude Code):**

1. Copy the skill folder into the tool's skills directory, for example `~/.claude/skills/research-proposal-drafter/`.
2. If you are unsure where your skills are supposed to be located, open a chat in the terminal and ask your agent to install the skill using the path to where your zip is located.
3. Restart the tool and start the task or name the skill explicitly.

## If your tool does not install skills

Any assistant with a custom-instructions or project field can still run a skill: paste everything below the frontmatter (the block between the two `---` lines at the top of `SKILL.md`) into that field, one skill per project. Where a skill folder has a `references/` directory, paste those files in too, or keep them to hand: the paper finder points its second reader at `references/research-paper-auditor.md`. Where a skill would hand its output to a separate helper, you do nothing: the skill notices that no helper is available, runs the same check itself in a fresh pass, and tells you it did. That fallback is written into every skill, so the check still happens on the plain-text route.

## Versions

Each skill carries a version in its `SKILL.md` frontmatter, under `metadata: version`. What changed between versions is in [CHANGELOG.md](CHANGELOG.md) at the top of this repository. If you copied a skill folder some time ago, compare its version against the one here before you assume they still do the same thing.

## License

These skills are licensed under [CC BY 4.0](LICENSE). Copy them, change them, use them in your own work, including commercially. The one condition is credit: name the source, link the license, and say if you changed anything.

> van Pelt, V. (2026). student-skills: starter research skills for thesis students [Agent Skills repository]. https://github.com/victorvanpelt/student-skills Licensed under CC BY 4.0.
