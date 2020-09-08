Write a SQL solution to output the 10 most dense countries.



SQL Query:

SELECT country,Cast(REPLACE(population,',','') AS FLOAT) / 
(SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT)) FROM world)
FROM world
ORDER BY Cast(REPLACE(population,',','') AS FLOAT) / 
(SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT)) FROM world) DESC
LIMIT 10



Result:



![p6](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p6.png)