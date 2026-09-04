# SQL-Analysis

Projekt testowy: Analiza danych E-commerce w SQL.
Czynności i cele analizy:
1) Sprawdzenie, które kategorie produktów przynoszą największy przychód w danym regionie.
2) Identyfikacja najpopularniejszych metod płatności.
3) Wyznaczenie TOP 5 klientów z największymi wydatkami.
Poniżej znajdują się zapytania SQL odpowiadające na powyższe pytania:

1) SELECT region, SUM(revenue) AS total_revenue
   FROM ecommerce_sales_analytics_5000
   GROUP BY region
   ORDER BY total_revenue DESC;

2) SELECT payment_method, COUNT(payment_method)
   FROM ecommerce_sales_analytics_5000
   GROUP BY payment_method;

3) SECECT customer_id FROM  ecommerce_sales_analytics_5000
   ORDER BY revenue DESC LIMIT 5;я
