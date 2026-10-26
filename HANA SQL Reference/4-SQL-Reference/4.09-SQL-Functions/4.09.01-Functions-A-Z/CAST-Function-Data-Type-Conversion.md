# 4.9.1.33 CAST Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 121–122

Returns the value of an expression converted to a supplied data type.

## Syntax

```sql
CAST( <expression> AS <data_type>[ ( <length> ) ] )
```

## Syntax Elements

#### expression

Specifies the expression to be converted.

#### data_type

Specifies the target data type.

```sql
<data_type >::= TINYINT
 | SMALLINT
 | INTEGER
 | BIGINT
 | DECIMAL
 | SMALLDECIMAL
 | REAL
 | DOUBLE
 | ALPHANUM
 | VARCHAR
 | NVARCHAR
 | DAYDATE
 | DATE
 | TIME
 | SECONDDATE
 | TIMESTAMP
```

**length** Specifies the maximum length of the string in characters. For example, `CAST (A AS VARCHAR(10))`.

## Description

Returns the value of an expression converted to a supplied data type.

## Examples

The following example converts the value `7` to the VARCHAR value `7`:

```sql
SELECT CAST (7 AS VARCHAR) "cast" FROM DUMMY;
```

The following example converts the value `10.5` to the INTEGER value `10`, truncating the mantissa.

```sql
SELECT CAST (10.5 AS INTEGER) "cast" FROM DUMMY;
```

## Related Information

Expressions [→](../../4.06-Expressions.md) Data Type Conversion [→](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
