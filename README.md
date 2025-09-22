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

First four Records:

|Car_id	Date	|Customer Name	|Gender	|Annual Income	|Dealer_Name	|Company	Model	|Engine	|Transmission	|Color	|Price ($)	|Dealer_No 	|Body Style	|Phone	|Dealer_Region	|Year|
|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|
|C_CND_000001	|1/2/2022	|Geraldine	|Male	|13500	|Buddy Storbeck's Diesel Service Inc	|Ford	|Expedition	|DoubleÃ‚Â Overhead Camshaft	|Auto	|Black	|26000	|06457-3834	|SUV	|8264678	|Middletown	|2022|
|C_CND_000002	|1/2/2022	|Gia	|Male	|1480000	|C & M Motors Inc	|Dodge	|Durango	|DoubleÃ‚Â Overhead Camshaft	|Auto	|Black	|19000	|60504-7114	|SUV	|6848189	|Aurora	|2022|
|C_CND_000003	|1/2/2022	|Gianna	|Male	|1035000	|Capitol KIA	|Cadillac	|Eldorado	|Overhead Camshaft	|Manual	|Red	|31500	|38701-8047	|Passenger	|7298798	|Greenville	|2022|
|C_CND_000004	|1/2/2022	|Giselle	|Male	|13500	|Chrysler of Tri-Cities	|Toyota	|Celica	|Overhead Camshaft	|Manual	|Pale White	|14000	|99301-3882	|SUV	|6257557	|Pasco	|2022|


## Query Language
Some of the query languages to retrieve records are displayed here

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


### Charts


### PowerBI Dashboard


### PowerBI Single Visual

#### Total Sales By customers



#### Total Sales By Age Category



#### Total Sales By Level of Preferred Payment Method, and Customer Gender



[View_my_Linkedin Profile](https://www.linkedin.com/in/ebube-ilo/)

