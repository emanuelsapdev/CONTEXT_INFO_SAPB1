# 5.2.17 CREATE INDEX Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1281–1283

Creates an index on an extended store table column.

## Syntax

```sql
CREATE [UNIQUE] [BTREE | CPBTREE] INDEX <index_name> ON <table_name>
   (<column_name_order_entry>[{, <column_name_order_entry>}...])
   [<global_index_order>] [<fillfactor>]
   [NOWAIT]
```

## Syntax Elements

**UNIQUE** Defines that a unique index should be created. A duplicates check occurs when the index is created and when a record is added to the table. **BTREE** Defines that a unique index should be created. A duplicates check occurs when the index is created and when a record is added to the table. **CPBTREE** Specifies a CPB+ tree index type. CPB+ tree stands for Compressed Prefix B+ tree; this index tree type is based on pkB tree. CPB+ tree is a very small index because it uses partial key that is only part of full key in index nodes. CPB+ tree shows better performance than B+ tree for larger keys.

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

## Permissions

You must have the INDEX object privilege.

## Description

The CREATE INDEX statement creates an index on an extended store table column.

Only BTREE and CPBREE index types are supported on extended store tables.

## Example

You create Table `t`, and then add index `idx` on column `b` of table `t` with ascending order.

```sql
CREATE ROW TABLE t (a INT, b NVARCHAR(10), c NVARCHAR(20)); CREATE INDEX idx ON
t(b);
```

Create a CPBTREE index `idx1` on column `a` of table `t` with ascending order and column `b` with descending order.

```sql
CREATE CPBTREE INDEX idx1 ON t(a, b DESC);
```

Create a CPBTREE index `idx2` on column `a` and `c` of table `t` with descending order.

```sql
CREATE INDEX idx2 ON t(a, c) DESC;
```

Create a UNIQUE CPBTREE index `idx3` on column `b` and `c` of table `t` with ascending order.

```sql
CREATE UNIQUE INDEX idx3 ON t(b, c);
```

Create a UNIQUE BTREE index `idx4` on column `a` of table `t` with ascending order.

```sql
CREATE UNIQUE INDEX idx4 ON t(a);
```

## Related Information

INDEXES System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md) INDEXES System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md)
