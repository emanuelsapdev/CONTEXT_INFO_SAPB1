# 6.2.133 M_INIFILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1827–1828

Provides information about all configuration files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| FILE_NAME | VARCHAR(256) | Displays the configuration file name. |
| DEFAULT_LAYER | VARCHAR(5) | Indicates whether or not the file has configuration on the default layer. This value is always TRUE. |
| SYSTEM_LAYER | VARCHAR(5) | Indicates whether or not the file has configuration on the system layer: TRUE/FALSE. |
| DATABASE_LAYER | VARCHAR(5) | Indicates whether or not the file has configuration on the database layer: TRUE/FALSE. |
| HOST_LAYER | VARCHAR(5) | Indicates whether or not the file has configuration on the host layer: TRUE/ FALSE. |

## Additional Information

You can update configuration file settings using the ALTER SYSTEM ALTER CONFIGURATION statement.

## Related Information

M_INIFILE_CONTENTS System View [→](M_INIFILE_CONTENTS-System-View.md) M_INIFILE_CONTENT_HISTORY System View [→](M_INIFILE_CONTENT_HISTORY-System-View.md) ALTER SYSTEM ALTER CONFIGURATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-System-Management.md) ALTER SYSTEM ALTER CONFIGURATION Statement [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/5.02.07-ALTER-SYSTEM-ALTER-CONFIGURATION-DT/README.md)
