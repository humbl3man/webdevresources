**CREATE TABLE** creates new table


**INSERT INTO** adds a new row to a table


**SELECT** queries data from a table


**UPDATE** edits a row in a table


**ALTER TABLE** change an existing table


**DELETE FROM** deletes rows from a table


**SELECT DISTINCT** return unique values in the result set. It filters out all duplicate values.


The **_** means you can substitute any individual character here without breaking the pattern. 
*For example (se_en will match both seven and se7en)*


**%** is a wildcard character that matches zero or more missing letters in the pattern.

The **BETWEEN** operator is used to filter the result set within a certain range. 

```
  SELECT * FROM movies
  WHERE name BETWEEN 'A' AND 'J';
```

```
  SELECT * FROM movies WHERE year BETWEEN 1990 AND 2000;
```
