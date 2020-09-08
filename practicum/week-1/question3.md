Write a SQL solution to output the population density (population per unit area) of all countries.

SQL Query:


SELECT country, Cast(REPLACE(population,',','') AS INT) / NULLIF(CAST(REPLACE(area,',','') AS INT),0) 
FROM world



Result:

![p3](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p3.png)