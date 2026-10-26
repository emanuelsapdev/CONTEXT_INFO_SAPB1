# 5.2.37 REFRESH STATISTICS Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1365–1369

Refreshes data statistic objects that the query optimizer uses to make better decisions for query plans.

## Syntax

```sql
REFRESH STATISTICS { <data_statistics_name>[,<data_statistics_name>[,...] ]
   | ON <data_sources> [ [HAVING] <match_properties> ] };
```

## Syntax Element

#### data_statistics_name

Specifies the name of the data statistics object.

```sql
<data_statistics_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

#### data_sources

Specifies the data source(s) of the data statistics objects.

```sql
<data_sources> ::=
<table_name> [ ( <column_name>[, <column_name>[,...] ] )
[ FOR { DEFAULT | EXTENDED } STORAGE ] [ <match_type> ]
```

##### table_name

Specifies the table on which the data statistics are defined.

```sql
<table_name> ::= [<schema_name>.]<identifier>
```

##### column_name

Specifies the column for which the data statistics are defined.

```sql
<column_name> ::= <identifier>
```

If no `<column_name>` is specified, then all statistics for the table that match the specified properties are altered, including table-wide statistics (RECORD COUNT).

##### FOR {DEFAULT | EXTENDED} STORAGE

The STORAGE clause can be specified only for multistore tables. Specify DEFAULT when the data statistics object is created on the column store part. Specify EXTENDED STORAGE when the data statistics object is created on the extended storage part. If you do not specify anything, then two data statistics objects are created, one on the extended storage part and one on the column storage part.

Statistics of some types can only be created on one storage class partition; for example, SKETCH on HANA column store partitions, and RECORD COUNT on extended storage partitions. Attempting to create such objects on a multistore table without specifying storage type returns an error.

You can implement different statistics types for different storage classes, and create statistics to address specific performance problems that only affect the query plan for one of the storage classes of the table. The statement returns an error if no partitions of the specified storage type exist.

c

##### match_type

Controls which data statistics objects to match to `<data_sources>`.

```sql
<match_type> ::= EXACT | CASCADE
```

If `<match_type>` is not specified, then any data statistics object(s) that reference all or some of the columns, but no other columns specified in `<data_sources>` are refreshed.

Specify EXACT to refresh data statistics objects that precisely match `<data_sources>` (including column order).

Specify CASCADE to refresh data statistics objects that reference at least one column in `<data_sources>`.

Use this table to understand how matching is performed based on `<match_type>` when `<data_sources>` is T(A, B, C):

| **Match type** | **Example matches** | **Example non-matches** |
| --- | --- | --- |
| (not specified) | T(A,C)<br>T(C)<br>T(B,A) | T(A,X) - because T(X) is not a column in `<data_sources>`. |
| EXACT | T(A,B,C) | T(B,A,C) - because the column order is different than the column order of `<data_sources>`.<br>T(A)- because it does not contain the exact same columns and column order of `<data_sources>`. |
|   |   | T(X,A,B,C) - because T.(X) is not a column in `<data_sources>`. |
| CASCADE | T(A,C)<br>T(C)<br>T(B,A)<br>T(A,B,C)<br>T(A,X)<br>T(B,C)<br>T(A)<br>T(C,B,A,X) | T(X) - because it does not contain any columns that match the columns in `<data_sources>`. |

#### match_properties

Specifies properties to use for matching when selecting data statistics.

```sql
<match_properties> ::= <match_property>[...]
<match_property> ::=
 TYPE <data_statistics_type>  | REFRESH TYPE <refresh_type_filter>
```

If TYPE is not specified, then all data statistics objects of any type on the specified data sources are altered (ALL). For descriptions of the supported data statistics types see the CREATE STATISTICS Statement (Multistore Table) topic.

##### data_statistics_type

Specifies the type of data statistics objects to match when selecting the data statistics.

```sql
<data_statistics_type> := TYPE <type_name>
<type_name> ::=
 HISTOGRAM
 | SIMPLE
 | TOPK
 | SKETCH
 | SAMPLE
 | RECORD COUNT
 | ALL
```

##### refresh_type_filter

Specifies the refresh strategy to match in the data statistics objects when selecting data statistics. ALL is the default.

```sql
<refresh_type_filter> ::= AUTO | MANUAL | ALL
```

## Permissions

One of the following is true:

- You own the object you are refreshing statistics on.
- You have the ALTER privilege on the object you are refreshing statistics on.

## Description

The REFRESH STATISTICS statement rebuilds data statistics objects that approximate the specified `<data_sources>`.

The REFRESH STATISTICS statement only affects enabled data statistics objects.

See the CREATE STATISTICS [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) Statement for descriptions of the supported data statistic types (`<data_statistics_type>`).

For more information on schema names and identifiers, see Identifiers [→](../../4-SQL-Reference/4.01-Introduction-to-SQL.md).

## Example

The following example refreshes the HISTOGRAM on column T(X), where T is a virtual table:

```sql
REFRESH STATISTICS ON MYSCHEMA.T(X) TYPE HISTOGRAM;
```

The following example refreshes any SKETCH with `<data_sources>` containing one or more of columns T(X), T(Y), or T(Z) (only) in any order

```sql
REFRESH STATISTICS ON MYSCHEMA.T(X, Y, Z) TYPE SKETCH;
```

The following example refreshes the database statistics object named HISTOGRAM_T_X:

```sql
REFRESH STATISTICS MYSCHEMA.HISTOGRAM_T_X;
```

The following example refreshes any data statistic object with `<data_sources>` defined as `T(A,B)`. HISTOGRAMS on T(A) and on T(B) would not be affected.

```sql
REFRESH STATISTICS ON MYSCHEMA.T(A, B) EXACT;
```

The following example refreshes any data statistic object that has table columns T(A), T(B), or T(C) listed in `<data_sources>`:

```sql
REFRESH STATISTICS ON MYSCHEMA.T(A, B, C) CASCADE TYPE ALL;
```

The following example manually refreshes the HISTOGRAM MYSCHEMA.MYHISTOGRAM on table column MYSCHEMA.T(a):

```sql
REFRESH STATISTICS MYSCHEMA.MYHISTOGRAM ON MYSCHEMA.T(a) TYPE HISTOGRAM REFRESH
TYPE MANUAL;
```

The following example refreshes the row count on table T:

```sql
REFRESH STATISTICS ON T TYPE RECORD COUNT;
```

## Related Information

CREATE STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md) ALTER STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](ALTER-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md) DROP STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](DROP-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md) M_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md) M_SYSTEM_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md)
