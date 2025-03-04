# Superstore Sales Data Analysis

```sql
Tools being used for the project: Excel
```
## Overview
In this project, I will analyze a superstore sales dataset using Excel. The process will involve cleaning and transforming the dataset, followed by an in-depth analysis using Excel. Additionally, I will create pivot tables and develop a visual dashboard to present key insights revolving around the super stores sales. The following is the final output after completing the project. --> [Superstore Data Analysis](https://github.com/user-attachments/files/19046982/Superstore.Data.Analysis.1.xlsx)

## Retrieving the dataset
The dataset that i will be working with can be located from the following Tableau community post --> [Sample Dataset](https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls) 

## Understanding the dataset
1. **Orders Tab**
This is the primary tab containing most of the data that I will be cleaning and analyzing. The dataset uses the Order ID as the primary key, with each row representing a specific order and its associated details. It includes customer information, shipping modes, product details, and sales metrics such as sales amount, profit, and discounts. After an initial review, I noticed certain columns that may require further refinement, and I plan to explore ways to integrate the Returns and People tabs into the Orders dataset for a more comprehensive analysis.

2. **Returns Tab**
This is the second tab in the sample excel dataset I will be analyzing, which contains only the return status and Order ID. I plan to use VLOOKUP to bring in relevant columns from the Orders tab to enrich this Returns table.

3. **People Tab**
This tab contains information about the sales representatives assigned to each region. With only four columns and two rows, it is the smallest tab in the entire superstore dataset.

## Cleaning the dataset
The superstore dataset is already clean, which has saved me some time however i will be transforming the dataset prior to analyzing.

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
I worked exclusively with the Orders tab, focusing on sales to create the Superstore dashboard. The pivot tables I created can be found in the [Superstore Data Analysis](https://github.com/user-attachments/files/19046982/Superstore.Data.Analysis.1.xlsx) Excel File.

## Data visualization 
This is the Superstore Dashboard I created using the pivot tables developed in the Calculations tab, the dashboard specifically revolves around the super stores sales metric. The following is a snapshot of the dataset, but feel free to explore the dynamic dashboard by accessing the full version versopm of the [Superstore Data Analysis](https://github.com/user-attachments/files/19046982/Superstore.Data.Analysis.1.xlsx) excel file.
![](https://github.com/user-attachments/assets/6f63dcca-c00a-4e0c-9b20-85b36a73f372)

