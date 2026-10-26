# 4.9.1.124 MEMBER_AT Function (Array)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 253–254

Returns values from a specified array position.

## Syntax

```sql
MEMBER_AT(<array_value_expression>, <position> [, <default_value>])
```

## Description

Accesses an array element at the specified ordinal position and returns the value.

`<default_value>` indicates the value to return if `<position>` is greater than the cardinality of the `<array_value_expression>`. If `<default_value>` is not specified, and `<position>` is greater than the cardinality of the `<array_value_expression>`. then NULL is returned.

## Example

The following example creates a table and inserts arrays into it:

```sql
CREATE COLUMN TABLE ARRAY_TEST (IDX INT, VAL INT ARRAY);
INSERT INTO ARRAY_TEST VALUES (1, ARRAY(1, 2, 3));
INSERT INTO ARRAY_TEST VALUES (2, ARRAY(10, 20, 30, 40));
```

The following example returns the value in position 4 of each array in the table. The first array does not have a position 4, so NULL is returned:

```sql
SELECT MEMBER_AT(VAL, 4) "member_at" FROM ARRAY_TEST;
```

| **member_at** |
| --- |
| ? |
| 40 |

The following example returns the value in position 4 of each array in the table. The first array does not have a position 4, so 1 is returned `<position>` is greater than the cardinality of the array:

```sql
SELECT MEMBER_AT(VAL, 4, 1) "member_at" FROM ARRAY_TEST;
```

| **member_at** |
| --- |
| 1 |
| 40 |

## Related Information

[Expressions](../../4.06-Expressions.md)
