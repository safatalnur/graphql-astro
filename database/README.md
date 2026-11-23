# Database setup

This project uses the **University** sample database from the textbook
*Database System Concepts* (Silberschatz, Korth, Sudarshan).

The SQL files are **not** in this repo. Download them from the book's site:
https://www.db-book.com → "Laboratory Material" / "Sample Tables"

You need two files:
- `DDL.sql`: creates the tables
- `smallRelationsInsertFile.sql`: inserts the sample data

## Requirements
- MySQL 8 running locally

## Steps

1. Create an empty database:

   ```sql
   CREATE DATABASE universityApp;
   ```

2. Create the tables (run this **first**):

   ```bash
   mysql -u root -p universityApp < path/to/DDL.sql
   ```

3. Insert the data:

   ```bash
   mysql -u root -p universityApp < path/to/smallRelationsInsertFile.sql
   ```

4. Check it worked:

   ```sql
   USE universityApp;
   SHOW TABLES;
   ```

   You should see 11 tables: `advisor`, `classroom`, `course`, `department`,
   `instructor`, `prereq`, `section`, `student`, `takes`, `teaches`, `time_slot`.

## Troubleshooting

- **`Table 'universityapp.prereq' doesn't exist`**
  You ran the insert file before `DDL.sql`. Run `DDL.sql` first.

- **`Unknown table` error when running `DDL.sql`**
  The file starts with `drop table` statements, and on a new database there's
  nothing to drop. Add `--force` after `mysql`, or change each
  `drop table X;` to `drop table if exists X;`.

## Our own SQL
SQL files we write ourselves (for example, adding a `building` table) go in this
folder, numbered in the order they should run:
`01-add-building-table.sql`, `02-...`