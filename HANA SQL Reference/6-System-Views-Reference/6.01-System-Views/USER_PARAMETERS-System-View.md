# 6.1.179 USER_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1611–1612

Lists all parameters and their values, which have been assigned to users in the system (using CREATE USER ... SET PARAMETER or ALTER USER ... SET PARAMETER).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user. |
| PARAMETER | NVARCHAR(256) | Displays the client parameter name. |
| VALUE | NVARCHAR(5000) | Displays the parameter value. |

## Related Information

[USERS System View](USERS-System-View.md)
