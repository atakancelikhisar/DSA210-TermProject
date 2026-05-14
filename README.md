# Clash Royale Match Performance Analysis (DSA 210 Term Project)

## Project Overview & Motivation
This project analyzes personal Clash Royale gameplay data to identify the factors that contribute to winning. By leveraging 320 match logs retrieved via the official API, I explore whether temporal patterns (such as match hour or weekends) and deck elixir costs have a predictable impact on match outcomes. The goal is to move from intuitive play to a data-driven understanding of competitive performance.

## Key Findings & Results

### 1. Statistical Hypothesis Testing
To validate the observations made during Exploratory Data Analysis, I conducted rigorous statistical tests:
* **Weekend Performance:** An Independent T-test resulted in a **p-value of 0.5885**.
* **Hourly Trends:** A Point-Biserial correlation for match hours yielded a **p-value of 0.5913**.
* **Verdict:** Both results are statistically **insignificant** ($p > 0.05$). This proves that my win rate remains remarkably consistent across different times; the time or day I play does not fundamentally change the probability of winning.

### 2. Machine Learning Success
I implemented a **Logistic Regression** model to predict match outcomes:
* **Accuracy:** **59.38%**
* **F1-Score (Win):** **0.62**
* **Insight:** The model outperforms a random baseline (50%), suggesting that while timing is a weak predictor, it still provides some signal for match outcomes. The results suggest that in-game variables like deck synergy likely hold more predictive power.

## How to Reproduce
1.  **Install dependencies:** `pip install -r requirements.txt`
2.  **Statistical Analysis:** Run `DSA210_EDA_Hypothesis_Testing.ipynb`.
3.  **Predictive Modeling:** Run `DSA210_ML_Analysis.ipynb`.

## Limitations & Future Work
* **Limitations:** The average elixir cost was relatively constant across samples in this specific dataset, limiting its use as a predictive feature.
* **Future Work:** Future iterations will focus on incorporating opponent deck archetypes and card level differentials to improve model accuracy beyond 60%.

## AI Disclosure
Generative AI (LLM) was utilized in a limited, consultative capacity for code debugging and linguistic refinement. All core analyses, data collection, and findings remain the independent work of the author. Specific prompts and outputs are documented in the repository for transparency.
