# 4.9.1.184 STRING_AGG Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 337–339

Returns the concatenation string of the specified expression.

## Syntax

```sql
STRING_AGG( <expression>[, <delimiter> ] [ <order_by_clause> ] )
```

## Syntax Elements

#### expression

Specifies a VARCHAR or NVARCHAR expression with values to be concatenated. If the input values are a different data type than VARCHAR or NVARCHAR, then implicit casting is attempted.

For example, if the NUM column has five integer values (1, 2, 3, 4, 5), then STRING_AGG("NUM",0) returns 102030405.

#### delimiter

Specifies the character to use as a delimiter when aggregating values.

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

## Description

NULL values are treated as empty strings.

The default ordering is ASC NULLS FIRST. If DESC is specified, then the ORDER BY expression becomes DESC NULLS LAST.

## Example

The example below creates table r1 and populate it with data.

```sql
CREATE ROW TABLE r1(a INT, str VARCHAR(20), grp INT);
INSERT INTO r1 VALUES (3,'str2',0);
INSERT INTO r1 VALUES (0,'str1',0);
INSERT INTO r1 VALUES (NULL,'NULL',0);
INSERT INTO r1 VALUES (5,'str3',0);
INSERT INTO r1 VALUES (3,'val3',1);
INSERT INTO r1 VALUES (6,'val6',1);
INSERT INTO r1 VALUES (NULL,'NULL',1);
INSERT INTO r1 VALUES (1,'val1',1);
```

Execute the following statement to return the concatenation string of each record from table r1 in ascending order.

```sql
SELECT grp, STRING_AGG(str,','ORDER BY a)AS agg FROM R1 GROUP BY grp;
```

The statement above returns the following results.

| **GRP** | **AGG** |
| --- | --- |
| 0 | NULL,str1,str2,str3 |
| 1 | NULL,val1,val3,val6 |

Execute the following statement to return the concatenation string of each record from table r1 in descending order.

```sql
SELECT grp, STRING_AGG(str,','ORDER BY a DESC) AS agg FROM r1 GROUP BY grp;
```

The statement above returns the following results.

| **GRP** | **AGG** |
| --- | --- |
| 0 | str3,str2,str1,NULL |
| 1 | val6,val3,val1,NULL |

## Related Information

Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) COLLATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md)
