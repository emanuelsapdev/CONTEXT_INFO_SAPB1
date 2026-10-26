# 6.1.54 DATA_STATISTICS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1460–1464

Provides an overview of data statistics objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DATA_STATISTICS_OID | BIGINT | Displays the data statistics object ID. |
| DATA_STATISTICS_TYPE | VARCHAR(9) | Displays the data statistics type. |
| DATA_STATISTICS_SCHEMA_NAME | NVARCHAR(256) | Displays the data statistics object schema. |
| DATA_STATISTICS_NAME | NVARCHAR(256) | Displays the data statistics name. |
| DATA_SOURCE_OBJECT_TYPE | VARCHAR(5) | Displays the data source object type, for example, TABLE. |
| DATA_SOURCE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the data source. |
| DATA_SOURCE_OBJECT_NAME | NVARCHAR(256) | Displays the object name of the data source. |
| DATA_SOURCE_COLUMN_NAMES | NVARCHAR(5000) | Displays the column names of the data source. |
| DATA_SOURCE_STORAGE_TYPE | VARCHAR(8) | Displays the storage type of the data source: DEFAULT/EXTENDED. |
| DATA_SOURCE_PART_ID | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_TIME | TIMESTAMP | Displays the time when the data statistics object was created. |
| CONSTRAINT | VARCHAR(20) | Displays the constraint for the build algorithm for the data statistics object. |
| IS_PERSISTENT | VARCHAR(5) | Displays whether the content of the data statistics object is persistent or not: TRUE/FALSE. |
| REFRESH_TYPE | VARCHAR(7) | Displays the refresh type for the data statistics object. |
| IS_ENABLED | VARCHAR(5) | Displays whether the data statistics object is enabled: TRUE/FALSE. |
| LAST_REFRESH_TIME | TIMESTAMP | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| LAST_REFRESH_REASON | VARCHAR(19) | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| MINVALUE_NUMERIC | DOUBLE | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| MINVALUE_STRING | NVARCHAR(256) | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| MAXVALUE_NUMERIC | DOUBLE | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| MAXVALUE_STRING | NVARCHAR(256) | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| COUNT | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| DISTINCT_COUNT | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| NULL_COUNT | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_MEMORY | BIGINT | Displays the memory size that the data statistics object uses in bytes. This value is set in the CREATE STATISTICS statement. |
| LAST_REFRESH_MEMORY | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_MEMORY_PERCENT | REAL | Displays the memory size, as a percent age of the data source size, to be used by the data statistics object specified in the CREATE STATISTICS statement |
| LAST_REFRESH_MEMORY_PERCENT | REAL | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_BUCKETS | BIGINT | Displays the number of buckets speci fied in the CREATE STATISTICS statement |
| LAST_REFRESH_BUCKETS | BIGINT | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_QERROR | REAL | Displays the parameter qerror for the data statistics object of type HISTO GRAM as specified in the CREATE STA TISTICS statement |
| LAST_REFRESH_QERROR | REAL | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_QTHETA | INTEGER | Displays the parameter qtheta for the data statistics object of type HISTO GRAM as specified at the CREATE STA TISTICS statement |
| LAST_REFRESH_QTHETA | INTEGER | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_ACCURACY | REAL | Displays the parameter accuracy for the data statistics object of type SKETCH as specified in the CREATE STATISTICS statement |
| LAST_REFRESH_ACCURACY | REAL | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_PREFIX_BITS | INTEGER | Displays the parameter prefix bits for the data statistics object of type SKETCH as specified at the CREATE STATISTICS statement. |
| LAST_REFRESH_PREFIX_BITS | INTEGER | Deprecated. See the M_DATA_STATISTICS view for more information about this column. |
| CREATE_SAMPLE_SIZE | BIGINT | Displays the sample size, in bytes, to be used by the data statistics object of type SAMPLE specified in the CREATE STATISTICS statement. |
| CREATE_SAMPLE_SIZE_PERCENT | REAL | Displays the sample size, as a percent age of the data source size, to be used by the data statistics object of type SAMPLE specified in the CREATE STA TISTICS statement. |
| VALID_FOR | VARCHAR(32) | Displays how the data statistics object may be used: ESTIMATION/DATA DE PENDENCY. |
| INVALIDATION_REASON | VARCHAR(32) | Displays the reason for invalidating a data statistics object:<br>**NULL**<br>The object is valid. **USER ACTION**<br>The data statistics object is invalid because a user has disabled it. **ALTER TABLE MOVE**<br>The data statistics object is disabled because a user relocated the table to a different storage space. **ALTER COLUMN DATA TYPE**<br>The data statistics object is disabled because the data type of the underlying column(s) no longer supports the statistics type. |

## Related Information

CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md) M_DATA_STATISTICS System View [→](../6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md)

[M_SYSTEM_DATA_STATISTICS System View](../6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md)
