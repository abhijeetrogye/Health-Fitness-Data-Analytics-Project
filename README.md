# 📊 Health & Fitness Data Analytics Project

A complete **end-to-end Data Analytics project** using Python — from raw data to actionable insights and machine learning predictions.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-3776AB)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 🎯 Project Overview

This project analyzes a **Health & Fitness dataset** containing data from **3,000 users** tracked over **30 days** — combining Google Fit activity data with medical health records.

The goal is to uncover patterns in health metrics, identify key risk factors for cardiometabolic disease, and provide data-driven recommendations.

---

## 📁 Dataset Description

| Feature | Details |
|---------|---------|
| **Records** | 90,000 daily records |
| **Users** | 3,000 unique users |
| **Time Period** | 30 days (Jan 2024) |
| **Columns** | 37 features |
| **Source** | Hamon Google Fit Medical Realistic Dataset |

### Key Columns

| Category | Columns |
|----------|---------|
| **Demographics** | `user_id`, `age`, `sex`, `bmi`, `height_m`, `weight_kg` |
| **Lifestyle** | `smoking_status`, `family_history_cvd`, `fitness_level` |
| **Activity** | `steps`, `heart_points`, `move_minutes`, `calories_burned`, `distance_km`, `activity_type` |
| **Heart Health** | `avg_heart_rate`, `resting_hr`, `hrv`, `bp_systolic`, `bp_diastolic` |
| **Medical** | `fasting_glucose`, `postprandial_glucose`, `spo2`, `body_temp_c` |
| **Sleep** | `sleep_hours`, `sleep_efficiency` |
| **Nutrition** | `calories_consumed`, `water_intake_l` |
| **Target** | `cardiometabolic_risk_state` (0=Very Low → 4=Very High) |

---

## 🛠️ Project Pipeline

```
📥 Data Loading → 🧹 Data Cleaning → 🔍 EDA → 💡 Insights → ✅ Recommendations → 🎁 Bonus (ML)
```

### 1️⃣ Data Loading & Preview
- Import libraries (Pandas, NumPy, Matplotlib, Seaborn)
- Load CSV and preview with `head()`, `tail()`, `shape`, `info()`, `describe()`
- Full column glossary with plain-English explanations

### 2️⃣ Data Cleaning
- ✅ **Missing values** — Verified as intentional (BP, glucose, sleep measured on select days)
- ✅ **Duplicates** — None found
- ✅ **Data types** — Converted date column to datetime; extracted day_of_week, week_number
- ✅ **Outliers** — Detected via IQR method & box plots; all within biological ranges
- ✅ **Column renaming** — 7 columns renamed for clarity

### 3️⃣ Exploratory Data Analysis (EDA)

#### Univariate Analysis
- Age distribution (histogram + pie chart by age group)
- Activity type frequency
- Steps, calories burned, sleep hours distributions
- Heart rate & BMI distributions with health reference lines
- Cardiometabolic risk state distribution

#### Bivariate Analysis
- Activity type vs steps, calories, heart rate, risk
- Age group vs health metrics
- Smoking, family history, gender vs risk level
- Steps vs calories (scatter plots colored by activity & risk)

#### Correlation Analysis
- Full correlation heatmap (16 variables)
- Risk factor ranking chart
- 30-day time trends
- Day-of-week activity patterns
- Fitness level deep dive

### 4️⃣ Insights & Conclusions

| Finding | Detail |
|---------|--------|
| 🏋️ **Fitness is #1 protector** | Higher fitness level = significantly lower health risk at every age |
| 🚬 **Smoking raises risk** | Smokers have consistently higher cardiometabolic risk |
| 👴 **Age increases risk** | Older adults (60+) have the highest average risk scores |
| 🧬 **Family history matters** | CVD family history elevates risk (non-modifiable factor) |
| 😴 **Sleep impacts health** | Sleep quality and duration vary significantly across users |

### 5️⃣ Recommendations

| # | Recommendation | Impact |
|---|---------------|--------|
| 1 | Launch targeted fitness programs for low-fitness users | ⭐⭐⭐⭐⭐ |
| 2 | Implement smoking cessation programs | ⭐⭐⭐⭐⭐ |
| 3 | Create age-specific health plans | ⭐⭐⭐⭐ |
| 4 | Send daily step goal reminders | ⭐⭐⭐ |
| 5 | Monitor users with family CVD history more closely | ⭐⭐⭐⭐ |
| 6 | Promote sleep hygiene awareness | ⭐⭐⭐ |
| 7 | Encourage varied exercise activities | ⭐⭐⭐ |
| 8 | Alert high-risk users for medical consultation | ⭐⭐⭐⭐⭐ |

### 6️⃣ Bonus
- **Feature Engineering** — 7 new features (calorie balance, BMI category, step goal achievement, HR zone, active day flag, sleep quality, hydration status)
- **Predictive Modeling** — Random Forest classifier to predict cardiometabolic risk with feature importance analysis and confusion matrix

---

## 📈 Sample Visualizations

The notebook contains **20+ professional visualizations** including:

- 📊 Histograms & Distribution plots
- 📦 Box plots for outlier detection
- 🔥 Correlation heatmaps
- 📉 Scatter plots with color coding
- 📅 Time-series trend lines
- 🍩 Donut & pie charts
- 📊 Grouped bar charts with annotations

---

## 🚀 How to Run

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Run the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/abhijeetrogye/Health-Fitness-Data-Analytics-Project.git
   cd Health-Fitness-Data-Analytics-Project
   ```

2. Open the notebook:
   ```bash
   jupyter notebook data_analytics_project.ipynb
   ```

3. Run all cells: `Kernel` → `Restart & Run All`

---

## 📂 Project Structure

```
📦 Health-Fitness-Data-Analytics-Project
├── 📓 data_analytics_project.ipynb    # Main notebook (75 cells)
├── 📊 hamon_googlefit_medical_realistic.csv  # Dataset (90K records)
├── 📄 data_summary.txt               # Dataset summary statistics
├── 📄 .gitignore                      # Git ignore rules
└── 📄 README.md                       # This file
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3.x** | Core programming language |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical computations |
| **Matplotlib** | Base visualization library |
| **Seaborn** | Statistical data visualization |
| **Scikit-learn** | Machine learning (Random Forest) |
| **Jupyter Notebook** | Interactive development environment |

---

## 🔑 Key Takeaway

> *"Your health risk is largely determined by modifiable factors like fitness level and smoking status — not just age or genetics. Regular exercise and avoiding smoking are the two most impactful things you can do for your cardiometabolic health."*

---

## 👥 Contributors

| # | Name | LinkedIn |
|---|------|----------|
| 1 | **Abhijeet Rogye** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhijeetrogye/) |
| 2 | **Arya Kurup** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/arya-kurup-aa7264244/) |
| 3 | **Viraj Tamhanekar** | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/viraj-tamhanekar/) |

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project useful, please give it a star!**
