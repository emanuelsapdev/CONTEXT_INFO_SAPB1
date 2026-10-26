# 4.9.1.169 SERIES_ELEMENT_TO_PERIOD Function (Series Data)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 311–313

Returns the series period value associated with the specified one-based series element number.

## Syntax

```sql
SERIES_ELEMENT_TO_PERIOD( <element_number>, { <increment_by>, <min_value>,
<max_value> | SERIES TABLE <series_table> } )
```

## Syntax Elements

**element_number** Specifies the element number.

```sql
<element_number> ::= INTEGER
```

**increment_by** Defined as either an integer constant, an interval constant, or a defined number of elements between a minimum and a maximum.

```sql
<increment_by> ::= <real_const> | <interval_const>
```

If the period type is a DATETIME, then the number needs to be preceded by INTERVAL followed by a time unit, such as YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND. Exponential notation is allowed. **min_value** Specifies the minimum value. It can either be a numeric or a date/time value.

```sql
<min_value> ::= <real_const> | <datetime_const>
```

**max_value** Specifies the maximum value. It can either be a numeric or a date/time value.

```sql
<max_value> ::= <real_const> | <datetime_const>
```

**series_table** If a series table reference is used, then the `<increment_by>`, `<min_value>`, and `<max_value>` values from the SERIES TABLE definition are used as the parameters for this function.

```sql
<series_table> ::= <identifier>
```

## Description

Returns the series period value associated with the provided one-based series element number, where rounded_period = SERIES_ROUND (period, interval, round_mode) and element = 1 + ( rounded_period - min_value ) / interval.

## Examples

The example below picks the fifth element from a series from 0 to 10 in increments of 2 and returns `8`:

```sql
SELECT SERIES_ELEMENT_TO_PERIOD(5, 2, 0, 10) "val" FROM DUMMY;
```

The example below picks the sixth element from a series from 1 to 10 in increments of 1.25 and returns `7.25`:

```sql
SELECT SERIES_ELEMENT_TO_PERIOD(6, 1.25, 1, 10) "val" FROM DUMMY;
```

The example below picks the seventh element from a date series from 2014-01-01 to 2014-12-31 in increments of 1 day and returns `Jan 7, 2014`:

```sql
SELECT SERIES_ELEMENT_TO_PERIOD(7, 'INTERVAL 1 DAY', '2014-01-01', '2014-12-31')
    "val" FROM DUMMY;
```

The previous example can be written as follows to refer to an equidistant series table, and returns `7`:

```sql
CREATE COLUMN TABLE ExampleSeriesTable(id INTEGER, ts TIMESTAMP)
    SERIES(SERIES KEY(id) EQUIDISTANT INCREMENT BY INTERVAL 1 DAY
        MINVALUE '2014-01-01' MAXVALUE '2014-12-31' PERIOD FOR SERIES(ts));
SELECT SERIES_PERIOD_TO_ELEMENT(
    '2014-01-07',
    SERIES TABLE ExampleSeriesTable)
    "element" FROM DUMMY;
```

The example below picks the seventh element from a date series from 2014-01-01 to 2014-12-31 in increments of 1 month and returns `Jul 1, 2014`:

```sql
SELECT SERIES_ELEMENT_TO_PERIOD(7, 'INTERVAL 1 MONTH',
    '2014-01-01', '2014-12-31') "val" FROM DUMMY;
```

The example below picks the 500.000th element from a time series from 2014-01-01 to 2014-12-31 in increments of 1.5 seconds and returns `Jan 9, 2014 4:19:58.5 PM`:

```sql
SELECT SERIES_ELEMENT_TO_PERIOD(500000, 'INTERVAL 1.5 SECOND',
    '2014-01-01 00:00:00.000', '2014-12-31') "val" FROM DUMMY;
```
