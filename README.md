# 20260421_natashaHarvey_gata2_mouse
Affymetrix Array data processing for Jan's Gata2 2011 assay

# GATA2 Mouse Microarray Analysis (MoGene-1_0-st-v1)

## Overview

This project processes Affymetrix Mouse Gene 1.0 ST array (.CEL) files using R (v4.5.2) and Bioconductor. Data are normalized using the Robust Multi-array Average (RMA) method via the `oligo` package.

## Data Source

Raw CEL files are stored on a mounted HPC filesystem:

~/hpc_mount/uofaresstor/sacgf/sacgf/molpath/data/analysis/2011JanKazenWadel_Gata2_Array/GATA2 Affy Arrays/Mouse Genearrays

To avoid duplication, symbolic links are used within this project.

## Project Structure

project/
├── data/
│   ├── raw/          # symlinks to CEL files
│   ├── processed/    # normalized expression matrices
├── scripts/          # R scripts
├── results/          # downstream outputs
├── README.md

## Processing Steps

1. Symlink CEL files into `data/raw/`
2. Load CEL files using `oligo`
3. Perform RMA normalization
4. Save:

   * Expression matrix
   * Sample metadata
   * Session info

## Reproducibility

* R version: 4.5.2
* Platform: Affymetrix MoGene-1_0-st-v1
* Normalization: RMA
* All paths are relative within the project
* Package versions recorded via `sessionInfo()`

## Notes

* Original array design based on mm9; annotations may be updated
* No raw data duplication (symlinks used)

