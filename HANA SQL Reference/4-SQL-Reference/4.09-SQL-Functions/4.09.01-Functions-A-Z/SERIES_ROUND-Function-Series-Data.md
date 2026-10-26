# 4.9.1.173 SERIES_ROUND Function (Series Data)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 323–327

Rounds a specified value to the series value using the specified rounding settings.

## Syntax

```sql
SERIES_ROUND( <value>, { <increment_by> | SERIES TABLE <series_table> } [,
<rounding_mode> [, <alignment_expression> ] ] )
```

## Syntax Elements

**value** Specifies that the value parameter can either be a numeric value or a date/time type.

```sql
<value> ::= { <real_const> | <datetime_const> }
```

**increment_by** If the `<value>` parameter is numeric, then the `<increment_by>` value must be a numeric value that defines the period of the series.

```sql
<increment_by>::= <interval_const>
```

If the `<value>` parameter is a date/time type, then the `<increment_by>` value must be a string of the form "INTERVAL number units" where units is either YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND and the number must be an integer, unless the unit type is SECOND and the associated data type is TIMESTAMP. **series_table** Specifies that the maximum and minimum values in a provided series table are used to calculate the rounded values.

```sql
<series_table> ::= <identifier>
```

If a SERIES TABLE reference is specified, then the `<increment_by>` value is retrieved from the series descriptor of that table. This series must be equidistant. **rounding_mode** Specifies that the natural zero that serves as the basis for the rounding depends on the data type and interval.

```sql
<rounding_mode> ::= ROUND_HALF_UP
 | ROUND_HALF_DOWN
 | ROUND_HALF_EVEN
 | ROUND_UP
 | ROUND_DOWN
 | ROUND_CEILING
 | ROUND_FLOOR
```

For numeric types, zero is the numeric zero. For date types with the interval units of DAY or smaller, zero is midnight. For MONTH and YEAR intervals, zero is midnight on the first day of the month, and midnight on the first day of the year, respectively. The following rounding modes are supported:

| **Mode** | **Description** |
| --- | --- |
| ROUND_HALF_UP | Specifies the default value. The value is rounded to the nearest series value. Values that fall halfway between two series values are rounded up, away from zero. |
| ROUND_HALF_DOWN | Specifies that the value is rounded to the nearest series value. Values that fall halfway between two round values are rounded down, toward zero. |
| ROUND_HALF_EVEN | Specifies that the value is rounded to the nearest series value. Values that fall halfway between two rounded values are rounded to the even series value, based on element number. |
| ROUND_UP | Specifies that the value is always rounded away from zero to the larger series value. |
| ROUND_DOWN | Specifies that the value is always rounded toward zero to the smaller series value. |
| ROUND_CEILING | Specifies that the value is always rounded in a positive direction to the larger series value. |
| ROUND_FLOOR | Specifies that the value is always rounded in a negative direction to the smaller series value. |

**alignment_expression** Specifies that this parameter must be convertible to the `<value>` data type.

```sql
<alignment_expression> ::= { <real_const> | <datetime_const> }
```

A `<rounding_mode>` must be specified when using this parameter.

## Description

Rounds a specified value to the series value using the specified rounding settings.

## Examples

The example below horizontally aggregates a series table by using the ROUND_DOWN mode:

```sql
CREATE COLUMN TABLE ExampleSeriesTable(
    sid INTEGER NOT NULL,
    ts TIMESTAMP NOT NULL,
    val DOUBLE)
    SERIES(SERIES KEY(sid) PERIOD FOR SERIES(ts)
        EQUIDISTANT INCREMENT BY INTERVAL 60 SECOND);
SELECT rounded.sid, week, AVG(val) AS weekly_avg FROM(
    SELECT t.sid, SERIES_ROUND(ts, 'INTERVAL 7 DAY', ROUND_DOWN)
        AS week, val FROM ExampleSeriesTable AS t
    ) AS rounded
    GROUP BY rounded.sid, week;
```

The fictitious example below illustrates another way to perform horizontal aggregation, using the fictional table DailyWeather:

```sql
INSERT INTO DailyWeather(id, date, avg_temp)
    SELECT id, SERIES_ROUND(ts, SERIES TABLE DailyWeather) date, AVG(temp)
    FROM HourlyWeather
    GROUP BY id, SERIES_ROUND(ts, SERIES TABLE DailyWeather)
    ORDER BY 1, 2;
```

The example below illustrates different ways of aggregating data when moving from narrower to wider intervals:

```sql
CREATE COLUMN TABLE SampleSensorData (
    machine_id varchar(10),
    ts timestamp,
    power_consumption double,
    flow_rate double,
    primary key(machine_id, ts))
SERIES (
    SERIES KEY(machine_id)
    PERIOD FOR SERIES(ts)
    EQUIDISTANT INCREMENT BY INTERVAL 1 MINUTE MISSING ELEMENTS ALLOWED);
-- Going from 1 minute to 1 day using Standard SQL:
SELECT machine_id,
    TO_DATE(YEAR(ts) || '-' || MONTH(ts) || '-' || DAYOFMONTH(ts),
        'YYYY-MM-DD') AS ts,
    SUM(power_consumption) AS power_consumption
    FROM SampleSensorData
    GROUP BY machine_id, YEAR(ts), MONTH(ts), DAYOFMONTH(ts);
-- Going from 1 minute to 15 minutes using SERIES_ROUND:
SELECT machine_id, ts AS original_ts,
    SERIES_ROUND(ts, 'INTERVAL 15 MINUTE', ROUND_FLOOR) AS rounded_ts
        FROM SampleSensorData
        WHERE machine_id = 'EQ42-P01'
        ORDER BY ts;
-- Going from 1 minute to 15 minutes using SERIES_ROUND (variant #1)
SELECT machine_id, ts, SUM(power_consumption) AS power_consumption
    FROM (
        SELECT machine_id, SERIES_ROUND(ts, 'INTERVAL 15 MINUTE', ROUND_FLOOR)
            AS ts, power_consumption
            FROM SampleSensorData
    )
    GROUP BY machine_id, ts
    ORDER BY machine_id, ts;
-- Going from 1 minute to 15 minutes using SERIES_ROUND (variant #2)
SELECT machine_id, SERIES_ROUND(ts, 'INTERVAL 15 MINUTE', ROUND_FLOOR)
    AS ts, sum(power_consumption) AS power_consumption
    FROM SampleSensorData
    GROUP BY machine_id, SERIES_ROUND(ts, 'INTERVAL 15 MINUTE', ROUND_FLOOR);
```

The example below shows how to round up 4.5 to a series incremented by 3. It returns the result `6`:

```sql
SELECT SERIES_ROUND(4.5, 3, ROUND_HALF_UP) "result" FROM DUMMY;
```

The example below shows how to round down 4.5 to a series incremented by 3. The example below shows returns the result `3`:

```sql
SELECT SERIES_ROUND(4.5, 3, ROUND_HALF_DOWN) "result" FROM DUMMY;
```

The previous example could be written as follows in the fictitious example below to refer to an equidistant series table:

```sql
CREATE COLUMN TABLE ExampleSeriesTable(id INTEGER, pos INTEGER)
    SERIES(SERIES KEY(id) EQUIDISTANT INCREMENT BY 3 PERIOD FOR SERIES(pos));
SELECT SERIES_ROUND(4.5, SERIES TABLE ExampleSeriesTable, ROUND_HALF_DOWN)
    "result" FROM DUMMY;
```

The example below shows how to round down a date to the beginning of the year. It returns the result `Jan 1, 2013`:

```sql
SELECT SERIES_ROUND('2013-05-24', 'INTERVAL 1 YEAR', ROUND_DOWN) "result"
    FROM DUMMY;
```

The example below shows how to round up a time to the next 10 minute interval. It returns the result `4:30:00 AM`:

```sql
SELECT SERIES_ROUND('04:25:01', 'INTERVAL 10 MINUTE') "result" FROM DUMMY;
```
