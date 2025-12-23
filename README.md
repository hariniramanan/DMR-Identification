# DMR-Identification

## Overview
This repository contains code and workflows for identifying Differentially Methylated Regions (DMRs)
from genome-wide DNA methylation datasets using R/Bioconductor packages, primarily **DMRcate**
and **bumphunter**.

The project focuses on statistically robust and biologically informed DMR detection strategies,
including region-level filtering and comparative method evaluation.

## Methods
The DMR identification workflow includes:
- Preprocessing and quality control of DNA methylation data
- Identification of differentially methylated CpG sites
- Region-level aggregation using:
  - DMRcate (kernel smoothing–based approach)
  - bumphunter (bump hunting approach)
- Filtering DMRs based on:
  - Minimum number of CpG sites
  - Effect size (delta-beta)
  - Statistical significance
  - Genomic span constraints

## Tools and Packages
- R (>= 4.x)
- Bioconductor
- DMRcate
- bumphunter
- limma
- tidyverse

## Data
Input data consist of genome-wide DNA methylation profiles (e.g., Illumina 450K/EPIC arrays).
Raw data are not included due to size and privacy constraints.

## Output
The pipeline produces:
- Tables of identified DMRs with genomic coordinates
- Effect size and statistical metrics
- Summary plots for downstream interpretation

## License
MIT License
