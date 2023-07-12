# what is the `row_number` function in SQL?

## explanation

The `row_number` function is a window function that assigns a unique number to each row in a partition. It is often used to create a unique identifier for each row in a table

## example

```sql
select name,
       row_number() over (order by name) as row_number
  from users
```
