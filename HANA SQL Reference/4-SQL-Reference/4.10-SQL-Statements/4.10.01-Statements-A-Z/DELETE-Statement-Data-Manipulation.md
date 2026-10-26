# 4.10.1.80 DELETE Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 886–889

Deletes records from a table where a specified condition is met.

## Syntax

```sql
DELETE [HISTORY] FROM <table_name> [ <partition_restriction> ]
   [ WHERE <condition> ] [ <hint_clause> ]
```

## Syntax Elements

#### HISTORY

Marks the selected records of a history table for deletion.

#### FROM table_name

Specifies the table name where the deletion is to occur, with optional schema name.

```sql
<table_name> ::= [[<database_name>.][<schema_name>.]]<identifier>

<schema_name> ::= <unicode_name>
```

For linked database, `<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

#### partition_restriction

For a partitioned table, `<partition_restriction>` specifies the partition in which the target rows are located.

```sql
<partition_restriction> ::= PARTITION ( <partition_number> )
<partition_number> ::= <unsigned_integer>
```

If you do not specify a partition restriction, then the database checks all partitions for the delete. But if there is a partition restriction, then only the rows in the specified partition are deleted. Use the TABLE_PARTITIONS system view to determine the partition number.

The `<partition_restriction>` clause is supported for multistore tables but not extended store tables.

#### WHERE condition

Specifies the conditions where the command should be performed.

```sql
<condition> ::=
 <condition> OR <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>
 | CURRENT OF <cursor>
```

WHERE CURRENT OF `<cursor>` specifies to perform the delete at the current position in the cursor.

For more information on `<predicate>`, see the Predicates topic in this guide.

#### hint_clause

Specifies the hint clause. For information on specifying hints, see the HINT clause of the SELECT statement.

## Description

If the WHERE clause is omitted, then DELETE removes all records from a table.

When using the DELETE HISTORY command, time travel queries referencing the deleted rows may still access these rows. To physically delete these rows, you must execute the following statements:

```sql
ALTER SYSTEM RECLAIM VERSION SPACE;
            MERGE HISTORY DELTA of <table_name>;
```

In some cases even the execution of the two statements above may not lead to physical deletion.

To check whether the rows are physically deleted, execute the following statement:

```sql
SELECT * FROM <table_name> WHERE <condition>
            WITH PARAMETERS ('REQUEST_FLAGS'= ('ALLCOMMITTED','HISTORYONLY'));
```

The "WITH PARAMETERS ('REQUEST_FLAGS'= ('ALLCOMMITTED','HISTORYONLY'))" clause is only supported for validating the result of using the DELETE HISTORY statement.

## Examples

This example deletes values equal to 1 from table T.

Create a table T and insert some data.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
               INSERT INTO T VALUES (1, 1);
               INSERT INTO T VALUES (2, 2);
               INSERT INTO T VALUES (3, 3);
```

Delete from table T where the key column is equal to 1;

```sql
DELETE FROM T WHERE KEY = 1;
```

After executing the above query, the contents of table T are as follows, showing that one row was deleted from the table:

| KEY | VAL |
| --- | --- |
| 2 | 2 |
| 3 | 3 |

This example deletes partition 1 from table T1.

```sql
CREATE COLUMN TABLE T1 (a int, b int) PARTITION BY RANGE (a)
     (PARTITION 0 <= VALUES < 10, PARTITION OTHERS);
INSERT INTO T1 PARTITION(1) VALUES(1,50);
DELETE FROM T1 PARTITION(1);
```

This example deletes the updated record history.

Create a history table and insert a value.

```sql
CREATE HISTORY COLUMN TABLE HIST(KEY INT PRIMARY KEY, VAL INT);
               INSERT INTO HIST VALUES (1, 1);
               COMMIT;
```

Update the row you inserted in the previous step.

```sql
UPDATE HIST SET VAL=42 WHERE KEY=1;
COMMIT;
```

Merge in the table delta-storage with the table main-storage.

```sql
MERGE DELTA OF HIST;
```

Assuming the merge statement has moved the updated record into the history storage of the history table, delete the updated record history.

```sql
DELETE HISTORY FROM HIST WHERE KEY=1;
```

Delete from the table using an array value.

```sql
DELETE FROM T1 WHERE 3 MEMBER OF C1;
```

The following statements provide an example of updating and deleting multiple tables (currently only COLUMN tables are supported) through an updatable cursor. In this case, you must specify columns of tables to be locked using FOR UPDATE OF within the cursor's SELECT statement. DML execution using updatable cursor is allowed just one time per row.

```sql
CREATE COLUMN TABLE employees (employee_id INTEGER, employee_name VARCHAR(30),
department_id INTEGER);
INSERT INTO employees VALUES (1, 'John', 1);
INSERT INTO employees VALUES (2, 'Sam', 2);
INSERT INTO employees VALUES (3, 'Julie', 3);
INSERT INTO employees VALUES (4, 'Kate', 4);
CREATE COLUMN TABLE departments (department_id INTEGER, department_name
VARCHAR(20));
INSERT INTO departments VALUES (1, 'Development');
INSERT INTO departments VALUES (2, 'Operation');
INSERT INTO departments VALUES (3, 'HR');
INSERT INTO departments VALUES (4, 'Security');
DO BEGIN
      DECLARE CURSOR cur FOR SELECT employees.employee_name,
departments.department_name
      FROM employees, departments WHERE employees.department_id =
departments.department_id
      FOR UPDATE OF employees.employee_id, departments.department_id;
      FOR r AS cur DO
      IF r.department_name = 'Development' THEN
      UPDATE employees SET employee_id = employee_id + 10000, department_id =
department_id + 100
      WHERE CURRENT OF cur;
      UPDATE departments SET department_id = department_id + 100
      WHERE CURRENT OF cur;
      ELSEIF r.department_name = 'HR' THEN
      DELETE FROM employees WHERE CURRENT OF cur;
      DELETE FROM departments WHERE CURRENT OF cur;
      END IF;
      END FOR;
END;
```

## Related Information

TABLE_PARTITIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md) Introduction to SQL [→](../../4.01-Introduction-to-SQL.md) Predicates [→](../../4.07-Predicates/README.md) SELECT Statement (Data Manipulation) [→](4.10.01.144-SELECT/README.md) HINTS System View [→](../../../6-System-Views-Reference/6.01-System-Views/HINTS-System-View.md) HINT Details [→](4.10.01.144-SELECT/4.10.01.144.01-HINT-Details.md)
