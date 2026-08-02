---
ADR ID: ADR-003
Title: Choose PostgreSQL as Primary Database
Status: Accepted
Date: 2026-08-02
---

# ADR-003 — Choose PostgreSQL

## Context

AI Film OS requires transactional consistency together with AI-related capabilities.

## Decision

Use PostgreSQL 17.

## Reasons

- ACID
- JSONB
- pgvector
- Full Text Search
- Mature ecosystem

## Alternatives

- MySQL
- SQL Server
- MongoDB

## Status

Accepted
