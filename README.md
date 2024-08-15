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
Separate arguments with comma if needed

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

### AND/OR

WHERE + AND - both must be true
WHERE + OR - one must be true 
AND is proceeded first in query! 
When more than two conditions -> Use parentheses and make them two 


### BETWEEN ... AND ...

Syntax:
...
WHERE column_name BETWEEN/NOT BETWEEN number/string AND number2/string2 
eg. date 'YYYY-MM-DD' - you can add time (midnight is default time)

### IN

WHERE column_name IN (value1,...)

### LIKE

_ - any character
% - any sequence of chars
WHERE column_name LIKE/NOT LIKE 'A%' (string is case sensitive) ILIKE (a%) (case insensitive)

## Commenting & Aliases
"--" - for single line
/* ...*/ - for many lines

### AS

To change column name in a query output
e.g.
...
COUNT (*) AS number_of_customers
...

## Aggregate functions

e.g SUM,MIN,MAX,AVG (you can't list other column than aggregated)
Can list many agg functions (separate by comma)

## GROUP BY

Immediately after FROM or WHERE(if it's present)
Syntax:
SELECT
column_name,
SUM(column_name2)
FROM table_name
WHERE...
GROUP BY column_name

Every column here should be in agg functions or in GROUP BY clause

You can ORDER BY agg function as well here.

### HAVING

Filter groupings only by aggregations 
e.g:
...
GROUP BY...
HAVING COUNT(*) > 4000 (AND/OR etc. is possible)