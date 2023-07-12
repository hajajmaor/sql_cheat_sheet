# Queries examples

## Select all columns from the customers table

``` sql
Select * FROM customers;
```

## Select only the name and email columns from the customers table

``` sql
SELECT name, email FROM customers;
```

## Select all columns from the customers table where the age is greater than 30

``` sql
Select *FROM customers WHERE age > 30;
```

## Select all columns from the customers table where the name is 'John'

``` sql
Select *FROM customers WHERE name = 'John';
```

## Select all columns from the customers table where the name is 'John' or 'Jane'

``` sql
Select *FROM customers WHERE name IN ('John', 'Jane');
```

## Select all columns from the customers table where the name is not 'John'

``` sql
Select *FROM customers WHERE name != 'John';
```

## Select all columns from the customers table where the name starts with 'J'

``` sql
Select *FROM customers WHERE name LIKE 'J%';
```

## Select all columns from the customers table where the name contains 'oh'

``` sql
Select *FROM customers WHERE name LIKE '%oh%';
```

## Select all columns from the customers table sorted by age in ascending order

``` sql
Select *FROM customers ORDER BY age ASC;
```

## Select all columns from the customers table sorted by age in descending order

``` sql
Select *FROM customers ORDER BY age DESC;
```

## Select all columns from the customers table joined with the orders table on the customer_id column

``` sql
Select *FROM customers JOIN orders ON customers.id = orders.customer_id;
```

## Select all columns from the customers table joined with the orders table on the customer_id column where the order_total is greater than 100

``` sql
Select *FROM customers JOIN orders ON customers.id = orders.customer_id WHERE orders.order_total > 100;
```

## Select all columns from the customers table unioned with the employees table

``` sql
Select *FROM customers UNION ``` sql Select *FROM employees;
```

## Select only the name and email columns from the customers table unioned with the employees table

```sql
SELECT name, email FROM customers UNION SELECT name, email FROM employees;
```