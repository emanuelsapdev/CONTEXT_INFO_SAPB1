# 4.9.1.101 JSON_TABLE Function (JSON)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 213–221

Queries a JSON text and presents it as a relational table.

## Syntax

```sql
JSON_TABLE(
 <JSON_API_common_syntax>
 <JSON_table_columns_clause>
 [ <JSON_table_error_behavior> ON ERROR ]
 )
```

## Syntax Elements

#### JSON_API_common_syntax

Specifies a JSON context item and a path to the context item, using common syntax for the JSON API.

```sql
<JSON_API_common_syntax> ::= <JSON_context_item>, <JSON_path_specification>
```

##### JSON_context_item

Specifies the JSON document to operate on, such as a table column, string, or collection.

##### JSON_path_specification

Specifies the path to `<JSON_context_item>`.

```sql
<JSON_path_specification> ::= <JSON_path_mode> <JSON_path_wff>
<JSON_path_mode> ::= STRICT | LAX
```

If a structural error occurs within a JSON filter expression and `<JSON_path_mode>` is set to STRICT, then the error handling of a JSON filter expression applies. Otherwise, a structural error is an unhandled error.

When the path is set to LAX, one of the following options occurs:

- If an operation requires an SQL/JSON array but the operand is not an SQL/JSON array, then the operand is wrapped in an SQL/JSON array prior to performing the operation.
- If an operation requires something other than an SQL/JSON array, but the operand is an SQL/ JSON array, then the operand is unwrapped by converting its elements into an SQL/JSON sequence prior to performing the operation.

Array indexes start from 0, rather than 1 (the SQL standard).

If there is still a structural error after applying these resolutions, then the result is an empty SQL/JSON sequence.

`<JSON_path_wff>` indicates an actual JSON path (for example, `'$.item1'`). `<JSON_path_specification>` does not use double quotes.

#### JSON_table_columns_clause

Specifies the columns that are created.

```sql
<JSON_table_columns_clause> ::=
 COLUMNS ( <JSON_table_column_definition> [,... ] )

<JSON_table_column_definition> ::=
<JSON_table_ordinality_column_definition>
 | <JSON_table_regular_column_definition>
 | <JSON_table_formatted_column_definition>
 | <JSON_table_nested_columns>
```

##### JSON_table_column_definition

Defines the columns generated.

##### JSON_table_ordinality_column_definition

Defines an ordinality column. An ordinality column is similar to a column defined using the ROW_NUMBER window function.

```sql
<JSON_table_ordinality_column_definition> ::= <column_name> FOR ORDINALITY
```

##### JSON_table_regular_column_definition

Defines the regular columns. Each result (row) of a regular JSON table column is equivalent to a JSON_VALUE function result.

```sql
<JSON_table_regular_column_definition> ::= <column_name> <data_type>
 PATH <JSON_table_column_path_specification>
 [ JSON <table_column_empty_behavior> ON EMPTY ]
 [ <JSON_table_column_error_behavior> ON ERROR ]
<JSON_table_column_path_specification> ::= <JSON_path_specification>

<JSON_table_column_empty_behavior> ::=
ERROR
 | NULL
 | DEFAULT <value_expression>

<JSON_table_column_error_behavior> ::=
ERROR
 | NULL
 | DEFAULT <value_expression>
```

###### column_name

Specifies the name of the column.

###### data_type

Specifies the data type.

```sql
<data_type> ::=
BIGINT
 | DATE
 | DECIMAL
 | DOUBLE
 | INT
 | NVARCHAR (<int_const>)
 | SECONDDATE
 | SMALLDECIMAL
 | TIME
 | TIMESTAMP
 | VARCHAR (<int_const>)
```

###### JSON_table_column_path_specification

Specifies the JSON path that specifies which JSON value the JSON context item is extracted from.

###### table_column_empty_behavior ON EMPTY

Specifies the behavior of the function when the created column is empty. The default is DEFAULT `<value_expression>` ON EMPTY.

ERROR ON EMPTY returns an error when the created column is empty. NULL ON EMPTY returns a NULL when the created column is empty. DEFAULT `<value_expression>` ON EMPTY returns `<value_expression>` when the created column is empty.

###### JSON_table_column_error_behavior ON ERROR

Specifies the behavior of the function when there is an error during column creation. The default is DEFAULT `<value_expression>` ON ERROR.

ERROR ON ERROR results in an error being thrown if the function result includes an error. NULL ON ERROR returns a NULL if the function result includes an error. DEFAULT `<value_expression>` ON ERROR returns `<value_expression>` if the function result includes an error.

##### JSON_table_formatted_column_definition

Specifies the column definition for formatted columns where the records in the column are formatted in JSON syntax. Each result (row) of a regular JSON table column is equivalent to a JSON_QUERY function result.

```sql
<JSON_table_formatted_column_definition> ::=
 <column_name> <data_type>
 FORMAT <JSON_representation>
 PATH <JSON_table_column_path_specification>
 [ <JSON_table_formatted_column_wrapper_behavior> WRAPPER ]
 [ <JSON_table_formatted_column_empty_behavior> ON EMPTY ]
 [ <JSON_table_formatted_column_error_behavior> ON ERROR ]
```

##### column_name

Specifies the name of the column.

##### data_type

Specifies the data type to be set as the return type of the function. Supported data types for formatted columns are VARCHAR(`<n>`) and NVARCHAR(`<n>`).

##### JSON_representation

Specifies the JSON encoding to use.

```sql
<JSON_representation> ::=
JSON
 | JSON ENCODING { UTF8 }
 | JSON ENCODING { UTF16 }
 | JSON ENCODING { UTF32 }
```

##### JSON_table_column_path_specification

Specifies the JSON path that specifies which JSON value the JSON context item is extracted from.

##### JSON_table_formatted_column_wrapper_behavior WRAPPER

Specifies the wrapper behavior of the formatted column.

```sql
<JSON_table_formatted_column_wrapper_behavior> ::=
WITHOUT [ ARRAY ]
 | WITH [ CONDITIONAL | UNCONDITIONAL ] [ ARRAY ]
```

When WITHOUT [ ARRAY ] WRAPPER is specified, the formatted column is not represented as a JSON array. When WITH [ CONDITIONAL | UNCONDITIONAL ] [ ARRAY ] WRAPPER is specified, the formatted column is set with a conditional/unconditional array. With a conditional array, the result is formatted as a JSON array if the result is neither a JSON array nor a JSON object. With an unconditional array, the result is formatted as a JSON array if the result is not a JSON object. The difference between unconditional and conditional wrapper is that unconditional wrapper wraps the result as a JSON array once more when the result is a JSON array.

##### JSON_table_formatted_column_empty_behavior ON EMPTY

Specifies the JSON behavior if the related data is not in the context item.

```sql
<JSON_table_formatted_column_empty_behavior> ::=
ERROR
 | NULL
 | EMPTY ARRAY
 | EMPTY OBJECT
```

ERROR ON EMPTY returns an error if the related data is not in the context item. NULL ON EMPTY returns a NULL if the related data is not in the context item. EMPTY ARRAY ON EMPTY returns an empty array if the related data is not in the context item. EMPTY OBJECT ON EMPTY returns an empty JSON object if the related data is not in the context item.

##### JSON_table_formatted_column_error_behavior ON ERROR

Specifies the behavior when the formatted column throws an error.

```sql
<JSON_table_formatted_column_error_behavior> ::=
ERROR
 | NULL
 | EMPTY ARRAY
 | EMPTY OBJECT
```

ERROR ON ERROR returns an error if the function returns no result. NULL ON ERROR returns a NULL if the function returns no result. EMPTY ARRAY ON ERROR returns an empty array if the result of the formatted column is empty. EMPTY OBJECT ON ERROR returns an empty JSON object if the result of the formatted column is empty.

##### JSON_table_nested_columns

Defines nested columns.

```sql
<JSON_table_nested_columns> ::= NESTED [ PATH ]
<JSON_table_nested_path_specification>
 <JSON_table_columns_clause>
<JSON_table_nested_path_specification> ::= <JSON_path_specification>
```

- `<JSON_table_columns_clause>`: Specifies the columns that are created with the function.
- `<JSON_path_specification>`: The JSON path which specifies which JSON value from the JSON context item is extracted.

#### JSON_table_error_behavior

Specifies the behavior of the function when an error occurs. The default behavior is EMPTY ON ERROR.

```sql
<JSON_table_error_behavior> ::= { ERROR | EMPTY }
```

##### ERROR

If the function result includes an error, then the error is returned.

##### EMPTY

If the function result includes an error, then it returns an empty result.

## Description

Queries a JSON text and presents it as a relational table.

The following tokens are supported in `<JSON_API_common_syntax>`:

| **Token** | **Description** | **Example** |
| --- | --- | --- |
| $ | The current context item. | `'$'` |
| . | The member of an object. | `'$.item.description'` |
| [ | The array index specifier (open). |   |
| ] | The array index specifier (closed). | `'$[1]' '$.item.list[1]'` |
| to | The array index range. | `'$[3 to 5]' = '$[3,4,5]'` |
| \* | The wild card. | `'$.*.description' '$.item.list[*]'` |

## Example

The following examples use the table created below:

```sql
CREATE ROW TABLE T1 (A INT, B NVARCHAR(5000));
INSERT INTO T1 VALUES (1, '
{
        "PONumber": 1,
        "Reference": "BSMITH-74635645",
        "Requestor": "Barb Smith",
        "User": "BSMITH",
        "CostCenter": "A50",
        "ShippingInstructions":
               {
                       "name": "Barb Smith",
                       "Address":
                               {
                                      "street": "100 Fairchild Ave",
                                      "city": "San Diego",
                                       "state": "CA",
                                      "zipCode": 23345,
                                      "country": "USA"
                               },
                       "Phone": [{"type": "Office", "number": "519-555-6310"}]
               },
        "SpecialInstructions": "Surface Mail",
        "LineItems": [
               {"ItemNumber": 1, "Part": {"Description": "Basic Kit",
"UnitPrice": 19.95, "UPCCode": 73649587162}, "Quantity": 7},
               {"ItemNumber": 2, "Part": {"Description": "Base Kit 2",
"UnitPrice": 29.95, "UPCCode": 83600229374}, "Quantity": 1},
               {"ItemNumber": 3, "Part": {"Description": "Professional",
"UnitPrice": 39.95, "UPCCode": 33298003521}, "Quantity": 8},
               {"ItemNumber": 4, "Part": {"Description": "Enterprise",
"UnitPrice": 49.95, "UPCCode": 91827739856}, "Quantity": 8},
               {"ItemNumber": 5, "Part": {"Description": "Unlimited",
"UnitPrice": 59.95, "UPCCode": 22983303876}, "Quantity": 8}
        ]
}
');
```

The following example selects from an ordinality column and a regular column:

```sql
SELECT JT.*
FROM JSON_TABLE(T1.B, '$.LineItems[*]'
COLUMNS
    (
        RN FOR ORDINALITY,
        ITEM_NUMBER INT PATH '$.ItemNumber',
        UPC_CODE BIGINT PATH '$.Part.UPCCode'
    )
) AS JT;
```

| **RN** | **ITEM_NUMBER** | **UPC_CODE** |
| --- | --- | --- |
| 1 | 1 | 73649587162 |
| 2 | 2 | 83600229374 |
| 3 | 3 | 33298003521 |
| 4 | 4 | 91827739856 |
| 5 | 5 | 22983303876 |

The following example selects from a formatted column:

```sql
SELECT *
FROM JSON_TABLE(T1.B, '$.ShippingInstructions'
COLUMNS
    (
        PHONE VARCHAR(50) FORMAT JSON PATH '$.Phone'
    )
) AS JT;
```

| **PHONE** |
| --- |
| [{"number":"5195556310","type":"Office"}] |

The following example selects from a nested column:

```sql
SELECT *
FROM JSON_TABLE(T1.B, '$.ShippingInstructions'
COLUMNS
    (
        NESTED PATH '$.Address'
        COLUMNS
        (
            STREET NVARCHAR(50) PATH '$.street',
            CITY NVARCHAR(50) PATH '$.city'
        )
    )
) AS JT;
```

| **STREET** | **CITY** |
| --- | --- |
| 100 Fairchild Ave | San Diego |

The following example selects from an ordinality column with nested columns:

```sql
SELECT *
FROM JSON_TABLE(T1.B, '$'
    COLUMNS
    (
        RN FOR ORDINALITY,
        USER_NAME NVARCHAR(20) PATH '$.User',
        NESTED PATH '$.LineItems[1,2]'
        COLUMNS
        (
            ORDER_NUMBER FOR ORDINALITY,
            ITEM_NUMBER INT PATH '$.ItemNumber',
            QUANTITY INT PATH '$.Quantity'
        )
    )
) AS JT;
```

| **RN** | **USER_NAME** | **ORDER_NUMBER** | **ITEM_NUMBER** | **QUANTITY** |
| --- | --- | --- | --- | --- |
| 1 | BSMITH | 1 | 2 | 1 |
| 1 | BSMITH | 2 | 3 | 8 |

The following example demonstrates the difference when specifying CONDITIONAL ARRAY WRAPPER versus UNCONDITIONAL ARRAY WRAPPER when returning a JSON array:

```sql
CREATE ROW TABLE r1 ( a INT, b NVARCHAR(5000));
INSERT INTO r1 VALUES (1, '{"menu": {"header": "SVG Viewer","items": [{"id":
"Open"},{"id": "OpenNew", "label": "Open New"},null,{"id": "ZoomIn", "label":
"Zoom In"}]}}');
```

| **SELECT statement** | **Value returned** |
| --- | --- |
| `SELECT JSON_QUERY(B, '$.menu.items'WITH UNCONDITIONAL ARRAY WRAPPER)FROM r1 WITH HINT(IGNORE_PLAN_CACHE);` | `[[{"id":"Open"}, {"id":"OpenNew","label":"OpenNew"},null, {"id":"ZoomIn","label":"Zoom In"}]]` |
| `SELECT JSON_QUERY(B, '$.menu.items'WITH CONDITIONAL ARRAY WRAPPER)FROM r1;` | `[{"id":"Open"}, {"id":"OpenNew","label":"OpenNew"},null, {"id":"ZoomIn","label":"Zoom In"}]` |

The following example demonstrates an example of ERROR ON ERROR, which results in an error stating that the data for '$.User' cannot be parsed to an integer data type.

```sql
SELECT *
FROM JSON_TABLE(T1.B, '$'
    COLUMNS
    (
        RN FOR ORDINALITY,
        USER_NAME INT PATH '$.User' ERROR ON ERROR
    )
ERROR ON ERROR
) AS JT;
```

The following example demonstrates an example of EMPTY ON ERROR, which returns an empty result instead of throwing an error because the default behavior of JSON_table_error_behavior is EMPTY ON ERROR.

```sql
SELECT *
FROM JSON_TABLE(T1.B, '$'
    COLUMNS
    (
        RN FOR ORDINALITY,
        USER_NAME INT PATH '$.User' ERROR ON ERROR
    )
) AS JT;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
