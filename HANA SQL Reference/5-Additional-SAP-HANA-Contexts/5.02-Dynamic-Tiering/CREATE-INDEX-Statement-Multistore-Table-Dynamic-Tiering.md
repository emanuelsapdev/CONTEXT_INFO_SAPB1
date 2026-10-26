# 5.2.18 CREATE INDEX Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1283–1285

Creates an index on a multistore table column.

## Syntax

```sql
CREATE [UNIQUE] [BTREE | CPBTREE] INDEX <index_name> ON <table_name>
   (<column_name_order_entry>[{, <column_name_order_entry>}...])
   [<global_index_order>] [<fillfactor>]
   [NOWAIT] [FOR {DEFAULT|EXTENDED} STORAGE]
```

## Syntax Elements

**UNIQUE** Defines that a unique index should be created. A duplicates check occurs when the index is created and when a record is added to the table. **BTREE** Specifies a B+ tree index type. B+ tree uses an index tree that maintains sorted data in a way that performs efficient insertion, deletion, and search of records. **CPBTREE** Specifies a CPB+ tree index type. CPB+ tree stands for Compressed Prefix B+ tree; this index tree type is based on pkB tree. CPB+ tree is a very small index because it uses partial key that is only part of full key in index nodes. CPB+ tree shows better performance than B+ tree for larger keys.

#### index_name

Specifies the name of the index to be created, with optional schema name.

```sql
<index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

**column_name_order_entry** Specifies the columns to be used in the index, with an optional ordering.

```sql
<column_name_order_entry> ::= <column_name> [<column_order>]
```

**column_order** Specifies whether the column index should be created in ascending or descending order. The default ordering is ASC.

```sql
<column_order> ::= ASC | DESC
```

**global_index_order** Specifies the index ordering for all columns in the index.

```sql
<global_index_order> ::= ASC | DESC
```

> **Note**
>
> `<column_order>` and `<global_index_order>` cannot be used when `<global_index_order>` is used.

**fillfactor** Specifies how each node of a new index is filled. It is a percentage value of integer from 50 to 100, and the default value is 90.

```sql
<fillfactor> ::= FILLFACTOR <unsigned_integer>
```

#### NOWAIT

Specifies that `CREATE INDEX` statement returns an error immediately if a table lock cannot be acquired.

```sql
<NOWAIT>
```

#### FOR {DEFAULT | EXTENDED} STORAGE

Specifies that `CREATE INDEX` creates a partial index on one store or the other. FOR DEFAULT STORAGE creates a partial index on the default store. FOR EXTENDED STORAGE creates a partial index on the extended store. If you don't specify the FOR STORAGE clause, the statement creates a regular index on default and extended stores instead of a partial index.

```sql
<FOR {DEFAULT  | EXTENDED} STORAGE >
```

## Permissions

You must have the INDEX object privilege.

## Description

The CREATE INDEX statement creates an index on a multistore table.

Only BTREE and CPBREE index types are supported on multistore tables.

## Example

Create multistore table `ext_a`:

```sql
CREATE COLUMN TABLE ext_a (c1 INT, c2 INT)
PARTITION BY RANGE (c1) (USING DEFAULT STORAGE
(PARTITION 0 <= values < 10000, PARTITION 10000 <= values < 1000000)
USING EXTENDED STORAGE (PARTITION 1000000 <= values < 100000000));
```

Create a partial index on the default store only:

```sql
CREATE BTREE INDEX idx_a ON ext_a (c1) FOR DEFAULT STORAGE;
```

Drop the partial index from the default store and create an index again on extended storage:

```sql
DROP INDEX idx_a;
CREATE BTREE INDEX idx_a ON ext_a(c1) FOR EXTENDED STORAGE;
```

## Related Information

INDEXES System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md)
