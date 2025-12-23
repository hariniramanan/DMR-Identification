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

A genomic region is accepted as a Differentially Methylated Region (DMR) only if all of the following conditions are satisfied:
1. The region must contain ≥ 3 consecutive CpG sites: Ensures the signal is regional, not driven by a single CpG.
2. The absolute methylation difference (Δβ) between case and control must be:
                            ≥ 20% (|Δβ| ≥ 0.20)
3. The total genomic span of the region must satisfy:  Region width / number of CpGs ≤ 176 bp

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
