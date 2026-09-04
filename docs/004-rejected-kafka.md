# ADR 004 — Event bus

## Decision
Use Postgres LISTEN/NOTIFY plus an outbox table for domain events.

## Rejected
Apache Kafka — rejected: ops cost and on-call load too high for a three-person team; we do not need multi-subscriber replay yet.

## Constraint
Team size ≤ 3 engineers; no dedicated platform role.

## Citation
Capacity planning doc: Kafka cluster estimate exceeded monthly infra budget.
