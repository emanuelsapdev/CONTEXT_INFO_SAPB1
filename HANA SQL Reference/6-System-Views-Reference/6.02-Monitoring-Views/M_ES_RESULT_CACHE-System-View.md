# 6.2.104 M_ES_RESULT_CACHE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1781–1782

Provides details about each result that has been cached. You must have the EXTENDED STORAGE ADMIN privilege to access this view.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table. |
| COLUMNS | NLCOB | Displays the columns included in the result as a comma-separated list. |
| PREDICATES | NCLOB | Displays the predicates used to generate the result as a comma-separated list. |
| COMMIT_ID | BIGINT | Displays the version number of the table. |
| STATEMENT_STRING | NCLOB | Displays the query that generated the result. |
| CREATE_TIME | TIMESTAMP | Displays the time that the result cache entry was generated and stored. |
| CREATE_DURATION | BIGINT | Displays the number of milliseconds it took to generate the original result. |
| CREATE_CONNECTION_ID | BIGINT | Displays the connection ID that generated the result. |
| LAST_ACCESS_TIME | TIMESTAMP | Displays the last time that the result cache entry was accessed by a user. |
| LAST_CONNECTION_ID | BIGINT | Displays the last connection ID that accessed the result. |
| HIT_COUNT | BIGINT | Displays the number of accesses on the cache entry. |
| SUBSET_HIT_COUNT | BIGINT | Displays the number of cache entry accesses that only used a subset of the result. |
| EXACT_MATCH_HIT_COUNT | BIGINT | Displays the number of cache entry accesses that used the whole result. |
| RESULT_SIZE | BIGINT | Displays the size of the memory occupied by the result cache entry in bytes. |

## Related Information

ALTER SYSTEM REFRESH RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM REFRESH RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REFRESH-RESULT-CACHE-Statement-System.md) ALTER SYSTEM REMOVE RESULT CACHE ENTRY Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-RESULT-CACHE-ENTRY-Statement-System.md) ALTER SYSTEM CLEAR RESULT CACHE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-RESULT-CACHE-Statement-System-Management.md)
