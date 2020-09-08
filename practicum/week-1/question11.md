Write a SQL solution to output the 10 countries who have the lowest land share.



SQL Query:

SELECT country,Cast(REPLACE(area,',','') AS FLOAT) / 
CAST(REPLACE(population,',','') AS FLOAT)
FROM world
ORDER BY Cast(REPLACE(area,',','') AS FLOAT) / 
CAST(REPLACE(population,',','') AS FLOAT) ASC
LIMIT 10





Result:



![p11](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p11.png)

