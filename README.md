# Gold Price Prediction — NLP Sentiment & Algorithmic Trading Strategy

Can news sentiment predict gold prices? This project combines 10 years of gold price data with 10,570 financial news headlines to build predictive models and a backtested algorithmic trading strategy.

---

## Key Results

- **Models tested:** OLS Regression, Random Forest, AdaBoost
- **Finding:** Negative R² across all models interpreted as empirical support for the Efficient Market Hypothesis (EMH) — gold prices are not predictable from sentiment alone
- **Trading strategy:** Backtested a sentiment-driven strategy with transaction fees, evaluating real-world P&L performance

---

## Tech Stack

- **Language:** Python
- **NLP:** TextBlob, VADER
- **ML:** scikit-learn (Random Forest, AdaBoost), statsmodels (OLS)
- **Data:** pandas, numpy
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

---

## Project Structure

```
gold-price-nlp-prediction/
├── README.md
├── requirements.txt
├── data/
│   ├── gold_prices.csv
│   └── gold_news_headlines.csv
├── notebooks/
│   └── gold_price_prediction.ipynb
└── results/
    ├── model_comparison.png
    └── trading_backtest.png
```

---

## NLP Features Engineered

| Feature | Description |
|---|---|
| Sentiment Polarity | How positive or negative each headline is (-1 to +1) |
| Sentiment Subjectivity | Opinion-based vs factual language (0 to 1) |
| Forward-looking Orientation | Whether headline references future vs past price movement |

---

## Models Compared

| Model | Test R² | Notes |
|---|---|---|
| OLS Regression | Negative | Baseline linear model |
| Random Forest | Negative | Ensemble, hyperparameter tuned |
| AdaBoost | Negative | Boosting approach |

All models produced negative R², consistent with gold market efficiency.

---

## How to Run

1. Clone the repo
   ```bash
   git clone https://github.com/hydec5ive/gold-price-nlp-prediction
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook
   ```bash
   jupyter notebook notebooks/gold_price_prediction.ipynb
   ```

---

## Dataset

- **Gold prices:** GC:CMX historical data — 2,559 trading days (Aug 2011 – Aug 2021)
- **News headlines:** 10,570 gold-related financial news headlines with dates

---

## Key Takeaway

The failure of all models to achieve positive R² is itself a meaningful finding — it empirically supports the Efficient Market Hypothesis, suggesting that publicly available news sentiment is already priced into gold markets by the time it is published.

---

## Course

FINA 4390 — Applied Machine Learning in Finance  
Northeastern University, D'Amore-McKim School of Business
