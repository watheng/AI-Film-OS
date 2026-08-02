---
Document ID: AFOS-022
Title: Entity Relationship
Version: 1.0
Status: Draft
Owner: AI Film OS Project
Author: AI Film OS Team
Created: 2026-08-02
Last Updated: 2026-08-02

Depends On:
  - AFOS-020
  - AFOS-021

Related Documents:
  - AFOS-023
  - AFOS-027

Review Status: Draft
Approval: Pending

Tags:
  - ERD
  - Database
  - Entity
---

# AI Film OS

# Entity Relationship

---

# Purpose

This document defines the logical relationships between all core entities in AI Film OS.

The Entity Relationship model serves as the foundation for database implementation, API development, workflow orchestration, and AI reasoning.

---

# Core Entity Hierarchy

```
Workspace
│
├── Users
│
├── Projects
│   │
│   ├── Story
│   │    ├── Scenes
│   │    │     ├── Shots
│   │    │     │     ├── Prompts
│   │    │     │     │     ├── Render Jobs
│   │    │     │     │     │      └── Assets
│   │    │     │     │
│   │    │     │     └── Camera Settings
│   │    │     │
│   │    │     └── Storyboards
│   │
│   ├── Characters
│   │      ├── Character DNA
│   │      ├── Expressions
│   │      └── Costumes
│   │
│   ├── Locations
│   │
│   ├── Production Bible
│   │
│   ├── Project Memory
│   │
│   ├── Marketing Package
│   │
│   └── Export Package
│
└── System Logs
```

---

# Relationship Rules

Workspace

1 → N Projects

Project

1 → N Stories

Story

1 → N Scenes

Scene

1 → N Shots

Shot

1 → N Prompts

Prompt

1 → N Render Jobs

Render Job

1 → N Assets

Project

1 → N Characters

Project

1 → N Locations

Project

1 → N Storyboards

Project

1 → 1 Production Bible

Project

1 → 1 Project Memory

Project

1 → N Marketing Packages

Project

1 → N Export Packages

---

# Character Relationship

Character

↓

Character DNA

↓

Expressions

↓

Voice

↓

Costume

↓

Assets

Every render references Character DNA instead of recreating character definitions.

---

# Prompt Relationship

Prompt

↓

Positive Prompt

↓

Negative Prompt

↓

Style Prompt

↓

Render Parameters

↓

AI Model

↓

Seed

↓

Render Job

---

# Asset Relationship

Asset

↓

Prompt

↓

Render Job

↓

Shot

↓

Scene

↓

Project

Every asset can be traced back to its originating prompt.

---

# Memory Relationship

Project

↓

Project Memory

↓

AI Decisions

↓

Review History

↓

Prompt History

↓

Production Logs

---

# Workflow Relationship

Project

↓

Workflow

↓

Task

↓

Render

↓

Review

↓

Approval

↓

Export

---

# Cardinality Principles

One Workspace

Many Projects

One Project

Many Scenes

One Scene

Many Shots

One Shot

Many Assets

One Prompt

Many Render Jobs

---

# Future Expansion

Future versions may introduce:

Team

Client

Budget

Calendar

Task Assignment

Knowledge Graph

Semantic Links

---

# Design Principles

The Entity Relationship model must be:

Consistent

Scalable

Traceable

AI-Friendly

Modular

Future-Proof

---

# End of Document

Document Status: Draft

Next Document:

AFOS-023 API Architecture
