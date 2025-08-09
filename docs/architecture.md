# Architecture

Flow: GitHub (CSV data) → Azure Data Factory (HTTP Dataset) → ADLS Gen2 (bronze)

1) HTTP Linked Service connects to https://raw.githubusercontent.com/
2) HTTP Dataset constructs the file path dynamically via parameters
3) ForEach iterates over file names
4) Copy activity writes each file to ADLS Gen2 (bronze)
