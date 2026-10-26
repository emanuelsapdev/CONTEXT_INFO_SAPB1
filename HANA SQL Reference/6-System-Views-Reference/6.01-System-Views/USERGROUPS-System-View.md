# 6.1.176 USERGROUPS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1606–1607

Provides details on all user groups.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USERGROUP_NAME | NVARCHAR(256) | Displays the name of the user group. |
| USERGROUP_ID | BIGINT | Displays the user group ID. |
| CREATOR | NVARCHAR(256) | Displays the creator of the user group. |
| IS_USER_ADMIN_ENABLED | VARCHAR(5) | Displays whether a user with the USER ADMIN system privilege can manage the specified user group: TRUE/FALSE. |
| COMMENTS | NVARCHAR(5000) | Displays the description for the speci fied user group. |

## Additional Information

Users see different values in this view depending on their privileges, as follows:

- Users with one of the following privileges can see everything for all users: USER ADMIN, CATALOG READ, DATA ADMIN
- All other users see only information specific to themselves.

## Related Information

USERS System View [→](USERS-System-View.md) USERGROUP_PARAMETERS System View [→](USERGROUP_PARAMETERS-System-View.md)

USER_PARAMETERS System View [→](USER_PARAMETERS-System-View.md) CREATE USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USERGROUP-Statement-Access-Control.md) ALTER USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USERGROUP-Statement-Access-Control.md) DROP USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-USERGROUP-Statement-Access-Control.md)
