# SBOM + SAST Analyzer

Public overview of a Python-based security analysis tool designed to combine **SBOM parsing**, **static analysis concepts**, **vulnerability enrichment**, and **report generation** into a single workflow.

> **Note:** The full source code for this project is kept private.  
> This repository is a public overview intended to showcase the system architecture, main features, and sample outputs.

---

## Project Overview

Modern software security requires more than isolated checks. In practice, teams need visibility into:
- which dependencies are used,
- whether known vulnerabilities affect them,
- how risky the findings are,
- and how results can be reported in a structured way.

This project was built to address that workflow by combining **SBOM-based dependency analysis** with **security checks and reporting modules** in a modular Python system.

The result is a tool that helps transform raw dependency and vulnerability information into a more usable **security review output**.

---

## Motivation

Software projects often depend on many third-party packages, libraries, and components.  
This creates a security challenge:

- dependencies may contain known CVEs,
- teams may lack a quick way to prioritize findings,
- outputs from different checks are often fragmented,
- and reporting is frequently inconsistent.

The goal of this project is to create a structured analysis pipeline that:
1. reads SBOM data,
2. checks for vulnerability-related information,
3. evaluates risk,
4. and produces readable reports.

---

## Core Features

### 1. SBOM Parsing
- Parses Software Bill of Materials (SBOM) data
- Extracts dependency/component information
- Normalizes package data for later analysis stages

### 2. Vulnerability Enrichment
- Enriches dependency data with vulnerability intelligence
- Supports CVE-oriented checking logic
- Connects package information to security findings

### 3. Risk Scoring
- Assigns severity/risk-based interpretation to findings
- Helps prioritize vulnerable components
- Supports more practical triage instead of raw vulnerability dumps

### 4. Report Generation
- Produces structured outputs for review
- Supports export-oriented reporting flows
- Designed for security analysis summaries such as:
  - HTML reports
  - PDF reports
  - CSV/text-based outputs

### 5. Modular Design
The system is organized into separate modules for:
- parsing,
- CVE checking,
- risk calculation,
- configuration loading,
- and report generation.

This makes the project easier to extend and maintain.

---

## High-Level Architecture

The project follows a modular pipeline:

1. **Input ingestion**
2. **SBOM parsing**
3. **Dependency / vulnerability enrichment**
4. **Risk scoring**
5. **Output generation**

### Main modules
- `sbom_parser.py`
- `cve_checker.py`
- `cve_api.py`
- `risk.py` / `risk_calculator.py`
- `report_generator.py`
- `config_loader.py`

This separation allows the tool to keep analysis logic, risk interpretation, and reporting concerns decoupled.

---

## Example Workflow

A typical run follows this flow:

1. A project SBOM is provided as input
2. Dependencies are extracted and normalized
3. Known vulnerability information is checked/enriched
4. Risk is calculated or categorized
5. A final report is generated for review

This makes the tool useful for secure development workflows where dependency visibility and vulnerability tracking matter.

---

## Tech Stack

- **Language:** Python
- **Security Focus:** SBOM analysis, vulnerability enrichment, reporting
- **Outputs:** HTML, PDF, CSV/text-oriented summaries
- **Architecture Style:** Modular analysis pipeline

---

## Sample Outputs

This overview repository includes example artifacts in the `docs/` folder such as:

- architecture diagram
- workflow illustration
- sample report screenshot
- risk summary screenshot

See:
- `docs/architecture.png`
- `docs/workflow.png`
- `docs/sample-report.png`
- `docs/risk-summary.png`

---

## Why This Project Matters

This project is relevant to modern **Application Security / Product Security** workflows because it sits at the intersection of:

- software supply chain security,
- dependency visibility,
- vulnerability management,
- and actionable reporting.

Rather than treating security data as scattered output, the project focuses on turning it into a more structured and reviewable analysis process.

---

## Future Improvements

Possible future extensions include:

- CI/CD integration
- richer vulnerability intelligence sources
- policy-based fail/pass decisions
- trend/history views across multiple scans
- dashboard-oriented visualization
- improved prioritization logic for remediation workflows

---

## Project Status

This repository is a **public overview** of the project.  
The implementation repository remains private.

If needed, this showcase can be extended with:
- additional screenshots,
- sample reports,
- redacted example inputs,
- or a short demo video.

---

## Contact

If you would like to learn more about the project, feel free to connect through my GitHub profile or LinkedIn.

- GitHub: [omerdemirci44](https://github.com/omerdemirci44)
- LinkedIn: [omer-talha-demirci](https://www.linkedin.com/in/omer-talha-demirci)

---
