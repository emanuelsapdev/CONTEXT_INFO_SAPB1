# 4.9.1.91 HEXTONUM Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 201–202

Converts a hexadecimal value to a BIGINT string value.

## Syntax

```sql
HEXTONUM(<string> [, -1])
```

## Syntax Elements

**string** Specifies the hexadecimal value to be converted to a string value.

#### -1

The result is interpreted as a negative number if a second parameter is provided.

## Description

Converts a hexadecimal value to a string value as a BIGINT data type. The input value can be a VARCHAR or NVARCHAR string type that is no longer than 16 characters.

## Example

The following example converts the hexadecimal value `c2` to a BIGINT string value `12,345`:

```sql
CREATE TABLE t2 (c2 VARCHAR(16));
INSERT INTO t2 VALUES('7FFFFFFFFFFFFFFF');
INSERT INTO t2 VALUES('8000000000000000');
INSERT INTO t2 VALUES ('FFFFFFFFFFFFFFFF');
INSERT INTO t2 VALUES ('0');
INSERT INTO t2 VALUES ('3039');
SELECT c2, HEXTONUM(c2) FROM t2;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
