# SWYNEX-Exploratory-Data-Analysis

Task 2 of the SWYNEX Technologies Data Science internship: perform exploratory data analysis (EDA) on the cleaned Titanic dataset from Task 1, and report insights that could influence a model or decision.

## Dataset
`cleaned_data.csv`, the output of Task 1: 891 rows, 13 columns, 0 missing values.
Original source: Titanic passenger data, https://github.com/datasciencedojo/datasets/blob/master/titanic.csv

## Five key insights
1. **Passenger class strongly predicts survival.** 1st class: 63% survived, 2nd class: 47%, 3rd class: 24%.
2. **Sex is the strongest single predictor.** Women survived at a much higher rate than men.
3. **Young children (age 0-10) had a survival advantage** over other age groups.
4. **Family size has a "sweet spot."** Small families (2-4 members) survived more often than solo travellers or large families.
5. **Fare and cabin record correlate with survival**, but mainly because both reflect passenger class rather than being independent causes.

## What this means for modelling
`Sex`, `Pclass`, `Age`, `FamilySize` and `Fare` are the strongest candidate features for predicting survival. `Fare` and `Pclass` are correlated with each other, so a model likely doesn't need both.

## Repository contents
| File | Description |
|------|-------------|
| `eda_analysis.ipynb` | Full analysis notebook with statistics, charts and insights |
| `cleaned_data.csv` | Input data (from Task 1) |
| `insight1_class_survival.png` … `insight5_fare_cabin_survival.png` | Chart for each insight |
| `correlation_heatmap.png` | Correlation heatmap of numeric features |
| `README.md` | This file |

## How to run
```bash
git clone https://github.com/challasrinuvas/SWYNEX-Exploratory-Data-Analysis.git
cd SWYNEX-Exploratory-Data-Analysis
pip install pandas numpy matplotlib jupyter
jupyter notebook eda_analysis.ipynb
```

## Tools
Python, pandas, NumPy, Matplotlib, Jupyter Notebook

#SWYNEX #Internship #DataScience
