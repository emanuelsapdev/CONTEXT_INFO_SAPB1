# 4.9.1.218 TO_VARCHAR Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 369–370

Converts a given value to an NVARCHAR data type, with an option to format the output value. It is a synonym of the TO_NVARCHAR function.

## Syntax

```sql
TO_VARCHAR(<value> [, <format>])
```

## Syntax Elements

#### value

The input value for the function. If `<value>` is a datetime data type, and `<format>` is not specified, then the default format is applied to the output value, unless the relevant session variable (DATE_FORMAT, TIME_FORMAT, TIMESTAMP_FORMAT, or SECONDDATE_FORMAT) is set to something different.

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

Use this function to convert values to an NVARCHAR value.

## Example

The following example converts the value `2009-12-31` to a date value with the format `YYYY/MM/DD`. It then converts it again to an NVARCHAR type and returns the value `2009/12/31`

```sql
SELECT TO_VARCHAR (TO_DATE('2009-12-31'), 'YYYY/MM/DD') "to varchar" FROM DUMMY;
```

The following statements demonstrate how to use the `<string_formatting>` option to define the format of the output values:

```sql
SELECT TO_VARCHAR(1, '00.00') FROM Dummy;    --> 01.00
SELECT TO_VARCHAR(100, '00.00') FROM Dummy;          --> 100.00
SELECT TO_VARCHAR(100, '9999.00') FROM Dummy;        --> 100.00
SELECT TO_VARCHAR(100, '0000.00') FROM Dummy;        --> 0100.00
SELECT TO_VARCHAR(100, 'S0000.00') FROM Dummy;       --> +0100.00
SELECT TO_VARCHAR(-100, 'S0000.00') FROM Dummy;      --> -0100.00
SELECT TO_VARCHAR(-100, 'S0.0E0') FROM Dummy;        --> -1.0E2
SELECT TO_VARCHAR(-0.001, 'S0.0E0') FROM Dummy;      --> -1.0E-3
SELECT TO_VARCHAR(-0.001, 'S0.0E00') FROM Dummy;     --> -1.0E-03
SELECT TO_VARCHAR(1000, '9,999.00') FROM Dummy;      --> 1,000.00
SELECT TO_VARCHAR(1000, '$9,999.00') FROM Dummy;     --> $1,000.00
SELECT TO_VARCHAR(1000, '$9,999.99') FROM Dummy;     --> $1,000.
SELECT TO_VARCHAR(1,'0.00%') FROM Dummy;             --> 100.00%
SELECT TO_VARCHAR(1,'100%') FROM Dummy;              --> 1100%
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) TO_NVARCHAR Function (Data Type Conversion) [→](TO_NVARCHAR-Function-Data-Type-Conversion.md) Data Type Conversion [→](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
