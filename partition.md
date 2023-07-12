# What is the `partition` clause in SQL?

## Explanation

The `partition` clause is used to divide the rows in a table into groups. It is used in conjunction with window functions to perform calculations on each group

## Example

```sql
select
  row_number() over (
        partition by user_id order by created_at
    ) as row_number,
  user_id,
  created_at
    from user_logins
```

### Query explanation

The `partition by user_id` clause divides the rows in the `user_logins` table into groups based on the `user_id` column. The `row_number` function is then applied to each group, and the results are returned in a single table
