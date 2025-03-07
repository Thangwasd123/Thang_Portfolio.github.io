---
layout: default
title: Enigma's Hackathon - IDL Logistics
---

# Enigma Hackathon: Time Series Demand Planning for IDL Logistics

## Overview
This project was developed during the Enigma Hackathon, where our team created a time series forecasting solution for IDL Logistics to predict and optimize supply chain demand.

## 🏆 Challenge
<img src="IDL%20Logo.png" alt="IDL Logo" width="300">
IDL Logistics is a logistics forwarder company with over 20 years of experiences. Being a logistics forwarder, meaning their business involve with a lot of fulfillment works. This can range anything from just a small one box order, to a big multi pallets, multi boxes orders. The human resources planning therefore is incredibly important to IDL Logistics operations. 

The challenge therefore was to create a prediction pipeline that forecasts how many orders IDL Logistics will receive in a given period. We were given 12 hours to work on this project.

The dataset contains:
- 2 years of data from July 2022 to August 2023.
- And data from January 2024 to 31st December 2024.

## 🛠️ Solution

We developed an ARIMA-based forecasting system that enables accurate prediction of logistics demand, helping IDL optimize their operations.
We also developed a protocol to cleaning and stablizing the high variance and trend difference that IDL Logstics have to acchive stationarity for predictions.

The final solution metrics were:
- RMSE: 822.83
- RMSE Percentage: 16.85%

Below you will find our predictions:

<img src="Final%20IDL%20predictions%20fit.png" alt="IDL predictions">

### Key Features
- Optimal outlier trimming parameter
- Time series analysis using ARIMA modeling

## 📊 Data Analysis Process

### 1. Data Exploration
- Initial dataset characteristics
- Identified seasonality and trend patterns
- Correlation analysis with external factors

### 2. Data Preprocessing
- Handling missing values
- Normalizing time series data
- Feature engineering

### 3. Model Development
- ARIMA parameter tuning
- Validation methodology
- Comparison with baseline models

### 4. Implementation
- Integration with existing systems
- Deployment approach
- Monitoring mechanisms

## 📈 Results & Impact

- [Quantitative results - accuracy metrics, performance improvements]
- [Business impact - cost savings, efficiency gains]
- [Feedback from IDL Logistics]

## 🔍 Technical Details

### Technologies Used
- Python
- ARIMA for time series forecasting
- [Other libraries/frameworks - add details]
- [Visualization tools used]

### Code Snippets

```python
# Add a key code snippet here that demonstrates your approach
# For example, your ARIMA model implementation or data preprocessing
```

## 👥 Team

- [Your name and role]
- [Team members - if applicable]

## 🔮 Future Improvements

- [Ideas for enhancing the model]
- [Additional features that could be implemented]
- [Potential applications to other business areas]

## 📚 Resources

- [Links to papers or resources that informed your approach]
- [Documentation for key technologies used]
- [Other related projects or inspirations]

---

*This project was completed as part of the Enigma Hackathon in [month/year]*
