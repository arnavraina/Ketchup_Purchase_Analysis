# Ketchup Purchase Analysis

## Overview
This repository contains the solution for an assignment that involves analyzing grocery store purchases of Heinz and Hunts ketchup using a dataset named `HeinzHunts`. The analysis includes building a logistic regression model to estimate the probability of purchasing Heinz ketchup based on various promotional and pricing factors. The assignment also explores how changes in these factors affect purchase probabilities and aims to optimize customer targeting for brand loyalty programs using cost analysis of misclassifications.

## Dataset Description
The dataset consists of the following variables, with each observation representing one purchase occasion of either Heinz or Hunts ketchup:

1. `Heinz`: Indicator variable (=1 if Heinz was purchased, =0 if Hunts was purchased).
2. `PriceHeinz`: Price of Heinz ketchup.
3. `PriceHunts`: Price of Hunts ketchup.
4. `DisplHeinz`: Indicator variable (=1 if Heinz had a store display, =0 otherwise).
5. `DisplHunts`: Indicator variable (=1 if Hunts had a store display, =0 otherwise).
6. `FeatureHeinz`: Indicator variable (=1 if Heinz was featured in-store, =0 otherwise).
7. `FeatureHunts`: Indicator variable (=1 if Hunts was featured in-store, =0 otherwise).

## Problem Statement
### Question 1: Model Estimation
- Create a new variable `LogPriceRatio = log(PriceHeinz/PriceHunts)`.
- Split the dataset into training (75%) and test (25%) samples.
- Estimate a logistic regression model to predict the probability of purchasing Heinz using the following explanatory variables: `LogPriceRatio`, `DisplHeinz`, `FeatureHeinz`, `DisplHunts`, `FeatureHunts`, and interaction terms between displays and features for each brand.
- Interpret the model's results, identifying effective promotional strategies and interaction effects for Heinz and Hunts.

### Question 2: Probability Change Calculation
- Based on the estimated model, calculate the change in the predicted probability of purchasing Heinz when the `LogPriceRatio` changes from 0.5 to 0.55, given that Heinz has no feature or display while Hunts has both a feature and display.

### Question 3: Optimal Coupon Targeting
- Develop a strategy for targeting customers with coupons for Hunts to build brand loyalty. Coupons should be sent to customers who are less likely to buy Heinz.
- Calculate the total cost of misclassification based on the following:
  - Cost of incorrectly sending a coupon to a customer who would have bought Heinz: $1.5.
  - Cost of incorrectly failing to send a coupon to a customer who would have bought Hunts: $0.25.
- Determine the optimal probability threshold to minimize the total cost of misclassification by creating an ROC table for the test data and calculating the total cost for each threshold.

## Contents
- `code/`: Contains the code for data processing, model training, and evaluation.
- `report/`: The final report detailing the results and analysis.
- `README.md`: This file providing a summary of the problem and repository structure.

## Requirements
- SAS for model estimation and ROC analysis.
- Python or R for additional data analysis (optional).

## Instructions
1. Follow the `code/` directory for scripts used in data preprocessing and model training.
2. View the `report/` directory for a detailed explanation of the results and interpretations.
3. Use the output images in the report as screenshots required by the assignment.

## Authors
- Arnav Raina
