# 4.9.1.61 CURRENT_UPDATE_TRANSACTION Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 169–170

Returns the unique ID of the current transaction when it is in write mode.

## Syntax

```sql
CURRENT_UPDATE_TRANSACTION()
```

## Description

Returns the unique ID (BIGINT) of the current transaction when it is in write mode. If the current transaction is in read mode, the function returns 0.

## Example

The following example returns the current update transaction id.

```sql
SELECT CURRENT_UPDATE_TRANSACTION() "current update transaction" FROM DUMMY;
```
