# 6.2.226 M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_GROUP_CONTAINERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1955–1956

Lists all CommitSequece virtual files for a remote source, and the number of entries stored in each virtual file.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REMOTE_SOURCE_OID | BIGINT | Displays the remote source OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| SUBSCRIPTION_OID | BIGINT | Displays the subscription OID |
| SUBSCRIPTION_SCHEMA_NAME | NVARCHAR(256) | Displays the subscription schema name. |
| SUBSCRIPTION_NAME | NVARCHAR(256) | Displays the subscription name. |
| CONTAINER_ID | BIGINT | Displays the ID of the container of the virtual file. |
| COMMIT_SEQUENCE_CONTAINER_ID | BIGINT | Displays the container ID of the CommitSequence virtual file. |
| MIN_SEQUENCE_ID | VARCHAR(256) | Displays the minimum sequence ID of the CommitSequence virtual file. |
| MAX_SEQUENCE_ID | VARCHAR(256) | Displays the maximum sequence ID of the CommitSequence virtual file. |
| ENTRY_COUNT | INTEGER | Displays the number of CommitSequence entries in the virtual file. |
| IS_DELETED | VARCHAR(5) | Indicates if the container identified by COMMIT_SEQUENCE_CONTAINER_ID is deleted. Values are TRUE or FALSE. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
