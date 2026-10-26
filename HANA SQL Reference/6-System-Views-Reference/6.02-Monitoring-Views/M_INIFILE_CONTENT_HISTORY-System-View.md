# 6.2.135 M_INIFILE_CONTENT_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1829–1830

Provides change history information for configuration (ini) files.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TIME | TIMESTAMP | Displays the timestamp when the configuration setting was changed. |
| FILE_NAME | VARCHAR(256) | Displays the name of the configuration file. |
| LAYER_NAME | VARCHAR(16) | Displays the configuration layer: DE FAULT, SYSTEM, HOST, or DATABASE. |
| HOST | VARCHAR(64) | Displays the host name, if the LAYER_NAME is HOST. Otherwise, this value is NULL. |
| USER_NAME | NVARCHAR(256) | Displays the user name if the change was made by an SAP HANA user. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the value of the APPLICATION session variable, if an application made the change. Otherwise, this value is NULL. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the value of the APPLICATIO NUSER session variable, if an application made the change. Otherwise, this value is NULL. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the name of the application source if an application made the change. Otherwise, this value is NULL. |
| SECTION | VARCHAR(128) | Displays the name of the section in the configuration file where the change was made. |
| KEY | VARCHAR(128) | Displays the name of the configuration key that was changed. |
| VALUE | VARCHAR(5000) | Displays the new configuration value. |
| PREV_VALUE | VARCHAR(5000) | Displays the value of the configuration parameter before the change was made. |
| COMMENTS | NVARCHAR(5000) | Displays the comment provided, if any, at the time of the configuration change. |

## Related Information

ALTER SYSTEM CLEAR INIFILE CONTENT HISTORY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-INIFILE-CONTENT-HISTORY-Statement-System.md) M_INIFILES System View [→](M_INIFILES-System-View.md) M_INIFILE_CONTENTS System View [→](M_INIFILE_CONTENTS-System-View.md) ALTER SYSTEM ALTER CONFIGURATION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-CONFIGURATION-Statement-System-Management.md)
