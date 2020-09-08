Write a SQL solution to output the land share value of the wold (that is, the sum of the land area divided by the sum of the population).



SQL Query:

SELECT SUM(CAST(REPLACE(area,',','') AS FLOAT))/
SUM(CAST(REPLACE(population,',','') AS FLOAT))
FROM world

![p12](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p12.png)