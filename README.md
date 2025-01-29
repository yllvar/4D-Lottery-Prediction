# 4D Lottery Prediction Using Linear Regression

## Project Overview

This project aims to predict the next 4-digit lottery number using historical 4D lottery data. The dataset contains previous draw results, including 1st, 2nd, and 3rd prize numbers, special numbers, and consolation numbers. A linear regression model is trained using this historical data to generate a prediction for the next draw's 1st prize number.

### Dataset Description

The dataset (4d.csv) consists of 5285 entries with the following columns:

DrawNo: The unique identifier for each draw.

DrawDate: The date of the draw.

1stPrizeNo, 2ndPrizeNo, 3rdPrizeNo: Winning numbers for the top three prizes.

SpecialNo1 - SpecialNo10: Ten special prize numbers.

ConsolationNo1 - ConsolationNo10: Ten consolation prize numbers.

### Implementation Steps

Data Loading and Exploration

The dataset is loaded using pandas.read_csv().

The first few rows and summary statistics are displayed to understand the structure and data types.

Feature Selection and Preprocessing

The model uses past winning numbers as input features.

The 1stPrizeNo is chosen as the target variable.

Missing values (if any) are filled using forward filling (ffill).

### Train-Test Split

The dataset is split into training (80%) and testing (20%) subsets using train_test_split().

## Model Training

A LinearRegression model from sklearn.linear_model is initialized and trained on the training set.

## Prediction

The trained model predicts the next 4-digit number based on the last row of the dataset.

### Key Observations

The model treats the prediction task as a regression problem, predicting the next 1stPrizeNo based on past numbers.

Due to the randomness of lottery results, the accuracy of this approach is highly uncertain.

The dataset contains structured numerical values, making it suitable for machine learning, but real-world lottery numbers follow a non-deterministic pattern.

## Limitations

Randomness: Lottery numbers are drawn randomly, making prediction inherently unreliable.

Linear Model Limitations: A simple linear regression model may not capture complex patterns in the data.

Feature Dependence: The model assumes past numbers influence future draws, which may not be valid.

### Future Improvements

Exploring deep learning techniques (e.g., recurrent neural networks) for better pattern recognition.

Incorporating additional data sources, such as statistical frequency analysis.

Testing alternative machine learning models, like decision trees or ensemble methods.

Applying time series forecasting techniques, such as ARIMA or LSTMs, to capture potential hidden patterns.

---
### Conclusion

This project demonstrates a machine learning approach to predicting lottery numbers but highlights the challenges due to randomness. While educational, it is not a reliable method for lottery prediction.

