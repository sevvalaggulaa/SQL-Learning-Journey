# 📚 Database Fundamentals

In this section, I learned the basics of working with databases and tables in MySQL. This includes creating and deleting databases, creating tables, and inspecting their structure.

---

# Topics Covered

- Creating databases
- Listing databases
- Selecting a database
- Dropping databases
- Creating tables
- Viewing tables
- Viewing table structure
- Dropping tables

---

# Listing Databases

Displays all available databases.

```sql
SHOW DATABASES;
```

---

# Creating a Database

Creates a new database.

**Syntax**

```sql
CREATE DATABASE database_name;
```

**Example**

```sql
CREATE DATABASE soap_store;
```

---

# Using a Database

Selects the database that will be used.

**Syntax**

```sql
USE database_name;
```

---

# Dropping a Database

Deletes an entire database.

**Syntax**

```sql
DROP DATABASE database_name;
```

---

# Creating Tables

Creates two simple tables.

```sql
CREATE TABLE cats (
    name VARCHAR(50),
    age INT
);

CREATE TABLE dogs (
    name VARCHAR(50),
    breed VARCHAR(50),
    age INT
);
```

---

# Listing Tables

Shows all tables in the current database.

```sql
SHOW TABLES;
```

---

# Viewing Table Structure

Displays the columns and data types of a table.

```sql
SHOW COLUMNS FROM cats;

DESC cats;
```

---

# Dropping a Table

Deletes a table.

**Syntax**

```sql
DROP TABLE table_name;
```

**Example**

```sql
DROP TABLE cats;
```

---

# Practice Example

Create a new table.

```sql
CREATE TABLE pastries (
    name VARCHAR(50),
    quantity INT
);
```

List all tables.

```sql
SHOW TABLES;
```

View the table structure.

```sql
DESC pastries;
```

Delete the table.

```sql
DROP TABLE pastries;
```

---

# Key Takeaways

- Learned how to create and remove databases.
- Learned how to create and delete tables.
- Learned how to inspect table structures.
- Learned basic MySQL data types such as `VARCHAR` and `INT`.
- Understood the relationship between databases and tables.