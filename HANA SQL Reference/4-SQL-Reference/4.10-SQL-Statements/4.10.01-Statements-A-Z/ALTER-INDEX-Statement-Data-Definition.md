# 4.10.1.8 ALTER INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 436–438

Alters an index.

## Syntax

```sql
ALTER INDEX <index_name>
 REBUILD
 | UNIQUE <cs_inverted_type_index>
 | <load_unit>
```

## Syntax Elements

#### index_name

Specifies the name of the index to be rebuilt with an optional schema name.

```sql
<index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### REBUILD

Rebuilds the index.

#### UNIQUE cs_inverted_type_index

Changes the index type of a composite UNIQUE INVERTED index on a column store table.

##### cs_inverted_type_index

Specifies the inverted index type for column store tables. Inverted index types are only applicable to column store tables.

```sql
<cs_inverted_type_index> ::= INVERTED { HASH | VALUE | INDIVIDUAL }
```

###### INVERTED HASH

INVERTED HASH should not be used as a composite type in cases where range queries or similar queries on the composite keys are a significant part of the workload. In these cases, use INVERTED VALUE instead.

###### INVERTED VALUE

INVERTED VALUE is the default index type for column store tables.

###### INVERTED INDIVIDUAL

An INVERTED INDIVIDUAL index is a lightweight index type for column store tables with reduced memory footprint. The name INVERTED INDIVIDUAL reflects that internally only inverted indexes on individual columns are created (that is, no concat attributes are created). This type of index is only available for multi-column unique constraints, which may be defined as secondary unique index or primary key.

#### load_unit

Changes the load unit for a composite inverted (value or hash) index on a column store table.

```sql
<load_unit> ::= { COLUMN | PAGE | DEFAULT } LOADABLE
```

**COLUMN LOADABLE** The query results are loaded by column. This is the default for column store tables. **PAGE LOADABLE** The query results are loaded by page. **DEFAULT LOADABLE** If you specify DEFAULT, then there is no explicit preference for the load unit that is used when the results are loaded from the table. The index inherits the load unit setting from the first level above it (if specified): column, table, database. If there is no load unit setting to inherit, the default behavior is COLUMN LOADABLE.

Column store inverted indexes can be as large as the column itself. The `<load_unit>` setting of an index impacts the memory footprint of the index. For example, a PAGE LOADABLE index consumes much less memory, but may degrade performance slightly. This may be suitable for an index that is not frequently used. When performance is the priority, you may want to set the index to COLUMN LOADABLE, assuming the memory overhead is acceptable.

The load unit for an index is noted in the LOAD_UNIT column of the INDEXES system view.

## Description

Alters the specification for an existing index.

## Example

The following example creates table A1 and an INDEX_1 on column b of table A1:

```sql
CREATE TABLE A1 (a INT, b NVARCHAR(10), c NVARCHAR(20));
 CREATE INDEX_1 ON A1(b);
```

The following example rebuilds INDEX_1:

```sql
ALTER INDEX_1 REBUILD;
```

The following example alters INDEX_1 to use a target index type INVERTED HASH:

```sql
ALTER INDEX_1 UNIQUE INVERTED HASH;
```

The following example changes the load unit type for the myIDX index to PAGE LOADABLE:

```sql
ALTER INDEX myIDX PAGE LOADABLE;
```

## Related Information

[CREATE INDEX Statement (Data Definition)](CREATE-INDEX-Statement-Data-Definition.md)
