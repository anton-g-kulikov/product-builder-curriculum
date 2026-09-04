# Test Documentation

This document owns repository-level verification intent. Curriculum exercises define their own learning assessments in the relevant module.

## Repository workflow bootstrap

- Behavior under change: Git hygiene and contributor workflow documentation.
- Happy path checks:
  - required root and workflow documents exist;
  - generated metacoding integration files are ignored;
  - Markdown links to repository files resolve;
  - the working tree is clean after commits;
  - `main` matches `origin/main` after push.
- Error and edge cases:
  - ordinary project files must not be hidden by broad ignore rules;
  - vendor-specific metacoding copies must not be staged accidentally;
  - documentation must not assign the same responsibility to multiple files.
- Regression risks: ignore patterns could become too broad or documentation links could drift.
- Automated checks to run: `git check-ignore`, `git diff --check`, and a local Markdown-link validation script.
- Manual verification to run: inspect the final commit sequence and compare local `main` with `origin/main`.

## TDD adaptation

This bootstrap changes repository configuration and documentation, not executable product behavior. The required artifacts were first checked and confirmed missing. Validation intent was then documented here before the repository changes were implemented. No application test framework exists yet.
