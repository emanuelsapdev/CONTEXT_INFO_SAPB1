# 4.10.1.126 MERGE DELTA Statement (Data Manipulation)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 994–995

Merges the column store table delta storage to the table's main storage.

## Syntax

```sql
MERGE [ HISTORY ] DELTA OF <table_name> [ PART <n> ]
   [ WITH PARAMETERS ( <parameter_list>, … ) ]
   [ FORCE REBUILD ]
```

## Syntax Elements

#### HISTORY

Merges the history-delta storage of a table into the history-main storage for column store temporal tables.

#### DELTA OF table_name

Specifies the table where the delta merge occurs, with the optional schema name.

```sql
<table_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### PART n

Merges the delta of a specific table partition to the table's main storage.

#### WITH PARAMETERS

Specifies options that are specific to the column store.

```sql
<parameter_list> ::= <parameter> [, <parameter> [,…] ]
<parameter> ::= <parameter_name> = <parameter_setting>
<parameter_name> ::= 'SMART_MERGE'
<parameter_setting> ::= 'ON' | 'OFF'
```

When SMART_MERGE is ON, the database does a smart merge based on merge criteria configured in `indexserver.ini`.

#### FORCE REBUILD

Force a delta merge even if the delta storage is empty and no deleted rows exist in the main storage that could be discarded. Use this option to create a new main storage matching the latest table definition (that is, reflecting current persistent memory preferences).

## Description

As a column store table is read, optimized, and compressed, deltas are introduced to optimize insert or update operations. All insertions are passed to the delta storage. At a certain point in time the delta changes to a table can be merged into the table main storage.

## Permissions

The UPDATE privilege on the column store table is required for performing a delta merge.

## Examples

Create history column table TableA.

```sql
CREATE HISTORY COLUMN TABLE TableA(c NVARCHAR(1000)) PARTITION BY ROUNDROBIN
PARTITIONS 2;
```

Merge the column store table delta storage to the tables main storage.

```sql
MERGE DELTA OF TableA;
```

Merge the column store table TableA using a smart merge.

```sql
MERGE DELTA OF TableA WITH PARAMETERS('SMART_MERGE' = 'ON');
```

Merge table TableA delta storage of partition 1 to the main storage of partition 1.

```sql
MERGE DELTA OF TableA PART 1;
```

Merge table TableA history-delta storage into its history-main storage.

```sql
MERGE DELTA OF TableA FORCE REBUILD;
```

Merge table TableA partition 1 history-delta storage to its history-main storage.

```sql
MERGE HISTORY DELTA OF TableA PART 1;
```
