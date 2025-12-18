# Postgres SQL Basics

## Datatypes in POSTGRES

https://www.postgresql.org/docs/current/datatype.html

## Create a table

```sql
CREATE TABLE student (
  id SERIAL PRIMARY KEY NOTNULL UNIQUE, -- SERIAL permet l'auto-incrément du champs
  first_name TEXT,
  last_name TEXT
);
```

## Create a One to One relationship

```sql
-- One to One --
CREATE TABLE contact_detail (
  id INTEGER REFERENCES student(id) UNIQUE,
  tel TEXT,
  address TEXT
);
```

## Add data

```sql
-- Data --
INSERT INTO student (first_name, last_name)
VALUES ('Angela', 'Yu');
INSERT INTO contact_detail (id, tel, address)
VALUES (1, '+123456789', '123 App Brewery Road');
```

## Read a table

```sql
SELECT world_food.country, world_food.wheat_production FROM world_food
WHERE world_food.wheat_production > 100
ORDER BY id ASC
```

```sql
SELECT world_food.country from world_food
WHERE world_food.country LIKE '%' || 'a' --anything ending with 'a'
```

```sql
-- Join --
SELECT *
FROM student
JOIN contact_detail
ON student.id = contact_detail.id
```

## Many to One Relationship

```sql
-- Many to One --
CREATE TABLE homework_submission (
id SERIAL PRIMARY KEY,
mark INTEGER,
student_id INTEGER REFERENCES student(id)
);

-- Data --
INSERT INTO homework_submission (mark, student_id)
VALUES (98, 1), (87, 1), (88, 1)

-- Join --
SELECT *
FROM student
JOIN homework_submission
ON student.id = student_id

SELECT student.id, first_name, last_name, mark
FROM student
JOIN homework_submission
ON student.id = student_id
```

## Many to Many Relationship

```sql
-- Many to Many --
CREATE TABLE class (
id SERIAL PRIMARY KEY,
title VARCHAR(45)
);

CREATE TABLE enrollment (
student_id INTEGER REFERENCES student(id),
class_id INTEGER REFERENCES class(id),
PRIMARY KEY (student_id, class_id)
);

-- Data --
INSERT INTO student (first_name, last_name)
VALUES ('Jack', 'Bauer');

INSERT INTO class (title)
VALUES ('English Literature'), ('Maths'), ('Physics');

INSERT INTO enrollment (student_id, class_id ) VALUES (1, 1), (1, 2);
INSERT INTO enrollment (student_id ,class_id) VALUES (2, 2), (2, 3);

-- Join --
SELECT \*
FROM enrollment
JOIN student ON student.id = enrollment.student_id
JOIN class ON class.id = enrollment.class_id;

SELECT student.id AS id, first_name, last_name, title
FROM enrollment
JOIN student ON student.id = enrollment.student_id
JOIN class ON class.id = enrollment.class_id;
```

## Using Aliases

```sql
-- ALIAS --
SELECT s.id AS id, first_name, last_name, title
FROM enrollment AS e
JOIN student AS s ON s.id = e.student_id
JOIN class AS c ON c.id = e.class_id;

SELECT s.id AS id, first_name, last_name, title
FROM enrollment e
JOIN student s ON s.id = e.student_id
JOIN class c ON c.id = e.class_id;
```

## Alter Database

```sql
ALTER TABLE <table to update>
  <DO SOMETHING>
```

```sql
-- Examples:
-- Rename table
ALTER TABLE student
  RENAME TO user

-- Change column type
ALTER TABLE user
  ALTER COLUMN first_name TYPE VARCHAR(20)

-- Add new column to table
ALTER TABLE user
  ADD email TEXT

-- Add combined unicity to two columns
ALTER TABLE visits
  ADD UNIQUE(user_id, countries_id)
```

## Update data

```sql
UPDATE <table to update>
SET <column to update>
WHERE <some condition>
```

## Order returned rows

```sql
SELECT *
FROM <some table>
ORDER BY <some condition>
```

Common conditions are :

```sql
ASC -- Ascending order
DESC -- Descending order
```

## Delete Data

```sql
DELETE FROM <some table>
WHERE <some condition>
```

```sql
-- Example:
DELETE FROM visits
WHERE users_id = 1 AND countries_id = 205
```
