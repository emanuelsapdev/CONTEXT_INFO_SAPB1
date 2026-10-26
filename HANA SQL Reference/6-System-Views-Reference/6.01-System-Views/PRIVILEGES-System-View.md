# 6.1.111 PRIVILEGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1529–1530

Provides information about available privileges.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| NAME | NVARCHAR(256) | Displays the privilege name. |
| TYPE | VARCHAR(32) | Displays the privilege type: SYSTEM PRIVILEGE, OBJECTPRIVILEGE, PACK AGEPRIVILEGE, or APPLICATIONPRIVI LEGE |

## Related Information

GRANTED_PRIVILEGES System View [→](GRANTED_PRIVILEGES-System-View.md) OBJECT_PRIVILEGES System View [→](OBJECT_PRIVILEGES-System-View.md) GRANT Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md)
