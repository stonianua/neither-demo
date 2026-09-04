# ADR 003 — Billing ledger

## Decision
Keep an append-only billing ledger table in Postgres; derive invoices from it.

## Rejected
Mutable invoice rows as source of truth — rejected because corrections must be compensating entries, not edits.

## Constraint
Auditors need an immutable history of amount changes.

## Citation
Finance review 2026-04.
