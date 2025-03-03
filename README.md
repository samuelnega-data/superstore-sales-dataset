# Superstore Sales Data Analysis

```sql
Tools being used for the project: Excel
```
## Overview
In this project, I will analyze a superstore sales dataset using Excel. The process will involve cleaning and transforming the dataset, followed by in-depth analysis using Excel. Additionally, I will create pivot tables and develop a visual dashboard to present key insights.

## Retrieving the dataset
The dataset that i will be working with can be located from the following Tableau community post: https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls 

## Understanding the dataset
1. **Orders Tab**
This is the primary tab containing most of the data that I will be cleaning and analyzing. The dataset uses the Order ID as the primary key, with each row representing a specific order and its associated details. It includes customer information, shipping mode, product details, and sales metrics such as sales amount, profit, and discounts. After an initial review, I noticed certain columns that may require further refinement, and I plan to explore ways to integrate the Returns and People tabs into the Orders dataset for a more comprehensive analysis.

2. **Returns Tab**
This is another tab that I will be analyzing, which contains only the return status and Order ID. I plan to use VLOOKUP to bring in relevant columns from the Orders tab to enrich this Returns table for a more comprehensive analysis.

3. **People Tab**
This tab contains information about the sales representatives assigned to each region. With only four columns and two rows, it is the smallest tab in the entire superstore dataset.

## Cleaning the dataset
The superstore dataset is already clean, which has saved me some time.

## Transforming the dataset
- **Added 5 columns** onto the **Orders tab.**
  - Profit per Product: ```=V2/T2``` (Profit/Quantity)
  - Discount Amount: ```=S2*U2``` (Sales*Discount)
  - Profit Margin: ```=V2/S2``` (Sales/Profit) 
  - COGS: ```=S2-V2``` (Sales-Profit)
  - Sales Rep: To add this column i used the filter column and pasted the names of the sales rep from each region. I could have also used ```VLOOKUP``` to do this aswell however since there were only 4 sales reps it didnt require much time.
- **Added 9 columns** onto the **Returns tab.**
  - Customer: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,6,FALSE)```
  - State: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,10,FALSE)```
  - City: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,9,FALSE)``` 
  - Region: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,12,FALSE)```
  - Product ID: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,13,FALSE)```
  - Category: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,14,FALSE)```
  - Subcategory: ```=VLOOKUP(B2,Orders!$B$2:$Q$9995,15,FALSE)```
  - Return Product: ```=VLOOKUP(B2,Orders!$B$2:$S$9995,17,FALSE)```
  - Quantity: ```=VLOOKUP(B2,Orders!$B$2:$T$9995,18,FALSE)```
    

## Creating Pivot tables (Calculations Tab) 
I worked exclusively with the Orders tab, focusing on sales to create the Superstore dashboard. Below are the pivot tables I created.
![image](https://github.com/user-attachments/assets/9ac3fc87-a4a7-44ec-8318-7490228f3bfc)
![image](https://github.com/user-attachments/assets/1ab3500b-f085-4dd2-8da7-3427f832b8be)
![image](https://github.com/user-attachments/assets/0720440c-39a4-4e7f-ac45-2bca23395f2d)
![image](https://github.com/user-attachments/assets/e8f6b25f-44f1-4cdc-a5d8-dcf47b940e55)
![image](https://github.com/user-attachments/assets/6636b8cd-7125-486e-b6e1-c1b4f0b9e78c)
![image](https://github.com/user-attachments/assets/bd72dacb-d622-48c6-a14c-cd699e632974)
![image](https://github.com/user-attachments/assets/af6c73b8-8445-409b-95b6-68b63591157a)
![image](https://github.com/user-attachments/assets/12be38bc-ce26-46f7-8b7e-aa21b311bc68)
![image](https://github.com/user-attachments/assets/d8ae0ea4-d9e3-4d7a-b80b-4836f352ab2e)


## Data visualization 
The dataset that i will b
