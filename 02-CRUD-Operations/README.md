# 📚 CRUD Operations

In this section, I learned the fundamentals of CRUD (Create, Read, Update, Delete) operations in MySQL. I also explored table constraints such as `NOT NULL`, `DEFAULT`, `PRIMARY KEY`, and `AUTO_INCREMENT`.

---

# Topics Covered

- INSERT
- SELECT
- UPDATE
- DELETE
- NOT NULL
- DEFAULT
- PRIMARY KEY
- AUTO_INCREMENT
- CRUD Challenge

---

# Creating the Table

```sql
CREATE TABLE cats (
    name VARCHAR(50),
    age INT
);
```

---

# INSERT

Insert a single record.

```sql
INSERT INTO cats (name, age)
VALUES ('Blue Steele', 5);

INSERT INTO cats (name, age)
VALUES ('Jenkins', 7);
```

Insert while changing the column order.

```sql
INSERT INTO cats (age, name)
VALUES (2, 'Beth');
```

Insert multiple records.

```sql
INSERT INTO cats (name, age)
VALUES
('Meatball', 5),
('Turkey', 1),
('Potato Face', 15);
```

---

# SELECT

Retrieve all records.

```sql
SELECT * FROM cats;
```

Retrieve specific columns.

```sql
SELECT age FROM cats;

SELECT name, breed FROM cats;
```

Filter records.

```sql
SELECT * FROM cats
WHERE age = 4;

SELECT * FROM cats
WHERE name = 'Egg';
```

Rename a column using `AS`.

```sql
SELECT cat_id AS id, name
FROM cats;
```

---

# UPDATE

Update existing records.

```sql
UPDATE cats
SET breed = 'Shorthair'
WHERE breed = 'Tabby';
```

```sql
UPDATE cats
SET age = 14
WHERE name = 'Misty';
```

---

# DELETE

Delete specific records.

```sql
DELETE FROM cats
WHERE name = 'Egg';
```

Delete all records.

```sql
DELETE FROM cats;
```

Delete using a condition.

```sql
DELETE FROM cats
WHERE age = 4;
```

---

# Table Constraints

## NOT NULL

```sql
CREATE TABLE cats2 (
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL
);
```

---

## DEFAULT

```sql
CREATE TABLE cats3 (
    name VARCHAR(20) DEFAULT 'no name provided',
    age INT DEFAULT 99
);
```

Example:

```sql
INSERT INTO cats3(age)
VALUES (13);

INSERT INTO cats3()
VALUES();
```

---

## NOT NULL + DEFAULT

```sql
CREATE TABLE cats4 (
    name VARCHAR(20) NOT NULL DEFAULT 'unnamed',
    age INT NOT NULL DEFAULT 99
);
```

---

## PRIMARY KEY

```sql
CREATE TABLE unique_cats2 (
    cat_id INT,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    PRIMARY KEY (cat_id)
);
```

---

## AUTO_INCREMENT

```sql
CREATE TABLE unique_cats3 (
    cat_id INT AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL,
    PRIMARY KEY (cat_id)
);
```

Example:

```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(255) NOT NULL,
    last_name VARCHAR(255) NOT NULL,
    middle_name VARCHAR(255),
    age INT NOT NULL,
    current_status VARCHAR(255) NOT NULL DEFAULT 'employed'
);
```

Insert a record.

```sql
INSERT INTO employees(first_name, last_name, age)
VALUES ('Dora', 'Smith', 58);
```

---

# CRUD Practice Project

Created a new `cats` table with a primary key.

```sql
CREATE TABLE cats (
    cat_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    breed VARCHAR(100),
    age INT
);
```

Inserted sample data and practiced:

- INSERT
- SELECT
- UPDATE
- DELETE
- WHERE
- AS

Example:

```sql
SELECT * FROM cats;

UPDATE cats
SET breed='British Shorthair'
WHERE name='Ringo';

DELETE FROM cats
WHERE name='Egg';
```

---

# CRUD Challenge

Created a simple inventory database.

```sql
CREATE DATABASE shirts_db;

USE shirts_db;
```

Created the table.

```sql
CREATE TABLE shirts (
    shirt_id INT AUTO_INCREMENT PRIMARY KEY,
    article VARCHAR(50),
    color VARCHAR(50),
    shirt_size VARCHAR(5),
    last_worn INT
);
```

Practiced:

- INSERT
- SELECT
- UPDATE
- DELETE
- Filtering with WHERE

Example:

```sql
SELECT article, color
FROM shirts;

UPDATE shirts
SET shirt_size = 'L'
WHERE article = 'polo shirt';

DELETE FROM shirts
WHERE article = 'tank top';
```

---

# Key Takeaways

- Learned the four basic CRUD operations.
- Practiced inserting single and multiple rows.
- Used `WHERE` to filter data.
- Updated existing records using `UPDATE`.
- Removed records using `DELETE`.
- Learned how `NOT NULL`, `DEFAULT`, `PRIMARY KEY`, and `AUTO_INCREMENT` work.
- Applied CRUD concepts in a small practice project.