# Module 4 — Interfaces and Contracts

## Goal

Understand how independently responsible parts of a system cooperate without needing to know each other's internal implementation.

## Interface

An interface is a defined way to interact with a component.

For example, the frontend might request:

```text
POST /api/images
```

and send:

```json
{
  "fileId": "file_123"
}
```

The backend might promise a response shaped like:

```json
{
  "jobId": "job_456",
  "status": "queued"
}
```

The frontend does not need to know which database tables the backend updates.

That separation is valuable.

## Contract

A useful contract includes more than the happy-path data shape.

It may specify:

- valid inputs;
- output shape;
- errors;
- permissions;
- side effects;
- timing expectations;
- whether repeating the request is safe;
- compatibility expectations.

Example:

> Creating a processing job requires an authenticated user. The referenced file must belong to that user. A successful request returns the job ID and current status. Repeating the same accepted request with the same idempotency key must not create a second chargeable job.

That is much more useful to an implementation agent than `POST /images`.

## Contracts exist everywhere

Not only HTTP APIs.

Examples include:

- a function signature;
- a database schema;
- an event format;
- a command-line interface;
- an environment variable;
- a file format;
- a third-party API.

## Why agents need contracts

If two agents work independently on frontend and backend, vague coordination creates integration failures.

One agent may expect:

```json
{"user_id": "123"}
```

while another returns:

```json
{"userId": 123}
```

Both implementations may look locally reasonable.

The contract is the shared truth.

## Exercise

Product requirement:

> Show the current processing status of an uploaded image.

Design a conceptual contract between frontend and backend.

Decide:

- what identifier is sent;
- possible statuses;
- what happens if the job does not exist;
- what happens if it belongs to another user;
- whether the result is included when processing finishes.

No code is required.

## Exit criterion

You can describe what two components need to agree on before separate agents can implement them independently.
