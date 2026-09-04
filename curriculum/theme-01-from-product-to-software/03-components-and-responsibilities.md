# Module 3 — Components and Responsibilities

## Goal

Learn to divide a system by responsibility rather than treating the application as one undifferentiated block.

## Responsibility

A responsibility is something a part of the system is accountable for doing or knowing.

For the image-processing example:

```text
Frontend
- collect image from user
- show upload progress
- display processing status and result

Backend
- verify user permission
- create processing job
- coordinate storage and AI provider
- expose status to frontend

Database
- persist user/job metadata and state

Object storage
- persist image bytes

AI provider
- perform model inference
```

This is already an architectural decision, but at a deliberately simple level.

## Why responsibility matters

When ownership is unclear, several components may implement the same rule differently.

Imagine the rule:

> A free user may process at most 20 images per month.

If the frontend alone enforces this, a user may bypass it by calling the backend directly.

The frontend can still display the limit, but the authoritative enforcement should normally exist in a trusted server-side component.

This introduces two important ideas:

- responsibility;
- authority.

The place that displays a rule is not necessarily the place that owns the rule.

## Boundaries

A boundary separates responsibilities.

Useful boundaries can make systems easier to understand and change. Bad boundaries can create unnecessary communication and complexity.

Do not create a component merely because a noun exists in the PRD.

Ask:

> What needs to change independently?

> What must be protected from what?

> Where should this rule have one authoritative owner?

## Avoid architecture-by-diagram

A common beginner mistake is assuming that more boxes mean better architecture.

They do not.

Every boundary has a cost:

- communication;
- interfaces;
- failure modes;
- coordination;
- testing;
- deployment complexity.

Good decomposition creates useful boundaries, not maximum boundaries.

## Exercise

Feature:

> A team owner can invite a member and choose whether the member is an editor or viewer.

List plausible responsibilities for:

- frontend;
- backend;
- database;
- email service.

Then answer:

1. Where should the permission to invite be authoritatively checked?
2. Where should the selected role be persisted?
3. Should the email service decide whether the invitation is valid?
4. Which parts might display the same rule without owning it?

## Exit criterion

You can decompose a feature into responsibilities and explain why a particular component should own an important rule or piece of state.
