Which countries receive the most migrants? List the name and the migrants number of the top 10.



SQL Query:

SELECT country,Cast(REPLACE(migrants,',','') AS FLOAT) 
FROM world
WHERE Cast(REPLACE(migrants,',','') AS FLOAT) IS NOT NULL
ORDER BY Cast(REPLACE(migrants,',','') AS FLOAT) DESC
LIMIT 10

Result:

![p14](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p14.png)