
# Project 
## Sales Insights of Data Analysis-AtliQ Hardware




## Problem Statement

AtliQ Hardware is a company that distributes computer hardware and peripherals to various clients, including surge stores and Nomad stores, across India. The company's headquarters is located in Delhi, India, with numerous regional offices throughout the country.

The sales director is currently grappling with challenges due to the dynamic growth of the market. Tracking sales in this rapidly evolving market has become problematic, and there are concerns about the overall business growth, as sales have been on the decline. The sales director oversees regional managers for North India, South India, and Central India. However, obtaining insights from these regions involves verbal communication, with regional managers providing quarterly sales updates over the phone.

The frustration arises from the lack of tangible proof and facts regarding how the business is being affected. Despite the apparent decline in overall sales, the verbal updates from regional managers do not provide a comprehensive picture. This is particularly concerning given the size of AtliQ Hardware as a significant business entity.

To address this issue and gain a clearer understanding of business insights, the sales director is seeking a simple data visualization tool. He envisions a tool that can be accessed daily, providing visual representations of key sales metrics. The objective is to move towards data-driven decision-making to reverse the declining sales trend.

In response to this need, our project aims to assist the company in creating its own sales-related dashboard using Power BI. This tool will enable the sales director to access and interpret critical data regularly, empowering him to make informed decisions aimed at boosting the company's sales performance.
## Tools

1.MySQL

2.Microsoft Power BI

3.Power Query Editor

3.DAX Language
## Data Analysis Using MySQL

Analysis of different SQL statement on data base

1.To find of all customers records

SELECT * FROM sales.customers;

2.To find total number of customers

SELECT count(*) From sales.customers;

3.To find transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM sales.transactions where market_code='Mark001';

4.To find distrinct product codes that were sold in chennai

SELECT distinct product_code FROM sales.transactions where market_code='Mark001';

5.To find transactions for Chennai market (market code for chennai is Mark002

SELECT * FROM sales.transactions where market_code='Mark002';

6.To find distrinct product codes that were sold in mumbai

SELECT distinct product_code FROM sales.transactions where market_code='Mark002';

7.To find transactions where currency is US dollars

SELECT * from sales.transactions where currency="USD";

8.To find transactions in 2020 join by date table

SELECT sales.transactions.*, sales.date.* FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020;

8.To find transactions in 2019 join by date table

SELECT sales.transactions.*, sales.date.* FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2019;

9.To find total revenue in year 2020,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r";

10.To find total revenue in year 2019,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2019 and sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r";

11.To find total revenue in year 2020, January Month,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.date.month_name="January" and (sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r");

12.To find total revenue in year 2020, February Month,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.date.month_name="February" and (sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r");

13.To find total revenue in year 2019, January Month,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.date.month_name="January" and (sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r");

14.To find total revenue in year 2019, February Month,

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.date.month_name="February" and (sales.transactions.currency="INR\r" or sales.transactions.currency="USD\r");

15.To find total revenue in year 2020 in Chennai

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.transactions.market_code="Mark001";

16.To find total revenue in year 2020 in Mumbai

SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020 and sales.transactions.market_code="Mark002";
## Data Model

![Data Model](https://github.com/JBPANDYA/AtliQ-sales-insights/blob/main/DataModel%20(2).png)

## Dashboard

![Dashboard](https://github.com/JBPANDYA/AtliQ-sales-insights/blob/main/Atliq%20Dashboard.png)
