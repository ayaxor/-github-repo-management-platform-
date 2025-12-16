
# Examples — ADR Starter Kit

This document provides **example ADRs**
written using the ADR Starter Kit templates.

Examples illustrate proper structure,
clarity, and decision rationale.

---

## Example 1 — Agent Identity Canonicalization

### ADR-0001: Canonical Agent Identity

## Status
Accepted

---

## Context
Multiple agent names were used inconsistently across documentation
(e.g., "Illithia" vs "Alithia"), creating ambiguity in identity,
auditability, and security assumptions.

---

## Decision
Adopt a single canonical agent identity with immutable agent_id
and versioned display names.

---

## Rationale
A canonical identity is required to:
- Ensure auditability
- Prevent impersonation
- Enable multi-tenant isolation

---

## Consequences
Positive:
- Clear agent ownership
- Improved security posture

Negative:
- Requires migration of existing references

---

## Alternatives Considered
- Allow multiple aliases (rejected due to ambiguity)
- Infer identity dynamically (rejected due to audit risk)

---

## References
- docs/00_registry/agents.md
- ADR-0001-agent-identity.md

---

## Example 2 — Message Envelope Schema

### ADR-0002: Message Envelope Schema

## Status
Accepted

---

## Context
Agents require a consistent message format
to validate, route, and audit communications.

---

## Decision
Define a strict JSON-based message envelope schema
validated at ingress.

---

## Rationale
Schema validation ensures:
- Predictable parsing
- Policy enforcement
- Observability hooks

---

## Consequences
Positive:
- Reduced runtime errors
- Clear contract between agents

Negative:
- Initial schema design overhead

---

## Alternatives Considered
- Free-form messages (rejected)
- Ad-hoc per-agent schemas (rejected)

---

## References
- docs/03_protocol/MESSAGE_ENVELOPE.md
- schemas/envelope.schema.json

