# 6.1.131 REMOTE_SUBSCRIPTION_EXCEPTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1551–1552

Provides remote subscription exception information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| EXCEPTION_OID | BIGINT | Displays the exception ID. |
| OBJECT_TYPE | VARCHAR(19) | Displays the object type: REMOTE_SOURCE/REMOTE_SUBSCRIPTION. |
| OBJECT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the remote source or the remote subscription, based on the OBJECT_TYPE. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name of the remote source or remote subscription, based on the OBJECT_TYPE. |
| EXCEPTION_TIME | TIMESTAMP | Displays the time at whoch the exception was raised. |
| ERROR_NUMBER | INTEGER | Displays the error number. |
| ERROR_MESSAGE | NVARCHAR(2000) | Displays the error message. |
| COMPONENT | VARCHAR(11) | Displays the component that raised the exception. |

## Related Information

REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTION_DATA_CONTAINERS System View [→](REMOTE_SUBSCRIPTION_DATA_CONTAINERS-System-View.md) REMOTE_USERS System View [→](REMOTE_USERS-System-View.md) CREATE REMOTE SUBSCRIPTION Statement [Smart Data Integration] ALTER REMOTE SUBSCRIPTION Statement [Smart Data Integration] DROP REMOTE SUBSCRIPTION Statement [Smart Data Integration]
