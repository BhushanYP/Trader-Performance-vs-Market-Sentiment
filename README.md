# Hyperliquid Trader Behavior vs Market Sentiment

## Objective
This project analyzes how Bitcoin market sentiment (Fear/Greed index) influences trader behavior and performance on Hyperliquid.

The goal is to identify patterns that can help improve trading strategies.

---

## Dataset

Two datasets were used:

1. **Bitcoin Fear & Greed Index**
   - Market sentiment indicator

2. **Hyperliquid Historical Trader Data**
   - Trade details including trader account, trade size, direction, and PnL

---

## Methodology

### 1. Data Preparation
- Loaded both datasets using pandas
- Converted timestamps to daily format
- Merged sentiment data with trader data using the date field
- Created analysis metrics:
  - Daily PnL per trader
  - Win rate
  - Trade frequency
  - Average position size
  - Long/Short ratio

### 2. Behavioral Analysis
Compared trader performance across different sentiment states:
- Fear
- Neutral
- Greed

Behavior metrics analyzed:
- Trade frequency
- Position size
- Long vs short bias

### 3. Trader Segmentation
Traders were divided into segments based on behavior:

- Frequent vs Infrequent traders
- Consistent vs Inconsistent traders (PnL volatility)

Segment performance was then compared.

---

## Key Insights

**Insight 1:**  
Trader profitability varies with market sentiment.  
Charts show differences in average PnL and win rate between Fear and Greed periods.

**Insight 2:**  
Trader behavior changes depending on sentiment conditions.  
Trade frequency and position sizes vary across Fear, Neutral, and Greed periods.

**Insight 3:**  
Different trader segments show different performance patterns.  
Frequent and consistent traders generally display more stable performance compared with less active traders.

---

## Strategy Ideas

**Strategy 1 — Sentiment-Based Risk Control**

During Fear periods:
- Look for potential long opportunities
- Maintain moderate position sizing

During Greed periods:
- Reduce position size
- Avoid excessive trading due to increased market risk.

---

**Strategy 2 — Segment-Based Trading**

Frequent and consistent traders may maintain active strategies.

Infrequent or inconsistent traders should:
- reduce trade frequency
- apply stricter risk management.

---

## How to Run

1. Clone the repository
git clone https://github.com/yourusername/hyperliquid-sentiment-analysis.git


2. Install dependencies
pip install -r requirements.txt


3. Open the notebook
jupyter notebook

4. Run:
notebooks/sentiment_trader_analysis.ipynb

---

## Outputs

The notebook generates charts including:

- Average PnL vs Sentiment
- Win Rate vs Sentiment
- Trade Frequency vs Sentiment
- Long vs Short Bias
- Trader Segment Performance

---

## Methodology

The analysis combined Bitcoin Fear & Greed sentiment data with Hyperliquid trading data. After cleaning and aligning timestamps, key metrics such as trader PnL, win rate, trade frequency, and position sizes were calculated. Traders were then segmented into behavioral groups to examine differences in performance.

## Insights

The results show that trader profitability varies across sentiment states, indicating that market psychology affects trading outcomes. Behavioral analysis also shows that traders adjust activity levels and position sizes depending on sentiment. Finally, segmentation analysis reveals that frequent and consistent traders demonstrate more stable performance compared with less active or inconsistent traders.

## Strategy Recommendations

Two simple strategies emerge from the analysis. First, sentiment-based risk management can help traders reduce exposure during greed-driven markets and cautiously increase participation during fear periods. Second, trader segmentation suggests that more active traders may benefit from maintaining consistent strategies, while less active traders should focus on fewer trades and stronger risk controls.
