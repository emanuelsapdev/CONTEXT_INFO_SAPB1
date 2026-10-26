# 6.1.177 USERGROUP_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1607–1608

Provides the list of parameter sets defined for usergroups.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USERGROUP_NAME | NVARCHAR(256) | Displays the name of the usergroup. |
| PARAMETER_SET_NAME | VARCHAR(64) | Displays the name of the parameter set the parameter belongs to. |
| IS_PARAMETER_SET_ENABLED | VARCHAR(5) | Displays if the parameter set is enabled for the usergroup: TRUE/FALSE. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the name of the parameter. |
| PARAMETER_VALUE | NVARCHAR(5000) | Displays the value of the parameter. |

## Additional Information

Users see different values in this view depending on their privileges, as follows:

- Users with one of the following privileges can see everything for all usergroups: USER ADMIN, CATALOG READ, DATA ADMIN, or USERGROUP OPERATOR
- All other users see only information specific to the usergroup they are in.

## Related Information

USERGROUPS System View [→](USERGROUPS-System-View.md) USERS System View [→](USERS-System-View.md) CREATE USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USERGROUP-Statement-Access-Control.md) CREATE USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USERGROUP-Statement-Access-Control.md) ALTER USERGROUP Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USERGROUP-Statement-Access-Control.md)

[DROP USERGROUP Statement (Access Control)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-USERGROUP-Statement-Access-Control.md)
