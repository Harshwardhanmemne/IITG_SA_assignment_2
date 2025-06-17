# 🌿 NDVI-based Land Cover Classification

A robust machine learning pipeline for classifying land cover types using noisy NDVI time-series data from satellites. Developed as part of the **Summer Analytics 2025** Hackathon organized by the Consulting & Analytics Club and GeeksforGeeks.

## 🛰️ Problem Statement

The task is to classify each location into one of six land cover types:

- Water
- Impervious
- Farm
- Forest
- Grass
- Orchard

The input is a time-series of **27 NDVI readings per location**, but the data is noisy and contains missing values due to cloud cover and other real-world factors.

## 🧠 Approach

The notebook includes a full pipeline with preprocessing, feature engineering, dimensionality reduction, and classification:

### ✅ Preprocessing & Feature Engineering
- **Temporal Features**: Computed rolling stats, deltas, and summaries across time points.
- **Missing Value Imputation**: Used `IterativeImputer` to fill gaps in the NDVI series.
- **Feature Scaling**: Standardized the data using `StandardScaler`.

### 📉 Dimensionality Reduction
- Applied **PCA** to reduce dimensionality while retaining 95% of the variance.
  
### ⚖️ Model Training
- Used **Logistic Regression** with class balancing (`class_weight='balanced'`) to address label imbalance.
- Evaluation using classification metrics such as **accuracy**, **precision**, **recall**, and **F1-score**.

## 📊 Results

- **Overall Accuracy**: 72%
- **Forest Class Performance**:
  - Precision: 97%
  - F1-Score: 83%

These results reflect strong generalization in the face of noisy, real-world data.

## 🛠️ Tech Stack

| Tool/Library     | Purpose                             |
|------------------|-------------------------------------|
| Python           | Core programming language           |
| scikit-learn     | ML pipeline, imputation, PCA, model |
| pandas & numpy   | Data wrangling and transformation   |
| matplotlib & seaborn | Visualizations (if needed)     |

## 📁 Files

- `IITG_SA_assignment_2.ipynb`: Full Jupyter notebook with data processing, modeling, and evaluation.
- `submission5.csv`: Final test set predictions for submission.


Participated in Summer Analytics 2025 Hackathon - A great learning experience in handling real-world noisy satellite data!
