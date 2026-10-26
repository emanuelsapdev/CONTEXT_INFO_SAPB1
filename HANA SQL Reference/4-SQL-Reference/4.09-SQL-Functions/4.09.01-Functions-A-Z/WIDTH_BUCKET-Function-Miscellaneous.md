# 4.9.1.232 WIDTH_BUCKET Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 384–385

Returns the bucket number that has been assigned to the result of a specified expression.

## Syntax

```sql
WIDTH_BUCKET(<expression>, <min_value>, <max_value>, <num_buckets>)
```

## Syntax Elements

**expression** Specifies the value that the histogram is created for. `<expression>` must be a numeric or datetime value, or a value that can be implicitly converted to a numeric or datetime value. If `<expression>` evaluates to NULL, then `<expression>` returns NULL. **min_value** Specifies the minimum endpoint range for `<expression>`. `<min_value>` must be a numeric or datetime value and cannot evaluate to NULL. **max_value** Specifies the maximum endpoint range for `<expression>`. `<max_value>` must be a numeric or datetime value and cannot evaluate to NULL. **num_buckets** Specifies the number of buckets to distribute values across. `<num_buckets>` must be a positive integer.

## Description

The returned bucket number is an integer between 0 and `<num_buckets>` +1. This function always returns `<num_buckets>` plus two additional buckets: bucket 0 and `<num_buckets>`+1. Bucket 0 contains the count of values less than `<min_value>` and bucket `<num_buckets>` +1 contains the count of values greater than or equal to `<max_value>`.

## Example

The following example returns the bucket numbers for `myTable`:

```sql
CREATE TABLE myTable (myValues INT);
INSERT INTO myTable VALUES(1);
INSERT INTO myTable VALUES(2);
INSERT INTO myTable VALUES(3);
INSERT INTO myTable VALUES(4);
INSERT INTO myTable VALUES(5);
SELECT myValues, WIDTH_BUCKET( myValues, 2, 5, 2 ) AS "BucketNo" FROM myTable;
```

| **myValues** | **BucketNo** |
| --- | --- |
| 1 | 0 |
| 2 | 1 |
| 3 | 1 |
| 4 | 2 |
| 75 | 3 |

## Related Information

[Expressions](../../4.06-Expressions.md)
