Problem Statement:
The aim of this project is to develop a machine learning model capable of predicting the next day’s closing price of a stock using historical stock market data. Stock price prediction is inherently complex due to market volatility, noise, and the influence of multiple external factors. This project focuses on leveraging historical numerical features to perform short-term forecasting of stock prices.

Objective:
The primary objective is to predict the next day’s closing price of a selected stock using historical data such as Open, High, Low, and Volume. The project involves applying machine learning models, specifically Linear Regression and Random Forest Regressor, to learn patterns from past data. Additionally, the project aims to evaluate model performance and visualize the comparison between actual and predicted stock prices.

Dataset and Data Downloading:
The dataset is obtained from Yahoo Finance using the yfinance Python library. Historical stock data is fetched programmatically by specifying the stock ticker symbol along with a defined date range. The dataset includes key features such as Open price, High price, Low price, Close price, and Volume of shares traded. To create the prediction target, the Close price column is shifted upward by one day, allowing the model to learn how current day features relate to the next day’s closing price.

Solution Approach:
The solution begins with collecting historical stock data using the yfinance library. The data is then preprocessed by selecting relevant features (Open, High, Low, Volume) and removing missing values. A new target variable representing the next day’s closing price is created by shifting the Close column. The dataset is split into training and testing sets, typically in an 80:20 ratio, while maintaining the time-series order (no shuffling).

Two machine learning models are trained: Linear Regression, which serves as a simple baseline model assuming a linear relationship between features and the target, and Random Forest Regressor, an ensemble learning method capable of capturing non-linear relationships and providing more robust predictions.

Model performance is evaluated using Root Mean Squared Error (RMSE), which measures the difference between actual and predicted values. Lower RMSE indicates better performance. Finally, the trained models are used to predict the next day’s closing price based on the most recent available data. Visualization is also performed by plotting actual versus predicted prices, helping to assess how well the models perform.

Overall, the project demonstrates how machine learning techniques can be applied to financial time-series data for short-term stock price prediction, while also highlighting limitations such as lack of external factors like news sentiment or economic indicators.
