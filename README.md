# Genome-Wide Association and Population-Tailored Polygenic Risk for Parkinson's Disease in Taiwan

`GP2 ❤️ Open Science 😍`

\[DOI: pending] under **CC-BY license**

**Last Updated:** January 2026

---

## **Summary**

This repository accompanies the manuscript **"Genome-Wide Association and Population-Tailored Polygenic Risk for Parkinson's Disease in Taiwan."** It contains analysis scripts and summary resources for the first and largest genome-wide investigation of Parkinson's disease in Taiwanese populations. 

Genotype imputation was performed using the **Taiwan Biobank Imputation Server**, leveraging a population-specific whole-genome reference panel to optimize variant coverage and accuracy.

---

## **Data Statement**

* All data used in this repository were generated using GP2-funded resources from the East Asian Parkinson's Disease Genomics Consortium (EAPDGC), as part of the Global Parkinson's Genetics Program (GP2).
* Access to the individual-level data used in this article is coordinated by the corresponding authors and governed by the GP2 Tier 2 data access policy.
* Data access may be granted upon reasonable request, subject to approval and a Data Use Agreement signed by the applicant's institution.

---

## **Helpful Links**

* [EAPDGC](https://eapdgc.org/)
* [GP2 website](https://gp2.org/)
  * [Introduction to GP2](https://gp2.org/about/)
  * [Other GP2 publications](https://gp2.org/publications/)
* [Taiwan Biobank Imputation Server](https://twbimputation.twbiobank.org.tw/)
  * [Taiwan Biobank: A rich biomedical research database of the Taiwanese population](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6288301/)

---

## **Citation**

If you use this repository or find it helpful for your research, please cite the corresponding manuscript:

> **Genome-Wide Association and Population-Tailored Polygenic Risk for Parkinson's Disease in Taiwan**
> *\[Authors, Global Parkinson's Genetics Program (GP2), 2025]* (DOI: pending)


---

## **Repository Orientation**

* `analyses/` – scripts used throughout the project

```
├── analyses
│   ├── 01_QC_PCA.R
│   ├── 02_GWAS.R
│   ├── 03_manhattan.R
│   ├── 04_regional_plot.R
│   ├── 05_SNCA_conditional.R
│   ├── 06_haplotype.R
│   ├── 07a_1000G_TW_projection.R
│   ├── 07b_1000G_TW_LRRK2_PCA.R
│   ├── 08_LRRK2.R
│   ├── 09_beta_comparison.R
│   └── 10_PRS.R
├── LICENSE
└── README.md
```

---

## **Analysis Scripts**

**Primary language:** R

| **Script**                      | **Description**                                                                                            |
| ------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `01_QC_PCA.R`                   | Genotyping QC and principal component analysis. Input genotypes are PLINK files converted from IDAT via Illumina GenomeStudio. |
| `02_GWAS.R`                     | Genome-wide association analysis using imputed data and PLINK 2.0.                                        |
| `03_manhattan.R`                | Generation of Manhattan plots for GWAS results.                                                           |
| `04_regional_plot.R`            | LocusZoom-style regional association plots for key loci.                                                  |
| `05_SNCA_conditional.R`         | Conditional association analyses at the SNCA locus and regional plots.                                    |
| `06_haplotype.R`                | Haplotype estimation and visualization for SNCA and LRRK2.                                                |
| `07a_1000G_TW_projection.R`     | PCA-based ancestry projection using 1000 Genomes and the Taiwan cohort.                                   |
| `07b_1000G_TW_LRRK2_PCA.R`      | East Asian + Taiwan PCA with LRRK2 variant carriers highlighted.                                          |
| `08_LRRK2.R`                    | Case–control and age-at-onset analyses stratified by LRRK2 Asian variants.                               |
| `09_beta_comparison.R`          | Effect size comparison with prior PD GWAS (e.g., Nalls 2019, Foo 2020) and beta–beta plots.              |
| `10_PRS.R`                      | Construction and evaluation of polygenic risk scores (AUC, ROC, deciles).                                 |

---

## **Software**

| **Software**      | **Version(s)** | **Resource URL**                                                                                                          | **RRID**          | **Notes**                                                                                                                      |
| ----------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| GenomeStudio      | 2.0            | [https://www.illumina.com/products/by-type/informatics-products/microarray-software/genomestudio.html](https://www.illumina.com/products/by-type/informatics-products/microarray-software/genomestudio.html) | RRID:SCR_010973   | Convert IDAT intensity files to PLINK-formatted genotype data                                                                 |
| PLINK             | 2.0            | [https://www.cog-genomics.org/plink/2.0/](https://www.cog-genomics.org/plink/2.0/)                                       | RRID:SCR_001757   | GWAS, scoring (PRS), and basic genotype processing                                                                            |
| PLINK             | 1.9            | [https://www.cog-genomics.org/plink/](https://www.cog-genomics.org/plink/)                                               | RRID:SCR_001757   | LD calculations, pruning, IBD, and legacy QC steps                                                                            |
| R                 | 4.3            | [https://www.r-project.org/](https://www.r-project.org/)                                                                 | RRID:SCR_001905   | Downstream analyses and visualization. Key packages: dplyr, tidyr, data.table, ggplot2, haplo.stats, geneHapR, pROC, patchwork |

---

> *For questions, please open an issue or contact the corresponding author.*
