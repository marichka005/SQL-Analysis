# SQL-Analysis

Projekt testowy: Analiza danych E-commerce w SQL.
Czynności i cele analizy:
1) Sprawdzenie, które kategorie produktów przynoszą największy przychód w danym regionie.
2) Identyfikacja najpopularniejszych metod płatności.
3) Wyznaczenie TOP 5 klientów z największymi wydatkami.
Poniżej znajdują się rozwiązania SQL odpowiadające na powyższe pytania:

1) SELECT region, SUM(revenue) AS total_revenue
   FROM ecommerce_sales_analytics_5000
   GROUP BY region
   ORDER BY total_revenue DESC;

2) SELECT payment_method, COUNT(payment_method)
   FROM ecommerce_sales_analytics_5000
   GROUP BY payment_method;

3) SECECT customer_id, SUM(revenue) AS total
   FROM  ecommerce_sales_analytics_5000
   GROUP BY customer_id
   ORDER BY total DESC LIMIT 5;
