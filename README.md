# World University Rankings – Data Visualization Project

This project explores the **World University Rankings** dataset using R, focusing on data cleaning, exploratory data analysis (EDA), and visualizations to understand patterns in university performance worldwide.

## Project Overview

- Load and inspect the CWUR (Center for World University Rankings) dataset.
- Perform basic data cleaning (handling missing values, type conversions).
- Explore the structure and summary statistics of the data.
- Compute correlations for numeric variables.
- Create visualizations such as histograms, boxplots, and bar charts.

## Repository Structure

- [World University Rankings.Rproj](World%20University%20Rankings.Rproj) – RStudio project file.
- [data/](data/) – Contains the raw dataset:
  - [cwurData.csv](data/cwurData.csv)
- [scripts/](scripts/) – R Markdown scripts for analysis and data loading:
  - [load_data.Rmd](scripts/load_data.Rmd) – Loads the CWUR dataset, performs initial cleaning, EDA, and basic visualizations.
- [report/](report/) – Project report files:
  - [project_report.Rmd](report/project_report.Rmd) – Main analysis report (R Markdown).
  - [project_report.html](report/project_report.html) – Rendered HTML report.
- [output/](output/) – Folder for saving any generated figures or intermediate outputs.
- [presentation/](presentation/) – Folder for slides or presentation material (if used).
- [renv/](renv/) – Dependency management folder created by the renv package.

## Main Scripts

### scripts/load_data.Rmd

This script:
- Installs/loads required packages (e.g., `readr`, `dplyr`, `GGally`).
- Reads the dataset from `data/cwurData.csv`.
- Prints dataset dimensions, structure, and summary statistics.
- Checks missing values and the number of unique values per column.
- Optionally removes rows with missing values.
- Ensures `world_rank` is numeric if present.
- Computes a correlation matrix for numeric variables.
- Optionally creates:
  - Pairwise scatterplots using `GGally::ggpairs`.
  - A boxplot for `score`.
  - A histogram of `world_rank`.
  - A bar chart of the top 10 countries by number of universities.

## Requirements

This project is written in **R** and uses the following key packages (among others managed by renv):

- `readr`
- `dplyr`
- `GGally`
- `ggplot2`
- `rmarkdown`

The exact package versions are managed by `renv` inside the project.

## How to Run the Project

1. **Open the project**
   - Open [World University Rankings.Rproj](World%20University%20Rankings.Rproj) in RStudio.

2. **Restore the R environment (recommended)**
   - In the R console, run:
     - `install.packages("renv")` (if not already installed)
     - `renv::restore()`

3. **Run the data loading and EDA script**
   - Open [scripts/load_data.Rmd](scripts/load_data.Rmd).
   - Knit the document ("Knit" button in RStudio) or run chunks interactively.

4. **Generate the main report**
   - Open [report/project_report.Rmd](report/project_report.Rmd).
   - Click "Knit" to generate [report/project_report.html](report/project_report.html).

## Data Source

The dataset [cwurData.csv](data/cwurData.csv) is based on university rankings published by the **Center for World University Rankings (CWUR)**. Please consult CWUR for original data and licensing details.

## Reproducibility

- Use `renv::snapshot()` after adding or updating packages to keep the environment lockfile in sync.
- Re-run the R Markdown files to reproduce all tables and figures.

## Contact

If you have questions or suggestions for improving this analysis, feel free to open an issue or modify the project and extend the visualizations and models.
