# 4.9.1.233 WORKDAYS_BETWEEN Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 385–389

Computes the number of workdays between a specified start date and a specified end date.

## Syntax

```sql
WORKDAYS_BETWEEN(<factory_calendar_id>, <start_date>, <end_date> [,
<source_schema>])
```

## Syntax Elements

#### factory_calendar_id

Specifies the ID of a factory calendar in the factory calendar table TFACS.

```sql
<factory_calendar_id> ::= <string_literal>
```

#### start_date

Specifies the start date. You can use either a type or a date format string (for example '20140101' or '2014-01-01') for this parameter.

```sql
<start_date> ::= <string_literal> | <>
```

#### end_date

Specifies the end date. You can use either a type or a date format string (for example '20140101' or '2014-01-01') for this parameter.

```sql
<end_date> ::= <string_literal> | <>
```

#### source_schema

Specifies the schema where the factory calendar table TFACS is located. This parameter can be omitted if the schema of the TFACS is the same as the current schema.

```sql
<source_schema> ::= <string_literal>
```

## Return Type

INTEGER

## Description

In order to use the WORKDAYS_BETWEEN function, a factory calendar table TFACS must be available in the SAP HANA database. In SAP BW, SAP CRM, and SAP ERP systems running on an SAP HANA database, the table TFACS is located in the ABAP schema `SAP<SID>`. For other SAP HANA databases, the TFACS table can be replicated from an SAP Business Suite system.

Computes the number of workdays between a `<start_date>` and an `<end_date>`.

Computations are done with respect to a factory calendar with ID `<factory_calendar_id>`.

If the `<start_date>` is earlier than or equal to the `<end_date>`, then the number of working days in the period starting at the `<start_date>` and ending at the `<end_date>` is returned. The returned number of days includes the day of the `<start_date>`, but excludes the day of the `<end_date>`.

If the `<start_date>` is after the `<end_date>`, then a negative number of workdays in the period starting at the `<end_date>` and ending at the `<start_date>` is returned. The returned number of days includes the day of the `<end_date>`, but excludes the day of the `<start_date>`.

## Examples

The examples below assume that the following TFACS table for the month of January 2014 is used. The content in your TFACS may vary.

| **TFACS bitfield** | **Day of the month** | **Reason for not working** |
| --- | --- | --- |
| 0 | 1 | Public Holiday |
| 1 | 2 |   |
| 1 | 3 |   |
| 0 | 4 | Weekend |
| 0 | 5 | Weekend |
| 0 | 6 | Public Holiday |
| 1 | 7 |   |
| 1 | 8 |   |
| 1 | 9 |   |
| 1 | 10 |   |
| 0 | 11 | Weekend |
| 0 | 12 | Weekend |
| 1 | 13 |   |
| 1 | 14 |   |
| 1 | 15 |   |
| 1 | 16 |   |
| 1 | 17 |   |
| 0 | 18 | Weekend |
| 0 | 19 | Weekend |
| 1 | 20 |   |
| 1 | 21 |   |
| 1 | 22 |   |
| 1 | 23 |   |
| 1 | 24 |   |
| 0 | 25 | Weekend |
| 0 | 26 | Weekend |
| 1 | 27 |   |
| 1 | 28 |   |
| 1 | 29 |   |
| 1 | 30 |   |
| 1 | 31 |   |

### Example 1 - Simple start date after end date.

The following fictitious example returns the value `1` for work days between the two specified dates:

```sql
SELECT WORKDAYS_BETWEEN('01', '2014-01-09', '2014-01-10' , 'FCTEST') "workdays"
FROM DUMMY;
```

A single workday has been computed starting on the 9th and finishing on, but not including, the 10th.

### Example 2 - Simple end date before the start date.

The following fictitious example returns the value `-1` for work days between the two specified dates:

```sql
SELECT WORKDAYS_BETWEEN('01', '2014-01-10', '2014-01-09' , 'FCTEST') "workdays"
FROM DUMMY;
```

A single workday has been computed on the 10th, excluding the day of the 9th.

### Example 3 - Dates including a non-working weekend period.

The following fictitious example returns the value `1` for work days between the two specified dates:

```sql
SELECT WORKDAYS_BETWEEN('01', '2014-01-17', '2014-01-20', 'FCTEST') "workdays"
FROM DUMMY;
```

The single workday has been computed on the 17th. The weekend period and the end date day are excluded.

### Example 4 - End date before start date including a non-working weekend period.

The following fictitious example returns the value `-1` for work days between the two specified dates:

```sql
SELECT WORKDAYS_BETWEEN('01', '2014-01-20', '2014-01-17', 'FCTEST') "workdays"
FROM DUMMY;
```

The single workday has been computed on the 20th. The weekend period and the start date day are excluded.

### Example 5 - Complex example

The following fictitious example returns the value `20` for work days between the two specified dates:

```sql
SELECT WORKDAYS_BETWEEN('01', '2014-01-01', '2014-01-31', 'FCTEST') "workdays"
FROM DUMMY;
```

The system takes into account the weekends (4th, 5th, 11th, 12th, 18th, 19th, 25th and 26th) and public holidays (1st and 6th) and excludes them from the working period.

### Example 6 - Using a table for input

The following fictitious example returns the values `30`, `28`, `25`, and `20`:

```sql
SET SCHEMA "SAPABC";
 CREATE ROW TABLE MY_DATES (FCID NVARCHAR(2), STARTDATE , ENDDATE );
 INSERT INTO MY_DATES VALUES ('01', '2014-01-01', '2014-02-14');
 INSERT INTO MY_DATES VALUES ('01', '2014-04-01', '2014-05-14');
 INSERT INTO MY_DATES VALUES ('01', '2014-07-01', '2014-08-05');
 INSERT INTO MY_DATES VALUES ('01', '2014-10-01', '2014-10-30');
 SELECT WORKDAYS_BETWEEN(FCID, STARTDATE, ENDDATE) "production duration" FROM
MY_DATES;
```

## Related Information

Data Types [→](../../4.03-Data-Types/README.md) Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md)
