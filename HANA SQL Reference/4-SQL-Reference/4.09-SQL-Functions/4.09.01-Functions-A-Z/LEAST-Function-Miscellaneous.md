# 4.9.1.109 LEAST Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 231–232

Returns the lesser value of two specified arguments.

## Syntax

```sql
LEAST(<argument_1> [, <argument_2>]...)
```

## Description

Returns the lesser value of the arguments. If one of the arguments is NULL, the return is NULL.

## Example

The following query returns `aa`.

```sql
SELECT LEAST('aa', 'ab', 'ba', 'bb') "least" FROM DUMMY;
```
