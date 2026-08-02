---
Document ID: AFOS-021A
Title: Database Design Rules
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
  - AFOS-022
  - AFOS-023

Review Status: Draft
Approval: Pending

Tags:
  - Standards
  - Database
  - Design Rules
---

# AI Film OS

# Database Design Rules

---

# Purpose

This document defines the mandatory database design standards for every database component within AI Film OS.

These rules ensure consistency, maintainability, scalability, and compatibility across all backend services.

---

# General Principles

Every database object must follow:

- Consistency
- Simplicity
- Scalability
- Traceability
- Reusability
- Vendor Independence

---

# Naming Rules

Tables

snake_case

Example

projects

render_jobs

project_memory

Columns

snake_case

Primary Key

id

Foreign Key

<object>_id

Example

project_id

scene_id

shot_id

---

# Primary Keys

Every table uses

UUID v7

Never use auto increment IDs.

---

# Required Columns

Every table contains

id

created_at

updated_at

created_by

updated_by

version

status

deleted_at

---

# Timestamp Rules

All timestamps

UTC

ISO-8601

Examples

created_at

updated_at

deleted_at

---

# Status Enum

Standard values

draft

review

approved

published

archived

deleted

---

# Soft Delete

Records are never physically deleted.

deleted_at stores deletion time.

---

# Foreign Keys

Every relationship uses UUID.

No business logic may depend on table ordering.

---

# Index Rules

Index

Primary Keys

Foreign Keys

Status

Created Date

Project ID

Search Fields

---

# JSON Fields

Allowed only for

Metadata

AI Parameters

Render Settings

Camera Settings

Dynamic Configuration

---

# Version Rules

Approved data is immutable.

Editing creates a new version.

---

# Audit Rules

Every change records

Who

When

Why

Previous Version

New Version

---

# Security Rules

No sensitive information stored in plaintext.

Passwords

Hashed

Secrets

Encrypted

API Keys

Encrypted

---

# Performance Rules

Avoid duplicated data.

Prefer normalization.

Cache expensive queries.

Use pagination.

---

# AI Compatibility

Every schema must support:

AI reasoning

Semantic search

Vector search

Knowledge graph

Prompt history

Character DNA

---

# Future Expansion

Support

Multi Tenant

Horizontal Scaling

Distributed Storage

Microservices

Event Sourcing

---

# End of Document

Document Status: Draft

Next Document:

AFOS-022 Entity Relationship
