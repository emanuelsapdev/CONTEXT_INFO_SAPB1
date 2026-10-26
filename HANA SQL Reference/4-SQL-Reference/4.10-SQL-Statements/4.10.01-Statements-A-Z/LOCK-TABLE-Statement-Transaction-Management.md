# 4.10.1.125 LOCK TABLE Statement (Transaction Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 992–994

Acquires an exclusive lock for a table.

## Syntax

```sql
LOCK TABLE <table_name>
 IN { EXCLUSIVE | INTENTIONAL EXCLUSIVE } MODE
 [ <wait_nowait> ]
```

## Syntax Elements

#### table_name

Specifies the table to lock, with the optional schema name.

```sql
<table_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### EXCLUSIVE

Locks the table in EXCLUSIVE mode. EXCLUSIVE locks are acquired explicitly by LOCK TABLE, but are also acquired implicitly by DDL commands. EXCLUSIVE locks have the following characteristics:

- The transaction that holds the lock can read and write to the table. All other transactions can read from the table but cannot write to it.
- When a table has an EXCLUSIVE lock on it, all other lock requests by other transactions are blocked.
- The database releases acquired locks at the end of the transaction.

#### INTENTIONAL EXCLUSIVE

Locks the table in INTENTIONAL EXCLUSIVE mode. However, INTENTIONAL EXCLUSIVE locks are only acquired by DML commands; use EXCLUSIVE mode instead. The description for INTENTIONAL EXCLUSIVE locks (acquired implicitly by DML commands **only**) is being provided here to explain the behavioral differences between the two different locks that are used in the database.

- Multiple transactions can acquire an INTENTIONAL EXCLUSIVE lock.
- When a table has an INTENTIONAL EXCLUSIVE lock on it, incoming EXCLUSIVE lock requests for the table by other transactions are blocked, whereas other INTENTIONAL EXCLUSIVE locks are allowed.
- The database releases acquired locks at the end of the transaction.

#### wait_nowait

Specifies when to return an error if the table lock could not be acquired.

```sql
<wait_nowait> ::= WAIT <unsigned_integer> | NOWAIT
```

If WAIT `<unsigned_integer>` is specified, then the statement waits up to the specified number of seconds for the lock. If the statement fails to acquire a lock after waiting, then it returns an error message indicating a timeout. If NOWAIT is specified, and the statement fails to acquire a table lock, then an error is returned indicating that the resource is busy. WAIT 0 is equivalent to NOWAIT.

When a timeout error is returned, the current transaction is not rolled back.

If `<wait_nowait>` is not specified, then the default behavior reflects the lock_wait_timeout transaction timeout setting located in `indexserver.ini`.

## Description

LOCK TABLE acquires a lock for a table.

If EXCLUSIVE is specified and there are views that reference the table, then the LOCK TABLE statement also attempts to lock the views in exclusive mode so that new transactions cannot hold locks on any dependent views. If all of the view locks cannot be acquired at that time, then the statement returns a non-zero SQLCODE even though the table itself is locked. Schema locks are only released upon the COMMIT or ROLLBACK of a transaction.

## Example

The following statements create a table A, and acquire an exclusive lock on it:

```sql
CREATE ROW TABLE A (A INT PRIMARY KEY, B INT);
LOCK TABLE A IN EXCLUSIVE MODE;
```

The following statement attempts to acquire an exclusive lock for table A, and specifies that an error should be returned if the lock cannot be immediately obtained.

```sql
LOCK TABLE A IN EXCLUSIVE MODE NOWAIT;
```

## Related Information

Introduction to SQL [→](../../4.01-Introduction-to-SQL.md) M_OBJECT_LOCKS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_OBJECT_LOCKS-System-View.md)
