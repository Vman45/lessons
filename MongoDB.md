#Database Basics

## mongo | SQL

mongo: `use <db name>`
SQL: `CREATE DATABASE <db name>;`, `USE <db name>;`

Table | Collection
A place to keep records

- Creating a collection in mongo: `db.createCollection();`, `show collections`
- Creating a table in SQL:
  `CREATE TABLE <table name> (<column definitions>);`, `SHOW TABLES;`
  Difference I: SQL requires structure, `DESCRIBE <table name>`

  Row | Document
  A single record in a collection/table

- Inserting a document in mongo: `db.<collection>.insertOne(<document>);`
- Inserting a row in mySQL: `INSERT INTO <table name> VALUES (<values>);`
- Difference II: Mongo implicitly creates collections with `.insertOne()`

Column | Field
A value in a record

- Showing all documents in mongo: `db.<collection>.find({})`
- Showing all rows of a table in SQL: `SELECT * from <table name>`

Key | Id
An id / key uniquely identifies a record

- Adding Ids to SQL:
  `CREATE TABLE <table name> ( id NOT NULL AUTO_INCREMENT, <column definitions>, PRIMARY_KEY(id) );`

- Difference III: Mongo implicitly provides unique ids

CRUD: Four primary data operations

- Create: Inserting multiple rows / documents:
  mongo:
  `db.<collection>.insertMany([{ <document 1> }, { <document 2> }, <...>]);`
  SQL:
  `INSERT INTO <table> VALUES (<row 1>), (<row 2>), <...>;`
- Retrieve: Querying the table / collection by criteria:
  mongo:
  `db.<collection>.find({ <field name>: { criteria } });`
  SQL:
  `SELECT * from <table> WHERE <criteria>`
- Update: Updating a row / document:
  mongo:
  `db.<collection>.updateOne({ <criteria>, {$set: <values> });`
  SQL:
  `UPDATE <table> SET <values> WHERE <criteria>;`
- Delete: Deleting a row / document:
  mongo:
  `db.<collection>.deleteOne({ <criteria> });`
  SQL:
  `DELETE FROM <table> WHERE <criteria>;`
