# 6.1.55 DATA_TYPES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1464–1466

Provides information about available SQL data types.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TYPE_ID | SMALLINT | Displays the data type ID. |
| TYPE_NAME | VARCHAR(16) | Displays the data type name. |
| COLUMN_SIZE | INTEGER | Displays the maximum size, in bytes, of the data type that this system can support. |
| LITERAL_PREFIX | CHAR(1) | Displays the ODBC 2.0 SQLGetTypeInfo VARCHAR. Character or characters used to prefix a literal, for example, a single quotation mark (') for character data types or 0x for binary data types; NULL is returned for data types where a literal prefix is not applicable. |
| LITERAL_SUFFIX | CHAR(1) | Displays the ODBC 2.0 SQLGetTypeInfo VARCHAR. Character or characters used to terminate a literal, for example, a single quotation mark (') for character data types; NULL is returned for data types where a literal suffix is not applicable. |
| CREATE_PARAMS | VARCHAR(16) | Displays the ODBC 2.0 SQLGetTypeInfo VARCHAR. A list of keywords, separated by commas, corresponding to each parameter that the application may specify in parentheses when using the name that is returned in the TYPE_NAME field. |
| NULLABLE | TINYINT | Displays whether the data type can accept NULL or not. |
| CASE_SENSITIVE | TINYINT | Displays the ODBC 2.0 SQLGetTypeInfo SMALLINT. Whether a character data type is case-sensitive in collations and comparisons. |
| SEARCHABLE | TINYINT | Displays the how the data type can be used in the WHERE clause. |
| UNSIGNED_ATTRIBUTE | TINYINT | Displays whether the attribute is signed or unsigned. |
| FIXED_PREC_SCALE | TINYINT | Displays the whether the data type has predefined fixed precision and scale (ODBC). |
| AUTO_UNIQUE_VALUE | TINYINT | Displays whether the data type is auto incrementing (ODBC). |
| LOCAL_TYPE_NAME | VARCHAR(16) | Displays the ODBC 2.0 SQLGetTypeInfo VARCHAR. Localized version of the data source-dependent name of the data type. |
| MINIMUM_SCALE | SMALLINT | Displays the ODBC 2.0 SQLGetTypeInfo SMALLINT. The minimum scale of the data type on the data source. |
| MAXIMUM_SCALE | SMALLINT | Displays the ODBC 2.0 SQLGetTypeInfo SMALLINT. The maximum scale of the data type on the data source. |
| SQL_DATA_TYPE | SMALLINT | Displays the ODBC 3.0 SQLGetTypeInfo SMALLINT. The value of the SQL data type as it appears in the SQL_DESC_TYPE field of the descriptor. This column is the same as the DA TATYPE column, except for interval and DATETIME data types. |
| SQL_DATETIME_SUB | SMALLINT | Displays the ODBC 3.0 SQLGetTypeInfo SMALLINT. When the value of SQL_DATATYPE is SQL_DATETIME or SQL_INTERVAL, this column contains the DA TETIME/interval subcode. |
| NUM_PREC_RADIX | INTEGER | Displays the ODBC 3.0 SQLGetTypeInfo INTEGER. In case of an approximate numeric data type, value is 2 to indicate that COLUMN_SIZE specifies the number of bits. For exact numeric data types value 10 indicates that COLUMN_SIZE specifies the number of decimal digits. |
| INTERVAL_PRECISION | SMALLINT | Displays the ODBC 3.0 SQLGetTypeInfo SMALLINT. If the data type is an interval data type, then this column contains the value of the interval leading precision. Otherwise, this column is NULL. |

## Related Information

Data Types [→](../../4-SQL-Reference/4.03-Data-Types/README.md) Data Type Conversion Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.04-Data-Type-Conversion-Functions.md)
