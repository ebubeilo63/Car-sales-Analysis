# Mobile-Sales-Analysis

## Overview:
**This is the sales report for Mobile Sales Product**

---

## Contents
[Project Overview](#Project-Overview)  |  [Dataset Source](#Dataset-Source)  |  [Tools used](#Tools-Used)  |  [Table Outlay](#Table-Outlay)  |  [Query Language](#Query-Language)  |  [Visuaization](#Visualization) 

---
## Project Overview
> >This project analyzes the sales of Mobile Product to uncover the insights on sales distributio by arious attributes such as Brands, Customer Gender and payment methods. Using Pivot tables, I explored metrics like total sales by Payment Method and Gender, average income of buyers, gender distribution and overall revenue. This analysis helps to understand the key factors driving sales in the dataset provided.

##  Dataset Source  
www.kaggle.com/dataset

## Tools Used  
+ **Power BI** 
+ **Excel**  
+ **SQL** 


## Table Outlay:

First Three Records:

|TransactionID| Date	|MobileModel	|Brand	|Price	|UnitsSold	|TotalRevenue	|CustomerAge	|CustomerGender	|Location |PaymentMethod
|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b	|1/6/2024	|direction	|Green Inc	|1196.95	|85	|28002.8	|32	|Female	|Port Erik	|Online|
|4f87d114-f522-4ead-93e3-f336402df6aa	|4/5/2024	|right	|Thomas-Thompson	|1010.34	|64	|2378.82	|55	|Female	|East Linda	|Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1	|2/13/2024	|summer	|Sanchez-Williams	|400.8	|95	|31322.56	|57	|Male	|East Angelicastad	|Online|
|7da7de95-f772-4cc2-bce0-b0873f98233e	|4/17/2024	|keep	|Greer and Sons	|338.6	|79	|31159.75	|46	|Other	|East Kevin	|Cash|

## Query Language
Some of teh query languages to retrieve records are displayed here

```SQL

--- Table for New Car Dataset---
SELECT * FROM [dbo].[CarDataCSV];

--categorizing the data into silver,gold,diamond---

SELECT Price,
CASE
WHEN Price <= 15000 THEN 'Silver' WHEN Price >= 15100 THEN 'Gold'
ELSE 'Diamond'
END 'Ranking'
FROM [dbo].[CarDataCSV] ;

---2. Retriving all female customer that bought goods with Price above 900 ---

SELECT Gender,Price FROM  [dbo].[CarDataCSV]
WHERE Gender = 'Female' AND Price > 900;

---3. Retriving the sales by payment method arranging from largest to smallest amount---

SELECT Annual_Income,SUM (Price) AS Sales
FROM [dbo].[CarDataCSV]
GROUP BY Annual_Income
ORDER BY Sales DESC;

---4. Retrive the most expensive Body_style---

SELECT MAX (Price) AS Price,Body_style FROM [dbo].[CarDataCSV]
GROUP BY Body_style
ORDER BY Price DESC;

---5.How many Body_style are there---

SELECT COUNT (DISTINCT Body_Style) AS Num_of_BodyStyle FROM [dbo].[CarDataCSV];
```

## Visualization
### Pivot Tables

<img width="1316" height="385" alt="Screenshot 2025-09-20 034011" src="https://github.com/user-attachments/assets/0df6e9e7-d171-4d55-8b45-3e83bf16e2c3" />

### Charts

<img width="1793" height="678" alt="Screenshot 2025-09-20 033735" src="https://github.com/user-attachments/assets/3949c77f-7a5f-4e1f-a85c-60aaf20fa5c7" />

### PowerBI Dashboard

<img width="1397" height="764" alt="Screenshot 2025-09-07 211709" src="https://github.com/user-attachments/assets/02cad351-77cc-48d0-bdc0-a6bdeabd0f08" />

### PowerBI Single Visual

#### Total Sales By customers

<img width="1397" height="785" alt="Screenshot 2025-09-07 211651" src="https://github.com/user-attachments/assets/a1738abb-0529-4736-b76d-fe3807711c28" />

#### Total Sales By Age Category

<img width="1400" height="782" alt="Screenshot 2025-09-07 211601" src="https://github.com/user-attachments/assets/f7a9fd21-e896-4e70-a96d-651ed384b185" />

#### Total Sales By Level of Preferred Payment Method, and Customer Gender

<img width="1399" height="788" alt="Screenshot 2025-09-07 211627" src="https://github.com/user-attachments/assets/8ba5adc9-5075-421b-a6be-4638d4c4b902" />

[View_my_Linkedin Profile](https://www.linkedin.com/in/ebube-ilo/)

