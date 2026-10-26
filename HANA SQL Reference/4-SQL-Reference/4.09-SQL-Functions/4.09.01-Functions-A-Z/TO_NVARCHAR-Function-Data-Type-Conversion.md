# 4.9.1.210 TO_NVARCHAR Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 362–363

Converts a given value to an NVARCHAR data type, with an option to format the output value.

## Syntax

```sql
TO_NVARCHAR(<value> [, <format>])
```

## Syntax Elements

#### format

Specifies the desired formatting to apply to the converted value. For datetime values, use `<format>` to define the desired datetime output format (for example, `YYYY/MM/DD`. See the Datetime Data Types topic in this guide for more information on possible datetime formats.

To define other types of output formats, for example numbers with custom symbols, commas, zeros and so on, specify `<format>` using the following conventions:

- 9 - Return the number in the specified position; otherwise, return nothing.
- 0 - Return the number in the specified position; otherwise, return a zero (0).
- S - Return the sign symbol (either + or -) for the value.
- E - Divide the number into significant part and exponent part.
- % - Multiply `<value>` by 10^2 and adds a percent symbol (%) at the end.
- . (a period) - Insert a period in the specified position.
- All other characters other than the items above: Return the character in the specified position.

## Description

If the `<format>` specifier is omitted, then the conversion is performed using the date format model.

The following data types can be converted to NVARCHAR using the TO_NVARCHAR function:

- ALPHANUM, BIGINT, DATE, DECIMAL, DOUBLE, FIXED12, FIXED16, FIXED8, INTEGER, REAL, SECONDDATE, SMALLDECIMAL, SMALLINT, TIME, TIMESTAMP, TINYINT, VARBINARY, VARCHAR
- CLOB, NCLOB, TEXT (if the value is longer than the maximum length of NVARCHAR, then an exception is thrown)

## Example

The following example coverts the value `2009/12/31` to the NVARCHAR value `09-12-31`.

```sql
SELECT TO_NVARCHAR(TO_DATE('2009/12/31'), 'YY-MM-DD') "to nvarchar" FROM DUMMY;
```

The following statements demonstrate how to use the `<string_formatting>` option to define the format of the output values:

```sql
SELECT TO_NVARCHAR(1, '00.00') FROM Dummy;   --> 01.00
SELECT TO_NVARCHAR(100, '00.00') FROM Dummy;          --> 100.00
SELECT TO_NVARCHAR(100, '9999.00') FROM Dummy;        --> 100.00
SELECT TO_NVARCHAR(100, '0000.00') FROM Dummy;        --> 0100.00
SELECT TO_NVARCHAR(100, 'S0000.00') FROM Dummy;       --> +0100.00
SELECT TO_NVARCHAR(-100, 'S0000.00') FROM Dummy;      --> -0100.00
SELECT TO_NVARCHAR(-100, '000.00') FROM Dummy;        --> -100.00
SELECT TO_NVARCHAR(-100, 'S0.0E0') FROM Dummy;        --> -1.0E2
SELECT TO_NVARCHAR(-0.001, 'S0.0E0') FROM Dummy;      --> -1.0E-3
SELECT TO_NVARCHAR(-0.001, 'S0.0E00') FROM Dummy;     --> -1.0E-03
SELECT TO_NVARCHAR(1000, '9,999.00') FROM Dummy;      --> 1,000.00
SELECT TO_NVARCHAR(1000, '$9,999.00') FROM Dummy;     --> $1,000.00
SELECT TO_NVARCHAR(1000, '$9,999.99') FROM Dummy;     --> $1,000.
SELECT TO_NVARCHAR(1,'0.00%') FROM Dummy;             --> 100.00%
SELECT TO_NVARCHAR(1,'100%') FROM Dummy;              --> 1100%
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) TO_VARCHAR Function (Data Type Conversion) [→](TO_VARCHAR-Function-Data-Type-Conversion.md) Data Type Conversion [→](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
