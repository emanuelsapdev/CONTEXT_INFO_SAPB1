# 6.1.17 ANONYMIZATION_VIEWS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1418–1419

Provides information about anonymized views in the SAP HANA database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the anonymized view. |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the anonymized view. |
| ALGORITHM | VARCHAR(32) | Displays the algorithm used to anonymize the view: K-ANONYMITY/DIFFEREN TIAL PRIVACY. |
| PARAMETERS | NCLOB | Displays the view-level anonymization parameters defined for the view, in JSON format. |

## Related Information

ANONYMIZATION_VIEW_COLUMNS System View [→](ANONYMIZATION_VIEW_COLUMNS-System-View.md) M_ANONYMIZATION_VIEWS System View [→](../6.02-Monitoring-Views/M_ANONYMIZATION_VIEWS-System-View.md) VIEWS System View [→](VIEWS-System-View.md) CREATE VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIEW-Statement-Data-Definition.md) ALTER VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIEW-Statement-Data-Definition.md) REFRESH VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-VIEW-Statement-Data-Definition.md)
