# 4.10.1.109 DROP TYPE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 928–930

Removes a userdefined table type.

## Syntax

```sql
DROP TYPE <type_name> [<drop_option>]
```

## Syntax Elements

#### type_name

Specifies the table type to be dropped with optional schema name.

```sql
<type_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the desired drop behavior.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

The default behavior is to drop only the specified table type, regardless of dependencies. When RESTRICT is specified, an error is returned if there are any objects (currently only tables are supported) that are dependent on the type. When CASCADE is specified, both the specified type and any dependent objects are dropped. For example, assume there is a type T being used by a database object O:

- DROP TYPE T - Only type T is dropped; object O becomes invalid.
- DROP TYPE T RESTRICT - The drop operation fails and an error is returned (because O is dependent on type T).
- DROP TYPE T CASCADE - Both type T and object O are dropped.

## Description

The DROP TYPE statement removes a userdefined table type.

To find invalid objects in the database, look at the IS_VALID columns in the relevant system view. For example, you can look at the IS_VALID column of the TABLES system view to determine which tables are valid.

Invalidated objects can be revalidated when an object that has same schema and object name is created.

## Example

Create a table type called my_type.

```sql
CREATE TYPE "my_type" AS TABLE ( "column_a" DOUBLE );
```

Drop the my_type table type.

```sql
DROP TYPE "my_type";
```
