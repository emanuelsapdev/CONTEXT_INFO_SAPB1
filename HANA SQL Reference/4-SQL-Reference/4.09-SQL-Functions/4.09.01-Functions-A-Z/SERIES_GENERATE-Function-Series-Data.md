# 4.9.1.171 SERIES_GENERATE Function (Series Data)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 317–321

Generates a complete series table based on the specified series definition.

## Syntax

```sql
SERIES_GENERATE( SERIES TABLE <table_name> [, <min_value> [, <max_value> ]] )
| SERIES_GENERATE_<generation_spec>
```

## Syntax Elements

#### generation_spec

A version of the function that specifies the data type for the generated parameters.

```sql
<generation_spec> ::= <data_type> <generate_parameters>
```

##### data_type

The type of data to use for the series.

```sql
<data_type> ::=
TINYINT
 | SMALLINT
 | INTEGER
 | BIGINT
 | SMALLDECIMAL
 | DECIMAL
 | TIME
 | DATE
 | SECONDDATE
 | TIMESTAMP
```

##### generate_parameters

Specifies the increment value used to generate parameters.

```sql
<generate_parameters> ::=
( <increment_by>, <min_value>, <max_value> )
<increment_by> ::= { <numeric_literal> | INTERVAL <date_literal> }
```

`<increment_by>` defines the period size. If the period type is a DATETIME, then the number needs to be preceded by INTERVAL followed by a time unit, such as YEAR, MONTH, DAY, HOUR, MINUTE, or SECOND.

#### table_name

Specifies the name of the series table containing the series definition.

```sql
<table_name> ::= <identifier>
```

#### min_value

Sets the minimum value of the generated series. This overrides the value defined in the series table, if one is specified.

```sql
<min_value> ::= <numeric_literal> | <date_literal>
```

#### max_value

Sets the maximum value of the generated series. This overrides the value defined in the series table, if one is specified.

```sql
<max_value> ::= <numeric_literal> | <date_literal>
```

## Description

The range is defined by the `<min_value>` and `<max_value>` parameters, and the period size is defined by the `<increment_by>` parameter. The `<min_value>` and `<max_value>` specifies the increment value used to generate values must be aligned with the `<increment_by>` value. The generated intervals have closed-open semantics, so the GENERATED_PERIOD_END does not belong to the interval.

Alternatively, the name of an existing series table can be defined with the SERIES TABLE syntax. In this case, the values of the increment, `<min_value>`, and `<max_value>` are retrieved from the series definition associated with that table. The `<min_value>` and `<max_value>` can still be manually specified if a SERIES TABLE reference is supplied; the manually specified values override those in the series table definition. The generic form of the procedure that takes at least one SERIES TABLE reference does not have to use the name of the series data type in the procedure name.

The `<min_value>` parameter for the numeric versions of this function does not need to be aligned to numeric zero with respect to the `<increment_by>` value. You can specify a source increment of 2 and a `<min_value>` of 1, which results in a source series of 1, 3, 5, and so on. This behavior differs from the SERIES TABLE descriptor, which requires that the values of `<min_value>` and `<max_value>` be aligned to zero with respect to the `<increment_by>` value.

This function returns a table with the following columns:

| **Column Name** | **Column Type** | **Description** |
| --- | --- | --- |
| GENERATED_PERIOD_START | PERIOD_TYPE | Specifies the start of the period represented by this row, including the `<period_start>` parameter. This is a closed interval at the start. |
| GENERATED_PERIOD_END | PERIOD_TYPE | Specifies the end of the period represented by this row as an open interval. The period represented by this row consists of all times that are greater than or equal to the start, and less than the end. |
| ELEMENT_NUMBER | BIGINT | Specifies the element number of this period within the generated series. This value is equivalent to the result set's row number. |

FRACTION_OF_MIN_MAX_RANGE DOUBLE Specifies the ratio of the length of this

period to the length of all periods gener ated by this function. The sum of FRAC TION_OF_MIN_MAX_RANGE is close to 1.0. For fixed size intervals, such as 1

|   |   | DAY, the value is computed as 1/ numPeriods. For nonfixed size intervals, such as MONTH and YEAR, the value is computed individually for each row, which is calculated by the time span of the interval divided by the time span of the entire result. |
| --- | --- | --- |

## Examples

The example below illustrates how to generate a series table:

```sql
CREATE COLUMN TABLE MyTab (
    profile_id INT,
    ts TIMESTAMP,
    consumption DECIMAL(4,3))
    SERIES(
        SERIES KEY(profile_id)
        PERIOD FOR SERIES(ts)
        EQUIDISTANT INCREMENT BY INTERVAL 1 HOUR MISSING ELEMENTS ALLOWED
        MINVALUE '2010-01-01'
        MAXVALUE '2015-01-01');
SELECT * FROM SERIES_GENERATE_TIMESTAMP(SERIES TABLE MyTab);
```

The example below generates a series of decimals ranging from 0 to 10 that increments by 2.5:

```sql
SELECT * FROM SERIES_GENERATE_DECIMAL(2.5, 0, 10);
```

The following result is returned by the example above:

| **GENERATED_PERIOD_START** | **GENERATED_PERIOD_END** | **ELEMENT_NUMBER** | **FRACTION_OF_MIN_MAX_RANGE** |
| --- | --- | --- | --- |
| 0 | 2.5 | 1 | 0.25 |
| 2.5 | 5 | 2 | 0.25 |
| 5 | 7.5 | 3 | 0.25 |
| 7.5 | 10 | 4 | 0.25 |

The example below generates a series of integers ranging from 1 to 5 that increments by 2:

```sql
SELECT * FROM SERIES_GENERATE_INTEGER(2, 1, 5);
```

The following result is returned by the example above:

| **GENERATED_PERIOD_START** | **GENERATED_PERIOD_END** | **ELEMENT_NUMBER** | **FRACTION_OF_MIN_MAX_RANGE** |
| --- | --- | --- | --- |
| 1 | 3 | 1 | 0.5 |
| 3 | 5 | 2 | 0.5 |

The example below illustrates an equivalent way of writing the previous example using the SERIES TABLE syntax and a series table named MySeries:

```sql
CREATE COLUMN TABLE MySeries(id  INTEGER, pos INTEGER)
   SERIES(SERIES KEY(id) EQUIDISTANT INCREMENT BY 1
   MINVALUE 1 MAXVALUE 5 PERIOD FOR SERIES(pos));
SELECT * FROM SERIES_GENERATE(SERIES TABLE MySeries);
```

The example below generates a series of timestamps ranging from 1999-01-01 to 1999-01-02 that increments by 30 second intervals:

```sql
SELECT * FROM SERIES_GENERATE_TIMESTAMP(
    'INTERVAL 30 SECOND', '1999-01-01', '1999-01-02');
```

The following result is returned by the example above:

| **GENERATED_PERIOD_START** | **GENERATED_PERIOD_END** | **ELEMENT_NUMBER** | **FRACTION_OF_MIN_MAX_RANGE** |
| --- | --- | --- | --- |
| Jan 1, 1999 12:00:00.0 AM | Jan 1, 1999 12:00:30.0 AM | 1 | 0.00034722222222222224 |
| Jan 1, 1999 12:00:30.0 AM | Jan 1, 1999 12:01:00.0 AM | 2 | 0.00034722222222222224 |
| Jan 1, 1999 12:01:00.0 AM | Jan 1, 1999 12:01:30.0 AM | 3 | 0.00034722222222222224 |
| Jan 1, 1999 12:01:30.0 AM | Jan 1, 1999 12:02:00.0 AM | 4 | 0.00034722222222222224 |
| ... |   |   |   |
| Jan 1, 1999 11:59:00.0 PM | Jan 1, 1999 11:59:30.0 PM | 2,879 | 0.00034722222222222224 |
| Jan 1, 1999 11:59:30.0 PM | Jan 2, 1999 12:00:00.0 AM | 2,880 | 0.00034722222222222224 |

The example below illustrates how to implement a series of timestamps ranging from 1999-01-01 to 1999-01-02 that increments by 30 second intervals using a series table named testseries:

```sql
CREATE COLUMN TABLE testseries(id  INT, ts TIMESTAMP, val DOUBLE)
    SERIES (SERIES KEY(id) EQUIDISTANT INCREMENT BY INTERVAL 30 SECOND
        MINVALUE '1999-01-01'  MAXVALUE '1999-01-02'  PERIOD FOR SERIES (ts));
SELECT * FROM SERIES_GENERATE(SERIES TABLE testseries);
```

The example below illustrates how to generate a date series table with closed-closed semantics where the period end belongs to the interval:

```sql
SELECT GENERATED_PERIOD_START AS from_date,
    ADD_DAYS(GENERATED_PERIOD_END, -1) AS to_date
    FROM SERIES_GENERATE_DATE('INTERVAL 1 MONTH', '2010-01-01', '2011-01-01')
```
