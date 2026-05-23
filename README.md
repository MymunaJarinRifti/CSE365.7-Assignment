# Diabetes Risk Predictor

A machine learning-based diabetes risk prediction app built with Python and scikit-learn. It uses BRFSS 2015 health indicator datasets to train classification models and predict whether a user is non-diabetic, prediabetic, or diabetic.

## Project Overview

This project loads one of three diabetes datasets, preprocesses the data, trains the best model for each dataset, evaluates performance, saves confusion matrix plots, and then accepts user health information to generate a diabetes risk prediction.

The best-performing dataset in the project is the balanced binary dataset, which achieved a macro F1-score of 0.7483 [file:28].

## Features

- Supports three datasets for classification.
- Automatically preprocesses data using one-hot encoding when needed.
- Trains and evaluates machine learning models.
- Saves confusion matrix plots as PNG files.
- Accepts manual user input for diabetes risk prediction.
- Displays prediction confidence and probability breakdown.

## Datasets Used

1. `diabetes012healthindicatorsBRFSS2015.xlsx`  
   - 3-class target.
   - Labels: Non-diabetic or pregnancy only, prediabetic, diabetic.
   - Best model: Logistic Regression.

2. `diabetesbinary5050splithealthindicatorsBRFSS2015.xlsx`  
   - Balanced binary target.
   - Labels: Non-diabetic, diabetic/prediabetic.
   - Best model: Logistic Regression.

3. `diabetesbinaryhealthindicatorsBRFSS2015.xlsx`  
   - Imbalanced binary target.
   - Labels: Non-diabetic, diabetic/prediabetic.
   - Best model: Gradient Boosting [file:28].

## Requirements

- Python 3.11+
- pandas
- numpy
- matplotlib
- scikit-learn
- openpyxl

## Installation

Clone the repository:

```bash
git clone https://github.com/MymunaJarinRifti/CSE365.7-Assignment.git
cd CSE365.7-Assignment
```

Install the required packages:

```bash
pip install pandas numpy matplotlib scikit-learn openpyxl
```

## How to Run

Make sure the Excel dataset files are in the same directory as the script, then run:

```bash
python main.py
```

If your main file has a different name, replace `main.py` with that filename.

## Input Features

The model asks for the following user inputs:

- High blood pressure
- High cholesterol
- Cholesterol checked in the last 5 years
- BMI
- Current smoker
- Had stroke
- Heart disease or attack
- Physically active
- Heavy alcohol consumption
- Has healthcare
- Could not see doctor because of cost
- General health
- Poor mental health days in last 30 days
- Poor physical health days in last 30 days
- Age category
- Sex
- Education level
- Income level

## Output

After training and prediction, the program prints:

- Dataset name
- Model type
- Accuracy
- Macro F1-score
- Confusion matrix plot saved as PNG
- Diabetes risk prediction
- Confidence percentage
- Probability breakdown [file:28].

## Generated Files

The program saves confusion matrix plots such as:

- `diabetes012healthindicatorsBRFSS2015LogisticRegressionconfusionmatrix.png`
- `diabetesbinary5050splithealthindicatorsBRFSS2015LogisticRegressionconfusionmatrix.png`
- `diabetesbinaryhealthindicatorsBRFSS2015GradientBoostingconfusionmatrix.png` [file:28].

## Results Summary

- `diabetes012healthindicatorsBRFSS2015.xlsx` → Accuracy: 64.44, Macro F1: 0.4263.
- `diabetesbinary5050splithealthindicatorsBRFSS2015.xlsx` → Accuracy: 74.84, Macro F1: 0.7483.
- `diabetesbinaryhealthindicatorsBRFSS2015.xlsx` → Accuracy: 86.51, Macro F1: 0.5908 [file:28].

## Notes

- The balanced binary dataset performed best based on macro F1-score.
- Class balancing was used to handle imbalance in the binary classification setup.
- The project is ready for report, thesis, or assignment submission [file:28].

## Author

Mymuna Jarin Rifti
