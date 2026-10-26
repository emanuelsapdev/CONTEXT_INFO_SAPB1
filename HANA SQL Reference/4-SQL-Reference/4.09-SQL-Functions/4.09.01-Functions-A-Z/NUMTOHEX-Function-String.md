# 4.9.1.142 NUMTOHEX Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 272–273

Converts a numeric value to a hexadecimal value.

## Syntax

```sql
NUMTOHEX(<integer> [, <integer>])
```

## Syntax Elements

#### integer

Specifies the numeric value to be converted to a hexadecimal value.

The second parameter controls the length of the target type. If only one parameter is provided, then the length depends on the input type. The second parameter is limited to a 16 hex string length of BIGINT type.

## Description

Converts a numeric value to a hexadecimal value as a VARCHAR data type. The input value can be a TINYINT, SMALLINT, BIGINT, or INTEGER data type.

## Example

The following example converts the numeric value `c1` to a hexadecimal VARCHAR value, `3039`:

```sql
CREATE TABLE t1 (c1 BIGINT);
INSERT INTO t1 VALUES(9223372036854775807);
INSERT INTO t1 VALUES(-9223372036854775808);
INSERT INTO t1 VALUES (-1);
INSERT INTO t1 VALUES (0);
INSERT INTO t1 VALUES (12345);
SELECT c1, NUMTOHEX(c1) FROM t1;
```
