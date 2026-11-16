# Core workflow: PRD → PLAN → TASK → IMPLEMENTATION

This is the procedure for the **AI Driven Development Methodology**. The
templates and prompts in `.aam/` support it.

The methodology has four phases:

```
PRD  →  PLAN  →  TASK  →  IMPLEMENTATION
```

## Phases and resources

| Phase | File | What it does |
|---|---|---|
| **PRD** | [PRD-template.md](../templates/PRD-template.md) | Define and approve what you want to build before implementation; AI may help draft |
| **PLAN** | [PLAN-template.md](../templates/PLAN-template.md) | Break the PRD into structured tasks for agent execution |
| **TASK** | [TASK-template.md](../templates/TASK-template.md) | Give Copilot precise, context-rich instructions — one task at a time |
| **IMPLEMENTATION** | [IMPLEMENTATION-checklist.md](../templates/IMPLEMENTATION-checklist.md) | Review what the agent built before it merges — a human checklist, not a fill-in template |
| **Task context** | [bounded-task-template.md](../templates/bounded-task-template.md) | Define five parts of a bounded task and request a read-only gap check before edits |
| **Session continuity** | [fresh-session-handoff.md](../prompts/fresh-session-handoff.md) | Prepare a handoff, then verify it against current sources in a new conversation |
| **Guidance review** | [agent-guidance-review-prompts.md](../prompts/agent-guidance-review-prompts.md) | Analyze existing instructions, approve one bounded change and check procedure loading without removing safeguards |

The public [methodology reference](https://aiarchitectmastery.com/methodology/) explains the structure independently of any course purchase.

---

## The workflow — in 6 steps

**Step 1.** Copy the template you need from `.aam/templates/` into your project's [agent-workflow/](../../agent-workflow/README.md) folder (`prd/`, `plan/` or `tasks/`). Keep project-specific context with the relevant work.

**Step 2.** Fill in [PRD-template.md](../templates/PRD-template.md) for your current feature or project. The human owner reviews and approves the intent, scope and acceptance criteria before implementation planning proceeds.

**Step 3.** Open Copilot Chat and say:
> *"Read this PRD and generate an implementation plan."*

**Step 4.** Review the output and structure it using [PLAN-template.md](../templates/PLAN-template.md). The human owner approves the approach before delegating TASKs.

**Step 5.** For each authorized task in the approved plan, use [TASK-template.md](../templates/TASK-template.md) to give Copilot bounded instructions. State when to stop and ask, and require actual check results and any unexecuted checks in the return.

**Step 6.** Before merging, work through [IMPLEMENTATION-checklist.md](../templates/IMPLEMENTATION-checklist.md) for the TASK you just completed — scope, tests, conventions, security and edge cases.

> **Human checkpoints are mandatory.** Never merge AI-generated code without review. You are the architect — Copilot is the builder.

Record the human decision against the reviewed work and evidence. Acceptance does not by itself authorize release or deployment. These written instructions do not enforce runtime permissions.

The workflow is iterative: if IMPLEMENTATION shows that the intent, approach or assignment was inadequate, the human returns the work to the PRD, PLAN or TASK and refreshes the dependent work before continuing.

## Supporting resources

For a focused task, use [bounded-task-template.md](../templates/bounded-task-template.md) to state the goal, current observation, relevant sources, constraints and acceptance criteria. Ask the agent to surface gaps read-only before edits.

When moving to a fresh conversation, use the two prompts in [fresh-session-handoff.md](../prompts/fresh-session-handoff.md). Review the handoff yourself and verify it against current sources before continuing; it is not proof that a check passed.

If your project already has agent guidance, [agent-guidance-review-prompts.md](../prompts/agent-guidance-review-prompts.md) helps you review it one approved change at a time.

---

## The core principle

Most developers use AI tools reactively — accept a suggestion, fix it, try again. This workflow makes your AI usage **proactive and structured**:

- The **PRD** tells the AI what success looks like
- The **PLAN** tells the AI what to build and in what order
- The **TASK prompt** tells the AI exactly how to build one piece — with constraints, context, and verification criteria
- The **IMPLEMENTATION checklist** tells you what to verify before anything ships

The goal is more consistent work and architectural control. Actual quality still depends on the task, environment, verification and human judgment.
