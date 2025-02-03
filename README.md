# README - Adult Census Income Dataset Processing

## Overview
This project focuses on cleaning, preparing, and analyzing the Adult Census Income dataset. The dataset is preprocessed to ensure quality and readiness for machine learning or statistical analysis. The key steps include data cleaning, feature engineering, exploratory data analysis (EDA), and final dataset preparation.

## Steps Involved

### 1. Data Cleaning
- Replaced missing values in `occupation` and `native.country` with their respective mode values.
- Replaced `?` values with `NaN` and handled them appropriately.
- Removed duplicate rows to maintain dataset integrity.

### 2. Feature Engineering
- Grouped education levels into broader categories:
  - "dropout"
  - "HighGrad"
  - "CommunityCollege"
  - "Bachelors"
  - "Masters"
  - "Doctorate"
- Simplified marital status into fewer meaningful categories.
- Converted categorical variables into numerical form using one-hot encoding (`pd.get_dummies()`).

### 3. Exploratory Data Analysis (EDA)
- Visualized income distribution across various features using `sns.countplot()`.
- Generated a correlation heatmap using `sns.heatmap(df.corr(), annot=True)`.
- Analyzed distributions of age and education.
- Evaluated mean income for different groups (e.g., workclass, sex, education levels).

### 4. Final Dataset Preparation
- Dropped irrelevant or redundant columns:
  - `fnlwgt`
  - `capital.gain`
  - `capital.loss`
  - `education.num`
- Merged the transformed categorical data with the numerical dataset to form the final version.

## Next Steps
- Perform feature selection to determine the most significant predictors for income classification.
- Train machine learning models to predict income levels.
- Optimize and tune models for better performance.
- Further explore additional feature transformations if necessary.

## Requirements
To execute the preprocessing steps, ensure the following Python libraries are installed:

```bash
pip install pandas numpy seaborn matplotlib
```

## Usage
Run the preprocessing script to clean and prepare the dataset:
```python
python preprocess.py
```

This will generate a cleaned and transformed dataset ready for further analysis or model training.

---
This README provides an overview of the dataset preparation workflow, ensuring a structured approach to handling the Adult Census dataset.

