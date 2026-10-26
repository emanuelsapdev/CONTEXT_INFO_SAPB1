# 6.2.155 M_LIVECACHE_OMS_VERSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1858–1859

Detailed information on the OMS versions that currently exists.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VERSION_ID | VARCHAR(22) | Displays the ID of the OMS version. |
| CREATE_DATE | TIMESTAMP | Displays the timestamp of the creation of the OMS version. |
| LAST_OPEN_DATE | TIMESTAMP | Displays the timestamp when the OMS version was opened last. |
| IS_OPEN | VARCHAR(5) | Displays the flag indicating whether the version is currently open: TRUE/FALSE. |
| CONNECTION_ID | INTEGER | Displays the ID of the connection/ session that the version is bound to. |
| LIVECACHE_MVCC_SNAPSHOT_TIMESTAMP | BIGINT | Displays the consistent view MVCC snapshot timestamp. |
| HEAP_USAGE | BIGINT | Displays the memory that is currently used by the version in bytes. |
| VERSION_DESCRIPTION | NVARCHAR(512) | Displays the description. |

## Additional Information

Status information is shown for each OMS version that currently exists.

This view can only be used if liveCache is enabled.

## Related Information

[M_LIVECACHE_PROCEDURE_STATISTICS System View](M_LIVECACHE_PROCEDURE_STATISTICS-System-View.md)
