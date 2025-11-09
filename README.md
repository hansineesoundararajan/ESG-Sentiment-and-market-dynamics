# ESG-Sentiment-and-market-dynamics
Exploring how ESG sentiment on Twitter and Reddit influences retail trading activity — combining NLP, sentiment analysis, and financial data forecasting.

# ESG Sentiment and Retail Trading Volume

This project investigates how **Environmental, Social, and Governance (ESG)** sentiment expressed on **social media** platforms like Twitter and Reddit impacts **retail trading activity** in ESG-related stocks.

We combine **Natural Language Processing (NLP)** for sentiment extraction with **financial time-series analysis** to explore the interaction between public sentiment and retail market behavior.

---

## Project Objectives

1. **Analyze** social media discussions around ESG-related topics.  
2. **Quantify** weekly ESG sentiment using NLP-based sentiment scoring models.  
3. **Correlate** sentiment trends with retail trading volume data.  
4. **Forecast** future ESG sentiment shifts using time-series and deep learning models.  

---

## Datasets Used

| Dataset | Source | Description | Size |
|----------|--------|--------------|------|
| **Twitter ESG Sentiment** | Twitter API | Tweets containing ESG-related hashtags such as `#ESG`, `#Sustainability`, `#ClimateChange`, etc. | ~250 MB |
| **Reddit ESG Discussions** | Reddit API (`r/stocks`, `r/investing`, `r/ESGInvesting`) | User discussions and comments on ESG investing and related trends. | ~180 MB |
| **Retail Trading Volume** | Yahoo Finance / NASDAQ | Historical daily/weekly trading volume data for retail-traded ESG-focused stocks. | ~50 MB |

---

## Methodology

### 1. **Data Collection**
- Extract tweets using the **Twitter API v2** with ESG-related keywords.
- Scrape Reddit posts and comments from relevant subreddits using **PRAW**.
- Fetch historical trading data from **Yahoo Finance API**.

### 2. **Data Preprocessing**
- Clean text (remove URLs, mentions, emojis, and non-ASCII).
- Tokenize and lemmatize words.
- Filter English text and remove spam/reposts.
- Merge by week for time-based sentiment aggregation.

### 3. **Sentiment Analysis**
- Apply **VADER**, **RoBERTa**, and **FinBERT** models to compute ESG sentiment scores.
- Aggregate sentiment by **week** and **platform** (Twitter, Reddit).

### 4. **Correlation & Causality Analysis**
- Compute **Pearson** and **Spearman** correlations between sentiment and trading volume.
- Perform **Granger causality tests** to check predictive influence of sentiment.

### 5. **Forecasting ESG Sentiment**
- Build forecasting models:
  - ARIMA / SARIMA
  - LSTM / BiLSTM networks
  - Prophet (for explainable seasonal trends)
- Evaluate performance using **Mean Squared Error (MSE)**.

---

## Evaluation Metrics

| Metric | Description |
|---------|--------------|
| **Mean Squared Error (MSE)** | Measures deviation between predicted and actual sentiment values — suitable for continuous regression-based forecasting. |

---

## Tech Stack

- **Python 3.10+**
- **Libraries**
  - `pandas`, `numpy`, `matplotlib`, `seaborn`
  - `tweepy`, `praw`, `yfinance`
  - `transformers`, `torch`, `nltk`, `vaderSentiment`
  - `statsmodels`, `prophet`, `scikit-learn`

---

## Results & Insights

- ESG discussions on Twitter tend to **lead** Reddit sentiment shifts by a few days.  
- **Positive ESG sentiment** correlates with **higher retail trading volume** in ESG ETFs and sustainability-focused companies.  
- Sentiment spikes often precede **short-term trading surges**, suggesting social sentiment has **predictive power** for market activity.

---

## Future Work

- Expand sentiment sources to include **news articles** and **financial reports**.  
- Integrate **topic modeling (LDA/BERT)** to analyze subthemes (e.g., climate tech, governance).  
- Use **multimodal learning** combining text sentiment and financial indicators.  
- Deploy a **real-time ESG sentiment dashboard** with live API feeds.

---

## 📊 Repository Structure

