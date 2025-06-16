# 🏆 Game of the Year (GOTY) Candidate Prediction Model

This project leverages machine learning to predict Game of the Year (GOTY) nominations for video games on the Steam platform. Using data wrangling, web scraping, feature engineering, and robust modeling, the workflow demonstrates how data science can uncover the factors that drive critical acclaim in the gaming industry.

Developed for the Analytics & Discovery Informatics practicum (Fall 2024), this project combines detailed data collection with advanced predictive methods to analyze and forecast GOTY nomination candidates.

---

## 📌 Problem Statement

Predicting which games will earn a GOTY nomination is complex, as it depends on a mix of game characteristics, player engagement, and critical reception. This project aims to build a supervised learning model that classifies Steam games as potential GOTY nominees, using features such as genre, player statistics, reviews, release information, and more.

---

## 🗃️ Data Collection & Processing

- **Sources:**  
  - [Steam API](https://partner.steamgames.com/doc/webapi_overview): Real-time game details, reviews, pricing, release dates  
  - [SteamSpy](https://steamspy.com/): Aggregated player engagement and ownership metrics  
  - Manual labeling from [The Game Awards](https://thegameawards.com/) for GOTY candidate status

- **Wrangling & Cleaning:**  
  - Combined, deduplicated, and filtered to focus on high-engagement games (owners, playtime, reviews)
  - Imputed missing values, translated non-English tags, normalized numerical/categorical features
  - Engineered new features (e.g., one-hot encoded genres/seasons, averaged owner ranges, consolidated multiplayer columns)

- **Target:**  
  - Binary label: 1 = GOTY candidate, 0 = non-candidate  
  - Created via manual mapping of Game Awards nominee AppIDs

---

## 🧠 Modeling Approach

- **Feature Engineering:**  
  - Game genre (one-hot), release date (season/year), player engagement stats, review scores, price, multiplayer, etc.

- **Models:**  
  - Logistic Regression and Decision Trees (baseline)  
  - Random Forest and Gradient Boosting (advanced)  
  - GridSearchCV for hyperparameter tuning  
  - Threshold adjustment to optimize F1-score  
  - Evaluation: AUC-ROC, Precision, Recall, F1

- **Results:**  
  - **Random Forest:** Highest recall (1.00), F1-score 0.80  
  - **Gradient Boosting/Decision Tree:** F1-score 0.727, balanced precision/recall  
  - Threshold adjustment improved recall/precision trade-off  
  - Feature importance analysis highlights impact of engagement, reviews, genre, and release timing

---

## 📊 Key Insights

- High engagement (owners, playtime, reviews) is strongly predictive of GOTY nomination
- Genre and release timing (season/year) influence nomination likelihood
- Data cleaning, imputation, and focused filtering are critical for model accuracy

---

## 📁 Project Structure

```
goty-candidate-prediction/
├── data/         # Sample datasets, processed data, data dictionary
│   └── README.md
├── models/       # Trained model artifacts or configs (not included)
│   └── README.md
├── notebook/     # Jupyter notebook: EDA, modeling pipeline, results
│   └── goty_prediction.ipynb
├── reports/      # PDF report, presentation slides, visualizations
│   ├── goty_report.pdf
│   └── goty_presentation.pdf
├── images/       # Plots and figures for results and the README
│   └── (e.g., feature_importance.png)
├── src/          # Data wrangling, scraping, and feature engineering scripts
│   └── README.md
├── requirements.txt  # Python dependencies (optional, for reproducibility)
├── .gitignore
└── README.md     # Project overview, usage, and instructions
```

---

## 📥 Data Availability

Due to API and aggregation rate limits, as well as size constraints, **full datasets are not uploaded**. Sample/processed data structures and code are provided for reference. Data can be recreated using the code and instructions in `notebook/` and `src/`.

---

## 📄 Reproducibility

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/goty-candidate-prediction.git
   ```
2. (Optional) Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
3. Explore the Jupyter notebook for the full analysis and modeling pipeline.

---

## 📫 Contact

For questions, collaborations, or feedback:  
[syed.hashim.raza@email.com]  
[LinkedIn](https://www.linkedin.com/in/your-linkedin/)

---

## ⚖️ License

To be specified. Intended for academic and portfolio purposes.

---
