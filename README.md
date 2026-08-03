# Titanic Data Cleaning — Week 1

## Objective
Load and clean the Titanic dataset using pandas as part of Week 1 of the EDP AI/ML Project Plan. This task focuses on understanding raw data, handling missing values, and learning the difference between features and labels.

## Dataset
Titanic dataset — 891 rows, 12 columns — containing passenger details and survival outcomes from the Titanic disaster.

## Steps Performed
- Inspected the dataset using `.info()`, `.describe()`, and `.isnull().sum()`
- Filled missing `Age` values with the median
- Dropped the `Cabin` column (77% missing values)
- Filled missing `Embarked` values with the mode (most common value)
- Removed duplicate rows
- Converted categorical columns (`Survived`, `Pclass`, `Sex`, `Embarked`) to the `category` data type
- Renamed unclear columns for readability:
  - `SibSp` → `siblings_spouses`
  - `Parch` → `parents_children`
  - `Fare` → `ticket_price`
  - `Cabin` → `cabin_number`
  - `Embarked` → `boarding_port`
  - `Pclass` → `ticket_class`
- Saved the cleaned dataset as `titanic_cleaned.csv`

## Features and Labels

**Label (target)** — the value we want to predict:
- `survived` — 0 = did not survive, 1 = survived

**Features** — the input columns used to predict the label:
- `ticket_class` — 1st, 2nd, or 3rd class ticket
- `sex` — male or female
- `age` — passenger's age
- `siblings_spouses` — number of siblings/spouse aboard
- `parents_children` — number of parents/children aboard
- `ticket_price` — amount paid for the ticket
- `boarding_port` — port they boarded from (S/C/Q)

## Files
- 'EDP_WEEK1.ipynb` — full cleaning notebook
- `Titanic_Dataset.csv` — raw dataset
- `titanic_cleaned_dataset.csv` — cleaned dataset

## Tools Used
Python, pandas, Google Colab

## What I Learned
Through this Week 1 task, I learned:
- How to load a dataset into pandas and inspect it using `.info()`, `.describe()`, and `.isnull()`
- How to handle missing values by filling them with median/mode or dropping columns with too much missing data
- How to remove duplicate rows
- How to convert columns to appropriate data types, including using the `category` type for columns that represent fixed labels rather than continuous numbers
- How to rename unclear column names for better readability
- The difference between features (input columns used to predict something) and labels (the actual outcome we're trying to predict)
- How to save a cleaned dataset and prepare it for future analysis or model training
