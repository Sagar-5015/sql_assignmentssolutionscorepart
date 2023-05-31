# sql_assignmentssolutionscorepart
=============================================================================================================================
Q1.Ans:-  select * from city where countrycode = 'USA' and population > 100000;
=============================================================================================================================
Q2.Ans:-  select name from city where countrycode = 'USA' and population > 120000;
===============================================================================================================================
Q3.Ans:-  select * from city;
==============================================================================================================================
Q4.Ans:-  select * from city where id = '1661';
==============================================================================================================================
Q5.Ans:-  select * from city where countrycode = 'JPN';
==============================================================================================================================
Q6.Ans:-  select name from city where countrycode = 'JPN';
=============================================================================================================================
Q7.Ans:- select city,state from station;
=============================================================================================================================
Q8.Ans:- select distinct(City) from station where id % 2 = 0;
=============================================================================================================================
Q9.Ans:- select count(City) - count(distinct(City)) as difference from station;
============================================================================================================================
Q10.Ans:- (select City, length(City) as length from station order by length(City) asc, City asc limit 1)
union
(select City, length(City) as length from station order by length(City) desc, City desc limit 1);
============================================================================================================================
Q11.Ans:- select distinct city from station where left(city,1) in ('a','e','i','o','u');
============================================================================================================================
Q12.Ans:- select distinct city from station where right(city,1) in ('a','e','i','o','u');
==============================================================================================================================
Q13.Ans:- select distinct city from station where left(city,1) not in ('a','e','i','o','u');
==============================================================================================================================
Q14.Ans:- select distinct city from station where right(city,1) not in ('a','e','i','o','u');
============================================================================================================================
Q15.Ans:- select distinct city from station where left(city,1) not in ('a','e','i','o','u') or right(city,1) not in ('a','e','i','o','u');
=============================================================================================================================
Q16.Ans:- select distinct city from station where left(city,1) not in ('a','e','i','o','u') or right(city,1) not in ('a','e','i','o','u');
===========================================================================================================================
Q17.Ans:- (select p.product_id, p.product_name
from product p
inner join sales s on p.product_id = s.product_id 
where s.sale_date >= '2019-01-01' and s.sale_date <= '2019-03-31')
EXCEPT
(select p.product_id, p.product_name
from product p
inner join sales s on p.product_id = s.product_id 
where s.sale_date < '2019-01-01' or s.sale_date > '2019-03-31');
===========================================================================================================================
Q18.Ans:- select distinct(author_id) as id from views where author_id = viewer_id order by author_id asc;
===========================================================================================================================
Q19.Ans:- select round((select count(*) from delivery where order_date = customer_pref_delivery_date)/count(*)*100,2) as immediate_delivery_percentage from delivery;
======================================================================================================================================================================
Q20.Ans:- 




