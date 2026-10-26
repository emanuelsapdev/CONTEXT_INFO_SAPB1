# 4.9.1.64 CURRENT_UTCDATE Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 172–173

Returns the current UTC date.

## Syntax

```sql
CURRENT_UTCDATE
```

## Description

Returns the current UTC date.

In application code, it is recommended that you use UTC dates instead of local dates.

## Example

The following example returns the local and UTC date of the local system:

```sql
SELECT CURRENT_DATE "Current Date", CURRENT_UTCDATE "Coordinated Universal Date"
FROM DUMMY;
```

|   | **Current Date** | **Coordinated Universal Date** |
| --- | --- | --- |
| 1 | May 1, 2019 | May 1, 2019 |

## Related Information

[Datetime Data Types](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
