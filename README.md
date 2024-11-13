# Passenger Volume Prediction for Bus Travel in Passau

## Project Overview

This project aims to forecast bus passenger volume in Passau, Bavaria, Germany, by analyzing historical ticket sales data from Deutsche Bahn Regional and weather data from the Deutscher Wetterdienst (DWD). The models used include Random Forest, ARIMA, and LSTM, each applied to address specific research questions on the effect of external factors like weather, weekends, and holidays on passenger counts.

## Research Questions

1. **Impact of Weather**: How does weather affect passenger volume during different periods?
2. **Impact of Days**: What effect do working days, weekends, and holidays have on passenger volume?
3. **Model Performance**: How well do ARIMA and LSTM models predict passenger counts?
4. **Geolocation Influence**: Does the location of bus stops, represented by population density, affect passenger volume?

## Data Sources

- **Ticket Sales Data**: Sourced from Deutsche Bahn Regional for different bus stops in Passau.
- **Weather Data**: Collected from the DWD Climate Data Center, including temperature, precipitation, and wind speed data.

## Methodology

1. **Random Forest**: Used as a baseline model to analyze the effect of features like weather, weekend, and holiday.
2. **ARIMA**: Applied to predict passenger volume based on a stationary time series, optimized through Auto ARIMA.
3. **LSTM**: Deployed with 50 models, one per bus stop, using a sequential structure to predict passenger volumes with time series data.

## Results

- **Random Forest**: F1-score ranged from 0.36 to 0.40, with the weekend feature having the most significant impact.
- **ARIMA**: Produced a low F1-score of 0.11, potentially due to data imbalances and limited feature handling.
- **LSTM**: Achieved a mean F1 score between 0.2 and 0.4, indicating better performance than ARIMA but still requiring improvements.

## Evaluation Metrics

- **Accuracy**: Ratio of correct predictions.
- **F1-Score**: Harmonic mean of precision and recall, used to address imbalanced data.

## Limitations and Future Work

- **ARIMA Limitations**: Sensitivity to hyperparameters and limited feature handling.
- **LSTM Improvements**: Further tuning of hyperparameters and model complexity needed.
- **Future Enhancements**: Incorporate additional features, refine pre-processing, and potentially explore other models like GRU or advanced RNN architectures.

## References

1. Deutsche Bahn - DB Bahn Regional.
2. Deutscher Wetterdienst Open Data Service.
3. Various studies on time series forecasting in transportation.
