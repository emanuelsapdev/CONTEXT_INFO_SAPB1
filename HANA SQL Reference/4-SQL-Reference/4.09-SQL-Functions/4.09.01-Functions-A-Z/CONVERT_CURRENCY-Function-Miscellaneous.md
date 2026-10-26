# 4.9.1.39 CONVERT_CURRENCY Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 127–137

Calculates values in different currencies.

## Syntax

```sql
CONVERT_CURRENCY( <named_parameter_value>[{, <named_parameter_value>}...])
```

## Syntax Elements

#### named_parameter_value

Specifies the parameters for the conversion.

```sql
<named_parameter_value> ::=
"<field_reference_parameter>" => <expression>
 | "<const_string_parameter>" => <const_string>
```

```sql
<field_reference_parameter> ::=
 AMOUNT
 | SOURCE_UNIT
 | TARGET_UNIT
 | REFERENCE_DATE
 | CLIENT
```

You use field reference parameters to refer to table columns for the conversion.

| **Field Reference ParameterName** | **Description** | **Mandatory** | **Default Value** |
| --- | --- | --- | --- |
| AMOUNT | The column identifier containing the values to be converted. | Yes | None |
| CLIENT | Defines a three character string that is used to separate tenants within ERP system tables. This is used in the conversion tables to select the correct rows for each user. A column identifier is also accepted using double quotations.<br>This parameter is mandatory, as the CLIENT session context variable is not used by this command. | Yes | None |
| SOURCE_UNIT | The column identifier describing the input unit. A constant string is also accepted using single quotations. | Yes | None |
| TARGET_UNIT | The column identifier describing the target unit. A constant string is also accepted using single quotations. | Yes | None |
| REFERENCE_DATE | The column identifier describing the currency reference date. A constant string is also accepted using single quotations. | Yes | None |

```sql
<const_string_parameter> ::=
 SCHEMA
| DATABASE
| CONVERSION_TYPE
| LOOKUP
| ERROR_HANDLING
| ACCURACY
| DATE_FORMAT
| STEPS
| CONFIGURATION_TABLE
| PRECISIONS_TABLE
| NOTATIONS_TABLE
| RATES_TABLE
| PREFACTORS_TABLE
```

`<const_string_parameter>` defines constant parameter values used in the conversion.

| **Constant Parameter Name** | **Description** | **Mandatory** | **Default Value** |
| --- | --- | --- | --- |
| SCHEMA | Defines the schema that contains the conversion tables used for the conversion. | Yes | None |
| DATABASE | Defines the tenant where the conversion tables are located (for example the TCUR\* tables of the ERP currency conversion). If not specified, the conversion uses the current database. | No | None |
| METHOD | Possible values: ERP, Banking | No | ERP |
| BID_ASK_TYPE | Possible values: bid, ask, mid | No | (empty string) |
| MARKET_DATA_AREA | Defines the market data area as stored in the tables. This is mandatory for banking currency conversion. | No | (empty_string) |
| SYSTEM_TIME | Defines the system time stamp for time travel functionality. | No | Current system timestamp in GMT |
| CONVERSION_TYPE | Defines the conversion type as stored in the conversion tables. The conversion types available in your system vary according to the setup of your ERP system. In general, these are either M or EURX. Contact your system administrator for the details of your specific table configuration. | No | M |
| LOOKUP | The type of lookup to be performed. Possible values:<br>**Regular**<br>A regular conversion is performed. **Reverse**<br>Performs a reverse conversion with the in put units swapped. | No | Regular |
| ERROR_HANDLING | Defines how the system handles a situation where a row could not be converted. Possible values:<br>**fail on error**<br>The conversion fails with an error. **set to null**<br>The output from the row that caused the error is set to NULL. **keep unconverted**<br>The input value is re turned. | No | Fail on error |
| ACCURACY | Defines the rounding behavior of the system. Possible values:<br>**compatibility**<br>Mimics ERP behavior by rounding the result. **highest**<br>Keeps as many digits as possible in the result. | No | Compatibility |
| DATE_FORMAT | Defines the format in which the reference date is pre sented. Possible values<br>**auto detect**<br>Attempt automatic detection of the date format. **normal**<br>Date is provided in a regular format **inverted**<br>Date is provided in inverted SAP legacy format. | No | Auto detect |
| STEPS | Defines the steps that should be included in the conversion process. You provide a comma delimited list of the steps to be included, and the order of the steps is irrelevant.<br>**shift**<br>Enables a decimal shift according to the source currency selected. For example, if the source currency has 0 valid digits according to PRECISIONS_TABLE, each value needs to be multiplied by 100 be cause in SAP ERP systems, values are stored using two digits. This has to be done to convert ERP values to their correct numerical representation. **convert**<br>Triggers the actual con version from the source to the target currency. **round**<br>Rounds the converted value to the number of digits of the target currency. Use this step carefully if subsequent aggregations take place on the number, as rounding errors could accumulate. **shift_back**<br>While shift changes the decimals from two to the configured precision of the source currency, shift_back | No | shift, convert |
|   | changes them back to two, but from the target currency. If error handling is set to `keep` `unconverted` the output currency might be the source instead of the target currency. In case of an error, the rounding and the shift_back are done with respect to the source currency and the conversion is dropped. This renders all steps redundant, and yields the input value again. |   |   |
| CONFIGURATION_TABLE | The table identifier of the conversion type configuration. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | TCURV |
| PRECISIONS_TABLE | The table identifier of the precision table. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | TCURX |
| NOTATIONS_TABLE | The table identifier of the table that stores notations. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | TCURN |

Additional Parameters and Defaults for Method ERP

| **Constant Parameter Name** | **Description** | **Mandatory** | **Default Value** |
| --- | --- | --- | --- |
| CONFIGURATION_TABLE | The table identifier of the conversion type configuration. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No TCURV | TCURV |
| RATES_TABLE | The table identifier of the conversion rates table. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No TCURR | TCURR |
| PREFACTORS_TABLE | The table identifier of the pre-factors table. If the table resides in a different ten ant, provide a fully qualified name for the table or use the DATABASE parameter. | No TCURF | TCURF |

Additional Parameters and Defaults for Method Banking

| **Constant Parameter Name** | **Description** | **Mandatory** | **Default Value** |
| --- | --- | --- | --- |
| MARKET_DATA_AREA | Defines the market data area as stored in the tables. This is mandatory for banking currency conversion. | Yes | (empty_string) |
| SYSTEM_TIME | Defines the system time stamp for time travel functionality. T | No | Current system timestamp in GM |
| CONFIGURATION_TABLE | The table identifier of the conversion type configuration. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | /BA1/TF4_FXRTTYP |
| RATES_TABLE | The table identifier of the conversion rates table. If the table resides in a different tenant, provide a fully qualified name for the table or use the DATABASE parameter. | No | /BA1/F4_FXRATES |
| PREFACTORS_TABLE | The table identifier of the pre-factors table. If the table resides in a different ten ant, provide a fully qualified name for the table or use the DATABASE parameter. | No | /BA1/TF4_FXCVFCT |

## Description

The CONVERT_CURRENCY function provides an efficient method to calculate values in different currencies. CONVERT_CURRENCY function is an SQL representation of the SQLScript built-in function CE_CONVERSION, and internally uses CE_CONVERSION for computation.

The HANA currency conversion provides two different methods. The ERP method, which stores the cross rates in table TCURR with 9 digits, and the Banking method, which stores the rates in table /BA1/F4_FXRATES with 15 digits. In both cases, you can alternatively use tables that store the cross rates in a data type with more digits, such as DECIMAL(25,21).

To use the CONVERT_CURRENCY function, the currency conversion tables TCURV, TCURX, TCURN, TCURR, and TCURF must be available in the SAP HANA database for method ERP. Alternatively, the currency conversion tables /BA1/TF4_FXRTTYP , TCURX, TCURN, /BA1/F4_FXRATES, and /BA1/TF4_FXCVFCT must be available for method Banking. If you have stored the rates information in tables with a different layout, you can use views to map the table content to the format used in the ERP or Banking tables.

The CONVERT_CURRENCY function does not support some conversion functions. It only supports columns XINVR, BWAER, XBWRL and XEURO from customizing table TCURV. An error message appears when one of the unsupported fields BKUZU, GKUZU or XBWRL are maintained in table TCURV. Refer to SAP Note 2792149 - Currency/unit conversion error: conversion type '\<conversion type>' has unsupported 'BKUZU' or 'GKUZU' type set.

## Example

Create a table and populate it with two example currency amounts.

```sql
CREATE ROW TABLE sample_input (price DECIMAL(15,2),
                             source_unit VARCHAR(4),
                             target_unit VARCHAR(4),
                             ref_date VARCHAR(10)
                             );
 INSERT INTO sample_input VALUES (1.0, 'SRC', 'TRG', '2011-01-01');
 INSERT INTO sample_input VALUES (1.0, 'SRC', 'TRG', '2011-02-01');
```

Convert the values in the currency table using conversion tables contained in the SYSTEM schema in tenant NDB.

```sql
SELECT CONVERT_CURRENCY(amount=>price,
"SOURCE_UNIT" =>source_unit,
"SCHEMA" => 'SYSTEM',
"DATABASE" => 'NDB',
"TARGET_UNIT" => target_unit,
"REFERENCE_DATE" =>'2013-09-23',
"ERROR_HANDLING"=>'set to null',
"CLIENT" => '000') as converted
FROM sample_input;
```

Convert the values by using the `Banking method`.

```sql
SELECT *, CONVERT_CURRENCY(method=>'Banking', -- new
                           market_data_area=>'S000’,  -- new (and mandatory for
Banking)
                           amount=>ext_limit,
                           source_unit =>ext_limit_curr,
                           schema => 'SAPCOB',
                           target_unit=> 'EUR',
                           reference_date => business_day,
                           error_handling=> 'set to null',
                           client => '150') as converted from v_fx_input
```

Convert the values by using the `Banking method` and `system_time`.

```sql
SELECT *, CONVERT_CURRENCY(method=>'Banking', -- new
                           market_data_area=>'S000', -- mandatory (for Banking)
                           bid_ask_type=>'MID',   -- optional
                           system_time=>to_timestamp('2011-05-11
12:59.999','YYYY-MM-DD HH:SS.FF3') -- optional
                           amount=>ext_limit,
                           source_unit =>ext_limit_curr,
                           schema => 'SAPCOB',
                           target_unit=> 'EUR',
                           reference_date => business_day,
                           error_handling=> 'set to null',
                           client => '150') as converted from v_fx_input
```

## Related Information

SAP Note 2792149 Expressions [→](../../4.06-Expressions.md) Currency Translation Associate Measures with Currency
