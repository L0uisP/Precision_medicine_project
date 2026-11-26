
# Computational Precision Medicine — Group 3 project

Analysis of gene-expression biomarkers of immunotherapy response
using the IMvigor210 dataset (Mariathasan et al., Nature 2018).

Members of group 3:
- [Lun Suša](https://github.com/lundrought) (s253705) 
- [Rasmus Bertelsen](https://github.com/s235350) (s235350)
- [Henrique Gomes](https://github.com/quiquegomes123-cloud) (s253710)
- [Maxence Marbouty](https://github.com/MaxenceMarbouty) (s253730)
- [Louis Page](https://github.com/L0uisP) (s253729)


## Project structure

```
Precision_medicine_project/
├── README.md
├── data/                        # not tracked by git
├── notebooks/
│   ├── 00_data_prep.qmd         # to be run first to proccess data for analyses
│   ├── 01_RQ1_differential_expression.qmd
│   ├── 02_RQ2_immune_related_signatures.qmd
│   ├── 03_RQ3_biomarker_comparison.qmd
│   ├── 04_RQ4_tumor_purity.qmd
│   └── 05_RQ5_survival_analysis.qmd
└── results/
    ├── plots/         
    └── rendered/                # here are the html files rendered with all code + results
    
```

## Data

The dataset is not tracked by git. It contains pre-processed data from the
IMvigor210 clinical trial (atezolizumab in metastatic urothelial cancer).

The RDS file contains three objects:
- `counts` — raw RNAseq counts (31087 genes × 192 patients)
- `tpm` — normalized expression
- `clinical` — patient metadata (BOR, TMB, pat_id, sample_id)

Data for survival analysis is additionally sourced from the fuller [IMvigor210CoreBiologies package](https://github.com/BioInfoCloud/IMvigor210CoreBiologies).


## Research questions

| Notebook | RQ 
|----------|----
| 01 | Differential expression (DESeq2)
| 02 | T-cell inflamed GEP score 
| 03 | Biomarker comparison (PD-1, GEP, TMB) 
| 04 | Tumor purity and confounding
| 05 | Survival analysis

## Reference

Mariathasan et al. (2018). TGFβ attenuates tumour response to PD-L1 blockade
by contributing to exclusion of T cells. *Nature*, 554, 544–548.
https://doi.org/10.1038/nature25501

## Course

This project was carried out as part of the course **22123 Computational Precision Medicine** at DTU, autumn 2026.

Course responsible: Parvaneh Ebrahimi (pareb@dtu.dk)
