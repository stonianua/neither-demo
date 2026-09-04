# ADR 002 — Session tokens (initial)

## Decision
Issue short-lived JWTs from the API for browser and agent clients.

## Rejected
Server-side sessions in Redis — rejected for first ship to avoid sticky-session coupling across regions.

## Constraint
Must work behind multiple stateless API replicas.

## Citation
Launch checklist: three regions, no shared session store yet.
