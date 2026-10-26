# 6.2.293 M_STREAMING_SERVICES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2058

Provides streaming service monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SERVICE_ALIAS | NVARCHAR(256) | Displays the name of the SAP HANA streaming node. |
| HOST | VARCHAR(64) | Displays the name of the host. |
| PORT | INTEGER | Displays the internal port. |

## Related Information

M_SERVICES System View [→](M_SERVICES-System-View.md) ALTER SYSTEM RECONFIGURE SERVICE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECONFIGURE-SERVICE-Statement-System-Management.md) ALTER SYSTEM STOP SERVICE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-STOP-SERVICE-Statement-System-Management.md)
