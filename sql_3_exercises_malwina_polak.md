

***TABLE: RESTAURANTS***

Name | Cuisine | Date_Founded
--- | --- | ---
Chipotle |	Mexican	| 7/13/1993
Taco Bell | Mexican	| 3/21/1962
McDonald's |	American |	4/15/1955
Popeye's |	American |	NULL
Panda Express |	Chinese |	1/23/1983

***

***TABLE: CONTINENT***

Cuisine	| Continent
--- | ---
American |	North America
Mexican	 | North America



### ***Part 1:***

1. Show me everything in the RESTAURANTS table.
~~~~ sql
SELECT * FROM RESTAURANT;
~~~~

2. Show me the Names in the table.
~~~~ sql
SELECT Name FROM RESTAURATS; 
~~~~
3. Show me the unique Cuisines.
~~~~ sql
SELECT DICTINCT CUISINE FROM CONTINENT;
~~~~
4. Show me 3 rows of data.
~~~~ sql
SELECT DICTINCT CUISINE FROM CONTINENT LIMIT3;
~~~~
5. Sort the restaurant names alphabetically.
~~~~ sql
SELECT Name FROM RESTAURANTS ORDER BY Name ASC;
~~~~
6. Exclude the rows with NULL values.
~~~~ sql
SELECT * FROM REASTAURANT WHERE Date_Founded IS NOT NULL;
~~~~
7. What is the number of rows without NULL values?
~~~~ sql
SELECT COUNT(Date_Founded) FROM REASTAURANT WHERE Date_Founded IS NULL;
~~~~
8. Show me all restaurants founded between 1/1/1950 and 1/1/1970.
~~~~ sql
SELECT Name FROM REASTAURANT WHERE Date BETWEEN '1-1-1950' AND '1-11970';
~~~~
9. Out of all the restaurants, show me all restaurants that start with the letter P.
~~~~ sql
SELECT Name FROM REASTAURANT WHERE Name LIKE 'P%';
~~~~
### ***Part 2:***

10. In the RESTAURANTS table, how many restaurants are there of each type of cuisine?
~~~~ sql
SELECT, Name, COUNT(DISTINCT(Cousine)) FROM RESTAURANTS;
~~~~
11. Rename the new column you created as Num_Cuisine.
~~~~ sql
SELECT Name, COUNT(DISTINCT(Cousine)) AS "Num_Cuisine" FROM RESTAURANTS;

~~~~
12. For every restaurant, show me the continent that its cuisine is from. If the continent isn't in the CONTINENT table, don't show the data.
~~~~ sql
SELECT * FROM RESTAURANTS RIGHT JOIN CONTINENT ON Cuisine.RESTAURANTS = Cuisine.CONTINENT;
~~~~
13. For every restaurant, show me the continent that its cuisine is from. If the continent isn't in the CONTINENT table, still show the data.
~~~~ sql
SELECT * FROM RESTAURANTS LEFT JOIN CONTINENT ON Cuisine.RESTAURANTS = Cuisine.CONTINENT;

~~~~
14. Show me restaurants that are Mexican or Chinese.
~~~~ sql
SELECT * FROM RESTAURANTS WHERE Cuisine IS 'Mexican' OR 'Chinese';
~~~~
15. Show me restaurants that are not American.
~~~~ sql
SELECT * FROM RESTAURANTS WHERE Cuisine NOT 'American';
~~~~
16. Output the name of the Mexican restaurant that was founded most recently.
~~~~ sql
SELECT Name FROM RESTAURANTS WHERE Cuisine IS 'Mexican' ORDER BY Date_Founded DESC  limit1;
~~~~
