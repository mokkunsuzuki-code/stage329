# REMEDA Stage329: Evidence Match Gate + Audit Submission Package

Stage329 extends the Stage328 Evidence Match Gate into a submit-ready audit artifact workflow.

## Core Flow

AI Claim  
↓  
Reproduction Evidence  
↓  
Stage328 Evidence Match Gate  
↓  
accept / pending / reject  
↓  
Stage329 Signed Audit Report  

## What Stage329 Adds

- Stage328 interactive verification page
- Stage327 + Stage328 integrated builder
- Machine-readable Stage328 decision JSON
- Stage329 audit submission layer
- Signed audit report
- Audit JSON
- Audit signature
- Verification instructions
- Japanese and English public pages

## Public Pages

Japanese:

https://mokkunsuzuki-code.github.io/stage329/

English:

https://mokkunsuzuki-code.github.io/stage329/en/

## Public Verification Files

- `docs/index.html`
- `docs/en/index.html`
- `docs/reports/audit_report.html`
- `docs/reports/audit_report.json`
- `docs/reports/audit_report.json.asc`
- `docs/reports/audit_report.sha256`
- `docs/reports/verify.txt`

## Security Boundary

Private core logic is not published.

Excluded from GitHub:

- `core/`
- `engine/`
- `private/`
- `secrets/`
- `keys/`
- `.env`
- private keys

Only public verification artifacts and audit submission files are published.

## Verify

```bash
shasum -a 256 docs/reports/audit_report.json

gpg --verify docs/reports/audit_report.json.asc docs/reports/audit_report.json
License

MIT License

Copyright (c) 2025 Motohiro Suzuki
