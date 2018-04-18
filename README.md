# Walmart Recruiting: Trip Type Classification

## Classification Team Project

### Data Science School 7th Team B-2

Competition Source: [Kaggle Competition - Walmart Recruiting: Trip Type Classification](https://www.kaggle.com/c/walmart-recruiting-trip-type-classification#description)

- Language: Python
- Classificatoin: scikit-learn, XGBoost

### Overview

- Subject: Walmart Trip Type Classification
- Dataset: Walmart
- Objective: Classification of each customers' TripType based on thier data
- Evaluation: multi-class logarithmic loss (cross entropy)

### Data fields

| Index | Feature               | Description                                  | Unique |
|-------|-----------------------|----------------------------------------------|--------|
| 1     | TripType              | A categorical id representing the type of shopping trip the customer made.                                       | 38     |
| 2     | VisitNumber           | An id corresponding to a single trip by a single customer                              | 95674  |
| 3     | Weekday               | The weekday of the trip                    | 7      |
| 4     | Upc                   | The UPC number of the product purchased                  | 97715  |
| 5     | ScanCount             | The number of the given item that was purchased. A negative value indicates a product return          | 39     |
| 6     | DepartmentDescription | A high-level description of the item's department                                | 69     |
| 7     | FinelineNumber        | A more refined category for each of the products, created by Walmart | 5196   |

## Contents

### 1. EDA & Preprocessing

### 2. Feature Engineering
- Feauture Engineering
    - UPC decoding
    - ScanCount seperation
    - Feature encoding
    - Dummy variables
    - Identifing the most frequently purchased items per VisitNumber

### 3. Modeling (Random Forest and XGBoost)
- Random Forest
- XGBoost

### 4. Results

### 5. Kaggle Submission
- Total Teams : 1,047 teams
- Final Score : 0.79154
- Leaderboard : 294/1,047 (top 30%)

### 6. Lesson
