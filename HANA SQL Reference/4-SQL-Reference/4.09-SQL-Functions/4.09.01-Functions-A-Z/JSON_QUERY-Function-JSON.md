# 4.9.1.100 JSON_QUERY Function (JSON)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 210–213

Extracts JSON text from a JSON context item by using a SQL/JSON path expression.

## Syntax

```sql
JSON_QUERY(
 <JSON_API_common_syntax>
 [ <JSON_output_clause> ]
 [ <JSON_query_wrapper_behavior> ]
 [ <JSON_query_empty_behavior> ON EMPTY ]
 [ <JSON_query_error_behavior> ON ERROR ]
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

#### JSON_output_clause

Specifies the output created by the JSON_QUERY function.

```sql
<JSON_output_clause> ::= RETURNING <data_type>
```

##### data_type

Specifies the data type to be set as the return type of the JSON QUERY function. Supported data types: NVARCHAR(`<length>`), VARCHAR(`<length>`).

#### JSON_query_wrapper_behavior WRAPPER

Specifies the wrapper behavior of the JSON query.

```sql
<JSON_query_wrapper_behavior> WRAPPER
<JSON_query_wrapper_behavior> ::=
WITHOUT [ ARRAY ]
 | WITH [ CONDITIONAL | UNCONDITIONAL ] [ ARRAY ]
```

The default is WITHOUT ARRAY WRAPPER. However, if WITH is specified, then the default is UNCONDITIONAL ARRAY WRAPPER.

#### JSON_query_empty_behavior ON EMPTY

Specifies the behavior of the function if the related data is not in the context item. The default is NULL ON EMPTY.

```sql
<JSON_query_empty_behavior> ON EMPTY
<JSON_query_empty_behavior> ::=
ERROR
 | NULL
 | EMPTY ARRAY
 | EMPTY OBJECT
```

ERROR ON EMPTY returns an error if the related data is not in the context item. NULL ON EMPTY returns a NULL if the related data is not in the context item. EMPTY ARRAY ON EMPTY returns an empty array if the related data is not in the context item. EMPTY OBJECT ON EMPTY returns an empty JSON object if the related data is not in the context item.

#### JSON_query_error_behavior ON ERROR

Specifies the behavior of the function when the query throws an error. The default is NULL ON ERROR.

```sql
<JSON_query_error_behavior> ON ERROR
<JSON_query_error_behavior> ::=
ERROR
 | NULL
 | EMPTY ARRAY
 | EMPTY OBJECT
```

ERROR ON ERROR returns an error if the function result includes an error. NULL ON ERROR returns a NULL if the function result includes an error. EMPTY ARRAY ON ERROR returns an empty array if the function result includes an error. EMPTY OBJECT ON ERROR returns an empty JSON object if the function result includes an error.

## Description

Extracts JSON text from a JSON context item using a SQL/JSON path expression.

The following tokens are supported in `<JSON_API_common_syntax>`:

| **Token** | **Description** | **Example** |
| --- | --- | --- |
| $ | The context item (the first argument of the function). | `'$'` |
| . | The member of an object. | `'$.item.description'` |
| [ | The array index specifier (open). |   |
| ] | The array index specifier (closed). | `'$[1]' '$.item.list[1]'` |
| to | The array index range. | `'$[3 to 5]' = '$[3,4,5]'` |
| \* | The wild card. | `'$.*.description' '$.item.list[*]'` |

## Example

The following query returns the value `{"item1":1,"item2":2,"item3":3}`.

```sql
SELECT JSON_QUERY('{"item1":1, "item2":2, "item3":3}', '$') AS JSONQUERY FROM
DUMMY;
```

The following query returns the value `[1]`.

```sql
SELECT JSON_QUERY('{"item1":1, "item2":2, "item3":3}', '$.item1' WITH WRAPPER )
AS JSONQUERY FROM DUMMY;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
