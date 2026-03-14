# Market Sentiment vs Trader Behavior Analysis

## Setup

1. Clone or download this repository.

```bash
git clone https://github.com/KathullaYamini/market-sentiment-analysis.git
cd market-sentiment-analysis
```

2. Install the required Python libraries.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Make sure the following files are available in the project folder:
- Fear & Greed Index dataset
- Historical trading dataset
- Analysis notebook or Python script

---

## How to Run

1. Open the project in **Jupyter Notebook** or any Python environment.

2. Run the analysis script or notebook.

Example:

```bash
python sentiment_trader_analysis.py
```

or open the notebook:

```bash
jupyter notebook
```

3. Execute all cells to:
- Clean the datasets
- Merge trading and sentiment data
- Generate charts and insights
- Train the simple predictive model

---

# Project Overview

This project analyzes the relationship between **cryptocurrency market sentiment** and **trader behavior**. The goal is to understand how different sentiment conditions (Fear, Greed, etc.) influence trading activity, profitability, and trading strategies.

The analysis combines a **Fear & Greed Index dataset** with **historical trader data** to identify patterns in trader performance and behavior.

---

# Datasets Used

## 1. Fear & Greed Index Dataset
This dataset contains the daily market sentiment classification:

- Extreme Fear  
- Fear  
- Neutral  
- Greed  
- Extreme Greed  

It represents the overall psychological state of the cryptocurrency market.

## 2. Historical Trader Dataset
This dataset contains trade-level information including:

- Account ID  
- Trade direction (Long/Short)  
- Position size (USD)  
- Closed Profit/Loss (PnL)  
- Timestamp of trade  

---

# Methodology

## 1. Data Cleaning
- Converted timestamps into datetime format
- Extracted trading dates
- Prepared the datasets for analysis

## 2. Data Merging
The trading dataset was merged with the Fear & Greed dataset using the **date column** so each trade corresponds to the market sentiment of that day.

## 3. Feature Engineering
Additional features were created:

- Win indicator (Closed PnL > 0)
- Daily trade counts
- Average trade size per trader
- Trader activity segmentation

## 4. Data Analysis
The following metrics were analyzed:

- Profit/Loss distribution
- Win rate
- Trade frequency
- Average position size
- Long vs Short trading bias
- Trader segmentation

## 5. Visualization
Charts were created using **Matplotlib and Seaborn** to analyze trader behavior.

---

# Charts Used

1. PnL Distribution by Market Sentiment (Boxplot)  
2. Market Sentiment Distribution (Countplot)  
3. Number of Trades Per Day (Line Chart)  
4. Average Trader PnL by Market Sentiment (Bar Chart)  
5. Trade Frequency by Market Sentiment (Bar Chart)  
6. Average Position Size by Market Sentiment (Bar Chart)  
7. PnL Distribution by Trader Performance Type (Boxplot)

---

# Key Insights

1. Trader profitability varies across market sentiment conditions.  
Extreme Greed periods tend to generate higher average profits, while Extreme Fear periods show larger average losses.

2. Traders become more active during Fear conditions.  
Higher trade frequency suggests traders attempt to take advantage of increased market volatility.

3. Trading direction changes with sentiment.  
Long positions are more common during Fear and Neutral markets, while short positions increase during Greed periods.

4. Trading activity impacts profitability.  
Infrequent traders tend to show higher average PnL compared to frequent traders.

---

# Trader Segmentation

Two types of segmentation were performed:

## Frequent vs Infrequent Traders
Traders were classified based on their trade count relative to the median.

## Consistent vs Inconsistent Traders
Traders were classified based on win rate:

- Consistent Winner → win rate ≥ 50%  
- Inconsistent Trader → win rate < 50%

---

# Strategy Recommendations

## Strategy 1: Reduce Risk During Extreme Fear
During Extreme Fear conditions:

- Reduce position sizes
- Avoid excessive leverage
- Focus on high-confidence trades

This helps reduce downside risk during volatile markets.

## Strategy 2: Use Momentum Strategies During Greed
During Greed and Extreme Greed conditions:

- Follow strong market trends
- Increase trade activity slightly
- Identify short opportunities when markets appear overextended

This helps traders benefit from trend continuation during optimistic markets.

---

# Tools and Libraries Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn
