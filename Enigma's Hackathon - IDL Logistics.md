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

**The dataset contains:**
- 2 years of data from July 2022 to August 2023.
- And data from January 2024 to 31st December 2024.

## 🛠️ Solution

We as a team (Yash, Yashar and me - Thang)  developed an ARIMA-based forecasting system that enables accurate prediction of logistics demand, helping IDL optimize their operations.
We also developed a protocol to cleaning and stablizing the high variance and trend difference that IDL Logstics have to acchive stationarity for predictions.

**The final solution metrics were:**
- **RMSE: 822.83**
- **RMSE Percentage: 16.85%**

**Below is our predictions:**

<img src="Final%20IDL%20predictions%20fit.png" alt="IDL predictions">

### Key Features
- Optimal outlier trimming parameter
- Time series analysis using ARIMA modeling

## 📊 Data Analysis Process

### 1. Data Preparation & Exploration
- Initial dataset characteristics:

  **The dataset contains 15 columns with diverse data concerning date of orders, pcs of orders, and delivered pcs, etc.**
  
  <img src="IDL%20Dataset.png" alt="IDL Dataset Table">

  **After multiple plotting and decision making, we decided that the best two variables to proceed with are:**
    - Interface Date (Order Date in laymen term) as feature.
    - Ordered Pce's (Ordered Pcs in a single in laymen term) as target variable.

  Therefore we performed columns dropping of all the unecessary columns:
  <img src="IDL%20-%20Dropping%20Columns%20to%20lighten%20overhead%20Calculation.png" alt="IDL Columns Dropping">

  We then concatenated the dataset, and below is the line plot.
  <img src="IDL%20-%20Dataset%20without%20Interpolation.png" alt="IDL Data Plot w.o. Interpolation">

-> It therefore became clear to us that we had a missing period of 4 months. This was a hidden part of the challenge that we had to overcome. Hence, the decision was to interpolate this missing period with the same period of the previous multiply by a random variable. 

  **This is the interpolation procedure using Numpy.**
  <img src="IDL%20-%20Interpolation%20of%20dataset.png" alt="Interpolation of dataset">

  **The plot of the dataset with interpolation.**
  <img src="IDL%20-%20Final%20Dataset%20plot%20post%20interpolation.png" alt="Interpolation plot of dataset">
  
  **-> We are now confident that we have a complete dataset to begin performing addtional exploratory work on.**

- Histogram plot
  <img src="IDL%20-%20Histogram%20of%20dataset.png" alt="Histogram plot of dataset">
  **-> It became clear to us that the general distribution is between 3000 -> 9.000**

- Diving a bit deeper, we wanted to see how many days are there with orders above 9000 to confirm that we can single them out as outlier.
  <img src="IDL%20-%20Outlier%20Identification.png" alt="scatter plot of outliers">
  **-> We can confirm now that there are only a couple of days that has abnormal low sales or high sales due to Q4 or just an technical issue in data system.**
  
- Next, to learn more about the dataset, we needed to lean about the seasonality of the dataset.
  **Box plot of days of year**
  <img src="IDL%20-%20Boxplot%20by%20day%20of%20year.png" alt="Box Plot by day of years">

  **Box plot of day of week**
  <img src="IDL%20-%20Boxplot%20by%20day%20of%20week.png" alt="Box Plot by day of week">
  
- Features Target relationship box plot


### 2. Model Development
- ARIMA parameter tuning
- Validation methodology
- Comparison with baseline models

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
