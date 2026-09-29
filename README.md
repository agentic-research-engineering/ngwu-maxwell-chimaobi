# A Philosophical Investigation into the Institutions of State in Francis Fukuyama's *The Origins of Political Order*

This repository contains the research record, chapter drafts, verification registers, audit trail, source material, and final human-review manuscript for Maxwell Chimaobi Ngwu's undergraduate Philosophy project.

The project examines how Francis Fukuyama explains the emergence, differentiation, interaction, and decay of the state, rule of law, and political accountability, and evaluates the philosophical adequacy of that framework.

> [!IMPORTANT]
> The human researcher remains the author. AI agents may assist with research, checking, formatting, and revision, but must not invent scholarship, citations, quotations, institutional wording, or personal details.

## Current status

- Substantive status: **FROZEN**
- Technical status: **READY FOR FINAL HUMAN REVIEW**
- Submission status: **NOT READY FOR SUBMISSION — HUMAN-SUPPLIED FRONT MATTER REMAINS**
- Review manuscript: `Ngwu-Maxwell-Chimaobi-Thesis-Final-Review.docx`
- Verified apparatus: 89 native Word footnotes and 28 bibliography entries
- Remaining human work: final submission date, approval page, certification, dedication, acknowledgements, and a Microsoft Word TOC refresh

Read `drafting/finalization/phase-5-completion-report.md` and `drafting/finalization/10-post-assembly-audit.md` before treating the manuscript as complete.

## Repository structure

```text
.
├── AGENTS.md                         # Mandatory instructions for AI agents
├── research-bible/                   # Governing question, method, claims, sources, and decisions
├── research/
│   ├── dossiers/                     # Section-level evidence dossiers
│   └── source-notes/                 # Source extraction and verification notes
├── drafting/
│   ├── chapter-01.md ... chapter-05.md
│   ├── plans/                        # Chapter and section plans
│   ├── audits/                       # Draft and whole-thesis audits
│   ├── integration/                  # Cross-chapter consistency records
│   └── finalization/                 # Phase 5 checks and DOCX builder
├── skills/                           # Repository-specific agent workflows
├── *.pdf                             # Local research copies of source texts
├── *.docx                            # Precedents, inherited manuscript, and review output
└── Ngwu-Maxwell-Chimaobi-Thesis-Final-Review.docx
```

The authoritative chapter structure is in `research-bible/03-table-of-contents.md`. Do not silently change it.

## Clone and work locally

### Requirements

- Git 2.23 or newer
- Python 3.10 or newer to rebuild the DOCX
- Microsoft Word or LibreOffice for opening and visually checking the manuscript

Clone the repository:

```bash
git clone https://github.com/agentic-research-engineering/ngwu-maxwell-chimaobi.git
cd ngwu-maxwell-chimaobi
```

Confirm the checkout:

```bash
git status
git log --oneline -5
```

This is a research and document project, not a web application. There is no server to start. The Markdown files can be opened in any editor, and the review manuscript can be opened directly in Word or LibreOffice.

## Rebuild the review DOCX

Create an isolated Python environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install python-docx lxml
```

On Windows PowerShell, activate the environment with:

```powershell
.venv\Scripts\Activate.ps1
```

Build the document:

```bash
python drafting/finalization/build_review_docx.py
```

The script writes:

```text
Ngwu-Maxwell-Chimaobi-Thesis-Final-Review.docx
```

After rebuilding:

1. Open the DOCX in Microsoft Word.
2. Select the table of contents and choose **Update entire table**.
3. Check Roman front-matter numbering and the Arabic restart at Chapter One.
4. Confirm that all 89 footnotes remain attached to the correct sentences.
5. Recheck the final bibliography and every visible `PENDING HUMAN-SUPPLIED` placeholder.
6. Do not call the file submission-ready until the human-supplied front matter is complete.

## Governing research workflow

Before changing research or prose, read:

1. `AGENTS.md`
2. `research-bible/00-project-charter.md`
3. `research-bible/03-table-of-contents.md`
4. `research-bible/05-source-hierarchy.md`
5. `research-bible/06-citation-and-evidence-rules.md`
6. The relevant dossier, claims, gaps, and decisions
7. The relevant workflow under `skills/`

The required evidence order is:

1. Primary texts
2. Peer-reviewed scholarship and scholarly monographs
3. Institutional sources
4. Scholarly reference works
5. General or tertiary sources for discovery only

Never guess a quotation, page number, DOI, author, publication detail, historical fact, or institutional statement. Use `[UNVERIFIED]` or `[CITATION NEEDED]` when the evidence is incomplete.

## Connecting an AI coding or research agent

All agents should be launched from the repository root so they can see the full project and its instructions:

```bash
cd ngwu-maxwell-chimaobi
```

Start every new agent with a bounded task. A useful first prompt is:

```text
Read AGENTS.md and the required Research Bible files before acting. Preserve the
authoritative table of contents, researcher authorship, evidence labels, citation
rules, and substantive freeze. Inspect the relevant dossiers and registers for
this task. Do not invent scholarship or modify unrelated files. First explain
what you intend to inspect, then make only the requested changes and report the
verification performed.
```

### OpenAI Codex

Install and launch the Codex CLI:

```bash
npm install -g @openai/codex
codex
```

You may also install it on macOS with `brew install --cask codex`. Codex automatically discovers repository `AGENTS.md` instructions. Open the cloned folder in Codex Desktop, an IDE integration, or start the CLI from the repository root.

Recommended first task:

```text
Read AGENTS.md and summarize the project status, evidence hierarchy, frozen
elements, and required verification workflow. Do not edit anything.
```

Official references: [Codex](https://developers.openai.com/learn/codex), [Codex CLI repository](https://github.com/openai/codex), and [AGENTS.md behavior](https://developers.openai.com/api/docs/guides/latest-model#using-agentsmd).

### Anthropic Claude Code

Install and launch Claude Code:

```bash
npm install -g @anthropic-ai/claude-code
claude
```

Claude Code automatically loads `CLAUDE.md`, not the repository's root `AGENTS.md`, as its native project-memory file. Until a dedicated `CLAUDE.md` adapter is added, begin each session with:

```text
Read AGENTS.md in full and treat it as the repository's mandatory project
instructions. Then read the Research Bible files it identifies. Do not edit yet.
```

Alternatively, create a short `CLAUDE.md` containing `@AGENTS.md` after reviewing it for conflicts. Keep platform-specific instructions thin so `AGENTS.md` remains the single governing source.

Official references: [Claude Code setup](https://code.claude.com/docs/en/getting-started) and [Claude project instructions](https://code.claude.com/docs/en/claude-directory).

### OpenCode

Install and launch OpenCode V2:

```bash
npm install -g @opencode/cli
opencode
```

OpenCode V2 recognizes `AGENTS.md` directly, so launching it from the repository root loads this project's instructions. Use `/connect` inside OpenCode to configure a supported model provider or account.

Official references: [OpenCode installation](https://opencode.ai/v2/docs) and [OpenCode instructions](https://opencode.ai/v2/docs/instructions).

### Google Gemini CLI

Install and launch Gemini CLI:

```bash
npm install -g @google/gemini-cli
gemini
```

Gemini CLI uses `GEMINI.md` for persistent project context. Until a dedicated adapter is added, explicitly ask Gemini to read `AGENTS.md` before working. If a `GEMINI.md` adapter is later added, keep it short and direct it to the governing repository files rather than duplicating their contents.

Official reference: [Gemini CLI installation](https://github.com/google-gemini/gemini-cli/blob/main/docs/get-started/installation.mdx).

### GitHub Copilot

Clone or open the repository in a Copilot-supported environment. GitHub Copilot CLI recognizes `AGENTS.md`; repository-wide Copilot instructions may also be added at `.github/copilot-instructions.md` if needed.

Do not duplicate the full research protocol across instruction files. Point any Copilot-specific file back to `AGENTS.md` and the Research Bible so the rules remain consistent.

Official reference: [GitHub Copilot custom instructions](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions).

### Other agentic platforms

For Cursor, Windsurf, Aider, Continue, Cline, Roo Code, or similar tools:

1. Clone the repository and open its root directory.
2. Give the agent read/write access only to this project.
3. Tell it to read `AGENTS.md` before acting.
4. If the platform has a native rules file, create only a small adapter that points to `AGENTS.md` and the required Research Bible files.
5. Keep shell and network actions approval-based.
6. Review diffs before committing or pushing.

Do not assume every platform automatically discovers `AGENTS.md`; verify its current documentation.

## Safe change workflow

Create a branch for each focused change:

```bash
git switch main
git pull --ff-only
git switch -c improve/<short-description>
```

Before editing, define:

- the exact research or formatting question;
- the files allowed to change;
- the evidence needed;
- what is explicitly out of scope;
- the checks required before completion.

Inspect changes frequently:

```bash
git status --short
git diff --check
git diff
```

Commit a coherent change:

```bash
git add <specific-files>
git commit -m "Describe the verified change"
git push -u origin improve/<short-description>
```

Then open a pull request and review:

- source-to-claim fit;
- quotations and locators;
- note-to-bibliography correspondence;
- changes to the thesis argument or conclusion;
- table-of-contents conformity;
- accidental removal of qualifications;
- formatting and rendered DOCX output;
- unexplained changes to binary source files.

Avoid committing directly to `main` for substantive work.

## How to improve the project

Prioritize improvements that are traceable and reviewable:

### Research quality

- Resolve remaining `[UNVERIFIED]`, `[CITATION NEEDED]`, P1, and P2 items through authoritative sources.
- Record new sources in `research-bible/16-bibliography-register.md`.
- Record claims in `research-bible/09-claims-register.md` and quotations in `research-bible/15-quotation-ledger.md`.
- Preserve disagreement and uncertainty instead of forcing a false consensus.

### Argument quality

- Distinguish exposition, reconstruction, comparison, analysis, and evaluation.
- Test whether each conclusion follows from the evidence actually cited.
- Keep state, state capacity, government, rule of law, accountability, democracy, development, and decay conceptually distinct.
- Challenge universal claims with the strongest relevant historical counterexamples.

### Citation quality

- Verify every quotation against the correct edition.
- Prefer stable chapter, section, or printed-page locators.
- Ensure every footnote source appears in the bibliography and every bibliography entry is used.
- Do not transfer pagination between editions or cite extracted-PDF pages as printed pages.

### Document quality

- Make textual changes in the Markdown source before rebuilding the DOCX.
- Treat the generated review DOCX as an output, not the primary editable source.
- Render and inspect the complete DOCX after any assembly change.
- Recheck footnotes, page breaks, pagination, italics, bibliography wrapping, and TOC fields.

### Agent quality

- Give agents one bounded task at a time.
- Ask for evidence-backed findings before authorizing edits.
- Require a file list and verification report after changes.
- Use read-only review agents to audit work produced by editing agents.
- Never let an agent silently broaden scope, replace the researcher's judgment, or declare submission readiness.

## High-risk files and actions

- Do not overwrite the five chapter Markdown files without reviewing the diff.
- Do not change `research-bible/03-table-of-contents.md` without explicit researcher approval.
- Do not replace the verified bibliography with an inherited preliminary bibliography.
- Do not fabricate approval, certification, dedication, acknowledgement, signatory, or date content.
- Do not delete source PDFs or inherited DOCX files merely because duplicates appear to exist; first consult the source-identity records.
- Do not commit API keys, access tokens, cookies, local `.env` files, or private credentials.

The included source files may be subject to copyright or licensing restrictions. Keep the repository private unless the human researcher has confirmed that every source file may lawfully be redistributed.

## Suggested agent tasks

Good tasks:

```text
Audit Chapter Four footnotes against the source-verification register. Report
problems only; do not edit.
```

```text
Check whether a proposed paragraph repeats existing analysis. Read the relevant
chapter, argument map, and repetition audit before recommending a change.
```

```text
Rebuild the review DOCX from the frozen Markdown, render it, and report any
layout regression without changing thesis prose.
```

Unsafe or underspecified tasks:

```text
Improve the whole thesis.
```

```text
Add more citations wherever needed.
```

```text
Make it submission ready.
```

Replace broad requests with a defined section, evidence standard, file scope, and acceptance test.

## License and authorship

No open-source license is currently declared. All manuscript prose, research notes, source files, and compiled documents remain subject to their respective authorship, copyright, and licensing terms. Contact the repository owner before reuse or redistribution.
