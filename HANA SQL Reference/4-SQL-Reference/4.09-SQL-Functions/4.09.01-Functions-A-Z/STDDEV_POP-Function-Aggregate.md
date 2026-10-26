# 4.9.1.182 STDDEV_POP Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 335–336

Returns the standard deviation of a given expression as the square root of the VAR_POP function.

## Syntax

```sql
STDDEV_POP(<expression>)
```

## Description

Returns the standard deviation of the given expression as the square root of the VAR_POP function.

## Examples

The following example returns `0` for the standard deviation of the specified expression:

```sql
CREATE ROW TABLE RTABLE (A INT);
INSERT INTO RTABLE VALUES (1);
SELECT STDDEV_POP(A) "STDDEVPOP" FROM RTABLE;
```

The following examples returns `0.5` for the standard deviation of the specified expression:

```sql
INSERT INTO RTABLE VALUES (2);
SELECT STDDEV_POP(A) "STDDEVPOP" FROM RTABLE;
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) STDDEV Function (Aggregate) [→](STDDEV-Function-Aggregate.md) STDDEV_SAMP Function (Aggregate) [→](STDDEV_SAMP-Function-Aggregate.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md)
