# 4.3 Data Types

> [↑ 4 SQL Reference](../README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 31–33

A data type defines the characteristics of a data value. A special value of NULL is included in every data type to indicate the absence of a value.

## Classification of Data Types

In the SAP HANA database, each data type can be classified by its characteristics as follows:

Classification of data types

| **Classification** | **Data Type** |
| --- | --- |
| Datetime types | DATE, TIME, SECONDDATE, TIMESTAMP |
| Numeric types | TINYINT, SMALLINT, INTEGER, BIGINT, SMALLDECIMAL, DECIMAL, REAL, DOUBLE |
| Boolean type | BOOLEAN |
| Character string types | VARCHAR, NVARCHAR, ALPHANUM, SHORTTEXT |
| Binary types | VARBINARY |
| Large Object types | BLOB, CLOB, NCLOB, TEXT |
| Multi-valued types | ARRAY |
| Spatial types | ST_GEOMETRY, ST_POINT |

## Typed Constants

A constant is a symbol that represents a specific fixed data value.

#### Character string constant

A character string constant is enclosed in single quotation marks, for example: 'Brian' or '100'.

Unicode strings have a similar format to character strings but are preceded by an N identifier (N stands for National Language in the SQL-92 standard).

```sql
SELECT 'Brian' "character string 1", '100' "character string 2", N'abc'
"unicode string" FROM DUMMY;
```

The example above returns the following results:

| **character String 1** | **character String 2** | **unicode string** |
| --- | --- | --- |
| Brian | 100 | abc |

#### Number constant

A number constant is represented by a string of numbers that are not enclosed in quotation marks. Numbers may contain a decimal point or a scientific notation. For example, 123, 123.4, or 1.234e2.

A hexadecimal number constant is a string of hexadecimal numbers and has the prefix 0x. For example, 0x0abc.

```sql
SELECT 123 "integer", 123.4 "decimal1", 1.234e2 "decimal2", 0x0abc
"hexadecimal" FROM DUMMY;
```

The example above returns the following results:

| **integer** | **decimal1** | **decimal2** | **hexadecimal** |
| --- | --- | --- | --- |
| 123 | 123.4 | 123.4 | 2,748 |

#### Binary string constant

A binary string has the prefix X and is a string of hexadecimal numbers that are enclosed in quotation marks. For example, X'00abcd' or x'dcba00'.

```sql
SELECT X'00abcd' "binary string 1", x'dcba00' "binary string 2" FROM DUMMY;
```

The example above returns the following results:

| **binary string 1** | **binary string 2** |
| --- | --- |
| 00ABCD | DCBA00 |

#### Date/Time/Timestamp constant

Date, Time, and Timestamp each have the following prefixes:

- date'2010-01-01'
- time'11:00:00.001'
- timestamp'2011-12-31 23:59:59'

```sql
SELECT date'2010-01-01' "date", time'11:00:00.001' "time",
timestamp'2011-12-31 23:59:59' "timestamp" FROM DUMMY;
```

The example above returns the following results:

| **date** | **time** | **timestamp** |
| --- | --- | --- |
| Jan 1, 2010 | 11:00:00 AM | Dec 31, 2011 11:59:59.0 PM |

## Contenido de esta sección

- [4.3.1 Binary Data Types](4.03.01-Binary-Data-Types.md)
- [4.3.2 Boolean Data Type](4.03.02-Boolean-Data-Type.md)
- [4.3.3 Character String Data Types](4.03.03-Character-String-Data-Types.md)
- [4.3.4 Data Type Conversion](4.03.04-Data-Type-Conversion.md)
- [4.3.5 Datetime Data Types](4.03.05-Datetime-Data-Types.md)
- [4.3.6 Large Object (LOB) Data Types](4.03.06-Large-Object-LOB-Data-Types.md)
- [4.3.7 Multi-valued Data Types](4.03.07-Multi-valued-Data-Types.md)
- [4.3.8 Numeric Data Types](4.03.08-Numeric-Data-Types.md)
- [4.3.9 Spatial Data Types](4.03.09-Spatial-Data-Types.md)
