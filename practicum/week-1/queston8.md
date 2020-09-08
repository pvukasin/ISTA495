Write a SQL solution to output the population density of the world. That is, the sum of the population 
of all the countries divided by the sum of the land area of all the countries. 



SQL Query:

SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT))/
SUM(CAST(REPLACE(area,',','') AS FLOAT))
FROM world



Result:

![p8](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p8.png)