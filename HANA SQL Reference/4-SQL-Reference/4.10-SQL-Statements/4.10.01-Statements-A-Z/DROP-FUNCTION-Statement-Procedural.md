# 4.10.1.90 DROP FUNCTION Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 903–904

Deletes a function from the database.

## Syntax

```sql
DROP FUNCTION <func_name> [<drop_option>]
```

## Syntax Elements

#### func_name

Specifies the name of the function to be dropped, with optional schema name.

```sql
<func_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies whether a cascaded drop is performed.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

When `<drop_option>` is not specified, a non-cascaded drop is performed. This only drops the specified function; dependent objects of the function are invalidated but not dropped.

The invalidated objects can be revalidated when an object that has same schema and object name is created.

##### CASCADE

Drops the function and dependent objects.

##### RESTRICT

Drops the function only when dependent objects do not exist. If this drop option is used and a dependent object exists an error is thrown.

## Description

Drops a function created using CREATE FUNCTION from the database catalog.

## Examples

Drop a function called my_func from the database using a non-cascaded drop.

```sql
DROP FUNCTION my_func;
```
