# 6.2.243 M_RS_TABLE_VERSION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1972–1974

Provides information on row table versions: detailed version counts and used sizes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema to which the container belongs. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the container. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| CONTAINER_ID | INTEGER | Indicates that some tables may have several containers to store its data. The container ID is a unique identifier for each container. |
| IS_SYSTEM_TABLE | VARCHAR(5) | Indicates whether or not the table is a system table: TRUE/FALSE. |
| VERSION_COUNT | BIGINT | Displays the number of all versions in the container. This includes all versions regardless of their version type and status. |
| INSERT_VERSION_COUNT | BIGINT | Displays the number of insert-versions in the container. |
| UPDATE_VERSION_COUNT | BIGINT | Displays the number of update-versions in the container. |
| DELETE_VERSION_COUNT | BIGINT | Displays the number of delete-versions in the container. |
| COMMITTED_VERSION_COUNT | BIGINT | Displays the number of all committed versions in the container (includes all types). |
| COMMITTED_INSERT_VERSION_COUNT | BIGINT | Displays the number of committed insert-versions in the container. |
| COMMITTED_UPDATE_VERSION_COUNT | BIGINT | Displays the number of committed up date-versions in the container. |
| COMMITTED_DELETE_VERSION_COUNT | BIGINT | Displays the number of committed delete-versions in the container. |
| UNCOMMITTED_VERSION_COUNT | BIGINT | Displays the number of all uncommitted versions in the container (includes all types). |
| UNCOMMITTED_INSERT_VERSION_COUNT | BIGINT | Displays the number of uncommitted insert-versions in the container. |
| UNCOMMITTED_UPDATE_VERSION_COUNT | BIGINT | Displays the number of uncommitted update-versions in the container. |
| UNCOMMITTED_DELETE_VERSION_COUNT | BIGINT | Displays the number of uncommitted delete-versions in the container. |
| VERSION_SIZE | BIGINT | Displays the used size of the versions in the container in bytes. This includes all versions regardless of their version type and status. |
| INSERT_VERSION_SIZE | BIGINT | Displays the used size of the insert-versions in the container in bytes. |
| UPDATE_VERSION_SIZE | BIGINT | Displays the used size of update-versions in the container in bytes. |
| DELETE_VERSION_SIZE | BIGINT | Displays the used size of delete-versions in the container in bytes. |
| COMMITTED_VERSION_SIZE | BIGINT | Displays the used size of all of the committed versions in the container (includes all types) in bytes. |
| COMMITTED_INSERT_VERSION_SIZE | BIGINT | Displays the used size of committed insert-versions in the container in bytes. |
| COMMITTED_UPDATE_VERSION_SIZE | BIGINT | Displays the used size of committed up date-versions in the container in bytes. |
| COMMITTED_DELETE_VERSION_SIZE | BIGINT | Displays the used size of committed delete-versions in the container in bytes. |
| UNCOMMITTED_VERSION_SIZE | BIGINT | Displays the used size of all uncommitted versions in the container (includes all types) in bytes. |
| UNCOMMITTED_INSERT_VERSION_SIZE | BIGINT | Displays the used size of uncommitted insert-versions in the container in bytes. |
| UNCOMMITTED_UPDATE_VERSION_SIZE | BIGINT | Displays the used size of uncommitted update-versions in the container in bytes. |
| UNCOMMITTED_DELETE_VERSION_SIZE | BIGINT | Displays the used size of uncommitted delete-versions in the container in bytes. |
| MIN_COMMIT_ID | BIGINT | Indicates that each committed version has its commit ID. MIN_COMMIT_ID refers to the minimum value of commit ID among all committed versions. |
