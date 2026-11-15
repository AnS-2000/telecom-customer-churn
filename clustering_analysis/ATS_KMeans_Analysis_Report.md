# K-Means Customer Segmentation

- Input file: Dataset_ATS_without_duplicates(1).csv
- Rows analysed: 6,741
- Features used: 12; Churn was excluded from fitting.
- Scaling: StandardScaler inside the saved model pipeline.
- Candidate cluster counts: 2 to 8.
- Selected k: 6 (highest sampled silhouette score: 0.2298).
- The PCA figure is a visual projection; the model used all selected features.

## Cluster summary

| ID | Description | Customers | Share | Avg. tenure | Avg. monthly charges | Churn rate |
|---:|---|---:|---:|---:|---:|---:|
| 0 | No phone service / mixed contracts | 673 | 10.0% | 31.9 | 42.1 | 24.7% |
| 1 | Month-to-month / DSL | 1,483 | 22.0% | 32.7 | 69.8 | 28.8% |
| 2 | Month-to-month / Fiber optic | 1,817 | 27.0% | 33.6 | 68.3 | 26.7% |
| 3 | Two-year / DSL | 1,485 | 22.0% | 32.9 | 68.7 | 25.6% |
| 4 | One-year / Fiber optic | 477 | 7.1% | 34.3 | 67.5 | 25.2% |
| 5 | One-year / DSL | 806 | 12.0% | 32.0 | 66.4 | 26.3% |

## Observations
- Highest observed churn rate: Month-to-month / DSL (28.8%).
- Lowest observed churn rate: No phone service / mixed contracts (24.7%).
- Overall churn rate in the dataset: 26.6%.
- These rates describe groups after clustering; they do not show that a feature caused churn.

## Limitations
K-Means uses Euclidean distance and works best for compact groups. The silhouette score is modest and was measured on a sample. The result depends on the selected features and the tested k range. Cluster descriptions summarise dominant profiles; they are not fixed customer categories.
