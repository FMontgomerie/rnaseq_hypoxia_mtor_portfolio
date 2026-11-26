# RNA-seq differential expression analysis — hypoxia and mTOR inhibition

Part of a bioscience PhD computing portfolio (biochemistry, molecular biology, cell biology).

Multi-factor RNA-seq analysis of hypoxia and mTOR inhibitor (PP242) treatment in a non-malignant (MCF10A) and a triple-negative breast cancer (MDA-MB-231) cell line, using DESeq2, pathway enrichment (GSEA) and reproducible R Markdown.

**[View the full report](https://fmontgomerie.github.io/rnaseq_hypoxia_mtor_portfolio/rnaseq_hypoxia_report.html)**
[Source code](rnaseq_hypoxia_report.Rmd)

## Approach

1. Retrieve raw counts and sample metadata for GSE104193 from GEO, checked against the published experimental design.
2. Build sample metadata and a multi-factor DESeq2 model (`~ cell_line + oxygen + drug + fraction + cell_line:oxygen + oxygen:fraction`), capturing cell line, oxygen, drug and polysome/sub-polysome fraction effects.
3. QC the model (library sizes, PCA, dispersion estimates) before drawing any conclusions from it.
4. Extract and visualise results for each contrast of interest, with shrinkage (apeglm) applied to fold changes.
5. Run gene set enrichment analysis (GSEA) against MSigDB Hallmark gene sets to interpret the differential expression results at a pathway level.
6. Manage the full R environment with `renv` so the analysis is reproducible from a fresh clone.

## Repository structure

```
.
├── README.md
├── rnaseq_hypoxia_report.Rmd            source
├── rnaseq_hypoxia_report.html           knitted report
├── data/                                raw data (GEO counts and metadata)
└── renv.lock                            R package versions
```

## Related projects

This is one part of a broader bioscience PhD computing portfolio. The other projects are in their own repositories:

- [Microscopy image analysis — nuclear translocation assay](https://github.com/FMontgomerie/Nuclear_translocation_image_analysis)
