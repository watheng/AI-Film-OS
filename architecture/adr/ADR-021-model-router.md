---
ADR ID: ADR-021
Title: AI Model Router
Status: Accepted
Date: 2026-08-02
---

# ADR-021 — AI Model Router

## Context

AI Film OS integrates multiple AI providers with different capabilities, costs, and response times.

## Decision

Introduce a centralized Model Router responsible for selecting the most appropriate AI model for every task.

## Responsibilities

- Model Selection
- Cost Optimization
- Fallback Handling
- Load Distribution
- Provider Health Check

## Selection Criteria

- Task Type
- Cost
- Latency
- Quality
- User Preference
- Available API Keys

## Benefits

- Lower operating cost
- Better reliability
- Easy provider expansion

## Status

Accepted
