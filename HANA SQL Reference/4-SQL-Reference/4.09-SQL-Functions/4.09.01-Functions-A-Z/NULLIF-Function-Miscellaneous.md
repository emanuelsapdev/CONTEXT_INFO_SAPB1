# 4.9.1.141 NULLIF Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 271–272

Determines whether two expressions are equal.

## Syntax

```sql
NULLIF(<expression1>, <expression2>)
```

## Description

NULLIF compares the values of two expressions and returns NULL if `<expression1>` equals `<expression2>`.

If `<expression1>` does not equal `<expression2>`, then NULLIF returns `<expression1>`.

If `<expression2>` is NULL, then NULLIF returns `<expression1>`.

NULLIF returns the same data type as `<expression1>`. However, if `<expression1>` is either TINYINT or SMALLINT, then NULLIF returns an INTEGER.

## Example

The following query returns `diff`.

```sql
SELECT NULLIF ('diff', 'same') "nullif" FROM DUMMY;
```

The following query returns `NULL`.

```sql
SELECT NULLIF('same', 'same') "nullif" FROM DUMMY;
```
