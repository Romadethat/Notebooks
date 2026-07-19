# Security policy

## Supported version

Only the newest public testing preview is supported. This is local-first desktop software and should not be treated as a hardened multi-user or enterprise system.

## Reporting a vulnerability

Do not open a public issue containing exploit details, personal notebooks, private paths, or secrets. Use GitHub's private vulnerability reporting feature for this repository when it is enabled. If it is unavailable, open a minimal issue asking the maintainer for a private reporting channel without including sensitive details.

Include the application version, Windows version, reproduction steps, expected behavior, actual behavior, and whether the issue requires a crafted `.inkbook` file.

## Book safety model

- Opening and importing an Inkbook must not execute book-supplied code.
- Imported HTML and SVG content is sanitized before rendering.
- Reference assets are read only from the application-owned book-assets directory.
- Skill installation, trust, enable/disable, and removal are separate user-approved actions.
- Treat books downloaded from unknown sources as untrusted data and inspect their import preview.

## Privacy

Never attach a complete application data directory, recovery snapshot, or private Inkbook to a public report. Create a minimal test book with invented content instead.

