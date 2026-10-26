# 4.9.1.59 CURRENT_TRANSACTION_ISOLATION_LEVEL Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 168

Returns a string containing the current transaction isolation level.

## Syntax

```sql
CURRENT_TRANSACTION_ISOLATION_LEVEL
```

## Description

Returns a string containing the current transaction isolation level.

## Example

The following example returns the current transaction isolation level:

```sql
SELECT CURRENT_TRANSACTION_ISOLATION_LEVEL "current transaction isolation level"
FROM DUMMY;
```
