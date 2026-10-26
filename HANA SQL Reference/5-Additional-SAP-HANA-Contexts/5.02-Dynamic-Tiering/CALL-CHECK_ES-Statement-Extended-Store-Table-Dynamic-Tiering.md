# 5.2.12 CALL CHECK_ES Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1267–1270

Checks the validity of the current database in the extended store. Optionally, it corrects allocation problems for dbspaces or databases. CHECK_ES does not check a partitioned table if partitioned data exists in offline dbspaces.

## Syntax

```sql
CALL CHECK_ES ('<action>', '<object_type>', '<object_name>',
'<resource_percentage>')
```

## Syntax Elements

#### action

The type of consistency check to perform.

```sql
<action> ::=
 CHECK
 | VERIFY
 | ALLOCATION
 | ALLOCATION_LEAKED_BLOCKS
 | ALLOCATION_DUPLICATE_BLOCKS
 | ALLOCATION_UNALLOCATED_BLOCKS
 | DROPLEAKS
```

##### CHECK

Verifies that all database pages can be read for the entire database, main cache, specific index, specific index type, specific table, or specific dbspace. If the table is partitioned, then check mode will check the table’s partition allocation bitmaps.

Run in check mode if metadata, null count, or distinct count errors are returned when running a query. **VERIFY** Verifies the content of indexes for the entire database, or a specific index, table, or dbspace to detect keys or rows that are either missing or extras.

##### ALLOCATION

Checks allocation with blockmap information for the entire database, a specific index, a specific index type, specific table, or a specific dbspace. Does not check index consistency.

##### ALLOCATION_LEAKED_BLOCKS

Detects leaked blocks (allocated blocks unclaimed by any object in the specified target) for database or dbspace targets, and returns the block numbers for leaked blocks.

##### ALLOCATION_DUPLICATE_BLOCKS

Detects duplicate blocks (blocks for which two or more objects claim ownership) or extra blocks (unallocated blocks owned by an object), and returns the block numbers for duplicate blocks.

##### ALLOCATION_UNALLOCATED_BLOCKS

Checks allocation for the entire database, and returns block numbers for unallocated blocks.

##### DROPLEAKS

Resets the allocation map for the entire database or dbspace.

Allocation problems can be repaired in dropleaks mode.

#### object_type

Specifies the analyzed object:

```sql
<object_type> ::=
INDEX
 | DATABASE
 | TABLE
 | PARTITION
 | COLUMN
 | DBSPACE
```

If you specify DATABASE as your `<object_type>`, all dbspaces must be online.

#### object_name

Specifies the name of the analyzed object.

```sql
<object_name> :: =
 <indexname>
 | <table_name>
 | <column_name>
 | <dbspace_name>
 | NULL
```

##### indexname

May contain owner and table qualifiers: `[[<owner>.]<tablename>.]<indexname>`.

If `<owner>` is not specified, current user and database owner (`dbo`) are substituted in that order. If `<table>` is not specified, `<indexname>` must be unique.

##### table_name

May contain an owner qualifier `[<owner>.]<table_name>`.

If `<owner>` is not specified, current user and database owner (`dbo`) are substituted in that order. `<tablename>` cannot be a temporary or pre-join table.

> **Note**
>
> If either the table name or the index name contains spaces, enclose the `<tablename>` or `<indexname>` parameter in double quotation marks.

##### dbspace_name

The `<dbspace_name>` parameter contains no qualifiers. If it contains spaces, enclose it in double quotation marks.

The dbspace target examines a subset of the database's pages that belong to that dbspace. The dbspace must be online. The dbspace and database target are semantically equivalent when the table has only one dbspace.

##### NULL

NULL if you specify DATABASE for`<object_type>`.

#### resource_percentage

The resources percentage allows you to limit the CPU utilization of the database consistency checker by controlling the number of threads with respect to the number of CPUs. If you specify `<resource_percentage>` as 100 (the default value), then one thread is created per CPU. If you specify a value greater than 100, then there are more threads than CPUs, which might increase performance for some machine configurations. The value must be greater than 0; the minimum number of threads is 1.

## Permissions

The privilege needed depends on the clause used:

- Check action – CATALOG READ or DATA ADMIN
- Repair action – DATA ADMIN

## Description

CHECK_ES checks the validity of the current database in the extended store. Optionally, it corrects allocation problems for dbspaces or databases. CHECK_ES does not check a partitioned table if partitioned data exists in offline dbspaces.

Enclose the CHECK_ES parameter string in single quotes. It cannot be greater than 255 bytes in length.

If an identifier contains a dot, enclose object names in square brackets. For example:

```sql
call CHECK_ES('allocation','table','[SCH_A].[EXT.A]','100)
```

Depending on the execution mode, CHECK_ES output includes summary results, errors, informational statistics, and repair statistics. Error statistics are indicated by asterisks (\*\*\*\*\*), and appear only if errors are detected.

If a CHECK_ES call returns an error, use the ES_REBUILD_INDEX procedure to rebuild indexes for tables in extended storage, including extended store partitions of a multistore table.

For more information, see SAP HANA SQL and System Views Reference > SQL Reference > SQL Statements > Procedural Statements > CALL Statement (Procedural)

## Examples

This procedure checks the consistency of block allocation for the entire database, allocating a resource percentage of 100 percent (which creates one thread per CPU):

> **Sample Code**
>
> ```sql
> Call CHECK_ES ( 'allocation', 'database', '', '100' );
> ```

> **Output Code**
>
> ```sql
> Statistic                Value           Flag
> =========================================================
> DBCC Allocation Mode Report
> =========================================================
>    DBCC Status                 No Errors Detected
> =========================================================
> Allocation Summary
> =========================================================
>    Blocks Total                25600
>    Blocks in Current Version   5917
>    Blocks in All Versions      5917
>    Blocks in Use               5917
>    % Blocks in Use             23
> =========================================================
> Allocation Statistics
> =========================================================
>    Marked Logical Blocks       8320
>    Marked Physical Blocks      5917
>    Marked Pages                520
>    Blocks in Freelist          2071196
>    Imaginary Blocks            2014079
>    Highest PBN in Use          1049285
>    Total Free Blocks           19683
>    Usable Free Blocks          19382
>    % Total Space Fragmented    1
>    % Free Space Fragmented     1
>    Max Blocks Per Page         16
>    1  Block Page Count         165
>    3  Block Page Count         200
>    4  Block Page Count         1
>    10 Block Page Count         1
>    16 Block Page Count         153
>    2  Block Hole Count         1
>    3  Block Hole Count         19
>    6  Block Hole Count         12
>    7  Block Hole Count         1
>    10 Block Hole Count         1
>    15 Block Hole Count         1
>    16 Block Hole Count         1220
> ```
