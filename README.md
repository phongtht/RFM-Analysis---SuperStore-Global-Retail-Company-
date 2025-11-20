# Customer Segmentation For Marketing Campaigns of SuperStore | Python

---
![E-commerce Website_Analysis](https://github.com/Dorothy-Ho-Vy/Sample-Readme-template/blob/0e47d32968459ec80d7d2666fbf5044ac56894e6/1.png)

# Applying the RFM model in Python to bulid customers segmentation and recommend appropriate marketing solutions.*

**Author:** Tran Huu Tran Phong

**Date:** June 2025

**Tools Used:** Python

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

### Objective:
### 📖 What is this project about ? 
 🎯 Main Business Question

SuperStore use RFM segmentation to efficiently categorize customers and design high-impact marketing campaigns for Christmas and New Year ?

📘 Project Overview
- To maximize the impact of marketing campaigns for the global retailer SuperStore, this project applied the RFM model (Recency, Frequency, Monetary value) to intelligently segment customers. By implementing this high-volume segmentation process in Python, we can accurately measure customer value, categorize the entire customer base, and deliver data-backed insights for highly targeted and efficient marketing recommendations.

- Key Steps Included:

 - Preparing the RFM dataset.

 - Calculating R, F, and M scores (using 31/12/2011 as the Recency reference date).

 - Applying quintile scoring (1–5 scale) to define segment boundaries.

 - Assigning segments and visualizing their distribution.

 - Processing actionable insights and marketing recommendations.


### 👤 Who is this project for ?  
✔️ Data analysts & Business analysts  
✔️ Sales & Marketing Management  
✔️ Business Management
✔️ Customrer Relationship Managerment Teams

### What is RFM model ? Why RFM ? How does it work ?

🚩 What ?
- RFM (Recency, Frequency, Monetary) analysis is a proven marketing model for behavior-based customer segmentation. It groups customers based on their transaction history – how recently, how often, and how much they have purchased.

🚩 Why RFM?

RFM - Recency, Frequency, and Monetary value.
- Recency: How long it has been since a customer last bought something.
- Frequency: How many times the customer has made purchases.
- Monetary: How much money the customer has spent in total.

RFM helps divide customers into various categories or clusters to identify customers who are more likely to respond to promotions and also for future personalization services.

This model could be very useful, especially for small and medium-sized enterprises (SMEs) with limited marketing resources, helping them focus on the potentially right customer segments to increase ROI, reduce churn, reduce cost, improve customer relationship, and a lot more.

🚩 How does it work?
- In RFM analysis, customers are scored based on three factors (Recency - how recently, Frequency - how often, Monetary - how much), then labeled based on the combination of RFM scores.
- By combining these quintile scores, customers are segmented into distinct groups based on their R, F, and M profiles. This enables businesses to pinpoint high-value assets, loyal patrons, and those at risk of churning.
---

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
- Source: Superstore — Kaggle 
- Size:
    E-commerce retail table - 541909 rows & 8 columns
    Segmentaition table - 12 rows & 2 columns
- Format: .xlsx  

### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used:  2 tables 
- Table 1: E-commerce Retail – 541909 rows & 8 columns

|        | InvoiceNo | StockCode |                         Description | Quantity |         InvoiceDate | UnitPrice | CustomerID |        Country |
|--------|-----------|-----------|-------------------------------------|----------|---------------------|-----------|------------|----------------|
|    0   |    536365 |    85123A |  WHITE HANGING HEART T-LIGHT HOLDER |        6 | 2010-12-01 08:26:00 |      2.55 |    17850.0 | United Kingdom |
|    1   |    536365 |     71053 |                 WHITE METAL LANTERN |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |
|    2   |    536365 |    84406B |      CREAM CUPID HEARTS COAT HANGER |        8 | 2010-12-01 08:26:00 |      2.75 |    17850.0 | United Kingdom |
|    3   |    536365 |    84029G | KNITTED UNION FLAG HOT WATER BOTTLE |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |
|    4   |    536365 |    84029E |      RED WOOLLY HOTTIE WHITE HEART. |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |
|   ...  |       ... |       ... |                                 ... |      ... |                 ... |       ... |        ... |            ... |
| 541904 |    581587 |     22613 |         PACK OF 20 SPACEBOY NAPKINS |       12 | 2011-12-09 12:50:00 |      0.85 |    12680.0 |         France |
| 541905 |    581587 |     22899 |         CHILDREN'S APRON DOLLY GIRL |        6 | 2011-12-09 12:50:00 |      2.10 |    12680.0 |         France |
| 541906 |    581587 |     23254 |        CHILDRENS CUTLERY DOLLY GIRL |        4 | 2011-12-09 12:50:00 |      4.15 |    12680.0 |         France |
| 541907 |    581587 |     23255 |     CHILDRENS CUTLERY CIRCUS PARADE |        4 | 2011-12-09 12:50:00 |      4.15 |    12680.0 |         France |
| 541908 |    581587 |     22138 |        BAKING SET 9 PIECE RETROSPOT |        3 | 2011-12-09 12:50:00 |      4.95 |    12680.0 |         France |

- Sheet 2: Segmentation – 12 rows & 2 columns

|        Segment        |                                                        RFM Score                                                       |
|-----------------------|------------------------------------------------------------------------------------------------------------------------|
| Champions             | 555, 554, 544, 545, 454, 455, 445                                                                                      |
| Loyal                 | 543, 444, 435, 355, 354, 345, 344, 335                                                                                 |
| Potential Loyalist    | 553, 551, 552, 541, 542, 533, 532, 531, 452, 451, 442, 441, 431, 453, 433, 432, 423, 353, 352, 351, 342, 341, 333, 323 |
| New Customers         | 512, 511, 422, 421, 412, 411, 311                                                                                      |
| Promising             | 525, 524, 523, 522, 521, 515, 514, 513, 425, 424, 413, 414, 415, 315, 314, 313                                         |
| Need Attention        | 535, 534, 443, 434, 343, 334, 325, 324                                                                                 |
| About To Sleep        | 331, 321, 312, 221, 213, 231, 241, 251                                                                                 |
| At Risk               | 255, 254, 245, 244, 253, 252, 243, 242, 235, 234, 225, 224, 153, 152, 145, 143, 142, 135, 134, 133, 125, 124           |
| Cannot Lose Them      | 155, 154, 144, 214, 215, 115, 114, 113                                                                                 |
| Hibernating Customers | 332, 322, 233, 232, 223, 222, 132, 123, 122, 212, 211                                                                  |
| Lost Customers        | 111, 112, 121, 131, 141, 151                                                                                           |                            
#### 2️⃣ Table Schema & Data Snapshot  

Table 1: Products Table  

| Column Name | Data Type | Description |  
|-------------|-----------|-------------|  
|StockCode	   | TEXT	   |The unique product code or item identifier.|
|Description  |	TEXT	     |The short description of the product.|
|Quantity	    | INT	      |The number of units of the product purchased in that transaction line item. Negative values indicate a return/cancellation.|
|InvoiceDate  |	TEXT	     | The date and time when the transaction was generated. (Needs conversion to DATETIME for analysis).|
|UnitPrice	   | FLOAT     |	The price per unit of the item in the local currency.|
|CustomerID	  | FLOAT     |	The unique identifier for the customer. Null values indicate sales made to unregistered/guest customers.|
|Country	     | TEXT	     |The name of the country where the customer resides or where the transaction occurred.|

Table 2: Sales Transactions  

| Column Name    | Data Type | Description |  
|----------------|-----------|-------------|  
| Segment        | TEXT      | The descriptive name of the customer group (e.g., Champions, Loyal, About To Sleep).|  
| RFM Score      | TEXT      | A comma-separated list of 3-digit scores corresponding to that segment. The score is based on Recency, Frequency, and Monetary Value. |  
 
---

## 3. 🔍 Exploratory Data Analysis (EDA)

### 3.1. Understand Data

#### a. Import Packages & Load Data Set
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
!pip install squarify
import squarify
raw_data = pd.read_csv(path+'ecommerce_retail.csv')
seg = pd.read_csv(path+'segmentation.csv')

raw_data.head
```
|        | InvoiceNo | StockCode |                         Description | Quantity |         InvoiceDate | UnitPrice | CustomerID |        Country |
|--------|-----------|-----------|-------------------------------------|----------|---------------------|-----------|------------|----------------|
|    0   |    536365 |    85123A |  WHITE HANGING HEART T-LIGHT HOLDER |        6 | 2010-12-01 08:26:00 |      2.55 |    17850.0 | United Kingdom |
|    1   |    536365 |     71053 |                 WHITE METAL LANTERN |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |
|    2   |    536365 |    84406B |      CREAM CUPID HEARTS COAT HANGER |        8 | 2010-12-01 08:26:00 |      2.75 |    17850.0 | United Kingdom |
|    3   |    536365 |    84029G | KNITTED UNION FLAG HOT WATER BOTTLE |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |
|    4   |    536365 |    84029E |      RED WOOLLY HOTTIE WHITE HEART. |        6 | 2010-12-01 08:26:00 |      3.39 |    17850.0 | United Kingdom |

#### b. Data Type & Data Value

```
print(df.info()) 
print(df.describe())
```
*Information of thed data type of each column*
| # | Column      | Non-Null Count  | Dtype          |
|---|-------------|-----------------|----------------|
| 0 | InvoiceNo   | 541909 non-null | object         |
| 1 | StockCode   | 541909 non-null | object         |
| 2 | Description | 540455 non-null | object         |
| 3 | Quantity    | 541909 non-null | int64          |
| 4 | InvoiceDate | 541909 non-null | datetime64[ns] |
| 5 | UnitPrice   | 541909 non-null | float64        |
| 6 | CustomerID  | 406829 non-null | float64        |
| 7 | Country     | 541909 non-null | object         |

*Describe the data value of the columns (min, max, count,...)*
|       | Quantity      |  UnitPrice     | CustomerID    |
|-------|---------------| ---------------|---------------|
| count | 541909.000000 |  541909.000000 | 406829.000000 |
| mean  | 9.552250      |  4.611114      | 15287.690570  |
| min   | -80995.000000 |  -11062.060000 | 12346.000000  |
| 25%   | 1.000000      |  1.250000      | 13953.000000  |
| 50%   | 3.000000      |  2.080000      | 15152.000000  |
| 75%   | 10.000000     |  4.130000      | 16791.000000  |
| max   | 80995.000000  |  38970.000000  | 18287.000000  |
| std   | 218.081158    |  96.759853     | 1713.600303   |

#### Insights:

After reviewing desription of the data value of numerical columns ( Quantity, UnitPrice, CustomerID), there are several data quality issues. These must be tackled before conducting deeper analysis or building models:

- Negative values detected in 'Quantity' and 'UnitPrice'.
- Missing values of 'Description' and 'CustomerID'.
- Incorrect or inconsistent product descriptions in some orders.
- Transactions with negative quantities that are not marked as cancellations.


### 3.2. Hanlde missing values

```
raw_data.isnull().sum()
```
<img width="242" height="369" alt="ss" src="https://github.com/user-attachments/assets/dc08bfdc-5806-4040-b559-c71d0def9cf8" />

```
create_report(raw_data)
```

### 3.3.


raw_data['transaction_date'] = pd.to_datetime(raw_data['InvoiceDate']).dt.date
raw_data.head()




## 🧠 Design Thinking Process  

Explain the step-by-step approach taken to solve the problem.  

👉🏻 Insert a screenshot of the Design Thinking steps (Screenshot your Excel design thinking tables for better presentation).  

1️⃣ Empathize  
2️⃣ Define point of view  
3️⃣ Ideate  
4️⃣ Prototype and review  

**_📌Use Canva/ Powerpoint to change the format of your Design thinking table, making it more visually pleasant_**
---

## ⚒️ Main Process

**_📌If your project involves SQL as 1st part of data preprocessing, do this part, or else you can skip this part and jump directly into the Visualization part_**

1️⃣ Data Cleaning & Preprocessing 
2️⃣ Exploratory Data Analysis (EDA)  
3️⃣ SQL/ Python Analysis 

- In each step, show your Code

- Include query/ code execution screenshots or result samples

- Explain its purpose and its findings


4️⃣ Power BI Visualization  (applicable for PBI Projects)

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  
👉🏻 Insert Power BI dashboard screenshots here  

📌 Analysis 1:  
- Observation: _Describe trends, key metrics, and patterns. Any insights from those observation_  
- Recommendation: _Suggest actions based on insights._  

#### 2️⃣ Dashboard 2 Preview  
👉🏻 Insert Power BI dashboard screenshots here

📌 Analysis 2:   
- Observation: _Describe trends, key metrics, and patterns. Any insights from those observation_  
- Recommendation: _Suggest actions based on insights._  

#### 3️⃣ Dashboard 3 Preview  
👉🏻 Insert Power BI dashboard screenshots here  

📌 Analysis 3:  
- Observation: _Describe trends, key metrics, and patterns. Any insights from those observation_  
- Recommendation: _Suggest actions based on insights._  

---

## 🔎 Final Conclusion & Recommendations  

👉🏻 Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:  

📌 Key Takeaways:  
✔️ Recommendation 1  
✔️ Recommendation 2  
✔️ Recommendation 3

**_📌Remember to summarize the most core insights/ observations you extract from the entire projects. 
 Recap ONLY key actions/ recommendations. DO NOT copy paste everything above_**
