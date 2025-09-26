# 📊 PostgreSQL Sales Analysis  

## 📌 Project Overview  
This project analyzes an **E-Commerce Sales Dataset** using PostgreSQL.  
The goal is to extract **KPIs**, analyze trends, and understand customer & market performance.  

---

## ✅ Key KPIs  

1. **Total Sales** – Overall revenue  
2. **Total Customers** – Unique customer count  
3. **Average Order Number** – Avg order lines per transaction  
4. **Monthly Sales Trend** – Revenue growth by month  
5. **Top 10 Cities** – Cities with highest sales  
6. **Top 10 Customers** – Customers contributing the most revenue  
7. **Shipped Orders** – Count of shipped orders  
8. **Orders by Status** – Revenue & count split by order status  

---

## 🗄️ SQL Queries  

All queries are written in **PostgreSQL**. Example:  

```sql
-- Total Sales
SELECT SUM(SALES) AS TOTAL_SALES 
FROM SALES;

-- Monthly Sales Trend
SELECT TO_CHAR(ORDERDATE, 'MM-YYYY') AS MONTHLY_SALE, 
       SUM(SALES) AS SALES
FROM SALES
GROUP BY MONTHLY_SALE
ORDER BY MONTHLY_SALE;# SQL-REPORT-FILES-
