---
ADR ID: ADR-031
Title: Secrets Management
Status: Accepted
Date: 2026-08-02
---

# ADR-031 — Secrets Management

## Context

AI Film OS uses API keys, database credentials, JWT secrets, and third-party integrations that must never be stored in source code.

## Decision

All secrets shall be managed through environment variables and secure secret management systems.

## Secret Types

- API Keys
- Database Credentials
- JWT Secrets
- OAuth Credentials
- Encryption Keys

## Rules

- Never commit secrets into Git.
- Use .env for local development.
- Use Secret Manager in production.

## Status

Accepted
