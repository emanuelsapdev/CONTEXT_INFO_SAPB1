# 4.9.1.14 ALLOW_PRECISION_LOSS Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 99–100

Allows loss of precision when aggregating decimal values using an aggregate expression.

## Syntax

```sql
ALLOW_PRECISION_LOSS( <aggregate_expression> )
```

## Syntax Elements

#### aggregate_expression

The aggregate expression for which to allow precision loss. Currently SUM is the only supported aggregate expression.

```sql
<aggregate_expression> ::= SUM ( <expression> )
```

## Description

Use this function to improve performance of an aggregation expression on DECIMAL values when loss of precision is acceptable and to improve performance of the aggregation.

## Example

The following example shows the difference in values returned when using the ALLOW_PRECISION_LOSS function:

```sql
CREATE TABLE TESTTABLE (COL1 decimal(10,5), COL2 decimal);
INSERT INTO TESTTABLE VALUES(1.139999, 1.138888888);
INSERT INTO TESTTABLE VALUES(2.119999, 2.118888888);
INSERT INTO TESTTABLE VALUES(2.119999, 2.118888888);
INSERT INTO TESTTABLE VALUES(2.669999, 2.668888888);

-- The following query, which does not allow precision loss, returns 8.01, 8.01
SELECT SUM(TO_DECIMAL(COL1,10,2)), SUM(TO_DECIMAL(COL2,10,2)) FROM TESTTABLE;
-- The following query, which uses the ALLOW_PRECISION_LOSS function to allow
precision loss, returns 8.04, 8.04
SELECT ALLOW_PRECISION_LOSS(SUM(TO_DECIMAL(COL1,10,2))),
ALLOW_PRECISION_LOSS(SUM(TO_DECIMAL(COL2,10,2))) FROM TESTTABLE;
```

## Related Information

[Expressions](../../4.06-Expressions.md)
