# Vehicle Classification – Machine Learning

## Project Overview

Machine learning project for classifying vehicles based on numerical geometric features extracted from vehicle silhouettes.

The dataset contains three vehicle classes:

- Bus
- Van
- Car

The project combines supervised and unsupervised learning to evaluate classification performance and explore the underlying structure of the dataset.

## Tech Stack

**Python | Pandas | NumPy | scikit-learn | Matplotlib | Seaborn | PCA | SVM | Random Forest | K-Means**

## Data Preparation & EDA

Exploratory data analysis was performed to examine class distribution, missing values, feature distributions, correlations, and class separability.

The preprocessing workflow included:

- Stratified train-test split
- Median imputation for missing values
- Feature standardization
- Pipeline-based preprocessing
- Weighted F1-score as the primary evaluation metric

## Supervised Learning

Three classification models were trained and compared:

| Model | Train F1 | Test F1 |
|---|---:|---:|
| Logistic Regression | 0.936 | 0.929 |
| Random Forest | 1.000 | 0.959 |
| SVM | 0.975 | 0.976 |

### Best Model – SVM

SVM achieved the strongest overall performance with a **weighted F1-score of approximately 0.976** on the test set.

The nearly identical training and test scores indicate strong generalization and model stability.

Confusion matrix analysis showed that most vehicles were classified correctly, with some remaining overlap between geometrically similar vehicle classes.

## Unsupervised Learning

Unsupervised learning was used to explore the natural structure of the vehicle data without using the target labels.

Methods included:

- PCA
- K-Means clustering
- Elbow Method
- Silhouette analysis
- Hierarchical clustering
- DBSCAN

The first two principal components explained approximately **68.9% of the total variance**.

K-Means revealed meaningful geometric structure in the data, although the resulting clusters only partially aligned with the true vehicle classes.

## Key Findings

- Vehicle silhouette features contain strong predictive information.
- SVM provided the strongest and most stable classification performance.
- Random Forest achieved high performance but showed slight overfitting.
- PCA revealed partially separable vehicle groups.
- Unsupervised clustering identified meaningful structure but was less effective than supervised learning for vehicle classification.

## Limitations

The dataset is relatively small and slightly imbalanced. Some features are strongly correlated, and the physical meaning of several geometric descriptors is limited.

The project uses pre-extracted numerical silhouette features rather than raw vehicle images.

## Repository Contents

- `vehicle_classification.ipynb` – complete ML analysis
- `vehicle.csv` – vehicle silhouette dataset
- `Projekt_Presentation_ML.pptx` – project presentation
- `README.md` – project overview
