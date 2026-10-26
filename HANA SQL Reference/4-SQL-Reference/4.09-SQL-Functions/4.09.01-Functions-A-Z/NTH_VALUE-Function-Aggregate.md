# 4.9.1.139 NTH_VALUE Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 268–269

Returns the value of an element at a specific position in an expression. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
NTH_VALUE( <expression>, <position> <order_by_clause> )
```

### Window function:

```sql
NTH_VALUE( <expression>, <position> <order_by_clause> ) <window_specification>
```

## Syntax Elements

#### expression

Specifies the expression where the position of the element occurs.

#### position

Specifies the position of the element in `<expression>`.

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

Returns the value of the element at position specified by `<position>` in `<expression>` as ordered by `<order_by_clause>`.

Null is returned if the value is NULL or if the value of `<position>` is greater than the number of elements in `<expression>`.

An error is raised if `<position>` is less than or equal to 0.

The output of NTH_VALUE function can be non-deterministic among tied values.

## Example

The example below returns the second value in column `COL1`: `700`, when the table is ordered by `COL2`.

```sql
CREATE ROW TABLE T (COL1 DOUBLE, COL2 DOUBLE);
INSERT INTO T VALUES(900, 10);
INSERT INTO T VALUES(400, 50);
INSERT INTO T VALUES(700, 30);
INSERT INTO T VALUES(200, 40);
SELECT NTH_VALUE (COL1, 2 ORDER BY COL2) FROM T;
```

## Related Information

COLLATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md) Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md)
