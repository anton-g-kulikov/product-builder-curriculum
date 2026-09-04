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

## Curriculum usage guide

- Behavior under change: the root README explains how a learner should navigate the curriculum, complete topic questions, and receive curriculum-grounded LLM feedback.
- Happy path checks:
  - a `How to use this curriculum` section exists;
  - the sequence links to the curriculum overview before the Theme I README;
  - learners are told to answer `Check yourself` questions and `Exercise` prompts before consulting an LLM;
  - the LLM is instructed to review against the root overview, current theme README, current topic, and topic exit criterion;
  - a reusable, vendor-neutral review prompt is included.
- Error and edge cases:
  - the workflow must not assume an LLM can read a local checkout or GitHub repository without being given access;
  - the LLM must assess the learner's attempt rather than silently replacing it with a generated answer;
  - the guidance must remain useful when later themes use different exercise labels.
- Regression risks: relative links could break, or future lesson structure could diverge from the described workflow.
- Automated checks to run: heading/content assertions, local Markdown-link validation, and `git diff --check`.
- Manual verification to run: compare the instructions with the Theme I README and representative topic endings.

### TDD adaptation

This is a documentation behavior change. The initial check confirmed that the usage section was absent; this test intent was recorded before editing the README.
