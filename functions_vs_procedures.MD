# What is the difference between a function and a procedure in MS-SQL?

## differences in a table

| Function                            | Procedure                           |
| ----------------------------------- | ----------------------------------- |
| returns a table variable            | returns a table variable            |
| can be used in a select statement   | can be used in a select statement   |
| can be used in a where statement    | can be used in a where statement    |
| can be used in a having statement   | can be used in a having statement   |
| can be used in a from statement     | can be used in a from statement     |
| can be used in a group by statement | can be used in a group by statement |
| can be used in a order by statement | can be used in a order by statement |

## differences in a 3 sentence summary

- A function is a subprogram that returns a single value.
- A procedure is a subprogram that performs a specific action.
- Functions can be used in a select statement, where as procedures cannot.
- Procedures can be used to execute business logic, where as functions cannot.
