Wich countries send the most migrants? List the top 10.

SQL Query:

SELECT country,Cast(REPLACE(migrants,',','') AS FLOAT)
FROM world
ORDER BY Cast(REPLACE(migrants,',','') AS FLOAT) ASC
LIMIT 10



Result:

![p13](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p13.png)