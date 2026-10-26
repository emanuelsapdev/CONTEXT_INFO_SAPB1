# 4.9.1.85 GROUPING Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 192–194

Determines whether a specified column is used in grouping.

## Syntax

```sql
GROUPING(<column_name>)
```

## Description

The GROUPING function can be used with GROUPING SETS, ROLLUP, or CUBE, which return multiple levels of aggregation in a single result set. The function returns 1 if the specified column is used in aggregation, and 0 otherwise. The column of GROUPING must be an element of the GROUPING SETS.

## Example

```sql
CREATE COLUMN TABLE mySchema.Customers (
 cust_id INTEGER NOT NULL,
 cust_name NVARCHAR(20),
 num_emp INTEGER,
 region NVARCHAR(20),
 s_tier NVARCHAR(20),
 PRIMARY KEY ("CUST_ID")
 );

INSERT INTO mySchema.Customers VALUES( 1, 'CustA', 5, 'NorthEast', 'gold' );
INSERT INTO mySchema.Customers VALUES( 2, 'CustB', 26, 'NorthWest', 'gold' );
INSERT INTO mySchema.Customers VALUES( 3, 'CustC', 250, 'NorthEast', 'silver' );
INSERT INTO mySchema.Customers VALUES( 4, 'CustD', 180, 'SouthEast',
'platinum' );
INSERT INTO mySchema.Customers VALUES( 5, 'CustE', 32, 'SouthWest', 'silver' );
INSERT INTO mySchema.Customers VALUES( 6, 'CustF', 45, 'NorthEast', 'platinum' );
INSERT INTO mySchema.Customers VALUES( 7, 'CustG', 15, 'NorthWest', 'platinum' );
INSERT INTO mySchema.Customers VALUES( 8, 'CustH', 99, 'SouthEast', 'gold' );
INSERT INTO mySchema.Customers VALUES( 9, 'CustI', 6, 'NorthEast', 'silver' );
INSERT INTO mySchema.Customers VALUES( 10,'CustJ', 101, 'NorthEast', 'silver' );
INSERT INTO mySchema.Customers VALUES( 11,'Custk', 108, 'SouthEast', 'silver' );
SELECT cust_name AS "cust_name", cust_id AS "cust_id", region AS "region",
s_tier AS "s_tier", num_emp AS "num_emp",
GROUPING (region) AS "gr_reg", GROUPING (s_tier) AS "gr_tier", GROUPING
(num_emp) AS "gr_num"
FROM mySchema.Customers
GROUP BY GROUPING SETS (
    (s_tier, region),
    (region, s_tier),
    (cust_id, cust_name, num_emp)
);
```

| **cust_name** | **cust_id** | **region** | **sales_tier** | **num_emp** | **gr_reg** | **gr_tier** | **gr_num** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| NULL | NULL | NorthEast | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthWest | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthEast | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthWest | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthEast | silver | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | silver | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthWest | silver | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthEast | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthWest | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | gold | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthEast | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthWest | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | platinum | NULL | 0 | 0 | 1 |
| NULL | NULL | NorthEast | silver | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthEast | silver | NULL | 0 | 0 | 1 |
| NULL | NULL | SouthWest | silver | NULL | 0 | 0 | 1 |
| CustA | 1 | NULL | NULL | 5 | 1 | 1 | 0 |
| CustI | 9 | NULL | NULL | 6 | 1 | 1 | 0 |
| CustG | 7 | NULL | NULL | 15 | 1 | 1 | 0 |
| CustB | 2 | NULL | NULL | 26 | 1 | 1 | 0 |
| CustE | 5 | NULL | NULL | 32 | 1 | 1 | 0 |
| CustF | 6 | NULL | NULL | 45 | 1 | 1 | 0 |
| CustH | 8 | NULL | NULL | 99 | 1 | 1 | 0 |
| CustJ | 10 | NULL | NULL | 101 | 1 | 1 | 0 |
| CustK | 11 | NULL | NULL | 108 | 1 | 1 | 0 |
| CustD | 4 | NULL | NULL | 180 | 1 | 1 | 0 |
| CustC | 3 | NULL | NULL | 250 | 1 | 1 | 0 |
