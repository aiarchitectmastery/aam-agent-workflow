# agent-workflow/ — your project's work products

This folder is for **your** work: the PRDs, PLANs, TASKs and review records you
create while following the [core workflow](../.aam/workflows/core-workflow.md).
It starts empty apart from this README. Create each subfolder the first time
you need it.

| Subfolder | What goes in it | Start from |
|---|---|---|
| `prd/` | Approved statements of intent | [PRD-template.md](../.aam/templates/PRD-template.md) |
| `plan/` | Approved implementation plans | [PLAN-template.md](../.aam/templates/PLAN-template.md) |
| `tasks/` | Work items: TASK (known work), BUG (behavior that breaks a requirement) and PROB (a problem showing that the PRD, PLAN, TASK or implementation may be insufficient), plus their IMPLEMENTATION review records | [TASK-template.md](../.aam/templates/TASK-template.md), [bounded-task-template.md](../.aam/templates/bounded-task-template.md), [IMPLEMENTATION-checklist.md](../.aam/templates/IMPLEMENTATION-checklist.md) |

## Suggested naming

These are suggestions, not rules. Use your team's conventions if you have them.

```text
agent-workflow/
├── prd/PRD-export-csv.md
├── plan/PLAN-export-csv.md
└── tasks/
    ├── TASK-001-export-endpoint.md
    └── TASK-001-export-endpoint-review.md   ← filled IMPLEMENTATION checklist
```

Keep the version and approval of each PRD and PLAN inside the file, so a TASK
can reference exactly what it was derived from.
