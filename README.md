# Bioscience PhD Computing Portfolio

Data analysis and computing portfolio prepared for PhD applications in biochemistry, molecular biology and cell biology.

## Projects

### 1. RNA-seq differential expression analysis — hypoxia and mTOR inhibition
Multi-factor RNA-seq analysis of hypoxia and mTOR inhibitor (PP242) treatment in a non-malignant (MCF10A) and a triple-negative breast cancer (MDA-MB-231) cell line, using DESeq2, pathway enrichment (GSEA) and reproducible R Markdown.

**[View the full report](https://fmontgomerie.github.io/rnaseq_hypoxia_mtor_portfolio/rnaseq_hypoxia_mtor_analysis/rnaseq_hypoxia_report.html)**
[Source code](rnaseq_hypoxia_mtor_analysis/rnaseq_hypoxia_report.Rmd)

### 2. Microscopy image analysis — nuclear translocation assay
Quantification of FKHR-EGFP nuclear translocation in response to two PI3K inhibitors (Wortmannin, LY294002), using classical image segmentation (Otsu thresholding, watershed), dose-response curve fitting, and assay quality metrics (Z'-factor, V-factor), benchmarked against the published BBBC013 dataset.

**[View the full notebook](https://github.com/FMontgomerie/rnaseq_hypoxia_mtor_portfolio/blob/main/microscopy_nuclear_translocation/nuclear_translocation_analysis.ipynb)**
[Source code](microscopy_nuclear_translocation/nuclear_translocation_analysis.ipynb)

### 3. Single-cell RNA-seq clustering and cell-type analysis
*In progress.*

## Repository structure

```
.
├── README.md
├── rnaseq_hypoxia_mtor_analysis/            Project 1: RNA-seq (R)
│   ├── rnaseq_hypoxia_report.Rmd            source
│   ├── rnaseq_hypoxia_report.html           knitted report
│   ├── data/                                raw data
│   └── renv.lock                            R package versions
└── microscopy_nuclear_translocation/        Project 2: image analysis (Python)
    ├── nuclear_translocation_analysis.ipynb  notebook (source + report in one)
    ├── data/                                 raw images
    └── results/                              output figures/tables
```
