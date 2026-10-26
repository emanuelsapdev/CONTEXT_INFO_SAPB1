# 5.2.24 DROP STATISTICS Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1317–1319

Drops userdefined data statistics objects that the query optimizer uses to make decisions for query plans.

## Syntax

```sql
 DROP STATISTICS { <data_statistics_name>[,<data_statistics_name>[,...] ]
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
<table_name> [ ( <column_name>[, <column_name>[,...] ] ) [ <match_type> ]
```

Specifies the data source(s) of the data statistics objects.

```sql
<data_sources> ::=
<table_name> [ ( <column_name>[, <column_name>[,...] ] ) [ <match_type> ]
```

#### match_properties

Specifies properties to use for matching when selecting data statistics.

```sql
<match_properties> ::= <match_property>[...]
<match_property> ::=
 TYPE <data_statistics_type>  | REFRESH TYPE <refresh_type_filter>
```

If TYPE is not specified, then all data statistics objects of any type on the specified data sources are refreshed (ALL). For descriptions of the supported data statistics types see the CREATE STATISTICS Statement (Extended Store Table) topic.

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

- You own the table you are creating statistics on.
- You have the ALTER privilege on the object you are dropping.

## Example

Drop all statistics over `T(COL2)` extended storage partitions.

```sql
DROP STATISTICS ON MYSCHEMA.T(COL2) FOR EXTENDED STORAGE
```

Drop data statistics objects with the name "HISTOGRAM_T_X" or "HISTOGRAM_T_Y"".

```sql
DROP STATISTICS "HISTOGRAM_T_X","HISTOGRAM_T_Y";
```

Drop the HISTOGRAMS on table columns T(A), T(B), and T(C):

```sql
DROP STATISTICS ON MYSCHEMA.T(A,B,C) TYPE HISTOGRAM;
```

## Related Information

CREATE STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](CREATE-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) ALTER STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](ALTER-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) REFRESH STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](REFRESH-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) M_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md) M_SYSTEM_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md)
