# 4.9.1.51 CURRENT_DATE Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 162–163

Returns the current local system date.

## Syntax

```sql
CURRENT_DATE
```

## Description

Returns the current local system date.

It is recommended that you use UTC dates instead of local dates. See to the CURRENT_UTCDATE function for more information.

## Example

The following example returns the local and UTC date of the local system:

```sql
SELECT CURRENT_DATE "Current Date", CURRENT_UTCDATE "Coordinated Universal Date"
FROM DUMMY;
```

|   | **Current Date** | **Coordinated Universal Date** |
| --- | --- | --- |
| 1 | May 1, 2019 | May 1, 2019 |
| `SELECT CURRENT_DATE FROM DUMMY;` | `"Current Date", CURRENT_UTCDATE "Coordinated Universal Date"`<br>**Current Date** | **Coordinated Universal Date** |
| 1 | May 1, 2019 | May 1, 2019 |

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) CURRENT_UTCDATE Function (Datetime) [→](CURRENT_UTCDATE-Function-Datetime.md)
