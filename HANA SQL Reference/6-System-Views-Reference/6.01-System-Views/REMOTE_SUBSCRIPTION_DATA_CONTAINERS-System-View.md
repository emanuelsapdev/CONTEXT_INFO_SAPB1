# 6.1.130 REMOTE_SUBSCRIPTION_DATA_CONTAINERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1549–1551

Provides information regarding remote subscription data.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_NAME | NVARCHAR (256) | Displays the remote source name. |
| CONTENT_TYPE | VARCHAR(40) | Displays the category of data containers:<br>• COMMIT SEQUENCE GROUP<br>• COMMIT SEQUENCES (displays the order that transactions get committed and a sequence number for each commit row)<br>• TRANSACTION (each container contains only one transaction)<br>• LOBS<br>• ROLLBACK SAVEPOINTS<br>• DISTRIBUTOR QUEUE DATA (displays the data currently being queued by the distributor)<br>• DISTRIBUTOR QUEUE DATA REF ERENCES (displays the list of transactions currently being referenced by the distributor) |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the remote subscription. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the name of the remote subscription. |
| TRANSACTION_ID | VARCHAR(512) | Displays the ID of the transaction being replicated. |
| CONTAINER_ID | BIGINT | Displays the ID of the data container. Depending on the content type, a container can be searched by REMOTE_SOURCE_ID and CONTENT_TYPE or with additional information such as SUBSCRIPTION_OID or TRANSACTION_ID. |

## Related Information

REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTION_EXCEPTIONS System View [→](REMOTE_SUBSCRIPTION_EXCEPTIONS-System-View.md) CREATE REMOTE SUBSCRIPTION Statement [Smart Data Integration] ALTER REMOTE SUBSCRIPTION Statement [Smart Data Integration] DROP REMOTE SUBSCRIPTION Statement [Smart Data Integration]
