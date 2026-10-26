# 4.10.1.136 RENAME INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1023–1024

Changes the name of an index.

## Syntax

```sql
RENAME INDEX <current_index_name> TO <new_index_name>
```

## Syntax Elements

#### current_index_name

Specifies the current index name with an optional schema name.

```sql
<current_index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### new_index_name

Specifies the new index name.

```sql
<new_index_name> ::= <identifier>
```

## Description

The RENAME INDEX statement changes the name of an index.

## Example

Create Table B and then index idx on column B of table B.

```sql
CREATE ROW TABLE B (A INT PRIMARY KEY, B INT);
 CREATE INDEX idx on B(B);
```

Show the list of index names on table B by using the INDEXES system table.

```sql
SELECT INDEX_NAME FROM INDEXES WHERE SCHEMA_NAME = CURRENT_SCHEMA AND TABLE_NAME
= 'B';
```

Rename index idx to new_idx.

```sql
RENAME INDEX idx TO new_idx;
```

Show a list of index names on table B after the renaming has occurred.

```sql
SELECT INDEX_NAME FROM INDEXES WHERE SCHEMA_NAME = CURRENT_SCHEMA AND TABLE_NAME
= 'B';
```

## Related Information

INDEXES System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) INDEX_COLUMNS System View [→](../../../6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md)
