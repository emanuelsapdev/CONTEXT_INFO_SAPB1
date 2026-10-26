# 4.9.1.40 CONVERT_UNIT Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 137–140

Converts the specified source units to specified target units.

## Syntax

```sql
CONVERT_UNIT( <named_parameter_value>, ... )
```

## Syntax Elements

#### named_parameter_value

Named value of field reference, or constant string, parameters.

```sql
<named_parameter_value> := "<field_reference_parameter>" =>
 <expression> | "<const_string_parameter>" => <const_string>
```

```sql
<field_reference_parameter> ::=
 QUANTITY
 | SOURCE_UNIT
 | TARGET_UNIT
 | CLIENT
```

```sql
<const_string_parameter> ::=
 SCHEMA
 | DATABASE
 | ERROR_HANDLING
 | RATES_TABLE
 | DIMENSION_TABLE
```

| **Field Reference ParameterName** | **Description** | **Mandatory** | **Default Value** |
| --- | --- | --- | --- |
| QUANTITY | The column to be converted. | Yes | None |
| SOURCE_UNIT | The column identifier describing the input unit. A constant string is also accepted using single quotations. | Yes | None |
| TARGET_UNIT | The column identifier describing the target unit. A constant string is also accepted using single quotations. | Yes | None |
| CLIENT | Defines a three character string that is used to separate tenants within ERP system tables. This is used in the conversion tables to select the correct rows for each user. A column identifier is also accepted using double quotations. This parameter is mandatory, as the CLIENT session context variable is not used by this command. | Yes | None |
| SCHEMA | Defines the schema that contains the conversion tables used for the conversion. | Yes | None |
| DATABASE | Defines the tenant where the conversion tables are located. If not specified, the conversion uses the current database. | No | None |
| ERROR_HANDLING | Defines how the system handles a situation where a row cannot be converted.<br>**Value Purpose**<br>fail on error The conversion fails with an error.<br>set to null The output from the row that caused the error is set to NULL.<br>keep uncon The input verted value is re turned. | No | fail on error |
| RATES_TABLE | Defines a table that stores the conversion rates. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | T006 |
| DIMENSION_TABLE | Defines a table that stores the conversion dimensions. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | no | T006D |

## Description

The CONVERT_UNIT function is an SQL representation of the SQL Script built-in function CE_CONVERSION, and internally uses CE_CONVERSION for computation.

To use the CONVERT_UNIT function, the unit conversion tables T006 and T006D must be available in the SAP HANA database. For other SAP HANA databases, replicate the T006 and T006D tables from an SAP ERP system.

## Example

```sql
CREATE ROW TABLE sample_input (
 quant DECIMAL(15,2),
 source_unit VARCHAR(4),
 target_unit VARCHAR(4)
 );
 INSERT INTO sample_input VALUES (1.0, 'SRC', 'TRG');
 INSERT INTO sample_input VALUES (1.0, 'SRC', 'TRG');

 SELECT CONVERT_UNIT("QUANTITY"=>quant
 , "SOURCE_UNIT" =>source_unit
 , "SCHEMA" => 'SYSTEM'
 , "DATABASE" => 'NDB'
 , "TARGET_UNIT" => target_unit
 , "ERROR_HANDLING"=>'set to null'
 , "CLIENT" => '000') AS converted
 FROM sample_input;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
