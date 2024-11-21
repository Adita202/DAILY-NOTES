#### Day - 6 - More keywords of SQL

Aggregate fns count, max, min, avg, sum

- SELECT MIN
- SELECT MAX
- SELECT COUNT


**GROUP BY**
often used with count, min, max or sum

   - to change name : COUNT (year) **year_count** - new name


###### ***order of keywords SELECT * FROM WHERE G-H-O-L*** 


#### JOIN
combine data in multiple tables
* types
	* Inner join - only compares same value and gives this at 
	* Left join
	* Right join
	* Full outer join
	* Natural join


***Sub Queries or nested queries or Inner queries***

First inner query executed then outer query executed

**SELECT actor_id FROM roles WHERE movies_id IN
(SELECT id FROM movies where name = 'Schindler's List')**


*SOME OPERATORS TO USE IN Sub Queries*

IN , NOT, EXISTS, NOT EXISTS, ANY, ALL, Comparison Operators

**INSERT command**
Can be used to insert a particular row into other rows

*INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7);
We can also add multiple values*


**UPDATE command**
UPDATE <TableName> SET col1=val1, col2=val2

**ALTER command** - modify structure of table, adding new columns, rename columns

**DELETE command**- DELETE FROM movies WHERE id = 

**DROP** - deletes both table and all the data permanently

**TRUNCATE** - Delete contents of the table without deleting the table, the table exists
