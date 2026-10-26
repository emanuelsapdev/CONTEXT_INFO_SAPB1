# 4.9.1.134 NDIV0 Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 263

Returns 0 when divided by 0; otherwise, it returns the result of the division.

## Syntax

```sql
NDIV0( <numerator>, <denominator> )
```

## Description

Returns 0 if `<denominator>` is 0. Otherwise, it returns the division of the numerator by the denominator. `<numerator>` and `<denominator>` can be any numeric value. The function allows you to avoid divided-by-zero error messages and can continue a calculation with a defined result.

## Example

The following example uses the NDIV0 function to allow the revenue calculation to complete without a divide by zero error:

```sql
SELECT Revenue, Quantity, NDIV0(Revenue, Quantity) as AverageRevenue FROM DUMMY;
```

| **Revenue** | **Quantity** | **AverageRevenue** |
| --- | --- | --- |
| 1000 | 4 | 250 |
| 2000 | 0 | 0 |
| 2500 | 0 | 0 |
| 3000 | 5 | 600 |
