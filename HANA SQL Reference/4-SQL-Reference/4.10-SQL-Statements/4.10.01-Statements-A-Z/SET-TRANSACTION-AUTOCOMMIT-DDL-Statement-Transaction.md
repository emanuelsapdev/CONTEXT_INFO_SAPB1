# 4.10.1.151 SET TRANSACTION AUTOCOMMIT DDL Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1105–1107

Specifies the auto commit property for DDL statements specific to the session.

## Syntax

```sql
SET TRANSACTION AUTOCOMMIT DDL { ON | OFF }
```

## Description

The default is ON. A user can specify the auto commit property for DDL statements specific to the session. If the auto commit property is on, then the transaction commits implicitly after executing each DDL statement. Otherwise, the transaction commits after executing a commit statement, and rollbacks of DDL statements are supported.

Partial rollback of DML is possible during an AUTOCOMMIT DDL OFF session, provided that no DDL was executed as part of the transaction.

Partial rollback of DDL is not possible during an AUTOCOMMIT DDL OFF session; a failure during an AUTOCOMMIT DDL OFF session that contains DDL triggers a full rollback. For example:

```sql
SET TRANSACTION AUTOCOMMIT DDL OFF;
CREATE TABLE T1 (A INT PRIMARY KEY); <– Successful DDL
INSERT INTO T1 VALUES (1); <– Successful DML
INSERT INTO T1 VALUES (1); <- Uniqueness violation, triggering a full rollback
due to the DDL in the transaction
SELECT * FROM T1; <- returns an invalid table name error due to the full rollback
```

There are some DDL cases that do not affect the rollback behavior, such as DDL that fails at syntax check, or DDL that fails due to a reference to a non-existent object. These cases are considered as ‘DDL is not executed’, and would not qualify the transaction for full rollback in the event of some other failure in the transaction.

Supportability of DDL rollbacks for various table types is as follows:

- Column, history column and row table: Rollbacks on DDL and DML statements are supported.
- Global temporary and global temporary column table: Rollbacks on DDL are supported, but rollbacks on DML for global temporary column tables are not supported.
- Local temporary and local temporary column table: Rollbacks on DDL are supported, but rollbacks on DML for local temporary column tables are not supported.
- No logging column table: Rollbacks on DDL are not supported, but rollbacks on DML are supported.

Rollbacks on the following DDL are not supported:

- ALTER TABLE {SET | UNSET} ROW ORDER
- ALTER TABLE to enable, disable client-side encryption or to change column encryption keys
- DDL on extended storage and extended storage tables
- {CREATE | ALTER | DROP} ADAPTER
- {CREATE | ALTER | DROP} AGENT

Before attempting to execute SET TRANSACTION AUTOCOMMIT DDL OFF, ensure that you are using an autocommit-disabled session.

## Example

Turn off DDL autocommit mode.

```sql
SET TRANSACTION AUTOCOMMIT DDL OFF;
```

Create a table T and insert two rows into it.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
INSERT INTO T VALUES (1, 1);
INSERT INTO T VALUES (2, 2);
```

Commit the current transaction.

```sql
COMMIT;
```

Add a new column VAL2 to table T and insert a row.

```sql
ALTER TABLE T ADD (VAL2 INT);
INSERT INTO T VALUES (3, 3, 3);
```

Roll back the current transaction.

```sql
ROLLBACK;
```

Select the data in table T and get two rows with two columns.

```sql
SELECT * FROM T;
```
