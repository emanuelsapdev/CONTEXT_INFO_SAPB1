# 6.2.238 M_RESULT_CACHE_EXCLUSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1967

Provides information about result cache exclusions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| REASON | NVARCHAR(1024) | Displays the reason why the object can not use result cache. |
| EXCLUDE_TIME | TIMESTAMP | Displays the timestamp when disabling the result cache was decided. |

## Related Information

[M_RESULT_CACHE System View](M_RESULT_CACHE-System-View.md)
