# Sales analysis dashboard

## Project Aim
The aim is to create an interactive sales dashboard that provides insights into sales performance across different products and categories, helping stakeholders make data-driven decisions.

## Project Overview
The sales dashboard will include key metrics such as:
1. Total sales
2. Quantity sold
4. Top-selling products
5. Sales trends over time
6. Producct categories
7. Total profit and profit percentage
   
   ## Tools used
   1. Excel
   - for data cleaning
   2. Power BI 
   - data transformation and data visualization
   - Dashboard creation
     
   ## Data
   The data used in this project was downloaded from kaggle.Download [here](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard%20data.xlsx)
   
   ### Data description
   The excel file has two sheets
   1. ### Input data
   This sheet has the following columns:
    - Date - This is the date the transaction took place.
    - Product id - unique product identifier.
    - Quantity - The quantity of products bought.
    - Sale type - The type of sale ( either wholesale, direct sale or online sale).
    - Payment mode - The mode of payment used by customer to pay for the product(either cash or online). 
    - Discount - The amount of discount awarded for each product.
   2. ### Master data
      This sheet has the following columns:
      - Product id - unique product identifier.
      - Product - specific type of product.
      - Category - specific product category (Categories 1-5) 
      - UOM - this describes the unit of measurement for each product.
      - Buying price - the price the product was bought for.
      - Selling price - the price the product was sold for.
   ### Data cleaning
   1. Checked for missing values - there were no missing values
   2. Checked for duplicates - there were no duplicates
   
   ## Data transformation and preparation
   
    1. Added four columns from the date column :
        - Day
        - Month
        - Year
        - Name of month and extracted the first 3 characters
    2. Using merge query, added the columns from the master data
        - The data was merged using left join on product id
    3. Added new columns for total buying value and total selling value
        - Total buying value = sold quantity * buying price
        - Total selling value = sold quantity * selling price * (1 - discount)
    4. Added measures for profit and profit percentage
        - Profit = Total selling value - Total buying value
        - Profit percentage = profit / total buying value
      
  ## Data visualization and dashboard creation 
  1. Added slicers for month, year, sales type and mode of payment.
     - List slicer for year and
     - Drop down for sales type and payment mode
  2. Card visual for total sales, total profit, profit percentage, total quantity
  3. Added stacked column chart for monthly visual for total sales and total profit, sorting it by month(add profit % to tool tip)
  4. Clustered bar chart for total sales and products
  5. Stacked area chart for total sales and days of the week
  6. Donut chart for sale type and total sales
  7. Tree map for category and total sales
     ## Preview of created dashboard
     ![My Image](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard%20preview.jpg)

     ## How to Use the Dashboard:
     You can download the `.pbix` file from this repository.
      Download  [here](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard.pbix)
     ## Results and Insights:
     ### 2021
     
| Metric          | Direct sales  |     Online     |   Wholesaler     |
|-----------------|---------------|----------------|------------------|
| Total sales     |     95k       |     68k        |    25k           |
| Total profit    |     16k       |     11k        |    4k            |
| profit%         |     20%       |     19%        |    19%           |
| Product quantity|     41        |     41         |    16            |
| Top product     |   product 41  |   product 24   |   product 42     |
| Top category    |   category 02 |   category 03  |   category 05    |

   ### 2022
   
| Metric          | Direct sales  |     Online     |   Wholesaler     |
|-----------------|---------------|----------------|------------------|
| Total sales     |     113k      |     66k        |    35k           |
| Total profit    |     20k       |     11k        |    7k            |
| profit%         |     22%       |     21%        |    24%           |
| Product quantity|     45        |     46         |    23            |
| Top product     |   product 30  |   product 02   |   product 19     |
| Top category    |   category 02 |   category 01  |   category 05    |
     
     ## Conclusion and Recommendations:
      
