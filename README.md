# SQL Snippets

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