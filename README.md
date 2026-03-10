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


## 🚀 Getting Started

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Google Colab (for cloud execution)

### Installation

1. Clone the repository:

git clone https://github.com/mohitjain2/Energy-Consumption-Forecast.git
cd Energy-Consumption-Forecast

pip install pandas numpy matplotlib scikit-learn keras statsmodels

jupyter notebook Energy_Consumption_Forecast.ipynb

2. Data Setup
The notebook expects data in Google Drive under the path:
/content/drive/MyDrive/Colab Notebooks/Project Energy/Input/daily_dataset/daily_dataset/

Update the data path in the notebook if your structure differs.

## 📝 Notebook Sections
Google Drive Mount: Connect to Google Drive for data access
Importing Libraries: Load all required dependencies
Energy Data Preparation:
Combine blocks into single dataframe
Calculate energy sums
Household Normalization:
Account for varying household counts across days
Create per-household metrics
Data Analysis: Descriptive statistics and visualizations
Time Series Analysis: ACF/PACF plots and stationarity tests
Forecasting Models: Implementation of ARIMA, SARIMA, and LSTM models

## 📊 Output
The analysis produces:

Combined energy dataset with normalized consumption metrics
Time series visualizations showing consumption trends
Model predictions and forecasting accuracy metrics
Weather-energy correlation insights

## 🔍 Key Findings
Seasonal Patterns: Clear seasonal variations in energy consumption
Household Adoption: Gradual increase in smart meter adoption from 13 to 5,541 households
Normalization Impact: Per-household metrics provide more reliable forecasting baseline
Data Quality: Starting with only 13 households in November 2011, reaching full deployment over time

## 🔧 Future Improvements
 Include weather data integration
 Advanced feature engineering (holidays, events)
 Ensemble forecasting methods
 Real-time prediction pipeline
 Model deployment for production use
 Explainability analysis (SHAP, LIME)

## 📚 References
Smart Meters Initiative: EU-led program for energy infrastructure upgrade
Dataset Source: London Data Store
Time Series Forecasting: ARIMA/SARIMA methodology
Deep Learning: LSTM networks for sequential data

## 👨‍💻 Author
Mohit Jain - @mohitjain2
