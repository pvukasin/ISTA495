Write a SQL solution to output the land share of all the countries. 
Land share = land area divided by the population

SQL Query:

SELECT country,Cast(REPLACE(area,',','') AS FLOAT) / 
CAST(REPLACE(population,',','') AS FLOAT)
FROM world



Result:

![p9](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p9.png)