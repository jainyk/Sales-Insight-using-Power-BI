# Sales Insight using Power BI
 This project uses SQL database to analyze and visualize through Power BI

## Introduction
PowerBI is a tool like MS-excel which is much easier to use. It is used for analysis and visualization with a simple to use interface.
It runs it's queries using DAX (Data Analysis Expression). PowerBI is steroid on excel. 
It provides many features like publishing a report, viewing dashboard and report on app, loading the data in various formats like excel, text/csv, sql, powerBI dataset etc.

## Dataset description 
We have a sql dataset where we have details like sales data, sales description, sales market and sales products.
Below are some of the queries which we can run on SQL workbench to have a brief view of dataset:
1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`

## PowerBI steps
* Start importing the data by clicking on 'Get Data' option and from that select SQL server option.
* On the left we have 3 option i.e, Report, Data and Models (this basically shows the relationship between different tables).
* On clicking transform data it will launch a powerBI query editor where we can do data cleaning and transformation.
* On the home screen of report section, this is the place where we start our visualization part. On the center we have canvas and on the right we have filters, vislualization      and fields.
* In total we have 3 pages named key insights, profit analysis and performance insights. 
* Below GIF represent key sights in different years. We can click on various options of revenue by markets, sales quantity by markets etc to look at their respective stats. 
<img src="https://github.com/jainyk/Sales-Insight-using-Power-BI/blob/main/img/key_insight_gif.gif"/>

* Below GIF represents profit analysis in different years.
<img src="https://github.com/jainyk/Sales-Insight-using-Power-BI/blob/main/img/profit_analysis_gif.gif"/>

* Below GIF represents performance insights in different years.
<img src="https://github.com/jainyk/Sales-Insight-using-Power-BI/blob/main/img/performance_gif.gif"/>
* PowerBI also allow you to publish report. There is an option called publish which publishes report on cloud. The only precondition is that we need have a working mail account. 

