# 4.9.1.60 CURRENT_UPDATE_STATEMENT_SEQUENCE Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 168–169

Returns the number of write statements that have been issued in a transaction incremented by 1.

## Syntax

```sql
CURRENT_UPDATE_STATEMENT_SEQUENCE()
```

## Description

Returns the number of write statements that have been issued in a transaction incremented by 1. If the transaction has never issued a write transaction, then the function returns 1. The initial value is 1. In a read transaction, the function always returns 1.

## Examples

The following example shows how to retrieve the current write statement sequence number of the current transaction and returns 1:

```sql
CREATE COLUMN TABLE T(id INT);
INSERT INTO T VALUES (1);
SELECT CURRENT_UPDATE_STATEMENT_SEQUENCE() "statement sequence number" FROM
DUMMY;
```

The following statement also returns 1:

```sql
DELETE FROM T;
SELECT CURRENT_UPDATE_STATEMENT_SEQUENCE() "statement sequence number" FROM
DUMMY;
```
