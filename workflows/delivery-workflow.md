# Delivery Workflow

```mermaid
flowchart LR
    A[Backlog] -->|Refined + accepted| B[Ready]
    B -->|Start work| C[In Progress]
    C -->|External constraint| D[Blocked]
    D -->|Constraint removed| C
    C -->|Implementation complete| E[Review]
    E -->|Accepted| F[Done]
    E -->|Rework| C
```

## Transition controls

| Transition | Required condition |
|---|---|
| Backlog → Ready | owner, priority and acceptance criteria present |
| Ready → In Progress | assignee present |
| In Progress → Blocked | blocker reason + blocker owner + next review date |
| In Progress → Review | implementation notes or linked deliverable present |
| Review → Done | acceptance criteria satisfied |
