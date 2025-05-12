# TCR-Analysis
This repository contains a Quarto-based R analysis pipeline for T-cell receptor (TCR) repertoire data. The workflow is designed to preprocess, clean, and analyze multiple TCR sequencing datasets based on immunogenomics principles.

## Overview
The main objectives of this analysis pipeline include:
- Loading and combining multiple .csv TCR-seq files
- Cleaning and standardizing sample identifiers
- Classifying samples by antigen type
- Filtering and visualizing TCR repertoire features

## Requirements
Ensure the following R packages are installed:

install.packages(c("dplyr", "readr", "stringr", "ggplot2"))
install.packages("ggseqlogo")
install.packages("patchwork")

## File Structure
- TCR 200325.qmd – Main Quarto file that performs the analysis and generates an HTML report.
- TCR .csv files – Raw data files expected in the working directory (TCRseq_data).

## How to Use
1. Place all .csv TCR sequencing files into the directory TCRseq_data.
2. Open the TCR 200325.qmd file in RStudio.
3. Set your working directory in R to match the path of the data files:

setwd("path/to/TCRseq_data")

4. Render the Quarto file using the Render button in RStudio or:

quarto::quarto_render("TCR 200325.qmd")

## Output
The output HTML report includes:
- Cleaned and combined TCR data
- Sample classification based on antigen type
- Filtering criteria applied
- Visualizations including sequence logos and ggplot2 summaries
