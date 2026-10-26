# 4.9.1.102 JSON_VALUE Function (JSON)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 221–224

Extracts an SQL value of a predefined type from a JSON value.

## Syntax

```sql
JSON_VALUE(
 <JSON_API_common_syntax>
 [ <JSON_returning_clause> ]
 [ <JSON_value_empty_behavior> ON EMPTY ]
 [ <JSON_value_error_behavior> ON ERROR ]
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

When `<JSON_path_mode>` is set to STRICT, if the structural error occurs within a JSON filter expression, then the error handling of a JSON filter expression applies. Otherwise, a structural error is an unhandled error.

When the path is set to LAX, one of the following options occurs:

- If an operation requires an SQL/JSON array but the operand is not an SQL/JSON array, then the operand is wrapped in an SQL/JSON array prior to performing the operation.
- If an operation requires something other than an SQL/JSON array, but the operand is an SQL/ JSON array, then the operand is unwrapped by converting its elements into an SQL/JSON sequence prior to performing the operation.

Array indexes start from 0, rather than 1 (the SQL standard).

If there is still a structural error after applying these resolutions, then the result is an empty SQL/JSON sequence.

`<JSON_path_wff>` indicates an actual JSON path (for example, `'$.item1'`). `<JSON_path_specification>` does not use double quotes.

#### JSON_returning_clause

Defines the data type of the result.

```sql
<JSON_returning_clause> ::= RETURNING <data_type>
<data_type> ::=
INTEGER
 | BIGINT
 | DECIMAL
 | VARCHAR(<integer>)
 | NVARCHAR(<integer>)
```

#### JSON_value_empty_behavior ON EMPTY

Specifies the behavior of the function when the related data is not in the context item. The default is NULL ON EMPTY

```sql
<JSON_value_empty_behavior> ON EMPTY
<JSON_value_empty_behavior> ::=
ERROR
 | NULL
 | DEFAULT <value_expression>
```

ERROR ON EMPTY returns an error if the related data is not in the context item. NULL ON EMPTY returns a NULL if the related data is not in the context item. DEFAULT `<value_expression>` ON EMPTY returns `<value_expression>` if the related data is not in the context item.

#### JSON_value_error_behavior ON ERROR

Specifies the behavior of the JSON_VALUE function when an error occurs. The default is NULL ON ERROR.

```sql
<JSON_value_error_behavior> ON ERROR
<JSON_value_error_behavior> ::=
ERROR
 | NULL
 | DEFAULT <value_expression>
```

ERROR ON ERROR returns an error if the function results include an error. NULL ON ERROR returns a NULL if the function results include an error. DEFAULT `<value_expression>` ON ERROR returns `<value_expression>` if the function results include an error.

## Description

Extracts an SQL value of a predefined type from a JSON value.

The following tokens are supported in `<JSON_API_common_syntax>`:

| **Token** | **Description** | **Example** |
| --- | --- | --- |
| $ | The context item (the first argument of the function). | `'$'` |
| . | The member of an object. | `'$.item.description'` |
| [ | The array index specifier (open). |   |
| ] | Array index specifier (closed). | `'$[1]' '$.item.list[1]'` |
| to | The array index range. | `'$[3 to 5]' = '$[3,4,5]'` |
| \* | The wild card. | `'$.*.description' '$.item.list[*]'` |

## Example

The following statement returns a value of 10:

```sql
SELECT JSON_VALUE('{"item1":10}', '$.item1') AS "value" FROM DUMMY;
```

The following statement returns a value of 5:

```sql
SELECT JSON_VALUE('{"item1":{"sub1":10}, "item2":{"sub2":5}, "item3":{"sub3":
7}}', '$.*.sub2') AS "value" FROM DUMMY;
```

The following statement returns a value of 0:

```sql
SELECT JSON_VALUE('[0, 1, 2, 3]', '$[0]') AS "value"  FROM DUMMY;
```

The following statement returns the value "No last name found":

```sql
SELECT JSON_VALUE('{"firstname":"John"}', '$.lastname' DEFAULT 'No last name
found' ON EMPTY) AS "Last Name" FROM DUMMY;
```

The following statement causes a type conversion error to demonstrate the behavior for ERROR ON ERROR:

```sql
SELECT JSON_VALUE('{"item":"string"}', '$.item' RETURNING DECIMAL ERROR ON
ERROR) AS "Item" FROM DUMMY;
```

The following statement demonstrates what happens when there is no value (the object does not have the name "last name"):

```sql
SELECT JSON_VALUE('{"firstname":"John"}', 'strict $.lastname' ERROR ON ERROR) AS
"Last Name" FROM DUMMY;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
