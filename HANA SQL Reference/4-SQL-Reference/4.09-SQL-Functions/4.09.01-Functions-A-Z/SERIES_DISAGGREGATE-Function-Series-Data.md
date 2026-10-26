# 4.9.1.168 SERIES_DISAGGREGATE Function (Series Data)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 306–311

Generates a complete series table with rows disaggregated into defined partitions.

## Syntax

```sql
SERIES_DISAGGREGATE(
    {SERIES TABLE <source_series_table> | <source_increment_by>},
    {SERIES TABLE <generate_series_table> | <target_increment_by>}
    [, <value_range> ] )
| { SERIES_DISAGGREGATE_TINYINT
| SERIES_DISAGGREGATE_SMALLINT
| SERIES_DISAGGREGATE_INTEGER
| SERIES_DISAGGREGATE_BIGINT
| SERIES_DISAGGREGATE_SMALLDECIMAL
| SERIES_DISAGGREGATE_DECIMAL
| SERIES_DISAGGREGATE_TIME
| SERIES_DISAGGREGATE_DATE
| SERIES_DISAGGREGATE_SECONDDATE
| SERIES_DISAGGREGATE_TIMESTAMP }
(<source_increment_by>, <target_increment_by>, <min_value>, <max_value>)
```

## Syntax Elements

**source_series_table** Defines the name of one or two equidistant series tables with the SERIES TABLE syntax.

```sql
<source_series_table> ::= <identifier>
<generate_series_table> ::= <identifier>
```

**value_range** Defines the range of values.

```sql
<value_range> ::= <min_value> [, <max_value>]
<min_value> ::= <real_const> | <datetime_const>
<max_value> ::= <real_const> | <datetime_const>
```

When using the SERIES TABLE syntax, the values of the source increment and/or generated increment are retrieved from the series definitions of the respective table references. The `<min_value>` is the greater `<min_value>` of the two specified tables, and the `<max_value>` is the lesser `<max_value>` of the two specified tables. The `<min_value>` and `<max_value>` can still be manually specified if a SERIES TABLE reference is supplied. Manually specified values override those in the series table definition. The generic form of the procedure that takes at least one SERIES TABLE reference does not have to use the name of the series data type in the procedure name. **source_increment_by** Sets the source increment value.

```sql
<source_increment_by> ::= <real_const> | <datetime_const>
```

**generate_series_table** Generates the series table with the SERIES TABLE syntax.

```sql
<generate_series_table> ::= <identifier>
```

**target_increment_by** Sets the target increment value.

```sql
<target_increment_by> ::= <real_const> | <datetime_const>
```

**constant_literal** The `<constant_literal>` parameter is defined as a `<real_const>` or a `<datetime_const>`.

```sql
<constant_literal> ::= <real_const> | <datetime_const>
```

It is either an integer constant, an interval constant, or a defined number of elements between a minimum and maximum. If the period type is a DATETIME, then the number needs to be preceded by INTERVAL followed by a time unit, such as YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND. Exponential notation is allowed.

## Description

Generates a complete series table with rows disaggregated into partitions defined by the `<generate_increment_by>` parameter.

The resulting table can be joined with a series table to perform horizontal disaggregation.

For date/time types, the `<increment_by>` parameter should be a string in the form "INTERVAL number units" where units is either YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND and the number must be an integer, unless the units type is SECOND and the associated data type is TIMESTAMP.

The `<min_value>` parameter for the numeric versions of this function does not need to be aligned to numeric zero with respect to the `<increment_by>` value. You can specify a `<source_increment>` of 2 and a `<min_value>` of 1, which results in a source series of 1, 3, 5, and so on. This behavior differs from the SERIES TABLE descriptor, which requires that the values of `<min_value>` and `<max_value>` be aligned to zero with respect to the `<increment_by>` value.

This function returns a table with the following columns:

| **Column Name** | **Column Type** | **Description** |
| --- | --- | --- |
| SOURCE_PERIOD_START | PERIOD_TYPE | Specifies the start of the source period that generated this row. |
| SOURCE_PERIOD_END | PERIOD_TYPE | Specifies the end of the source period that generated this row. |
| GENERATED_PERIOD_START | PERIOD_TYPE | Displays the start of the period represented by this row, including the pe riod_start. This value is a closed interval at the start. |
| GENERATED_PERIOD_END | PERIOD_TYPE | Displays the end of the period represented by this row as an open interval. The period represented by this row consists of all times that are greater than or equal to the start and less than the end. |
| ELEMENT_NUMBER_IN_SOURCE_PERIOD | BIGINT | Specifies the element number of this period within its source interval. |
| ELEMENT_NUMBER_IN_GENERATED_SERIES | BIGINT | Specifies the element number within the whole result set. |
| FRACTION_OF_SOURCE_PERIOD | DOUBLE | Specifies the fraction of the length of the source period that this generated period covers. |
| FRACTION_OF_MIN_MAX_RANGE | DOUBLE | Specifies the fraction of the length of all generated periods that this generated period covers. |

## Examples

The fictitious example below illustrates how to use disaggregation when inserting data into a series table:

```sql
CREATE COLUMN TABLE sourceseries(id INT, ts TIMESTAMP, val DECIMAL(8,2))
   SERIES(SERIES KEY(id ) EQUIDISTANT INCREMENT BY INTERVAL 1 YEAR
   MINVALUE '1999-01-01'
   MAXVALUE '2003-01-01'
   PERIOD FOR SERIES (ts));

CREATE COLUMN TABLE targetseries(id INT, ts TIMESTAMP, val DECIMAL(8,2))
   SERIES(SERIES KEY(id ) EQUIDISTANT INCREMENT BY INTERVAL 3 MONTH
   MINVALUE '1999-01-01'
   MAXVALUE '2001-01-01'
   PERIOD FOR SERIES (ts));
INSERT INTO targetseries(id , ts, val)
   SELECT id, GENERATED_PERIOD_START AS ts, val * FRACTION_OF_SOURCE_PERIOD AS
val
   FROM SERIES_DISAGGREGATE(
      SERIES TABLE sourceseries, SERIES TABLE targetseries)
   SD JOIN sourceseries S ON source_period_start = ts ORDER BY id, ts;
```

The example below generates a series of dates ranging from 1999-01-01 to 2001-01-04:

```sql
SELECT * FROM SERIES_DISAGGREGATE_DATE
    ('INTERVAL 1 year', 'INTERVAL 3 MONTH', '1999-01-01', '2001-01-04' );
```

The following result is returned by the example above:

| **SOURCE_PERIOD_START** | **SOURCE_PERIOD_END** | **GENERATED_PERIOD_START** | **GENERATED_PERIOD_END** | **ELEMENT_NUMBER_IN_SOURCE_PERIOD** | **ELEMENT_NUMBER_IN_GENERATED_SERIES** | **FRACTION_OF_SOURCE_PERIOD** | **FRACTION_OF_MIN_MAX_RANGE** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Jan 1, 1999 | Jan 1, 2000 | Jan 1, 1999 | Apr 1, 1999 | 1 | 1 | 0.246575342 4657534 | 0.1231190150 4787962 |
| Jan 1, 1999 | Jan 1, 2000 | Apr 1, 1999 | Jul 1, 1999 | 1 | 2 | 0.249315068 4931507 | 0.124487004 10396717 |
| Jan 1, 1999 | Jan 1, 2000 | Jul 1, 1999 | Oct 1, 1999 | 1 | 3 | 0.252054794 52054796 | 0.125854993 16005472 |
| Jan 1, 1999 | Jan 1, 2000 | Oct 1, 1999 | Jan 1, 2000 | 1 | 4 | 0.252054794 52054796 | 0.125854993 16005472 |
| Jan 1, 2000 | Jan 1, 2001 | Jan 1, 2000 | Apr 1, 2000 | 2 | 5 | 0.248633879 78142076 | 0.124487004 10396717 |
| Jan 1, 2000 | Jan 1, 2001 | Apr 1, 2000 | Jul 1, 2000 | 2 | 6 | 0.248633879 78142076 | 0.124487004 10396717 |
| Jan 1, 2000 | Jan 1, 2001 | Jul 1, 2000 | Oct 1, 2000 | 2 | 7 | 0.251366120 21857924 | 0.125854993 16005472 |
| Jan 1, 2000 | Jan 1, 2001 | Oct 1, 2000 | Jan 1, 2001 | 2 | 8 | 0.251366120 21857924 | 0.125854993 16005472 |

The example below returns the same result set as the previous example:

```sql
CREATE COLUMN TABLE sourceseries(id  INT, ts TIMESTAMP, val DECIMAL(8,2))
    SERIES(SERIES KEY(id ) EQUIDISTANT INCREMENT BY INTERVAL 1 YEAR
        MINVALUE '1999-01-01'
        MAXVALUE '2003-01-01'
        PERIOD FOR SERIES (ts));
CREATE COLUMN TABLE targetseries(id  INT, ts TIMESTAMP, val DECIMAL(8,2))
    SERIES(SERIES KEY(id ) EQUIDISTANT INCREMENT BY INTERVAL 3 MONTH
        MINVALUE '1999-01-01'
        MAXVALUE '2001-01-01'
        PERIOD FOR SERIES (ts));
SELECT * from SERIES_DISAGGREGATE(
    SERIES TABLE sourceseries, SERIES TABLE targetseries);
```

The most restrictive values of the min/max in the series table references are used.

The example below illustrates how to create a series table and perform a horizontal disaggregation:

```sql
CREATE COLUMN TABLE testdata AS (
     SELECT g.*, CAST(RAND() * 10 AS DECIMAL(5, 2)) AS val
     FROM SERIES_GENERATE_DECIMAL(1,0,10000) g);
 SELECT s.ELEMENT_NUMBER, s.val,
     g.ELEMENT_NUMBER_IN_GENERATED_SERIES,
     s.val * g.FRACTION_OF_SOURCE_PERIOD AS DA
     FROM testdata AS s
         LEFT JOIN SERIES_DISAGGREGATE_DECIMAL(1, 0.5, 0, 10000) g
             ON s.GENERATED_PERIOD_START = g.SOURCE_PERIOD_START;
```

The example above returns a result similar to the following:

| **ELEMENT_NUMBER** | **VAL** | **ELEMENT_NUMBER_IN_GENERATED_SERIES** | **DA** |
| --- | --- | --- | --- |
| 1 | 2.21 | 1 | 1.105 |
| 1 | 2.21 | 2 | 1.105 |
| 2 | 5.52 | 3 | 2.76 |
| 2 | 5.52 | 4 | 2.76 |
| 3 | 2.35 | 5 | 1.175 |
| 3 | 2.35 | 6 | 1.175 |
| ... |   |   |   |
