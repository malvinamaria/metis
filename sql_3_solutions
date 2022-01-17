# SQL 3 Exercises Solutions



***TABLE: RESTAURANTS***

Name | Cuisine | Date_Founded
--- | --- | ---
Chipotle | Mexican | 7/13/1993
Taco Bell | Mexican | 3/21/1962
McDonald's | American | 4/15/1955
Popeye's | American | NULL
Panda Express | Chinese | 1/23/1983

***

***TABLE: CONTINENT***

Cuisine | Continent
--- | ---
American | North America
Mexican | North America



### ***Part 1:***

1. Show me everything in the RESTAURANTS table.
~~~~ sql
SELECT *
FROM RESTAURANTS
~~~~
2. Show me the Names in the table.
~~~~ sql
SELECT Name
FROM RESTAURANTS
~~~~
3. Show me the unique Cuisines.
~~~~ sql
SELECT DISTINCT Cuisine
FROM RESTAURANTS
~~~~
4. Show me 3 rows of data.
~~~~ sql
SELECT *
FROM RESTAURANTS
LIMIT 3
~~~~
5. Sort the restaurant names alphabetically.
~~~~ sql
SELECT *
FROM RESTAURANTS
ORDER BY Name
~~~~
6. Exclude the rows with a NULL date founded.
~~~~ sql
SELECT *
FROM RESTAURANTS
WHERE Date_Founded IS NOT NULL
~~~~
7. What is the number of rows without a NULL date founded?
~~~~ sql
SELECT COUNT(*)
FROM RESTAURANTS
WHERE Date_Founded IS NOT NULL
~~~~
8. Show me all restaurants founded between 1/1/1950 and 1/1/1970 (inclusive, on both ends).
~~~~ sql
SELECT *
FROM RESTAURANTS
WHERE Date_Founded BETWEEN '1/1/1950' AND '1/1/1970'
~~~~
9. Out of all the restaurants, show me all restaurants that start with the letter P.
~~~~ sql
SELECT *
FROM RESTAURANTS
WHERE NAME LIKE 'P%'  -- LIKE is case insensitive
~~~~
### ***Part 2:***

10. In the RESTAURANTS table, how many restaurants are there of each type of cuisine?
~~~~ sql
SELECT 
    Cuisine, 
    COUNT(Name)
FROM RESTAURANTS
GROUP BY Cuisine
~~~~
11. Rename the new column you created as Num_Cuisine.
~~~~ sql
SELECT 
    Cuisine, 
    COUNT(Name) AS Num_Cuisine
FROM RESTAURANTS
GROUP BY Cuisine
~~~~
12. For every restaurant, show me the continent that its cuisine is from. If the continent isn't in the CONTINENT table, don't show the data.
~~~~ sql
SELECT 
    r.Name, 
    c.Continent
FROM RESTAURANTS r 
INNER JOIN CONTINENT c 
    ON r.Cuisine = c.Cuisine
~~~~
13. For every restaurant, show me the continent that its cuisine is from. If the continent isn't in the CONTINENT table, still show the data.
~~~~ sql
SELECT 
    r.Name, 
    c.Continent
FROM RESTAURANTS r 
LEFT JOIN CONTINENT c 
    ON r.Cuisine = c.Cuisine
~~~~
14. Show me restaurants that are Mexican or Chinese.
~~~~ sql
SELECT 
    Name,
    Cuisine
FROM RESTAURANTS
WHERE Cuisine IN ('Mexican', 'Chinese')
~~~~
15. Show me restaurants that are not American.
~~~~ sql
SELECT
    Name,
    Cuisine
FROM RESTAURANTS
WHERE Cuisine <> 'American'
~~~~
16. Output the name of the Mexican restaurant that was founded most recently.
~~~~ sql
SELECT Name
FROM RESTAURANTS
WHERE Cuisine = 'Mexican'
ORDER BY Date_Founded DESC
LIMIT 1
~~~~
