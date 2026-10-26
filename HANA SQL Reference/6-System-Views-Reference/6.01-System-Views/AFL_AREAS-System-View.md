# 6.1.6 AFL_AREAS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1405–1406

Provides information about available AFL areas.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| AREA_OID | BIGINT | Displays the object ID of the AFL area. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the AFL area |
| AREA_NAME | NVARCHAR(256) | Displays the name of the AFL area. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the AFL area was created. |

## Related Information

AFL_FUNCTIONS System View [→](AFL_FUNCTIONS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](AFL_FUNCTION_PARAMETERS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](AFL_FUNCTION_PROPERTIES-System-View.md) AFL_PACKAGES System View [→](AFL_PACKAGES-System-View.md) AFL_TEXTS System View [→](AFL_TEXTS-System-View.md) M_AFL_STATES System View [→](../6.02-Monitoring-Views/M_AFL_STATES-System-View.md) M_PLUGIN_STATUS System View [→](../6.02-Monitoring-Views/M_PLUGIN_STATUS-System-View.md) CREATE WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-WORKLOAD-MAPPING-Statement-Workload-Management.md) ALTER WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-WORKLOAD-MAPPING-Statement-Workload-Management.md)
