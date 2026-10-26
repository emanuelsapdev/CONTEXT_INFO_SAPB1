# 5.2.4 ALTER INDEX Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1222–1223

Changes the storage type of an index on a multistore table.

## Syntax

```sql
ALTER INDEX <index_name>
{CREATE|DROP} FOR {DEFAULT|EXTENDED} STORAGE
```

## Syntax Elements

#### index_name

Specifies the name of the index with an optional schema name.

```sql
<index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

## Description

The ALTER INDEX statement changes the storage type of the index on a multistore table.

The CREATE FOR clause adds the index to default or extended storage. The DROP FOR clause drops the index from the specified (extended or default) storage.

## Permissions

This statement requires the INDEX object privilege.

## Example

Create multistore table `ext_a`:

```sql
CREATE COLUMN TABLE EXT_A (c1 INT, c2 INT)
PARTITION BY RANGE (c1) (USING DEFAULT STORAGE
(PARTITION 0 <= values < 10000, PARTITION 10000 <= values < 1000000)
USING EXTENDED STORAGE (PARTITION 1000000 <= values < 100000000));
```

Create a partial index on the column store only:

```sql
CREATE BTREE INDEX idx_a ON ext_a (c1) FOR DEFAULT STORAGE;
```

Alter the index storage type to create it also on extended storage:

```sql
ALTER INDEX idx_a CREATE FOR EXTENDED STORAGE;
```

Change the index storage type to remove it from the column store. Now it is a partial index on extended storage only:

```sql
ALTER INDEX idx_a DROP FOR DEFAULT STORAGE;
```
