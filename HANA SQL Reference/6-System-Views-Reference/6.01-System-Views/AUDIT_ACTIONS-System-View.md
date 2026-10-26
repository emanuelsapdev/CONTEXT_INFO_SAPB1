# 6.1.22 AUDIT_ACTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1423–1424

Provides information about all available audit actions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ACTION_GROUP | SMALLINT | Displays the ID of the group of audit actions. |
| ACTION_GROUP_DESCRIPTION | VARCHAR(64) | Displays the description for the group of audit actions. |
| ACTION_NAME | VARCHAR(64) | Displays the audit action. |
| IS_USER_MANDATORY | VARCHAR(5) | Displays if the audit action needs a user specification: TRUE/FALSE |
| IS_OBJECT_MANDATORY | VARCHAR(5) | Displays if the audit action needs an object specification: TRUE/FALSE |
| IS_DATABASE_SUPPORTED | VARCHAR(5) | Displays whether the audit action is allowed in an audit policy created by an authorized user remotely on SYS TEMDB: TRUE/FALSE. |

## Additional Information

If viewed on a tenant, database users with the CATALOG READ, DATA ADMIN, or AUDIT ADMIN system privilege can view information in this system view. If viewed on SYSTEMDB, users also need the DATABASE AUDIT ADMIN or DATABASE ADMIN system privilege. For all other database users, this view is empty.

## Related Information

ALL_AUDIT_LOG System View [→](ALL_AUDIT_LOG-System-View.md) AUDIT_LOG System View [→](AUDIT_LOG-System-View.md) AUDIT_POLICIES System View [→](AUDIT_POLICIES-System-View.md)
