# 4.9.1.161 ROUND Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 297–299

Rounds the specified argument to the specified amount of places after the decimal point.

## Syntax

```sql
ROUND(<number> [, <position> [, <rounding_mode>]])
```

## Syntax Elements

#### number

Specifies the numeric argument to round.

#### position

Specifies the amount of places after the decimal point to round `<number>` to. The default value is 0. A positive or negative integer rounds to the specified position to the right or left of the decimal point, respectively.

#### rounding_mode

Defines how the rounding should be carried out.

```sql
<rounding_mode> ::=
ROUND_HALF_UP
| ROUND_HALF_DOWN
| ROUND_HALF_EVEN
| ROUND_UP
| ROUND_DOWN
| ROUND_CEILING
| ROUND_FLOOR
```

##### ROUND_HALF_UP

The value is rounded up to the next round figure. This is the default.

If the value falls precisely halfway between two rounded values, it is rounded up away from zero (as is done in commercial rounding).

##### ROUND_HALF_DOWN

The value is rounded down to the next round figure. If the value falls precisely halfway between two round values, it is rounded down towards zero.

##### ROUND_HALF_EVEN

The value is rounded to the next round figure. If the value falls precisely halfway between two rounded values, it is rounded to the value whose last decimal place is an even number.

##### ROUND_UP

The value is always rounded away from zero, to the larger round figure.

##### ROUND_DOWN

The value is always rounded towards zero, to the smaller round figure.

##### ROUND_CEILING

The value is always rounded in a positive direction, to the larger value.

##### ROUND_FLOOR

The value is always rounded in a negative direction, to the smaller value.

## Description

Rounds argument `<n>` to the specified amount of places (`<pos>`) after the decimal point.

When using ROUND with floating point types, REAL and DOUBLE, the precision of the numeric representation can affect the result. In this case, the actual number of digits after the decimal point is influenced by the precision of the type used. For example, the result of the following statement is `399.7099914550781` not `399.71`:

```sql
SELECT ROUND(TO_REAL(399.71429443359375),2) from DUMMY;
```

## Examples

The following example returns the value `16.2`:

```sql
SELECT ROUND (16.16, 1) "round" FROM DUMMY;
```

The following example returns the value `20` :

```sql
SELECT ROUND (16.16, -1) "round" FROM DUMMY;
```

The following example returns the value `438.8`:

```sql
SELECT ROUND( 438.75, 1, ROUND_HALF_UP) "round" FROM DUMMY;
```

The following example returns the value `438.7`:

```sql
SELECT ROUND( 438.75, 1, ROUND_HALF_DOWN) "round" FROM DUMMY;
```

The following example returns the value `438.8`:

```sql
SELECT ROUND( 438.75, 1, ROUND_HALF_EVEN) "round" FROM DUMMY;
```

The following example returns the value `438.8`:

```sql
SELECT ROUND( 438.71, 1, ROUND_UP) "round" FROM DUMMY;
```

The following example returns the value `438.7`:

```sql
SELECT ROUND( 438.79, 1, ROUND_DOWN) "round" FROM DUMMY;
```

The following example returns the value `438.8`:

```sql
SELECT ROUND( 438.75, 1, ROUND_CEILING) "round" FROM DUMMY;
```

The following example shows the difference when specifying a positive and negative integer for `<pos>`:

```sql
SELECT ROUND(1234.1234, 1)"round" FROM DUMMY;  ==> 1234.1000
SELECT ROUND(1234.1234, -1)"round" FROM DUMMY; ==> 1230.0000
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
