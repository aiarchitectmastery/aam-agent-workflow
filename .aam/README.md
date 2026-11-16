# .aam/ — the AAM reference Agent Harness

`.aam/` holds the reusable part of the AAM Agent Workflow: the procedure,
the templates and the prompts. Your project's own work (PRDs, PLANs, TASKs and
review records) goes in [agent-workflow/](../agent-workflow/README.md), not here.

| Folder | What it contains | How you use it |
|---|---|---|
| [workflows/](workflows/core-workflow.md) | The core workflow: PRD → PLAN → TASK → IMPLEMENTATION, with human checkpoints | Read it once; follow it for every piece of work |
| `templates/` | Starting structures for PRD, PLAN, TASK and a bounded task, plus the IMPLEMENTATION review checklist | Copy a template into `agent-workflow/` and fill it in. A template is not itself a work product |
| `prompts/` | Prompts a human runs deliberately: fresh-session handoff and agent guidance review | Paste them into your AI chat when the situation calls for them |

## What `.aam/` is not

- **Not runtime-enforced.** These are plain Markdown files. They do not grant,
  restrict or check agent permissions. Use your environment's own permission
  controls and review every result.
- **Not loaded automatically.** An agent reads these files when you or your
  instructions reference them.
- **Not a complete harness.** This release contains only the folders above.
  Later releases add folders only when they have content.

The structure follows the AAM reference project layout: `.aam/` for the
harness, `agent-workflow/` for project work products, and your own source code
alongside them.
