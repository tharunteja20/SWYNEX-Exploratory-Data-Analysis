# Task 2: Exploratory Data Analysis — Titanic Passenger Dataset

## Overview
This task performs exploratory data analysis (EDA) on the cleaned
Titanic dataset produced in Task 1 (titanic_cleaned.csv), using Python
(pandas, matplotlib, seaborn).

## Files in This Submission
- titanic_cleaned.csv — the cleaned dataset from Task 1 (carried over as the input for this analysis)
- eda_titanic.py — the full EDA script (fully reproducible)
- eda_insights.txt — auto-generated summary of the key statistics and insights
- chart1_survival_by_class.png — survival rate by passenger class
- chart2_survival_by_sex.png — survival rate by sex
- chart3_age_distribution.png — age distribution split by survival outcome
- chart4_fare_by_class.png — fare distribution by passenger class (boxplot)
- chart5_correlation_heatmap.png — correlation heatmap of numeric features
- chart6_survival_by_cabin_flag.png — survival rate for passengers with vs. without a recorded cabin
- README.md — this file

## Key Statistics Calculated
- Overall survival rate
- Survival rate broken down by passenger class, sex, and embarkation port
- Average fare by passenger class
- Average age of survivors vs. non-survivors
- Correlation matrix across Survived, Pclass, Age, SibSp, Parch, and Fare

## Five+ Key Insights

1. Class mattered a lot. Overall survival was 34.4%, but 1st class
   passengers survived at 47.8% versus only 28.0% for 3rd class —
   wealth/class was strongly tied to survival chances.

2. Sex was the single strongest predictor of survival. Women survived
   at 70.9% versus just 15.2% for men, consistent with the historical
   "women and children first" evacuation approach.

3. Younger passengers had a slight survival edge. Survivors were on
   average ~4 years younger than non-survivors (24.7 vs 29.1 years).

4. Fare tracked with class, and both tracked with survival. 1st class
   passengers paid ~73 on average versus ~15 for 3rd class, and higher
   fares were mildly positively correlated with survival — reinforcing
   the class-based survival gap.

5. Having a recorded cabin number was linked to higher survival
   (58.3% vs 28.7%), but this is best read as a proxy for higher passenger
   class rather than an independent cause, since cabin records were far
   more common on 1st/2nd class tickets.

6. The correlation heatmap confirms Pclass has the strongest negative
   correlation with Survived among the numeric features, matching the
   class-based patterns seen above rather than contradicting them.

Bottom line: survival on the Titanic was driven mainly by a
combination of sex, passenger class, and age, with fare and cabin records
acting as secondary indicators of that same underlying class effect.

## How to Reproduce
pip install pandas matplotlib seaborn
python eda_titanic.py

This regenerates all 6 charts and eda_insights.txt from titanic_cleaned.csv.
