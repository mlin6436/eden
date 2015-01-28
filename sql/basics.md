# Basics

### Basic SQL statement

```sql
-- select result with the given conditions
SELECT <expression1>, <expression2>, ... <expression_n>,
       aggregate_function (expression)
FROM <tables>
WHERE <conditions>
GROUP BY <expression1>, <expression2>, ... <expression_n>
HAVING <condition>;

-- insert a single line of record
INSERT INTO <table_name>
(<column1>, <column2>, ... <columnn>)
VALUES
(<expression1>, <expression2>, ... <expression_n>);

-- insert multiple records using select statement
INSERT INTO <table_name>
(<column1>, <column2>, ... <columnn>)
SELECT <expression1>, <expression2>, ... <expression_n>
FROM <source_tables>
WHERE <conditions>;
```

### JOIN & APPLY

[This](http://www.mssqltips.com/sqlservertip/1958/sql-server-cross-apply-and-outer-apply/) is a good source to explore the possibilities.

### Alter

```sql
-- add a column
ALTER TABLE <table_name>
ADD <column_name1> <datatype1> <constraint1>

-- alter a column datatype
ALTER TABLE <table_name>
ALTER COLUMN <column_name1> <datatype1> <constraint1>

-- drop a column
ALTER TABLE <table_name>
DROP COLUMN <column_name1> <datatype1>
```

### Functions

```sql
-- select a random row: NEWID()
SELECT TOP 1 <column_name1> FROM <table_name>
ORDER BY NEWID()

-- get sum of a certain column: SUM
SELECT SUM(<column_name1>) AS "result"
FROM <table_name>
GROUP BY <column_name2>

-- get the number of records: COUNT
SELECT COUNT(*) AS "Number of records"
FROM <table_name>

-- get minimum value record for a given column: MIN
SELECT MIN(column_name1) AS "Lowest number"
FROM <table_name>

-- get maximum value record for a given column: MAX
SELECT MAX(column_name1) AS "Highest number"
FROM <table_name>
```

### Conversion

```sql
-- integer to string
SELECT CAST(@i AS VARCHAR) FROM <table_name>

-- string to integer
SELECT CAST(@s AS INT) FROM <table_name>
Or
SELECT CONVERT(INT, @s) FROM <table_name>

-- replace substring inside string
update <table_name> set <column_name1> = replace(<column_name1>,'<old_pattern>','<new_pattern>') where <column_name1> like '%<old_pattern>%'

-- trim string leading or trailing space
SELECT TRIM(' sample ')
Or
SELECT LTRIM(RTRIM(' sample '))
```

### Operation

```sql
-- disconnect all users (or set database to offline)
ALTER DATABASE <database_name> SET SINGLE_USER WITH ROLLBACK IMMEDIATE
```
