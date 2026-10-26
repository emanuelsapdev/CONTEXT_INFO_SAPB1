# 5.2.14 CALL ES_REBUILD_INDEX Statement (Multistore Tables) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1273–1274

When you encounter reports or errors running the CHECK_ES extended store database consistency checker, or if an index fails to meet performance expectations, call this procedure to rebuild indexes for tables in extended storage, including extended store partitions of a multistore table.

## Syntax

```sql
CALL ES_REBUILD_INDEX ( '<SCHEMA_NAME>' , '<TABLE_NAME>' , '<OBJECT_NAME>' ,
'<OBJECT_TYPE>', '<ESTIMATED_CARDINALITY>' )
```

## Syntax Elements

#### SCHEMA_NAME

The schema name.

#### TABLE_NAME

The table name.

#### OBJECT_NAME

The object name.

```sql
<OBJECT_NAME> ::=
{ COL_NAME | INDEX_NAME | NULL }
```

Use NULL when `<OBJECT_NAME>` is PRIMARY_KEY.

#### OBJECT_TYPE

The object type.

```sql
<OBJECT_TYPE> ::=
{ INDEX | COLUMN | PRIMARY_KEY }
```

- INDEX – for building HG indexes
- COLUMN – for building FP indexes
- PRIMARY_KEY – for rebuilding system-created primary key indexes

#### ESTIMATED_CARDINALITY

```sql
<ESTIMATED_CARDINALITY> ::=
{ INTEGER | NULL }
```

Use INTEGER when OBJECT_TYPE is COLUMN, and you are creating an Nbit index with non-default distinct count. Otherwise, use NULL.

## Permissions

You must have the DATA ADMIN privilege.

## Examples

- The following example rebuilds column-indexes:

```sql
CALL ES_REBUILD_INDEX ( 'SCH_1', 'TAB_1', 'COL_1', 'COLUMN', NULL )
```

- The following example rebuilds column indexes with distinct count:

```sql
CALL ES_REBUILD_INDEX ( 'SCH_1', 'TAB_1', 'COL_1', 'COLUMN', '1024' )
```

- The following example rebuilds user-created HG indexes:

```sql
CALL ES_REBUILD_INDEX ( 'SCH_1', 'TAB_1', 'IDX_1', 'INDEX', NULL )
```

- The following example rebuilds primary key-related HG indexes:

```sql
CALL ES_REBUILD_INDEX ( 'SCH_1', 'TAB_1', NULL, 'PRIMARY_KEY', NULL )
```
