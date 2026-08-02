---
ADR ID: ADR-001
Title: Choose Next.js as Frontend Framework
Status: Accepted
Date: 2026-08-02
Decision Makers:
- CTO
- Chief Software Architect
Related ADR:
- ADR-002
- ADR-008
Supersedes: None
---

# ADR-001 — Choose Next.js as Frontend Framework

## Context

AI Film OS requires a modern web application capable of supporting AI chat, project management, storyboard editing, dashboards, timelines, asset management, and enterprise administration.

## Problem

Selecting a frontend framework that balances developer productivity, performance, scalability, and long-term maintainability.

## Decision

Adopt **Next.js 15** with the App Router architecture.

## Alternatives Considered

- React SPA
- Angular
- Vue/Nuxt
- SvelteKit

## Rationale

- React ecosystem maturity
- App Router
- Server Components
- Streaming
- Excellent TypeScript support
- SEO support
- Middleware
- Large community

## Consequences

### Positive

- Excellent developer experience
- Enterprise scalability
- Fast rendering
- Strong ecosystem

### Negative

- Slight learning curve
- Frequent framework updates

## Risks

- Major version upgrades may require migration.

## Future Review

Review every major Next.js release.

## References

https://nextjs.org
