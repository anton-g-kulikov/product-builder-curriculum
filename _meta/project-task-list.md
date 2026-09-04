# Project Task List

This document owns active work, task status, and deferred repository follow-ups. Stable project guidance belongs in `README.md`; curriculum scope belongs in `CURRICULUM.md`; verification intent belongs in `test/test-documentation.md`.

## Active

### Explain how to study with the curriculum

- Status: in progress
- Goal: add a learner-facing usage workflow to the root README.
- Success criteria:
  - the workflow starts with the curriculum overview and then the selected theme README;
  - learners answer each topic's questions themselves before requesting feedback;
  - LLM review is grounded in this repository's relevant curriculum files and exit criteria;
  - the instructions work with any LLM chat and explain how to provide repository context;
  - repository documentation checks pass.
- In scope: root README guidance, a reusable review prompt, verification, commits, and push.
- Out of scope: lesson changes, answer keys, automated assessment, and vendor-specific chat instructions.
- Blocking subtasks: none.
- Deferred follow-ups: revisit the review workflow when the curriculum gains a dedicated learning application.

## Completed

### Bootstrap the metacoding repository workflow

- Status: complete
- Goal: align the checked-in repository with the initialized metacoding workflow.
- Result: generated integrations remain local, repository responsibilities are separated, contributor guidance is linked from the README, and the changes are organized as focused commits.
- Verification: ignore-rule checks, Markdown-link validation, and whitespace checks passed.
- Deferred follow-up: choose an automated Markdown checker when the repository gains package tooling or CI.

- Initial curriculum repository created and published.
