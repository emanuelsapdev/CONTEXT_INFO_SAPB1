# 4.10.1.117 EXPORT Statement (Data Import Export)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 942–950

Exports catalog objects.

## Syntax

```sql
EXPORT <export_object_name_list>
 [ WHERE <condition> | HAVING <condition_list> ]
 [ AS <export_format> ]
 INTO <path> [ <archive_file_name> ]
 [ WITH <export_option_list> ]
 [ <query_export_specification> ]
```

## Syntax Elements

#### export_object_name_list

Specifies a list of objects to export. The ALL and \* options export all objects from a specified schema.

```sql
<export_object_name_list> ::=
 <export_object_name>[, <export_object_name>[,...]]
 | CLIENTSIDE ENCRYPTION COLUMN KEY <encryption_column_key_name>[,
<encryption_column_key_name>[,...]]
 | { ALL | * }
<export_object_name> ::= [<schema_name>.]{<identifier> | "*" }
<encryption_column_key_name> ::= [<schema_name>.]{<identifier> }
<schema_name> ::= <identifier>
```

##### export_object_name

Specifies objects in a schema for export. Specify `<schema_name>`."\*" to select all objects within the specified schema for export. Specify ALL (without `<schema_name>`) to select all objects from all schemas in the system for export. `<schema_name>`,"\*" is not supported with the HAVING clause.

##### encryption_column_key_name

Specifies the name of a column encryption key (CEK).

#### WHERE condition

Exports a subset of table data.

```sql
WHERE <condition> ::=
 <condition> OR <condition>
 | <condition> AND <condition>
 | NOT <condition>
 | ( <condition> )
 | <predicate>
<predicate> ::=
 <comparison_predicate>
 | <range_predicate>
 | <in_predicate>
 | <exist_predicate>
 | <like_predicate>
 | <null_predicate>

<comparison_predicate> ::=
 <expression> { = | != | <> | > | < | >= | <= } [ ANY | SOME | ALL ]
( { <expression_list> | <subquery> } )

<range_predicate> ::=
 <expression> [ NOT ] BETWEEN <expression> AND <expression>

<in_predicate> ::=
 <expression> [ NOT ] IN ( { <expression_list> | <subquery> } )

<exist_predicate> ::=
 [NOT] EXISTS ( <subquery> )

<like_predicate> ::=
 <expression> [ NOT ] LIKE <expression> [ ESCAPE <expression> ]

<null_predicate> ::=
 <expression> IS [ NOT ] NULL
<expression_list> ::= <expression> [, <expression> [,...] ]
```

The WHERE clause follows, and is associated with, a single table in the EXPORT statement. If at least one table has a WHERE clause specified, then the following restrictions are enforced:

- Only the CSV format is supported for export
- The following options are not allowed: CATALOG ONLY, STATISTICS ONLY, and NO DEPENDENCIES

The WHERE clause cannot be used in conjunction with ALL or \*.

#### HAVING

Exports a subset of data from a specified object.

```sql
HAVING <condition_list>
```

The HAVING clause cannot be used in conjunction with `<schema>`.`<identifier>` or `<schema>`."\*".

For the types of conditions you can specify, see `<condition_list>`.

#### condition_list

Specifies the conditions defined for the HAVING and DEPENDENCIES clauses.

```sql
<condition_list> ::=
<condition> OR <condition>
| <condition> AND <condition>
| NOT <condition>
| ( <condition> )
| <predicate>
<predicate> ::=
<comparison_predicate>
| <range_predicate>
| <in_predicate>
| <like_predicate>
| <null_predicate>
<comparison_predicate> ::=
<column_expression> { = | != | <> | > | < | >= | <= } [ ANY | SOME | ALL ]
( { <expression_list>  | <subquery> } )
<range_predicate> ::=
<column_expression> [NOT] BETWEEN <expression> AND <expression>
<in_predicate> ::=
<column_expression> [NOT] IN ( { <expression_list> | <subquery> } )
<like_predicate> ::=
<column_expression> [NOT] LIKE <expression> [ ESCAPE <expression> ]
<null_predicate> ::=
<column_expression> IS [NOT] NULL
<expression_list> ::= <expression>[, <expression>[,...] ]
<column_expression> ::= SCHEMA_NAME | OBJECT_NAME | OBJECT_TYPE
<expression>> ::= <identifier> | <type_name> | <expression>
<type_name> ::= TABLE | VIEW | PROCEDURE | FUNCTION | LIBRARY | SEQUENCE
     | SYNONYM | TASK | GRAPH WORKSPACE | EPMMODEL | EPMQUERYSOURCE | DATA
STATISTICS
     | ANALYTIC_PRIVILEGE | CLIENTSIDE ENCRYPTION COLUMN KEY
```

#### AS export_format

Specifies the format to export the data to. The default value is BINARY.

```sql
<export_format> ::= BINARY | CSV
```

| **Format Type** | **Details** |
| --- | --- |
| BINARY | Table data is exported in an internal binary format. Exporting in this format is orders of magnitude faster than exporting the same table in CSV format. Only column non-temporary tables can be exported in binary format. Row tables are always exported in CSV format regardless of the format specified. |
| CSV | Table data is exported in CSV format. With this export format the exported data can be scrambled. Both column and row tables can be exported in CSV format. |

#### INTO path [ archive_file_name ]

Specifies the location where export files are placed.

```sql
<path> [ <archive_file_name> ] ::= <string_literal>
```

Include the file extension `.tar.gz` or `.tgz` on `<archive_file_name>` to export the data to an archive file. Each file added to the archive file must not exceed 8 GB in size or it will become corrupt. There is no size restriction on the archive file itself. See SAP Note 2907201 - Importing Data From Compressed Format Throws Error: "Archive is incomplete".

For security reasons, the path must not contain symbolic links and must not point inside the database instance folder, except its `backup` and `work` subfolders. Examples of valid values include:

```sql
'/tmp'
 '/usr/sap/HDB/HDB00/backup'
 '/usr/sap/HDB/HDB00/work/myexport.tgz'
```

In distributed systems, `<path>` must be a shared disk; otherwise, the operation may fail or have unexpected results.

#### WITH export_option_list

Specifies a list of export options.

```sql
WITH <export_option_list>
<export_option_list> ::= <export_option>[, <export_option>[,...] ]
<export_option> ::=
 REPLACE
 | CATALOG ONLY
 | NO DEPENDENCIES
 | DEPENDENCIES <condition_list>
 | SCRAMBLE [BY <password>]
 | STRIP
 | THREADS <number_of_threads>
 | [ SYSTEM | ALL ] STATISTICS [ COLUMNS <column_list> ] [ TYPE
<dstat_type> ] [ ONLY ]
 | NO STATISTICS
 | TRACE
 | PERSISTENT MEMORY
 | NO REMOTE DATA
```

##### REPLACE

Defines the behavior if the export data already exists in the specified directory. If REPLACE is not specified, then an error is returned if previously exported data exists in the specified export directory.

##### CATALOG ONLY

Specifies to export only the database catalog.

This option interacts with the STATISTICS ONLY and NO STATISTICS options.

##### NO DEPENDENCIES

Specifies to not export the underlying dependencies of an export object.

##### DEPENDENCIES

Specifies the underlying dependencies of an object to export.

```sql
DEPENDENCIES <condition_list>
```

For the types of conditions you can specify, see `<condition_list>`.

DEPENDENCIES is not supported with the WHERE clause.

##### SCRAMBLE [BY scramble_seed]

Obfuscates CSV format exported data.

```sql
SCRAMBLE [BY <scramble_seed>]
<scramble_seed> ::= <string_literal>
```

Provides an export of the structure of your database with the string data scrambled so that it cannot easily be interpreted. When the optional `<scramble_seed>` is not specified, a default scramble seed is used. Make the `<scramble_seed>` at least 8 to 10 characters long.

Only CSV format character string data is scrambled by this parameter.

##### STRIP

Strips attributes that can be reconstructed at import time from the export data. This option can reduce the size of the export file in some cases.

##### THREADS number_of_threads

Specifies the number of process threads to be used for concurrent export processing.

```sql
THREADS <number_of_threads>
<number_of_threads> ::= <unsigned_integer>
```

The THREADS parameter specifies how many objects are exported in parallel; the default is 1. Increasing the number of threads reduces export time, but can also negatively affect database system performance. Consider the following items when you use this parameter:

- When exporting a single table. THREADS has no effect.
- When exporting a view or procedure, two or more threads should be used, up to the number of dependent objects.
- When exporting a whole schema, consider using more than 10 threads, with a maximum being the number of CPU cores in the system.
- When exporting a whole BW/ERP system database with tens of thousands of tables by using the ALL keyword, a large number of threads can be used (up to 256).

**PERSISTENT MEMORY** Exports the persistent memory data as files for columns that are actively using persistent memory. If this option is specified and persistent memory is not configured for the database, then the EXPORT statement fails.

##### [ SYSTEM | ALL ] STATISTICS [ COLUMNS column_list ] [ TYPE dstat_type ] [ ONLY ]

Userdefined data statistics objects are exported by default, along with the objects they reference in `<export_object_name_list>` (for example, tables).

```sql
[ SYSTEM | ALL ] STATISTICS [ COLUMNS <column_list> ] [ TYPE
<dstat_type> ] [ ONLY ]
<column_list> ::= <col_name1>[, <col_name2>[,...] ]
<col_name> ::= <identifier>
<dstat_type> ::= { SIMPLE | TOPK | HISTOGRAM | SKETCH | SAMPLE | RECORD
COUNT }
```

SYSTEM statistics are only available on column and row tables.

If you specify SYSTEM, then system statistics that were automatically generated for the specified data sources are exported. If no system statistics are available for a data source, then no data statistics objects are exported. If you specify ALL, then both system- and userdefined data statistics are exported, where available. If both system- and userdefined statistics are available on a data source, then only the userdefined statistics are exported. If neither SYSTEM nor ALL is specified, then only userdefined data statistics are exported. This is the default behavior in the absence of the STATISTICS clause.

If `<column_list>` is specified, then any data statistics objects that reference all or some of the specified columns, but none of the other columns are exported. When you export SYSTEM data statistics, `<column_list>` is required when the statistics type SAMPLE is specified. If `<column_list>` is not specified and SYSTEM statistics are requested, then TOPK and SIMPLE data statistics for each column of the specified data object are exported, if available. If `<column_list>` is specified, then only a single data object can be specified. If `<column_list>` is specified and SYSTEM statistics are requested, then data statistics of type SIMPLE, TOPK, and SAMPLE are exported. SIMPLE and TOPK are generated for every eligible column on the list, while a single SAMPLE covering all eligible columns from the specified list is generated.

`<dstat_type>` filters exported data statistics to only the specified type. For SYSTEM data statistics, supported types are SIMPLE, TOPK, and SAMPLE.

If you specify STATISTICS ONLY without CATALOG ONLY, then both the data and metadata for user defined data statistics objects are exported, as well as the metadata for the objects in `<export_object_name_list>`.

If you specify STATISTICS ONLY and CATALOG ONLY, then only the metadata for the data statistics objects and the objects in `<export_object_name_list>` are exported; no data is exported.

##### NO STATISTICS

Excludes both system- and userdefined data statistics objects from the export. Metadata and data for the objects in `<export_object_name_list>` are still exported, and they are impacted as normal by whether CATALOG ONLY is specified.

##### TRACE export_trace_file_name

Writes execution information to the specified trace file when exporting data.

```sql
TRACE <export_trace_file_name>
<export_trace_file_name> ::= <string_literal>
```

The info level trace file contains detailed error descriptions for troubleshooting. The file is saved to the current trace directory.

The contents of the trace file can be found in the M_TRACEFILE_CONTENTS system view. It contains information on:

- The export list
- Dependencies to the export list
- Feasibility checks on the export
- Metadata exported
- The format of the exported data (binary or CSV)
- The single archive for a single archive export
- The results table from the export

To delete the trace file, use the ALTER SYSTEM REMOVE TRACES statement.

##### NO REMOTE DATA

Excludes data in remote records from the export. When the EXPORT statement references virtual tables, remote table data is included in the export if you don't specify CATALOG ONLY. Including remote table records can significantly slow the export process.

#### query_export_specification

Specifies a query to use for the export.

```sql
<query_export_specification> ::=
 [ ON <sqlscript_location_list> ] FOR <dml_statement>
```

For information on query exports, see the SAP HANA SQLScript Reference.

## Permissions

You must have the EXPORT and CREATE TEMPORARY TABLE system privileges. You also need the SELECT privilege on the objects being exported.

To export column encryption keys (CEKs), you must also have the USAGE privilege on the CEK.

## Description

The EXPORT command exports tables, views, column views, synonyms, data statistics objects, sequences, procedures, or column encryption keys in the specified format as BINARY or CSV.

The EXPORT command does not support parameterized views.

System-versioned tables and their associated history table must be exported separately and must be exported by using AS BINARY.

Data stored in "no logging" tables can only be exported in CSV format. For global temporary tables, only the table catalog can be exported. The export of local temporary tables is not supported.

You can only import exported binary files that were generated on an SAP HANA system with the same endianness.

You can cancel an export session by using the ALTER SYSTEM CANCEL WORK IN SESSION statement and specifying the connection ID from the M_EXPORT_BINARY_STATUS view.

Detailed results of the last successful execution of the EXPORT statement are stored in the session-local temporary table `<current_schema>`.#EXPORT_RESULT. If EXPORT has not been executed in the current session, then selecting from `<current_schema>`.#EXPORT_RESULT returns an error. If `<current_schema>` of the session is invalid, then EXPORT throws an exception as it cannot create its result table in `<current_schema>`.

current_schema.#EXPORT_RESULT

| **Column Name** | **Data type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | NVARCHAR(256) | The database of the exported object |
| SCHEMA_NAME | NVARCHAR(256) | The schema of the exported object |
| OBJECT_NAME | NVARCHAR(256) | The name of the exported object |
| OBJECT_TYPE | VARCHAR(32) | The type of the exported object (TA BLE, VIEW, and so on) |
| LOCATION | VARCHAR(75) | The location (`<host>`:`<port>`) where the object was exported |
| STATUS | VARCHAR(16) | The export status (done, skipped, failed) |
| ERROR | VARCHAR(512) | The error text if there is an export failure |

The user exporting tables with encrypted columns must export all relevant column encryption keys (CEKs) used by this table. Exporting a CEK exports all CEK copies of the CEK. The export of a CEK copy also includes the public key of the relevant client key pairs.

> **Note**
>
> When using CSV format to export/import tables that have columns of type GENERATED ALWAYS AS `<expression>`, verify that the imported records match what was exported. If there are anomalies:
>
> - For column tables, switch to exporting/importing as BINARY.
>
> - For row tables, change the table to be a column table and export/import as BINARY.

For more information on security on exported files, refer to the SAP HANA Security Checklists and Recommendations guide.

## Examples

This example exports a client-side encryption key:

```sql
EXPORT CLIENTSIDE ENCRYPTION COLUMN KEY MYSCHEMA.MYCEK1, MYSCHEMA.MYCEK2 AS CSV
INTO '/tmp/';
```

The example exports the information from `MY_SCHEMA TAB1` in CSV format with the REPLACE and SCRAMBLE options enabled.

```sql
EXPORT MY_SCHEMA.TAB1 AS CSV INTO '/tmp' WITH REPLACE SCRAMBLE THREADS 10;
```

This example exports all the database objects in schema A and B, replacing any existing export that may be present in the `tmp` directory.

```sql
EXPORT a."*", b."*" AS CSV INTO '/tmp' WITH REPLACE;
```

The following two examples show how to filter the data exported from tables by using the WHERE clause:

```sql
EXPORT SYSTEM.TBL_A WHERE COL_A > 5 INTO '/tmp/' WITH REPLACE;
EXPORT SYSTEM.TBL_A WHERE COL_B LIKE '%ch%' AND MOD(COL_C, 2) = 0, SYSTEM.TBL_B
INTO ‘/tmp/’ WITH REPLACE;
```

This example exports the schema `my_schema` and creates the trace file `export.trc`.

```sql
EXPORT my_schema."*" INTO '/usr/sap/MS1/HDB01/work' WITH TRACE 'export.trc';
```

In this example, `my_schema` has two tables, `T1` and `T2`, each with column `a`, and two views. V1 selects T1.a from T1 and T2. V2 selects \* from T2. The following syntax exports the object type `VIEW` and all object names not equal to `V2`. It also exports its dependency `T1`.

```sql
EXPORT ALL HAVING schema_name = 'my_schema' AND object_type = 'VIEW' AND
object_name != 'V2'
    INTO '/usr/sap/MS1/HDB01/work/incexc' WITH REPLACE DEPENDENCIES object _name
= 'T1';
```

## Related Information

CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) M_TRACEFILE_CONTENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) IMPORT Statement (Data Import Export) [→](IMPORT-Statement-Data-Import-Export.md) M_EXPORT_BINARY_STATUS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_EXPORT_BINARY_STATUS-System-View.md) SAP Note 2907201
