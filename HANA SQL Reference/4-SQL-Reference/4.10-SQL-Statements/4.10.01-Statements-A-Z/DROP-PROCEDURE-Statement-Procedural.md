# 4.10.1.96 DROP PROCEDURE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 910–911

Deletes a procedure from the database.

## Syntax

```sql
DROP PROCEDURE <proc_name> [<drop_option>]
```

## Syntax Elements

#### proc_name

Specifies the name of the procedure to be dropped, and optionally, a schema name.

```sql
<proc_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies whether a cascaded drop is performed.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

When `<drop_option>` is not specified, then a non-cascaded drop be performed. Only the specified procedure is dropped; dependent objects of the procedure are invalidated, but they are not dropped.

The invalidated objects can be revalidated when an object that has same schema and object name is created.

##### CASCADE

Drops the procedure and dependent objects.

##### RESTRICT

Drops the procedure only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

## Description

Drops a procedure created using CREATE PROCEDURE from the database catalog.

## Examples

Drop a procedure called my_proc from the database using a non-cascaded drop.

```sql
DROP PROCEDURE my_proc;
```
