# 6.1.153 SQLSCRIPT_VARIABLE_CACHE System view

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1571–1572

Provides information about procedures and functions that have variable caches defined.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the target object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the target object name. |
| OBJECT_TYPE | VARCHAR(16) | Displays the target object type: PROCE DURE/FUNCTION. |
| VARIABLE_NAME | NVARCHAR(256) | Displays the name of the variable to be cached. |
| VARIABLE_TYPE | VARCHAR(16) | Displays the type of variable. |
| ENABLE_MODE | VARCHAR(16) | Displays the activation mode: ENA BLED, DISABLED, or AUTOMATIC. |

## Related Information

[M_SQLSCRIPT_VARIABLE_CACHE System view](../6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md)
