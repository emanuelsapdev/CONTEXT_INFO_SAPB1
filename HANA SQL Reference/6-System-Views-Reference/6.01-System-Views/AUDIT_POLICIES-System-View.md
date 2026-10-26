# 6.1.24 AUDIT_POLICIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1426–1428

Provides information about audit policies.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| AUDIT_POLICY_NAME | NVARCHAR(256) | Displays the audit policy name. |
| AUDIT_POLICY_OID | BIGINT | Displays the object ID of the audit policy. |
| EVENT_STATUS | VARCHAR(32) | Displays the status of events to be audited: SUCCESSFUL EVENTS, UNSUC CESSFUL EVENTS, ALL EVENTS. |
| EVENT_LEVEL | VARCHAR(16) | Displays the level of events to be audited: EMERGENCY, CRITICAL, ALERT, WARNING, INFO. |
| IS_AUDIT_POLICY_ACTIVE | VARCHAR(5) | Displays whether the audit policy is active: TRUE/ FALSE. |
| IS_VALID | VARCHAR(32) | Displays whether an audit policy is valid. An audit policy can be invalid if the referenced user or object does not exist or an invalid combination of action and object is specified (for example, EXECUTE on a table). Possible values are TRUE/ FALSE. |
| IS_DATABASE_LOCAL | VARCHAR(5) | Displays whether the policy was created locally on the current database and can be changed from within this database:TRUE/FALSE. |
| EVENT_ACTION | VARCHAR(32) | Displays the action to be audited, such as SELECT or GRANT PRIVILEGE. |
| USER_NAME | NVARCHAR(256) | Displays the user whose actions are to be audited. |
| EXCEPT_USER_NAME | NVARCHAR(256) | Displays the user whose actions are not to be audited. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of object to be audited, or INVALID if the object type was changed after the audit policy was created. |
| OBJECT_SCHEMA | NVARCHAR(256) | Displays the schema of object to be audited. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of object to be audited. |
| TRAIL_TYPE | VARCHAR(6) | Displays the name of the audit trail where the audit entry is written. |
| RETENTION_PERIOD | INTEGER | Displays the number of days the corresponding audit entries are retained. |

## Additional Information

Database users with the CATALOG READ, DATA ADMIN, or AUDIT ADMIN system privilege can view information in this system view. For all other database users, this view is empty.

## Related Information

ALL_AUDIT_LOG System View [→](ALL_AUDIT_LOG-System-View.md) AUDIT_LOG System View [→](AUDIT_LOG-System-View.md) CREATE AUDIT POLICY Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-AUDIT-POLICY-Statement-Access-Control.md) ALTER AUDIT POLICY Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-AUDIT-POLICY-Statement-Access-Control.md) DROP AUDIT POLICY Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-AUDIT-POLICY-Statement-Access-Control.md)
