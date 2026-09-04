# Theme I — From Product to Software

## Goal

Learn to look at a product requirement and see the software system implied by it.

A product manager can often describe what a user should be able to do. Software engineering requires another layer of precision: what components must exist, what each is responsible for, what information moves between them, what states and failures are possible, and what qualities the system must preserve.

This theme builds that bridge.

No manual coding is required.

## Outcome

By the end of the theme, you should be able to take a modest product feature and produce a useful engineering brief for a coding agent or engineering team.

You should be able to:

- sketch the major parts of a full-stack product;
- distinguish frontend, backend, data stores, infrastructure, and external services;
- decompose a product capability into software responsibilities;
- identify interfaces and data exchanged between components;
- trace a feature end-to-end;
- distinguish functional requirements from quality constraints;
- identify important failure cases, edge cases, and hidden assumptions;
- recognize when a request such as “implement password reset” is underspecified.

## Running example

Several lessons use a deliberately ordinary product:

> A user creates an account, uploads an image, the system processes it using an external AI service, and the user can later view the result.

We will progressively turn that sentence into a software model.

## Modules

1. [The Shape of a Software Product](01-shape-of-a-software-product.md)
2. [From Product Requirements to Software Requirements](02-product-to-software-requirements.md)
3. [Components and Responsibilities](03-components-and-responsibilities.md)
4. [Interfaces and Contracts](04-interfaces-and-contracts.md)
5. [Following a Feature Through the System](05-following-a-feature.md)
6. [Functional and Non-Functional Requirements](06-functional-and-non-functional.md)
7. [Failure Cases, Edge Cases, and Assumptions](07-failures-edges-assumptions.md)
8. [Theme Project — Engineering Brief](08-theme-project.md)

## Assessment style

The first theme tests system comprehension, not syntax.

Expect questions such as:

- Which component should own this responsibility?
- Which pieces of the system need to communicate?
- What requirement is missing?
- What happens if this dependency fails?
- Which statement is functional versus non-functional?
- Is this specification sufficient for an implementation agent?
