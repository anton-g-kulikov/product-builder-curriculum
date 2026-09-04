# Product Builder — Curriculum

## Destination

A Product Builder learner should become capable of taking a real product requirement and controlling the complete engineering loop:

> Product requirement → software requirements → system design → task decomposition → agent implementation → integration → verification → deployment → observation → debugging → architectural evolution

The curriculum is full-stack and TypeScript-centered. It is designed around metacoding: specification, architecture, agent orchestration, inspection, and verification rather than manual code production. It teaches implementation literacy without making manual code production the objective.

## Helicopter view

### Theme I — From Product to Software

Translate product intent into an engineering problem. Learn the major parts of a software product, how responsibilities are divided, how components communicate, how a feature travels through a system, and how to identify requirements that a PRD usually leaves implicit.

### Theme II — Designing Software

Learn architecture early from first principles: responsibilities, boundaries, coupling, cohesion, dependencies, abstraction, state ownership, data flow, interfaces, invariants, and basic system-level trade-offs.

This is the first pass through architecture. Advanced architectural patterns wait until the learner has experienced the implementation and operational problems they solve.

### Theme III — Understanding Code

Become literate in TypeScript: values, types, variables, functions, objects, collections, modules, state, control flow, errors, async/await, Promises, and enough runtime behavior to inspect and reason about agent-produced code.

### Theme IV — The Web & Full Stack

Understand the browser/server system end-to-end: HTML, CSS, DOM, React, networking, DNS, TCP/TLS at a useful conceptual level, HTTP, APIs, cookies, sessions, frontend/backend boundaries, and request lifecycles.

### Theme V — Data

Learn relational modelling, SQL, PostgreSQL, schemas, constraints, indexes, transactions, migrations, caching, files, object storage, and data ownership.

### Theme VI — Building Software We Can Trust

Learn how to establish evidence of correctness and quality: types, static analysis, unit/integration/end-to-end testing, contract and property tests, mutation testing, security, error handling, reliability, performance, and observability.

### Theme VII — Production Engineering

Understand Git deeply enough to reason about history and integration; then builds, environments, containers, CI/CD, infrastructure, deployment, migrations, rollback, feature flags, logs, metrics, and incidents.

### Theme VIII — Architecture of Real Systems

Return to architecture with implementation experience. Study modular monoliths, layers, ports and adapters, domain boundaries, queues, event-driven systems, distributed systems, consistency, scalability, technical debt, and architectural evolution.

### Theme IX — Agentic Software Engineering

Apply software engineering knowledge to coding-agent workflows: specifications, decomposition, context, parallel work, ownership, reviews, integration, verification gates, agent failure modes, and human escalation.

### Theme X — Meta-Software Architecture

Design the system that designs and builds software: human and agent roles, information flow, architectural governance, reusable capabilities, automated verification, feedback loops, cost and latency trade-offs, and continuous improvement.

---

## The spiral

Architecture appears early and returns later.

The first pass asks:

> What shape should this system have, and why?

The later pass asks:

> Now that we understand implementation, data, production, failures, and verification, what architecture should this system actually have?

The same principle applies throughout Product Builder: encounter a concept, form a useful mental model, use it, then revisit it with more evidence.

## Theme I modules

1. The Shape of a Software Product
2. From Product Requirements to Software Requirements
3. Components and Responsibilities
4. Interfaces and Contracts
5. Following a Feature Through the System
6. Functional and Non-Functional Requirements
7. Failure Cases, Edge Cases, and Assumptions
8. Theme Project — Turn a Product Idea into an Engineering Brief

See `curriculum/theme-01-from-product-to-software/`.

## Theme II provisional modules

1. Why Software Needs Design
2. Boundaries and Separation of Concerns
3. Coupling and Cohesion
4. Dependencies and Direction
5. State Ownership and Sources of Truth
6. Data Flow and Control Flow
7. Abstraction, Encapsulation, and Interfaces
8. Invariants and System Rules
9. Basic Architectural Decisions
10. Theme Project — Design the First Architecture

Later themes remain intentionally less specified. Product Builder should develop them as learners gain the context required to judge what belongs there.
