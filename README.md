# AAM Agent Workflow

A free, versioned template for the **AI Driven Development Methodology**:
PRD → PLAN → TASK → IMPLEMENTATION, with the human as the final gate at every
step. Your repository, your rules — human as architect, AI as builder.

---

## What this is

The AAM Agent Workflow is a set of plain Markdown files that live in your own
repository: a core workflow, templates for each phase, an IMPLEMENTATION review
checklist and reusable prompts. It turns ad hoc AI usage into a structured,
reviewable way of working with AI coding agents (sometimes called *structured
Vibe Coding*). It works with GitHub Copilot and with other AI agents that can
read files in your repository.

**What it is not:**

- Not an agent, installer or tool to configure. You copy files; nothing runs.
- Not a runtime control. The files do not enforce permissions — use your
  environment's permission controls.
- Not a guarantee of correctness or productivity. Quality still depends on the
  task, your verification and your judgment.

## What's inside

```text
.
├── .aam/                              ← the reusable workflow (reference harness)
│   ├── README.md
│   ├── workflows/core-workflow.md     ← start here: the procedure
│   ├── templates/
│   │   ├── PRD-template.md
│   │   ├── PLAN-template.md
│   │   ├── TASK-template.md
│   │   ├── bounded-task-template.md
│   │   └── IMPLEMENTATION-checklist.md
│   └── prompts/
│       ├── fresh-session-handoff.md
│       └── agent-guidance-review-prompts.md
└── agent-workflow/                    ← your own PRDs, PLANs and TASKs go here
    └── README.md
```

| File | Purpose |
|---|---|
| [core-workflow.md](.aam/workflows/core-workflow.md) | The four phases, six steps and mandatory human checkpoints |
| [PRD-template.md](.aam/templates/PRD-template.md) | Capture intent, scope, constraints and acceptance criteria |
| [PLAN-template.md](.aam/templates/PLAN-template.md) | Turn an approved PRD into ordered tasks with checkpoints |
| [TASK-template.md](.aam/templates/TASK-template.md) | Delegate one bounded task with context, constraints and verification |
| [bounded-task-template.md](.aam/templates/bounded-task-template.md) | A short brief plus a read-only gap check before any edits |
| [IMPLEMENTATION-checklist.md](.aam/templates/IMPLEMENTATION-checklist.md) | The human review before anything merges, with an evidence-based verdict |
| [fresh-session-handoff.md](.aam/prompts/fresh-session-handoff.md) | Move work to a fresh conversation without losing verified context |
| [agent-guidance-review-prompts.md](.aam/prompts/agent-guidance-review-prompts.md) | Review existing agent instructions one approved change at a time |

Looking for the prompts from the AAM agent-guidance demo video? They are in the
appendix of [agent-guidance-review-prompts.md](.aam/prompts/agent-guidance-review-prompts.md#appendix-the-exact-prompts-from-the-aam-agent-guidance-demo).

---

## Get started

Choose one of three ways. None of them needs an installer.

### 1. New project: use this template

On GitHub, select **Use this template → Create a new repository**. Leave
**Include all branches** unchecked: only `main` contains released content.

Or with the [GitHub CLI](https://cli.github.com/):

```bash
gh repo create my-project --template aiarchitectmastery/aam-agent-workflow --private --clone
```

### 2. Existing project: copy two folders

Copy `.aam/` and `agent-workflow/` into the root of your repository.

If either folder already exists in your project, **do not overwrite it**.
Copy only the files that are missing and compare the rest by hand:

```bash
# from the root of your project; -n never overwrites an existing file
mkdir -p .aam agent-workflow
cp -Rn /path/to/aam-agent-workflow/.aam/. .aam/
cp -Rn /path/to/aam-agent-workflow/agent-workflow/. agent-workflow/
```

Review the result with `git status` before you commit anything. On some
systems `cp -n` reports a non-zero exit status when it skips an existing file;
that is expected. Files you kept are not updated, so compare them with the
template version yourself.

### 3. ZIP

Download the ZIP from the [latest release](../../releases/latest) and copy the
folders as in option 2.

---

## Your first cycle

Pick one small, real change in your project and plan for a short session.

1. Read [core-workflow.md](.aam/workflows/core-workflow.md).
2. Copy [PRD-template.md](.aam/templates/PRD-template.md) to
   `agent-workflow/prd/`, fill it in for the change and approve it yourself.
3. Ask your AI agent: *"Read this PRD and generate an implementation plan."*
   Review the answer and record the approved plan in `agent-workflow/plan/`
   using [PLAN-template.md](.aam/templates/PLAN-template.md).
4. Pick one task. Write it with [TASK-template.md](.aam/templates/TASK-template.md)
   (or [bounded-task-template.md](.aam/templates/bounded-task-template.md) for a
   small fix) in `agent-workflow/tasks/` and give it to the agent. Copy only the
   template block from these files; the rest is guidance and a filled example.
5. When the agent returns, work through
   [IMPLEMENTATION-checklist.md](.aam/templates/IMPLEMENTATION-checklist.md)
   and record your verdict: accept, revise, reject, reassign or return.

## Human checkpoints

**Nothing merges without human review.** Agent output is a draft, not a
delivery. The human approves the PRD and the PLAN, authorizes each TASK and
decides on each result. Acceptance does not by itself authorize release or
deployment.

---

## Roadmap

Status labels follow the AAM methodology. Planned items are not available and
may change.

| Item | Status |
|---|---|
| Template v2.0: core workflow, templates, checklist and prompts in the reference structure | Verified implementation (this release; Markdown files only, no runtime behavior) |
| Worked example: a small filled-in PRD → PLAN → TASK → IMPLEMENTATION chain | Planned product capability |
| Multi-agent roles, skills and quality gates | Planned product capability |
| Opt-in GitHub Cloud Agent adapter | Planned product capability |
| Free VS Code and IntelliJ extensions | Planned product capability |

## Versioning

Releases use [Semantic Versioning](https://semver.org/) tags. `main` contains
only released, template-safe content. See [CHANGELOG.md](CHANGELOG.md).

Version 2.0.0 succeeds the downloadable AAM Starter Kit, which remains
available on aiarchitectmastery.com at its own version 3.1.

## Contributing

This release does not accept pull requests or issues. Send feedback to
info@aiarchitectmastery.com.

## License and trademarks

Licensed under the [Apache License 2.0](LICENSE). See [NOTICE](NOTICE).

"AI Architect Mastery", "AAM" and the AI Architect Mastery logos are brand
names of AI Architect Mastery. They are not licensed under the Apache License
2.0, and forks must not use them in a way that suggests endorsement or
affiliation.

---

Learn more about the methodology at [aiarchitectmastery.com](https://aiarchitectmastery.com/methodology/).

*AI Architect Mastery — Human as architect. AI as builder.*
*Questions or feedback: info@aiarchitectmastery.com*
