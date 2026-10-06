# Financial News Sentiment vs NIFTY50 Analysis

## Project Overview
This project explores the relationship between financial news sentiment and NIFTY50 market direction using real-world datasets. The goal is to investigate whether information extracted from financial news headlines can provide useful signals about short-term stock market movement.

### Key Components
* 3,000+ financial news articles
* NIFTY50 stock market dataset
* Rule-based sentiment analysis
* Data preprocessing and feature engineering
* Exploratory Data Analysis (EDA)
* Simple prediction logic

**Tech Stack:** Python, Pandas, Matplotlib, and JupyterLab.

---

## Problem Statement
Financial markets are heavily influenced by information flow, investor psychology, and public sentiment. This project attempts to answer the following question:

> **Can financial news sentiment help explain or predict NIFTY50 market movement?**

Rather than using complex neural networks or pretrained sentiment engines, this project uses a transparent, rule-based approach to build a complete end-to-end data processing workflow.

---

## Objectives
* **Clean and Preprocess:** Handle real-world financial text and market time-series datasets.
* **Align Data:** Synchronize stock market sessions with financial news headlines by date.
* **Sentiment Scoring:** Create a custom dictionary-based sentiment scoring system using domain vocabulary.
* **Analyze and Visualize:** Explore relationships between sentiment scores and price movements using structured plots.
* **Predict:** Build and evaluate a basic sentiment-driven prediction baseline.

---

## Dataset Description

### 1. Financial News Dataset
* **Volume:** 3,000+ financial news headlines (multiple headlines per day)
* **Coverage Period:** February 2025 – August 2025
* **Features:** Date, News title / headline text

### 2. NIFTY50 Stock Dataset
* **Coverage Period:** February 2025 – August 2025
* **Features:** Date, Open, High, Low, Close, Shares Traded, Turnover

---

## Repository Structure

├── data/
│   ├── news.csv                     # Raw financial news headlines
│   ├── nifty50.csv                  # Nifty 50 historical price data
│   └── final_project_dataset.csv    # Merged & feature-engineered dataset
├── plots/
│   ├── histogram.png                # Distribution of sentiment scores
│   ├── barplot.png                  # Sentiment vs Market Direction
│   ├── scatterplot.png              # Sentiment vs Intraday Movement
│   └── confusion_matrix.png         # Model confusion matrix
├── notebooks/
│   └── sentiment_analysis.ipynb     # Main execution notebook
└── README.md                        # Project documentation

---

## Project Workflow

Raw Financial News Dataset  +  Raw NIFTY50 Dataset
                        ↓
                  Data Cleaning
                        ↓
              Date Standardization
                        ↓
             News Grouping by Date
                        ↓
                 Dataset Merging
                        ↓
               Feature Engineering
                        ↓
         Rule-Based Sentiment Scoring
                        ↓
           Exploratory Data Analysis
                        ↓
                 Prediction Logic
                        ↓
              Performance Evaluation

---

## Methodology and Results

### 1. Sentiment Score Formulation
Scores are calculated using exact string matching against a domain-specific financial vocabulary:

Sentiment Score = Sum(Count(Positive Terms)) - Sum(Count(Negative Terms))

### 2. Empirical Findings
* **Average Sentiment (Up Days):** +21.63
* **Average Sentiment (Down Days):** +14.81
* **Part A Rule-Based Accuracy:** 59.85% (vs. 53.85% Majority-Class Baseline)
* **Part B Machine Learning Accuracy:** 50.00% (Logistic Regression) vs. 30.77% (Tuned Random Forest)

---

## License
This project is open-source and available under the MIT License.