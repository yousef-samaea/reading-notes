# SQL:
or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, & thers alot kinf of like: "SQLite, MySQL, Postgres, Oracle and Microsoft SQL" & All of them support the common SQL language standard.


To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries.
A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned.

if we want to filter certain results from being returned, we need to use a WHERE clause in the query and we cane make
More complex clauses can be constructed by joining numerous AND or OR logical keywords.

sometimes we need to convenient way to discard rows that have a duplicate column value by using the DISTINCT,
and sometimes we need to sort some results by a given column in ascending or descending order using the ORDER BY clause 
and we cane use LIMIT and OFFSET clauses,The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.

and Using the JOIN clause in a query, we can combine row data across two separate tables using this unique key. The first of the joins that we will introduce is the INNER JOIN

INNER JOIN is a process that matches rows from the first table and the second table which have the same key to create a result row with the combined columns from both tables.
....................................................................................................................................................................................................................................................................
# DATABASE

In SQL thre is something cals  the database schema is what describes the structure of each table, and the datatypes that each column of the table can contain.

and if we want to insert data we need to use an INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert.

and if we want to UPDATE data we need to use an UPDATE statement The statement works by taking multiple column/value pairs,
and applying those changes to each and every row that satisfies the constraint in the WHERE clause.

and if we want to DELETE data we need to use an DELETE statement which describes the table to act on, and the rows of the table to delete through the WHERE clause.

and if we want to CREATE TABLE we need to use an CREATE TABLE statement The structure of the new table is defined by its table schema, which defines a series of columns.

and if we want to ALTER TABLE we need to use an ALTER TABLE statement The syntax for adding a new column is similar to the syntax when creating new rows in the CREATE TABLE statement.

and if we want to DROP TABLE we need to use an DROP TABLE statement Like the CREATE TABLE statement, the database may throw an error if the specified table does not exist, and to suppress that error, you can use the IF EXISTS clause.




