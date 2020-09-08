Write a SQL solution to output the 10 countries who have the highest land share.



SQL Query:

SELECT country,Cast(REPLACE(area,',','') AS FLOAT) / 
CAST(REPLACE(population,',','') AS FLOAT)
FROM world
ORDER BY Cast(REPLACE(area,',','') AS FLOAT) / 
CAST(REPLACE(population,',','') AS FLOAT) DESC
LIMIT 10



Result:

![p10](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p10.png)