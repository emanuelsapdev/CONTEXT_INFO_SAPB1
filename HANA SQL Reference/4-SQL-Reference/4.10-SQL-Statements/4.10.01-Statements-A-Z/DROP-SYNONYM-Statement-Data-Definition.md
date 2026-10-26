# 4.10.1.106 DROP SYNONYM Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 924–925

Removes a synonym.

## Syntax

```sql
DROP [PUBLIC] SYNONYM <synonym_name> [<drop_option>]
```

## Syntax Elements

#### PUBLIC

Allows the removal of a public synonym.

#### SYNONYM synonym_name

Drops the specified synonym, with the optional schema name.

```sql
<synonym_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### drop_option

Specifies the drop option to use.

```sql
<drop_option> ::= CASCADE | RESTRICT
```

CASCADE drops the synonym and dependent objects. RESTRICT drops the synonym only when dependent objects do not exist. If this drop option is used and a dependent object exists, then an error is thrown.

If `<drop_option>` is not specified, then a non-cascaded drop is performed which only drops the specified synonym. Dependent objects of the synonym are invalidated but not dropped.

The invalidated object can be re-validated when an object that has same schema and object name is created.

## Description

The DROP SYNONYM statement removes a synonym.

## Permissions

Only database users with DROP object privilege on the remote source can drop a synonym from a remote source.

## Example

Create a table a, then a synonym, a_synonym, and a public synonym, pa_synonym, for the table.

```sql
CREATE ROW TABLE a (c INT);
 CREATE SYNONYM a_synonym FOR a;
 CREATE PUBLIC SYNONYM pa_synonym FOR a;
```

Drop both the synonym a_synonym and public synonym pa_synonym using a non-cascaded drop in both cases.

```sql
DROP SYNONYM a_synonym;
 DROP PUBLIC SYNONYM pa_synonym;
```
