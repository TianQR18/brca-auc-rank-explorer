# EACR 2026 Poster Copy Blocks

These blocks are written to be pasted directly into PowerPoint text boxes. The company note is intentionally separated from the research affiliation.

## Header

**Title**

Top genes are not a single answer

**Subtitle**

Leakage-aware repeated random-subspace XGBoost improves top-gene stability in TCGA-BRCA transcriptomic models

**Authors**

Qirui Tian, Johannes Benedikt, Rachel Hargest, Wen G. Jiang, Tracey A. Martin

**Affiliation**

CCMRC, Cardiff University, Cardiff, UK

## Background / Gap

Transcriptomic biomarker models are often interpreted through a single ranked gene list.

Two problems make this risky:

- feature selection outside resampling can leak held-out information;
- leakage-free top-gene lists can still change substantially across split seeds and folds.

## Objective

To test whether repeated, fold-contained local feature competition can make high-ranked genes more reproducible while preserving predictive performance.

## Methods Workflow Labels

1. TCGA-BRCA expression matrix  
2. Five-fold split, feature selection inside each training fold  
3. Random gene batches: 100, 250, 500 or 1000 genes  
4. Shallow XGBoost ranking over repeated local competitions  
5. Fold-specific Top2000 panel construction  
6. Internal CV5, stability audit, baseline and METABRIC context

## At A Glance

0.57  
Mean best small-batch or consensus Top100 Jaccard

0.24  
Mean full-space Top100 Jaccard

6 / 7  
Tasks within 0.005 primary-metric units of full Top2000

Top30  
Selected panels supplied for downstream inspection

## Result 1: Stability

Small-batch or consensus ranking improved Top100 reproducibility across all seven TCGA-BRCA tasks.

Mean Top100 Jaccard increased from 0.24 for full-space rankings to 0.57 for the best small-batch or consensus rankings.

## Result 2: Performance

Stability did not require a meaningful loss of internal performance.

The best small-batch Top2000 panel was within 0.005 primary-metric units of the full Top2000 comparator in six of seven tasks.

## Result 3: Prior-Gene Recovery

Small-batch screening recovered additional fold-stable BRCA/PAM50 prior genes in receptor-status and subtype-related tasks.

The largest mean recovery gain was 19.8 prior-union genes for TNBC status at batch size 100.

## Baselines and External Validation

Top30 panels retained task signal under XGBoost, logistic regression and elastic net.

METABRIC transfer was evaluated only for label-compatible primary-tumour tasks. Full and consensus primary metrics ranged from 0.756 to 0.993.

## Exploratory Prognosis

Prognosis analyses were retained as exploratory evidence only.

Endpoint mapping and cross-cohort calibration introduce additional uncertainty, so these results are best used for discussion rather than as the main poster claim.

## Take-Home Message

A high model score does not make one top-gene list definitive.

Fold-contained repeated screening makes ranking instability visible and produces more reproducible candidate panels for biological follow-up.

## Limitations

- Candidate-panel study, not biomarker validation.
- METABRIC validation is label-limited.
- Tumour-normal transfer was not available in the downloaded METABRIC matrix.
- Recovered genes require biological follow-up before mechanistic or clinical claims.

## Footer / Contact

Linkle: Qirui Tian

Poster materials: insert QR code or URL

NovoRadiant | independent outreach

