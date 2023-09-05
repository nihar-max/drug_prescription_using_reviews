# 💊Drugs Prescription  using reviews

#### Since COVID-19 our medical fraternity is in distress, which results in numerous individuals demise. Due to unavailability, so people independently started taking medicines without proper consult which led to even worse condition. In such case Machine Learning can be useful to build the Prescription  system that uses the reviews of patients using various NLP techniques and recommend the top drug for given disease.


Number of data points: 161,297<br>
Number of unique drugs: 3,436<br>
Number of disease: 884<br>
Timespan: Apr 2008 - Sep 2017<br>
Attributes: 7<br>

Attribute Information:

1. UniuqeID -
2. DrugName - Drug Name
3. Condition - Patient condition
4. review - reviews given by patient after drug consumption
5. ratings - ratings given by patient after drug consumption (0-10)
6. date - Date when review given by patient
7. UsefulCount - Number of patient marked it as useful

Target Var:

1. Drug: Prescribe the best Drug based on sentiment of patients.

### **Objective**:
To build Prescription  model, which help in Prescribing the best drug based on given conditions and sentiment of patients.

## 2. Exploratory Data Analysis

### 2.1 Distribution of ratings
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/38c5eb69-0175-4929-8218-ccf10003586b)

### 2.3 Number of Ratings per a Year
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/b2a08bdd-e901-4b8d-9aa2-7ad12e2211f7)
Observation: There is a huge spike in ratings from 2014.

### 2.3 Univariate Analysis on condition using CDF
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/1366d47c-0152-4aea-8f8b-64e02d636f42)
Observation: By looking at CDF it seems that out of 800 unique conditions our 90% of data includes only top (50-75) conditions

### Q1. What is the 6 most frequent illness condition?
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/ceb50164-0379-47e9-94b9-d097300524af)

### Q2. What are 4 most frequently suggested drugs for those top 6 most frequent condition?
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/163ce10d-b7a4-44ad-9199-b8e78482e5d5)

### Q3. What is the 5 Highest Voted drugs by patients?
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/891bb718-d1a8-4d91-b56d-0eda2fae5bb6)

## 3. Reviews
### 3.1 Plot Word Clouds
- Creating Word Cloud for Likes i.e (positive / negative reviews)
- We can observe the most frequent occuring words for negative / positive reviews
### 1. Highly Satisfied
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/465bd45f-595b-42bd-89e8-9508678aecfd)

### 2.Satisfied
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/f14de8ef-b16d-47c3-94c6-7f762532107e)

### 3.Highly Unsatisfied
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/d4745d3c-ff2a-4221-9817-fad8ce985909)

## Feature Engineering

- So after loading the data we started with EDA process to understand the data through visualizations and also handles outliers and NaN values.In feature engineering we have created some of the features like rating per year,Last time prescribed drug,rating from 1-10.
- With help of Natural language processing we tried to understand the sentiment of patient w.r.t.o drug for given condition and calculated sentiment score (0-1) with help of inbult library sentiment_analyzer in NLP.

### Scoring Process
- After EDA & Feature engineering we scaled the data using MinMax scaler and with important features we have applied scoring process by manually adding weights to each feature and calculated score.
- After that we build the recommender system where by inserting the given condition it will provide top 5 best drugs with higher scores.
![image](https://github.com/nihar-max/drug_prescription_using_reviews/assets/61958476/f1f18c0f-2e3e-46d3-9acf-0c44abc2f272)








