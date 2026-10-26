# 4.10.1.67 CREATE SYNONYM Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 776–778

Creates an alternate name for a table, view, procedure, or sequence.

## Syntax

```sql
CREATE [ OR REPLACE ] [ PUBLIC ] SYNONYM <synonym_name> FOR
<synonym_source_object_name>
```

## Syntax Elements

#### OR REPLACE

Replaces the definition of the synonym if it already exists. A CREATE OR REPLACE operation does not change the ID of the synonym, nor any privileges associated with it.

#### synonym_name

Specifies the name of the synonym to be created, with optional schema name.

```sql
<synonym_name> ::= [ <schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

When you create a synonym for PUBLIC, you cannot specify a schema name (`<schema_name>`).

#### synonym_source_object_name

Specifies the object you are creating a synonym for.

```sql
<synonym_source_object_name> ::=
 <table_name>
 | <view_name>
 | <procedure_name>
 | <sequence_name>
<table_name> ::= [ [ <database_name>.]<schema_name>.]<identifier>
<view_name> ::= [ <schema_name>.]<identifier>
<sequence_name> ::= [ <schema_name>.]<identifier>
<procedure_name> ::= [ <schema_name>.]<identifier>

<database_name> ::= <identifier>
<schema_name> ::= <unicode_name>
```

`<database_name>` can only be applied to tables and views, not to sequences or procedures.

The `<database_name>` syntax can be used only in a system with multiple database containers where cross-database access is enabled for the given database name.

For linked database, `<database_name>` is the name of the remote source. `<identifier>` is the name of the table on the remote source.

## Description

Use a synonym to re-point functions and stored procedures to differing tables, views, or sequences without rewriting the function or stored procedure.

The optional PUBLIC element allows you to create a public synonym.

## Permissions

No additional privilege is required to create a synonym on an object within your own schema. The CREATE ANY object privilege is required to create synonym on an object within another user's schema.

Any user can access a public synonym, but only the users that have the proper privileges on its base object can access the base object.

## Example

Create table A.

```sql
CREATE ROW TABLE A (A INT PRIMARY KEY, B INT);
```

Create a synonym for table A, a_synonym.

```sql
CREATE SYNONYM a_synonym FOR A;
```
