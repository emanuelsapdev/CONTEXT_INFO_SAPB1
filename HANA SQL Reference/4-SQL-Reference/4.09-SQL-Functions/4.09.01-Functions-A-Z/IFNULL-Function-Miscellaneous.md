# 4.9.1.93 IFNULL Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 203–204

Returns the first non-NULL input expression.

## Syntax

```sql
IFNULL(<expression1>, <expression2>)
```

## Description

IFNULL returns the first non-NULL input expression. If the data types of `<expression1>` and `<expression2>` are different, then SAP HANA chooses the data type with the higher precedence. For example, between TIMESTAMP and STRING, TIMESTAMP has the higher precedence. See the data types documentation for more information about data type precedence.

- Returns `<expression1>` if `<expression1>` is not NULL.
- Returns `<expression2>` if `<expression1>` is NULL.
- Returns NULL if both input expressions are NULL.

## Example

The following query returns `diff`:

```sql
SELECT IFNULL ('diff', 'same') "ifnull" FROM DUMMY;
```

The following query returns `same`:

```sql
SELECT IFNULL (NULL, 'same') "ifnull" FROM DUMMY;
```

The following query returns `NULL`:

```sql
SELECT IFNULL (NULL, NULL) "ifnull" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Data Types [→](../../4.03-Data-Types/README.md)
