# 6.2.9 M_AFL_STATES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1648–1649

Provides information about AFL states.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STATE_ID | NVARCHAR(256) | Displays the ID of the state. |
| AREA_NAME | NVARCHAR(256) | Displays the name of the area. |
| DESCRIPTION | NVARCHAR(256) | Displays the state description. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the time when the state was created. |
| LAST_ACCESS_TIMESTAMP | TIMESTAMP | Displays the time stamp of the last access. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

M_AFL_FUNCTIONS System View [→](M_AFL_FUNCTIONS-System-View.md) AFL_FUNCTIONS System View [→](../6.01-System-Views/AFL_FUNCTIONS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](../6.01-System-Views/AFL_FUNCTION_PARAMETERS-System-View.md) AFL_PACKAGES System View [→](../6.01-System-Views/AFL_PACKAGES-System-View.md) AFL_TEXTS System View [→](../6.01-System-Views/AFL_TEXTS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](../6.01-System-Views/AFL_FUNCTION_PROPERTIES-System-View.md)
