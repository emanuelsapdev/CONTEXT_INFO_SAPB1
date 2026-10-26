# 4.9.1.127 MINUTE Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 257–258

Returns an integer representation of the minute for the specified time.

## Syntax

```sql
MINUTE(<time>)
```

## Description

Returns an integer representation of the minute for time `<time>`.

## Example

The following example returns the value `34` as the minute for the specified time:

```sql
SELECT MINUTE ('12:34:56') "minute" FROM DUMMY;
```

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
