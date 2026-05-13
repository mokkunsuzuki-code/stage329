# Stage329: Audit Artifact Package

Stage329 converts the Stage328 verification decision into a submit-ready audit evidence package.

## Core Concept

AI Claim
↓
Reproduction Evidence
↓
QSP Decision
↓
Signed Audit Report

## What Stage329 Adds

Stage328 produced a verification decision:

- accept
- pending
- reject

Stage329 turns that decision into audit artifacts that can be submitted, reviewed, stored, and verified by third parties.

## Generated Artifacts

- audit_report.json
- audit_report.html
- audit_report.pdf
- verify.txt
- audit_report.sha256
- audit_report.json.asc

## Why This Matters

A decision alone is not enough for real-world audit use.

Enterprises, auditors, governments, and financial institutions need:

- evidence package
- verification trace
- signed report
- machine-readable JSON
- human-readable HTML
- PDF report
- verification instructions

Stage329 moves REMEDA from verification decision to audit submission.

## Security Boundary

The private core logic is not published.

Excluded from GitHub:

- core/
- engine/
- private/
- secrets/
- keys/
- .env
- private keys

Only public audit artifacts and verification instructions are published.

## Verify

```bash
shasum -a 256 docs/reports/audit_report.json

gpg --verify docs/reports/audit_report.json.asc docs/reports/audit_report.json
License

MIT License

Copyright (c) 2025 Motohiro Suzuki
