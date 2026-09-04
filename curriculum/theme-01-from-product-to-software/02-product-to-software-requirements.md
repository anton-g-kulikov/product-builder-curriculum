# Module 2 — From Product Requirements to Software Requirements

## Goal

Learn why a good product requirement is usually not yet a sufficient software requirement.

## Product intent

A product requirement describes desired behavior from a user or business perspective.

Example:

> Users can reset a forgotten password.

That is useful. It is also radically incomplete as an implementation specification.

## Expand the requirement

A software engineer must ask what capabilities the requirement implies.

One possible decomposition:

```text
Frontend
- request-reset form
- new-password form
- loading, success, and error states

Backend
- accept reset request
- generate secure reset capability
- validate reset attempt
- change password

Data
- user identity
- reset state or token metadata

External service
- email delivery

Security
- expiration
- single use
- rate limiting
- avoid leaking whether an account exists

Verification
- valid flow
- invalid token
- expired token
- reused token
- excessive requests
```

The product requirement has not changed. Our understanding of what must be true for it to exist has.

## Requirements versus implementation

Software requirements should become more precise without prematurely dictating every implementation choice.

For example:

> A password-reset link must become invalid after successful use.

is a requirement.

> Store a boolean `used` column in PostgreSQL.

is an implementation decision.

The distinction matters when working with coding agents. Too little specification leaves important behavior to chance. Too much premature implementation detail prevents the agent from considering better designs.

## Ask systematic questions

For a capability, ask:

### Actors

Who or what initiates the behavior?

### Inputs

What information enters the system?

### Outputs

What should the user or another system receive?

### State

What information must survive after the current request or session?

### Rules

What conditions must always hold?

### Dependencies

Which other systems are required?

### Permissions

Who is allowed to perform the action?

### Failures

What can go wrong, and what should happen then?

### Quality constraints

How fast, reliable, secure, scalable, or auditable must it be?

## The specification gap

Coding agents are good at filling gaps.

That is both useful and dangerous.

If you say:

> Add team invitations.

an agent may silently decide:

- whether invitations expire;
- whether an email can have several active invitations;
- what happens to an invitation after a user joins;
- whether invitations can change roles;
- who may invite;
- whether invitations are logged.

A successful implementation can therefore be technically functional while implementing product policy nobody consciously chose.

## Check yourself

Take:

> Users can delete their account.

Which of the following are questions that should probably be resolved before implementation?

- What happens to content the user created?
- How long should deletion take?
- Can deletion be reversed?
- What happens to active sessions?
- Does the system have legal retention requirements?
- Which CSS framework is used?

Explain why.

## Exit criterion

Given a short product requirement, you can identify the major unanswered engineering questions without immediately jumping to code or technology choices.
