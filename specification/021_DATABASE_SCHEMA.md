---
Document ID: AFOS-021
Title: Database Schema
Version: 1.0
Status: Draft
Owner: AI Film OS Project
Author: AI Film OS Team
Created: 2026-08-02
Last Updated: 2026-08-02

Depends On:
  - AFOS-020

Related Documents:
  - AFOS-022
  - AFOS-023
  - AFOS-027

Review Status: Draft
Approval: Pending

Tags:
  - Database
  - Schema
  - PostgreSQL
  - MongoDB
---

# AI Film OS

# Database Schema

---

# Purpose

This document defines the logical database schema of AI Film OS.

The schema provides a unified data model supporting relational data, document storage, vector search, and object storage while maintaining consistency across all production workflows.

---

# Design Principles

The schema follows these principles.

- UUID Primary Keys
- Immutable IDs
- Soft Delete
- Version Controlled
- Audit Ready
- AI Friendly
- Cloud Ready
- Vendor Independent

---

# Primary Database

Recommended

PostgreSQL

Purpose

Structured production data

---

# Secondary Database

MongoDB

Purpose

Flexible production documents

---

# Vector Database

Qdrant

Purpose

Semantic Search

Prompt Search

Knowledge Search

Character Memory

---

# Object Storage

Google Cloud Storage

Amazon S3

Cloudflare R2

Purpose

Media Assets

---

# Global Table Standards

Every relational table contains the following fields.

| Field | Type |
|---------|------|
| id | UUID |
| created_at | Timestamp |
| updated_at | Timestamp |
| created_by | UUID |
| updated_by | UUID |
| version | Integer |
| status | Enum |
| deleted_at | Timestamp (Nullable) |

---

# Core Entities

AI Film OS Version 1 contains the following primary entities.

```
Workspace

User

Project

Story

Scene

Shot

Character

Location

Asset

Prompt

RenderJob

Workflow

Export

ProductionBible

ProjectMemory

MarketingPackage
```

---

# Entity Overview

## Workspace

Stores

- Organization
- Members
- Settings

Relationship

One Workspace

↓

Many Projects

---

## User

Stores

- Profile
- Permissions
- Preferences

Relationship

One User

↓

Many Projects

---

## Project

Stores

- Metadata
- Production Status
- Genre
- Language
- Settings

Relationship

One Project

↓

Many Stories

↓

Many Assets

↓

Many Characters

↓

Many Prompts

---

## Story

Stores

- Logline
- Synopsis
- Outline
- Script

Relationship

One Story

↓

Many Scenes

---

## Scene

Stores

- Scene Number
- Description
- Mood
- Duration

Relationship

One Scene

↓

Many Shots

---

## Shot

Stores

- Camera
- Lens
- Movement
- Prompt
- Duration

Relationship

One Shot

↓

Many Assets

↓

Many Render Jobs

---

## Character

Stores

- Character DNA
- Face Reference
- Clothing
- Voice
- Expressions

Relationship

Reusable Across Projects

---

## Asset

Stores

- Images
- Videos
- Audio
- Documents

Relationship

Belongs To

Project

↓

Shot

↓

Prompt

---

## Prompt

Stores

- Prompt Text
- Negative Prompt
- Parameters
- AI Model

Relationship

One Prompt

↓

Many Renders

---

## RenderJob

Stores

- Model
- Seed
- Resolution
- Cost
- Processing Time

Relationship

One Render

↓

Many Assets

---

## Workflow

Stores

- Current Step
- Status
- Assigned AI Agents
- Progress

---

## ProductionBible

Stores

Approved production knowledge.

Examples

Story Bible

Character Bible

World Bible

Camera Bible

Lighting Bible

---

## ProjectMemory

Stores

Dynamic production memory.

Examples

Prompt History

Review History

AI Decisions

---

## MarketingPackage

Stores

SEO

Hashtags

Descriptions

Campaign Assets

Publishing Data

---

# Naming Convention

Tables

snake_case

Example

```
project_memory

render_jobs

story_scenes
```

Columns

snake_case

Primary Keys

id

Foreign Keys

<entity>_id

Examples

```
project_id

story_id

character_id

shot_id
```

---

# UUID Policy

Every entity uses UUID v7.

Advantages

- Globally unique

- Chronologically sortable

- Distributed friendly

---

# Soft Delete Policy

Records are never permanently removed.

Instead

```
deleted_at

!= NULL
```

means deleted.

---

# Index Strategy

Every table should index

Primary Key

Foreign Keys

created_at

updated_at

status

project_id

Search Fields

---

# Audit Strategy

Every update records

Who

When

What

Version

Reason

---

# JSON Support

Certain fields use JSON.

Examples

```
camera_settings

lighting_settings

render_parameters

ai_reasoning

metadata
```

---

# Future Expansion

Version 2

Task System

Calendar

Budget

Clients

Studio Collaboration

Version 3

Knowledge Graph

AI Memory Graph

Semantic Relationships

---

# End of Document

Document Status: Draft

Next Document:

AFOS-022 Entity Relationship
