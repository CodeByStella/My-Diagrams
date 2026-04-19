# AI Coding Agent Pipeline (Logic)

```mermaid
flowchart TD
    U[User goal / task] --> I[Intent and constraints]
    I --> C[Context assembly]
    C --> CTX[Context: repo, rules, history, optional RAG]
    CTX --> R[Reasoning / plan]

    R --> T{Next action?}
    T -->|Read / search| E[Explore codebase]
    T -->|Write / edit| M[Propose or apply changes]
    T -->|Run| X[Shell, tests, lints]
    T -->|Clarify| Q[Question for user]

    E --> R
    M --> V[Verify: tests, lints, diff]
    X --> V
    V -->|More work needed| R
    V -->|Good enough| O[Result: code, diff, or explanation]
    Q --> I

    R -->|Stuck or risky| S[Stop or escalate]
```

**Description:**  
An AI coding agent loops between gathering context, planning, taking actions (read, search, edit, run), and verifying outcomes until the task is done or the agent stops for safety or clarification.

**Flow:** Task → context → plan → (tools + edits + checks) → iterate until verified output or handoff.
