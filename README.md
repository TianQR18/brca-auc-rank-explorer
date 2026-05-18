# BRCA 100-Test Rank Explorer

This static website presents task-specific TCGA-BRCA gene-ranking stability after:

1. selecting one interpretable small-batch Top2000 panel per task from CV5 summaries;
2. rerunning XGBoost 100 times with new stratified splits and model seeds;
3. ranking genes within each test by XGBoost gain.

Rerank profile: Full-rank AUC, depth 4, colsample_bytree=0.3, colsample_bynode=0.4

Effective XGBoost parameters: binary: n_estimators=150, max_depth=4, learning_rate=0.03, subsample=0.8, colsample_bytree=0.3, colsample_bynode=0.4; multiclass: n_estimators=200, max_depth=4, learning_rate=0.03, subsample=0.8, colsample_bytree=0.3, colsample_bynode=0.4

Ranking mode: full_auc

Start locally:

```powershell
cd outputs/final_rank_web/web
python -m http.server 8000
```

Open `http://localhost:8000/index.html`.

If Python is unavailable, any static file server can serve this directory.
