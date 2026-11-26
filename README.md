# RCC-Gene-Expression-Analysis
  
This project investigates whether gene expression patterns from RNA sequencing (RNA-seq) can distinguish clear cell renal cell carcinoma (ccRCC) from non-clear cell renal cell carcinoma (nccRCC).


<div align="center">
  <img src="pic/Renal Cell Carcinoma Research Workflow Infographic.png" alt="Blikit" />
</div>

This image is created by Astra ;)

## Content

- [main goal](#main-goal)
- [methodology](#methodology)
- [dataset](#dataset)
- [feature selection](#feature-selection)
- [results](#result)
- [limitation](#limitation)


## Main Goal

> **Which transcriptomic features consistently help distinguish clear cell from non-clear cell renal cell carcinoma within the GSE312695 cohort?**

## Methodology

the code flow, followed these steps:

1. Data preparation: Match RNA-seq expression data with cancer subtype labels.

2. Quality control: Examine sequencing counts and low-expression genes.

3. Feature selection: Use ANOVA F-scores to select 300 genes within each training fold.

4. Model training: Compare Logistic Regression, Random Forest, and XGBoost.

5. Evaluation: Apply repeated stratified 5-fold cross-validation (3 repetitions).

6. Biological analysis: Examine gene-selection stability, expression differences, and pathway enrichment.

7. Sensitivity analysis: Evaluate different feature counts and the exclusion of low-count samples.

## Dataset

- [Link](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE312695)

## Feature Selection

<div align="center">
  <img src="pic/Feature Selection Pipeline Infographic.png" alt="" />
</div>

This image is created by Astra ;(

## Result

sorry, but honestly  I'm really impressed by classical models.

|Model | Balanced Accuracy | Macro F1 | ROC-AUC |
|---|---:|---:|---:|
|Logistic Regression | 0.9518 | 0.9273 | 0.9641 |
|Random Forest | 0.9401 | 0.9200 | 0.9605 |
|XGBoost | 0.8721 | 0.8784 | 0.9598 |


### Limitation

My main limitation is that, I don't know that the rows are subject independent or not. and my dataset is small. not guilty ...
