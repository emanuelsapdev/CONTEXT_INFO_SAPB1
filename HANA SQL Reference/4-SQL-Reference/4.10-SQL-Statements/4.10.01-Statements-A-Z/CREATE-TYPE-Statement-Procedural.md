# 4.10.1.70 CREATE TYPE Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 842–844

Creates a userdefined type

## Syntax

```sql
CREATE TYPE <type_name>
   AS TABLE (<column_definition>[{,<column_definition>}...]) [ SQLSCRIPT SEARCH
KEY( <column_name> [,…] ) ]
```

## Syntax Elements

#### type_name

Identifies the table type to be created and, optionally, in which schema the creation should take place.

```sql
<type_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <unicode_name>
```

#### column_definition

Defines a table column.

```sql
<column_definition> ::= <column_name> <data_type> [<column_store_data_type>]
```

##### column_name

Specifies the table column name.

```sql
<column_name> ::= <identifier>
```

##### data_type

Specifies the data type for the column.

```sql
<data_type> ::=
 DATE | TIME | SECONDDATE | TIMESTAMP | TINYINT
 | SMALLINT | INTEGER | BIGINT | SMALLDECIMAL | DECIMAL
 | REAL | DOUBLE | VARCHAR | NVARCHAR | ALPHANUM
 | VARBINARY | BLOB | CLOB | NCLOBSHORTTEXT
 | TEXT | BINTEXT
<column_store_data_type> ::=
 CS_ALPHANUM | CS_INT | CS_FIXED | CS_FLOAT | CS_DOUBLE
 | CS_DECIMAL_FLOAT | CS_FIXED(p-s, s) | CS_SDFLOAT | CS_STRING | CS_DATE
 | CS_TIME | CS_FIXEDSTRING | CS_RAW | CS_DAYDATE | CS_SECONDTIME
 | CS_LONGDATE | CS_SECONDDATE
```

#### SQLSCRIPT SEARCH KEY clause

Specifies sorting instructions for the table. For use with SQLScript procedures. See the SAP HANA SQLScript Guide for more information.

## Description

Use a userdefined type in the CREATE PROCEDURE and CREATE FUNCTION commands.

The syntax for defining table types follows the SQL syntax for defining new types. The table type is specified using a list of attribute names and primitive data types. For each table type, attributes must have unique names.

## Example

Create a table type called tt_publishers.

```sql
CREATE TYPE tt_publishers AS TABLE (
   publisher INTEGER,
   name VARCHAR(50),
   price DECIMAL,
   cnt INTEGER);
```

## Related Information

CREATE PROCEDURE Statement (Procedural) [→](CREATE-PROCEDURE-Statement-Procedural.md) Data Types [→](../../4.03-Data-Types/README.md) CREATE FUNCTION Statement (Procedural) [→](CREATE-FUNCTION-Statement-Procedural.md)
