# 4.9.1.12 ADD_WORKDAYS Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 94–98

Computes a date by adding a number of workdays to a starting date.

## Syntax

```sql
ADD_WORKDAYS(<factory_calendar_id>, <start_date>, <workdays> [, <source_schema>])
```

## Syntax Elements

#### factory_calendar_id

The ID of a factory calendar in the factory calendar table TFACS.

```sql
<factory_calendar_id> ::= <string_literal>
```

#### start_date

The start date that the work days will be added to. This parameter can be either a DATE type or a date format string (for example '20140101' or '2014-01-01').

```sql
<start_date> ::= <string_literal> | <date>
```

#### workdays

The number of working days to be added to the starting date.

```sql
<workdays> ::= <signed_integer>
```

#### source_schema

The schema where the factory calendar table TFACS is located.

```sql
<source_schema> ::= <string_literal>
```

This parameter can be omitted if the schema of the TFACS is the same as the current schema.

## Return Type

DATE

## Description

Computes a date by adding a number of workdays to a starting date.

In order to use the ADD_WORKDAYS function, a factory calendar table TFACS must be available in the SAP HANA database. In SAP BW, SAP CRM, and SAP ERP systems running on an SAP HANA database, the table TFACS is located in the ABAP schema `SAP<SID>`. For other SAP HANA databases, the TFACS table can be replicated from an SAP Business Suite system.

When `<workdays>` is positive, the resulting calculated date is the next working day after the period defined by the number of `<workdays>`.

When `<workdays>` is negative, the resulting calculated date is the previous working day before the period defined by the number of `<workdays>`.

## Examples

For the examples below, assume that the following TFACS table for the month of January 2014 is used. However, the content in your TFACS table may vary.

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

The following example returns the value `10.01.2014`:

```sql
SELECT ADD_WORKDAYS('01', '2014-01-09', 1, 'FCTEST') "result date" FROM DUMMY;
```

From this result you can see that a single workday was added to the start date of the ninth, with the result being the tenth

The following example returns the value `09.01.2014`:

```sql
SELECT ADD_WORKDAYS('01', '2014-01-10', -1, 'FCTEST') "result date" FROM DUMMY;
```

From this result you can see that the tenth was considered to be a working day, producing a final result of the ninth.

The following example takes positive workday input and returns the value `20.01.2014`, a result after a non-working weekend period:

```sql
SELECT ADD_WORKDAYS('01', '2014-01-17', 1, 'FCTEST') "result date" FROM DUMMY;
```

From this result you can see that a single workday was added to the start date of the 17th. This produced the resulting day of the 20th, which allowed for the non-working period of the weekend.

The following example takes negative workday input and returns the value `17.01.2014`, showing a result after a non-working weekend period:

```sql
SELECT ADD_WORKDAYS('01', '2014-01-20', -1, 'FCTEST') "result date" FROM DUMMY;
```

From this result you can see that the 20th was considered to be the working day, producing a result of the 17th. This result takes into account the non-working time of the weekend.

The following complex example returns the value `27.01.2014`:

```sql
SELECT ADD_WORKDAYS('01', '2014-01-01', 16, 'FCTEST') "result date" FROM DUMMY;
```

The statement above adds 16 working days to the start date of the first. The system takes into account the weekends (4th, 5th, 11th, 12th, 18th and 19th) and public holidays (1st and 6th) during the working period, which gives the last working day as the 24th. The system then returns the next possible working day after this, which is the 27th.

The following example uses a table for input and returns the values `4.02.2014`, `14.05.2014`, `05.08.2014`, and `30.10.2014`:

```sql
CREATE SCHEMA SAPABC;
 SET SCHEMA "SAPABC";
 CREATE ROW TABLE MY_DATES (FCID NVARCHAR(2), STARTDATE DATE, DURATION INTEGER);
 INSERT INTO MY_DATES VALUES ('01', '2014-01-01', 30);
 INSERT INTO MY_DATES VALUES ('01', '2014-04-01', 28);
 INSERT INTO MY_DATES VALUES ('01', '2014-07-01', 25);
 INSERT INTO MY_DATES VALUES ('01', '2014-10-01', 20);
SELECT ADD_WORKDAYS(FCID, STARTDATE, DURATION) "shipment date" FROM MY_DATES;
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) WORKDAYS_BETWEEN Function (Datetime) [→](WORKDAYS_BETWEEN-Function-Datetime.md)
