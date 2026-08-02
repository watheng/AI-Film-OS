---
ADR ID: ADR-016
Title: Event-Driven Architecture
Status: Accepted
Date: 2026-08-02
---

# ADR-016 — Event-Driven Architecture

## Context

Multiple services and AI agents must communicate asynchronously.

## Decision

Adopt an event-driven architecture for internal workflows.

## Example Events

- ProjectCreated
- StoryGenerated
- RenderCompleted
- AgentFinished
- ExportReady

## Benefits

- Loose coupling
- Better scalability
- Easier automation

## Status

Accepted
