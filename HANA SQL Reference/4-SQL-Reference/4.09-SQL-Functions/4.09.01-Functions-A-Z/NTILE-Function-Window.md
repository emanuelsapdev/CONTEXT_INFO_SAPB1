# 4.9.1.140 NTILE Function (Window)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 269–271

Distributes rows into a specified number of buckets and assigns the bucket number starting from 1 to each row in the bucket.

## Syntax

```sql
NTILE( <number_of_buckets> ) <window_specification>
```

## Syntax Elements

#### number_of_buckets

Specifies the number of buckets to distribute rows to.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

The output of NTILE function can be non-deterministic among tie values.

## Examples

```sql
CREATE ROW TABLE T (class CHAR(10), val INT, offset INT);
 INSERT INTO T VALUES('A', 1, 1);
 INSERT INTO T VALUES('A', 3, 3);
 INSERT INTO T VALUES('A', 5, null);
 INSERT INTO T VALUES('A', 5, 2);
 INSERT INTO T VALUES('A', 10, 0);
 INSERT INTO T VALUES('B', 1, 3);
 INSERT INTO T VALUES('B', 1, 1);
 INSERT INTO T VALUES('B', 7, 1);
SELECT class, val,
  NTILE(3) OVER (PARTITION BY class ORDER BY val) AS NTILE,
  FIRST_VALUE(val) OVER (PARTITION BY class ORDER BY val) AS first,
  LAST_VALUE(val) OVER (PARTITION BY class ORDER BY val) AS last,
  NTH_VALUE(val, 4) OVER (PARTITION BY class ORDER BY val) AS nth
 FROM T;
```

| **CLASS** | **VAL** | **NTILE** | **FIRST** | **LAST** | **NTH** |
| --- | --- | --- | --- | --- | --- |
| A | 1 | 1 | 1 | 1 | null |
| A | 3 | 1 | 1 | 3 | null |
| A | 5 | 2 | 1 | 5 | 5 |
| A | 5 | 2 | 1 | 5 | 5 |
| A | 10 | 3 | 1 | 10 | 5 |
| B | 1 | 1 | 1 | 1 | null |
| B | 1 | 2 | 1 | 1 | null |
| B | 7 | 3 | 1 | 7 | null |

## Related Information

Expressions [→](../../4.06-Expressions.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md)
