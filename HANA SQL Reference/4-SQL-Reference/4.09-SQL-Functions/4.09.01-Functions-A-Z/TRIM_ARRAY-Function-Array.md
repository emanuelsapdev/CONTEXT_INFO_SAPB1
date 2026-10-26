# 4.9.1.220 TRIM_ARRAY Function (Array)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 371–372

Removes the specified number of elements from the end of an array.

## Syntax

```sql
TRIM_ARRAY(<array_value_expression>, <truncate_length>)
```

## Syntax Elements

**array_value_expression** Specifies the array that the function removes the elements from. **truncate_length** Specifies the number of elements to remove at the end of the array.

## Description

Returns an array that has a specified number of elements trimmed from the end.

If `<truncate_length>` is less than or equal to 0, then an exception is thrown.

## Example

The following example demonstrates the removal of three elements from an array. The query returns `10`.

```sql
CREATE COLUMN TABLE ARRAY_TEST (IDX INT, VAL INT ARRAY);
INSERT INTO ARRAY_TEST VALUES (1, ARRAY(1, 2, 3));
INSERT INTO ARRAY_TEST VALUES (2, ARRAY(10, 20, 30, 40));
SELECT TRIM_ARRAY(VAL, 3) "trim_array" FROM ARRAY_TEST;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
