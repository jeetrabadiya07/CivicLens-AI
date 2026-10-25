# Security Policy

## Supported Versions

CivicLens AI currently maintains the latest release branch.

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability within CivicLens AI:

1. **Do not create a public issue** on GitHub.
2. Email security findings or privately open a GitHub Security Advisory detailing:
   * Description of the vulnerability
   * Steps to reproduce the issue
   * Potential impact on municipal deployments
3. We will acknowledge receipt within 48 hours and work with you to patch the issue before public disclosure.

## Security Controls Implemented

* **Administrative Authorization**: Duplicate confirmation, incident group creation, CSV export, and demo reset endpoints are protected by `X-Admin-API-Key` verification.
* **SQL Injection Protection**: All database queries use parameterized SQLAlchemy queries and ORM objects.
* **Input Validation**: Coordinates are bounded to \([-90, +90]\) and \([-180, +180]\); description lengths are enforced via Pydantic schemas.
* **Privacy by Design**: No personal telephone numbers, national identifiers, or private resident emails are exposed in public API outputs.
* **Error Masking**: Database stack traces are masked behind clean JSON error responses in production environments.
