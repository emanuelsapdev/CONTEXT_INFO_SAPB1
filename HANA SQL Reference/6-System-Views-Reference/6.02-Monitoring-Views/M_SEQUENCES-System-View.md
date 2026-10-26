# 6.2.250 M_SEQUENCES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1985–1986

Provides statistics for sequence caches.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host where the sequence cache exists. This is only displayed when the cache is greater than 1 and the value has been cached. |
| PORT | INTEGER | Displays the port where the sequence cache exists. This is only displayed when the cache is greater than 1 and the value has been cached. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the sequence. |
| SEQUENCE_NAME | NVARCHAR(256) | Displays the sequence name. |
| CACHE_SIZE | INTEGER | Displays the cache size of the sequence cache in bytes. |
| START_VALUE | DECIMAL | Displays the start value of the sequence cache. This is only displayed when the cache is greater than 1 and the value has been cached. |
| END_VALUE | DECIMAL | Displays the end value of the sequence cache. This is only displayed when the cache is greater than 1 and the value has been cached. |
| CURRENT_VALUE | DECIMAL | Displays the current value of the sequence cache in bytes. |

## Related Information

SEQUENCES System View [→](../6.01-System-Views/SEQUENCES-System-View.md) CREATE SEQUENCE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SEQUENCE-Statement-Data-Definition.md) ALTER SEQUENCE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-SEQUENCE-Statement-Data-Definition.md)
