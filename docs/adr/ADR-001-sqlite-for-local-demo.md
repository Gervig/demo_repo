---
title: ADR-001-sqlite-for-local-demo
---

## Context

The project requires a small, local demo without external dependencies. A lightweight database solution was needed for rapid development and deployment.

## Decision

Use SQLite as the database for this evaluation. SQLite provides a simple, file-based database that requires no separate server process.

## Consequences

- **Pros:**
  - No need for complex database setup
  - Simple file-based storage
  - Easy to use for small-scale applications

- **Cons:**
  - Limited to single-user operation
  - No built-in concurrency support
  - Not suitable for high-traffic or production environments

- **Alternatives Considered:**
  - PostgreSQL
  - MySQL
  - SQLite

- **Why SQLite?**
  - Meets the requirement for a small, local demo
  - No external dependencies
  - Easy to integrate with Python applications

- **Limitations:**
  - Not suitable for large-scale or concurrent applications
  - No automatic backup or replication
  - File-based storage may be less secure for production use