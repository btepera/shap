# Tree explainer benchmark — CPU: EPYC 9555 | GPU: RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition, RTX PRO 6000 Blackwell Server Edition

## Metadata

- **CPU:** AMD EPYC 9555 64-Core Processor
- **GPU:** ['NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition', 'NVIDIA RTX PRO 6000 Blackwell Server Edition']
- **OS:** Linux-6.17.0-35-generic-x86_64-with-glibc2.39
- **Python:** 3.12.3
- **Explanation timeout (seconds):** 1200
- **Setup timeout (seconds):** 180
- **Timing scope:** Explainer construction and exp(X); excludes process startup and data creation
- **Skip rule:** More samples at the same feature count and model configuration, for the same explainer type, after an explanation timeout
- **Started (UTC):** 2026-10-12T20:09:41+00:00
- **Model:** RandomForestRegressor(max_depth=grid, n_estimators=grid, random_state=0); other parameters use sklearn defaults
- **Depth convention:** Root depth is 0; max_depth is a configured limit, actual depths are measured after fitting
- **Tree depth statistics:** Min, max and mean of each tree's maximum path depth across the forest
- **Training data:** One shared make_regression invocation: 20000 samples, 50 features, 10 informative features, 1 target, noise=0.0, random_state=0
- **Explanation data:** Standard normal, numpy default_rng seed=1
- **Feature perturbation:** tree_path_dependent
- **Validation:** First 100 samples; CPU/GPU assert_allclose with rtol=1e-4, atol=1e-4
- **Max depth limits:** [12, 20, 28, 36]
- **Tree counts:** [10, 50, 100]
- **Explanation sample counts:** [100, 1000, 10000]
- **Explanation feature count:** 50
- **shap version:** 0.52.1.dev72
- **numpy version:** 2.4.6
- **scikit-learn version:** 1.9.1

## Results

| run_id | explainer_type | n_samples | n_features | max_depth | n_trees | min–max tree depth | mean tree depth | mean leaves/tree | total_nodes | time (s) | status | validation | details |
| ---: | --- | ---: | ---: | ---: | ---: | --- | ---: | ---: | ---: | ---: | --- | --- | --- |
| 1 | TreeExplainer | 100 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 0.701464 | success | passed |  |
| 2 | GPUTreeExplainer | 100 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 0.501132 | success | passed |  |
| 3 | TreeExplainer | 1000 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 6.574844 | success | passed |  |
| 4 | GPUTreeExplainer | 1000 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 0.479369 | success | passed |  |
| 5 | TreeExplainer | 10000 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 69.319893 | success | passed |  |
| 6 | GPUTreeExplainer | 10000 | 50 | 12 | 10 | 12–12 | 12.00 | 3039.30 | 60776 | 0.770810 | success | passed |  |
| 7 | TreeExplainer | 100 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 3.475010 | success | passed |  |
| 8 | GPUTreeExplainer | 100 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 0.646939 | success | passed |  |
| 9 | TreeExplainer | 1000 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 34.592700 | success | passed |  |
| 10 | GPUTreeExplainer | 1000 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 0.732302 | success | passed |  |
| 11 | TreeExplainer | 10000 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 346.878606 | success | passed |  |
| 12 | GPUTreeExplainer | 10000 | 50 | 12 | 50 | 12–12 | 12.00 | 3041.98 | 304148 | 1.226966 | success | passed |  |
| 13 | TreeExplainer | 100 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 6.603629 | success | passed |  |
| 14 | GPUTreeExplainer | 100 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 0.840996 | success | passed |  |
| 15 | TreeExplainer | 1000 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 70.147042 | success | passed |  |
| 16 | GPUTreeExplainer | 1000 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 1.016380 | success | passed |  |
| 17 | TreeExplainer | 10000 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 657.568225 | success | passed |  |
| 18 | GPUTreeExplainer | 10000 | 50 | 12 | 100 | 12–12 | 12.00 | 3041.49 | 608198 | 1.796425 | success | passed |  |
| 19 | TreeExplainer | 100 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 4.280555 | success | passed |  |
| 20 | GPUTreeExplainer | 100 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 0.614862 | success | passed |  |
| 21 | TreeExplainer | 1000 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 43.825704 | success | passed |  |
| 22 | GPUTreeExplainer | 1000 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 0.700877 | success | passed |  |
| 23 | TreeExplainer | 10000 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 416.509239 | success | passed |  |
| 24 | GPUTreeExplainer | 10000 | 50 | 20 | 10 | 20–20 | 20.00 | 12365.40 | 247298 | 1.260922 | success | passed |  |
| 25 | TreeExplainer | 100 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | 22.030395 | success | passed |  |
| 26 | GPUTreeExplainer | 100 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | 1.389622 | success | passed |  |
| 27 | TreeExplainer | 1000 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | 213.005329 | success | passed |  |
| 28 | GPUTreeExplainer | 1000 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | 1.913718 | success | passed |  |
| 29 | TreeExplainer | 10000 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | — | timeout | — | explanation exceeded 1200 s |
| 30 | GPUTreeExplainer | 10000 | 50 | 20 | 50 | 20–20 | 20.00 | 12372.48 | 1237198 | 3.714616 | success | — |  |
| 31 | TreeExplainer | 100 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | 44.530308 | success | passed |  |
| 32 | GPUTreeExplainer | 100 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | 2.532069 | success | passed |  |
| 33 | TreeExplainer | 1000 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | 428.674437 | success | passed |  |
| 34 | GPUTreeExplainer | 1000 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | 2.993798 | success | passed |  |
| 35 | TreeExplainer | 10000 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | — | timeout | — | explanation exceeded 1200 s |
| 36 | GPUTreeExplainer | 10000 | 50 | 20 | 100 | 20–20 | 20.00 | 12369.47 | 2473794 | 6.722283 | success | — |  |
| 37 | TreeExplainer | 100 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 4.537587 | success | passed |  |
| 38 | GPUTreeExplainer | 100 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 0.664620 | success | passed |  |
| 39 | TreeExplainer | 1000 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 43.260527 | success | passed |  |
| 40 | GPUTreeExplainer | 1000 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 0.780870 | success | passed |  |
| 41 | TreeExplainer | 10000 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 433.935430 | success | passed |  |
| 42 | GPUTreeExplainer | 10000 | 50 | 28 | 10 | 25–28 | 26.60 | 12644.50 | 252880 | 1.301076 | success | passed |  |
| 43 | TreeExplainer | 100 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | 22.893804 | success | passed |  |
| 44 | GPUTreeExplainer | 100 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | 1.482352 | success | passed |  |
| 45 | TreeExplainer | 1000 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | 229.330258 | success | passed |  |
| 46 | GPUTreeExplainer | 1000 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | 1.890809 | success | passed |  |
| 47 | TreeExplainer | 10000 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | — | timeout | — | explanation exceeded 1200 s |
| 48 | GPUTreeExplainer | 10000 | 50 | 28 | 50 | 24–28 | 26.38 | 12641.58 | 1264108 | 4.126998 | success | — |  |
| 49 | TreeExplainer | 100 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | 44.854135 | success | passed |  |
| 50 | GPUTreeExplainer | 100 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | 2.547839 | success | passed |  |
| 51 | TreeExplainer | 1000 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | 448.625604 | success | passed |  |
| 52 | GPUTreeExplainer | 1000 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | 3.101551 | success | passed |  |
| 53 | TreeExplainer | 10000 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | — | timeout | — | explanation exceeded 1200 s |
| 54 | GPUTreeExplainer | 10000 | 50 | 28 | 100 | 24–28 | 26.25 | 12642.14 | 2528328 | 6.866825 | success | — |  |
| 55 | TreeExplainer | 100 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 4.334035 | success | passed |  |
| 56 | GPUTreeExplainer | 100 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 0.667439 | success | passed |  |
| 57 | TreeExplainer | 1000 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 44.671591 | success | passed |  |
| 58 | GPUTreeExplainer | 1000 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 0.784717 | success | passed |  |
| 59 | TreeExplainer | 10000 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 433.337733 | success | passed |  |
| 60 | GPUTreeExplainer | 10000 | 50 | 36 | 10 | 25–29 | 26.70 | 12644.60 | 252882 | 1.298509 | success | passed |  |
| 61 | TreeExplainer | 100 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | 22.366885 | success | passed |  |
| 62 | GPUTreeExplainer | 100 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | 1.463323 | success | passed |  |
| 63 | TreeExplainer | 1000 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | 221.049084 | success | passed |  |
| 64 | GPUTreeExplainer | 1000 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | 1.842826 | success | passed |  |
| 65 | TreeExplainer | 10000 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | — | timeout | — | explanation exceeded 1200 s |
| 66 | GPUTreeExplainer | 10000 | 50 | 36 | 50 | 24–32 | 26.52 | 12641.88 | 1264138 | 3.709260 | success | — |  |
| 67 | TreeExplainer | 100 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | 46.613341 | success | passed |  |
| 68 | GPUTreeExplainer | 100 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | 2.500802 | success | passed |  |
| 69 | TreeExplainer | 1000 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | 463.129758 | success | passed |  |
| 70 | GPUTreeExplainer | 1000 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | 3.028017 | success | passed |  |
| 71 | TreeExplainer | 10000 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | — | timeout | — | explanation exceeded 1200 s |
| 72 | GPUTreeExplainer | 10000 | 50 | 36 | 100 | 24–33 | 26.40 | 12642.45 | 2528390 | 6.792859 | success | — |  |
