# 4.9.1.57 CURRENT_TIME Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 166–167

Returns the local system time.

## Syntax

```sql
CURRENT_TIME
```

## Description

Returns the current local system time.

It is recommended that you use UTC times instead of local times. See to the CURRENT_UTCTIME function for more information.

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

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) CURRENT_UTCTIME Function (Datetime) [→](CURRENT_UTCTIME-Function-Datetime.md)
