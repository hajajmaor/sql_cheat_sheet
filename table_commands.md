# sample table commands for MS-SQL

## create a table

```sql
CREATE TABLE customers (
    id INT IDENTITY(1,1) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    age INT NOT NULL
);
```

## add index to table

```sql
CREATE INDEX idx_name ON customers (name);
```

## alter a table

```sql
alter table customers
add column address varchar(255) not null;
```

### change column type from varchar 255 to varchar 512

```sql
alter table customers
alter column address varchar(512) not null;
```

### drop a column

```sql
alter table customers
drop column address;
```

## drop a table

```sql
drop table customers;
```

## clear a table

```sql
truncate table customers;
```

## create table with FK not null

```sql
CREATE TABLE addresses(
    id INT IDENTITY(1,1) PRIMARY KEY,
    street VARCHAR(255) NOT NULL,
    city VARCHAR(255) NOT NULL,
    state VARCHAR(255) NOT NULL,
    zip VARCHAR(255) NOT NULL
);
```

```sql
CREATE TABLE customers (
    id INT IDENTITY(1,1) PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    age INT NOT NULL,
    address_id INT NOT NULL,
    CONSTRAINT fk_address_id FOREIGN KEY (address_id) REFERENCES addresses(id)
);
```
