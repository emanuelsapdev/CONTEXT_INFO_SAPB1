# 6.1.148 SEQUENCES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1567–1568

Provides information about available sequences.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the sequence. |
| SEQUENCE_NAME | NVARCHAR(256) | Displays the name of the sequence. |
| SEQUENCE_OID | BIGINT | Displays the object ID of the sequence. |
| START_NUMBER | DECIMAL | Displays the start number. |
| MIN_VALUE | DECIMAL | Displays the minimum value of the sequence in bytes. |
| MAX_VALUE | DECIMAL | Displays the maximum value of the sequence in bytes. |
| INCREMENT_BY | DECIMAL | Displays the incremental value. |
| IS_CYCLED | VARCHAR(5) | Displays whether the sequence starts with the MIN_VALUE after having reached the MAX_VALUE in cases where INCREMENT_BY is greater than 0, or if the sequence starts with the MAX_VALUE after having reached the MIN_VALUE in cases where INCREMENT_BY is less than 0: TRUE/FALSE. |
| RESET_BY_QUERY | NCLOB | Displays the reset by query string for the sequence. |
| CACHE_SIZE | INTEGER | Displays the cache size of the sequence in bytes. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the sequence. |

## Related Information

[M_SEQUENCES System View](../6.02-Monitoring-Views/M_SEQUENCES-System-View.md)

CREATE SEQUENCE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-SEQUENCE-Statement-Data-Definition.md) ALTER SEQUENCE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-SEQUENCE-Statement-Data-Definition.md)
