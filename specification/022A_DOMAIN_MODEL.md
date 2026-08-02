---
Document ID: AFOS-022A
Title: Domain Model
Version: 1.0
Status: Draft
Owner: AI Film OS Project
Author: AI Film OS Team
Created: 2026-08-02
Last Updated: 2026-08-02

Depends On:
  - AFOS-021
  - AFOS-022

Related Documents:
  - AFOS-023
  - AFOS-024

Review Status: Draft
Approval: Pending

Tags:
  - Domain
  - DDD
  - Architecture
---

# AI Film OS

# Domain Model

---

# Purpose

This document defines the business domains of AI Film OS.

The Domain Model separates business responsibilities into independent bounded contexts, enabling scalable development, maintainability, and clear ownership.

---

# Objectives

The Domain Model provides:

- Business separation
- Domain ownership
- Service boundaries
- Independent evolution
- AI-friendly architecture

---

# Core Domains

AI Film OS Version 1 consists of the following domains.

---

## Identity Domain

Responsible for:

- Workspace
- User
- Roles
- Permissions
- Authentication

---

## Project Domain

Responsible for:

- Projects
- Project Settings
- Project Metadata
- Project Status

---

## Story Domain

Responsible for:

- Story
- Characters
- World
- Locations
- Scenes
- Shots

---

## Production Domain

Responsible for:

- Storyboards
- Camera Plans
- Shot Lists
- Production Bible

---

## Prompt Domain

Responsible for:

- Prompt Templates
- Prompt Versions
- Prompt Variables
- Negative Prompts

---

## Render Domain

Responsible for:

- AI Models
- Render Jobs
- Queue
- Cost
- Render History

---

## Asset Domain

Responsible for:

- Images
- Videos
- Audio
- Documents
- References

---

## Knowledge Domain

Responsible for:

- Project Memory
- Knowledge Engine
- AI Reasoning
- Character DNA
- Prompt Memory

---

## Workflow Domain

Responsible for:

- Workflow Templates
- Production States
- Task Progress
- Review Gates

---

## Marketing Domain

Responsible for:

- SEO
- Campaign
- Social Media
- Distribution

---

## Export Domain

Responsible for:

- Output Packages
- Archive
- Metadata
- Manifest

---

# Domain Relationships

```
Identity

↓

Project

↓

Story

↓

Production

↓

Prompt

↓

Render

↓

Assets

↓

Export
```

Knowledge Domain supports every other domain.

Workflow Domain orchestrates every other domain.

---

# Design Principles

Every domain:

- Owns its own data
- Exposes public interfaces
- Avoids direct database coupling
- Communicates through services
- Can evolve independently

---

# Future Expansion

Future domains may include:

- Budget
- Calendar
- Clients
- Team Collaboration
- Marketplace
- AI Marketplace

---

# End of Document

Document Status: Draft

Next Document:

AFOS-023 API Architecture
