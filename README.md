# 📊 Trader Performance vs Market Sentiment Analysis

## 👩‍💻 Candidate: Shahid Mansuri 
Role: Data Science / Analytics Intern – Round 0 Assignment  
Company: Primetrade.ai  

---

# 🎯 Objective

The objective of this project is to analyze how Bitcoin market sentiment (Fear vs Greed) impacts trader behavior and performance on Hyperliquid.

The goal is to identify behavioral patterns and generate actionable trading insights based on sentiment regimes.

---

# 📁 Datasets Used

## 1️⃣ Bitcoin Market Sentiment Data
- Columns: Date, Classification (Fear / Greed)
- Link to download dataset :  https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing

## 2️⃣ Historical Trader Data (Hyperliquid)
- Account  
- Coin  
- Execution Price  
- Size Tokens  
- Size USD  
- Side (BUY/SELL)  
- Timestamp IST  
- Closed PnL  
- Fee and more.
- Link to download the datasets: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

⚠ Note: The dataset did not contain a leverage column.  
Therefore, **Size USD was used as a proxy for risk exposure.**

---

# 🧹 Part A — Data Preparation

### ✔ Data Cleaning Steps
- Loaded both datasets using pandas
- Checked number of rows and columns
- Checked missing values and duplicates
- Converted Timestamp IST to datetime format
- Extracted daily Date from timestamp
- Merged trader data with sentiment data on Date

### ✔ Key Metrics Created
- Daily PnL per trader
- Win rate per trader
- Average trade size (Size USD)
- Trade size distribution (risk proxy)
- Trades per day
- Long/Short ratio

---

# 📈 Part B — Analysis

## 1️⃣ Performance: Fear vs Greed

Compared:
- Average Closed PnL
- Win rate
- Trade frequency

### 🔎 Finding:
Trader profitability and behavior vary across Fear and Greed market regimes.

---

## 2️⃣ Behavioral Changes by Sentiment

Observed differences in:
- Trade frequency
- Risk exposure (Size USD)
- Long/Short bias
- Position sizing

---

## 3️⃣ Trader Segmentation

Created 3 behavioral segments:

### 🔹 High Risk vs Low Risk Traders  
(Based on median Size USD)

High risk traders showed larger PnL swings, especially during Fear days.

### 🔹 Frequent vs Infrequent Traders  
Frequent traders performed better during Greed periods but showed overtrading tendencies during Fear periods.

### 🔹 Consistent Winners vs Inconsistent Traders  
Consistent winners maintained positive average PnL across sentiment regimes.

---

# 💡 Key Insights

### ✅ Insight 1  
Average PnL is generally higher during Greed days compared to Fear days.

### ✅ Insight 2  
High risk traders (large Size USD) experience higher volatility and larger drawdowns during Fear periods.

### ✅ Insight 3  
Frequent traders increase activity during Greed days, improving profitability.

---

# 🚀 Part C — Strategy Recommendations

## 📌 Strategy Rule 1  
During Fear days:
- Reduce position size (Size USD)
- Avoid overtrading
- Focus on risk management

## 📌 Strategy Rule 2  
During Greed days:
- Allow moderate increase in position size
- Enable higher trade frequency for consistent winners

---

# 🤖 (Optional) Predictive Model

A simple Random Forest model was built to:
- Predict trade profitability bucket  

Using:
- Trade Size (Size USD)
- Sentiment classification

This demonstrates the potential of sentiment-aware trading strategies.

---

# 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# 📊 Conclusion

Market sentiment significantly influences trader performance and behavior.  

Incorporating sentiment-based risk management and position sizing strategies can improve trading outcomes and reduce losses during volatile periods.

---

# ▶ How to Run

1. Install required libraries:
   
   pip install pandas numpy matplotlib seaborn scikit-learn
   

2. Open the notebook:
   
   Trader_Sentiment_Analysis.ipynb
   

3. Run all cells sequentially.

---

# 📌 Repository Structure

- Trader_Sentiment_Analysis.ipynb  
- README.md (contains datasets link)

---
