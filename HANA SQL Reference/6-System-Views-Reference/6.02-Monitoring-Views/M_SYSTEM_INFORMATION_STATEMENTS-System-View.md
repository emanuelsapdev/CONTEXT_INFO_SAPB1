# 6.2.296 M_SYSTEM_INFORMATION_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2064

Provides system information statements.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| NAME | VARCHAR(64) | Displays the statement name. |
| DESCRIPTION | NVARCHAR(256) | Displays the statement description. |
| STATEMENT | NCLOB | Displays the actual SQL statement. |
