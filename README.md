# student-skills

Light-weight skills that students writing a thesis or a research paper can use and develop further into skill workflows. A skill is a written procedure your AI tool follows when your request matches it. Each skill here does a single job, stops to ask you something, and ends by reporting what it did and could not do. Each one is a single folder you can copy anywhere; the folders follow the [Agent Skills](https://agentskills.io) standard, so any capable tool can read them. Please note that these skills are bare-bone "starter" skills that serve as examples. Students can use them and tailor them to their own needs. The skills also follow WHU's principles for Responsible AI use.

## Skills as workflows

Each skill in this repo captures a particular workflow. It tries to automate the careful, boring work, while handing the important decisions and judgments to you. Some skills dispatch a second, independent auditor to improve quality of output, because a tool checking its own work in the same conversation tends to approve it or miss things. Everything a skill needs is written in its folder; the only thing your AI tool has to do is import the folder's contents.

## The skills

- **research-proposal-drafter**: Asks the three questions every researcher has to answer, then builds a proposal from your answers alone. Ships with **research-proposal-auditor**, an independent check on the draft: unsupported claims, language, references, checkable facts.
- **research-paper-finder**: Searches for papers on your topic, confirms every candidate against a second search, and drops what it cannot confirm rather than padding the list. Ships with **research-paper-auditor**, an independent field-by-field existence check on the results.
- **research-analysis-coder**: Gives you the code that computes a result based on data, never the result itself, so every number comes from a script you can run again.
- **research-section-drafter**: Turns your own bullets and outline into prose and reports every claim, hedge, and magnitude it added.
- **research-english-editor**: Returns a numbered list of language corrections you accept or reject one by one.
- **research-text-humanizer**: Quotes the phrasing in your text that reads as machine-written and leaves the rewriting to you.
- **research-reviewer**: Reads a chapter you wrote and reports where the argument does not hold, without rewriting a word.
- **research-feedback-reviser**: Splits supervisor comments into separate items and applies only the ones you accept, recording your reasons for the ones you reject.
- **research-auditor**: Audits the finished document against the rules you give it: numbers against tables, every reference checked and resolved, terms used consistently, claims against evidence.
- **research-defense-questions**: Produces the questions your examiner will ask, grouped by research question, theory, design, data, results, limits, and contribution, then checks whether your own answers point at anything in your document.

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
