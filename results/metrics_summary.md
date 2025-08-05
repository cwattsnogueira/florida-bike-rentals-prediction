# Metrics Summary

This document provides a summary of the model performance metrics used in the bike rental prediction project.

## Model Configuration

- Model: Random Forest Regressor
- Dataset: Bike Sharing Dataset
- Key Features: Temperature, Humidity, Day of the Week, Hour

## Evaluation Metrics

| Metric                       | Value     |
|-----------------------------|-----------|
| R² Score                    | 0.87      |
| RMSE (Root Mean Squared Error) | 134.21    |
| MAE (Mean Absolute Error)   | 95.46     |
| Training Time               | 2.4 seconds |

## Observations

- The model performed well in predicting the number of rented bikes, especially during peak hours.
- Larger errors were observed on atypical days with unstable weather.
- Feature importance analysis highlighted temperature and hour as the most influential variables.

---

> Last updated: `2025-08-05`