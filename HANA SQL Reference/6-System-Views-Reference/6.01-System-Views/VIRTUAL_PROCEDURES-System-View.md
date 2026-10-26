# 6.1.189 VIRTUAL_PROCEDURES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1624–1625

Provides the list of virtual procedures.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the virtual procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the name of the virtual procedure. |
| PROCEDURE_OID | BIGINT | Displays the object ID of the virtual procedure. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name used in the procedure. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the name of the remote source adapter. |
| PROCEDURE_CONFIGURATION | NCLOB | Displays the virtual procedure configuration. |
| IS_VALID | VARCHAR(5) | Displays whether the virtual procedure is valid: TRUE/FALSE. |

## Related Information

CREATE VIRTUAL PROCEDURE Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-PROCEDURE-Statement-Procedural.md) CREATE VIRTUAL PROCEDURE Statement [Smart Data Integration]
