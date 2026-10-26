# 4.10.1.120 IMPORT Statement (Data Import Export)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 970–978

Imports catalog objects.

## Syntax

```sql
IMPORT <import_object_name_list>
 [ HAVING <object_condition> ] [ AS <format_option> ]
 FROM <path> [ <archive_file_name> ]
 [ WITH <import_option_list> ]
 [ AT [ LOCATION ] <indexserver_host_port> ]
 [ IGNORE NUMA NODE ]
```

## Syntax Elements

#### import_object_name_list

Specifies the list of objects to be imported. The ALL and \* options import all objects from a specified schema.

```sql
<import_object_name_list> ::=
 <import_object_name>[, <import_object_name>[,...] ]
 | CLIENTSIDE ENCRYPTION COLUMN KEY <encryption_column_key_name>[,
<encryption_column_key_name>[,...] ]
 | { ALL | * }
```

##### import_object_name

Specifies objects to import data from. Specify `<schema_name>`."\*" to select all objects within a schema for import. Specify ALL (without `<schema_name>`) to select all objects from all schemas in the system for export. `<schema_name>`,"\*" is not supported with the HAVING clause.

```sql
<import_object_name> ::= [ <schema_name>.]{<identifier> | "*" | ALL}
```

If you use SAP_TIMEZONE_DATASET as the `<format-option>` for the AS clause, then you can only specify \* or ALL for `<import_object_name_list>`.

##### encryption_column_key_name

Specifies the name of a column encryption key (CEK).

```sql
<encryption_column_key_name> ::= [ <schema_name>.]{<identifier> }
```

#### HAVING

Imports a subset of data from a specified object type.

```sql
HAVING <object_condition>
```

The HAVING clause cannot be used in conjunction with `<schema>`."\*".

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

#### AS format_option

Specifies the file type of the input source. CSV and BINARY are automatically detected.

```sql
<format_option> ::= CSV | BINARY | SHAPEFILE | LOAD_HISTORY |
SAP_TIMEZONE_DATASET
```

Specify LOAD_HISTORY to import load history traces; You can only specify one `<import_object_name>` when doing so.

#### FROM path [ archive_file_name ]

Specifies the location where the import source is found. Specify `<archive_file_name>` if the import data is in an archive file. The archive file must have the file extension `.tar.gz` or `.tgz`.

```sql
<path> [ <archive_file_name> ] ::= <string_literal>
```

If AS LOAD_HISTORY is specified, then `<path>` must point to a directory that contains the unzipped dump created with `fullSystemInfoDump.py` or directly to a load history file.

If AS SHAPEFILE is specified, then `<path>` must include the directory plus the base name of the shapefile(s) (there are usually 3 files). For example, `/path/to/data/myshape`. Refer to the SAP HANA Spatial Reference guide for a complete documentation on importing from shapefiles.

If AS SAP_TIMEZONE_DATASET is specified, then `<path>` must point to a directory that contains the `tzdata.dat` file that was downloaded from 198411 , or a similarly formatted file. If no import schema is specified, then the default timezone table schema is used.

In distributed systems, `<path>` must be a shared disk; otherwise, the operation may fail or have unexpected results.

#### WITH import_option_list

Specifies a list of import options. If AS LOAD_HISTORY or AS SAP_TIMEZONE_DATASET is also specified, then WITH REPLACE is the only supported import option.

```sql
<import_option_list> ::= <import_option>[, <import_option>[,...] ]
<import_option> ::=
 REPLACE
 | CATALOG ONLY
 | DATA ONLY
 | NO DEPENDENCIES
 | DEPENDENCIES <object_condition>
 | THREADS <number_of_threads>
 | RENAME SCHEMA <rename_schema_list>
 | FAIL ON INVALID DATA
 | IGNORE EXISTING
 | PERSISTENT MEMORY
 | STATISTICS ONLY
 | NO STATISTICS
 | LOOPBACK REMOTE SOURCE
 | RENAME REMOTE OBJECT
 | <shapefile_option_list>
 | TRACE
```

##### REPLACE

Defines the behavior if the import data already exists in the database. When specified, if a table defined in the import data currently exists in the database, then it is dropped and recreated before the data is imported. If the REPLACE option is not specified, then an error is thrown if an existing database table is defined in the import data.

##### CATALOG ONLY

Imports only the database catalog.

This option interacts with the STATISTICS ONLY and NO STATISTICS options.

##### DATA ONLY

Specifies that only the data in the import file should be imported, without updating or changing the metadata. This option is only valid when the specified target object has its own data, such as a table or a data statistics (as opposed to procedures and views, whose data is materialized from other objects at runtime). The target objects must exist in the database and their definition must match that of the data being imported.

When specifying `IMPORT <schema_name>."*"...` and `IMPORT ALL...` with DATA ONLY, other objects that do not have records are ignored.

For BINARY data, the existing table data is overwritten with the imported data. For CSV data without the REPLACE option, the import data is appended to the existing table data.

This option interacts with the STATISTICS ONLY and NO STATISTICS option and is not supported for virtual tables.

##### NO DEPENDENCIES

Specifies to not import the underlying dependencies of an import object.

##### DEPENDENCIES

Specifies the underlying dependencies of an object to import.

```sql
DEPENDENCIES <object_condition>
```

For the types of conditions you can specify, see `<condition_list>`.

##### THREADS number_of_threads

Specifies how many objects are imported in parallel; the default is 1.

```sql
<number_of_threads> ::= <unsigned_integer>
```

Increasing the number of threads reduces import time, but can also negatively affect database system performance. Consider these items when you use this parameter:

- When importing a single table, THREADS has no effect.
- When importing a view or procedure, two or more threads should be used, up to the number of dependent objects.
- When importing a whole schema consider using more than 10 threads. With a maximum being the number of CPU cores in the system.
- When importing a whole BW/ERP system database with tens of thousands of tables by using the ALL keyword, a large number of threads can be used (up to 256).

##### RENAME SCHEMA rename_schema_list

Specifies whether to rename the object's schema during the import.

```sql
<rename_schema_list> ::= <rename_schema_token>[,
<rename_schema_token>[,   ] ]
<rename_schema_token> ::= <source_schema> TO <target_schema>
```

You cannot specify the same schema as both `<source_schema>` and `<target_schema>` in the same or a different `<rename_schema_token>`.

##### FAIL ON INVALID DATA

Fails the import operation if not all data is imported successfully.

##### IGNORE EXISTING

Does not import objects that already exist in the database. The IGNORE EXISTING option is ignored, if it is used in combination with REPLACE.

**PERSISTENT MEMORY** Imports persistent memory data files from exported data into persistent memory. If no persistent memory data files are found, then this clause is ignored. If this option is specified and persistent memory is not configured for the database, then the IMPORT statement fails.

##### STATISTICS ONLY

Data statistics objects are imported by default, along with the objects they reference in `<import_object_name_list>` (for example, tables). When you specify STATISTICS ONLY, the metadata and data for non-statistics objects in `<import_object_name_list>` are excluded from the import.

If you specify STATISTICS ONLY without DATA ONLY or CATALOG ONLY, then the data and metadata for data statistics objects are imported.

If you specify STATISTICS ONLY and DATA ONLY, then only the data for the data statistics objects is imported.

If you specify STATISTICS ONLY and CATALOG ONLY, then only the metadata for the data statistics objects is imported.

##### NO STATISTICS

Excludes data statistics objects from the import. Metadata and data for non-statistics objects in `<import_object_name_list>` are still imported, and they are impacted as normal by whether CATALOG ONLY or DATA ONLY is specified. **LOOPBACK REMOTE SOURCE** Creates a reproduction workflow for virtual tables. When importing tables, a loopback remote source is created that points to the local SAP HANA server. For every virtual table imported, a corresponding dummy local table is created with the same metadata. Virtual tables are then created by using this loopback remote source and the dummy local tables. **RENAME REMOTE OBJECT** Specify a mapping of the old remote object to new remote object when importing virtual tables into another system.

When importing virtual tables, each virtual table is created by using the same remote source and remote object when it was exported by default.

##### shapefile_option_list

Refer to the SAP HANA Spatial Reference guide for the current, complete option list for importing shapefiles.

##### TRACE import_trace_file_name

Writes execution information to the specified trace file when importing data.

```sql
<import_trace_file_name> ::= <string_literal>
```

The info level trace file contains detailed error descriptions for troubleshooting. The file is saved to the current trace directory.

The contents of the trace file can be found in the M_TRACEFILE_CONTENTS system view. It contains information on:

- The single archive for the single archive import
- The import list
- Import feasibility checks
- Objects created and dropped during the import
- Schemas created during the import
- Schemas renamed during the import
- Metadata imported for column tables
- The format of the imported data (binary or CSV)
- Indexes, triggers, and foreign keys created during the import
- The results table from the import

To delete the trace file, use the ALTER SYSTEM REMOVE TRACES statement.

#### AT LOCATION indexserver_host_port

Specifies the index server on which tables are created and imported.

```sql
<indexserver_host_port> ::= '<host_name>:<port_number>'
```

If you specify the hostname and port, then the tables are created and imported at that location.

#### IGNORE NUMA NODE

By default, SAP HANA attempts to apply the NUMA node preferences that were set in the source system for the table you are importing. If the number of NUMA nodes on the target system is greater than or equal to the number on the source system, then the NUMA node preferences are applied. If the target system has fewer NUMA nodes, then the NUMA node preferences are ignored.

Specify IGNORE NUMA NODE to override the default behavior and not import NUMA location preferences into the target system.

## Permissions

You must have the IMPORT and CREATE TEMPORARY TABLE system privileges. You also need the CREATE ANY privilege on the schema that is being imported into. If the schema being imported does not exist, you must also have the CREATE SCHEMA system privilege. If the REPLACE option is specified, you must also have the DROP privilege on the schema being imported into.

In addition to the IMPORT privilege, you must have CLIENTSIDE ENCRYPTION COLUMN KEY ADMIN privilege on the schema and CREATE CLIENTSIDE ENCRYPTION KEYPAIR privilege to import CEKs.

## Description

The IMPORT statement imports catalog objects (tables, views, synonyms, sequences, and procedures) that have previously been exported with the EXPORT statement. To import external data into existing tables, use the IMPORT FROM statement. The IMPORT statement can also import load history data that is stored in `nameserver_history.trc` files and timezone definitions according to SAP note 198411 .

The format (BINARY or CSV) of the file being imported is detected automatically.

You can only import exported binary files that were generated on an SAP HANA system with the same endianness.

System-versioned tables and their associated history table must be imported separately. After import, execute an ALTER TABLE statement to associate the system-versioned table and its history table and specify NOT VALIDATED to bypass the check for whether the history table is empty.

Cancel an import session by using the ALTER SYSTEM CANCEL WORK IN SESSION statement and specifying the connection ID from the M_IMPORT_BINARY_STATUS view.

When using CSV format to export/import tables that have columns of type GENERATED ALWAYS AS `<expression>`, verify that the imported records match what was exported. If there are anomalies:

- For column tables, switch to exporting/importing as BINARY.
- For row tables, change the table to be a column table and export/import as BINARY.

For client-side encryption, importing a table with encrypted columns fails if there are no CEK copies for a given CEK used by the table. Importing a CEK copy imports the corresponding public keys of client key pairs as well. Importing a CEK WITH REPLACE fails if the existing CEK encrypts a column. Importing encrypted data into an existing table requires the UUIDs of the CEKs of the exported data to match the UUIDs of the CEKs of existing table columns.

A table with encrypted columns along with the CEK copies and public keys may be successfully imported into a new database, but you cannot access the encrypted data if the corresponding private keys are also not available to the clients trying to access that data. Either the clients accessing imported encrypted column must be the same clients that accessed them before and already have the private keys, or the private keys must be exported from the old clients and imported into the new ones separately.

Detailed results of the last successful execution of the IMPORT statement are stored in the following session-local temporary table `<current_schema>`.#IMPORT_RESULT. If IMPORT has not been executed in the current session, selecting from `<current_schema>`.#IMPORT_RESULT returns an error. If `<current_schema>` of the session is invalid, then IMPORT throws an exception as it cannot create its result table for the `<current_schema>`.

current_schema.#IMPORT_RESULT

| **Column Name** | **Data type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | NVARCHAR(256) | The database of the imported object |
| SCHEMA_NAME | NVARCHAR(256) | The schema of the imported object |
| OBJECT_NAME | NVARCHAR(256) | The name of the imported object |
| OBJECT_TYPE | VARCHAR(32) | The type of the imported object (TA BLE, VIEW, and so on) |
| LOCATION | VARCHAR(75) | The location (`<host>`:`<port>`) where the object was imported |
| STATUS | VARCHAR(16) | The import status (done, skipped, or failed) |
| ERROR | VARCHAR(512) | The error text in the case of an import failure |

## Example

The following example imports the contents of the `tzdata.dat` into the default timezone table schema:

```sql
IMPORT * AS SAP_TIMEZONE_DATASET FROM '/path/to/tzdata.dat;
```

The following example imports a client-side encryption key:

```sql
IMPORT CLIENTSIDE ENCRYPTION COLUMN KEY MYSCHEMA.MYCEK1, MYSCHEAM.MYCEK2 FROM '/
path/to/cek';
```

This example imports all tables from schema `TESTSCH` by using the REPLACE option and ten execution threads.

```sql
IMPORT TESTSCH."*" AS CSV FROM '/tmp' WITH REPLACE THREADS 10;
```

This example imports the load history data that is stored in an unzipped dump in directory `/path/to/dump` into the tables `MYSCHEMA.DATA_LOAD_HISTORY_HOST` and `MYSCHEMA.DATA_LOAD_HISTORY_SERVICE`:

```sql
IMPORT MYSCHEMA.DATA AS LOAD_HISTORY FROM '/path/to/dump';
```

This example imports the load history data from the given `nameserver_history.trc` file into the tables `MYSCHEMA.DATA_LOAD_HISTORY_HOST` and `MYSCHEMA.DATA_LOAD_HISTORY_SERVICE`:

```sql
IMPORT MYSCHEMA.DATA AS LOAD_HISTORY FROM '/path/to/nameserver_history.trc';
```

This example imports the schema `MY_SCHEMA` and creates the trace file `import.trc`:

```sql
IMPORT MY_SCHEMA."*" FROM '/usr/sap/MS1/HDB01/work' WITH TRACE 'import.trc'
REPLACE;
```

This example imports the schema from table T14, but ignores the NUMA NODE preferences.

```sql
IMPORT SYSTEM."T14" FROM '/tmp/test/' WITH REPLACE THREADS 40 IGNORE NUMA NODE;
```

In this example, `MY_SCHEMA` has two tables, `T1` and `T2`, each with column `A`, and two views. V1 selects T1.a from T1 and T2. V2 selects \* from T2. The following syntax imports the object type `VIEW` and all object names not equal to `V2`. It also imports its dependency `T1`.

```sql
IMPORT ALL HAVING schema_name = 'my_schema' AND object_type = 'VIEW' AND
object_name != 'V2'
    FROM '/usr/sap/MS1/HDB01/work' WITH REPLACE DEPENDENCIES object _name = 'T1';
```

## Related Information

CREATE CLIENTSIDE ENCRYPTION COLUMN KEY Statement (Encryption) [→](CREATE-CLIENTSIDE-ENCRYPTION-COLUMN-KEY-Statement-Encryption.md) M_TRACEFILE_CONTENTS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) ALTER SYSTEM REMOVE TRACES Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-REMOVE-TRACES-Statement-System-Management.md) EXPORT Statement (Data Import Export) [→](EXPORT-Statement-Data-Import-Export.md) M_IMPORT_BINARY_STATUS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_IMPORT_BINARY_STATUS-System-View.md)

IMPORT FROM Statement (Data Import Export) [→](IMPORT-FROM-Statement-Data-Import-Export.md) ALTER SYSTEM CANCEL [WORK IN] SESSION Statement (System Management) [→](4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CANCEL-WORK-IN-SESSION-Statement-System.md)
