## Queries and manipulation

**CREATE TABLE** creates new table


**INSERT INTO** adds a new row to a table


**SELECT** queries data from a table


**UPDATE** edits a row in a table


**ALTER TABLE** change an existing table


**DELETE FROM** deletes rows from a table


**SELECT DISTINCT** return unique values in the result set. It filters out all duplicate values.


The ```_``` means you can substitute any individual character here without breaking the pattern. 
*For example (se_en will match both seven and se7en)*


```%``` is a wildcard character that matches zero or more missing letters in the pattern.

The **BETWEEN** operator is used to filter the result set within a certain range. 

```
SELECT * FROM movies
WHERE name BETWEEN 'A' AND 'J';
```

```
SELECT * FROM movies WHERE year BETWEEN 1990 AND 2000;
```

**OR** is an operator that filters the result set to only include rows where either condition is true. 

**ORDER BY** is a clause that indicates you want to sort the result set by a particular column either alphabetically or numerically.

**ASC** low to high
**DESC** high to low

**LIMIT** is a clause that lets you specify the maximum number of rows the result set will have. Here, we specify that the result set can not have more than three rows.

```
SELECT * FROM movies
ORDER BY imdb_rating DESC
LIMIT 3;
```

### Aggregate Functions
_Aggregate functions_ compute a single result from a set of input values. For instance, when we need the sum or average of a particular column, we can use aggregate functions to quickly compute it for us.

```
SELECT COUNT(*) FROM fake_apps;
```

**COUNT()** is a function that takes the name of a column as an argument and counts the number of rows where the column is not **NULL**. Here, we want to count every row so we pass "*" as an argument.

**GROUP BY** is a clause in SQL that _is only used with aggregate functions_. It is used in collaboration with the SELECT statement to arrange identical data into groups.

```
SELECT price, COUNT(*) FROM fake_apps
GROUP BY price;
```

**SUM()** is a function that takes the name of a column as an argument and returns the sum of all the values in that column. Here, it adds all the values in the downloads column.

```
SELECT SUM(downloads) FROM fake_apps;
```

You can find the largest value in a column by using MAX().

**MAX()** is a function that takes the name of a column as an argument and returns the largest value in that column. Here, we pass downloads as an argument so it will return the largest value in the downloads column.

```
SELECT MAX(downloads) FROM fake_apps;
```

Similar to MAX(), SQL also makes it easy to return the smallest value in a column by using the MIN() function.

**MIN()** is a function that takes the name of a column as an argument and returns the smallest value in that column. Here, we pass downloads as an argument so it will return the smallest value in the downloads column.

```
SELECT MIN(downloads) FROM fake_apps;
```

SQL uses the AVG() function to quickly calculate the average value of a particular column.

The **AVG()** function works by taking a column name as an argument and returns the average value for that column.

```
SELECT AVG(downloads) FROM fake_apps;
```

By default, SQL tries to be as precise as possible without rounding. We can make the result set easier to read using the ROUND() function.

**ROUND()** is a function that takes a column name and an integer as an argument. It rounds the values in the column to the number of decimal places specified by the integer. Here, we pass the column AVG(downloads) and 2 as arguments. SQL first calculates the average for each price and then rounds the result to two decimal places in the result set.

```
SELECT price, ROUND(AVG(downloads), 2) FROM fake_apps
GROUP BY price;
```
