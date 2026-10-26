# 4.10.1.137 RENAME SCHEMA Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1024–1026

Rename a schema without creating a new schema.

## Syntax

```sql
RENAME SCHEMA <source_schema_name> TO <target_schema_name>
```

## Syntax Elements

#### source_schema_name

Specifies the current name of the schema that you want to rename.

```sql
<source_schema_name>:;= <unicode_name>
```

#### target_schema_name

Specifies the new name of the schema.

```sql
<target_schema_name>:;= <unicode_name>
```

Attempting to use an existing schema name returns an error.

## Description

Rename an existing schema. The schema name of all objects in the source schema is also renamed. All privileges granted to schema objects, data contained in those objects, the validity of the objects, and object IDs are unaffected by the rename.

You cannot rename a user's default schema.

## Permissions

You must be the owner of the source schema and you must have the CREATE SCHEMA system privilege.

## Example

Execute the following statements to create two schemas, named schema0 and schema1:

```sql
CREATE SCHEMA schema0;
CREATE SCHEMA schema1;
```

Create and populate a table in schema1 and create views based on that table:

```sql
CREATE TABLE schema1.tb1(x, INT);
INSERT INTO schema1.tb1 VALUES (1);
CREATE VIEW schema1.vi1 AS SELECT * FROM schema1.tb1;
CREATE VIEW schema0.vi0 AS SELECT * FROM schema1.vi1;
```

Execute the following statement to rename schema1 to schema2:

```sql
RENAME SCHEMA schema1 TO schema2;
```

Execute the following SELECT statement:

```sql
SELECT * FROM schema2.tb1;
```

The statement executes successfully and returns `1` as a result, since the table schema1.tb1 has been renamed to schema2.tb1.

Execute the following SELECT statement:

```sql
SELECT * FROM schema2.vi1;
```

The statement executes successfully and returns `1` as a result, since the view schema1.vi1 has been renamed to schema2.vi1.

Execute the following SELECT statement:

```sql
SELECT * FROM schema0.vi0;
```

The statement returns an error indicating that it is invalid as the view schema0.vi0 relies on the view schema1.vi1, which has been renamed to schema2.vi2.

## Related Information

CREATE SCHEMA Statement (Data Definition) [→](CREATE-SCHEMA-Statement-Data-Definition.md) DROP SCHEMA Statement (Data Definition) [→](DROP-SCHEMA-Statement-Data-Definition.md) SET SCHEMA Statement (Session Management) [→](SET-SCHEMA-Statement-Session-Management.md)
