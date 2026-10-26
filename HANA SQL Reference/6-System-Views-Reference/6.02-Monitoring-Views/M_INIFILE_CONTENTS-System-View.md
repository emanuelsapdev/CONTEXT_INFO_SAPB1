# 6.2.134 M_INIFILE_CONTENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1828–1829

Provides configuration information from INI files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| FILE_NAME | VARCHAR(256) | Displays the configuration file name. |
| LAYER_NAME | VARCHAR(16) | Displays the configuration layer: DE FAULT, SYSTEM, HOST or DATABASE. |
| TENANT_NAME | VARCHAR(256) | Deprecated. |
| HOST | VARCHAR(64) | Displays the host name, if the LAYER_NAME is HOST. Otherwise, this value is NULL. |
| SECTION | VARCHAR(128) | Displays the configuration section name. |
| KEY | VARCHAR(128) | Displays the configuration key name. |
| VALUE | VARCHAR(5000) | Displays the configuration value. |

## Related Information

M_INIFILES System View [→](M_INIFILES-System-View.md) M_INIFILE_CONTENT_HISTORY System View [→](M_INIFILE_CONTENT_HISTORY-System-View.md) ALTER SYSTEM ALTER CONFIGURATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-System-Management.md)
