# Hourly Bike Rentals Forecasting in Florida

## Submission Date
July 12, 2025

By Carllos Watts-Nogueira  

As the sole developer and analyst, I designed and implemented an end-to-end machine learning pipeline in the context of my academic journey at the University of San Diego’s AI and Machine Learning program, powered by Fullstack Academy (Anticipated Graduation Date: October 2025).

The project exemplifies the hands-on skill development central to the bootcamp, covering topics such as applied data science, machine learning, deep learning, NLP, and generative AI. I engineered features, cleaned and scaled data, built and tuned regression models, conducted exploratory testing with PCA and polynomial transformations, and evaluated performance using industry-standard metrics.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)
![Model](https://img.shields.io/badge/Best%20Model-Poly_Lasso%20(R²%3D0.739)-success.svg)
![Feature Engineering](https://img.shields.io/badge/Feature%20Engineering-Custom%20Interactions-orange.svg)
![PCA](https://img.shields.io/badge/PCA-Optional-lightgrey.svg)
![Pipeline](https://img.shields.io/badge/ML%20Pipeline-4%20Versions-yellow.svg)
![Platform](https://img.shields.io/badge/Platform-Jupyter%20Notebook-blueviolet.svg)
![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red.svg)

## Project Objective
Forecast hourly bike rental demand based on weather and time-based features, applying various regression techniques and modeling workflows.

## Technologies & Skills Used

- **pandas** – data wrangling, preprocessing
- **scikit-learn** – regression models (Linear, Ridge, Lasso, ElasticNet), pipeline building, scaling, encoding, PolynomialFeatures, PCA, GridSearchCV, cross-validation
- **joblib** – saving serialized models
- **matplotlib** – data visualization
- **Feature Engineering** – including:
  - Interactions like Temp × Humidity, Hour × Weekday, Wind × Visibility
  - Polynomial feature expansion (degree=2)
  - PCA dimensionality reduction
- **Experimental Design** – iterative testing of four pipelines, isolating the impact of PCA and engineered features
- **Performance Evaluation** – metrics: MAE, MSE, R²

## Pipeline Versions

| Version                          | PCA | Feature Interactions | Best Model   | R²     |
|----------------------------------|-----|-----------------------|--------------|--------|
| 01_base_model                    | ❌  | ❌                    | Lasso        | 0.481  |
| 02_scaler_then_pca               | ✅  | ❌                    | Poly_Lasso   | 0.617  |
| 03_pca_only                      | ✅  | ❌                    | Poly_Lasso   | 0.346  |
| **04_no_pca_with_interactions** | ❌  | ✅                    | **Poly_Lasso** | **0.739** ✅

## Highlight
The best-performing model was **Poly_Lasso (R² = 0.739)** using **hand-crafted feature interactions without PCA**, demonstrating the power of meaningful feature design over dimensionality reduction in this context.

## Business Impact
These forecasts can support:
- Resource planning during peak hours
- Weather-based fleet allocation
- Staffing, dynamic pricing, and maintenance scheduling
- Integration into real-time decision systems

## Next Steps
- Extend feature engineering (e.g., time-of-day bins, lag features)
- Try ensemble models (RandomForest, XGBoost)
- Create visual dashboards for ongoing monitoring

---

## Additional Testing – Final Model Evaluation (August 2025)

A new round of testing was conducted to validate model performance using updated metrics and a refined pipeline.

📁 Folder: [`update_model_test_lasso`](./update_model_test_lasso)

This folder contains:
- A new notebook with updated evaluation and cross-validation
- A saved production-ready model (`best_model_lasso.pkl`)
- A dedicated README summarizing the results and rationale

The best model from this round was **Lasso Regression**, selected for its balanced performance across MAE, MSE, and R², and its suitability for deployment.

### Key Improvements

- **Removed PCA from final pipeline**  
  This version uses only original features and engineered interactions.

- **Enhanced Feature Engineering**  
  - Added temporal features: `Weekday`, `IsWeekend`, `Month`, `Hour`  
  - Created meaningful interactions:  
    - `Temperature × Humidity`  
    - `Hour × Weekday`  
    - `Wind × Visibility`  
    - `Temperature × Month`  
  - Scaled all numerical features using `StandardScaler`

- **Polynomial Feature Expansion**  
  - Applied `PolynomialFeatures(degree=3)` to selected variables  
  - Captured complex nonlinear relationships without overfitting

- **Model Selection & Evaluation**  
  - Compared Linear, Ridge, Lasso, ElasticNet, and Polynomial Regression  
  - Used `GridSearchCV` for hyperparameter tuning  
  - Applied 5-fold cross-validation and test set evaluation  
  - Final model: **Lasso Regression** with R² = 0.556 and lowest MAE

### Business Impact

These forecasts support:
- Resource planning during peak hours  
- Weather-based fleet allocation  
- Staffing, dynamic pricing, and maintenance scheduling  
- Integration into real-time decision systems
