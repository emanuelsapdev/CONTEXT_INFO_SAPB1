# 4.9.1.84 GREATEST Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 192

Returns the greatest value among the specified arguments.

## Syntax

```sql
GREATEST(<argument> [{, <argument>}...])
```

## Description

Returns the greatest value among the arguments (n1, n2, ...). If one of the arguments is NULL, the return is NULL.

## Example

The following example returns bb as the greatest value:

```sql
SELECT GREATEST ('aa', 'ab', 'ba', 'bb') "greatest" FROM DUMMY;
```
