-- question 1

SELECT rep_name,
coalesce(sum(amount), 0) as revenue
FROM sales
group by rep_name;

-- question 2

select product,
round(avg(amount), 2) as average_amount
from sales
group by product
order by average_amount DESC;

-- question 3

select rep_name,
sum(amount) as total_sales,
count(case when product = 'Phone' then 1 end) as phone_sales,
count(case when amount > 1000 then 1 end) as sales_above_1000
from sales
group by rep_name;

-- question 4

SELECT rep_name,
       SUM(amount) as total
FROM sales
GROUP BY rep_name;

-- question 5

SELECT
  rep_name,
  COUNT(*) AS total_sales,
  COUNT(CASE WHEN product = 'Laptop' THEN 1 END) AS laptops,
  COALESCE(ROUND(SUM(amount), 2), 0) AS revenue,
  COALESCE(ROUND(AVG(amount), 2), 0) AS avg_sale
FROM sales
GROUP BY rep_name
HAVING COUNT(*) >= 2
ORDER BY revenue DESC;
