# SQLPetProject
Hands-on project using PostgreSQL(ver.16) DBMS (Database Management System) and pgAdmin 4 GUI 

## Database creation
Right-click on pg Admin Databases option and choose "Create"

## To insert data from source file
Right click on Schemas and choose Query Tool. Then open your file and execute it - press "play button" 

## SELECT
Remember about comma between column names (last argument without it!)
<b>SELECT 
column1,...
FROM 
table name</b>

### SELECT DISTINCT
Get first occurence only. 
<b>Distinct in terms of all selected columns!</b>

## ORDER BY
You can use a number of column instead of it's name(not a best practice)
DESC - descending
ASC - ascending (default)

## LIMIT
Always at the very end of query
e.g LIMIT 3

## COUNT()
COUNT(*) and COUNT(columnName) results can be different because (columnName) don't count null values.
Syntax example:
SELECT
COUNT(*)
FROM 
table_name

### COUNT(DISTINCT)

Syntax:
SELECT
COUNT(DISTINCT column_name)
FROM 
table_name

## WHERE

Always immediately after FROM.
Strings are case sensitive!
SYNTAX:
...
FROM table_name
WHERE condition (strings in '')
Operators:
is null, is not null, != and <> + arithmetic