# Walmart Recruiting: Trip Type Classification

## Classification Team Project

### Data Science School 7th Team B-2

Competition Source: [Kaggle Competition - Walmart Recruiting: Trip Type Classification](https://www.kaggle.com/c/walmart-recruiting-trip-type-classification#description)

- Language: Python
- Classificatoin: scikit-learn, XGBoost

### Overview

- Subject: Walmart Trip Type Classification
- Dataset: Walmart
- Objective: Improving the science behind trip type classification to help Walmart refine their segmentation process.
- Evaluation: multi-class logarithmic loss (cross entropy)

### Data fields

| Index | Feature               | Description                                  | Unique |
|-------|-----------------------|----------------------------------------------|--------|
| 1     | TripType              | Target                                       | 38     |
| 2     | VisitNumber           | 각 손님의 Index                              | 95674  |
| 3     | Weekday               | VisitNumber가 발생한 요일                    | 7      |
| 4     | Upc                   | 구매한 제품의 고유한 바코드                  | 97715  |
| 5     | ScanCount             | 구매 수량 ( 반품 시 - 값으로 표기 )          | 39     |
| 6     | DepartmentDescription | 제품의 대분류                                | 69     |
| 7     | FinelineNumber        | 월마트 자체적으로 정의 한 제품의 소분류 코드 | 5196   |

## Contents

### 1. EDA & Preprocessing

### 2. Feature Engineering

### 3. Modeling (Random Forest and XGBoost)

### 4. Results

### 5. Kaggle Submission

### 6. Lesson
