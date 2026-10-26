# 4.10.1.101 DROP SCHEMA Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 916–917

Removes a schema.

## Syntax

```sql
DROP SCHEMA <schema_name> [<drop_option>]
```

## Syntax Elements

#### schema_name

Drops the specified schema.

```sql
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the schema and all objects contained in the schema, regardless of which user created them. If there are objects in another schema that refer to objects in the schema being dropped, they are dropped if they belong to the user who is dropping the schema, otherwise they are invalidated.

Invalidated objects can be re-validated when an object that has same schema name is created.

RESTRICT drops the schema, but only when there are no objects in it. If RESTRICT is specified while there are still objects in the schema, then an error is returned.

If `<drop_option>` is not specified, then RESTRICT is used by default.

Invalidated objects can be re-validated when an object that has same schema name is created.

## Description

The DROP SCHEMA statement removes a schema.

Dropping a schema also drops any expression macros defined for the view. The list of all expression macros for a schema can be obtained by querying the VIEW_EXPRESSION_MACROS system view.

If you drop a schema, any schema synonym that references it is also dropped.

## Example

Create a schema named my_schema and a table named my_schema.t.

```sql
CREATE SCHEMA my_schema;
 CREATE ROW TABLE my_schema.t (a INT);
```

Drop my_schema with a CASCADE option.

```sql
DROP SCHEMA my_schema CASCADE;
```
