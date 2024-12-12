---
id: 1734034463-model-accuracy-and-metrics
aliases:
  - Model Accuracy and Metrics
tags:
  - regression
---

# Model Accuracy and Metrics

## Key Concepts:
1. **Model Accuracy**: Measures how well a model predicts values, ensuring better decisions and identifying areas for improvement. Residuals (differences between actual and predicted values) help assess model fit.

2. **Metrics for Accuracy**:
   - **Mean Absolute Error (MAE)**: Average absolute residual values, less sensitive to outliers.
   - **Mean Squared Error (MSE)**: Average squared residuals, emphasizes larger errors.
   - **Root Mean Squared Error (RMSE)**: Square root of MSE, interpretable in the same units as the target variable.

3. **Context Importance**: Accuracy metrics should be interpreted within the context of the problem.

## Python Example: MAE, MSE, and RMSE Calculation
```python
import numpy as np

# Observed and predicted values
observed = np.array([10, 20, 30, 40, 50])
predicted = np.array([12, 18, 33, 39, 47])

# Calculations
mae = np.mean(np.abs(observed - predicted))
mse = np.mean((observed - predicted) ** 2)
rmse = np.sqrt(mse)

print(f"MAE: {mae:.2f}, MSE: {mse:.2f}, RMSE: {rmse:.2f}")
```

This script calculates the error metrics for any observed and predicted dataset, aiding in model evaluation.
