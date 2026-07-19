# Public release audit — Notebooks 0.6.1

Audit date: 2026-07-19  
Target: Windows x64 public testing preview  
Decision: **Pass for public testing with the limitations below**

## Public Git boundary

The Git repository is deliberately an information-and-download companion, not a source distribution. Its allowlist contains only:

- Product overview and usage documentation
- Security and third-party notices
- Three curated screenshots created with the public field guide
- The portable public `Notebooks Field Guide.inkbook`
- This verification report

Application code, tests, build scripts, package manifests, dependencies, build output, local application data, private books, recovery snapshots, proof profiles, logs, and internal tools are ignored. The installer is also ignored by Git and is prepared separately as a GitHub Release asset.

## Companion book

The public **Notebooks Field Guide** was validated successfully:

- 12 physical pages
- 4 chapters
- 8 indexed highlights
- 0 external assets
- Composition-style cover
- User and agent instructions for the shelf, writing, finite pages, paper, indexes, import/export, privacy, structured authoring, validation, and handoff

A clean packaged profile passed the complete flow: **Guide → import preview → Import notebook → open the 12-page, 4-chapter guide**.

## Verification evidence

- Automated application suite: **72 passed, 0 failed**
- Dependency audit at build time: **0 known vulnerabilities**
- Production renderer build: **passed**
- Windows NSIS package: **passed**
- Packaged regression: **passed**
  - 816 × 1056 physical letter sheet
  - College-rule line height 26.8346 px (7.1 mm at 96 DPI)
  - Heading baseline deltas 0.00 px and -0.02 px
  - Finite overflow pagination and backward reflow
  - Search, trash recovery, chapters, Cover Studio, portability, autosave, and recovery points
- Packaged public UI proof: **passed at 1424 × 875 with no document-level horizontal overflow**
- Packaged privacy scan: **no known personal paths or named personal books found**

## Installer

- Release asset: `Notebooks-Setup-0.6.1.exe`
- Size: 122,687,136 bytes
- SHA-256: `8E9AA52471B227B6354B870A0428B3C1DE6E913DE544425FC291800D1A05C394`

## Known preview limitations

1. The installer and executable are not code-signed. Windows can display an unknown-publisher warning.
2. Windows x64 is the verified target.
3. The preview is local-first and under active development. Testers should export important books before upgrading or experimenting with recovery.
4. The GitHub repository does not distribute application source or grant source reuse rights.
