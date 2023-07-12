# How to create and use Procedures in MS-SQL

## Create a procedure with input and output params

```sql
CREATE PROCEDURE dbo.uspGetStock
(
@ProductID int,
@Stock int OUTPUT
)
AS
BEGIN
    SELECT @Stock = SUM(p.Quantity)
    FROM Production.ProductInventory p
    WHERE p.ProductID = @ProductID
    GROUP BY p.ProductID
END
GO
```

## usage of the procedure

```sql
DECLARE @Stock int
EXEC dbo.uspGetStock @ProductID = 1, @Stock = @Stock OUTPUT
SELECT @Stock
```
