# SISG26 — Meta-Analysis in Statistical Genetics

A hands-on course covering GWAS and ExWAS meta-analysis using **METAL** and **REMETA**, with practical exercises modelled on the [SISG 2025 QG3 format](https://joellembatchou.github.io/SISG2025_Association_Mapping/) by Joelle.

## 🌐 Course Website

**[moeenriaz2.github.io/SISG26](https://moeenriaz2.github.io/SISG26)**

## 📋 Sessions

| Session | Topic | Link |
|---------|-------|------|
| Practical 1 | GWAS meta-analysis with METAL — single-variant tests, IVW, heterogeneity | [practical_METAL.html](docs/practical_METAL.html) |
| Practical 2 | Gene-based ExWAS meta-analysis with REMETA — Burden, SKAT-O, ACAT-O | [practical_REMETA.html](docs/practical_REMETA.html) |

## 🛠️ Software Required

- [R ≥ 4.1](https://www.r-project.org/) + [RStudio](https://rstudio.com/products/rstudio/download/)
- [METAL](https://csg.sph.umich.edu/abecasis/metal/) — GWAS meta-analysis
- [REGENIE](https://github.com/rgcgithub/regenie/releases/) — whole-genome regression
- [REMETA](https://github.com/rgcgithub/remeta) — gene-based ExWAS meta-analysis
- [PLINK 2.0](https://www.cog-genomics.org/plink/2.0/)

R packages:
```r
install.packages(c("data.table", "ggplot2", "dplyr", "qqman", "SKAT"))
devtools::install_github("yaowuliu/ACAT")
```

## 📁 Repository Structure

```
SISG26/
├── docs/
│   ├── index.html              # Course home page (GitHub Pages)
│   ├── practical_METAL.html    # Practical 1: METAL
│   └── practical_REMETA.html   # Practical 2: REMETA
├── data/
│   ├── cohort1_UKB_BMI.txt     # Simulated BMI GWAS cohort 1 (N=14,823)
│   ├── cohort2_Rotterdam_BMI.txt  # Simulated BMI GWAS cohort 2 (N=8,421)
│   └── cohort3_HUNT_BMI.txt    # Simulated BMI GWAS cohort 3 (N=6,178)
└── README.md
```

> **Note:** All cohort data files are **simulated for teaching purposes**. Effect sizes and p-values are fabricated to illustrate real GWAS/meta-analysis behaviour. All published studies referenced in the practicals are explicitly cited.

## 🎯 Learning Objectives

After completing this course, students will be able to:

1. Explain why meta-analysis is necessary for complex trait GWAS (power, winner's curse, regulatory requirements)
2. Implement inverse-variance weighted fixed-effects meta-analysis from first principles in R
3. Run METAL and interpret its output columns (Effect, StdErr, HetISq, HetPVal)
4. Describe the REGENIE → REMETA pipeline for gene-based ExWAS meta-analysis
5. Interpret REMETA output including Burden/SKAT-O p-values, MAC filters, and mask composition
6. Apply appropriate significance thresholds (p < 5×10⁻⁸ for GWAS; p < 2.5×10⁻⁶ for ExWAS)

## 📚 Key References

- Willer CJ, Li Y, Abecasis GR. **METAL**: fast and efficient meta-analysis of genomewide association scans. *Bioinformatics*. 2010;26(17):2190-2191.
- Mbatchou J et al. **REGENIE**: computationally efficient whole-genome regression for quantitative and binary traits. *Nat Genet*. 2021;53:1151-1157.
- Mbatchou J et al. **REMETA**: computationally efficient meta-analysis of gene-based tests for ExWAS. *bioRxiv*. 2024.
- Lee S et al. Optimal tests for rare variant effects in sequencing association studies (**SKAT-O**). *Biostatistics*. 2012;13(4):762-775.
- Lin DY & Zeng D. Meta-analysis of genome-wide association studies: no efficiency gain in using individual participant data. *Biometrics*. 2010.
- Ioannidis JP. Why most discovered true associations are inflated (**winner's curse**). *Nat Genet*. 2008.

## 🔗 Related Resources

- [SISG 2025 QG3 — Association Mapping](https://joellembatchou.github.io/SISG2025_Association_Mapping/) (Mbatchou & Epstein)
- [REGENIE documentation](https://rgcgithub.github.io/regenie/)
- [REMETA GitHub](https://github.com/rgcgithub/remeta)

## ⚙️ Enable GitHub Pages

To host this as a website:
1. Go to your repository **Settings → Pages**
2. Set Source to **Deploy from a branch**
3. Select branch: `main`, folder: `/docs`
4. Your site will be live at `https://moeenriaz2.github.io/SISG26`
