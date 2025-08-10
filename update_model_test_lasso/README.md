#  Final Model Evaluation – August 2025

## Overview

This folder contains the final evaluation of regression models for hourly bike rental forecasting in Florida. The goal was to validate previous findings and identify the most production-ready model.

## Best Model

- **Model**: Lasso Regression
- **Filename**: `best_model_lasso.pkl`
- **Rationale**:
  - Lowest MSE and competitive MAE
  - Stable R² across cross-validation
  - Regularization improves generalization and interpretability

##  Performance Summary

| Model               | MAE       | MSE         | R²     |
|--------------------|-----------|-------------|--------|
| Linear              | 323.390   | 185159.083  | 0.556  |
| Ridge               | 323.235   | 185107.190  | 0.556  |
| **Lasso**           | **323.085** | **185053.764** | **0.556** |
| ElasticNet          | 328.642   | 199354.289  | 0.522  |
| Polynomial (d=3)    | 310.369   | 195423.132  | 0.531  |

##  Files Included

- `best_model_lasso.pkl` – serialized model
- `unit3capstone_updates.ipynb` `unit3capstone_updates.py` – notebook with full pipeline and evaluation
- `README.md` – this file

##  Next Steps

- Integrate model into a production pipeline
- Add feature importance analysis
- Explore ensemble models for further improvement