# 4.9.1.215 TO_TIME Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 366–367

Converts a specified time string to a TIME data type.

## Syntax

```sql
TO_TIME(<time> [, <format>])
```

## Description

Converts time string `<time>` to the TIME data type.

If the `<format>` specifier is omitted, then the conversion is performed using the time format model.

## Example

The following example converts the value `08:30 AM` to a TIME value with format `HH:MI AM` and returns the value `08:30:00`:

```sql
SELECT TO_TIME ('08:30 AM', 'HH:MI AM') "to time" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
