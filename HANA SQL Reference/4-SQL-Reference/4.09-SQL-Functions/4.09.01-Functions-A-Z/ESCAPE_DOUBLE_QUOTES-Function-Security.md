# 4.9.1.76 ESCAPE_DOUBLE_QUOTES Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 185

Escapes double quotes in the specified string.

## Syntax

```sql
ESCAPE_DOUBLE_QUOTES(<value>)
```

## Description

Escapes double quotes in the `<value>` string, ensuring that a valid SQL identifier is used in dynamic SQL statements to prevent SQL injections. The function returns the input string with escaped double quotes.

## Example

The following query escapes the double quotes and returns the value `TAB""LE`.

```sql
SELECT ESCAPE_DOUBLE_QUOTES('TAB"LE') "table_name" FROM DUMMY;
```
