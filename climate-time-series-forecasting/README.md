# Climate Time Series Forecasting

## Description
This project implements RNN-based models for temperature forecasting using the Jena Climate dataset. It compares SimpleRNN, LSTM, and Bidirectional LSTM architectures for multivariate time series prediction.

## Dataset
- **Source**: Jena Climate Dataset (2009-2016)
- **Target**: Temperature (T in degC)
- **Task**: Multi-step ahead forecasting (horizon = 10)

## Approach
1. **Data Loading**: Load climate data from Google Storage
2. **Preprocessing**: 
   - Extract temperature variable
   - Train/Validation/Test split (70/15/15)
   - MinMax normalization
3. **Sequence Creation**: Create sequences with lookback=72, horizon=10
4. **Models**:
   - SimpleRNN
   - LSTM
   - Bidirectional LSTM
5. **Evaluation**: MAE, RMSE, R2 per horizon

## Results
- Performance comparison across models
- Learning curves visualization
- Horizon-wise metrics analysis

## Key Insights
- LSTM outperforms SimpleRNN for long-term dependencies
- Bidirectional LSTM provides additional context
- Prediction error increases with horizon

## Technologies
- Python 3
- TensorFlow / Keras
- Scikit-learn
- Pandas, NumPy, Matplotlib

## Author
Zakaria Rebbah

## License
MIT