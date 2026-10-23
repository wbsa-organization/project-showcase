# WBSA Community Edition

**Peptide mass spectrometry · Computational chemistry · Scientific visualization · Research software engineering**

- **Scientific purpose:** Interpret peptide tandem mass spectrometry (MS/MS) data and investigate chemical modification assignments through fragment evidence.
- **Integrated platform:** Combine chemical hypothesis modeling, computational analysis, interactive visualization, and persistent research records in a local browser application.
- **Research workflow:** Supply a peptide sequence, prepared experimental peak list, and modification information; compare hypotheses, inspect evidence, and preserve results.

## Scientific Scope and Research Value

- **Manual Annotation:** Match experimental peaks to theoretical peptide fragments using specified modifications, charge states, neutral losses, and mass tolerances.
- **Auto Localization:** Compare candidate modification positions through ranked hypotheses, relative support, and ambiguity reporting.
- **Lanthiopeptide Chemistry:** Explore chemically constrained hypotheses using official presets or custom rules for modification combinations, occurrence counts, and residue restrictions.
- **Evidence-based interpretation:** Connect molecular mass calculations to observed signals through fragment assignments, sequence coverage, and mass-error plots.
- **Complementary ranking:** Examine lanthiopeptide candidates using the original scoring method or an alternative based on serine/threonine–cysteine (S/T–C) fragmentation evidence.
- **Defined scientific scope:** Scores and probabilities express uncalibrated support within an evaluated condition; they do not establish experimental accuracy or prove ring opening. See the [scientific user guide](docs/user-guide.md).

## Integrated Software Engineering

- **Full-stack architecture:** React, Next.js, and TypeScript integrate with a Python scientific engine through a Django REST API, separating analysis, presentation, persistence, and exports.
- **Controlled computation:** Execution budgets, bounded concurrency, caching, progress reporting, and cancellation govern lanthiopeptide analyses, with explicit completion, partial-result, and failure states.
- **Traceable research records:** SQLite-backed plans and results preserve input/output snapshots and method metadata; explicit reruns and saved configurations support repeatable analysis.
- **Extensible chemical models:** Versioned configuration files, read-only official presets, editable custom libraries, and format migration accommodate evolving research questions.
- **Interactive visualization:** Spectrum exploration, peptide coverage, figure editing, and saved views support evidence inspection while preserving scientific result values.
- **Research communication:** CSV, HTML, SVG, PDF, Word, and Excel exports connect computational results to further analysis, figures, and reports.

## Engineering Evidence

- **Verification framework:** Scientific regression suites, API and persistence checks, export verification, frontend checks, and isolated runners address computational and application behavior.
- **Recorded evidence:** Executed checks cover calculations, saved-data behavior, type checking, and application builds. The [testing guide](docs/testing.md) distinguishes implemented checks from executed evidence.
- **Remaining validation:** The [verification record](test/verification-results.md) documents dependency-related failures and outstanding target-runtime, browser, container, security, and independently reviewed experimental validation.

## Access and Documentation

- **Local deployment:** Docker Compose defines separate web and API services, health checks, and persistent storage. See [architecture and deployment](docs/deployment.md).
- **Operating environments:** [Installation guidance](docs/installation.md) covers macOS, Windows, and Linux, including platform requirements and verification status.
- **Windows Edition:** [Installer and launcher documentation](docs/windows.md) is available; distributable builds and Windows-host acceptance testing remain required.
- **Learn the workflows:** [User guide](docs/user-guide.md) · [English / Chinese offline guide](docs/WBSA_User_Guide_ZH_EN.html)
- **Explore example inputs:** [Manual Annotation](demos/manual/demo.ts) · [Auto Localization](demos/auto/demo.ts) — constructed demonstrations with documented provenance.
- **Extend the analysis:** [Chemical configuration libraries](docs/modification-sets.md) · [Repository overview](README.md)
