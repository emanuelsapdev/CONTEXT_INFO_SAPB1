# 6.2.297 M_SYSTEM_LIMITS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2064–2065

Provides system limit information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CATEGORY | VARCHAR(128) | Displays whether the category of the system limit is adaptable. |
| NAME | NVARCHAR(256) | Displays the name of the system limit. |
| VALUE | VARCHAR(256) | Displays the value of the system limit. |
| TYPE | VARCHAR(128) | Displays the type of value. |
| UNIT | VARCHAR(256) | Displays the unit of value. |
| COMMENT | VARCHAR(2000) | Displays any additional comments for system limits. |

## Related Information

[System Limitations](../../4-SQL-Reference/4.11-System-Limitations.md)
