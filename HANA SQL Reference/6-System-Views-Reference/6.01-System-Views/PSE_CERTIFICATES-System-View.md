# 6.1.119 PSE_CERTIFICATES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1537–1538

Provides information about certificates used in PSEs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PSE_NAME | NVARCHAR(256) | Displays the name of the PSE. |
| CERTIFICATE_ID | BIGINT | Displays the unique ID of the certificate. |
| SUBJECT_NAME | NVARCHAR(5000) | Displays the subject of the X.509 certificate. |
| ISSUER_NAME | NVARCHAR(5000) | Displays the issuer of the X.509 certificate. |
| VALID_FROM | TIMESTAMP | Displays the start time of certificate's validity. |
| VALID_UNTIL | TIMESTAMP | Displays the end time of certificate's validity. |
| CERTIFICATE_USAGE | VARCHAR(5) | Displays the certificate usage: OWN, CHAIN, or TRUST. |

## Related Information

PSES System View [→](PSES-System-View.md) PSE_PURPOSE_OBJECTS System View [→](PSE_PURPOSE_OBJECTS-System-View.md) CREATE PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PSE-Statement-System-Management.md) SET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-PSE-Statement-System-Management.md) UNSET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-PSE-Statement-System-Management.md) ALTER PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-PSE-Statement-System-Management.md) DROP PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-PSE-Statement-System-Management.md)
