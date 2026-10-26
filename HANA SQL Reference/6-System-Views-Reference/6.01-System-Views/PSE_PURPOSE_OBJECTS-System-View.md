# 6.1.120 PSE_PURPOSE_OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1538–1540

Provides information about all PSEs and their assigned providers or hosts, referred to as purpose objects.

## Structure

| **Column Name** | **Purpose** | **Purpose Object** |
| --- | --- | --- |
| PSE_NAME | NVARCHAR(256) | Displays the name of the PSE store. |
| PURPOSE | NVARCHAR(24) | Displays the purpose of the PSE store. |
| PURPOSE_OBJECT | NVARCHAR(256) | For JWT or SAML purposes, displays the name of the assigned provider. For the SSL purpose, this is the assigned host name. |

## Additional Information

One PSE may have multiple lines, one line per assigned provider or host. All PSEs are shown, including those with and without a purpose and those with and without a purpose object assigned.

## Permissions

No additional privilege is required to see those entries for which you have the REFERENCES or ALTER privilege on the PSE object. To see all entries in the PSE_PURPOSE_OBJECTS system view, you must have the TRUST ADMIN system privilege.

## Related Information

PSES System View [→](PSES-System-View.md) PSE_CERTIFICATES System View [→](PSE_CERTIFICATES-System-View.md) CREATE PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PSE-Statement-System-Management.md) SET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-PSE-Statement-System-Management.md) UNSET PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNSET-PSE-Statement-System-Management.md) ALTER PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-PSE-Statement-System-Management.md) DROP PSE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-PSE-Statement-System-Management.md)
