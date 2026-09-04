# Product Builder

**Full-stack software engineering for the agentic era.**

> Build from the product down. Understand from the code up.

Product Builder is a curriculum for people who use coding agents to build complete software products — from product requirements and software architecture through implementation, verification, deployment, and operation.

Its goal is not to teach learners to type code from memory. The goal is to become capable of taking responsibility for a complete software product as an engineered system: understanding its shape, designing it, directing agents that implement it, judging their work, and operating the result.

## How to use this curriculum

This curriculum is meant to be worked through, not merely read. Use the questions and exercises to make your reasoning visible, then use an LLM to test that reasoning against the curriculum's own concepts and standards.

Follow this sequence:

1. Start with the [curriculum overview](CURRICULUM.md). Read the destination, helicopter view, and learning spiral so you understand where the themes are going and why they appear in this order.
2. Open the README for the theme you are studying. It explains the theme's goal, intended outcome, module order, and assessment style. Begin with [Theme I — From Product to Software](curriculum/theme-01-from-product-to-software/README.md).
3. Work through the theme's topics in order. At the end of a topic, stop at sections such as **Check yourself**, **Exercise**, or **Theme Project**. Write your own answers, diagrams, decisions, or analysis before asking an LLM for help.
4. Give your answers to an LLM chat of your choice and ask it to review them using this repository as the source of truth. The review should be based on the root overview, the current theme README, the topic itself, and its exit criterion—not only on a generic understanding of software engineering.
5. Revise weak answers and ask follow-up questions until you can explain the reasoning yourself and satisfy the topic's exit criterion. Then continue to the next topic.

At this stage of the repository, there is no separate answer key or automated grading system. The LLM review conversation is the assessment loop. Its purpose is to reveal missing reasoning, incorrect assumptions, and shallow understanding while keeping you responsible for producing and improving the answers.

### Give the LLM the right context

An LLM does not necessarily have access to your local checkout or know which version of the curriculum you are using. If the chat can open public links, give it the [repository URL](https://github.com/anton-g-kulikov/product-builder-curriculum) and identify the exact theme and topic. Otherwise, attach or paste these files:

- this root `README.md`;
- `CURRICULUM.md`;
- the current theme's `README.md`;
- the current topic file;
- your answers or exercise output.

You can adapt this prompt:

```text
I am studying the Product Builder curriculum in this repository:
https://github.com/anton-g-kulikov/product-builder-curriculum

Review my answers using the repository's curriculum as the source of truth.
Read the root README, CURRICULUM.md, the current theme README, and the
current topic before evaluating me. Judge my answers against the concepts,
scope, terminology, and exit criterion in those files rather than giving a
generic software-engineering answer.

For each answer:
1. Explain what is correct and demonstrates understanding.
2. Identify errors, unsupported assumptions, or important missing reasoning.
3. Ask a focused follow-up question when my reasoning is unclear.
4. Distinguish a conflict with the curriculum from a reasonable alternative.
5. Do not replace my attempt with a complete model answer before I have had
   a chance to revise it.

Current theme: [theme name and link or attached file]
Current topic: [topic name and link or attached file]

Questions and my answers:
[paste them here]
```

## The premise

Coding agents can increasingly translate specifications into implementation. This changes where human engineering judgment is most valuable, but it does not remove the need for software engineering knowledge.

A Product Builder needs to be able to:

- translate product intent into software requirements;
- understand the components and behavior of full-stack systems;
- design responsibilities, boundaries, interfaces, data flows, and architecture;
- read and reason about implementation when necessary;
- judge correctness, security, reliability, scalability, and maintainability;
- debug and operate real systems;
- decompose work for coding agents and integrate their output;
- design verification mechanisms that make agent-produced software trustworthy.

Manual code production is not a learning objective. Software comprehension and engineering judgment are.

## The learning direction

The curriculum starts from a level familiar to product-minded learners: the product itself.

It moves primarily from the top down:

> Product intent → software requirements → system design → architecture → components → interfaces → implementation → computation

It then moves back upward as implementation knowledge becomes deeper:

> Implementation → verification → production → architecture → product

Architecture is therefore learned twice: first from principles, then again after the learner has encountered the implementation and operational problems architecture is meant to solve.

## Full-stack means the whole product

Here, full-stack is broader than frontend plus backend.

It includes product requirements, system design, frontend, backend, data, integrations, networking, security, testing, infrastructure, CI/CD, production, observability, and architectural evolution.

The curriculum uses an opinionated TypeScript-centered stack so learners can build depth rather than sample many technologies:

- TypeScript
- Node.js
- React
- PostgreSQL
- HTTP/JSON
- Git
- Docker
- GitHub Actions

Specific frameworks may evolve. The concepts should remain portable.

## Learn by building

The Product Builder learning system is itself part of the curriculum.

It begins deliberately small. As the learner reaches new concepts, the application evolves to use them. Databases, authentication, APIs, observability, background work, and other abstractions should appear when the learner can understand the problems they solve.

The project should remain close enough to the learner's current understanding that important decisions can be explained rather than merely delegated.

## Metacoding

Product Builder teaches software engineering. **Metacoding** is the working methodology.

Metacoding means building software primarily through specification, architecture, coding-agent orchestration, inspection, and verification rather than manual code production.

The eventual objective is to control the complete loop:

> Product requirement → software requirements → architecture → agent implementation → integration → verification → production → observation → iteration

## Repository workflow

Changes to this repository follow a verification-first metacoding workflow:

1. Capture the bounded task, success criteria, status, and deferred work in the [`_meta/project-task-list.md`](_meta/project-task-list.md).
2. Define the evidence that will prove the change correct in [`test/test-documentation.md`](test/test-documentation.md) before implementation.
3. Make one coherent change at a time, run the relevant checks, and preserve each concern in a focused commit.

The task list owns temporal project status. Test documentation owns verification intent. This README remains the stable project overview and contributor entry point.

## Assessment

Product Builder tests understanding and engineering judgment rather than syntax performance.

Assessments progress from diagrams, multiple choice, feature decomposition, and requirement analysis to predicting behavior, reading code, finding bugs, identifying missing requirements, comparing architectures, reasoning about failure modes, and deciding what evidence is sufficient to trust an implementation.

The eventual standard is:

> Can you independently take a product requirement to a trustworthy production system while using coding agents for implementation?

## An evolving curriculum

This repository is intended to be cloned, used, and changed.

The shared curriculum provides a common full-stack spine. Individual learners can progress at their own pace, deepen particular areas, and evolve their copy of the learning system.

The curriculum itself is expected to improve through use.
