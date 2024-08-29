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
   - For data cleaning
   2. Power BI 
   - Data transformation and data visualization
   - Dashboard creation
     
   ## Data
   The data used in this project was downloaded from kaggle.Download [here](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard%20data.xlsx)
   
   ### Data description
   The excel file has two sheets.
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
   3. Checked for errors, and data types to ensure consistency and acuuracy of the data.  
   
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
     - List slicer for year 
     - Drop down for sales type and payment mode
  2. Card visual for total sales, total profit, profit percentage, top product and top category. 
  3. Added stacked column chart for monthly visual for total sales and total profit, sorting it by month(add profit % to tool tip)
  4. Clustered bar chart for total sales and products
  5. Stacked area chart for total sales and days of the week
  6. Donut chart for sale type, payment mode and total sales
  7. Tree map for category and total sales
     ## Preview of the created dashboard
     ![My Image](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard%20preview.jpg)

     ## How to Use the Dashboard:
     You can download the `.pbix` file from this repository.
      Download  [here](https://github.com/Emily-Ngahu/Sales-dashboard/blob/main/Sales%20dashboard.pbix)
     ## Results and Insights:
The tables below shows the distribution of the type of the type of sales for the years 2021 and 2022

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

 1. In both 2021 and 2022, direct sales generated the most revenue.
 2. In 2021, most sales were generated in October while in 2022, most sales were generated in November.
 3. In 2021, a total of 187k sales were made with a profit of 30k.
 4. In 2022, a total of 214k sales were made with a profit of 39k.
 5. Online(mode of payment) generated the highest sales in both years.
 6. In 2021, product 42 generated most sales while in 2022, product 30 generated the most sales.
 7. In 2021, category 05 generated most sales while in 2022, category 04 generated the most sales.
 
     ## Conclusions:
    1. Sales and Profit Growth:
- There was a significant increase in both sales and profit from 2021 to 2022. Sales grew from 187k in 2021 with a profit of 30k to 214k in 2022 with a profit of 39k, demonstrating a positive trend in overall business performance.
  
    2. Online Payment Dominance:
- Online payment was the most popular mode of payment in both years, reflecting a customer preference for convenience and digital transactions.
  
    3. Seasonal Sales Trends:
- Sales peaked in October 2021 and November 2022, indicating potential seasonal factors or marketing campaigns that drove higher sales during these months.
  
    4. Revenue Growth Across Both Years:
- Direct sales were consistently the top revenue generator in both 2021 and 2022, highlighting the importance of direct channels in driving overall revenue growth.
  
     ## Recommendations:
  1. Focus on Direct Sales Channels:
- Since direct sales consistently generate the highest revenue, it is important to continue optimizing these channels. This could include improving customer experience, expanding the sales team, and enhancing CRM strategies.
  
  2. Enhance Online Payment Options:
- With online payments being the most preferred mode, continue enhancing the online payment experience. Consider offering more payment options, improving transaction security, and promoting the convenience of online payments.
  
  3. Plan for Growth and Scalability:
- Given the year-over-year growth in sales and profits, invest in scaling operations, enhancing supply chain efficiency, and expanding market reach. Forecast future demand based on historical growth trends and prepare to meet increasing customer needs.
  
      
