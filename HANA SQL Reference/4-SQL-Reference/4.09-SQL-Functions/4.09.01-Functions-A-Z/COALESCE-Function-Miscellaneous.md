# 4.9.1.36 COALESCE Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 124–125

Returns the first non-NULL expression from a specified list.

## Syntax

```sql
COALESCE(<expression_list>)
```

## Syntax Elements

**expression_list** Specifies the expressions to return the first non-NULL expression from.

## Description

Returns the first non-NULL expression from a list. At least two expressions must be contained in `<expression_list>`, and all expressions must be comparable. The result is NULL if all the expressions are NULL.

## Example

```sql
CREATE ROW TABLE coalesce_example (ID INT PRIMARY KEY, A REAL, B REAL);
 INSERT INTO coalesce_example VALUES(1, 100, 80);
 INSERT INTO coalesce_example VALUES(2, NULL, 63);
 INSERT INTO coalesce_example VALUES(3, NULL, NULL);
 SELECT id, a, b, COALESCE (a, b*1.1, 50.0) "coalesce" FROM coalesce_example;
```

The example above returns the results below:

| **ID** | **A** | **B** | **coalesce** |
| --- | --- | --- | --- |
| 1 | 100.0 | 80.0 | 100.0 |
| 2 | NULL | 63.0 | 69.30000305175781 |
| 3 | NULL | NULL | 50.0 |

## Related Information

[Expressions](../../4.06-Expressions.md)
