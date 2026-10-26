# 6.2.76 M_DATA_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1742–1746

Lists data statistics generated when you query column and row store object.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DATA_STATISTICS_OID | BIGINT | Displays the data statistics object ID. |
| DATA_STATISTICS_TYPE | VARCHAR(12) | Displays the data statistics object type. |
| DATA_STATISTICS_SCHEMA_NAME | NVARCHAR(256) | Displays the data statistics object schema. |
| DATA_STATISTICS_NAME | NVARCHAR(256) | Displays the data statistics object name. |
| DATA_SOURCE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the data source object. |
| DATA_SOURCE_OBJECT_NAME | NVARCHAR(256) | Displays the name of the data source object. |
| DATA_SOURCE_COLUMN_NAMES | NVARCHAR(5000) | Lists the column names of the data source. |
| DATA_SOURCE_STORAGE_TYPE | VARCHAR(8) | Displays the source storage type of the data source. |
| DATA_SOURCE_PART_ID | INTEGER | Displays the partition ID of the data source. |
| LAST_REFRESH_TIME | TIMESTAMP | Displays the time the data statistics on the object were last generated. |
| LAST_REFRESH_REASON | VARCHAR(19) | Displays the time the data statistics object was generated. |

DATA_STATISTICS_CONTENT NCLOB (max size 2Gb) Lists the content and properties of the

data statistics object as of the last re fresh (JSON format). The content sec tion is empty for SIMPLE, SKETCH, and RECORD COUNT; it contains bucket boundaries and counts for HISTOGRAM and a values and frequencies list for TOPK. For SAMPLE, it contains a list of sample output. The content is similar to exported data for data statistics ob jects.

The properties section contains proper ties relevant to the data statistics of the specified type. The properties section, when present, may include some of the following properties:

###### MEMORY

Displays the memory size used by the data statistics object in bytes

###### MEMORY PERCENT

Displays the memory size used by the data statistics object, as a per centage of the data source size

###### COUNT

Displays the number of rows in the data source

###### DISTINCT COUNT

Displays the number of unique val ues in the data source

###### NULL COUNT

Displays the number of NULL val ues in the data source

###### BUCKETS

Displays the number of buckets in the data statistics object

###### QERROR

Displays the value of the qerror pa rameter used for building the data statistics object

###### QTHETA

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
|   |   | Displays the value of the qtheta parameter used for building the data statistics object **ACCURACY**<br>Displays the accuracy parameter used for building the data statistics object **PREFIX BITS**<br>Displays the prefix bits parameter used for building the data statistics object **MIN VALUE**<br>Displays the minimum value in the data source in bytes **MAX VALUE**<br>Displays the maximum value in the data source in bytes **MAX_ROWID**<br>Displays the maximum rowID for the data statistics object **MIN MAX IS VALID** Displays whether MIN/MAX values are valid **SAMPLE SIZE** Displays the sample size at build time, expressed in bytes **SAMPLE SIZE PERCENT** Displays the sample size at build time, expressed as a percent of the data volume |

## Related Information

CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md) M_SYSTEM_DATA_STATISTICS System View [→](M_SYSTEM_DATA_STATISTICS-System-View.md) DATA_STATISTICS System View [→](../6.01-System-Views/DATA_STATISTICS-System-View.md)
