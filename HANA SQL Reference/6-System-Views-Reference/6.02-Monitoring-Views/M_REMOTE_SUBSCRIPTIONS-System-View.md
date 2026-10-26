# 6.2.224 M_REMOTE_SUBSCRIPTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1952–1954

Provides the status and run-time information of a remote subscription.

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the remote subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the remote subscription name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| STATE | VARCHAR(256) | Displays the event state:<br>• CREATED<br>• MAT_START_BEG_MARKER - Materialization started. Waiting for BEGIN MARKER<br>• MAT_START_END_MARKER - Materialization started. Waiting for end marker<br>• MAT_COMP_BEG_MARKER - Materialization completed. Waiting for begin marker<br>• MAT_COMP_END_MARKER - Materialization completed. Waiting for end marker<br>• AUTO_CORRECT_CHANGE_DATA<br>• APPLY_CHANGE_DATA |
| OPTIMIZED_QUERY_STRING | NCLOB | Displays the optimized query string. If there are multiple subscriptions interested in the same query result, with the same internal distribution ID, each subscription can use the same result. |
| OPTIMIZED_QUERY_HASH | VARCHAR(128) | Displays the hash of the optimized query string. |
| INTERNAL_DISTRIBUTION_ID | BIGINT | Displays the generated integer that identi fies if multiple target tables are interested in the changes from the same source SQL or virtual table. |
| OPTIMIZED_QUERY_RESULTSET_TYPE | TINYINT | Displays the query result set type:<br>0 - REGULAR<br>1 - CLUSTER<br>2 - POOL |
| REMOTE_SUBSCRIPTION | NVARCHAR(256) | Displays an optional subscription name registered by the adapter in the remote source system. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| BEGIN_MARKER | VARCHAR(64) | Displays the generated begin marker when the QUEUE command is called. The begin marker must use the format: B`<remote_source_oid>`_`<remote_subs` `cription_oid>`_`<YYYYMMDDHH24MMSSFF` `7>`. |
| END_MARKER | VARCHAR(64) | Displays the generated end marker when the DISTRIBUTE command is called. The end marker must use the format: E`<remote_source_oid>`_`<remote_subs` `cription_oid>`_`<YYYYMMDDHH24MMSSFF` `7>`. |
| BEGIN_MARKER_TIME | TIMESTAMP | Displays the timestamp when the QUEUE request is received. |
| END_MARKER_TIME | TIMESTAMP | Displays the timestamp when the DISTRIB UTE command is called. |
| LAST_PROCESSED_TRANSACTION_ID | VARBINARY(128) | Displays the transaction ID of the last processed transaction. |
| LAST_PROCESSED_TRANSACTION_TIME | TIMESTAMP | Displays the time when the last transaction was applied. |
| LAST_PROCESSED_BEGIN_SEQUENCE_ID | VARBINARY(68) | Displays the begin record sequence ID of the last processed transaction. |
| LAST_PROCESSED_COMMIT_SEQUENCE_ID | VARBINARY(68) | Displays the commit record sequence ID of the last processed transaction. |
| LAST_RECEIVED_SEQUENCE_ID | VARBINARY(68) | Displays the last received sequence ID. |
| LAST_RECEIVED_CUSTOM_ID | NVARCHAR(64) | Displays the last received custom ID. Custom IDs may be used by adapters with every changed-data row of a transaction. |
| LAST_PROCESSED_CUSTOM_ID | NVARCHAR(64) | Displays the last processed custom ID. Custom IDs may be used by adapters with every changed-data row of a transaction. |
