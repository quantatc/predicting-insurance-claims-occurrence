# Predicting Insurance Claim Occurrence

## Brief Description

This project builds a comprehensive machine learning classification model to predict whether a policyholder will file an insurance claim. We implement multiple algorithms with hyperparameter tuning and detailed evaluation to identify the best-performing model.

**Target Variable**: `claim_status` (Binary: 0 = No claim, 1 = Claim filed)

**Key Features**: Age, vehicle characteristics, previous claim history, premium amount, policy type, deductible, and policy duration.

## Data Source

https://www.kaggle.com/datasets/litvinenko630/insurance-claims

## Project Structure

```
README.md
Predicting_Insurance_Claim_Occurrence_prd.md
data/
  input/
    Insurance_claims_data.csv
  output/
models/
notebooks/
  01.insurance-claim-occurrence-ML_pipeline.ipynb
```

## Notebooks Overview

### 01.insurance-claim-occurrence-ML_pipeline.ipynb

Complete ML pipeline with:

**Data Preparation & EDA**:
- Data loading and quality assessment
- Exploratory data analysis with visualizations
- Missing value handling and data cleaning

**Feature Engineering & Selection**:
- Feature creation and transformation
- Correlation analysis
- Feature selection based on statistical significance

**Machine Learning Models**:
1. **Baseline** - Naive classifier (majority class predictor)
2. **Logistic Regression** - Linear classification model
3. **K-Nearest Neighbors (KNN)** - Distance-based classifier with hyperparameter tuning
4. **Decision Tree Classifier** - Decision Tree classifier with hyperparameter tuning to find optimal tree depth and split criteria
5. **Random Forest Classifier** - Random Forest model which combines multiple decision trees for improved performance and robustness

**Model Evaluation**:
- Confusion matrices and classification reports
- ROC curves and AUC scores
- Comprehensive comparison across all metrics
- Best model selection and persistence

**Metrics Tracked**:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## How to Run

### Setup Environment

1. Sync the environment with UV:
   ```
   uv sync
   ```
   This will:
   - Read the UV configuration from `pyproject.toml`
   - Install all dependencies (pandas, scikit-learn, matplotlib, seaborn, joblib, jupyter)
   - Create a Python virtual environment

### Start Jupyter

2. Start Jupyter Lab:
   ```
   uv run jupyter lab
   ```

3. Open the notebook:
   - Navigate to: `notebooks/01.insurance-claim-occurrence-ML_pipeline.ipynb`

### Run the Notebook

4. Execute all cells (Shift+Enter or Run menu)

## Key Features

- **Comprehensive ML Pipeline**: From data loading through model deployment  
- **Multiple Algorithms**: Baseline, Logistic Regression, KNN, SVM, Gradient Boosting   
- **Professional Visualization**: ROC curves, confusion matrices, performance comparisons  
- **Model Persistence**: Saves best model, scaler, and feature names for production use  
- **Detailed Evaluation**: Multiple metrics and comprehensive model comparison  

## Output Files

After running the notebook, the generated files are saved as `.sav` in `data/output/`
