# Module 7 — Failure Cases, Edge Cases, and Assumptions

## Goal

Learn to inspect the negative space around a requirement: what happens outside the expected happy path.

## Happy paths are cheap

Requirement:

> A user pays for a subscription and receives access to Pro features.

The happy path is straightforward:

```text
User -> Checkout -> Payment succeeds -> Subscription active -> Pro access
```

Real systems must also answer:

- What if payment succeeds but our backend never receives confirmation?
- What if the provider sends the same event twice?
- What if payment is later reversed?
- What if the subscription expires while the user is active?
- What if the provider is unavailable?
- What if two browser tabs start checkout simultaneously?
- Which system is the authoritative source of subscription state?

These questions often reveal more architecture than the happy path.

## Failure case

A failure case describes something expected to sometimes go wrong: timeout, unavailable dependency, rejected payment, invalid input, disk full, lost connection.

## Edge case

An edge case occurs at an unusual boundary of valid or possible behavior: empty collection, maximum size, duplicate request, account with no email, date at a timezone boundary.

The categories overlap. The practical skill is finding them.

## Assumption

An assumption is something the design treats as true.

Examples:

- email addresses are unique;
- every user belongs to exactly one organization;
- the external API responds within 30 seconds;
- IDs never change;
- a request is delivered only once.

Unstated assumptions are dangerous because an implementation may depend on them without anyone verifying them.

## Turn assumptions into decisions

For important assumptions:

1. state them;
2. test whether they are true;
3. make them explicit constraints if appropriate;
4. design for violation when necessary.

## Agent-specific risk

Coding agents are exceptionally capable of supplying plausible unstated assumptions.

A good orchestration process therefore asks an agent to surface assumptions before or during implementation, especially for security, data ownership, concurrency, and external integrations.

## Exercise

Requirement:

> A user can invite another person to a workspace by email.

Produce:

- five failure cases;
- five edge cases;
- five assumptions that an implementation agent might silently make.

Then mark which assumptions require a product decision before implementation.

## Exit criterion

You habitually ask “what if?” and “what are we assuming?” before accepting a feature specification as complete.
