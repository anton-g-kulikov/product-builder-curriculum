# Module 1 — The Shape of a Software Product

## Goal

Build a first mental model of the pieces that turn a product idea into a running software system.

## Start from the product

Consider:

> A user creates an account, uploads an image, the system processes it using an external AI service, and the user can later view the result.

The user experiences one product. Technically, several systems cooperate to produce that experience.

A simplified shape might be:

```text
User
  |
Browser
  |
Frontend
  |
HTTP API
  |
Backend
  |---- Database
  |---- File storage
  `---- External AI service
```

This is not the only possible architecture. It is a useful first model.

## Major pieces

### Frontend

The software directly responsible for the user's interface.

It displays information, collects input, manages interface state, and communicates with other parts of the system.

For a web application, frontend code executes primarily in the browser.

### Backend

Software running on servers rather than inside the user's browser.

It commonly owns business rules, permissions, access to persistent data, coordination with external services, and operations that should not be trusted to a client device.

### Database

Persistent structured data.

For the example product, it might contain users, image records, processing jobs, statuses, and results.

### File or object storage

Large files such as uploaded images are often stored separately from ordinary database records.

The database might know that image `123` belongs to user `456`; object storage contains the actual image bytes.

### External services

Products rarely implement everything themselves.

Email delivery, payments, AI inference, maps, identity, analytics, and many other capabilities may come from other systems through APIs.

### Network

The pieces must communicate.

The browser and backend may exchange HTTP requests. The backend may connect to the database and call external APIs.

Networking is not invisible plumbing. Latency, failure, authentication, and security boundaries arise wherever communication crosses a network.

### Repository

The source files and configuration used to build the product are usually versioned in a Git repository.

The repository is not the running application. It is a major source from which versions of the application are built.

### Build and CI/CD

Source code must become deployable software.

Automated systems can install dependencies, check code, run tests, build artifacts, and deploy approved versions.

### Production

Production is the environment where real users interact with the running system.

A working development environment is not evidence that the production system will behave identically.

### Observability

Once software is running, engineers need evidence about its behavior: logs, metrics, traces, error reports, and alerts.

Without observability, many failures become guesswork.

## A second view

The application exists inside a delivery system:

```text
Product requirements
       |
Git repository
       |
CI / tests / build
       |
Deployment
       |
Production application
       |
Users
       |
Logs / metrics / errors
       |
Engineering feedback
```

Software engineering concerns both the application and the machinery used to change it safely.

## Important distinction: logical versus physical components

A diagram is a model.

A box labelled `Backend` may contain many modules while still being one deployed application. Conversely, one conceptual capability may involve several deployed services.

Do not assume every box needs its own server.

## Check yourself

1. True or false: the frontend and backend are simply two folders that every web application must have.
2. Which component would normally be the safest owner of a secret API key: browser frontend or backend?
3. Why might uploaded images live outside the relational database?
4. Is a Git repository the same thing as the production application?
5. What new engineering problem appears whenever two components communicate over a network?
6. Draw the smallest plausible system for a web product that lets a user save a private note and read it later.

## Exit criterion

You can look at a simple product and identify the major technical systems likely required to make it work, without treating the diagram as a mandatory architecture.
