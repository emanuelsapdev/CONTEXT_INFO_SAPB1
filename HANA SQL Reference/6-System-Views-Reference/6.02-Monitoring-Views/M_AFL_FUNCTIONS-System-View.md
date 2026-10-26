# 6.2.8 M_AFL_FUNCTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1647–1648

Provides application function execution information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| AREA_NAME | NVARCHAR(256) | Displays the area of the function. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the name of the function. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| EXECUTION_COUNT | BIGINT | Displays the number of executions. |
| LAST_EXECUTION_TIMESTAMP | TIMESTAMP | Displays the timestamp of the last execution. |

## Related Information

AFL_FUNCTIONS System View [→](../6.01-System-Views/AFL_FUNCTIONS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](../6.01-System-Views/AFL_FUNCTION_PARAMETERS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](../6.01-System-Views/AFL_FUNCTION_PROPERTIES-System-View.md) AFL_TEXTS System View [→](../6.01-System-Views/AFL_TEXTS-System-View.md) AFL_PACKAGES System View [→](../6.01-System-Views/AFL_PACKAGES-System-View.md) M_AFL_STATES System View [→](M_AFL_STATES-System-View.md)
