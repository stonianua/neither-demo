# ADR 005 — Session model (supersedes ADR 002)

## Status
Supersedes ADR 002.

## Decision
Move to opaque server-side session IDs stored in Postgres; browsers hold only an httpOnly cookie.

## Rejected
Continuing with JWTs as the sole session — rejected after we needed immediate revocation for compromised agent tokens.

## Constraint
Compromised tokens must be revocable within 60 seconds without waiting for JWT expiry.

## Citation
Incident 2026-06: JWT TTL left a revoked agent key valid for 14 minutes.
