# 4.9.1.32 CARDINALITY Function (Array)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 120–121

Returns the number of elements in a specified array.

## Syntax

```sql
CARDINALITY(<array_value_expression>)
```

## Syntax Elements

**array_value_expression** Specifies the array that the function returns the number of elements for.

## Description

Returns the number of elements in `<array_value_expression>`.

## Example

The following example returns the number of elements (3 and 4, respectively) contained in two arrays.

```sql
CREATE COLUMN TABLE ARRAY_TEST (IDX INT, VAL INT ARRAY);
INSERT INTO ARRAY_TEST VALUES (1, ARRAY(1, 2, 3));
INSERT INTO ARRAY_TEST VALUES (2, ARRAY(10, 20, 30, 40));
SELECT CARDINALITY(VAL) "cardinality" FROM ARRAY_TEST;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
