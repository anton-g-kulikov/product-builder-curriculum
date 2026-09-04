# Theme Project — Turn a Product Idea into an Engineering Brief

## Goal

Apply Theme I without writing code.

Choose a modest product capability. You may use a real feature from your own project.

Examples:

- invite a teammate;
- upload and process a file;
- reset a password;
- create and share a private document;
- subscribe to a paid plan;
- export account data.

## Part 1 — Product requirement

Describe the capability in product language.

Keep it short. The point is to expand it through engineering reasoning.

## Part 2 — System shape

Draw or describe the major components involved.

At minimum consider:

- frontend;
- backend;
- persistent data;
- external services;
- infrastructure or delivery concerns where relevant.

Do not add components merely to make the diagram look sophisticated.

## Part 3 — Responsibilities

For every component, state what it owns or is responsible for.

Identify authoritative owners for important business rules and state.

## Part 4 — Interfaces

Describe the information that must cross component boundaries.

You do not need formal API syntax yet.

Specify enough that two coding agents working independently would have a reasonable chance of integrating successfully.

## Part 5 — Feature flow

Trace one successful execution from user action to final visible result.

Then trace at least three important failure paths.

## Part 6 — Requirements

Separate:

- functional behavior;
- security constraints;
- reliability constraints;
- performance/scale expectations;
- observability needs;
- other relevant qualities.

Avoid vague requirements when a concrete constraint is available.

## Part 7 — Assumptions and open decisions

List assumptions.

For each important one, classify it as:

- known fact;
- product decision needed;
- engineering decision;
- needs investigation.

## Part 8 — Agent readiness review

Before asking a coding agent to implement the feature, answer:

1. What could the agent still reasonably interpret in more than one important way?
2. Which ambiguity could produce a working but wrong product?
3. Which decisions should remain implementation choices?
4. What evidence will you require before considering the feature complete?

## Completion standard

The project is complete when you can give the engineering brief to another person or coding agent and explain:

- what should exist;
- which parts own which responsibilities;
- how the parts cooperate;
- what can go wrong;
- what qualities matter;
- which questions remain intentionally unresolved.

Theme II will use this brief as input for the first explicit architecture design.
