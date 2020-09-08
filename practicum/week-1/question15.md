Which countries has the lowest urban population? List the top 10. 


SQL Query:

SELECT country,Cast(REPLACE(population,',','') AS FLOAT) 
FROM world
WHERE Cast(REPLACE(population,',','') AS FLOAT) IS NOT NULL
ORDER BY Cast(REPLACE(population,',','') AS FLOAT) ASC
LIMIT 10



Result:



![p16](/Users/petervukasin/Desktop/ISTA495/ISTA495/practicum/week-1/images/p16.png)