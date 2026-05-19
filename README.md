# create-html skill

Convert any document into a polished, self-contained HTML file using 20 purpose-built presentation templates.

## Usage

```bash
/create-html <file>                        # auto-select template and convert
/create-html <file> --template 09          # force a specific template by ID
/create-html <file> --output out.html      # set the output filename
/create-html <file> --template 11 --output report.html
/create-html --list-templates              # print the 20-template catalog and exit
```

## How it works

1. Converts the input document to Markdown using `uvx markitdown` (supports PDF, DOCX, PPTX, XLSX, HTML, images, audio, ZIP, YouTube URLs, and plain text — no installation required)
2. Analyzes the Markdown content and auto-selects the most appropriate template from the library below
3. Confirms the chosen template with you before writing
4. Generates a fully self-contained HTML file (inline CSS + JS, no external dependencies)

## Templates

| ID | Display name | Best for |
|----|--------------|----------|
| 01 | Side-by-side code approaches | Comparing implementation options with trade-offs visible inline |
| 02 | Visual design directions | Showing layout, palette, or visual alternatives as rendered options |
| 03 | Annotated pull request | Presenting diffs with severity tags, jump links, and reviewer notes |
| 04 | Module map | Explaining unfamiliar code with boxes, arrows, hot paths, and entry points |
| 05 | Living design system | Rendering tokens, type scale, spacing, and component primitives as a browsable sheet |
| 06 | Component variants | Reviewing every size, state, and intent of a UI component in one place |
| 07 | Animation sandbox | Tuning motion, duration, easing, and interaction feel before implementation |
| 08 | Clickable flow | Testing a small multi-screen interaction with enough fidelity to feel the workflow |
| 09 | Arrow-key slide deck | Turning a memo or thread into a lightweight browser-native presentation |
| 10 | SVG figure sheet | Creating editable inline diagrams or illustrations for posts and docs |
| 11 | Weekly status report | Formatting shipped/slipped work, timelines, and small charts for fast scanning |
| 12 | Incident timeline | Presenting post-mortems with chronological events, logs, and follow-up checklists |
| 13 | Annotated flowchart | Showing a pipeline or process with clickable steps, timings, and failure paths |
| 14 | Feature explainer | Explaining a repo feature with TL;DR, collapsible paths, tabs, callouts, and FAQ |
| 15 | Concept explainer | Teaching an abstract concept with interactive visuals, comparison tables, and glossary |
| 16 | Implementation plan | Laying out milestones, data flow, inline mockups, risky code, and risk tables |
| 17 | PR writeup | Giving reviewers motivation, before/after context, file tour, and focus areas |
| 18 | Ticket triage board | Building a temporary drag-and-drop board that exports the resulting order |
| 19 | Feature flag editor | Editing grouped toggles with dependency warnings and copyable config diff |
| 20 | Prompt tuner | Editing prompt templates while sample inputs re-render live beside them |

Template taxonomy inspired by [HTML Effectiveness](https://thariqs.github.io/html-effectiveness/).

## Installation

<details>
<summary><strong>Claude Code</strong></summary>

```bash
# project-level (this project only)
cp SKILL.md .claude/commands/create-html.md

# global (available in every project)
cp SKILL.md ~/.claude/commands/create-html.md
```

Invoke with: `/create-html`

</details>

<details>
<summary><strong>OpenAI Codex</strong></summary>

Append the contents of `SKILL.md` to `AGENTS.md` in your repo root, or to `~/.codex/instructions.md` for global availability.

Invoke with: `codex "convert slides.pptx to html"`

</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

Append the contents of `SKILL.md` to `.github/copilot-instructions.md` in your repo.

Invoke by opening Copilot Chat and describing the task: "convert this document to a slide deck HTML file".

</details>

## Contributing

Open an issue or pull request. Keep commits atomic.

## License

MIT
