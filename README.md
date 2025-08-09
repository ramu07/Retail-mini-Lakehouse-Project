# Retail Orders Mini Lakehouse (GitHub → ADF → ADLS Gen2)

Ingest version-controlled CSVs from GitHub into ADLS Gen2 using Azure Data Factory.
Includes parameterized HTTP and ADLS datasets, and a ForEach + Copy pipeline.

## Layout
- data/: sample CSVs
- adf/: linked services, datasets, pipeline JSON
- docs/: architecture and runbook

## Quick Start
1) Push this repo to GitHub (main branch).
2) In ADF, create linked services & datasets matching JSON names.
3) Import or recreate `pl_copy_github_to_adls`.
4) Trigger with parameters in docs/runbook.md.
