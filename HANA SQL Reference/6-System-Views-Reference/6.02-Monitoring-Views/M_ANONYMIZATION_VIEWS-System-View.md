# 6.2.11 M_ANONYMIZATION_VIEWS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1650–1651

Provides runtime information about anonymized views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the anonymized view. |
| ANONYMIZATION_STATUS | VARCHAR(16) | Displays the status of the anonymized view.<br>Possible values for views anonymized using the DIFFERENTIAL_PRIVACY algorithm are READY, INVALID, or RE FRESHING.<br>Possible values for views anonymized using the K-ANONYMITY and L-DIVER SITY algorithm are CREATED, RE FRESHING, READY, or INVALID. |
| REFRESH_RECOMMENDED | VARCHAR(5) | Displays whether a refresh is recommended: TRUE/FALSE. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the finish time of the latest refresh. |
| LAST_REFRESH_PARAMETERS | NCLOB | Displays the parameters specified during the last REFRESH VIEW command on the view, in JSON format |

## Related Information

ANONYMIZATION_VIEWS System View [→](../6.01-System-Views/ANONYMIZATION_VIEWS-System-View.md) ANONYMIZATION_VIEW_COLUMNS System View [→](../6.01-System-Views/ANONYMIZATION_VIEW_COLUMNS-System-View.md) VIEWS System View [→](../6.01-System-Views/VIEWS-System-View.md) CREATE VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIEW-Statement-Data-Definition.md) ALTER VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIEW-Statement-Data-Definition.md) REFRESH VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-VIEW-Statement-Data-Definition.md)
