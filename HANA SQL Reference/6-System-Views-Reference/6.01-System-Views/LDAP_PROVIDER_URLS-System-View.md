# 6.1.100 LDAP_PROVIDER_URLS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1518–1519

Lists all LDAP provider URLs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| LDAP_PROVIDER_NAME | NVARCHAR(256) | Displays the name of the LDAP provider. |
| URL TYPE | VARCHAR(32) | Displays the LDAP provider URL type. |
| URL | NVARCHAR(4096) | Displays the URL for the LDAP provider. |

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LDAP-PROVIDER-Statement-Access-Control.md) ALTER LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md) DROP LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_PROVIDERS System View [→](LDAP_PROVIDERS-System-View.md) LDAP_USERS System View [→](LDAP_USERS-System-View.md)
