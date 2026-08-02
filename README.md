# Time-Based-Stock-Price-Prediction-for-TSLA
Machine learning project for next-day TSLA stock price prediction using Linear Regression, Decision Tree, and Random Forest with technical indicators and time-based evaluation.

# 📈 Time-Based Stock Price Prediction for TSLA

A machine learning project for predicting the **next-day closing price of Tesla (TSLA) stock** using historical stock data, technical indicators, and multiple regression algorithms.

The project follows a **time-based train-test approach** to preserve the chronological order of stock market data and compares multiple machine learning models to determine the best-performing model.

---

## 🎯 Project Objective

The main objective of this project is to build and evaluate machine learning models for predicting the **next-day TSLA closing price**.

The project focuses on:

- Collecting historical TSLA stock data
- Performing data preprocessing
- Creating lag-based and technical indicator features
- Using an 80/20 time-based train-test split
- Training multiple regression models
- Performing hyperparameter tuning
- Evaluating and comparing model performance
- Selecting the best-performing model
- Visualizing predictions and model performance
- Saving the trained model and prediction results

---

## 📊 Dataset

Historical Tesla stock market data is downloaded directly using the **yfinance** Python library.

- **Stock:** Tesla, Inc.
- **Ticker:** TSLA
- **Period:** Last 5 years
- **Source:** Yahoo Finance through `yfinance`

---

## ⚙️ Feature Engineering

Several features are generated from the historical stock data.

### Lag Features
- 1-day lag
- 2-day lag
- 3-day lag
- 5-day lag
- 7-day lag
- 14-day lag

### Moving Averages
- SMA 5
- SMA 10
- SMA 20
- EMA 5
- EMA 10
- EMA 20

### Technical Indicators
- Relative Strength Index (RSI)
- MACD
- MACD Signal
- Bollinger Upper Band
- Bollinger Lower Band
- Momentum
- Daily Return
- Volatility

The target variable is created by shifting the closing price by one day, allowing the models to predict the **next-day closing price**.

---

## 🤖 Machine Learning Models

Three regression algorithms are implemented:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**

`GridSearchCV` is used to perform hyperparameter tuning for the Decision Tree and Random Forest models.

---

## ⏳ Time-Based Train-Test Split

Because stock prices are time-series data, the dataset is **not randomly shuffled**.

The data is divided chronologically:

- **80% Training Data**
- **20% Testing Data**

This ensures that earlier observations are used for training while later observations are used for testing.

---

## 📏 Evaluation Metrics

The models are evaluated using:

- **MAE** – Mean Absolute Error
- **MSE** – Mean Squared Error
- **RMSE** – Root Mean Squared Error
- **R² Score** – Coefficient of Determination

The best model is selected based primarily on **lower RMSE** and **higher R² Score**.

---

## 📉 Visualizations

The project generates several visualizations:

- TSLA Closing Price Trend
- Feature Correlation Heatmap
- Actual vs Predicted Stock Prices
- Residual Plots
- Feature Importance
- RMSE Comparison
- R² Score Comparison

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- yfinance
- Joblib

---

## 📂 Project Structure

```text
Time-Based-Stock-Price-Prediction-for-TSLA/
│
├── Time-Based Stock Price Prediction for TSLA.ipynb
├── README.md
├── requirements.txt
└── .gitignore

🔄 Project Workflow
TSLA Data Download
        ↓
Data Preprocessing
        ↓
Feature Engineering
        ↓
Create Next-Day Target
        ↓
80/20 Time-Based Split
        ↓
Model Training
        ↓
Hyperparameter Tuning
        ↓
Model Evaluation
        ↓
Model Comparison
        ↓
Best Model Selection
        ↓
Prediction & Visualization


## 🚀 How to Run the Project

### Option 1: Run Using Google Colab

1. Open the `Time-Based Stock Price Prediction for TSLA.ipynb` file from this repository.
2. Click **Open in Colab** at the top of the notebook.
3. Once the notebook opens in Google Colab, select:

   **Runtime → Run all**

4. If required, install the necessary libraries using:

```python
!pip install yfinance
```

5. Run all cells sequentially to download the TSLA stock data, perform feature engineering, train the machine learning models, and generate the results.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/Yatharth7651/Time-Based-Stock-Price-Prediction-for-TSLA.git
```

Navigate to the project directory:

```bash
cd Time-Based-Stock-Price-Prediction-for-TSLA
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Then open the `.ipynb` file using Jupyter Notebook or VS Code.


---

## 💾 Generated Outputs

After successfully running the notebook, the project generates:

- `best_model.pkl` – Saved best-performing machine learning model
- `predictions.csv` – Actual and predicted TSLA stock prices
- `model_metrics_comparison.csv` – Comparison of model evaluation metrics
- TSLA closing price trend visualization
- Feature correlation heatmap
- Actual vs Predicted price plots
- Residual plots
- Feature importance visualization
- Model performance comparison plots

---

## ⚠️ Disclaimer

This project is developed for **educational and academic purposes only**.

The stock price predictions generated by the machine learning models should not be considered financial or investment advice.
