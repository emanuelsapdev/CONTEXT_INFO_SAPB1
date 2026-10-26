# 4.9.1.65 CURRENT_UTCTIME Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 173

Returns the current UTC time.

## Syntax

```sql
CURRENT_UTCTIME
```

## Description

Returns the current UTC time.

## Example

The following example returns the local and UTC time of the system:

```sql
SELECT CURRENT_TIME "Current Time", CURRENT_UTCTIME "Coordinated Universal Time"
FROM DUMMY;
```

|   | **Current Time** | **Coordinated Universal Time** |
| --- | --- | --- |
| 1 | 7:56:51 AM | 2:56:51 PM |

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
