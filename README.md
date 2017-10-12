# SQL Snippets

## How to know the databases in the current SLQ instance

We should run the next query:

```sql
sp_databases;
```

It will return a list of available databases in the SQL instance

## How to return a list of tables from the currents selected DataBase

If we want a list of all the tables (including views, systems tables and so on), we can run the next store procedure:

```sql
USE SampleDB
GO

sp_tables
```

The store procedure accepts a serie of parameter that tell which database to use, as well as what specifically to list ('TABLE' as opposed to 'VIEW' or 'SYSTEM TABLE').

```sql
USE SampleDB
GO

sp_tables NULL, dbo, SampleDB, "'TABLE'"
```

## Create database

```sql
CREATE DATABASE SampleDB
``` 

## Create a table

```sql
USE SampleDB

CREATE TABLE ContactInformation (
  ContactID int IDENTITY(1,1) NOT NULL PRIMARY KEY,
  ContactName nvarchar(20) NOT NULL,
  PhoneNumber nvarchar(8) NOT NULL
);
```

## Insert into a table

```sql
USE MVCQuiz

INSERT INTO ContactInformation (ContactName, PhoneNumber)
    VALUES ('Alexis', '87665118');

GO
```