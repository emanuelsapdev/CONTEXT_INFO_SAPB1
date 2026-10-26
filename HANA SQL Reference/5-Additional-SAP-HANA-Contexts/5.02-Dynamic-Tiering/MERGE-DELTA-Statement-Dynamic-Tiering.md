# 5.2.35 MERGE DELTA Statement [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1359–1361

On a delta-enabled extended store or multistore table, MERGE DELTA triggers a merge of data from the delta dbspace to the user dbspace. When used in a multistore table, you can restrict a manual delta merge to just the default store partition or extended store partition of the multistore table.

## Syntax

```sql
MERGE DELTA OF <table_name> [PART <n>]
   [WITH PARAMETERS (<parameter_list>, ...)] [FOR {DEFAULT | EXTENDED} STORAGE]
```

## Syntax Elements

#### table_name

The table name where the delta merge will occur, with optional schema name.

```sql
<table_name> ::= [<schema_name>.]<identifier>
```

```sql
<schema_name> ::= <unicode_name>
```

You can create a multistore table with delta enabled for extended storage partitions and default store partitions.

#### PART n

Merge the delta of a specific table partition to the table's main storage.

#### WITH PARAMETERS

Passes option that are specific to the column store.

```sql
<parameter_list> ::= <parameter> [{, <parameter>}...]
```

```sql
<parameter> ::= <parameter_name> = <parameter_setting>
```

```sql
<parameter_name> ::= 'SMART_MERGE'
```

```sql
<parameter_setting> ::= 'ON' | 'OFF'
```

When SMART_MERGE is ON, the database does a smart merge based on merge criteria specified in the mergedog section of the indexserver configuration. **FOR {DEFAULT | EXTENDED} STORAGE** (Optional) Specifies whether to merge just the default store partitions or the extended store partitions. If you do not specify this parameter, the delta merge is performed in the default store.

**DEFAULT** Restricts the delta merge to just the default (column) store partition in a multistore table. **EXTENDED** Restricts the delta merge to just the extended store partition in a multistore table.

## Permissions

You must have the UPDATE object privilege on the table.

## Description

On a delta-enabled table, MERGE DELTA triggers a merge of data from the delta dbspace to the user dbspace. As a table is read optimized and compressed, deltas are introduced to optimize insert or update operations. All insertions are passed to the delta storage. At a certain point in time, delta changes to a table can be merged into the table main storage.

When used in a multistore table, you can restrict a manual delta merge to just the default store partition or extended store partition of the multistore table.

The UPDATE privilege on the column store table is required for performing a delta merge.

The behavior of merge types in multistore tables:

| **Merge Type** | **Behavior for Multistore Tables** |
| --- | --- |
| Automerge | Automerge is the default setting for delta merges, and is supported in both default store and extended store partitions. |
| Smart merge | Specified with the `SMART_MERGE` parameter, a smart merge determines whether a merge is necessary for the default store.<br>A smart merge is not supported in the extended store partition of a multistore. |
| Hard merge | Uses the `MERGE DELTA OF '<table_name>'` syntax, and performs a merge regardless of store type. |
| Forced merge | Specified with the `FORCED_MERGE` parameter, a forced merge performs a hard merge while disregarding factors like storage size and system resource availability.<br>A forced merge is not supported in the extended store partition of a multistore. |
| Memory merge | Specified with the `MEMORY_MERGE` parameter, performs a delta merge only in memory, and the merge is not persisted.<br>A memory merge is not supported in the extended store partition of a multistore. |
| Critical merge | When a database performs a critical merge, it only merges the delta for the default store partition of a multistore table. |

## Examples

In these examples, t1 is a multistore table.

The following example merges the delta for the default store partition of the t1 multistore table:

```sql
MERGE DELTA of t1;
```

The behavior is the same if you were to specify the following:

```sql
MERGE DELTA of t1 FOR DEFAULT STORAGE;
```

The following example merges the delta for just the extended store partition of the t1 multistore table:

```sql
MERGE DELTA of t1 FOR EXTENDED STORAGE;
```

The following example triggers a delta merge for partition 32 in table t1. If the partition is an extended store partition, the merge occurs in the extended store:

```sql
MERGE DELTA of t1 PART 32;
```
