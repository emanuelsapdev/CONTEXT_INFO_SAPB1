# 6.1.69 EPM_MODELS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1481–1482

Provides information about available EPM Models.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the EPM Model. |
| MODEL_NAME | NVARCHAR(256) | Displays the name of the EPM Model. |
| COMMENTS | NVARCHAR(256) | Displays the description of the EPM Model. |
| CDATA | NCLOB | Displays the definition of the EPM Model with JSON representation. |

## Related Information

EPM_QUERY_SOURCES System View [→](EPM_QUERY_SOURCES-System-View.md) M_EPM_SESSIONS System View [→](../6.02-Monitoring-Views/M_EPM_SESSIONS-System-View.md)
