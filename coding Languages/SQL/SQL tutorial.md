# SQL tutorial

Day|Title
---|-----
0 |  **[table opereation](./general-Information/General.md)**

## DISTINCT /GROUP BY

In SQL, both the DISTINCT keyword and the GROUP BY clause are used to retrieve unique values from a result set, but they function differently.
DISTINCT: The DISTINCT keyword is used to eliminate duplicate rows from the result set.
GROUP BY: The GROUP BY clause is used to group rows based on one or more columns. It is typically used in combination with aggregate functions like SUM, COUNT... etc

``` sql
SELECT DISTINCT column1, column2
FROM table;

SELECT column1, SUM(column2)
FROM table
GROUP BY column1;
```

## SQL Functions

COUNT(), MAX(), MIN(), SUM(), AVG()

## Operators in The WHERE

| Operator   | Description                                    |
|------------|------------------------------------------------|
| =          | Equal to                                       |
| <> or !=   | Not equal to                                   |
| <          | Less than                                      |
| >          | Greater than                                   |
| <=         | Less than or equal to                          |
| >=         | Greater than or equal to                       |
| BETWEEN    | Between a range of values                      |
| LIKE       | Pattern matching using wildcards               |
| IN         | Matches any values in a list or subquery        |
| NOT IN     | Does not match any values in a list or subquery |
| IS NULL    | Checks for a NULL value                         |
| IS NOT NULL| Checks for a non-NULL value                     |
| AND        | Logical AND operator                            |
| OR         | Logical OR operator                             |
| NOT        | Logical NOT operator                            |



