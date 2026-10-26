# 4.10.1.98 DROP REMOTE SOURCE Statement (Access Control)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 912–913

Removes an existing remote source.

## Syntax

```sql
DROP REMOTE SOURCE <remote_source_name> [<drop_option>]
```

## Syntax Elements

#### remote_source_name

Specifies the identifier of the remote source.

```sql
<remote_source_name> ::= <identifier>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

When `<drop_option>` is not specified, a RESTRICT drop is performed.

CASCADE drops the remote source and dependent objects.

RESTRICT drops the remote source only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

## Description

The DROP REMOTE SOURCE statement removes an existing remote source.

## Permissions

This statement requires the DROP object privilege on the remote source.

## Example

Create the remote source S and then drop it.

```sql
CREATE REMOTE SOURCE S ADAPTER ASEODBC
    CONFIGURATION 'DSN=ProductionASE'
    WITH CREDENTIAL TYPE 'PASSWORD' USING
'user="aseuser";password="asepassword"';
 DROP REMOTE SOURCE S;
```
