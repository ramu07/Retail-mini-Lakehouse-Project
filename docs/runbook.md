# Runbook — GitHub → ADLS Ingestion

## Prerequisites
- CSVs under `data/` folder in this GitHub repo
- ADLS Gen2 storage account
- ADF Managed Identity has `Storage Blob Data Contributor` on storage account

## Pipeline Parameters
- pOwner: <your GitHub username>
- pRepo: retail-mini-lakehouse
- pBranch: main
- pFiles: ["customers.csv","products.csv","orders.csv","order_items.csv"]
- pAdlsContainer: bronze
- pAdlsDirectory: ingest/retail/

## Execute
- Trigger `pl_copy_github_to_adls` with the above values
- Validate files at: abfss://bronze@<storage>.dfs.core.windows.net/ingest/retail/

## Troubleshooting
- HTTP 404: Confirm file path and branch
- ADLS write fail: Check IAM role on storage account
