# 4.9.1.72 DFT Function (Aggregate)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 179–181

Computes expressions and returns an array with specific elements.

## Syntax

```sql
DFT( <expression>, <N> { <series_orderby> | <order_by_clause> } ).{ REAL |
IMAGINARY | AMPLITUDE | PHASE }
```

## Syntax Elements

#### expression

Specifies a value assumed to be a sample taken at a constant time interval. `<expression>` cannot contain any NULL values.

#### N

This parameter must be a power of 2. The input is padded with zeros if it contains less than `<N>` elements.

#### series_orderby

The SERIES definition can only be used with an equidistant series.

```sql
<series_orderby> ::= SERIES( <series_period> <series_equidistant_definition> )
```

The series must not contain missing elements. For more information about this clause, see the SERIES_GENERATE function.

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

Computes the Discrete Fourier Transform of an expression for the first `<N>` values and returns an array with exactly `<N>` elements.

The returned values depend on the output parameter, which must be one of REAL, IMAGINARY, AMPLITUDE, or PHASE.

## Examples

The example below computes the Discrete Fourier Transform of a column in an equidistant series.

```sql
SELECT DFT(FRACTION_OF_MIN_MAX_RANGE, 4 SERIES(EQUIDISTANT INCREMENT BY 1 PERIOD
FOR SERIES(element_number))).REAL
    FROM SERIES_GENERATE_INTEGER(1,0,10);
```

The example below uses the fictional MY_TABLE and returns an array with 4 numbers representing the real part of the result.

```sql
SELECT DFT(col, 4 ORDER BY DATE).REAL FROM MY_TABLE;
```

The example below uses the fictional MY_TABLE and returns an array with 8 numbers representing the imaginary part of the result.

```sql
SELECT DFT(col, 8 ORDER BY DATE).IMAGINARY FROM MY_TABLE;
```

The example below uses the fictional MY_TABLE and returns an array with 8 numbers representing the amplitude part (i.e. SQRT(REAL^2 + IMAGINARY^2)) of the result.

```sql
SELECT DFT(col, 8 ORDER BY DATE).AMPLITUDE FROM MY_TABLE;
```

The example below uses the fictional MY_TABLE returns an array with 8 numbers representing the phase part of the result and ranges between -PI and +PI.

```sql
SELECT DFT(col, 8 ORDER BY DATE).PHASE FROM MY_TABLE;
```

## Related Information

Aggregate Functions [→](../4.09.02-Aggregate-Functions.md) COLLATIONS System View [→](../../../6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md) SERIES_GENERATE Function (Series Data) [→](SERIES_GENERATE-Function-Series-Data.md)
