# EACR 2026 IMRD Medical Poster Text Placement Guide

Poster size: A0 landscape, 46.8 x 33.1 in.  
Recommended font: Aptos or Arial.  
Colour rule: navy/blue = method and evidence; grey = cautious explanation; red = claim boundary or take-home.

This guide matches `eacr2026_imrd_medical_poster_with_figures.pptx`.

## Header

### Title

Position: top-left header, x 0.9 in, y 0.35 in, width 29.2 in.  
Font: 42 pt, bold, white.

Text:

```text
Top genes are not a single answer
```

### Subtitle

Position: under title, x 0.95 in, y 1.55 in, width 30.5 in.  
Font: 18 pt, bold, pale blue/white.

Text:

```text
Leakage-aware repeated random-subspace XGBoost improves top-gene stability in TCGA-BRCA transcriptomic models
```

### Authors

Position: top-right header, x 31.8 in, y 0.65 in, width 14.2 in.  
Font: 12 pt, bold, white, right aligned.

Text:

```text
Qirui Tian, Johannes Benedikt, Rachel Hargest, Wen G. Jiang, Tracey A. Martin
```

### Affiliation

Position: under authors, x 31.8 in, y 1.35 in, width 14.2 in.  
Font: 11 pt, pale blue/white, right aligned.

Text:

```text
CCMRC, Cardiff University, Cardiff, UK
```

### Meeting / Linkle

Position: top-right header, x 31.8 in, y 2.05 in, width 14.2 in.  
Font: 11 pt, bold, pale blue/white, right aligned.

Text:

```text
EACR 2026 | Linkle: Qirui Tian
```

## Introduction

Position: left column, first box, x 0.75 in, y 3.75 in, width 10.4 in, height 5.9 in.  
Section header: 12 pt, bold, white on blue bar.  
Body: 13 pt, grey. Keep to 2 short paragraphs.

Text:

```text
High-dimensional transcriptomic models are often interpreted through a single ranked gene list.

This is risky for two reasons: feature selection outside resampling can leak held-out information, and leakage-free rankings can still change across split seeds and folds.
```

## Objective

Position: left column, second box, x 0.75 in, y 9.9 in, width 10.4 in, height 3.0 in.  
Section header: 12 pt, bold, white on navy bar.  
Body: 15 pt, bold, black. This should be visually stronger than Introduction.

Text:

```text
Test whether repeated, fold-contained local feature competition can make high-ranked genes more reproducible while preserving predictive performance.
```

## Methods

Position: left column, large lower box, x 0.75 in, y 13.25 in, width 10.4 in, height 16.85 in.  
Section header: 12 pt, bold, white on blue bar.  
Body: 12 pt, grey.  
Figure: insert `fig1a_workflow.png` at x 1.1 in, y 16.35 in, width 9.7 in, height about 3.15 in.

Opening text:

```text
TCGA-BRCA expression matrix: 1218 samples and 20530 genes.

Seven tasks: tumour-normal, PAM50 subtype, PAM50 without PAM50 genes, IHC subtype, ER, HER2 and TNBC status.

Feature selection was nested inside five-fold cross-validation.
```

Design controls text:

```text
Design controls
1. Ranking occurs inside each training fold.
2. Random batches create repeated local feature competition.
3. Top100 Jaccard audits high-rank stability.
4. BRCA/PAM50 genes are interpretation controls only.
5. Logistic, elastic-net and METABRIC analyses constrain the claim.
```

Claim boundary note:

Position: bottom of Methods box.  
Font: 13 pt, bold, red.

Text:

```text
Claim boundary: candidate-panel prioritisation, not biomarker validation.
```

## Results

Position: central large box, x 11.7 in, y 3.75 in, width 23.15 in, height 26.35 in.  
Section header: 12 pt, bold, white on blue bar.

### Results Lead Sentence

Position: x 12.05 in, y 4.42 in, width 22.45 in.  
Font: 18 pt, bold, black.

Text:

```text
Small-batch screening improved high-rank reproducibility while retaining internal CV5 performance.
```

### Main Figure

Insert: `figure2_interpretability_context.png`.  
Position: x 12.05 in, y 5.35 in, width 22.45 in, height about 11.85 in.

### Main Figure Caption

Position: x 12.05 in, y 17.45 in, width 22.45 in.  
Font: 12 pt, grey.

Text:

```text
Figure 2. Full-space Top100 rankings were less stable than best small-batch or consensus rankings. Performance deltas remained close to zero, and prior-union recovery improved in receptor-status and subtype tasks.
```

### Metric Cards

Position: four cards across central Results box, y about 19.25 in.  
Number font: 28 pt, bold. Labels: 10 pt, grey.

Card 1:

```text
0.57
mean best Top100 Jaccard
```

Card 2:

```text
0.24
mean full-space Top100 Jaccard
```

Card 3:

```text
6 / 7
tasks within 0.005 of full Top2000
```

Card 4:

```text
19.8
largest mean prior-gene recovery gain
```

### Primary Finding

Position: x 12.05 in, y 23.0 in, width 22.45 in.  
Font: 13 pt, grey. Keep this as one paragraph or three very short bullets.

Text:

```text
Primary finding
Best small-batch or consensus rankings increased Top100 fold-stability across all seven tasks while retaining internal CV5 performance. Prior-gene recovery supported interpretability, but recovered genes remain candidates for follow-up rather than validated biomarkers.
```

## Validation

Position: right column, top box, x 35.35 in, y 3.75 in, width 10.7 in, height 10.9 in.  
Section header: 12 pt, bold, white on blue bar.  
Figure: insert `figure3_validation_and_baselines.png` at x 35.7 in, y 4.45 in, width 10.0 in, height about 5.15 in.  
Body: 12 pt, grey.

Text:

```text
Top30 panels retained task signal under XGBoost, logistic regression and elastic net. METABRIC transfer was evaluated only for label-compatible primary-tumour tasks.
```

## Exploratory Prognosis

Position: right column, middle box, x 35.35 in, y 15.15 in, width 10.7 in, height 5.55 in.  
Section header: 12 pt, bold, white on navy bar.  
Figure: insert `prognosis_latest_internal_regression_elasticnet_cindex.png` at x 35.75 in, y 15.85 in, width 9.9 in, height about 3.0 in.  
Body: 10 pt, grey.

Text:

```text
Retained as exploratory evidence because endpoint mapping and cross-cohort calibration add uncertainty.
```

## Discussion

Position: right column, lower box, x 35.35 in, y 21.2 in, width 10.7 in, height 8.9 in.  
Section header: 12 pt, bold, white on blue bar.  
Body: 12 pt, grey.

Text:

```text
Interpretation
Repeated fold-contained screening provides an audit layer for transcriptomic machine-learning studies. It helps distinguish predictive tasks that are accurate from gene rankings that are also reproducible.

Limitations
- Candidate-panel study, not biomarker validation.
- METABRIC validation is label-limited.
- Recovered genes require biological follow-up.
```

### Take-Home Message

Position: lower part of Discussion box.  
Font: 15 pt, bold, red.

Text:

```text
Take-home: a high model score does not make one top-gene list definitive.
```

## Footer

Position: full-width footer, x 0.65 in, y 30.65 in, width 45.5 in, height 1.5 in.  
Font: 10 pt.

Left:

```text
Study affiliation: CCMRC, Cardiff University
```

Middle-left:

```text
Linkle: Qirui Tian
```

Middle:

```text
Poster materials: insert final QR or URL
```

Right:

```text
NovoRadiant | independent outreach
```

Important: keep `NovoRadiant` in the footer only. Do not place it in the affiliation line or figure legends.
