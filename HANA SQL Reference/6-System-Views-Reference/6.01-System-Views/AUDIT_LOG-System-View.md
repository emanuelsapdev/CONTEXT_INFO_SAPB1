# 6.1.23 AUDIT_LOG System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1424–1426

Provides information about audit records, with the exception of XSA-auditing. You must have the AUDIT ADMIN, AUDIT OPERATOR, or AUDIT READ system privilege to access this view.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TIMESTAMP | TIMESTAMP | Displays the time that the event occurred. |
| HOST | VARCHAR(64) | Displays the name of the host where the event occurred. |
| PORT | INTEGER | Displays the port number. |
| SERVICE_NAME | VARCHAR(32) | Displays the name of the service. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| CLIENT_HOST | NVARCHAR(256) | Displays the IP of the client host. |
| CLIENT_IP | VARCHAR(45) | Displays the IP of the client application. |
| CLIENT_PID | BIGINT | Displays the PID of the client process. |
| CLIENT_PORT | INTEGER | Displays the port of the client process. |
| USER_NAME | NVARCHAR(256) | Displays the name of the user that is connected to the database. |
| STATEMENT_USER_NAME | NVARCHAR(256) | Displays the name of the user who executed the statement. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the name of the application user. |
| XS_APPLICATION_USER_NAME | NVARCHAR(256) | Displays the name of the XS application user. |
| AUDIT_POLICY_NAME | NVARCHAR(256) | Displays the name of the Audit Policy hit. |
| EVENT_STATUS | VARCHAR(32) | Displays whether the event was successful or not. |
| EVENT_LEVEL | VARCHAR(16) | Displays the severity level of the event. |
| EVENT_ACTION | VARCHAR(64) | Displays the action performed by the audit event. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of schema. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of object. |
| PRIVILEGE_NAME | NVARCHAR(256) | Displays the name of the granted privilege. |
| ROLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the granted role. |
| ROLE_NAME | NVARCHAR(256) | Displays the name of the granted role. |
| GRANTEE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the grantee in GRANT/REVOKE statements. |
| GRANTEE | NVARCHAR(256) | Displays the grantee in GRANT/ REVOKE statements. |
| GRANTABLE | VARCHAR(16) | Displays whether the privilege/role being granted is grantable or not. |
| FILE_NAME | VARCHAR(256) | Displays the configuration file that was changed. |
| SECTION | VARCHAR(128) | Displays the configuration that was changed. |
| KEY | NVARCHAR(2000) | Displays the attribute that was changed. |
| PREV_VALUE | NVARCHAR(5000) | Displays the old value of the attribute. |
| VALUE | NVARCHAR(5000) | Displays the new value of the attribute. |
| STATEMENT_STRING | NCLOB | Displays the SQL statement that caused the event. |
| COMMENT | VARCHAR(5000) | Displays extra information about the event. |
| ORIGIN_DATABASE_NAME | NVARCHAR(256) | Displays the original database name on cross-database queries. |
| ORIGIN_USER_NAME | NVARCHAR(256) | Displays the original user name on cross-database queries. |

## Additional Information

Database users with the AUDIT ADMIN, AUDIT OPERATOR, or AUDIT READ system privilege can view information in this system view. For all other database users, this view is empty.

## Related Information

ALL_AUDIT_LOG System View [→](ALL_AUDIT_LOG-System-View.md) AUDIT_ACTIONS System View [→](AUDIT_ACTIONS-System-View.md) AUDIT_POLICIES System View [→](AUDIT_POLICIES-System-View.md) GRANT Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/GRANT-Statement-Access-Control.md) REVOKE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REVOKE-Statement-Access-Control.md) ALTER SYSTEM CLEAR AUDIT LOG Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-AUDIT-LOG-Statement-System-Management.md)
