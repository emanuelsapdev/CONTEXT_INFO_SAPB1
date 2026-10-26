# 4.9.1.183 STDDEV_SAMP Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 336–337

Returns the standard deviation of the given expression as the square root of VAR_SAMP function.

## Syntax

```sql
STDDEV_SAMP(<expression>)
```

## Description

Returns the standard deviation of the given `<expression>` as the square root of the VAR_SAMP function.

## Examples

The following example returns `NULL` for the standard deviation of the specified expression, as the square root of the VAR_SAMP function:

```sql
CREATE ROW TABLE RTABLE (A INT);
INSERT INTO RTABLE VALUES (1);
SELECT STDDEV_SAMP(A) "STDDEVSAMP" FROM RTABLE;
```

The following example returns `0.707107` for the standard deviation of the specified expression, as the square root of VAR_SAMP function:

```sql
INSERT INTO RTABLE VALUES (2);
SELECT STDDEV_SAMP(A) "STDDEVSAMP" FROM RTABLE;
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) STDDEV Function (Aggregate) [→](STDDEV-Function-Aggregate.md) STDDEV_POP Function (Aggregate) [→](STDDEV_POP-Function-Aggregate.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md)
