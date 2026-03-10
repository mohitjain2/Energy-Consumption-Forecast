# Energy Consumption Forecast

A machine learning project to predict energy consumption patterns using historical data from London households. This project analyzes smart meter data and builds forecasting models to help energy suppliers better understand and predict energy demand.

## 📋 Project Overview

This project uses a dataset of 5,567 London households participating in the smart meter rollout program. The goal is to create accurate energy consumption forecasts by analyzing daily energy consumption patterns and incorporating weather conditions.

**Key Features:**
- Data aggregation from 112 CSV blocks into a unified dataset
- Household-level normalization to handle inconsistent data collection
- Weather-based clustering for pattern identification
- Time series forecasting using multiple approaches

## 📊 Dataset

- **Source**: London Data Store (refactored version)
- **Time Period**: November 23, 2011 - February 28, 2014
- **Households**: 5,567 London households
- **Records**: 3,536,007 daily energy readings
- **Coverage**: England, Wales, and Scotland

## 🎯 Approach

1. **Data Preparation**
   - Combine all 112 data blocks into a single dataframe
   - Extract relevant columns: `day`, `LCLid` (household ID), `energy_sum`
   - Normalize energy consumption by household count to account for gradual smart meter adoption

2. **Feature Engineering**
   - Aggregate daily energy consumption at the household level
   - Calculate average energy per household to normalize for inconsistent data collection
   - Create day-level aggregations for time series analysis

3. **Analysis & Clustering**
   - Explore relationships between weather conditions and energy consumption
   - Use K-Means clustering to identify weather patterns
   - Add weather identifiers to day-level data for enhanced predictions

4. **Forecasting Models**
   - ARIMA models for baseline time series forecasting
   - SARIMA for seasonal decomposition
   - LSTM neural networks for deep learning-based predictions
   - MinMax scaling for normalization

## 🛠️ Technologies & Libraries

### Data Processing
- **pandas**: Data manipulation and aggregation
- **numpy**: Numerical computations

### Time Series Analysis
- **statsmodels**: ARIMA, SARIMA, ACF/PACF analysis
- **statsmodels.tsa.statespace.sarimax**: Seasonal ARIMA modeling
- **pandas.plotting**: Autocorrelation plots

### Machine Learning
- **scikit-learn**: K-Means clustering, preprocessing, metrics
- **keras**: LSTM neural networks
- **MinMaxScaler**: Feature scaling

### Visualization
- **matplotlib**: Plotting and visualization

## 📈 Key Statistics

| Metric | Value |
|--------|-------|
| Average Daily Energy Sum | 43,535.33 kWh |
| Total Days Covered | 829 |
| Average Households per Day | 4,234 |
| Energy Range | 0.21 - 15.96 per household |

## 📁 Project Structure
