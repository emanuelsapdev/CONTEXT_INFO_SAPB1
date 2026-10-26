# 4.9.1.58 CURRENT_TIMESTAMP Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 167–168

Returns the current local system timestamp information.

## Syntax

```sql
CURRENT_TIMESTAMP
```

## Description

Returns the current local system timestamp information.

It is recommended that you use UTC timestamps instead of local timestamps. See to the CURRENT_UTCTIMESTAMP function for more information.

## Example

The following example returns the local and UTC timestamp of the system:

```sql
SELECT CURRENT_TIMESTAMP "Current Timestamp", CURRENT_UTCTIMESTAMP "Coordinated
Universal Timestamp" FROM DUMMY;
```

|   | **Current Timestamp** | **Coordinated Universal Timestamp** |
| --- | --- | --- |
| 1 | May 1, 2019 7:56:51.5 AM | May 1, 2019 2:56:51.5 PM |

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) CURRENT_UTCTIMESTAMP Function (Datetime) [→](CURRENT_UTCTIMESTAMP-Function-Datetime.md)
