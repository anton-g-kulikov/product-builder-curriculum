# Module 6 — Functional and Non-Functional Requirements

## Goal

Learn that specifying what software does is not enough to specify what acceptable software is.

## Functional requirements

Functional requirements describe behavior.

Examples:

- A user can upload an image.
- An owner can remove a team member.
- The system sends a reset email.
- A user can export their data.

## Quality constraints

Often called non-functional requirements, these describe properties or constraints on how the system behaves.

Examples:

- 95% of normal API requests should complete within 300 ms.
- A user must never access another organization's private data.
- Losing one application server must not lose persisted user data.
- Every administrative permission change must be auditable.
- The service should support 10,000 simultaneous active users.
- A deployment should be reversible without restoring the database from backup.

The name “non-functional” can be misleading: these requirements are frequently essential to whether the product works in the real world.

## Important qualities

### Correctness

Does the system implement the intended rules?

### Reliability

Does it continue behaving acceptably when things fail?

### Security

Can unauthorized actors cause or observe behavior they should not?

### Performance

Does it respond within acceptable resource and latency limits?

### Scalability

Can the architecture accommodate the expected increase in workload?

### Maintainability

Can engineers understand and change it without disproportionate risk?

### Observability

Can operators determine what the system is doing and why it failed?

### Deployability

Can changes be released and reversed safely?

## Requirements need context

“Scalable” is not a useful requirement by itself.

Scale to what?

100 users?

10 million users?

100 uploads per day?

100,000 per second?

Architecture should respond to actual constraints rather than prestige.

## Exercise

For each statement, classify it as primarily functional or a quality constraint:

1. Users can download an invoice as PDF.
2. Invoice generation should normally finish within five seconds.
3. Only organization administrators can download all-company invoices.
4. The service must retain an audit record of invoice downloads for one year.
5. Users can filter invoices by date.

Then rewrite:

> The application must be fast, secure, and scalable.

into measurable or at least decision-useful constraints for a hypothetical 1,000-user B2B SaaS.

## Exit criterion

You can challenge vague requests such as “make it scalable” and ask for the constraints needed to make an engineering decision.
