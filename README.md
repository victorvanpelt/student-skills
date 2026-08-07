# student-skills

Skills for students writing a thesis or a research paper with the help of an AI tool. A skill is a written procedure your AI tool follows when your request matches it. Each skill here does a single job, stops to ask you something, and ends by reporting what it did and could not do. Each one is a single folder you can copy anywhere; the folders follow the [Agent Skills](https://agentskills.io) standard, so any capable tool can read them.

## Skills as workflows

Each skill is a workflow, not a chat trick. It automates the careful, boring work (searching twice, checking every reference, listing every change it made) and hands the judgment calls back to you: the workflow stops where a decision is yours and reports what it could not verify. Some skills dispatch a second, independent helper to audit the result, because a tool checking its own work in the same conversation tends to approve it. Everything a skill needs is written in its folder; the only thing your AI tool has to do is read a `SKILL.md` file.

## The skills

**Start the project**
- **research-proposal-drafter**: Asks the three questions every researcher has to answer, then builds a proposal from your answers alone. Ships with **research-proposal-auditor**, an independent check on the draft: unsupported claims, language, references, checkable facts.

**Work with the literature**
- **research-paper-finder**: Searches for papers on your topic, confirms every candidate against a second search, and drops what it cannot confirm rather than padding the list. Ships with **research-paper-auditor**, an independent field-by-field existence check on the results.

**Analyze the data**
- **research-analysis-coder**: Gives you the code that computes a result, never the result itself, so every number comes from a script you can run again.

**Write**
- **research-section-drafter**: Turns your own bullets into prose and reports every claim, hedge, and magnitude it added.
- **research-english-editor**: Returns a numbered list of language corrections you accept or reject one by one; it never edits the document itself.
- **research-text-humanizer**: Quotes the phrasing in your text that reads as machine-written and leaves the rewriting to you.

**Check and defend**
- **research-reviewer**: Reads a chapter you wrote and reports where the argument does not hold, the way a marker would, without rewriting a word.
- **research-feedback-reviser**: Splits supervisor comments into separate items and applies only the ones you accept, recording your reasons for the ones you reject.
- **research-auditor**: Audits the finished document against the rules you give it: numbers against tables, every reference checked and resolved, terms used consistently, claims against evidence.
- **research-defense-questions**: Produces the questions your examiner will ask, grouped by chapter, then checks whether your own answers point at anything in your document.

## How to install them

First get the files: clone the repository with git, or download it as a zip from GitHub (Code > Download ZIP) and unpack it. Every skill is one self-contained folder; take only the ones you want.

**In the Claude app (web or desktop):**
1. Zip one skill folder, with the folder itself as the top level inside the zip.
2. In Claude's settings, make sure code execution and file creation are turned on, then open the Skills section and upload the zip.
3. Repeat for each skill you want. Then ask for the task in any chat; if Claude answers without using the skill, name it ("use research-paper-finder").

**In a CLI (a tool that runs in your terminal, such as Claude Code):**
1. Copy the skill folder into the tool's skills directory, for example `~/.claude/skills/research-proposal-drafter/`.
2. If the folder contains a second `.md` file, that is an agent definition; copy it into the agents directory, for example `~/.claude/agents/research-proposal-auditor.md`.
3. Restart the tool and ask for the task.

## If your tool does not install skills

Any assistant with a custom-instructions or project field can still run a skill: paste everything below the frontmatter (the block between the two `---` lines at the top of `SKILL.md`) into that field, one skill per project. Where a skill would dispatch an auditor, run the auditor the same way in a separate, fresh chat, so the check comes from a context that did not produce the document.
