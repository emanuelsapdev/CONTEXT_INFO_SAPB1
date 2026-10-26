# 5.2.26 EXPORT Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1322–1327

Exports extended store tables, views, column views, synonyms, sequences, and procedures in CSV format.

## Syntax

```sql
EXPORT <export_object_name_list> AS CSV
    INTO <path> [ <archive_file_name> ]
   [ WITH <export_option_list> ]
[ <query_export_specification> ]
```

## Syntax Elements

#### export_object_name_list

Species a list of objects to export.

```sql
<export_object_name_list> ::=
 <export_object_name>[, <export_object_name>[,...] ]
 | { ALL | * }
```

```sql
<export_object_name> ::= [ <schema_name>.]{<identifier> | "*" }
```

```sql
<schema_name> ::= <unicode_name>
```

[`<schema_name>`.]`<identifier>` specifies objects in a schema for export. Specify `<schema_name."*">` to select all objects within the specified schema for export. Specify ALL (without `<schema_name>`) to select all objects from all schemas in the system for export.

#### AS CSV

The format to export the data to.

BINARY format is not supported. If specified, data is exported in CSV format with gzip compression

#### INTO path [ archive_file_name ]

Specifies the location where export files are placed.

```sql
<path> [ <archive_file_name> ] ::= <string_literal>
```

Include the file extension `.tar.gz` or `.tgz` on `<archive_file_name>` to export the data to an archive file.

File locations for extended storage must be on a shared file system available to both SAP HANA and the extended storage system.

For security reasons, the path must not contain symbolic links and must not point inside the database instance folder, except its `backup` and `work` subfolders. Examples of valid values include:

```sql
'/tmp'
'/hana/shared/HDB/HDB00/backup'
'/hana/shared/HDB/HDB00/work/myexport.tgz'
```

#### WITH export_option_list

A list of export options.

```sql
<export_option_list> ::= <export_option>[, <export_option>[,...] ]
```

```sql
<export_option> ::=
REPLACE
 | CATALOG ONLY
 | NO DEPENDENCIES
 | THREADS <number_of_threads>
 | STATISTICS ONLY
| NO STATISTICS
| TRACE
```

##### REPLACE

If REPLACE is not specified, then an error is returned if previously exported data exists in the specified export directory.

##### CATALOG ONLY

Specifies to export only the database catalog.

##### NO DEPENDENCIES

Specifies to not export the underlying dependencies of an export object.

##### THREADS number_of_threads

Specifies the number of process threads to be used for concurrent export processing.

```sql
<number_of_threads> ::= <unsigned_integer>
```

The THREADS parameter specifies how many objects are exported in parallel, the default is 1. Increasing number of threads reduces export time, but can also negatively affect database system performance. Consider the following items when you use this parameter. When exporting:

- A single table – THREADS has no effect.
- A view or procedure – use two or more threads, up to the number of dependent objects.
- A whole schema – consider using more than 10 threads. With a maximum being the number of CPU cores in the system.
- A whole BW or ERP system database with tens of thousands of tables by using the ALL keyword – you can use up to 256 threads.

##### STATISTICS ONLY

Data statistics objects are exported by default, along with the objects they reference in `<export_object_name_list>` (for example, tables). Export behavior depends on what you specify. If you specify:

- STATISTICS ONLY (no CATALOG ONLY) – both the data and metadata for data statistics objects are exported, as well as the metadata for the objects in `<export_object_name_list>`.
- STATISTICS ONLY and CATALOG ONLY – only the metadata for the data statistics objects and the objects in `<export_object_name_list>` are exported; no data is exported.

##### NO STATISTICS

Excludes data statistics objects from the export. Metadata and data for the objects in `<export_object_name_list>` are still exported, and they are impacted as normal by whether CATALOG ONLY is specified.

##### TRACE export_trace_file_name

Writes execution information to the specified trace file when exporting data.

```sql
<export_trace_file_name> ::= <string_literal>
```

The info level trace file contains detailed error descriptions for troubleshooting. The file is saved to the current trace directory.

The contents of the trace file can be found in the M_TRACEFILE_CONTENTS system view and contains information on:

- The export list
- Dependencies to the export list
- Feasibility checks on the export
- Metadata exported
- The format of the exported data (CSV)
- The single archive for a single archive export
- The results table from the export

To delete the trace file, use the ALTER SYSTEM REMOVE TRACES statement.

#### query_export_specification

Specifies a query to use for the export. See the SAP HANA SQLScript Reference for information on Query Exports.

```sql
<query_export_specification> ::=
 ON <sqlscript_location_list> FOR <procedure_call_statement>
```

## Permissions

You must have the EXPORT system privilege, and have SELECT privilege on the objects being exported.

## Description

The EXPORT command exports tables, views, column views, synonyms, sequences, or procedures in CSV format.

You can only import exported binary files that were generated on an SAP HANA system with the same endianness.

Detailed results of the last execution of the EXPORT statement are stored in the session-local temporary table `<current_schema>`..#EXPORT_RESULT. If no EXPORT has not been executed in the current session, selecting from `<current_schema>`.#EXPORT_RESULT returns an error. If `<current_schema>` of the session is invalid, then EXPORT throws an exception as it cannot create its result table in `<current_schema>`.

| current_schema.#EXPORT_RESULT **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(255) | Schema of the exported object. |
| OBJECT_NAME | NVARCHAR(255) | Name of the exported object. |
| OBJECT_TYPE | VARCHAR(16) | Type of the exported object (TABLE, VIEW, and so on). |
| LOCATION | VARCHAR(32) | Location (`<host>`:`<port>`) where the object was exported. |
| STATUS | VARCHAR(16) | Export status (done, skipped, failed). |

| **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| ERROR | VARCHAR(512) | Error text in case of export failure. |

For more information on permissions on the exported files, see SAP HANA Security Checklists and Recommendations.

## Examples

Example 1: Export the information from `MY_SCHEMA TAB1` in CSV format and overwrite data previously exported.

```sql
EXPORT MY_SCHEMA.TAB1 AS CSV INTO '/tmp' WITH REPLACE;
```

Example 2: Export all the database objects in schema `A` and `B`, replacing any existing export that may exist in the `/tmp` directory.

```sql
EXPORT A."*", B."*" AS CSV INTO '/tmp' WITH REPLACE THREADS 10;
```

Example 3: Export the results of a query where tables T1 and T2 are extended tables.

```sql
EXPORT ALL AS CSV INTO '/usr/sap/JL01/HDB00/work' FOR SELECT * FROM T1, T2;
```

Example 4: Save and export an entire directory in compressed form.

```sql
EXPORT MY_EXTENDED_TABLE AS CSV INTO '/usr/sap/P30/HDB30/work/myexport.tar.gz'
WITH REPLACE;
```

Example 4: Export the schema `MY_SCHEMA` and create the trace file `export.trc`.

```sql
EXPORT MY_SCHEMA."*" INTO '/usr/sap/MS1/HDB01/work' WITH TRACE 'export.trc';
```

## Related Information

ALTER SYSTEM CANCEL [WORK IN] SESSION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CANCEL-WORK-IN-SESSION-Statement-System.md) M_CONNECTIONS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_CONNECTIONS-System-View.md) M_TRACEFILE_CONTENTS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) IMPORT Statement (Extended Store Table) [Dynamic Tiering] [→](IMPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)
