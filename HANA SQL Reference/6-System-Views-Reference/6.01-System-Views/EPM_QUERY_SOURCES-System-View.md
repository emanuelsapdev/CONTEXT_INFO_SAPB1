# 6.1.70 EPM_QUERY_SOURCES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1482

Provides information about available EPM query source.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the EPM query source. |
| QUERY_SOURCE_NAME | NVARCHAR(256) | Displays the name of the EPM query source. |
| COMMENTS | NVARCHAR(256) | Displays the description of the EPM query source. |
| CDATA | NCLOB | Displays the definition of the EPM query source with JSON representation. |

## Related Information

EPM_MODELS System View [→](EPM_MODELS-System-View.md) M_EPM_SESSIONS System View [→](../6.02-Monitoring-Views/M_EPM_SESSIONS-System-View.md)
