---
Document ID: AFOS-024
Title: API Specification
Version: 1.0
Status: Draft
Owner: AI Film OS Project
Author: AI Film OS Team
Created: 2026-08-02
Last Updated: 2026-08-02

Depends On:
  - AFOS-023

Related Documents:
  - AFOS-025
  - AFOS-026

Review Status: Draft
Approval: Pending

Tags:
  - API
  - REST
  - Backend
---

# AI Film OS

# API Specification

---

# Purpose

This document defines the REST API standards used throughout AI Film OS.

All backend services must follow these specifications.

---

# API Version

```
/api/v1/
```

Future versions

```
/api/v2/
/api/v3/
```

---

# Resource Naming

Use plural nouns.

Examples

```
/projects
/users
/stories
/scenes
/shots
/assets
/prompts
/renders
```

---

# HTTP Methods

GET

Retrieve

POST

Create

PUT

Replace

PATCH

Partial Update

DELETE

Soft Delete

---

# Response Format

Every API returns

```
{
  success,
  data,
  error,
  metadata
}
```

---

# Success Response

```
200 OK

201 Created

204 No Content
```

---

# Error Response

```
400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

409 Conflict

422 Validation Error

500 Internal Server Error
```

---

# Pagination

```
?page=1

&page_size=20
```

---

# Filtering

```
?status=approved

?genre=horror
```

---

# Sorting

```
?sort=created_at

?order=desc
```

---

# Search

```
?q=alien
```

---

# Standard Endpoints

Workspace

Projects

Stories

Scenes

Shots

Characters

Assets

Prompts

Render Jobs

Workflow

Export

---

# Validation

Every request validates

- Required Fields
- Data Type
- Permission
- Version

---

# API Principles

- REST First
- Stateless
- Versioned
- Secure
- Predictable
- Consistent

---

# End of Document

Document Status: Draft

Next Document:

AFOS-025 Authentication
