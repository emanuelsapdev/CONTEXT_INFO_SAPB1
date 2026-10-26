# 4.10.1.157 UPDATE Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1114–1120

Changes the values of the records of a table.

## Syntax

```sql
UPDATE [ <top_clause> ] <table_name> [ AS <alias_name> ]
   [ FOR PORTION_OF_APPLICATION_TIME <from_to_spec> ]
   [ <partition_restriction > ]
   [ <from_clause> ]
   <set_clause>
   [ WHERE <condition> ]
   [ <hint_clause> ]
```

## Syntax Elements

#### top_clause

Limits the number of updated records (for example, for chunkwise updates).

```sql
<top_clause> ::= TOP <unsigned_integer>
```

`<unsigned_integer>` defines the number of records updated in one chunk.

#### table_name

Specifies the table where the UPDATE is performed, with the optional schema name.

```sql
<table_name> ::= [ [ <database_name>.]<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

For linked database, `<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

#### alias_name

Specifies the alias that can be used to refer to the table defined by `<table_name>`.

```sql
<alias_name> ::= <identifier>
```

#### FOR PORTION OF APPLICATION_TIME

For use with application-time period tables, this clause specifies that the update be limited to the specified period of time between `<valid_from>` and `<valid_to>`, inclusively.

```sql
FOR PORTION OF APPLICATION_TIME <from_to_spec>
<from_to_spec> ::= FROM <valid_from> TO <valid_to>
```

`<valid_from>` and `<valid_to>` are date values found in the application-time period table specified for `<table_name>`.

#### partition_restriction

For a partitioned table, `<partition_restriction>` specifies the partition in which the target updated rows are located.

```sql
<partition_restriction> ::= PARTITION ( <partition_number> )
<partition_number> ::= <unsigned_integer>
```

If you do not specify a partition restriction, then the database checks all partitions for the update. But if there is partition restriction, only the rows in specified partition are updated.

Limitations:

- An UPDATE statement with a partition restriction is blocked if the following are true:
  - Partitioning key column update
  - UNIQUE constraint column update
  - PRIMARY KEY column update
- Updates that change the updated rows partition are not allowed.

#### from_clause

Specifies inputs such as tables to be used in the update statement.

```sql
<from_clause> ::= FROM <table_name> [, <table_name>]...
<table_name> ::= <identifier>
```

The object to be updated can be specified as an alias in the `<from_clause>`.

`<from_clause>` is not supported in combination with FOR PORTION OF

#### set_clause

Specifies the column names and associated values to be set by the update statement.

```sql
<set_clause> ::=
 SET {<column_name> = <expression>
 | ( <with_clause> <subquery> ) },...
```

For the definitions of the `<with_clause>` and `<subquery>`, see the SELECT statement. The `<with_clause>` can be used with column names, not with column lists.

#### WHERE condition

Specifies the conditions when the command should be performed.

```sql
<condition> ::=
 <condition> OR <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>
 | CURRENT OF <cursor>
```

WHERE CURRENT OF `<cursor>` specifies to perform the update at the current position in the cursor.

For more information on `<predicate>`, see the Predicates topic in this guide.

#### hint_clause

For information on hints, see the HINT clause in the SELECT statement.

## Description

When this command is used with the FROM clause, the UPDATE FROM query must include the updated table name in the FROM clause. Or if an alias exists, the alias should exist in the FROM clause. Otherwise an error is returned.

If the WHERE condition is used and is true for a specific row, then the an update is performed on that row. If the WHERE clause is omitted, then the UPDATE command updates all records of a table.

While some database vendors do not support multiple updates to one record by an UPDATE FROM statement; SAP HANA does. However, the result can be non-deterministic since the order in which the updates are performed cannot always be guaranteed.

## Examples

Create table T, and insert two rows into it.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
 INSERT INTO T VALUES (1, 1);
 INSERT INTO T VALUES (2, 2);
```

Update the rows of table T if the condition in the WHERE clause is true.

```sql
UPDATE T SET VAL = VAL + 1 WHERE KEY = 1;
SELECT * FROM T;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 2 |

This example shows how to update all rows of the table by omitting the WHERE clause.

```sql
UPDATE T SET VAL = KEY + 10;
SELECT * FROM T;
```

| KEY | VAL |
| --- | --- |
| 1 | 11 |
| 2 | 12 |

Create table T2, and insert two rows into it.

```sql
CREATE ROW TABLE T2 (KEY INT PRIMARY KEY, VAR INT);
 INSERT INTO T2 VALUES (1, 2);
 INSERT INTO T2 VALUES (3, 6);
```

Update the values of table T by joining the target table T with table T2.

```sql
UPDATE T SET VAL = T2.VAR FROM T, T2 WHERE T.KEY = T2.KEY;
SELECT * FROM T;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 12 |

Update the table T with an aliased table in the FROM clause by joining the target table T with table T2 which also has an alias.

```sql
UPDATE T A SET VAL = B.VAR FROM T A, T2 B WHERE A.KEY = B.KEY;
SELECT * FROM T;
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |
| 2 | 12 |

The updated table should exist in the FROM clause.

If you update a table using the FROM clause like the example below, ambiguity of the target table in the FROM clause is allowed.

```sql
UPDATE T SET VAL = B.VAL FROM T A, T B WHERE A.KEY = B.KEY; --> error due to
ambiguity of table T.
```

| KEY | VAL |
| --- | --- |
| 1 | 2 |

| 2 | 12 |
| --- | --- |

You can specify the partition that you want to update with partition restriction clause.

```sql
CREATE COLUMN TABLE PARTTAB1 (A INT, B INT, C INT) PARTITION BY RANGE(A)
(PARTITION 0 <= VALUES <3, PARTITION OTHERS);
 INSERT INTO PARTTAB1 VALUES (1,1,1);
 INSERT INTO PARTTAB1 VALUES (2,2,2);
 INSERT INTO PARTTAB1 VALUES (3,3,3);
 UPDATE PARTTAB1 PARTITION(1) SET B = 10; -- only records (1,1,1) and (2,2,2)
are updated.
```

Update a chunk of 100,000 records of the table testtab that contain 'XXX' in the request column and the value 0 in the updated column. For each row processed, the updated column is set to 1.

```sql
update top 100000 testtab set updated = 1 where request = 'XXX' and updated = 0
```

UPDATE a table with an array value construction by enumeration .

```sql
UPDATE T1 SET C1 = ARRAY ( 11, 12, 13, 14 ) WHERE ID = 1
```

UPDATE a table with an array value construction by query.

```sql
UPDATE T1 SET C1 = ARRAY( SELECT C1 FROM T0 ) WHERE ID = 1
```

The following statements provide an example of updating a single table using updatable cursor:

```sql
CREATE COLUMN TABLE employees (employee_id INTEGER, employee_name VARCHAR(30));
INSERT INTO employees VALUES (1, 'John');
INSERT INTO employees VALUES (20010, 'Sam');
INSERT INTO employees VALUES (21, 'Julie');
INSERT INTO employees VALUES (10005, 'Kate');
DO BEGIN
    DECLARE CURSOR cur FOR SELECT * FROM employees FOR UPDATE;
    FOR r AS cur DO
        IF r.employee_id < 10000 THEN
            UPDATE employees SET employee_id = employee_id + 10000
            WHERE CURRENT OF cur;
        ELSE
            DELETE FROM employees WHERE CURRENT OF cur;
        END IF;
  END FOR;
END;
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
            UPDATE employees SET employee_id = employee_id + 10000,
department_id = department_id + 100
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

The following example shows how the UPDATE...FROM syntax supports multiple updates to one record, even though the result can be non-deterministic.

```sql
CREATE COLUMN TABLE T (KEY INT PRIMARY KEY, VAL INT);
INSERT INTO T VALUES (1, 1);
CREATE COLUMN TABLE T2 (KEY INT, VAR INT);
INSERT INTO T2 VALUES (1, 2);
INSERT INTO T2 VALUES (1, 3);
INSERT INTO T2 VALUES (1, 4);
INSERT INTO T2 VALUES (1, 5);
UPDATE T SET VAL = T2.VAR FROM T, T2 WHERE T.KEY = T2.KEY;
SELECT * FROM T;   ----> [(1,5)]
```

While the last update (1,5) is returned as the result, the sequence of updates isn't guaranteed so the result is non-deterministic.

In this example, suppose you have the following application-period time table, TAB01, that you want to update:

| **ValidFrom** | **ValidTo** | **PKEY** | **Value** |
| --- | --- | --- | --- |
| 2018-08-01 | 2018-08-15 | 1 | 9494 |
| 2018-08-15 | 2018-08-31 | 1 | 20 |
| 2018-08-31 | 2018-09-10 | 1 | 30 |
| 2018-09-10 | 9999-12-31 | 1 | 40 |

When you execute the following UPDATE statement, the values are updated according to the description in the Comment column of table that follows:

```sql
UPDATE TAB01 FOR PORTION OF '2018-08-20' AND '2018-10-20' SET VALUE=42 WHERE
PKEY=1;
```

| **ValidFrom** | **ValidTo** | **PKEY** | **VALUE** | **Comment** |
| --- | --- | --- | --- | --- |
| 2018-08-01 | 2018-08-15 | 1 | 9394 | Not modified (outside of portion interval) |
| 2018-08-15 | 2018-08-20 | 1 | 20 | Newly inserted record (case partial overlap) |
| 2018-08-20 | 2018-08-31 | 1 | 42 | Validfrom and Value were updated (case partial overlap) |
| 2018-08-31 | 2018-09-10 | 1 | 42 | Only Value was updated (case full overlap) |
| 2018-09-10 | 2018-10-20 | 1 | 42 | Validto and value were updated (case partial overlap) |
| 2018-10-20 | 9999-12-31 | 1 | 40 | Newly inserted record (case partial overlap) |

## Related Information

Introduction to SQL [→](../../4.01-Introduction-to-SQL.md) Expressions [→](../../4.06-Expressions.md) SELECT Statement (Data Manipulation) [→](4.10.01.144-SELECT/README.md) Predicates [→](../../4.07-Predicates/README.md)
