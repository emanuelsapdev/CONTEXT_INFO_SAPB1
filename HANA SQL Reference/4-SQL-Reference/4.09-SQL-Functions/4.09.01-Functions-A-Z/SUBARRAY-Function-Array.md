# 4.9.1.186 SUBARRAY Function (Array)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 339–341

Returns a subset of values from the specified array beginning from the specified start position.

## Syntax

```sql
SUBARRAY(<array_value_expression>, <start_position> , <length>)
```

## Description

**array_value_expression** Specifies the array that the function returns the subset of values for. **start_position** Specifies where in the array the subset of values begins. **length** Determines the number of values.

Returns a values set of `<array_value_expression>` starting from the `<start_position>` within the string.

If `<start_position>` is less than or equal to 0, then it is considered as 1.

If the `<length>` is less than or equal to 0, or it is greater than the remaining part of `<array_value_expression>`, then SUBARRAY returns the remaining part from the `<start_position>`.

## Example

The following example returns subsets from the specified array:

```sql
CREATE COLUMN TABLE ARRAY_TEST (IDX INT, VAL INT ARRAY);
INSERT INTO ARRAY_TEST VALUES (1, ARRAY(1, 2, 3));
INSERT INTO ARRAY_TEST VALUES (2, ARRAY(10, 20, 30, 40));
```

The example below generates a subarray that begins with 1 and has a length of 2:

```sql
SELECT SUBARRAY(VAL, 1, 2) "subarray" FROM ARRAY_TEST;
```

The statement above returns the following results:

| **Subarray** |
| --- |
| 1, 2 |
| 10, 20 |
| 1, 2 |
| 10, 20 |

The example below generates a subarray beginning with 1 and with a length of 10:

```sql
SELECT SUBARRAY(VAL, 1, 10) "subarray" FROM ARRAY_TEST;
```

The statement above returns the following results:

| **Subarray** |
| --- |
| 1, 2, 3 |
| 10, 20, 30, 40 |
| 1, 2, 3 |
| 10, 20, 30, 40 |
| 1, 2, 3 |
| 10, 20, 30, 40 |

## Related Information

[Expressions](../../4.06-Expressions.md)
