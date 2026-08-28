# student-skills

This repository contains simple skills that students writing a thesis or a research paper can use and develop further into skill workflows. A skill is a written procedure your AI tool follows when your request or task matches it. Each these skills does a single job by automating the boring stuff and keeping you in the loop for the important stuff. Each skill is a single folder you can copy anywhere; the folders follow the commonly-accepted [Agent Skills](https://agentskills.io) standard, so any capable tool can read them. Please note that these skills are bare-bone "starter" skills that serve as examples and starting points. Please use and modify them as you see fit.

## Skills as workflows

Each skill in this repo captures a particular workflow. It tries to automate the boring work that can be forgotten, while handing the important decisions and input to you. Some skills dispatch a second, independent auditor to improve quality of output if your AI tool allows it. Everything a skill needs is written in its folder; the only thing your AI tool has to do is import the folder's contents.

## The skills

- **research-proposal-drafter**: Asks the three Kinney questions, drafts a short proposal using your preliminary answers, works with you to improve it over at most three rounds, and then hands you a brief to audit it in a separate chat before your own final pass.
- **research-paper-finder**: Searches for papers on your topic, confirms every candidate against a second search, and drops what it cannot confirm rather than padding the list. Ships with **research-paper-auditor**, an independent field-by-field existence check on the results.
- **research-analysis-coder**: Gives you the code that computes a result based on data, never the result itself, so every number comes from a script you can run again.
- **research-section-drafter**: Turns your own bullets into sentences, one per bullet, and reports every claim, hedge, and magnitude it added. It hands you the sentences to adopt one at a time, never a finished paragraph to paste.
- **research-english-editor**: Copy-edits any academic document you wrote for grammar, spelling, punctuation, and US academic style, and hands it back with every change marked and numbered, so you reject the ones you do not want.
- **research-text-humanizer**: Quotes the phrasing in your text that reads as machine-written and leaves the rewriting to you, weighting the structural tells above the word list, which ages fast.
- **research-document-reviewer**: Reads any document you wrote (thesis, chapter, proposal, paper, essay) and reports where the argument does not hold, without rewriting a word.
- **research-feedback-reviser**: Splits supervisor comments, referee reports, or seminar notes into separate items, says what each one asks of your document, and lays out two or three ways of addressing each. Once you have chosen, it drafts the smallest change that meets each item, lists anything it added, and records your reasons for the ones you reject.
- **research-document-auditor**: Audits any finished document (thesis, chapter, proposal, paper, essay) against the rules you give it: every reference checked, resolved, and in APA 7 with a working DOI link, every claim and checkable fact against a source, numbers and statistics against the tables, terms used consistently, claims against evidence.
- **research-defense-questions**: Produces the questions your examiner will ask, grouped by research question, theory, design, data, results, limits, and contribution, then checks whether your own answers point at anything in your document.

## The shape they share

Most of these skills stop exactly twice and work on their own in between.

- **Gate 1** comes before the work. The skill says what it is about to do and what it
  understood from you, and waits. This is where a misread question is cheap to fix.
- **Gate 2** comes when the work is done. The skill hands you four things in one message,
  what it made, what it checked, what it changed, and what is still open, then asks you one
  question. Nothing counts as finished until you answer it.

Between the two gates the skill does not ask for confirmation, so you are not clicking
"yes" through work you have not read. The point of the gates is the opposite: they put your
judgment at the two places where it actually decides something.

Three skills are built differently, on purpose. **research-proposal-drafter** runs four
phases and stops after each one, because you and it improve the proposal together over up
to three rounds, and every round is a decision you make. **research-english-editor** stops
once, because every change it makes arrives unaccepted and you go through them at that one
stop. **research-document-auditor** ends by handing you its report rather than asking you a
question, because an audit is not something you approve. You act on it.

Three of these skills write prose for you, and each one is built so you cannot accept it
without reading it. The section drafter gives you one sentence per bullet. The feedback
reviser drafts the smallest change that meets a comment. The proposal drafter writes a
short whole proposal, but only out of answers you wrote yourself, and it marks what you
still have to decide instead of filling the gap. A finished paragraph is a paragraph you
will accept without reading it properly, and then it is in your thesis and you have to
defend it.

## How to install them

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

Any assistant with a custom-instructions or project field can still run a skill: paste everything below the frontmatter (the block between the two `---` lines at the top of `SKILL.md`) into that field, one skill per project. Where a skill would dispatch an auditor, run the auditor the same way in a separate, fresh chat, so the check comes from a context that did not produce the document.
