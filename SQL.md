## Commands
  SELECT
  FROM
  JOIN
  WHERE
  GROUP BY
  HAVING
  ORDER BY
  LIMIT

Mnemonic: Sweaty feet will give horrible odors

## Keywords
  * DISTINCT - returns unique results
  * BETWEEN a AND b - limits the range of outputs
  * LIKE - pattern searches in the column text
  * IN (a,b,c) - Checks if value is in given sequence
  * "abc%", "%abc", "%abc%" - checks if value is a substring

## Aggregate functions
  * COUNT
  * SUM
  * AVG
  * MIN / MAX

## Joins
  * INNER JOIN - records that match both tables
  * LEFT (OUTER) JOIN - All records on left, matched records on right
  * RIGHT (OUTER) JOIN - All records on right, matched records on left
  * FULL (OUTER) JOIN - All records where there is a match in either left or right

![SQL JOINS](./images/SQL_joins.png)

## Subquery
SQL queries have a return value so we can use a whole query as a search term 

General Format

SELECT
  Name
FROM (
  SELECT
    Name, Director
  FROM
    Movies
  WHERE
    Yr = 1997
  ) AS subquery
WHERE
  Director = Steven Spielberg

## Notes
Can't use WHERE and GROUP BY in conjunction

## Resources
  [SQLBolt SQL tutorial](https://sqlbolt.com/)
