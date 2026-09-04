# Product Builder

**Full-stack software engineering for the agentic era.**

> Build from the product down. Understand from the code up.

Product Builder is a curriculum for people who use coding agents to build complete software products — from product requirements and software architecture through implementation, verification, deployment, and operation.

Its goal is not to teach learners to type code from memory. The goal is to become capable of taking responsibility for a complete software product as an engineered system: understanding its shape, designing it, directing agents that implement it, judging their work, and operating the result.

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

## Assessment

Product Builder tests understanding and engineering judgment rather than syntax performance.

Assessments progress from diagrams, multiple choice, feature decomposition, and requirement analysis to predicting behavior, reading code, finding bugs, identifying missing requirements, comparing architectures, reasoning about failure modes, and deciding what evidence is sufficient to trust an implementation.

The eventual standard is:

> Can you independently take a product requirement to a trustworthy production system while using coding agents for implementation?

## An evolving curriculum

This repository is intended to be cloned, used, and changed.

The shared curriculum provides a common full-stack spine. Individual learners can progress at their own pace, deepen particular areas, and evolve their copy of the learning system.

The curriculum itself is expected to improve through use.
