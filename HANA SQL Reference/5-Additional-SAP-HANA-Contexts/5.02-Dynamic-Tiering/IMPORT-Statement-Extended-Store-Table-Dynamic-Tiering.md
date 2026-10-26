# 5.2.29 IMPORT Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1333–1337

Imports catalog objects into an extended store table.

## Syntax

```sql
IMPORT <import_object_name_list>
   FROM <path> [ <archive_file_name> ]
   [ WITH <import_option_list> ]
   [ AT <indexserver_host_port> ]
```

## Syntax Elements

#### import_object_name_list

Specifies the list of objects to be imported. The ALL and \* options are only for use when importing all objects from a specified schema.

```sql
<import_object_name_list> ::=
 <import_object_name>[, <import_object_name>[,...] ]
 | { ALL | * }
```

#### import_object_name

Specifies an object to import data from.

```sql
<import_object_name> ::= [ <schema_name>.]{<identifier> | "*" }
```

```sql
<schema_name> ::= <identifier>
```

[`<schema_name>`.]`<identifier>` specifies an object in a schema for import. `<schema_name>`."\*" specifies to select all objects within a schema for import.

#### FROM path [ archive_file_name ]

Specifies the location where the import source is found. Specify `<archive_file_name>` if the import data is in an archive file. This file is uncompressed at runtime as part of the import process. The archive file must have the file extension `.tar.gz` or `.tgz`.

```sql
<path> [ <archive_file_name> ] ::= <string_literal>
```

File locations for extended storage must be on a shared file system accessible to both SAP HANA and the extended storage system.

When using a distributed system, the FULL_PATH must point to a shared disk. Examples for import path, assuming the database instance is located at:

#### WITH import_option_list

Specifies a list of import options.

```sql
<import_option_list> ::= <import_option>[, <import_option>[,...] ]
```

```sql
<import_option> ::= REPLACE
   | CATALOG ONLY
   | NO DEPENDENCIES
   | THREADS <number_of_threads>
   | RENAME SCHEMA <rename_schema_list>
   | FAIL ON INVALID DATA
   | IGNORE EXISTING
   | STATISTICS ONLY
   | NO STATISTICS
   | TRACE
```

##### REPLACE

Defines the behavior if the import data already exists in the database. When specified, if a table defined in the import data currently exists in the database, then it is dropped and recreated before the data is imported. If the REPLACE option is not specified, then an error is thrown if an existing database table is defined in the import data.

##### CATALOG ONLY

Specifies that only the database catalog should be imported.

This option interacts with the STATISTICS ONLY and NO STATISTICS options.

##### DATA ONLY

Specifies that only the data in the import file should be imported, without updating or changing the metadata. This option is only valid when the specified target object has its own data, such as a table or a data statistics (as opposed to procedures and views, whose data is materialized from other objects at runtime). The target objects must exist in the database and their definition must match that of the data being imported. For CSV data without the REPLACE option, the import data is appended to the existing table data.

When specifying `IMPORT <schema_name>."*"...` and `IMPORT ALL...` with DATA ONLY, other objects that do not have records are ignored.

This option interacts with the STATISTICS ONLY and NO STATISTICS options.

##### NO DEPENDENCIES

Specifies to not import the underlying dependencies of an import object.

##### THREADS number_of_threads

Specifies how many objects are imported in parallel; the default is 1.

```sql
<number_of_threads> ::= <unsigned_integer>
```

Increasing number of threads reduces import time, but can also negatively affect database system performance. Consider the following items when you use this parameter. When importing:

- A single table – THREADS has no effect.
- A view or procedure – use two or more threads, up to the number of dependent objects.
- A whole schema – consider using more than 10 threads, with a maximum being the number of CPU cores in the system.
- A whole BW or ERP system database with tens of thousands of tables by using the ALL keyword – you can use up to 256 threads.

##### RENAME SCHEMA rename_schema_list

Specifies whether to rename the object's schema during the import.

```sql
<rename_schema_list> ::= <rename_schema_token>[{, <rename_schema_token>}]
```

```sql
<rename_schema_token> ::= <source_schema> TO <target_schema>
```

You cannot specify the same schema as both `<source_schema>` and `<target_schema>` in the same or different `<rename_schema_token>`.

##### IGNORE EXISTING

Does not import objects that already exist in the database. The IGNORE EXISTING option is ignored, if it is used in combination with REPLACE.

##### STATISTICS ONLY

Data statistics objects are imported by default, along with the objects they reference in `<import_object_name_list>` (for example, tables). When you specify STATISTICS ONLY, the metadata and data for non-statistics objects in `<import_object_name_list>` are excluded from the import.

If you specify:

- STATISTICS ONLY without DATA ONLY or CATALOG ONLY – then the data and metadata for data statistics objects are imported.
- STATISTICS ONLY and DATA ONLY – then only the data for the data statistics objects is imported.
- STATISTICS ONLY and CATALOG ONLY – then only the metadata for the data statistics objects is imported.

##### NO STATISTICS

Excludes data statistics objects from the import. Metadata and data for non-statistics objects in `<import_object_name_list>` are still imported, and they are impacted as normal by whether CATALOG ONLY or DATA ONLY is specified.

##### TRACE import_trace_file_name

Writes execution information to the specified trace file when importing data.

```sql
TRACE <import_trace_file_name>
<import_trace_file_name> ::= <string_literal>
```

The info level trace file contains detailed error descriptions for troubleshooting. The file is saved to the current trace directory.

The contents of the trace file can be found in the M_TRACEFILE_CONTENTS system view and contains information on:

- The single archive for the single archive import
- The import list
- Import feasibility checks
- Objects created and dropped during the import
- Schemas created during the import
- Schemas renamed during the import
- Metadata imported for column tables
- The format of the imported data (CSV)
- Indexes, triggers, and foreign keys created during the import
- The results table from the import

To delete the trace file, use the ALTER SYSTEM REMOVE TRACES statement.

#### indexserver_host_port

Specifies the index server on which tables are created and imported.

```sql
<indexserver_host_port> ::= '<host_name>:<port_number>'
```

If you specify the hostname and port, the tables are created and imported on there.

If you specify the `<host_name>` and `<port_number>`, then the tables are created and the data imported to that location.

## Permissions

You must have the IMPORT system privilege and the CREATE ANY privilege on the schema that is being imported into.

## Description

The IMPORT statement imports catalog objects (tables, views, synonyms, sequences, and procedures) that have previously been exported with the EXPORT statement (Extended Store Table). To import external data into existing tables use IMPORT statement (Extended Store Table).

The format (BINARY | CSV) of the file being imported is automatically detected.

You can only import exported binary files that were generated on an SAP HANA system with the same endianness.

Detailed results of the last execution of the IMPORT statement are stored in the following session-local temporary table `<current_schema>`.#IMPORT_RESULT. If no IMPORT has not been executed in the current session, selecting from `<current_schema>`.#IMPORT_RESULT returns an error. If `<current_schema>` of the session is invalid, then IMPORT throws an exception as it cannot create its result table for the `<current_schema>`.

| current_schema.#IMPORT_RESULT **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(255) | The schema of the imported object |
| OBJECT_NAME | NVARCHAR(255) | The name of the imported object |
| OBJECT_TYPE | VARCHAR(16) | The type of the imported object (TA BLE, VIEW, and so on) |
| LOCATION | VARCHAR(75) | The location (`<host>`:`<port>`) where the object was imported |

| **Column Name** | **Data Type** | **Description** |
| --- | --- | --- |
| STATUS | VARCHAR(16) | The import status (done, skipped, or failed) |
| ERROR | VARCHAR(512) | The error text in the case of an import failure |

## Example

Example 1: Import all tables from schema `testsch` using the REPLACE option and 10 execution threads.

```sql
IMPORT "testsch"."*" AS CSV FROM '/tmp' WITH REPLACE THREADS 10
```

Example 2: Import the schema `my_schema` and create the trace file `import.trc`.

```sql
IMPORT my_schema."*" FROM '/usr/sap/MS1/HDB01/work' WITH TRACE 'import.trc';
```

## Related Information

ALTER SYSTEM CANCEL [WORK IN] SESSION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CANCEL-WORK-IN-SESSION-Statement-System.md) M_CONNECTIONS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_CONNECTIONS-System-View.md) SAP Note 2050807 M_TRACEFILE_CONTENTS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) EXPORT Statement (Extended Store Table) [Dynamic Tiering] [→](EXPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md)
