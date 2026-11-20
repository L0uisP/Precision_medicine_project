
# Computational Precision Medicine — Group Project

Analysis of gene-expression biomarkers of immunotherapy response
using the IMvigor210 dataset (Mariathasan et al., Nature 2018).

## Project structure

```
cpm-immunotherapy-project/
├── README.md
├── data/                        # not tracked by git
├── notebooks/
│   ├── 00_data_prep.qmd         # to be run first to proccess data for analyses
│   ├── 01_RQ1_differential_expression.qmd
│   ├── 02_RQ2_immune_related_signatures.qmd
│   ├── 03_RQ3_biomarker_comparison.qmd
│   ├── 04_RQ4_tumor_purity.qmd
│   └── 05_RQ5_survivor_analysis.qmd
├── scripts/
│   └── utils.R                  # helper functions (if neded?)
└── results/
    
```

## Data

The dataset is not tracked by git. It contains pre-processed data from the
IMvigor210 clinical trial (atezolizumab in metastatic urothelial cancer).

The RDS file contains three objects:
- `counts` — raw RNAseq counts (31087 genes × 192 patients)
- `tpm` — normalized expression
- `clinical` — patient metadata (BOR, TMB, pat_id, sample_id)

## Research questions

| Notebook | RQ 
|----------|----
| 01 | Differential expression (DESeq2)
| 02 | T-cell inflamed GEP score 
| 03 | Biomarker comparison (PD-1, GEP, TMB) 
| 04 | Tumor purity and confounding
| 05 | Survivor analysis

## Reference

Mariathasan et al. (2018). TGFβ attenuates tumour response to PD-L1 blockade
by contributing to exclusion of T cells. *Nature*, 554, 544–548.
https://doi.org/10.1038/nature25501