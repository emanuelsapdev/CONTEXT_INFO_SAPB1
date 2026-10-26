# 4.9.1.54 CURRENT_OBJECT_SCHEMA Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 164–165

Returns the current schema name when creating a view.

## Syntax

```sql
CURRENT_OBJECT_SCHEMA()
```

## Description

When creating a view, use the CURRENT_OBJECT_SCHEMA function where a schema name is required in the definition of the view, but a hard-coded schema name does not work. Currently, only the WORKDAYS_BETWEEN and CONVERT_CURRENCY functions support CURRENT_OBJECT_SCHEMA as replacement for an actual schema name.

## Example

The following example replaces CURRENT_OBJECT_SCHEMA with the name of the current schema (in this case, `SCHEMA1`):

```sql
CREATE VIEW SCHEMA1.VIEW1 AS SELECT WORKDAYS_BETWEEN('01', '2014-01-09',
'2014-01-10', CURRENT_OBJECT_SCHEMA()) FROM DUMMY;
```
