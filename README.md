# NBA_InjuryCollection
This project provides a **robust pipeline for analyzing NBA injury datasets** from CSV files.  
It automatically detects and standardizes column names, categorizes injuries, groups them into episodes, and generates a multi-sheet Excel report with detailed summaries.

## Features
- **Automatic CSV detection** – no need to hardcode filenames.
- **Flexible column mapping** – handles variations in column names (e.g., "Player Name" vs. "Player").
- **Injury categorization** – surgery, non-contact, illness, fracture, etc.
- **Episode grouping** – merges related injuries within 7 days into single episodes.
- **Player summaries** – total episodes, sidelined days, and more.
- **Excel output** – creates one file with multiple sheets:
  - `Raw+Labels` – raw data with standardized columns and injury labels
  - `Episodes` – merged episodes with start/end dates
  - `PlayerSummary` – per-player injury summaries

## Output
The script generates:

- **`injury_analysis.xlsx`**
  - Sheet 1: `Raw+Labels`  
  - Sheet 2: `Episodes`  
  - Sheet 3: `PlayerSummary`

The file is automatically downloaded when running in Google Colab.

## Getting Started

### 1. Open in Google Colab
- Upload your CSV injury dataset to the Colab working directory.  
- Or place multiple `.csv` files in the Colab file system – the script will auto-detect the right one.

### 2. Install Dependencies
This project requires:
- `pandas`
- `openpyxl`

In Colab these are preinstalled, but if needed, run:

```bash
pip install pandas openpyxl
