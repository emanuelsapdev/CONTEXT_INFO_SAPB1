# 4.10.1.86 DROP COLLECTION Statement (JSON Document Store)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 898–900

Drops a collection table.

## Syntax

```sql
DROP COLLECTION [ TABLE ] <collection_name> <drop_option>
```

## Syntax Elements

#### collection_name

Specifies the name of the collection table to drop.

```sql
<collection_name> ::= [[<database_name>.]<schema_name>.]<identifier>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the collection table and any dependent objects. RESTRICT drops the collection table only when dependent objects do not exist. If RESTRICT is specified and a dependent object exists, then an error is returned.

If `<drop_option>` is not specified, then a non-cascaded drop is performed, which only drops the specified collection table. Dependent objects of the collection table are invalidated but not dropped.

## Description

Drops a collection table from the database. When you drop a collection table, all JSON documents stored in the collection table are removed as well.

DROP COLLECTION fails if `<identifier>` is a regular table, not a collection table.

## Examples

The following statement drops a collection table called `MyCollection`.

```sql
DROP COLLECTION MyCollection;
```

The following statement drops a collection table called `MyCollection2` and any associated views.

```sql
DROP COLLECTION MyCollection CASCADE;
```
