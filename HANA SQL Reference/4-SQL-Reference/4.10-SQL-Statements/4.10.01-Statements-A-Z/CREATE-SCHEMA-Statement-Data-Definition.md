# 4.10.1.62 CREATE SCHEMA Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 761–762

Creates a schema in the current database.

## Syntax

```sql
CREATE SCHEMA <schema_name> [OWNED BY <user_name>]
```

## Syntax Elements

#### schema_name

Specifies the schema name.

```sql
<schema_name> ::= <unicode_name>
```

#### user_name

Specifies the name of the schema owner. If omitted, the current user is the owner of the schema.

```sql
<user_name> ::= <unicode_name>
```

## Description

The CREATE SCHEMA statement creates a schema in the current database.

## Example

```sql
CREATE SCHEMA my_schema OWNED BY system;
```
