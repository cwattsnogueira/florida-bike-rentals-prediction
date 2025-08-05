# Hourly Bike Rentals Forecasting in Florida

## Submission Date
July 12, 2025

## My Role  
By Carllos Watts-Nogueira  

As the sole developer and analyst, I designed and implemented an end-to-end machine learning pipeline in the context of my academic journey at the University of San Diego’s AI and Machine Learning program, powered by Fullstack Academy (Anticipated Graduation Date: October 2025).

The project exemplifies the hands-on skill development central to the bootcamp, covering topics such as applied data science, machine learning, deep learning, NLP, and generative AI. I engineered features, cleaned and scaled data, built and tuned regression models, conducted exploratory testing with PCA and polynomial transformations, and evaluated performance using industry-standard metrics.

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