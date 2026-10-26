# 4.10.1.52 CREATE INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 721–725

Creates an index on a table column.

## Syntax

```sql
CREATE [ <index_type> ] INDEX <index_name> ON <table_name>
   ( <column_name_order_entry>[, <column_name_order_entry> [,...])
   [ <global_index_order> ]
   [ <fillfactor> ]
   [ NOWAIT ]
   [ ONLINE ]
   [ <load_unit> ]
```

## Syntax Elements

#### index_type

Defines the type of index to create.

```sql
<index_type> ::=
 UNIQUE
 | [ UNIQUE ] <rs_tree_type_index>
 | [ UNIQUE ] <cs_inverted_type_index>
```

When the index type (`<rs_tree_type_index>` or `<cs_inverted_type_index>`) is omitted, the database server chooses the appropriate type by considering the table type and the column data type.

'rs_' and 'cs_' at the beginning of the specification types indicate which type of table the specification corresponds to (row store and column store, respectively). If you mistakenly specify a row store index type and the table is a column store table, then the specification is ignored and the index is created as INVERTED VALUE (default). If you mistakenly specify a column store index type and the table is a row store table, an error is returned.

##### UNIQUE

Specifies that the index must have unique values. The optional `<rs_tree_type_index>` specification is only applicable to row store tables.

A composite unique key enables the specification of multiple columns as a unique key. With a unique constraint, multiple rows cannot have the same value in the same column.

A UNIQUE column can contain multiple NULL values.

##### rs_tree_type_index

Specifies the tree type for the index. Tree type specification is only applicable to row store tables.

```sql
<rs_tree_type_index> ::= { BTREE | CPBTREE }
```

###### CPBTREE

Specifies a CPB+-tree index for row store tables. CPB+-tree stands for Compressed Prefix B+-Tree, which is based on pkB-tree. CPB+-tree is a very small index because it uses 'partial key' that is only part of full key in index nodes. CPB+-tree shows better performance than B+-Tree for larger keys. Specify this type of tree for the following scenarios:

- for character string types
- for binary string types
- for decimal types
- when the constraint is a composite key
- when the constraint is a non-unique constraint

###### BTREE

Specifies a B+-tree index. B+-tree indexes maintain sorted data, which performs efficient insertion, deletion, and search of records. Specify this type of tree for scenarios not described for CPBTREE.

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

#### index_name

Specifies the name of the index to be created, with optional schema name.

```sql
<index_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

**column_name_order_entry** Specifies the columns to be used in the index, with an optional ordering.

```sql
<column_name_order_entry> ::= <column_name> [ <column_order> ]
```

**column_order** Specifies whether the column index should be created in ascending or descending order. The default ordering is ASC.

```sql
<column_order> ::= { ASC | DESC }
```

**global_index_order** Specifies the index ordering for all columns in the index.

```sql
<global_index_order> ::= { ASC | DESC }
```

`<column_order>` and `<global_index_order>` cannot be used when `<global_index_order>` is used. **fillfactor** Specifies how each node of a new index is filled. It is a percentage value of integer from 50 to 100, and the default value is 90.

```sql
<fillfactor> ::= FILLFACTOR <unsigned_integer>
```

#### NOWAIT

Specifies that the CREATE INDEX statement returns an error immediately in case a table lock cannot be acquired.

#### ONLINE

For column store tables, the ONLINE keyword allows the creation of the index without serializing with concurrent DML operations. This is only supported for non-replicated, non-history tables when creating a non-unique index on non-paged base columns. Creating an index in a supported case results in an operation that acquires a shared table lock. In the unsupported cases, or when the ONLINE keyword is omitted, an exclusive table lock is only taken for a short time at the beginning and end of the CREATE INDEX operation; during the rest of the CREATE INDEX operation, shared table lock is taken, which allows concurrent read and DML access operations but blocks concurrent DDL operations.

For row store tables, you can specify ONLINE to not place an exclusive lock on the table and enable read access during index creation; if ONLINE is not specified neither concurrent read nor DML operations are allowed during index creation.

#### load_unit

Specifies the load unit for the index. This clause is supported only for multi-column INVERTED VALUE indexes on column store tables.

```sql
<load_unit> ::= { COLUMN | PAGE } LOADABLE
```

**COLUMN LOADABLE** The query results are loaded by column. This is the default for column store tables. **PAGE LOADABLE** The query results are loaded by page.

Column store inverted indexes can be as large as the column itself. The `<load_unit>` setting of an index impacts the memory footprint of the index. For example, a PAGE LOADABLE index consumes much less memory, but may degrade performance slightly. This may be suitable for an index that is not frequently used. When performance is the priority, you may want to set the index to COLUMN LOADABLE, assuming the memory overhead is acceptable.

The load unit for an index is noted in the LOAD_UNIT column of the INDEXES system view.

You cannot use the `<load_unit>` clause to create an INVERTED HASH index since it supports only dictionary-based inverted hash keys. If you attempt to create it, the following type of error is returned:

`*7: feature not supported: Dictionary based inverted hash index with load unit hint: line 1 col 44 (at pos 43) SQLSTATE: HY000`

## Description

When column data types are character string types, binary string types, decimal types, or when the constraint is a composite key, or a non-unique constraint, the default index type is CPBTREE. In other cases BTREE is used. If neither BTREE nor CPBTREE keyword is specified, then the SAP HANA database chooses the appropriate index type.

For row store tables, when column data types are character string types, binary string types, decimal types, or when the constraint is a composite key, or a non-unique constraint, the default index type is CPBTREE. In other cases BTREE is used. If neither BTREE nor CPBTREE keyword is specified, then the SAP HANA database chooses the appropriate index type.

For column store tables, the default index type is always INVERTED VALUE. Other index-types, such as INVERTED HASH or INVERTED INDIVIDUAL, have to be explicitly specified.

To determine the maximum index key size, check the MAXIMUM_SIZE_OF_KEY_IN_INDEX value in the M_SYSTEM_LIMITS system view.

## Example

#### Row store index example

Create a row store table `t`, and then add the index `idx` on column `b` of table `t` with ascending order.

```sql
CREATE ROW TABLE t (a INT, b NVARCHAR(10), c NVARCHAR(20));
CREATE INDEX idx ON t(b);
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

#### Column store index example

Create table s, and then add the index idx10 on column b of table s.

```sql
CREATE TABLE s (a INT, b NVARCHAR(10), c NVARCHAR(20));
CREATE INDEX idx10 ON s(b);
```

Create an INVERTED VALUE index idx11 on column a of table s.

```sql
CREATE INVERTED VALUE INDEX idx11 ON s(a, b);
```

Create a unique INVERTED INDIVIDUAL index idx12 on column a and c of table s.

```sql
CREATE UNIQUE INVERTED INDIVIDUAL INDEX idx12 ON s(a, c);
```

Create a UNIQUE INVERTED VALUE index idx13 on column b and c of table s and set the load unit type to PAGE LOADABLE.

```sql
CREATE UNIQUE INVERTED VALUE INDEX idx13 ON s(b, c) PAGE LOADABLE;
```

The base columns b and c allow NULL values. The following inserts are possible:

```sql
INSERT INTO s VALUES(0, 1, NULL);
INSERT INTO s VALUES(1, NULL, NULL);
INSERT INTO s VALUES(2, NULL, NULL);
```

But the following insert will generate a unique constraint violation error:

```sql
INSERT INTO s VALUES(3, 1, NULL);
```

## Related Information

ALTER INDEX Statement (Data Definition) [→](ALTER-INDEX-Statement-Data-Definition.md) INDEXES System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md) M_SYSTEM_LIMITS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_LIMITS-System-View.md)
