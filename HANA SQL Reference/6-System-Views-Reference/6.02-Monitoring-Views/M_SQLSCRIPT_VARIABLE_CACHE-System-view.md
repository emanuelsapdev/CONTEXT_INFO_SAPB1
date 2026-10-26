# 6.2.273 M_SQLSCRIPT_VARIABLE_CACHE System view

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2017–2018

Provides runtime information about procedures and functions that have variable caches defined.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host address of the node on which the cached data is located. |
| PORT | INTEGER | Displays the port number of the node on which the cached data is located. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the target object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the target object name. |
| OBJECT_TYPE | VARCHAR(16) | Displays the target object type: PROCE DURE/FUNCTION. |
| VARIABLE_NAME | NVARCHAR(256) | Displays the name of the variable to be cached. |
| VARIABLE_TYPE | VARCHAR(16) | Displays the type of variable. |
| SQLSCRIPT_PLAN_ID | INTEGER | Displays the ID of the execution plan. |
| SQLSCRIPT_OPERATOR_ID | INTEGER | Displays the ID of the execution plan operator. |
| MEMORY_SIZE | BIGINT | Displays the memory size of the cached data in bytes. |
| LAST_CACHE_TIME | TIMESTAMP | Displays the date and time when the latest cached data was generated. |

## Related Information

[SQLSCRIPT_VARIABLE_CACHE System view](../6.01-System-Views/SQLSCRIPT_VARIABLE_CACHE-System-view.md)
