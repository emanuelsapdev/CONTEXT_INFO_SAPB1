# 4.9.1.126 MIN Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 255–257

Returns the minimum value of the expression. This function can also be used as a window function.

## Syntax

### Aggregate function:

```sql
MIN( [ ALL | DISTINCT ] <expression> )
```

### Window function:

```sql
MIN( <expression> ) <window_specification>
```

## Syntax Elements

#### expression

Specifies the input data for the function.

#### window_specification

Defines a window on the data over which the function operates. For `<window_specification>`, see Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md).

## Description

| Result type based on input<br> `TINYINT` | `SMALLINT` | `INTEGER` | `BIGINT` | `DECIMAL(p ,s)` | `DECIMAL` | `REAL` | `DOUBLE` |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `TINYINT` | `SMALLINT` | `INTEGER` | `BIGINT` | `DECIMAL(p ,s)` | `DECIMAL` | `REAL` | `DOUBLE` |

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

The following example returns `20.99`, the minimum price of the products in the MyProducts table:

```sql
SELECT MIN("Price") FROM "MyProducts";
```

## Related Information

Window Functions and the Window Specification [→](../4.09.14-Window-Functions/README.md) Window Aggregate Functions [→](../4.09.14-Window-Functions/4.09.14.01-Window-Aggregate-Functions.md) Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) Expressions [→](../../4.06-Expressions.md)
