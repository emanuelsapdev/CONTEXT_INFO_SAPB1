# 4.9.1.138 NOW Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 267–268

Returns the current timestamp.

## Syntax

```sql
NOW()
```

## Description

Returns the current timestamp.

## Example

The following example returns a value similar to `2010-01-01 16:34:19.894` for the current timestamp:

```sql
SELECT NOW () "now" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
