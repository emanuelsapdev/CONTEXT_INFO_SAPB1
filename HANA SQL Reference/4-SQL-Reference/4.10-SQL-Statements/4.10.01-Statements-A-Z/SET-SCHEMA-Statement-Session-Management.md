# 4.10.1.147 SET SCHEMA Statement (Session Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1099–1100

Changes the default schema for the session to the specified schema.

## Syntax

```sql
SET SCHEMA <schema_name>
```

## Syntax Elements

#### schema_name

Specifies the name of the schema that the session should change to.

```sql
<schema_name> ::= <unicode_name>
```

If `<schema_name>` is the name of a schema synonym, then the current schema is set to the schema that is referenced by the schema synonym.

## Description

The user's schema is used as the default schema when executing a SQL statement that references database objects without specifying a schema name.

## Example

The following example creates a new schema called MY_SCHEMA, and then sets the default schema to it.

```sql
CREATE SCHEMA MY_SCHEMA;
SET SCHEMA MY_SCHEMA;
```

Now, if a table is created (for example, MY_TABLE) and no schema is specified, it is automatically created in the MY_SCHEMA schema. Likewise, a query such as `SELECT * FROM MY_TABLE;` would be equivalent to `SELECT * FROM MY_SCHEMA.MY_TABLE`.
