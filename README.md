# Weather Forecasting using Machine Learning

## Project Overview
This project focuses on weather forecasting using multiple machine learning models, including ARIMA, Prophet, and Gradient Boosting Regressor. The dataset was sourced from the Kaggle Global Weather Repository and analyzed to predict temperature trends. The project aligns with the **PM Accelerator Mission** by enhancing analytical, decision-making, and forecasting skills through structured learning and model evaluation.

## Table of Contents
- [Project Methodology](#project-methodology)
- [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Building and Evaluation](#model-building-and-evaluation)
- [Advanced Analyses](#advanced-analyses)
- [Key Insights and Conclusions](#key-insights-and-conclusions)
- [Future Work](#future-work)
- [Setup and Installation](#setup-and-installation)
- [Results](#results)
- [References](#references)

## Project Methodology
1. **Data Collection**: Obtained historical weather data from the Kaggle Global Weather Repository.
2. **Data Cleaning & Preprocessing**: Handled missing values, normalized data, and removed outliers.
3. **Exploratory Data Analysis (EDA)**: Identified trends, seasonality, and relationships between variables.
4. **Model Selection & Training**: Used ARIMA, Prophet, and Gradient Boosting Regressor for forecasting.
5. **Evaluation**: Compared model performance using MAE and RMSE.
6. **Advanced Analysis**: Performed anomaly detection, climate analysis, and spatial analysis.
7. **Results Interpretation**: Extracted meaningful insights for real-world applications.

## Data Cleaning and Preprocessing
- **Handling Missing Values**
  - Numeric columns: Filled with the median.
  - Categorical columns: Filled with the mode.
- **Handling Outliers**
  - Used the IQR method to cap outliers in numeric columns.
- **Normalization**
  - Applied MinMaxScaler to normalize numeric columns.

## Exploratory Data Analysis (EDA)
- **Temperature Trend Over Time**: Seasonal variations observed with peaks in summer and troughs in winter.
- **Precipitation Trend**: Higher rainfall during monsoon seasons and lower levels during dry periods.
- **Correlation Heatmap**: Strong positive correlation between temperature and humidity, negative correlation with wind speed.

## Model Building and Evaluation
### ARIMA Model
- Split data (80% training, 20% testing).
- Parameters: (5, 1, 0)
- **Performance**:
  - MAE: 0.2297
  - RMSE: 0.2580

### Prophet Model
- Forecasted future temperatures for 1 year.
- Captures seasonal trends and holidays effectively.

### Gradient Boosting Regressor
- Feature encoding and train-test split.
- **Performance**:
  - MAE: 0.0010
  - RMSE: 0.0015

### Ensemble Modeling
- Combined forecasts from ARIMA, Prophet, and Gradient Boosting.
- **Performance**:
  - MAE: 0.2042
  - RMSE: 0.2418

### Optimized Ensemble Model
- Used stacking model (Gradient Boosting) for optimization.
- **Performance**:
  - MAE: 0.1980
  - RMSE: 0.2253

## Advanced Analyses
- **Anomaly Detection**: Identified 2894 temperature anomalies using Isolation Forest.
- **Climate Analysis**: Long-term trends indicate potential climate change effects.
- **Environmental Impact**: Negative correlation between temperature and PM2.5 levels.
- **Feature Importance**: Key influencers include humidity, wind speed, and air quality metrics.
- **Spatial Analysis**: Temperature variations analyzed using GeoPandas.

## Key Insights and Conclusions
- ARIMA and Prophet models effectively capture seasonal trends.
- Gradient Boosting Regressor demonstrates high accuracy due to feature engineering.
- Ensemble modeling improves forecast performance.
- Significant correlations between air quality metrics and temperature.
- Regional temperature variations support spatial analysis.

## Future Work
- Integrate real-time data for continuous forecasting.
- Experiment with deep learning models like LSTM.
- Analyze additional weather parameters for enhanced insights.

## Setup and Installation
### Requirements
```bash
pip install numpy pandas scikit-learn statsmodels fbprophet matplotlib seaborn geopandas
```

### Running the Project
```bash
python forecast.py  # Run the forecasting models
```

## Results
- The **Gradient Boosting Regressor** achieved the highest accuracy with minimal error rates.
- The **ensemble model** further improved forecast reliability by combining multiple methods.
- **Environmental analysis** showed that temperature variations significantly impact air quality.
- **Anomaly detection** highlighted extreme weather conditions, aiding in climate impact studies.

## References
- Kaggle dataset: "Global Weather Repository"
- Libraries: Pandas, NumPy, Scikit-learn, Statsmodels, GeoPandas, Matplotlib & Seaborn
