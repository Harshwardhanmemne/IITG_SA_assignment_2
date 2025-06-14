# NDVI-based Land Cover Classification 

A machine learning solution for classifying land cover types using satellite NDVI time-series data, developed for the Summer Analytics 2025 hackathon hosted by Consulting & Analytics Club and GeeksforGeeks.

## Problem Overview

This project tackles the challenge of identifying different land cover types (Water, Impervious, Farm, Forest, Grass, Orchard) from noisy satellite imagery data. The main hurdle? Real-world NDVI (Normalized Difference Vegetation Index) data is messy - cloudy skies block satellite views, and crowdsourced labels aren't always perfect.

## My Approach

I built a robust preprocessing pipeline that handles the data's inherent messiness:

- **Temporal Feature Engineering**: Created meaningful features from 27 NDVI time points, including differences between consecutive measurements and statistical summaries
- **Smart Imputation**: Used IterativeImputer to fill missing values caused by cloud cover
- **Dimensionality Reduction**: Applied PCA to retain 95% of variance while reducing noise
- **Balanced Classification**: Implemented Logistic Regression with class balancing to handle uneven data distribution

## Key Results

The model achieved **72% accuracy** on the test set, with particularly strong performance on forest classification (97% precision, 83% F1-score). The approach successfully handled the noisy training data while maintaining good generalization.

## Tech Stack

- **Python**: Core language
- **scikit-learn**: Machine learning pipeline
- **pandas & numpy**: Data manipulation
- **Logistic Regression**: Classification model (as per hackathon requirements)

## Files

- `IITG_SA_assignment_2.ipynb`: Complete solution with preprocessing, training, and prediction pipeline
- `submission5.csv`: Final predictions for the test dataset

---

*Participated in Summer Analytics 2025 Hackathon - A great learning experience in handling real-world noisy satellite data!*
