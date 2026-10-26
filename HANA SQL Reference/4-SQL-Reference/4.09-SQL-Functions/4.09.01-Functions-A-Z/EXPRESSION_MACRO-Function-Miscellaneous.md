# 4.9.1.79 EXPRESSION_MACRO Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 187–188

Returns aggregated results from a query.

## Syntax

```sql
EXPRESSION_MACRO( <expression_macro_alias> )
```

## Syntax Elements

**expression_macro_alias** Specifies the name of an expression macro.

## Description

Use the EXPRESSION_MACRO function to select an expression that is based on columns and other EXPRESSION_MACROs from the view and that may also involve aggregation functions (like AVG). A SELECT statement with an EXPRESSION_MACRO that involves an aggregation function requires the same GROUP BY clause as if the aggregation function had appeared directly in the SELECT statement.

The list of all expression macros can be found in the VIEW_EXPRESSION_MACROS system view.

## Example

The following example creates a table, defines a view on the table that includes an expression macro, and then queries the view using the EXPRESSION_MACRO function to have the expression macro perform calculations on the result. In this example, the value 15 is returned (the average of 10 and 20).

```sql
CREATE TABLE t1(a INT);
INSERT INTO t1 VALUES(10);
INSERT INTO t1 VALUES(20);
CREATE VIEW v1 AS SELECT * FROM t1 WITH EXPRESSION MACROS(AVG(a) AS avgA);
SELECT EXPRESSION_MACRO(avgA) FROM v1;
```

## Related Information

[VIEW_EXPRESSION_MACROS System View](../../../6-System-Views-Reference/6.01-System-Views/VIEW_EXPRESSION_MACROS-System-View.md)
