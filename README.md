# ESG-Sentiment-and-market-dynamics

This research project explores how **Environmental, Social, and Governance (ESG)** sentiment expressed on **Twitter** and **Reddit** impacts **retail trading activity**.  

We analyze social media sentiment trends, correlate them with trading volumes, and apply advanced forecasting models to predict ESG sentiment shifts over time.

---

## Project Objectives

- Analyze social media discussions around ESG topics.  
- Quantify weekly ESG sentiment using NLP-based sentiment models.  
- Examine how sentiment trends correlate with retail trading volumes.  
- Develop forecasting models to predict sentiment evolution and market impact.

---

## Datasets Used

| Dataset | Source | Description | Size |
|----------|--------|-------------|------|
| **Twitter ESG Sentiment** | Twitter API | Tweets containing ESG-related hashtags like `#ESG`, `#Sustainability`, `#ClimateChange` | ~250 MB |
| **Reddit ESG Discussions** | Reddit API (`r/stocks`, `r/investing`, `r/ESGInvesting`) | User discussions on ESG-related topics | ~180 MB |
| **Retail Trading Volume** | Yahoo Finance / NASDAQ | Historical trading volume data for retail-traded ESG stocks | ~50 MB |

---

## Evaluation Metrics

**Mean Squared Error (MSE)** is used for performance comparison.  
Since the task is regression-based sentiment forecasting, MSE effectively measures the deviation between predicted and actual sentiment values.

---

## Key Insights 

- Social media sentiment toward ESG topics shows measurable correlation with trading volume in ESG-related stocks.  
- Positive ESG sentiment often precedes increases in retail trading activity.  
- Forecasting models can capture weekly sentiment shifts, offering potential signals for retail investors.

---

## Tech Stack

- **Python 3.10+**
- **Libraries:**
  - `pandas`, `numpy`, `matplotlib`, `seaborn`
  - `tweepy`, `praw`, `yfinance`
  - `nltk`, `transformers`, `torch`, `vaderSentiment`
  - `statsmodels`, `prophet`, `scikit-learn`

