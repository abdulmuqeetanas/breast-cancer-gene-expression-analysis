# Breast Cancer Gene Expression Analysis

## Overview

This project analyzes gene expression differences between breast tumor tissue and paired normal breast tissue using publicly available microarray data from the NCBI Gene Expression Omnibus (GEO).

The analysis was performed in Python and includes data processing, differential expression analysis, statistical testing, multiple-testing correction, gene annotation, and visualization.

**Dataset:** GSE15852  
**Platform:** GPL96 – Affymetrix Human Genome U133A Array  
**Samples:** 86 total samples  
- 43 breast tumor samples
- 43 paired normal breast tissue samples

## Project Objective

The objective of this project was to identify probe sets showing significant differences in expression between breast tumor and paired normal tissue and to map those probe sets to biological gene annotations.

This project also demonstrates the use of Python for working with real biological datasets and performing a reproducible bioinformatics analysis.

## Tools and Technologies

- Python
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib
- Google Colab
- NCBI Gene Expression Omnibus (GEO)
- Affymetrix GPL96 annotation

## Analysis Workflow

The analysis included the following steps:

1. Imported the GSE15852 gene expression dataset from NCBI GEO.
2. Explored a gene expression matrix containing 22,283 probe sets across 86 samples.
3. Separated the samples into 43 paired normal and 43 tumor samples.
4. Calculated mean expression levels for tumor and normal tissue.
5. Calculated log2 fold change for each probe set.
6. Performed paired t-tests to account for the matched tumor-normal study design.
7. Applied Benjamini-Hochberg false discovery rate (FDR) correction for multiple testing.
8. Identified significantly differentially expressed probe sets using:
   - Adjusted p-value < 0.05
   - Absolute log2 fold change ≥ 1
9. Mapped Affymetrix probe-set IDs to gene symbols using the GPL96 platform annotation.
10. Generated volcano and gene-level visualizations.
11. Exported significant results to CSV.

## Key Results

A total of **443 probe sets** met both the statistical significance and fold-change thresholds.

- **181 probe sets** showed higher expression in breast tumor tissue.
- **262 probe sets** showed lower expression in breast tumor tissue.

The analysis identified substantial differences in gene expression between breast tumor and paired normal breast tissue.

Examples appearing among the highly significant annotated results included **ADIPOQ, AKR1C1, FABP4, G0S2, CDKN1C, TNS1, CHRDL1, and PDZD2**.

These findings represent associations with tumor status and should not be interpreted as evidence that individual genes cause breast cancer.

## Visualizations

The project includes:

- Volcano plot of differential expression results
- Highlighted significant probe sets based on FDR and fold-change thresholds
- Visualization of genes with large expression differences between tumor and normal tissue

The complete visualizations and analysis workflow are available in the Jupyter notebook.

## Repository Files

### `Breast_Cancer_Gene_Expression_Analysis.ipynb`

Complete Python analysis including data import, processing, statistical testing, annotation, and visualization.

### `GSE15852_significant_results.csv`

Exported results for the 443 significant probe sets, including:

- Gene symbol
- Gene title
- Normal mean expression
- Tumor mean expression
- Log2 fold change
- Raw p-value
- FDR-adjusted p-value

## Skills Demonstrated

This project demonstrates experience with:

- Biological data analysis using Python
- Pandas DataFrame manipulation
- Gene expression analysis
- Microarray data
- Statistical hypothesis testing
- Paired t-tests
- Multiple-testing correction
- False discovery rate (FDR)
- Log2 fold-change analysis
- Gene/probe annotation
- Biological data visualization
- Working with NCBI GEO datasets
- Reproducible Jupyter/Google Colab workflows
- GitHub project documentation

## Limitations

This is an exploratory educational bioinformatics project.

The differential expression analysis was performed at the Affymetrix probe-set level. Multiple probe sets may represent the same gene, and some probe sets may map to multiple gene symbols.

Gene expression differences demonstrate associations with tumor status but do not establish biological causation.

Additional validation, alternative statistical methods, functional enrichment analysis, and independent datasets would be required before making stronger biological or clinical conclusions.

## Data Source

NCBI Gene Expression Omnibus (GEO)  
Accession: **GSE15852**  
Platform: **GPL96**

## Author

**Abdul Muqeet Anas**

Biology graduate and incoming M.S. Bioinformatics student at George Mason University with interests in bioinformatics, computational biology, biological data analysis, and genomics.
