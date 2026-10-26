# 6.2.88 M_DSO_OPERATIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1761–1763

Provides information about data store object (DSO) operations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| OPERATION | VARCHAR(32) | Displays the operation: ACTIVATION or ROLLBACK. |
| USAGE_MODE | VARCHAR(32) | Displays the usage mode. This clarifies which variant of DSO is used:<br>• ADSO for advanced DSOs<br>• ODSO for classic DSOs with persistent change log tables<br>• CDSO for CDS-based native DSOs<br>• IMO for older in-memory optimized DSOs (not recommended) |
| ACTIVATION_IDS | NVARCHAR(1024) | Displays the activation IDs. |
| TARGET_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the target table. |
| TARGET_TABLE_NAME | NVARCHAR(256) | Displays the name of the target table. |
| START_TIME | TIMESTAMP | Displays the start time of the operation. |
| END_TIME | TIMESTAMP | Displays the end time of the operation. |
| ERROR_CODE | INTEGER | Displays the last error code in the case of a failure. Otherwise this value is 0. |
| ERROR_MESSAGE | NVARCHAR(2000) | Displays the last error message in the case of a failure. Otherwise this value displays "no error". |
| SOURCE_RECORD_COUNT | BIGINT | Displays the number of source table rows activated. |
| INSERT_RECORD_COUNT | BIGINT | Displays the number of rows inserted into the target table. |
| DELETE_RECORD_COUNT | BIGINT | Displays the number of rows deleted from the target table. |
| UPDATE_RECORD_COUNT | BIGINT | Displays the number of target table rows that were updated. |
| CHANGE_LOG_RECORD_COUNT | BIGINT | Displays the number of rows inserted into the change log. |
| PACKAGE_PROCESSING_TIME | BIGINT | Displays the sum of the processing times for all packages in microseconds. |
| PACKAGE_INBOUND_QUEUE_READ_TIME | BIGINT | Displays the sum of the inbound queue read times in all packages in microseconds. |
| PACKAGE_ACTIVE_DATA_READ_TIME | BIGINT | Displays the sum of the active data read times in all packages in microseconds. |
| ACTIVE_DATA_READ_RECORD_COUNT | BIGINT | Displays the total number of active rows read. |
| PACKAGE_CALCULATION_TIME | BIGINT | Displays the sum of the calculation times for the change log and the new active data in microseconds. |
| AVG_CALCULATION_JOB_COUNT | DOUBLE | Displays the active number of jobs per package used for the calculation of the change log and the new active data. |
| CHANGE_LOG_INSERT_TIME | BIGINT | Displays the sum of the time spent inserting the change log records in microseconds. |
| ACTIVE_DATA_INSERT_TIME | BIGINT | Displays the sum of the time spent inserting new active data records in microseconds. |
| ACTIVE_DATA_UPDATE_TIME | BIGINT | Displays the sum of the time spent updating active data records in microseconds. |
| ACTIVE_DATA_DELETE_TIME | BIGINT | Displays the time spent deleting active data records in microseconds. |
| PACKAGE_COUNT | BIGINT | Displays the total number of packages. |
| PARAMETERS | NCLOB(2147483647) | Displays the call parameters. |
| CONFIGURATION | NCLOB(2147483647) | Displays the non-default, DSOspecific `ini` file settings used by the operation. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name. |

## Related Information

M_JOB_PROGRESS System View [→](M_JOB_PROGRESS-System-View.md) M_EXTRACTORS System View [→](M_EXTRACTORS-System-View.md)
