
# 📊 Bitcoin Market Sentiment & Trader Performance Analysis

## 📌 Project Overview

This project explores the relationship between **Bitcoin market sentiment (Fear vs Greed)** and **trader performance** using real trading data. The goal is to uncover hidden patterns in profitability, leverage, and trading behavior that can help design **smarter trading strategies**.

We use:

* **Bitcoin Market Sentiment Dataset**

  * Columns: `Date`, `Classification` (Fear/Greed)
* **Historical Trader Data (Hyperliquid)**

  * Columns: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`, etc.

---

## 🚀 Objectives

* 📌 Understand how **market sentiment** (Fear/Greed) influences **trader behavior**.
* 📌 Analyze **profitability, leverage, trade size, and volume** across different sentiment regimes.
* 📌 Build **ML models** to predict next-day profitability and sentiment-driven outcomes.
* 📌 Generate **visual insights** that highlight trading patterns.

---

## 🛠️ Tech Stack

* **Python** (Google Colab)
* **Pandas, NumPy** → Data Cleaning & Transformation
* **Matplotlib, Seaborn** → Visualization
* **Scikit-learn** → Machine Learning (RandomForest Classifier & Regressor)

---

## 📂 Project Structure

```
├── data/
│   ├── bitcoin_sentiment.csv
│   ├── trader_data.csv
├── notebook/
│   ├── Bitcoin_Trader_Sentiment_Analysis.ipynb
├── outputs/
│   ├── daily_merged.csv
│   ├── account_metrics.csv
├── README.md
```

---

## 🔎 Key Steps in Analysis

### 1️⃣ Data Loading & Exploration

* Load sentiment + trader data from CSV/Google Drive.
* Check columns, missing values, and data types.
* Align timestamps for merging.

### 2️⃣ Data Cleaning & Feature Engineering

* Normalize column names.
* Create rolling statistics (volatility, average PnL).
* Add lagged sentiment features.

### 3️⃣ Exploratory Data Analysis (EDA)

* Distribution of **Fear vs Greed** days.
* Profitability patterns across sentiments.
* Leverage and trade size analysis.

### 4️⃣ Modeling

* **Classification**: Predict sentiment-driven outcomes using RandomForest.
* **Regression**: Predict next-day trader PnL using RandomForest Regressor.

### 5️⃣ Visualization Insights

* 📊 **Boxplot**: PnL vs Sentiment (Fear/Greed).
* 📊 **Lineplot**: Average leverage trends by sentiment.
* 📊 **Scatterplot**: Trade size vs Profitability.

---

## 📈 Results

* **Feature Importances**:

  * Rolling volatility, lagged sentiment, and leverage were the strongest predictors.
* **Classification Model (RandomForest)**:

  * Achieved strong accuracy in predicting sentiment-driven profitability.
* **Regression Model**:

  * Reasonably predicted next-day PnL trends.
* **Insights**:

  * Traders often take **higher leverage during Greed days**, increasing both risk and reward.
  * **Fear days** showed smaller trade sizes but sometimes more stable profits.

---

## 💡 Key Takeaways

* Market sentiment plays a **significant role** in trading decisions.
* Features like **lagged sentiment & leverage** are strong indicators of profitability.
* RandomForest provides a solid baseline; next steps include **hyperparameter tuning, cross-validation, and backtesting**.

---

## 🖼️ Sample Visualizations

![PnL vs Sentiment](example_boxplot.png)
![Leverage Trend](example_lineplot.png)
![Trade Size vs Profitability](example_scatter.png)

---

## 📌 Next Steps

* 🔹 Add hyperparameter tuning (GridSearchCV).
* 🔹 Implement **time-series backtesting** instead of simple splits.
* 🔹 Extend to **real-time signals** for trading bots.

---

## 🤝 Contribution

Feel free to fork this repo and submit pull requests!
