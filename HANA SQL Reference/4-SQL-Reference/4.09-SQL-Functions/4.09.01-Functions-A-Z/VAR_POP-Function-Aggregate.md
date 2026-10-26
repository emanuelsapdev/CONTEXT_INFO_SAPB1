# 4.9.1.227 VAR_POP Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 378–379

Returns the population variance of an expression.

## Syntax

```sql
VAR_POP(<expression>)
```

## Description

Returns the population variance of the expression as the sum of squares of the difference of `<expression>` from the mean of `<expression>`, divided by the number of rows remaining.

## Examples

The following example returns `0.2` as the population variance for the specified expression:

```sql
CREATE ROW TABLE RTABLE (A INT);
INSERT INTO RTABLE VALUES (1);
SELECT VAR_POP(A) "VARPOP" FROM RTABLE;
```

The following example returns `0.24` as the population variance for the specified expression:

```sql
INSERT INTO RTABLE VALUES (2);
SELECT VAR_POP(A) "VARPOP" FROM RTABLE;
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) VAR Function (Aggregate) [→](VAR-Function-Aggregate.md) VAR_SAMP Function (Aggregate) [→](VAR_SAMP-Function-Aggregate.md) Expressions [→](../../4.06-Expressions.md)
