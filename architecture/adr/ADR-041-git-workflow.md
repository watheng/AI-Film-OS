---
ADR ID: ADR-041
Title: Git Workflow Strategy
Status: Accepted
Date: 2026-08-02
---

# ADR-041 — Git Workflow Strategy

## Context

A consistent Git workflow is required to support collaborative development, AI-assisted coding, and reliable releases.

## Decision

Adopt a simplified Git Flow with protected main branches.

## Branches

- main
- develop
- feature/*
- bugfix/*
- hotfix/*
- release/*

## Rules

- Never commit directly to main.
- All changes require Pull Requests.
- All Pull Requests require review before merge.

## Benefits

- Predictable release process
- Cleaner commit history
- Reduced merge conflicts

## Status

Accepted
