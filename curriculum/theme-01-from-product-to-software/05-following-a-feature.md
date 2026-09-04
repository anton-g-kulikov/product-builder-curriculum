# Module 5 — Following a Feature Through the System

## Goal

Learn to trace one user action through every relevant layer instead of reasoning about components in isolation.

## Example: upload and process an image

A simplified flow:

```text
1. User chooses image
        |
2. Frontend validates obvious client-side constraints
        |
3. Image is uploaded
        |
4. Backend authorizes operation
        |
5. File is stored
        |
6. Job record is created
        |
7. AI provider receives work
        |
8. Result returns
        |
9. Job state is updated
        |
10. Frontend learns new state
        |
11. User sees result
```

The exact architecture may differ. The technique does not.

## Follow the data

At every step ask:

- What data exists here?
- In what representation?
- Who owns it?
- Is it persistent?
- Is it trusted?
- Where does it go next?

## Follow control

Also ask:

- What causes the next step?
- Does one component wait for another?
- Can work continue later?
- What happens if the user closes the browser?
- What happens if a dependency is slow?

These questions eventually lead into synchronous versus asynchronous systems, queues, jobs, and events.

We do not need those abstractions yet. First recognize the problem.

## Follow failure

Now repeat the same flow while assuming each step can fail.

```text
Upload fails
Storage succeeds but DB write fails
AI provider times out
AI provider succeeds but response is lost
Browser closes during processing
Result exists but frontend still shows "processing"
```

The feature is not fully designed until important failure paths are understood.

## Why this matters for agent orchestration

A frontend agent may correctly implement steps 1–3.

A backend agent may correctly implement steps 4–9.

An integration failure can still make the product incorrect.

Your unit of reasoning must therefore sometimes be the complete feature, not the repository folder or agent assignment.

## Exercise

Trace this feature end-to-end:

> User changes their email address and must confirm the new address before it becomes active.

Identify:

- components involved;
- state changes;
- external interactions;
- trust/security boundaries;
- at least five failure or edge cases.

## Exit criterion

You can follow a feature across frontend, backend, persistence, integrations, and back to the user, including important failure paths.
