This project implements an ARMA(1,1) model in Python to analyze and forecast a univariate time series. It estimates model parameters, generates one-step-ahead forecasts, and evaluates prediction accuracy.

**Key Focus:**  
- Estimation of ARMA(1,1) model parameters and comparison to theoretical values  
- One-step-ahead forecasting for the last 10 observations  
- Evaluation using forecast errors and 90% prediction intervals  
- Analysis of model robustness and predictive reliability

**Tools & Methods:**  
- Python (statsmodels) for ARMA modeling and forecasting  
- One-step-ahead forecasts with 10-fold cross-validation  
- Prediction interval analysis  

**Results:**  
- Estimated parameters closely match theoretical values (AR: 0.416, MA: 0.565 vs true 0.5 each)  
- Forecasts capture the general structure of the series  
- 8 out of 10 observations fall within 90% prediction intervals, demonstrating model reliability

**Objective:**  
To develop a robust predictive model for time series data and demonstrate the ability to interpret, evaluate, and communicate model performance effectively.
