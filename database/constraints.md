### <a name="database-constraints"></a>Constraints

Reference: [Database SQL Language Reference](https://docs.oracle.com/cd/B28359_01/server.111/b28286/clauses002.htm)

Use a **constraint** to define an **integrity constraint** —- a rule that restricts the values in a database.

In SQL, we have the following constraints:

`NOT NULL Constraint`: Allows or disallows inserts or updates of rows containing a null in a specified column.

`UNIQUE Constraint`: Prohibits multiple rows from having the same value in the same column or combination of columns but allows some values to be null.

`PRIMARY KEY Constraint`: Combines a NOT NULL constraint and a unique constraint. It prohibits multiple rows from having the same value in the same column or combination of columns and prohibits values from being null.

`Foreign Key Constraint`: Designates a column as the foreign key and establishes a relationship between the foreign key and a primary or unique key, called the referenced key.

`Check Constraint`: Requires a database value to obey a specified condition.

`REF Constraint`: Dictates types of data manipulation allowed on values in a REF column and how these actions affect dependent values. In an object-relational database, a built-in data type called a REF encapsulates a reference to a row object of a specified object type. Referential integrity constraints on REF columns ensure that there is a row object for the REF.
