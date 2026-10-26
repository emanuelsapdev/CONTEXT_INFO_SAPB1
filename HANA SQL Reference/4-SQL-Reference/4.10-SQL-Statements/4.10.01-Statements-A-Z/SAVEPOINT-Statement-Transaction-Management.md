# 4.10.1.143 SAVEPOINT Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1035–1036

Defines a location to which a transaction can return if part of the transaction is conditionally canceled.

## Syntax

```sql
SAVEPOINT <savepoint_name>
```

## Syntax Elements

**savepoint_name** Specifies a unique incase-sensitive identifier for the savepoint.

## Description

Establish a savepoint within the current transaction.

The number of active savepoints for each transaction is unlimited. Savepoint names must be unique within a given transaction. If you create a second savepoint with the same identifier as an earlier savepoint, then the earlier savepoint is erased.

The `<savepoint_name>` identifier can be used in a RELEASE SAVEPOINT or ROLLBACK TO SAVEPOINT statement.

This statement should not be confused with the ALTER SYSTEM SAVEPOINT statement, which performs a database checkpoint, not a transactional checkpoint.

## Examples

Create a SAVEPOINT named savepoint1.

```sql
SAVEPONT savepoint1;
```

## Related Information

RELEASE SAVEPOINT Statement (Transaction Management) [→](RELEASE-SAVEPOINT-Statement-Transaction-Management.md) ROLLBACK TO SAVEPOINT Statement (Transaction Management) [→](ROLLBACK-TO-SAVEPOINT-Statement-Transaction-Management.md) ALTER SYSTEM SAVEPOINT Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SAVEPOINT-Statement-System-Management.md)
