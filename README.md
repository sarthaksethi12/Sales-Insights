# Sales Insights - Data Analysis using Tableau & SQL
- Analyzed the sales data of an Indian hardware company to gain insights.

- Developed SQL-based ETL mappings to extract unstructured data, which was then transformed and cleaned in Tableau's staging area..

- Designed and developed a Tableau dashboard that utilizes quantitative visualizations to analyze various parameters affecting the company's performance year over year, providing actionable business insights and solutions.


### Problem Statement
Sales director wants to know the performance of the company in different states across India and offer discounts accordingly.

- Q1. Revenue breakdown by cities.

- Q2. Revenue brekdown by years & months.

- Q3. Top 5 customers by revenue & sales quantity.

- Q4. Top 5 Products by revenue.
  
- Q5. Net Profit & Profit Margin by Market

## Data Analysis Using SQL
  
1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001)

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai.

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars.

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table.

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai.

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";`
    
    
## Data Analysis Using Tableau 


#### Tableau Dashboard - [Revenue Analysis](https://public.tableau.com/views/SalesInsights_16772616796710/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)
	
<p  align="center"><a href="https://public.tableau.com/app/profile/sarthak.sethi/viz/SalesInsights_16772616796710/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link"><img width="100%" src="https://github.com/sarthaksethi12/Sales-Insights/blob/main/Revenue%20Analysis.png" /></a></p>

#### Tableau Dashboard - [Profit Analysis](https://public.tableau.com/views/SalesInsights_16772616796710/Dashboard-ProfitAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)
	
<p  align="center"><a href="https://public.tableau.com/app/profile/sarthak.sethi/viz/SalesInsights_16772616796710/Dashboard-ProfitAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link"><img width="100%" src="https://github.com/sarthaksethi12/Sales-Insights/blob/main/Profit%20Analysis.png" /></a></p>
  

 
