# What is `view` in SQL?

## Explanation

A `view` is a virtual table that is created by a query. It can be used to simplify complex queries, and to hide the underlying table structure from the user.

## Example

```sql
create view user_logins_view as
  select
    row_number() over (
        partition by user_id order by created_at
    ) as row_number,
    user_id,
    created_at
      from user_logins
```

## drop view

```sql
drop view user_logins_view
```

## overwrite view

```sql
create or replace view user_logins_view as
  select
    row_number() over (
        partition by user_id order by created_at
    ) as row_number,
    user_id,
    created_at
      from user_logins
```
