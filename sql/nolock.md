# NOLOCK

The beauty of using `NOLOCK` while using select statement like following is: it improves the overall performance of SQL server, and creates a non-blocking query to the database. What that means is while a complex select statement is executing, other tasks can still run as normal.

```sql
SELECT <expression1>, <expression2>, ... <expression_n>
FROM <tables> WITH (NOLOCK)
```

It is exactly because of `NOLOCK` does not care what state the record is, it should not be used for generating most up-to-date information, not to mention using the generated records as a source of truth to update or modify records.
