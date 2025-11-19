# Customer Segmentation For Marketing Campaigns of SuperStore | Python

---
![E-commerce Website_Analysis](https://github.com/Dorothy-Ho-Vy/Sample-Readme-template/blob/0e47d32968459ec80d7d2666fbf5044ac56894e6/1.png)

Change Icon emoji 🔥🔍📘🚩 to your likings by clicking "Start" + "."


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



 This project analyzes sales trends and inventory control using SQL and Power BI. The objective is
✔️ Identify high-demand products and sales trends.  
✔️ Optimize inventory levels to prevent overstocking or stockouts.  
✔️ Provide actionable insights through Power BI dashboards.  


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

👉🏻 Insert a screenshot of table schema. if table is too long, only show a snapshot of it. Recommend to put it in a toggle format

 _Example:_

| Column Name | Data Type | Description |  
|-------------|----------|-------------|  
| Product_ID  | INT      | Unique identifier for each product |  
| Name        | TEXT     | Product name |  
| Category    | TEXT     | Product category |  
| Price       | FLOAT    | Price per unit |  



Table 2: Sales Transactions  

👉🏻 Insert a screenshot of table schema. if table is too long, only show a snapshot of it. Recommend to put it in a toggle format


 _Example:_

| Column Name    | Data Type | Description |  
|---------------|----------|-------------|  
| Transaction_ID | INT      | Unique identifier for each sale |  
| Product_ID     | INT      | Foreign key linking to Products table |  
| Quantity       | INT      | Number of items sold |  
| Sale_Date      | DATE     | Date of transaction |  


**_📌If the table is too big, only capture a part of it that contains key metrics you used in the projects or put the table in toggle_**

<details>
<summary>Click to toggle</summary>

This content is hidden by default and will expand/collapse when clicked.

You can add more details here, like code blocks, lists, or images.
</details>

#### 3️⃣ Data Relationships:  
Describe the connections between tables—e.g., one-to-many, many-to-many.  

👉🏻 Include a screenshot of Data Modeling to visualize relationships.  

---

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
