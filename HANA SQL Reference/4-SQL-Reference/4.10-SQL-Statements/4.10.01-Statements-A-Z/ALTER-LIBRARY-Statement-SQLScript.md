# 4.10.1.10 ALTER LIBRARY Statement (SQLScript)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 440–441

Alters a SQLScript userdefined library.

## Syntax

```sql
ALTER LIBRARY [ <schema_name>.]<library_name>
 [ LANGUAGE SQLSCRIPT ]
 AS BEGIN
   [ <sqlscript_user_defined_library_spec> ]
 END;
```

## Syntax Elements

#### library_name

Specifies the name of the SQLScript userdefined library.

#### sqlscript_user_defined_library_spec

Specifies the body of the new SQLScript userdefined library. See the SAP HANA SQLScript Reference for the syntax allowed in a SQLScript language library.

## Description

Use this statement to alter a SQLScript userdefined library in an SAP HANA database.

## Examples

The following example creates a table, creates a SQLScript userdefined library that operates on the table, and then alters the body of the library, replacing it to be BEGIN END:

```sql
CREATE TABLE data_table(col1 INT);

CREATE LIBRARY mylib AS BEGIN
   PUBLIC VARIABLE maxval CONSTANT INT = 100;
   PUBLIC PROCEDURE get_data(IN size INT, OUT result table(col1 INT)) AS
      BEGIN
        RESULT = SELECT TOP :size col1 FROM data_table;
      END;
   END;

ALTER LIBRARY mylib AS BEGIN END;
```

## Related Information

CREATE LIBRARY Statement (SQLScript) [→](CREATE-LIBRARY-Statement-SQLScript.md) DROP LIBRARY Statement (SQLScript) [→](DROP-LIBRARY-Statement-SQLScript.md) LIBRARIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARIES-System-View.md) LIBRARY_MEMBERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARY_MEMBERS-System-View.md)
