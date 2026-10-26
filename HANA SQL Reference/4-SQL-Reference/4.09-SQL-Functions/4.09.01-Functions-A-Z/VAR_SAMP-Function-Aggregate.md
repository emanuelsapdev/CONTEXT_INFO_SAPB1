# 4.9.1.228 VAR_SAMP Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 379–380

Returns the sample variance of an expression.

## Syntax

```sql
VAR_SAMP(<expression>)
```

## Description

Returns the sample variance of the expression as the sum of squares of the difference of `<expression>` from the mean of `<expression>`, divided by the number of rows remaining minus 1. This function is similar to VAR, the only difference is that it returns NULL when the number of rows is 1.

## Examples

The following example returns `NULL` as the sample variance of the specified expression:

```sql
CREATE ROW TABLE RTABLE (A INT);
INSERT INTO RTABLE VALUES (1);
SELECT VAR_SAMP(A)"VARSAMP" FROM RTABLE;
```

The following example returns `0.3` as the sample variance of the specified expression:

```sql
INSERT INTO RTABLE VALUES (2);
SELECT VAR_SAMP(A) "VARSAMP" FROM RTABLE;
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) VAR Function (Aggregate) [→](VAR-Function-Aggregate.md) VAR_POP Function (Aggregate) [→](VAR_POP-Function-Aggregate.md) Expressions [→](../../4.06-Expressions.md)
