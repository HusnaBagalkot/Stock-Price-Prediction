# 📈 Stock Price Prediction using Machine Learning
This project uses machine learning to predict stock prices based on historical data. It fetches data using yFinance, applies preprocessing and feature engineering, and uses a Random Forest model for prediction. The system also visualizes trends and evaluates performance using standard metrics.

🔍 Project Overview

This project focuses on predicting stock prices using historical data and machine learning techniques. It uses financial data fetched from Yahoo Finance and applies preprocessing, feature engineering, and a regression model to forecast future stock prices.

The goal is to build a simple yet effective pipeline for stock analysis and prediction that can be extended into real-world applications.

⚙️Technologies Used
* Python
* NumPy
* Pandas
* Matplotlib
* yFinance
* Scikit-learn

📊 Features of the Project
* Fetches real-time historical stock data
* Cleans and preprocesses financial datasets
* Handles multi-level column issues from yFinance
* Performs exploratory data analysis (EDA)
* Applies feature engineering (moving averages)
* Builds a machine learning model (Random Forest)
* Evaluates model performance using MAE, RMSE, and R²
* Visualizes stock trends and predictions
* Predicts next-day stock price
* Exports results to CSV file

---

📁 Dataset
The dataset is obtained using the `yfinance` library:

Stock: Apple Inc. (AAPL)
Time Period: 2015 – 2024

🧠 Machine Learning Workflow
1. Data Collection
Data is fetched using `yfinance.download()`

2. Data Preprocessing
Reset index
Fix multi-level columns
Handle missing values

3. Feature Engineering
Moving Average (MA10)
Moving Average (MA50)

4. Data Scaling
MinMaxScaler used to normalize values between 0 and 1

5. Sequence Creation
Past 60 days used to predict next day

6. Model Training
Random Forest Regressor

7. Prediction
Predict stock closing prices
8. Evaluation Metrics
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)
R² Score

📈 Sample Output
Data Preview
```
Date        Close     High     Low     Open     Volume
2015-01-02  24.21     24.68    23.77   24.67   212818400
```
Model Performance

```
MAE  : 6.09
RMSE : 9.11
R²   : 0.95 (approx)
```
Prediction Table
```
Actual Price | Predicted Price | Error
--------------------------------------
150.23       | 148.90          | 1.33
```
🔮 Next-Day Prediction
The model predicts the next day’s closing price based on the last 60 days of data.
Example:
```
Predicted Closing Price: $189.34
```
📦 How to Run the Project
1. Install Dependencies
```
pip install numpy pandas matplotlib yfinance scikit-learn
```
2. Run the Script

```
python stock_prediction.py
```

📂 Output Files
`stock_predictions.csv` → Contains actual vs predicted values

🚀 Future Improvements
Implement LSTM / Deep Learning models
Add real-time prediction dashboard (Streamlit)
Include multiple stocks
Add buy/sell signal generation
Deploy as a web application
 
Conclusion
This project demonstrates how machine learning can be applied to financial data for predictive analysis. While simple, it forms a strong foundation for building advanced AI-based trading systems.

👩‍💻Author
Husna Bagalkot
Computer Science Engineering (AI & ML)
