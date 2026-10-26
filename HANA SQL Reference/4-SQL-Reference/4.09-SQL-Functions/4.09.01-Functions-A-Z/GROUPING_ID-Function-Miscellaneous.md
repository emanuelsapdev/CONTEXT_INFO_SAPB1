# 4.9.1.86 GROUPING_ID Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 194–196

Returns an integer value to identify which grouping set each row belongs to.

## Syntax

```sql
GROUPING_ID(<column_name_list>)
```

## Description

The GROUPING_ID function can be used with GROUPING SETS, ROLLUP, or CUBE, which return multiple levels of aggregation in a single result set. . GROUPING_ID returns an integer value to identify which grouping set each row belongs to. Each column in GROUPING_ID must be an element of GROUPING SETS.

GROUPING_ID is assigned by converting the bit vector generated from GROUPING SETS to a decimal number by treating the bit vector as a binary number. When a bit vector is composed, 0 is assigned to each column specified in the GROUPING SETS and 1 otherwise in the order it appears in GROUPING SETS. By treating the bit vector as a binary number, this function returns an integer value as the output.

## Example

The following statement uses the fictitious table guided_navi_tab and the results indicates which grouping set each row belongs to:

```sql
SELECT customer, year, product, SUM(sales),
   GROUPING_ID(customer, year, product)
   FROM guided_navi_tab
   GROUP BY GROUPING SETS (
    (customer, year, product),
    (customer, year),
    (customer, product),
    (year, product),
    (customer),
    (year),
    (product));
```

| **CUSTOMER** | **YEAR** | **PRODUCT** | **SUM(SALES)** | **GROUPING_ID(CUSTOMER,YEAR,PRODUCT),** |
| --- | --- | --- | --- | --- |
| C1 | 2009 | P1 | 100 | 0 |
| C1 | 2010 | P1 | 50 | 0 |
| C2 | 2009 | P1 | 200 | 0 |
| C2 | 2010 | P1 | 100 | 0 |
| C1 | 2009 | P2 | 200 | 0 |
| C1 | 2010 | P2 | 150 | 0 |
| C2 | 2009 | P2 | 300 | 0 |
| C2 | 2010 | P2 | 150 | 0 |
| C1 | 2009 | a | 300 | 1 |
| C1 | 2010 | a | 200 | 1 |
| C2 | 2009 | a | 500 | 1 |
| C2 | 2010 | a | 250 | 1 |
| C1 | a | P1 | 150 | 2 |
| C2 | a | P1 | 300 | 2 |
| C1 | a | P2 | 350 | 2 |
| C2 | a | P2 | 450 | 2 |
| a | 2009 | P1 | 300 | 4 |
| a | 2010 | P1 | 150 | 4 |
| a | 2009 | P2 | 500 | 4 |
| a | 2010 | P2 | 300 | 4 |
| C1 | a | a | 500 | 3 |
| C2 | a | a | 750 | 3 |
| a | 2009 | a | 800 | 5 |
| a | 2010 | a | 450 | 5 |
| a | a | P1 | 450 | 6 |
| a | a | P2 | 800 | 6 |
