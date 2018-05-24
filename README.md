# [Walmart Recruiting: Trip Type Classification](https://github.com/novdov/dss7_SWYA_walmart/blob/master/main/2%ED%8C%80(SWYA)_B_%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C.ipynb)

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

- Indicate Null data (UPC, DepartmentDescription, FinelineNumber)
- Distribution of Triptype on Weekday
- Compare most rrequent and least frequent TripTypes
- Distrubution of DepartmentDescription on TripTypes
- Find manually intepretable TripType (e.g.) TripType 999: trip for return)
- Figure out how to handle data (DataFrame) - Pivot table by VisitNumber



<img src="https://i.imgur.com/KuSPjth.png" width="750">



### 2. Feature Engineering
- Feauture Engineering
    - UPC decoding
    - ScanCount separation
    - Feature encoding
    - Dummy variables
    - Identifing the most frequently purchased items per VisitNumber

### 3. Modeling
- XGBoost

### 4. Results

- Log Loss: 0.79154
- Accuracy: 73.73%

### 5. Kaggle Submission
- Total Teams : 1,047 teams
- Final Score : 0.79154
- Leaderboard : 294/1,047 (top 30%)

### 6. Lesson

- EDA & Feature Engineering
    - MF_FinelineNumber (Most Frequent FinelineNumber), company외에 중요한 feature 미반영
    - ScanCount로부터 다양한 수치적 feature (mean, min, max, min-max range)를 시도했으나 성능 향상에 도움이 안 됨
    - feature를 300~600개 사용했을 때보다 85개에서 가장 높은 성능 (feature 증가 시 다중공선성 의심)
    - 주어진 feature의 수가 적은 상황에서 효과적인 feature engineering에 대한 공부 필요


- Modeling
    - 효과적인 GridSearch에 대한 아쉬움
