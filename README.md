# Spotify-Premium-Subscription-Behavior-Modeling-and-Driver-Analysis

# Spotify Premium Adoption Modeling Using Logistic Regression & Behavioral EDA

This project investigates user-behavior drivers behind Spotify Premium adoption, with a focus on behavioral variables such as age segments, listening device types, and podcast satisfaction metrics. The analysis combines exploratory data analysis (EDA) and logistic regression to identify statistically meaningful predictors of subscription willingness.

## 🎯 Objective
Identify the most influential user-level factors associated with intention to upgrade from free to Premium on Spotify.

## 📁 Data Source
Survey-based Spotify behavior dataset (Kaggle).  
Contains demographic, usage, preference, and satisfaction fields.

### Key Variables
| Variable | Type | Description |
|---------|------|-------------|
| premium_sub_willingness_dummy | Binary | Target variable (0 = No, 1 = Yes) |
| age_group | Categorical | Age brackets (6-12, 12-20, 20-35, 35-60, 60+) |
| spotify_listening_device | Categorical | Device used to access Spotify |
| pod_variety_satisfaction | Likert (0-5) | Self-reported satisfaction with podcast variety |

> Dataset is **observational**, not experimental — results reflect associations, not causation.

---

## 🧠 Methodology
✔ Exploratory Data Analysis (EDA)  
✔ Dummy variable encoding for categorical features  
✔ Logistic Regression (one-variable models per hypothesis)  
✔ Interpretation using coefficients, p-values & pseudo R²  

### Why logistic regression?
Target variable is binary (subscribe or not), and logistic regression ensures predicted probabilities remain between 0 and 1.

---

## 🧪 Models Tested

| Hypothesis | Feature | Result |
|-----------|--------|-------|
| Age influences willingness to subscribe | age_group | Low predictive power (Pseudo R² ≈ 0.01) |
| Device usage influences subscription | device type | Low predictive power (Pseudo R² < 0.01) |
| Podcast variety satisfaction influences subscription | pod satisfaction | **Moderate predictive power (Pseudo R² ≈ 0.178)** ✅ |

### Key Result
Users with **higher podcast satisfaction** are significantly more likely to consider Spotify Premium.  
Age & device have negligible predictive value in this dataset.

---

## 📊 Insights
- Younger & mid-age segments (12-35) show stronger premium intent
- Short-form podcast listeners and low-frequency podcast users exhibited higher upgrade interest
- Signals suggest users prefer **high-quality, concise content** and may pay for it

---

## 📈 Business Implications
| Strategy | Rationale |
|--------|-----------|
Exclusive short-form premium podcast content | Matches behavior of high-intent users |
Student & young adult targeting | Core conversion demographic (12-35) |
“Podcast-first” upgrade path | Bundle premium podcast access as incentive |

---

## 📂 Project Structure
