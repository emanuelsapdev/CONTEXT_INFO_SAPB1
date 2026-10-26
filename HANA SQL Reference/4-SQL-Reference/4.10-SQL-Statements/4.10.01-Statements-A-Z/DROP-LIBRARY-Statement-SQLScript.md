# 4.10.1.94 DROP LIBRARY Statement (SQLScript)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 907–908

Drops a SQLScript userdefined library.

## Syntax

```sql
DROP LIBRARY [ <schema_name>.]<library_name>
```

## Syntax Elements

#### library_name

Specifies the name of the SQLScript userdefined library to drop.

## Description

For more information on SQLScript userdefined libaries, see the SAP HANA SQLScript Reference.

## Examples

The following example drops the mylib library;

```sql
DROP LIBRARY mylib;
```

## Related Information

CREATE LIBRARY Statement (SQLScript) [→](CREATE-LIBRARY-Statement-SQLScript.md) ALTER LIBRARY Statement (SQLScript) [→](ALTER-LIBRARY-Statement-SQLScript.md) LIBRARIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARIES-System-View.md) LIBRARY_MEMBERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARY_MEMBERS-System-View.md)
