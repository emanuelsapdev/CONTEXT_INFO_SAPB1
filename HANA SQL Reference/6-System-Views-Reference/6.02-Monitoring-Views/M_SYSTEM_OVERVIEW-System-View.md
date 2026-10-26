# 6.2.298 M_SYSTEM_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2065

Provides an overview of system status including important resource usage information and alerts.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SECTION | VARCHAR(16) | Displays the section name. |
| NAME | VARCHAR(32) | Displays the key name in section. |
| STATUS | VARCHAR(8) | Displays the status value: OK, ERROR, or WARNING. This row is empty for info items. |
| VALUE | VARCHAR(256) | Displays the key value in section. |

## Related Information

[System Limitations](../../4-SQL-Reference/4.11-System-Limitations.md)
