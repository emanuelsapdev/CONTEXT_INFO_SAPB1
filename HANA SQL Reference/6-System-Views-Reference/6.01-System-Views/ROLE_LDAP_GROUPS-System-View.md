# 6.1.142 ROLE_LDAP_GROUPS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1562

Shows the mapping between SAP HANA roles and LDAP groups.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the role. |
| ROLE_NAME | NVARCHAR(256) | Displays the name of the role. |
| LDAP_GROUP_NAME | NVARCHAR(1024) | Displays the name of the LDAP group. |

## Related Information

CREATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-LDAP-PROVIDER-Statement-Access-Control.md) ALTER LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-LDAP-PROVIDER-Statement-Access-Control.md) VALIDATE LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/VALIDATE-LDAP-PROVIDER-Statement-Access-Control.md) DROP LDAP PROVIDER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-LDAP-PROVIDER-Statement-Access-Control.md) LDAP_USERS System View [→](LDAP_USERS-System-View.md) LDAP_PROVIDERS System View [→](LDAP_PROVIDERS-System-View.md) CREATE ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-ROLE-Statement-Access-Control.md) ALTER ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-ROLE-Statement-Access-Control.md) DROP ROLE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-ROLE-Statement-Access-Control.md)
