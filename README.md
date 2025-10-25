# Big-five-personality-clusters-
Personality Trait Clustering & Country Analysis

This project explores global personality patterns using psychometric survey data from Kaggle: https://www.kaggle.com/datasets/tunguz/big-five-personality-test
It applies data preprocessing, feature engineering, PCA, and KMeans clustering to uncover patterns in the **Big Five personality traits** across countries.

# Objective

To analyze personality trends and identify clusters of similar individuals based on:
- Extraversion
- Agreeableness
- Conscientiousness
- Neuroticism
- Openness to Experience

# Methods & Workflow

### 1. Data Preprocessing
- Cleaned missing data and standardized column names  
- Dropped metadata columns and ensured numeric types  
- Reverse-scored negatively worded questionnaire items  

### 2. Feature Engineering
- Calculated mean scores per trait:

Scaled all traits using 'MinMaxScaler' (range 0–1)

### 3. Clustering & Dimensionality Reduction
- Applied **KMeans** clustering to group participants by personality profiles  
- Used **PCA (n_components=2)** to reduce trait dimensions and visualize clusters  
- Identified distinct personality groups across countries

### 4. Country-Level Aggregation
- Computed **mean trait scores and participant counts** per country  
- Filtered out small samples (Participants >= 30) for reliable comparisons  

## Key Results


<img width="847" height="853" alt="Untitled" src="https://github.com/user-attachments/assets/970d1ae0-6e9b-4806-99c6-eaa60ef364c3" />


| Trait | Highest Country | Score | Participants |
|--------|------------------|--------|--------------|
| Extraversion | ZM | 0.526 | 35 |
| Neuroticism | PA | 0.586 | 81 |
| Agreeableness | GU | 0.761 | 37 |
| Conscientiousness | AZ | 0.651 | 36 |
| Openness | ZW | 0.685 | 46 |

> **Note:** Scores are scaled (0–1); countries with fewer than 30 participants were excluded.


## Tools & Libraries

- **Python 3.12+**
- `pandas`, `numpy` — data handling  
- `scikit-learn` — scaling, PCA, KMeans  
- `seaborn`, `matplotlib` — visualization  
- `yellowbrick` — cluster optimization  

---

## Summary

- Engineered 5 personality trait features from 50+ item responses  
- Scaled data for cross-country comparability  
- Discovered personality clusters via KMeans  
- Used PCA for interpretable 2D visualizations  
- Derived country-level averages with participant context for reliability


