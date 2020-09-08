Write a SQL solution to output the population of the world.

SQL Query:

SELECT SUM(CAST(REPLACE(population,',','') AS INT))
FROM world





Result:

![p4](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p4.png)