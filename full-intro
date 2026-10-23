# WBSA Community Edition

**Peptide mass spectrometry · Computational chemistry · Scientific visualization · Research software engineering**

WBSA Community Edition is an integrated scientific computing platform for interpreting peptide tandem mass spectrometry (MS/MS) data. It connects chemical hypothesis modeling, fragment-ion analysis, interactive visualization, and persistent research records within a locally deployed browser application. Researchers supply a peptide sequence, a prepared experimental peak list, and modification information to investigate how observed fragmentation supports alternative chemical assignments.

## Scientific Scope and Research Value

WBSA brings three complementary analytical workflows into a common environment:

| Workflow | Scientific capability |
|---|---|
| **Manual Annotation** | Match experimental peaks to theoretical peptide fragments under specified modification assignments, charge states, neutral losses, and mass tolerances. |
| **Auto Localization** | Compare candidate modification positions using fragment evidence, ranked hypotheses, relative support, and ambiguity reporting. |
| **Lanthiopeptide Chemistry** | Explore chemically constrained hypotheses using official presets or custom rules for modification combinations, occurrence counts, and residue-specific restrictions. |

The computational framework links molecular mass calculations and theoretical fragmentation to observed signals. Candidate-level evidence, sequence coverage, and mass-error plots allow researchers to examine why an assignment is supported and where evidence remains incomplete. Lanthiopeptide analysis offers both the original scoring method and an alternative ranking based on serine/threonine–cysteine (S/T–C) fragmentation evidence.

Scores and relative probabilities describe support within an evaluated condition; they are uncalibrated and do not establish experimental accuracy or prove ring opening. The [scientific user guide](docs/user-guide.md) defines the methods, interpretation, and scope.

## Integrated Software Engineering

- **Full-stack architecture.** A React, Next.js, and TypeScript interface integrates with a Python scientific engine through a Django REST API. Distinct analysis, presentation, persistence, and export components organize the system around the research workflow.
- **Controlled computation.** Lanthiopeptide analyses use explicit execution budgets, bounded concurrency, calculation caching, progress reporting, and cancellation. Partial, failed, and completed outcomes remain distinguishable during hypothesis exploration.
- **Traceable research records.** SQLite-backed plans and results preserve input/output snapshots and method metadata. Explicit reruns, saved spectrum views, and configuration snapshots support repeatable analysis and retrospective review.
- **Extensible chemical models.** Versioned configuration files express modification rules independently of the interface. Read-only official presets, editable custom libraries, and migration of earlier configuration formats support evolving research questions.
- **Interactive scientific communication.** Spectrum exploration, peptide coverage, and figure editing connect numerical results with interpretable visual evidence. Presentation edits preserve scientific result values; CSV, HTML, SVG, PDF, Word, and Excel exports support further analysis and reporting.

Together, these capabilities connect experimental questions to computational hypotheses, inspectable evidence, and reusable research records. The engineering contribution is a coherent environment for conducting and communicating scientific analysis.

## Engineering Evidence

The repository includes scientific regression suites, API and persistence checks, export verification, frontend checks, and isolated verification runners. Recorded executions cover calculations, saved-data behavior, type checking, and application builds. The [verification record](test/verification-results.md) also documents dependency-related failures and outstanding target-runtime, browser, container, security, and independently reviewed experimental validation. The [testing guide](docs/testing.md) distinguishes implemented checks from executed evidence.

## Access and Documentation

WBSA is designed for local research use. Docker Compose defines separate web and API services, health checks, and persistent storage. Setup guidance covers **macOS, Windows, and Linux**; platform requirements and verification status are documented in the [installation guide](docs/installation.md). The [Windows Edition guide](docs/windows.md) describes installer and launcher support, with distributable builds and Windows-host acceptance testing still required.

- **Install and operate:** [Installation](docs/installation.md) · [Architecture and deployment](docs/deployment.md)
- **Learn the workflows:** [User guide](docs/user-guide.md) · [English / Chinese offline guide](docs/WBSA_User_Guide_ZH_EN.html)
- **Explore example inputs:** [Manual Annotation](demos/manual/demo.ts) · [Auto Localization](demos/auto/demo.ts) — constructed demonstrations with documented provenance.
- **Extend the analysis:** [Chemical configuration libraries](docs/modification-sets.md) · [Repository overview](README.md)
