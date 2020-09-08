Wite a SQL solution to output the population share (population of the country divided by the population of the world) of the countires.

SQL Query:

SELECT country,Cast(REPLACE(population,',','') AS FLOAT) / 
(SELECT SUM(CAST(REPLACE(population,',','') AS FLOAT)) FROM world)
FROM world



Result:

![p5](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p5.png)