# AI Film OS Architecture

```
Input

↓

Project Memory

↓

Workflow Engine

↓

AI Modules

↓

QA

↓

Export

```

Every module reads from Project Memory.

Every module writes back to Project Memory.

No module stores private data.

Project Memory is the single source of truth.
