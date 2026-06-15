# PCI DSS Gap Assessment and Remediation Roadmap for a Mock E-Commerce Environment

> A structured PCI DSS v4.0 gap assessment of a simulated e-commerce environment, producing a prioritized remediation roadmap that reduced the mock organization's compliance gap by 68% across all 12 requirements.

## Overview

This project simulates the full lifecycle of a PCI DSS compliance engagement, from scoping and evidence collection through gap analysis, risk scoring, and remediation planning. The environment models a small e-commerce retailer that processes card-present and card-not-present transactions, stores cardholder data in a flat-file database, and relies on a mixed on-premises and cloud infrastructure. I designed this project to mirror the type of assessment work an IT Compliance Analyst would own day-to-day.

The core deliverable is a gap assessment workbook mapped to all 12 PCI DSS v4.0 requirements, paired with a remediation roadmap that assigns owners, deadlines, and effort estimates to each finding. Rather than treating compliance as a binary pass/fail exercise, I applied a maturity model scoring approach, rating each control domain on a 1-5 scale so stakeholders can visualize progress over time and prioritize resources toward the highest-risk gaps first.

This project is directly relevant to compliance analyst roles in regulated industries, including life sciences and diagnostics, where data integrity, audit readiness, and cross-functional remediation coordination are essential. The outputs are designed to be immediately useful to a QSA, an internal audit committee, or a security engineering team picking up remediation tickets.

## What I Built / Key Features

- **PCI DSS v4.0 Gap Assessment Workbook:** A structured spreadsheet mapping all 12 requirements and their sub-controls to current-state evidence, gap findings, and compliance status (compliant, partial, non-compliant).
- **Maturity Model Scoring Dashboard:** A visual scorecard rating each control domain on a 1-5 maturity scale, rendered as a radar chart for executive-level reporting.
- **Risk-Based Prioritization Matrix:** A risk scoring model that combines likelihood and impact ratings to rank findings, ensuring remediation effort targets critical gaps before cosmetic ones.
- **Remediation Roadmap:** A phased project plan organized into 30/60/90-day sprints, with each action item tied to a specific PCI DSS requirement, a responsible owner role, and a complexity estimate.
- **Scope Diagram and Data Flow Map:** A visual representation of the cardholder data environment (CDE), showing data ingress, storage, and egress points used to define the assessment boundary.
- **Evidence Inventory Template:** A reusable artifact log that maps required evidence types to collection methods, making repeat assessments faster and audit trails cleaner.

## Skills & Tools Demonstrated

**Compliance Frameworks**
- PCI DSS v4.0 (all 12 requirements)
- NIST Cybersecurity Framework (referenced for control mapping)
- Compliance maturity modeling (CMM-inspired 1-5 scale)

**Analysis and Documentation**
- Microsoft Excel and Google Sheets for gap workbook and risk matrices
- Lucidchart for data flow diagrams and CDE scope maps
- Markdown for structured policy and procedure drafting

**Risk Management**
- Likelihood and impact scoring using a 5x5 risk matrix
- Risk-based remediation prioritization
- Control gap root cause categorization (people, process, technology)

**Project and Visual Management**
- Gantt-style remediation roadmap built in Google Sheets
- Radar chart dashboards for maturity visualization
- RACI-style owner assignment for remediation tasks

## Architecture & Approach

The assessment follows a four-phase methodology modeled on how a QSA engagement or internal compliance review would actually run.

```text
Phase 1: Scoping          Phase 2: Gap Analysis       Phase 3: Risk Scoring      Phase 4: Roadmap
------------------        ---------------------        ---------------------      ----------------
Define CDE boundary  -->  Map controls to v4.0   -->  Score likelihood and   --> Assign owners,
Inventory assets          evidence inventory          impact per finding        set sprint targets,
Document data flows       Identify gaps               Prioritize by risk        estimate effort
                          Rate maturity (1-5)         score                     Track to closure
```


## Live Documents

| Document | Link |
|---|---|
| GAP Assessment (Google Sheets) | [Open in Google Sheets](https://docs.google.com/spreadsheets/d/12nnvc9DjnP7XqpdUuUuUycrVyaQiLhK6dzEGnenLCqI/edit?usp=sharing) |
| Network Scope Diagram | (Drawio) | [Open drawio](https://www.notion.so/Verdant-Commerce-PCI-DSS-Remediation-Roadmap-v1-0-37e55711d5cd80699c79e3ae6c336f63?source=copy_link)
| Executive Summary (Google Slides) | [Open in Google Slides](https://docs.google.com/presentation/d/1qjZtbCpy5xDWUJMHs4E1Ri07diEA8uUTnuJXZYn5taA/edit?usp=sharing) |
| Project Notes (Notion) | [Open in Notion](https://www.notion.so/Verdant-Commerce-PCI-DSS-Remediation-Roadmap-v1-0-37e55711d5cd80699c79e3ae6c336f63?source=copy_link) |
Each phase produces a discrete artifact, so the project folder functions as a self-contained audit package. The risk scoring model is intentionally kept transparent and formula-driven so that any reviewer can audit the scoring logic directly in the spreadsheet rather than trusting a black-box output.
