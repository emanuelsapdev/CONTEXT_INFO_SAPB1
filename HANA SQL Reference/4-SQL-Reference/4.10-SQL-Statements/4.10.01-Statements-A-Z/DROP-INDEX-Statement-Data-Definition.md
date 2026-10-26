# 4.10.1.92 DROP INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 905–906

Removes an index.

## Syntax

```sql
DROP INDEX <index_name> [ ONLINE [ PREFERRED ] ]
```

## Syntax Elements

#### index_name

Drops the specified index, with the optional schema name.

```sql
<index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### ONLINE [ PREFERRED ]

Allows the dropping of the index without serializing with concurrent DML operations. ONLINE is only supported for column-store, non-replicated tables when dropping an index with non-paged base columns. The drop results in an operation that only acquires a shared table lock.

When PREFERRED is specified, if ONLINE execution is not supported, then a SQL warning message appears, and the drop index operation executes in table x-lock mode.

## Description

The DROP INDEX statement removes an index.

## Example

Create table A and then add an index, i, on column b of table A.

```sql
CREATE ROW TABLE A (a INT, b NVARCHAR(10), c NVARCHAR(20));
CREATE INDEX i ON A(b);
```

Drop index i.

```sql
DROP INDEX i;
```

## Related Information

INDEXES System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md)
