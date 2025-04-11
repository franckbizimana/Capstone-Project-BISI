# Capstone Project: Predicting Mental Health Trends in Canada

## Project Summary

This project investigates how economic, social, and environmental factors affect mental health trends across Canadian provinces. The goal is to forecast mental health perceptions using machine learning and visualize the results through an interactive Power BI dashboard.

## Team Members

✅ Yi Cao

Data preprocessing lead

Specialized in time series analysis (ARIMA/SARIMA)


✅ Akhila

Feature engineering and data integration

Worked on regression and XGBoost models


✅ Bibisha Mahat

Exploratory data analysis and correlation studies

Contributed to dashboard design and visuals



✅ Wamungu Francois

Ridge/Lasso regression and multicollinearity mitigation

Team communication and model validation


✅ Yuting Shen

LSTM development and model comparison

Helped resolve technical environment issues


## Objectives

Forecast mental health perception across provinces

Quantify the influence of CPI, unemployment, climate, and search trends

Deliver an interactive Power BI dashboard with scenario testing

## Data Sources

Mental Health Data (StatCan: by province/gender, quarterly)

Unemployment & Inflation Rates (Bank of Canada, StatCan)

Google Trends (topics: depression, anxiety, stress, therapy)

Climate Data (weather stats from Environment Canada)

## Methodology

Data Processing

Aggregated monthly data to quarterly

Filled missing values using midpoint estimation

Checked for seasonality and skewness

Variance inflation factor (VIF) analysis for multicollinearity

Predictive Models

1. Regression Models

Multiple Linear Regression

Ridge & Lasso Regression

Best R²: 0.39 for Fair/Poor mental health category

Addressed multicollinearity using regularization

2. Tree-Based Models

Random Forest Regressor

XGBoost

Effective on small datasets

Handled non-linear relationships

3. Time-Series Models

ARIMA / SARIMA / SARIMAX

SARIMAX best fit across categories

Applied multiple differencing rounds for stationarity

4. Deep Learning / Hybrid Models

LSTM (Limited by data span: 2021–2023)

Time-series XGBoost

Outperformed LSTM due to better generalization with limited data

## Key Challenges

Limited Time Span: Only 9 quarters of data

Model Variance: Different models performed best for different categories

Multicollinearity: Required use of Ridge/Lasso

TensorFlow Issues: Faced environment setup problems with LSTM

Google Colab Timeout: Switched to Jupyter for stability

## Power BI Dashboard Plan

Purpose

Present predictions & insights clearly

Support scenario testing and time/province filtering

Key Visuals

KPI Cards: mental health, inflation, unemployment

Line & Bar Charts: actual vs. predicted values

Heatmaps: by province

What-If Analysis: CPI, unemployment, precipitation

Integration

Combine prediction results from Python with main dataset

Allow user-driven forecasting through DAX parameters

## Repository Structure

📂 mental-health-trends-canada  
 ├── 📂 data/                 # All raw & cleaned datasets  
 ├── 📂 notebooks/           # EDA and modeling Jupyter notebooks  
 ├── 📂 models/              # Serialized models (.pkl/.joblib)  
 ├── 📂 dashboard/           # Power BI files and report exports  
 └── requirements.txt        # Python dependencies  

## Tools & Libraries

Python (pandas, scikit-learn, statsmodels, XGBoost, TensorFlow)

Jupyter Notebook & Google Colab

Power BI

## Want to Explore the Code or Dashboard?

Check the folders:

notebooks/: EDA, modeling

dashboard/: Power BI report and .pbix file

## License

For academic use only. All datasets used are publicly available.
