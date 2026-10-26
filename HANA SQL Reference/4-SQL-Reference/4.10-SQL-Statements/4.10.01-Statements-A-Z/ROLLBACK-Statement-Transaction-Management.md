# 4.10.1.141 ROLLBACK Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1033–1034

Changes made during the current transaction are reverted and current database session is set to an idle state.

## Syntax

```sql
ROLLBACK
```

## Description

The SAP HANA database supports transactional consistency which guarantees that a transaction is completely applied to the system or disposed. During a transaction, data manipulation language (DML) modifications to the database can be explicitly reverted via ROLLBACK command. After ROLLBACK is issued, changes made during the current transaction are reverted and current database session is set to an idle state. ROLLBACK only works with an autocommit disabled session.

If you attempt to use the ROLLBACK statements in an autocommit enabled session, then nothing occurs as transactions are automatically committed to the database.

For more information on changing the autocommit status of your database session, see the information about customizing the Administration Console in the SAP HANA Administration guide.

## Example

Before attempting to execute the example below, ensure that you are using an autocommit disabled session.

Create a table T.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
```

Insert three rows into table T.

```sql
INSERT INTO T VALUES (1, 1);
 INSERT INTO T VALUES (2, 2);
INSERT INTO T VALUES (3, 3);
```

Roll back the current transaction.

```sql
ROLLBACK;
```

Select the data in table T.

```sql
SELECT * FROM T;
```

The SELECT command above returns an empty table. The data definition language (DDL) command used to create the table persisted, but the DML used to create the table data has been rolled back.
