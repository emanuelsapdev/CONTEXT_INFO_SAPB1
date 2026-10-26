# 4.9.1.46 COUNT Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 150–152

Counts the number of rows returned by a query. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
COUNT (*)
 | COUNT ( [ ALL ] <expression> )
 | COUNT ( DISTINCT <expression_list>
```

### Window function:

```sql
COUNT (*) [ <window_specification> ]
 | COUNT ( [ ALL ] <expression> ) [ <window_specification> ]
 | COUNT ( DISTINCT <expression> ) [ <window_specification> ]
```

## Syntax Elements

#### *

Returns the number of rows returned by the query, regardless of the value of those rows, and including duplicate values.

#### ALL

Optional keyword reflecting the default behavior. That is, `COUNT(ALL <expression>)` and `COUNT(<expression>)` return the same result.

#### expression

Specifies the input data for the function. The function returns the number of non-NULL values for the specified expression returned by the query, including duplicate values (unless DISTINCT is also specified).

#### expression_list

Specifies the input data for the function as a comma-separated list of `<expression>`. `<expression_list>` is only supported for use with the DISTINCT clause.

```sql
<expression_list>::= <expression> [, <expression> [,…] ]
```

#### DISTINCT

Returns the number of distinct values returned by the query, excluding rows with all NULL values for that expression.

**window_specification** Defines a window on the data over which the function operates. For syntax, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

| Result type based on input<br> `TINYINT` | `SMALLINT` | `INTEGER` | `BIGINT` | `DECIMAL(p ,s)` | `DECIMAL` | `REAL` | `DOUBLE` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `BIGINT` | `BIGINT` | `BIGINT` | `BIGINT` | `BIGINT` | `BIGINT` | `BIGINT` | `BIGINT` |

## Example

The following statements create a table with data for example purposes:

```sql
DROP TABLE "MyProducts";
CREATE COLUMN TABLE "MyProducts"(
  "Product_ID" VARCHAR(10),
  "Product_Name" VARCHAR(100),
  "Category" VARCHAR(100),
  "Quantity" INTEGER,
  "Price" DECIMAL(10,2),
  PRIMARY KEY ("Product_ID") );

INSERT INTO "MyProducts" VALUES('P1','Shirts', 'Clothes', 32, 20.99);
INSERT INTO "MyProducts" VALUES('P2','Jackets', 'Clothes', 16, 99.49);
INSERT INTO "MyProducts" VALUES('P3','Trousers', 'Clothes', 30, 32.99);
INSERT INTO "MyProducts" VALUES('P4','Coats', 'Clothes', 5, 129.99);
INSERT INTO "MyProducts" VALUES('P5','Purse', 'Accessories', 3, 89.49);
```

The following example returns `5`, the number of rows in the MyProducts table:

```sql
SELECT COUNT(*) FROM "MyProducts";
```

The following example returns `2`, the number of rows with distinct values in the Category column:

```sql
SELECT COUNT(DISTINCT "Category") FROM "MyProducts";
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md)
