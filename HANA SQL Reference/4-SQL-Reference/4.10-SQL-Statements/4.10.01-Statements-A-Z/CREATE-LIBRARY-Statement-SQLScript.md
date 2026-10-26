# 4.10.1.54 CREATE LIBRARY Statement (SQLScript)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 727–729

Creates a SQLScript userdefined library.

## Syntax

```sql
CREATE [ OR REPLACE ] LIBRARY [ <schema_name>.]<library_name>
 [ LANGUAGE { SQLSCRIPT | SQLSCRIPT TEST } ]
 AS BEGIN
   <sqlscript_user_defined_library_spec>
 END;
```

## Syntax Elements

#### OR REPLACE

Specifying OR REPLACE replaces the existing library, if one exists, with the new definition.

#### library_name

Specifies a name for the new SQLScript userdefined library.

#### LANGUAGE

Specifies the type of library:

##### SQLSCRIPT

Specifies that the library will be a SQLScript library.

##### SQLSCRIPT TEST

Specifies that the library will be a SQLScript end-user test framework.

#### sqlscript_user_defined_library_spec

Specifies the body of the new SQLScript userdefined library.

See the SAP HANA SQLScript Reference for the syntax allowed in a SQLScript library.

## Description

Use this statement to define a SQLScript library in an SAP HANA database.

A SQLScript userdefined library is a library written in the SQLScript language that can be called by other procedures or functions. A SQLScript library can only be used by SQLScript procedures or functions; it is not available for use in other SQL statements.

## Examples

The following example statements create a table, a SQLScript userdefined library that operates on the table, and a procedure that calls the new library.

```sql
CREATE TABLE data_table(col1 INT);
 DO BEGIN
  DECLARE idx INT = 0;
  FOR idx IN 1..200 DO
    INSERT INTO data_table VALUES (:idx);
  END FOR;
 END;
CREATE OR REPLACE LIBRARY mylib AS BEGIN
  PUBLIC VARIABLE maxval CONSTANT INT = 100;
  PUBLIC FUNCTION bound_with_maxval(i INT) RETURNS x INT AS BEGIN
    x = CASE WHEN :i > :maxval THEN :maxval ELSE :i END;
  END;
  PUBLIC PROCEDURE get_data(IN size INT, OUT result table(col1 INT)) AS BEGIN
    RESULT = SELECT TOP :size col1 FROM data_table;
  END;
END;
CREATE PROCEDURE myproc (IN inval INT) AS BEGIN
  USING mylib AS mylib;
  DECLARE var1 INT = mylib:bound_with_maxval(:inval);
  IF :var1 > mylib:maxval THEN
    SELECT 'unexpected' FROM dummy;
  ELSE
    DECLARE tv table (col1 INT);
    CALL mylib:get_data(:var1, tv);
    SELECT COUNT(*) FROM :tv;
  END IF;
END;
CALL myproc(10);  - returns the value 10
CALL myproc(150);  – returns the value 100
```

## Related Information

DROP LIBRARY Statement (SQLScript) [→](DROP-LIBRARY-Statement-SQLScript.md) ALTER LIBRARY Statement (SQLScript) [→](ALTER-LIBRARY-Statement-SQLScript.md) LIBRARIES System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARIES-System-View.md) LIBRARY_MEMBERS System View [→](../../../6-System-Views-Reference/6.01-System-Views/LIBRARY_MEMBERS-System-View.md)
