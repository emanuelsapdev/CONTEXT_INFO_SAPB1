# 4.10.1.133 RELEASE SAVEPOINT Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1020–1021

Releases a specified savepoint name.

## Syntax

```sql
RELEASE SAVEPOINT <savepoint_name>
```

## Syntax Elements

**savepoint_name** Specifies the case-insensitive identifier that was specified on a SAVEPOINT statement within the current transaction.

## Description

Releases an established savepoint within the current transaction. The savepoint name specified must exist for the current transaction.

The `<savepoint_name>` identifier can be used in a SAVEPOINT or ROLLBACK TO SAVEPOINT statement.

## Examples

Release a SAVEPOINT named savepoint1.

```sql
RELEASE SAVEPONT savepoint1;
```

## Related Information

ROLLBACK TO SAVEPOINT Statement (Transaction Management) [→](ROLLBACK-TO-SAVEPOINT-Statement-Transaction-Management.md) SAVEPOINT Statement (Transaction Management) [→](SAVEPOINT-Statement-Transaction-Management.md)
