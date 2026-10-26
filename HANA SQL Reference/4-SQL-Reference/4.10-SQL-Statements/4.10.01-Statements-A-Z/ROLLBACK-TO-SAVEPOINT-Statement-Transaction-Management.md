# 4.10.1.142 ROLLBACK TO SAVEPOINT Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1034–1035

Rolls back a transaction to the named savepoint without terminating the transaction.

## Syntax

```sql
ROLLBACK TO SAVEPOINT <savepoint_name>
```

## Syntax Elements

**savepoint_name** Specifies the case-insensitive identifier that was specified on a SAVEPOINT statement within the current transaction.

## Description

The ROLLBACK TO SAVEPOINT statement undoes any changes that have been made since the SAVEPONIT was established without terminating the current transaction. Changes made before the SAVEPOINT was set are not undone. Savepoints set after that savepoint to which you rolled back are erased, but the rollback savepoint remains.

The savepoint name specified must exist within the current transaction.

A ROLLBACK or COMMIT erases all savepoints.

The `<savepoint_name>` identifier can be used in a SAVEPOINT or RELEASE SAVEPOINT statement.

## Examples

Create a table T.

```sql
CREATE ROW TABLE T (KEY INT PRIMARY KEY, VAL INT);
```

Insert two rows into table T.

```sql
INSERT INTO T VALUES (1, 1);
 INSERT INTO T VALUES (2, 2);
```

Set a savepoint.

```sql
SAVEPOINT savepoint1;
```

Insert a row into table T.

```sql
INSERT INTO T VALUES (3, 3);
```

Roll back the current transaction to savepoint1.

```sql
ROLLBACK TO SAVEPOINT savepoint1;
```

Select the data in table T.

```sql
SELECT * FROM T;
```

The SELECT command above rows one and two, but not three.

## Related Information

RELEASE SAVEPOINT Statement (Transaction Management) [→](RELEASE-SAVEPOINT-Statement-Transaction-Management.md) SAVEPOINT Statement (Transaction Management) [→](SAVEPOINT-Statement-Transaction-Management.md)
