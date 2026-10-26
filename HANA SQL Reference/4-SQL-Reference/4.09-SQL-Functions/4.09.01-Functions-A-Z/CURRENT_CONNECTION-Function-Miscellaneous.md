# 4.9.1.50 CURRENT_CONNECTION Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 161–162

Returns the ID of the current connection.

## Syntax

```sql
CURRENT_CONNECTION
```

## Description

Returns the ID of the current connection as an integer value.

This function is called without braces.

## Example

The following query returns the ID of the current connection.

```sql
SELECT CURRENT_CONNECTION "current connection" FROM DUMMY;
```

## Related Information

[M_CONNECTIONS System View](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_CONNECTIONS-System-View.md)
