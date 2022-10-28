# Phase 3 Project

Author: Magali Solimano

Date: September 2022

## Project Overview

The Phase 3 Project applies machine learning modeling to classify borrowers' creditworthiness.

## Business Problem

A German bank has been struggling to correctly identify creditworthy borrowers. As a results, it is foregoing business opportunities to extend credit to good borrowers. It is also experiencing increasing credit losses from non-performing loans made to uncrediworthy borrowers.

Goal: The bank has commissioned the development of a machine learning model that is trained to assess and predict the credit risk of borrowers (ie, identify which borrowers are creditworthy and which borrowers are not creditworthy.)

## The Data

The project uses the German Credit dataset, sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/South+German+Credit) and which can be found in  `german_credit.csv` in the data folder in this repo. The description of the column names can be found in the repo's Jupyter Notebook. The dataset has 1,000 records and 21 variables with continuous and categorical data.

## Methods
The analysis utilizes descriptive data analysis and descriptive statistics, in addition to machine learning modeling.

## Results
The selected random forest with balanced class weights model predicts 81% of true creditworthy classifications. Compared to the baseline model, it also sharply reduced false positives (from 75% to 33%) and false negatives (from 32% to 19%). The model's precision score is 85% and f1-score is 83%.

![cm_rf](./images/cm_rf.png)

The model determines the most important features to be related to checking account balance, amount of credit, duration of credit, age of borrower, and prior credit history.

![feature_importance](./images/feature_importance.png)

## Recommendations
The selected model indicates that the bank should make loans to borrowers who have:
- some balance in their account
- paid back credits on time
- other existing credits outstanding

The bank should also make loans that have:
- average balance of $3000
- average duration of 19 months

## Next Steps
Further analysis should seek to evaluate model performance against bank's existing, traditional credit risk assessment tools and processes. It should also seek to reduce model bias.  

## More Information
See the full analysis in the [Jupyter Notebook](https://github.com/magalisolimano/classification-of-credit/blob/master/notebook.ipynb) or review the [presentation](https://github.com/magalisolimano/classification-of-credit/blob/master/presentation_phase3.pdf). For additional information, contact Magali Solimano at magali.solimano@gmail.com.


## Repository Structure
```
├── data
├── images
├── README.md
├── notebook.ipynb
└── presentation_phase3.pdf
```
