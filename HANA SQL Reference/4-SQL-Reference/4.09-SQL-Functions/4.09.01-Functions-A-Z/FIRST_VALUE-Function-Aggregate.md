# 4.9.1.81 FIRST_VALUE Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 189–190

Returns the value of the first element of an expression. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
FIRST_VALUE( <expression> <order_by_clause> )
```

### Window function:

```sql
FIRST_VALUE( <expression> <order_by_clause> ) <window_specification>
```

## Syntax Elements

#### expression

Specifies the expression of data to operate over.

#### order_by_clause

Specifies the sort order of the input rows.

```sql
<order_by_clause> ::= ORDER BY <order_by_expression> [, <order_by_expression>
[,...] ]
<order_by_expression> ::=
 <column_name> [ ASC | DESC ] [ NULLS FIRST | NULLS LAST ]
[ <collate_clause> ]
 | <column_position> [ ASC | DESC ] [ NULLS FIRST | NULLS LAST ]
[ <collate_clause> ]
<collate_clause> ::= COLLATE <collation_name>
```

`<collate_clause>` specifies the collation to use for ordering values in the results. `<collate_clause>` can only be used on columns defined as NVARCHAR or VARCHAR.`<collation_name>` is one of the supported collation names listed in the COLLATIONS system view.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

Returns the value of the first element in `<expression>` as ordered by `<order_by_clause>`.

NULL is returned if the value is NULL or if `<expression>` is empty.

The output of the FIRST_VALUE function can be non-deterministic among tie values.

## Example

The example below returns the first value in the COL1 column when the table is ordered by COL2:

```sql
CREATE ROW TABLE T (COL1 DOUBLE, COL2 DOUBLE);
INSERT INTO T VALUES(9, 1);
INSERT INTO T VALUES(4, 5);
INSERT INTO T VALUES(7, 3);
SELECT FIRST_VALUE (COL1 ORDER BY COL2) FROM T;
```

The query returns `9`.

## Related Information

COLLATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md)
