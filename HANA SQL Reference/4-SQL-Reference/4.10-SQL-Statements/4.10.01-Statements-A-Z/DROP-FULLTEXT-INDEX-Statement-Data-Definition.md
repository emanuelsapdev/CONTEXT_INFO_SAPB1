# 4.10.1.89 DROP FULLTEXT INDEX Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 902–903

Removes a full text index.

## Syntax

```sql
DROP FULLTEXT INDEX <index_name>
```

## Syntax Elements

#### index_name

Drops the specified full text index.

```sql
<index_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

## Description

The DROP FULLTEXT INDEX statement removes a full text index.

## Example

Create table A and then add an index, i, on column b of table A.

```sql
CREATE ROW TABLE A (a INT, b NVARCHAR(10), c NVARCHAR(20));
 CREATE INDEX i ON A(b);
```

Drop index i.

```sql
DROP FULLTEXT INDEX i;
```
