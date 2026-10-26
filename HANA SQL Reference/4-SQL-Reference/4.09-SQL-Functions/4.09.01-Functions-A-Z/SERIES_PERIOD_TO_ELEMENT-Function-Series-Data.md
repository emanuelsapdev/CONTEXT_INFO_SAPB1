# 4.9.1.172 SERIES_PERIOD_TO_ELEMENT Function (Series Data)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 321–323

Returns the one-based series element number that the given period value is associated with.

## Syntax

```sql
SERIES_PERIOD_TO_ELEMENT(
 <value>, {<increment_by>, <min_value>, <max_value> [, <rounding_mode>]
 | SERIES TABLE <series_table> [, <rounding_mode>]}
 )
```

## Syntax Elements

**value** Specifies that the `<value>` parameter can either be a numeric value or a date/time type.

```sql
<value> ::= INTEGER | DOUBLE | TIMESTAMP
```

**increment_by** Sets the increment value.

```sql
<increment_by> ::= <identifier>
```

If the `<value>` parameter is a date/time type, then the `<increment_by>` parameter should be a string in the form "INTERVAL number units" where units is either YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND and the number must be an integer, unless the units type is SECOND and the associated data type is TIMESTAMP. If the value is numeric, then the `<increment_by>` parameter should be a numeric value that defines the period of the series. **min_value** Sets the minimum period value.

```sql
<min_value> ::= <integer>
```

For an equidistant series, there is a mapping between periods and elements. The periods are in the space of the period columns, usually timestamps. The elements are always BIGINT. The element 1 represents the first period, associated with `<min_value>`. **max_value** Sets the maximum period value.

```sql
<max_value> ::= <integer>
```

**rounding_mode** Specifies that if the period value is not on a series period value, then it is rounded to the nearest series period value, which returns the associated element number.

```sql
<rounding_mode> ::= ROUND_HALF_UP
 | ROUND_HALF_DOWN
 | ROUND_HALF_EVEN
 | ROUND_UP
 | ROUND_DOWN
 | ROUND_CEILING
 | ROUND_FLOOR
```

The supported rounding modes are:

| **Rounding mode** | **Description** |
| --- | --- |
| ROUND_HALF_UP | Specifies that the value is rounded to the nearest series value. Values that fall halfway between two series values are rounded up away from zero.<br>This is the default value. |
| ROUND_HALF_DOWN | Specifies that the value is rounded to the nearest series value. Values that fall halfway between two round values are rounded down toward zero. |
| ROUND_HALF_EVEN | Specifies that the value is rounded to the nearest series value. Values that fall halfway between two rounded values are rounded to the even series value based on element number. |
| ROUND_UP | Specifies that the value is always rounded away from zero to the larger series value. |
| ROUND_DOWN | Specifies that the value is always rounded towards zero to the smaller series value. |
| ROUND_CEILING | Specifies that the value is always rounded in a positive direction to the larger series value. |
| ROUND_FLOOR | Specifies that the value is always rounded in a negative direction to the smaller series value. |

**series_table** If a series table reference is used, then this specifies that the values for `<increment_by>`, `<min_value>`, and `<max_value>` from the SERIES TABLE definition are used as the parameters for this function.

```sql
<series_table> ::= <identifier>
```

## Description

Returns the one-based series element number with which the given period value is associated, where period = min_value + ( element - 1 ) \* interval.

## Examples

The following example returns the result 4:

```sql
SELECT SERIES_PERIOD_TO_ELEMENT(5, 2, 0, 10, ROUND_HALF_UP) "element" FROM DUMMY;
```

The following example returns the result 3:

```sql
SELECT SERIES_PERIOD_TO_ELEMENT(5, 2, 0, 10, ROUND_HALF_DOWN) "element" FROM
DUMMY;
```

The example below picks the next element rounded down from 2014-01-05 12:00:00 from a date series from 2014-01-01 to 2014-12-32 in increments of 1 day. It returns the result 5:

```sql
SELECT SERIES_PERIOD_TO_ELEMENT(
    '2014-01-05 12:00:00',
    'INTERVAL 1 DAY',
    '2014-01-01',
    '2014-12-31',
    ROUND_HALF_DOWN) "element" FROM DUMMY;
```

The previous example could be written like the following fictitious example to refer to an equidistant series table:

```sql
CREATE COLUMN TABLE ExampleSeriesTable(id INTEGER, ts TIMESTAMP)
 SERIES(SERIES KEY(id) EQUIDISTANT INCREMENT BY INTERVAL 1 DAY
 MINVALUE '2014-01-01' MAXVALUE '2014-12-31' PERIOD FOR SERIES(ts));
SELECT SERIES_PERIOD_TO_ELEMENT('2014-01-05 12:00:00', SERIES TABLE
ExampleSeriesTable, ROUND_HALF_DOWN) "element" FROM DUMMY;
```
