# Data Analysis Project on Sales Insight of a Company Using Power BI     

We have a case study in this project that is based on a computer hardware company that is dealing with issues in a rapidly changing market. The sales director chooses to invest in a data analysis project and plans to create a Power BI dashboard that will provide him with real-time sales data.


## Acknowledgements

 - [Power BI Templates](https://docs.microsoft.com/en-us/dynamics365/sales-enterprise/configure-sales-template-apps)
 - [Power BI release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/april18/power-bi/insights-apps/sales-insights#:~:text=The%20Power%20BI%20for%20Sales,to%20focus%20their%20attention%20on.)
 - [Power BI used for Sales Insight](https://powerbi.microsoft.com/en-us/landing/sales/)

  
## Problem Statement

To provide decision assistance to the sales team by unlocking previously unseen sales insights and automating them to decrease manual data collecting time.

  
## Instructions to setup mysql on your local computer

1.) To install MySQL on your local computer, follow the steps in this video: https://www.youtube.com/watch?v=WuBcTJnIuzo 

2.) The db dump.sql file above contains a SQL database dump. Download the db dump.sql file to your local computer and import it according to the tutorial video's instructions.
  
## Data Analysis Using SQL

1.) Show all customer records
```
SELECT * FROM customers;
```
2.) Show total number of customers
```
SELECT count(*) FROM customers;
```
3.) Show transactions for Chennai market (market code for chennai is Mark001
```
SELECT * FROM transactions where market_code='Mark001';
```
4.) Show distrinct product codes that were sold in chennai
```
SELECT distinct product_code FROM transactions where market_code='Mark001';
```
5.) Show transactions where currency is US dollars
```
SELECT * from transactions where currency="USD"
```
6.) Show transactions in 2020 join by date table
```
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
```
7.) Show total revenue in year 2020,
```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
```
8.) Show total revenue in year 2020, January Month,
```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");
```
9.) Show total revenue in year 2020 in Chennai
```
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
```
## Data Analysis Using Power BI

1.) Formula to create norm_amount column

```
= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)  
```


## Screenshots
Sales Data Dashboard
![Data Dashboard](https://i.postimg.cc/pphGnysr/1.png) 
![](https://i.postimg.cc/hJrpqmty/2.png)
![](https://i.postimg.cc/H8J25P4R/3.png)
![](https://i.postimg.cc/PNFVx1z0/4.png)

  
## Feedback

If you have any feedback, please reach out to us at anurag.priyadarshi1999@gmail.com

  
## Authors

- [@Anurag-Priyadarshi07](https://github.com/Anurag-Priyadarshi07/Anurag-Priyadarshi07)

  
# Hi, I'm Anurag Priyadarshi! 👋

  
## 🚀 About Me
Wanted to be a Frontend Developer and Business Analyst.

  
## 🛠 Skills
Javascript, HTML, CSS, ReactJS, Bootstrap, Python, C/C++, MySQL, SQL, Power BI, Microsoft Excel

  
## 🔗 Links

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white) (https://www.linkedin.com/in/anurag-priyadarshi-9b97a710a/](https://www.linkedin.com/)]
