# DATA_ANALYSYS-sales_insight-
Modeling, cleaning, initializing and analyzing data to extract insights about company sales and growth
, influential and declining markets using Workbench, Power Pi,ETL

![AS](https://github.com/abduallheid/DATA_ANALYSYS-sales_insight-/edit/main/pw.png)

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

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
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`



DATA soruce : ATLIQ HARD WARE c.


## Here report example

[embed] https://app.powerbi.com/groups/me/reports/2227add3-fda5-495d-baa8-d7e00fc5a44d?ctid=bc614756-3d44-40dc-a3b9-ac7117ae1e50&pbi_source=linkShare [/embed]
