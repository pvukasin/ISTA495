Write a SQL solution to output the 10 least dense countries.



SQL Query:

SELECT country,Cast(REPLACE(population,',','') AS FLOAT) / 
(SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT)) FROM world)
FROM world
ORDER BY Cast(REPLACE(population,',','') AS FLOAT) / 
(SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT)) FROM world) ASC
LIMIT 10



Result:

![p7](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p7.png)