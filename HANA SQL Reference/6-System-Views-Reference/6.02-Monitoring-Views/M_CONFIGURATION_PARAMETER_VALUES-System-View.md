# 6.2.44 M_CONFIGURATION_PARAMETER_VALUES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1685–1686

Displays landscape service parameter values.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SECTION | VARCHAR(128) | Displays the section of the parameter. |
| KEY | VARCHAR(128) | Displays the parameter key. |
| HAS_KEY_INDEX | VARCHAR(5) | Displays whether or not the parameter is an indexed parameter: TRUE/FALSE. |
| FILE_NAME | VARCHAR(16) | Displays the name of the file where the parameter value is defined. |
| LAYER_NAME | VARCHAR(8) | Displays that layer that the parameter is defined on. |
| VALUE | NVARCHAR(5000) | Displays the parameter value. |
| HAS_PROPERTIES | VARCHAR(5) | Displays whether or not the parameter has properties: TRUE or FALSE. |
| RAW_VALUE | NVARCHAR(5000) | Displays the raw string value of the parameter as it is cached in the service. |
| VIOLATED_RESTRICTIONS | VARCHAR(64) | Displays the restrictions violated by the set value: CUSTOM, VALUE_RESTRICTION, or LAYER_RESTRICTION. |
| RESTART_REQUIRED | VARCHAR(5) | Displays if the parameter value has been changed and requires a restart to become effective: TRUE/FALSE. |

## Related Information

[CONFIGURATION_PARAMETER_PROPERTIES System View](../6.01-System-Views/CONFIGURATION_PARAMETER_PROPERTIES-System-View.md)

ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/README.md) ALTER SYSTEM ALTER CONFIGURATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-System-Management.md) ALTER SYSTEM ALTER CONFIGURATION Statement [Accelerator for SAP ASE] [→](../../5-Additional-SAP-HANA-Contexts/5.01-Accelerator-for-SAP-ASE/5.01.02-ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-Accelerator-for.md)
