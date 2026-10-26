# 6.1.129 REMOTE_SUBSCRIPTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1548–1549

Lists all the remote subscriptions created for a remote source.

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| SUBSCRIPTION_OID | BIGINT | Displays the remote subscription OID. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the remote subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the remote subscription name. |
| OWNER_NAME | NVARCHAR(256) | Displays the owner's name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| IS_VALID | VARCHAR(5) | Displays whether the remote subscription is valid or not: TRUE/FALSE. This value is FALSE when its source or target objects are changed or dropped. |
| SUBSCRIPTION_TYPE | VARCHAR(13) | Displays the remote subscription type. |
| VIRTUAL_TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the virtual table schema name. |
| VIRTUAL_TABLE_NAME | NVARCHAR(256) | Displays the virtual table name. |
| SUBSCRIPTION_QUERY_STRING | NCLOB | Displays the SELECT statement specified in the subscription when subscription type is SQL. |
| TARGET_OBJECT_TYPE | VARCHAR(9) | Displays the remote subscription target object type: TABLE, PROCEDURE, or TASK. |
| TARGET_OBJECT_SCHEMA_NAME | NVARCHAR(256) | Displays the target object schema name. |
| TARGET_OBJECT_NAME | NVARCHAR(256) | Displays the target object name. |
| TARGET_OTHER_PARAM_STRING | NVARCHAR(4000) | Displays the constant parameter string to pass during execution when the target object type is PROCEDURE or TASK. |
| CHANGE_MODE | VARCHAR(6) | Displays the remote subscription change mode: NULL, NORMAL, UPSERT, or INSERT. |
| CHANGE_TYPE_COLUMN_NAME | NVARCHAR(256) | Displays the remote subscription change type column name in the target table: I (INSERT), D (DELETE), and so on. |
| CHANGE_TIME_COLUMN_NAME | NVARCHAR(256) | Displays the remote subscription change time column name in the target table. Supported data types are TIMESTAMP, CHAR, and VARCHAR with a minimum length of 27. |
| CHANGE_SEQUENCE_COLUMN_NAME | NVARCHAR(256) | Displays the remote subscription change sequence column name in the target table. |
| SCHEMA_CHANGES | VARCHAR(5) | Displays whether or not the remote subscription propagates schema changes: TRUE/FALSE. |
| TASK_PROCEDURE_PARAMETERS | NVARCHAR(5000) | Displays the comma-separated list of task parameters. |

## Related Information

REMOTE_SUBSCRIPTION_DATA_CONTAINERS System View [→](REMOTE_SUBSCRIPTION_DATA_CONTAINERS-System-View.md) REMOTE_SUBSCRIPTION_EXCEPTIONS System View [→](REMOTE_SUBSCRIPTION_EXCEPTIONS-System-View.md) REMOTE_USERS System View [→](REMOTE_USERS-System-View.md) REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) CREATE REMOTE SUBSCRIPTION Statement [Smart Data Integration] ALTER REMOTE SUBSCRIPTION Statement [Smart Data Integration] DROP REMOTE SUBSCRIPTION Statement [Smart Data Integration]
