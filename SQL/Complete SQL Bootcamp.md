# Complete SQL Bootcamp
Created 22 Sep 2020
My Notes for [The Complete SQL Bootcamp](https://www.udemy.com/course/the-complete-sql-bootcamp/) by Jose Portilla on Udemy.

## Statement Fundamentals
### SELECT
* retrieves info from the db
* capitalise SQL keywords
* `SELECT c1, c2 FROM table_name`
* `*` for all columns
* columns do not need to be in order
* tables can be found in Schemas

### SELECT DISTINCT
* to list distinct unique values

### COUNT
* returns the number of input rows of a query
* needs parenthesis as it is a function
* ` SELECT COUNT (DISTINCT rating) FROM film;`

### SELECT WHERE
* specify conditions for query
* `SELECT c1, c2 FROM table_name WHERE condition`
* comparison operators (+,- etc.)
* logical operators (AND OR NOT)

### ORDER BY
* to sort rows on a column value ASC/DESC
* ` SELECT COUNT (DISTINCT rating) FROM film ORDER BY col_1 ASC;`
* can sort by columns that are not selected

### LIMIT
* limit the number of rows for a query
* last command to be executed
* ` SELECT COUNT (DISTINCT rating) FROM film ORDER BY col_1 ASC LIMIT 5;`

### BETWEEN
* match a value against a range
* can use `NOT BETWEEN`
* tags with WHERE
* dates must be formatted by ‘YYYY-MM-DD’
	* goes to the 0hr mark only
* `SELECT * FROM payment WHERE amount BETWEEN 8 AND 9;`

### IN
* create a condition to check if a value is included in the provided options
* easier than using AND multiple times
* `SELECT * FROM cd.facilities WHERE id IN (1,5)`
	* selects for id of 1 & 5

### LIKE and ILIKE
* match against patterns in string (ie. strings with @gmail.com)
* `ILIKE` is case-insensitive
* % matches any sequence of characters
	* names that start with ‘A’: `WHERE name LIKE ‘A%’`
	* names that end with ‘a’: `WHERE name LIKE ‘%a’`
* `_` allows skipping of characters
	* any values that have "r" in the second position: `WHERE CustomerName LIKE '_r%'`
	* can use multiple underscores

### Aggregate Functions
* take in multiple inputs and produces a single output
* avg, count, max, min, sum
* used only in the SELECT call
* AVG returns a floating point value so necessary to round
	* ROUND(AVG(..), 2) - the 2nd argument is the no. of DP

### GROUP BY
* combine columns for some category and apply functions
* only categorical columns can be GROUPed BY
* ` SELECT category_col , AGG(data_col) FROM table GROUP BY category_col`
* `GROUP BY` must appear after a FROM or WHERE statement
* to convert timestamp to date use DATE()

### HAVING
* filter after aggregation has taken place (i.e. a function has been done)
* `HAVING SUM(amount) > 100`

## JOINS
### AS
* creates an alias (new name) for a column
* `SELECT SUM(column) AS new_name`
* gets executed in the end of the query so unable to use `WHERE` for the new name

![[../images/joins.png]]

### INNER JOIN
* joins allow for the combination of multiple tables together
* inner joins will result with the set of **records that match in 2 tables**
* `SELECT * FROM Table A INNER JOIN Table B ON TableA.col = TableB.col`
* just `JOIN` rather than `INNER JOIN` is also acceptable

### FULL OUTER JOIN
* grabs everything in Venn diagram
* null for no values
* use `WHERE Table.col IS NULL` to get unique values

### LEFT OUTER JOIN
* records from the left table, if no match with right, will be null
* order matters
* `SELECT * FROM Table A LEFT OUTER JOIN Table B ON TableA.col = TableB.col`
* use WHERE to get rows unique / exclusive to left table
	* `WHERE tableB.col IS null`

### RIGHT JOIN
* same as the left join but with opposite tables

### UNION
* combine the results of 2 or more SELECT statements
	* can then Group and Sum up
* `SELECT col FROM table1 UNION SELECT col FROM table2`

## Advanced SQL
### Timestamps and EXTRACT
* `TIME` - only time
* `DATE` - only date
* `TIMESTAMP` - date / time
* `TIMESTAMPTZ `-  date / time and timezone
* able to remove historical info but cannot add it
* `TIMEZONE, NOW, TIMEOFDAY, CURRENT_TIME, CURRENT_DATE`
* `SHOW ALL` to show all the available parameters to SELECT
* `EXTRACT()` - obtain a sub component of a date value
	* year, month, day, week etc.
	* `EXTRACT(YEAR FROM date_col)`
* `AGE()` - returns the age of a current timestamp
	* `AGE(date_col)`
* `TO_CHAR()` - convert datatypes to text
	* for time stamp formatting
	* `TO_CHAR(date_col, ‘mm-dd-yyyy’)`

### Mathematical Functions & Operators
* round(), ceil(), random() etc.

### String functions & Operators
* search for substrings, lowercase etc.
* `SELECT length(name) FROM customer`
* left (col, num) picks the first num of chars

### SubQuery
* merge 2 separate queries
* `SELECT grade FROM scores WHERE grade > (SELECT AVG(grade) FROM scores`
* `EXIST()` - check whether any rows will be returned

### Self-Join
* join of 2 copies of the same table
* assign 2 different aliases to the same table
```sql
SELECT f1.title, f2.title, f1.length
FROM film AS f1
INNER JOIN film AS f2 
ON f1.film_id != f2.film_id AND f1.length = f2.length
```

## Creating database & Tables
### Data types
* Boolean, Character, Numeric, Temporal
* UUID, Array, JSON, HStore key-value pair, Net address etc.
* data types have sub data types 
	* Numeric - decimal, real, integer etc.

### Primary & Foreign Keys
* **Primary Key** [PK] - column(s) to identify a row uniquely, non null, integer
* **Foreign Key** - references to a primary key in another table
	* silver key under constraints denote foreign key
	* able to view under dependencies

### Constraints
* Rules enforced on data columns on table to prevent invalid data
* Column Constraints
	* **NOT NULL** - cannot have a NULL value
	* **UNIQUE** - all values must be different
	* Primary Key & Foreign Keys
	* **CHECK** - Ensures values satisfy certain condition
	* **EXCLUSION** - ???
* Table Constraints
	* **CHECK** - check a condition
	* **REFERENCES** - value must reference a col in another table
	* **UNIQUE** - values within multiple cols must be unique
	* **PRIMARY KEY** - Define the PK

### CREATE Table
* `CREATE TABLE` name ( col_name TYPE constraint, … )
* type SERIAL - for PK Table which creates a sequenced value
	* will not reformat when row is removed (1,2,3,5)
	* only used in the PK Table, Integer as a SK when referencing
```sql
CREATE TABLE account (
	user_id SERIAL PRIMARY KEY,
	username VARCHAR(50) UNIQUE NOT NULL,
	password VARCHAR(50) NOT NULL,
	email VARCHAR(250) UNIQUE NOT NULL,
	created_on TIMESTAMP NOT NULL,
	last_login TIMESTAMP
)

CREATE TABLE account_job (
	user_id INTEGER REFERENCES account(user_id),
	job_id INTEGER REFERENCES job(job_id),
	hire_date TIMESTAMP
)
```

### INSERT
* add rows into a table
* `INSERT INTO table (colm_1, colm_2) VALUES`
```sql
INSERT INTO account (username,password,email, create_on)
VALUES
('Ruban','password','ruban@mail.com',CURRENT_TIMESTAMP)
```

### UPDATE
* update values in a table by using `SET`
```sql
UPDATE account
SET last_login = CURRENT_TIMESTAMP
RETURNING email, last_login

// OR

UPDATE account
SET last_login = created_on

// OR

UPDATE account_job
SET hire_date = account.created_on
FROM account
WHERE account_job.user_id = account.user_id
```

### DELETE
* remove rows from table
* `DELETE FROM table`  deletes all rows
* can also add RETURNING like in UPDATE
```sql
DELETE FROM job
WHERE job_name = 'Cow'
```

### ALTER
* add, drop or rename cols
```sql
ALTER TABLE new_info
RENAME COLUMN person TO people
```
* change a col data type
* set DEFAULT values for col
* add CHECK constraints
	* DROP to remove, SET to add
```sql
ALTER TABLE new_info
ALTER COLUMN people DROP NOT NULL
```
* rename table
```sql
ALTER TABLE information
RENAME TO new_info
```

### DROP
* completely removes a col, indexes and constraints
* does not remove columns used in views
```
ALTER TABLE new_info
DROP COLUMN people
```

### CHECK Constraint
* `SERIAL` keeps the fail attempts when inserting 
```sql
CREATE TABLE employees (
	birthdate DATE CHECK (birthdate > '1900-01-01'),
	hire_date DATE CHECK (hire_date > birthdate),
	salary INTEGER CHECK (salary > 0)
)
```

## Conditional Expressions & Operators
### CASE
* only execute SQL code when certain conditions are met (like IF / ELSE)
* general Case Statement - Most flexible
```sql
SELECT customer_id,
CASE 
	WHEN (customer_id <= 100) THEN 'Premium'
	WHEN (customer_id BETWEEN 100 AND 200) THEN 'Plus'
	ELSE 'Basic'
END AS customer_class
FROM customer
```
* CASE expression syntax
	* first evaluates an expression then compares the result with each value in the WHEN clause
```sql
SELECT customer_id,
CASE customer_id
	WHEN 2 THEN 'Winner'
	WHEN 5 THEN 'Second Place'
	ELSE 'Losers'
END AS raffle_results
FROM customer
```
* using functions with CASE
```sql
SELECT 
SUM(CASE rental_rate 
	WHEN 0.99 THEN 1
	ELSE 0
END) AS bargains,
SUM(CASE rental_rate 
	WHEN 2.99 THEN 1
	ELSE 0
END) AS regulars
FROM film
```