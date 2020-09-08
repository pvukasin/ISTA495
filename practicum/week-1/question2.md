Write a SQL solution to output all countries that either have an area bigger than 2 million square km or a population of more than 30 million. The solution should output 
only the followings: country, population and area.



SQL Query:

SELECT country,population,area FROM world
WHERE CAST(REPLACE(area,',','') AS INT) > 2000000
or CAST(REPLACE(population,',','') AS INT) > 30000000;

![p2](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p2.png)