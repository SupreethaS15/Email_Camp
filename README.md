# Email_Camp
# 📧 Email Campaign Optimizer

This project analyzes the performance of an email marketing campaign and applies machine learning to predict and optimize click-through rate (CTR). The dataset comes from a real-world case study where users were sent marketing emails, and their engagement was tracked.

## 🎯 Objectives

- Calculate open rate and click rate
- Build a classification model to predict user clicks
- Tune prediction thresholds to simulate uplift in CTR
- Perform data-driven segmentation analysis
- Visualize key behavior patterns across user and email attributes

## 🧠 Machine Learning Workflow

### 1. **Data Preparation**
- Load and merge three datasets:
  - `email_table.csv`: Email metadata
  - `email_opened_table.csv`: Opened email IDs
  - `link_clicked_table.csv`: Clicked email IDs
- Created target variables `opened` and `clicked`

### 2. **Feature Engineering**
- One-hot encoding for categorical features:
  - `email_text`, `email_version`, `weekday`, `user_country`
- Cyclic encoding of `hour` as sine and cosine

### 3. **Modeling**
- Trained:
  - **Logistic Regression** as baseline
  - **Random Forest Classifier** as main model
- Evaluated using:
  - Classification report (Precision, Recall, F1-score)
  - ROC-AUC score

### 4. **Threshold Tuning & Uplift Simulation**
- Tested various probability thresholds (0.0–1.0)
- Simulated CTR if emails were sent only above each threshold
- Identified optimal threshold for best CTR lift

### 5. **Segmentation Insights**
Visualizations included:
- 📬 CTR by email version (personalized/generic)
- 📅 Behavior over weekday
- 🕐 Click patterns by hour of send
- 🌍 CTR by top countries
- ✍️ CTR by combinations of text length & personalization
- 💸 User purchase history vs engagement


## 🖥️ Requirements
install pandas numpy matplotlib seaborn scikit-learn shap
