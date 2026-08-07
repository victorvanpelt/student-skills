# student-skills

Skills for students writing a thesis or a research paper with the help of an AI tool. A skill is a written procedure your AI tool follows when your request matches it. Each skill here does a single job, stops to ask you something, and ends by reporting what it did and could not do. Each one is a single folder you can copy anywhere; the folders follow the [Agent Skills](https://agentskills.io) standard, so any capable tool can read them.

They are ordered below by when you reach for them in a project, and each skill lives in the folder named in its table row.

## The skills

**Your first skill**

| Folder | What it does |
|---|---|
| `research-english-editor/` | Returns a numbered list of language corrections you accept or reject one by one, and never edits the document itself |

**After feedback**

| Folder | What it does |
|---|---|
| `research-feedback-reviser/` | Splits supervisor comments into separate items, classifies each, and applies only the ones you accept, keeping your reasons for the ones you reject |

**Starting the project**

| Folder | What it does |
|---|---|
| `research-proposal-drafter/` | Asks you the three questions every researcher has to answer, then builds a proposal from your answers alone. Dispatches the auditor below |
| `research-proposal-auditor` | The independent check on that draft: claims that came from nowhere, language, references, checkable facts. Ships inside the drafter's folder |

**Working with literature**

| Folder | What it does |
|---|---|
| `research-paper-finder/` | Searches for papers on your topic, checks every candidate against a second search, drops what it cannot confirm, and never pads the list to a requested number. Dispatches the auditor below |
| `research-paper-auditor` | The independent check on that search: does each paper exist, checked field by field against a fresh search. Ships inside the finder's folder |

**Analysis**

| Folder | What it does |
|---|---|
| `research-analysis-coder/` | Gives you the code that computes a result and refuses to give you the result, so every number comes from a script you can run again |

**Writing**

| Folder | What it does |
|---|---|
| `research-section-drafter/` | Turns your own bullets into prose and reports every claim, hedge, and magnitude it added |
| `research-text-humanizer/` | Finds the phrasing in your writing that reads as machine-written, quotes it, and leaves the rewriting to you |
| `research-reviewer/` | Reads a chapter you wrote and reports where the argument does not hold, the way a marker would, without rewriting a word |

**Before you hand it in, and before you defend**

| Folder | What it does |
|---|---|
| `research-auditor/` | Audits your document against the rules you give it: numbers against tables, every reference checked and resolved, terms used consistently, and anything claiming more than the evidence supports |
| `research-defense-questions/` | Produces the questions your examiner will ask, grouped by chapter, then checks whether your own answers point at anything in your document |

## Getting the files

Download this repository as a zip (the green Code button, then Download ZIP) and unpack it, or clone it with git if you use git. Either way you end up with the skill folders on your machine. Every skill works alone and every combination works, so take only the folders you want.

## Installing in the web or desktop app

Claude installs these as real skills, with no software and no copying. Do this first, because it is the version the files were written for.

1. In settings, turn on code execution and file creation. Skills run there, so without it the skills section stays empty.
2. Compress one skill folder into a zip. The folder itself has to be the top level inside the zip, not the files loose and not a folder wrapping it. The repository zip from the step above does not work here; it wraps everything in one outer folder.
3. In settings, open the skills section, add a skill, and upload the zip.
4. Start any chat and type the trigger sentence from the file's `description` line, for example "draft my thesis proposal".

Installed this way, the skills sit side by side and the tool picks the one your sentence matches. The part between the two lines of dashes at the top of each `SKILL.md` is called frontmatter, and this is what reads it.

If a request is something the tool can already do in one step, it may answer without reaching for the skill at all. That is the most common first run. Name the skill in your message when it happens.

## Installing in a CLI

A CLI is the version of the tool that runs in your terminal, such as Claude Code.

1. Copy the whole skill folder into your tool's skills directory, for example `~/.claude/skills/research-proposal-drafter/`.
2. Copy any agent definition file (the ones that are not `SKILL.md`) into your tool's agents directory, for example `~/.claude/agents/research-proposal-auditor.md`.
3. Restart the tool, then type the trigger sentence.

## If your tool does not install skills

Gemini's Gems and any assistant with a custom-instructions box take the text instead. Open the `SKILL.md` file, copy everything below the two lines of dashes, and paste it into the instructions field. Then start a chat there and type the trigger sentence.

One skill per project this way. A project holding three procedures will blend them, which is the limitation the upload route removes.

Where a procedure dispatches an auditor, a pasted-in project cannot start a second, separate helper. Do the audit yourself in a fresh chat instead: open a new chat without the project, paste everything below the two lines of dashes in the auditor file, add the two documents it asks for, and read what comes back. A new chat is a fresh context, which is the property that makes the check worth running.

Three skills are built to run in a fresh chat for exactly that reason, whatever tool you use: `research-proposal-auditor`, `research-paper-auditor`, and `research-auditor`. Do not run any of them in the conversation that produced the document it is checking.

## Changing them

These files are starting points, not fixed rules. After each run, note what went wrong: a step the tool misread, a check that was missing, a question it should have asked. Edit the file. The next run inherits the fix, which is the whole advantage of writing a procedure down instead of retyping a request.

Two edits are worth making early, once you have used one a few times. Sharpen the `description` line until it matches the words you actually type, because that line decides whether the procedure ever runs. And move the checkpoint to wherever you found yourself wishing the tool had stopped.
