# Multivariate Climate Forecasting

## Description
This project extends climate forecasting to predict multiple variables simultaneously (temperature, humidity, pressure) using LSTM and Bidirectional LSTM models.

## Dataset
- **Source**: Jena Climate Dataset (2009-2016)
- **Targets**: 
  - T (degC) - Temperature
  - rh (%) - Relative humidity
  - p (mbar) - Pressure
- **Features**: 6 meteorological variables
- **Task**: Multi-output multi-step forecasting

## Approach
1. **Data Loading & Preprocessing**:
   - Resample to hourly data
   - Handle missing values (interpolation)
   - Separate X (features) and y (targets)
2. **Train/Val/Test Split**: 70/15/15
3. **Normalization**: Separate scalers for X and y
4. **Sequence Creation**: lookback=72, horizon=12
5. **Models**:
   - LSTM (64 units)
   - Bidirectional LSTM (64 units)
6. **Evaluation**: MAE, RMSE, R2 per horizon and per variable

## Results
- Comparative analysis LSTM vs BiLSTM
- Per-variable performance metrics
- Horizon-wise error analysis

## Key Insights
- Temperature is easiest to predict
- Pressure shows more variability
- Prediction accuracy decreases with horizon

## Technologies
- Python 3
- TensorFlow / Keras
- Scikit-learn
- Pandas, NumPy, Matplotlib, Seaborn

## Author
Zakaria Rebbah

## License
MIT