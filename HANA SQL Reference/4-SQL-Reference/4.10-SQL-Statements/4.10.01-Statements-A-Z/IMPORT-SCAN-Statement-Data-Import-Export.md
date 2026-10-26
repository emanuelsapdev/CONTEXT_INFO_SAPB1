# 4.10.1.122 IMPORT SCAN Statement (Data Import Export)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 985–986

Searches the specified path for exported objects.

## Syntax

```sql
IMPORT SCAN <path>
```

## Syntax Elements

#### path

Specifies the path of the directory to be scanned for import data.

```sql
<path> ::= <string_literal>
```

## Description

The IMPORT SCAN statement searches the given path for objects exported with the EXPORT statement and stores its results in the following session-local temporary table at current_schema of the session if the statement is executed successfully. If current_schema of the session is invalid, then IMPORT SCAN throws an exception as it cannot create its result table of the current_schema.

`<current_schema>`**.#IMPORT_SCAN_RESULT**

| **Column Name** | **Data type** | **Description** |
| --- | --- | --- |
| DATABASE_NAME | NVARCHAR(256) | The database of the imported object |
| SCHEMA_NAME | NVARCHAR(256) | The schema of the object |
| OBJECT_NAME | NVARCHAR(256) | The name of the object |
| OBJECT_TYPE | VARCHAR(32) | The type of the object (TABLE, VIEW, and so on) |
| EXISTS | TINYINT | Does the object already exist in the system? (0/1) |

## Example

Scan the path `'/data/import_path'` for import data.

```sql
IMPORT SCAN '/data/import_path';
```

Select the data in the #IMPORT_SCAN_RESULT table to get the result of the scan.

```sql
SELECT * FROM #IMPORT_SCAN_RESULT;
```

## Related Information

[EXPORT Statement (Data Import Export)](EXPORT-Statement-Data-Import-Export.md)
