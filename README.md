*all data is from Tilastokeskus (https://stat.fi/fi)*

**SARIMAX**

Monthly time series of the industrial production volume index is modeled using a SARIMAX model in Python.

The final SARIMA model includes non-seasonal and seasonal moving average components with both non-seasonal and seasonal differencing, and it does not include any autoregressive components. SARIMAX(0,1,1)x(0,1,1,12)

These are used to capture the evolution of the index with a proper train-test split.

The forecast is a multi-step forecast in an internal recursion sense.

**VAR**

Quarterly time series of vacancies and unemployment is modeled using a Vector Autoregressive (VAR) model.

The optimal lag structure is selected using Python’s select_order function, minimizing the AIC (Akaike Information Criterion), which balances model complexity and goodness of fit.

The two series move in opposite directions, with vacancies acting as a leading indicator of unemployment.

The forecast is a multi-step forecast in an internal recursion sense.

**Prophet**

Quarterly time series of Kruununhaka m²/€ real estate prices is modeled using Prophet, to capture long-term trend and seasonality.

A forward forecast of 20 quarters (5 years) is generated.

The forecast is a one-shot multi-step forecast, where all future points are predicted simultaneously.

**RNNs (LSTM and GRU)**

A comparison of LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit) is performed on quarterly bankruptcy data.

The models are trained and evaluated using validation and test sets to select the best-performing architecture and feature set.

The GRU model shows slightly better generalization on the test set.

Both models are trained using a 12-period sliding window to predict a one-step-ahead forecast. Model weights are updated after each batch of 64 samples. This process is repeated for 60 epochs with early stopping (patience) with respect to validation loss.

- In-sample forecasting: one-step-ahead prediction

- Out-of-sample forecasting: recursive forecast of 8 quarters ahead
