# 6.1.118 PSES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1537

Provides information about personal security environments (PSE).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PSE_ID | BIGINT | Displays the unique ID of the PSE. |
| NAME | NVARCHAR(256) | Displays the name of the PSE. |
| PURPOSE | VARCHAR(16) | Displays the purpose of the PSE. |
| OWNER_NAME | NVARCHAR(256) | Displays the owner of the PSE. |

## Related Information

PSE_CERTIFICATES System View [→](PSE_CERTIFICATES-System-View.md) PSE_PURPOSE_OBJECTS System View [→](PSE_PURPOSE_OBJECTS-System-View.md) CREATE PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PSE-Statement-System-Management.md) SET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-PSE-Statement-System-Management.md) UNSET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-PSE-Statement-System-Management.md) ALTER PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-PSE-Statement-System-Management.md) DROP PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-PSE-Statement-System-Management.md)
