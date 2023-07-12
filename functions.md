# MS-SQL functions exmaple

## create functions with input and output params

```sql
CREATE FUNCTION dbo.ufnGetStock
(
@ProductID int)
RETURNS int
AS
BEGIN
    DECLARE @ret int
    SELECT @ret = SUM(p.Quantity)
    FROM Production.ProductInventory p
    WHERE p.ProductID = @ProductID
    GROUP BY p.ProductID
    RETURN @ret
END
GO
```

## Usage of the function

```sql
SELECT dbo.ufnGetStock(1)
```
