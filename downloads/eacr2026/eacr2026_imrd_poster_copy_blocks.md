# EACR 2026 IMRD Poster Copy Blocks

## Title
Top genes are not a single answer

## Subtitle
Leakage-aware repeated random-subspace XGBoost improves top-gene stability in TCGA-BRCA transcriptomic models

## Authors and Affiliation
Qirui Tian, Johannes Benedikt, Rachel Hargest, Wen G. Jiang, Tracey A. Martin

CCMRC, Cardiff University, Cardiff, UK

## Introduction
High-dimensional transcriptomic models are often interpreted through a single ranked gene list. This is risky because feature selection outside resampling can leak held-out information, and leakage-free rankings can still change substantially across split seeds and folds.

## Objective
To test whether repeated, fold-contained local feature competition can make high-ranked genes more reproducible while preserving predictive performance.

## Methods
TCGA-BRCA expression matrix: 1218 samples and 20530 genes. Seven tasks were analysed: tumour-normal, PAM50 subtype, PAM50 without PAM50 genes, IHC subtype, ER status, HER2 status and TNBC status. Feature selection was nested inside five-fold cross-validation.

Genes were randomly assigned to batches of 100, 250, 500 or 1000 genes. Shallow XGBoost models ranked genes within training folds. Fold-specific Top2000 panels were then assessed for performance, Top100 Jaccard stability and prior-gene recovery.

## Results
Best small-batch or consensus rankings improved Top100 reproducibility across all seven tasks. Mean Top100 Jaccard increased from 0.24 for full-space rankings to 0.57 for the best small-batch or consensus rankings.

Internal CV5 performance was retained. The best small-batch Top2000 panel was within 0.005 primary-metric units of the full Top2000 comparator in six of seven tasks.

Small-batch screening recovered additional fold-stable BRCA/PAM50 prior genes. The largest mean gain was 19.8 prior-union genes for TNBC status at batch size 100.

## Validation
Top30 panels retained signal under XGBoost, logistic regression and elastic net. METABRIC transfer was evaluated only for label-compatible primary-tumour tasks and was used as context rather than as proof of external superiority.

## Discussion
Repeated fold-contained screening provides an audit layer for transcriptomic machine-learning studies. It helps distinguish predictive tasks that are accurate from gene rankings that are also reproducible.

## Limitations
This is a candidate-panel study, not biomarker validation. METABRIC validation is label-limited, tumour-normal transfer was not available in the downloaded METABRIC matrix, and recovered genes require biological follow-up.

## Take-Home Message
A high model score does not make one top-gene list definitive.

## Footer
Linkle: Qirui Tian

NovoRadiant | independent outreach
