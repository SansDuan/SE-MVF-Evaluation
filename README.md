# SE-MVF: Evaluation Results

**Anonymized evaluation results for cross-view UAV localization**

This repository accompanies the paper **“SE-MVF: A Self-Supervised End-to-End Monocular Visual Frontend for Generalizable Cross-View UAV Localization.”** It provides per-query localization results for **1,311 queries** across two evaluation settings, with five matching methods evaluated on each query.

## Datasets

| Evaluation set | Queries | Evaluation setting |
| --- | ---: | --- |
| UAV-AVL | 487 | Automatic map retrieval and localization |
| East_LargeAngle | 824 | Large-angle matching and registration evaluation using 35 candidate map tiles per query |

## SE-MVF Results

| Evaluation set | Median (m) ↓ | RMSE (m) ↓ | P95 (m) ↓ | SR@5 m (%) ↑ |
| --- | ---: | ---: | ---: | ---: |
| UAV-AVL | 2.47 | 87.78 | 148.94 | 75.77 |
| East_LargeAngle | 2.029 | 33.922 | 47.057 | 72.937 |

Results for **SIFT, SuperGlue, LoFTR, RoMa, and SE-MVF** are provided in the CSV files.

## Files

| File | Description |
| --- | --- |
| [`UAV-AVL_487.csv`](UAV-AVL_487.csv) | Per-query results on UAV-AVL |
| [`East_LargeAngle_824.csv`](East_LargeAngle_824.csv) | Per-query results on the large-angle evaluation set |
| [`metrics_summary.csv`](metrics_summary.csv) | Summary statistics reported in the paper |

Per-query CSV columns are `sample_id`, `method`, `error_m`, `pose_valid`, `inlier_count`, and `runtime_s`. Sample identifiers are anonymized.

**Reporting note:** The summary retains the paper's original reporting convention: `pnp_pct` counts finite `error_m` entries, and `median_m` uses those entries, including any `10000` failure placeholders. Thus, `pnp_pct` is not necessarily identical to the `pose_valid` rate. All values are provided as originally reported.

Only evaluation results are released; source images, geographic coordinates, original identifiers, training data, and model code are not included.

## Citation

If you use these results, please cite the accompanying **SE-MVF** paper. Bibliographic details will be added upon publication.