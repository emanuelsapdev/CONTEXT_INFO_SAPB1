# 4.9.1.226 VAR Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 377–378

Returns the variance of the given expression as the square of the standard deviation. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
VAR( [ ALL | DISTINCT ] <expression> )
```

### Window function:

```sql
VAR( <expression> ) <window_specification>
```

## Syntax Elements

#### expression

Specifies the input data for the function.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

| Result type based on input<br> `TINYINT` | `SMALLINT` | `INTEGER` | `BIGINT` | `DECIMAL(p ,s)` | `DECIMAL` | `REAL` | `DOUBLE` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `DECIMAL(9 ,6)` | `DECIMAL(11,6)` | `DECIMAL(16,6)` | `DECIMAL(25,6)` | `DECIMAL(p ,s)` | `DECIMAL` | `REAL` | `DOUBLE` |

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

The following example returns `2128.67`, the variance of values in the Price column:

```sql
SELECT VAR("Price") FROM "MyProducts";
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) VAR_POP Function (Aggregate) [→](VAR_POP-Function-Aggregate.md) VAR_SAMP Function (Aggregate) [→](VAR_SAMP-Function-Aggregate.md)
