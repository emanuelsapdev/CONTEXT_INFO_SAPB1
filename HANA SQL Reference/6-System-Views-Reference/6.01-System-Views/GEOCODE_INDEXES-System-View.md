# 6.1.79 GEOCODE_INDEXES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1499–1500

Provides information about geocode indexes on tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| INDEX_NAME | NVARCHAR(256) | Displays the index name. |
| INDEX_OID | BIGINT | Displays the object ID of the index. |
| FLUSH_AFTER_ROWS | INTEGER | Used to store change-tracking behavior of the index. |
| FLUSH_EVERY_MINUTES | INTEGER | Used to store change-tracking behavior of the index. |

## Related Information

INDEXES System View [→](INDEXES-System-View.md) M_INDEXING_QUEUES System View [→](../6.02-Monitoring-Views/M_INDEXING_QUEUES-System-View.md) GEOCODE_INFO_CODES System View [Smart Data Quality] GEOCODE_STATISTICS System View [Smart Data Quality]
