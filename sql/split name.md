# Split Name

A common task in SQL is to get first name and last name given a full name. Here's couple ways to do it:

### SUBSTRING

```sql
DECLARE @FullName        VARCHAR(100)
SET @FullName = 'John Doe'

SELECT SUBSTRING(@FullName, 1, CHARINDEX(' ', @FullName) - 1) AS [FirstName],
       SUBSTRING(@FullName, CHARINDEX(' ', @FullName) + 1, LEN(@FullName)) AS [LastName]
```

### LEFT & RIGHT

```sql
DECLARE @FullName        VARCHAR(100)
SET @FullName = 'John Doe'

SELECT LEFT(@FullName, CHARINDEX(' ', @FullName) - 1) AS [FirstName],
       RIGHT(@FullName, CHARINDEX(' ', REVERSE(@FullName)) - 1) AS [LastName]
```

### PARSENAME

```sql
DECLARE @FullName        VARCHAR(100)
SET @FullName = 'John Doe'

SELECT PARSENAME(REPLACE(@FullName, ' ', '.'), 2) AS [FirstName],
       PARSENAME(REPLACE(@FullName, ' ', '.'), 1) AS [LastName]
```
