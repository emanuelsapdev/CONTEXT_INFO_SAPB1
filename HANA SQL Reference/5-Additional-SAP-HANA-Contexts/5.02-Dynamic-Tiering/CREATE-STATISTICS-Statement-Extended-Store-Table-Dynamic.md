# 5.2.19 CREATE STATISTICS Statement (Extended Store Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1285–1290

Creates data statistic objects that allow the query optimizer to make better decisions for query plans.

## Syntax

```sql
CREATE STATISTICS [<data_statistics_name>] ON <data_sources>
[ <data_statistics_type> ]
[ <data_statistics_properties> ]
[ <initial_refresh> ];
```

## Syntax Element

#### data_statistics_name

Specifies a unique name for the data statistics object.

```sql
<data_statistics_name> ::= [ <schema_name>.]<identifier>
```

`<data_statistics_name>` is only allowed when the result of the creation is a single data statistics object. The number of data statistics objects created by CREATE STATISTICS is determined by the combination of `<data_statistics_type>` and the number of columns specified in `<data_sources>`.

```sql
<schema_name> ::= <identifier>
```

`<schema_name>` must be the same as specified for data source.

#### data_sources

Specifies the data sources you want to create data statistics objects for.

```sql
<data_sources> ::=
<table_name> [ ( <column_name>[, <column_name>[,...] ] )
```

For RECORD COUNT data statistics objects, you cannot specify columns as part of data_sources.

##### table_name

Specifies the table name you want to create statistics on.

```sql
<table_name> ::= [<schema_name>.]<identifier>
```

If you specify a data statistics name, then you can only specify one data source.

##### column_name

Specifies the column for which the data statistics are defined.

```sql
<column_name> ::= <identifier>
```

If no `<column_name>` is specified, then all statistics for the table that match the specified properties are altered, including table-wide statistics (RECORD COUNT).

Specifying multiple columns when creating single-column data statistics is equivalent to executing a matching CREATE STATISTICS statement for each column individually. If you specify a data statistics name, then you can only specify one data source.

#### data_statistics_type

Specifies the type of data statistics object to create.

```sql
<data_statistics_type> := TYPE <type_name>
<type_name> ::=
HISTOGRAM
 | SIMPLE
 | TOPK
 | SKETCH
 | SAMPLE
 | RECORD COUNT
```

A data source can have only one data statistics object of a certain type. For example, column A of table T can have one data statistics object of type HISTOGRAM and one of type SIMPLE. If the TYPE clause is not specified, then the default is HISTOGRAM. Some data statistic types may not be appropriate for a given data source.

##### HISTOGRAM

Creates a data statistics object that helps the query optimizer estimate the data distribution in a single-column data source. If you specify multiple columns in `<data_sources>`, then multiple data statistics objects (HISTOGRAM) are created--one per column specified.

##### SIMPLE

Creates a data statistics object that helps the query optimizer calculate basic statistics, such as min, max, null count, count, and distinct count for a single-column data source. If you specify multiple columns in `<data_sources>`, then multiple data statistics objects are created--one per column specified.

##### TOPK

Creates a data statistics object that helps the query optimizer identify the highest-frequency values in a table data source. If you specify multiple columns in `<data_sources>`, then multiple data statistics objects are created--one per column specified.

##### SKETCH

Creates a data statistics object that helps the query optimizer estimate the number of distinct values in the data source. A data statistics object is created for the specified `<table_name>(<column- name>,...)`, which approximates the number of distinct tuples in the projection of the table on the set of specified columns.

##### SAMPLE

Creates a sample of data from `<data_source>` that the SQL optimizer can use during optimization. When beneficial, the SQL optimizer generates system SAMPLE data statistics objects automatically on column and row store tables. However, this behavior can incur a cost to performance. You can avoid this cost by creating SAMPLE data statistics objects explicitly (in advance). Creating them explicitly is especially useful in situations where sampling live table data is expensive (for example, very large tables).

##### RECORD COUNT

Creates a data statistics object that helps the query optimizer calculate the number of records (rows) in a table data source. The RECORD COUNT type is a table-wide statistic. You do not specify columns in `<data_sources>` when creating a RECORD COUNT data statistics object. When beneficial, the SQL optimizer maintains system RECORD COUNT data statistics objects automatically on column and row store tables.

#### data_statistics_properties

Specifies the properties of the data statistics objects.

```sql
<data_statistics_properties> ::=
 <data_statistics_property>[,<data_statistics_property>[,...].]
<data_statistics_property> ::=
 | REFRESH TYPE <refresh_type>
 | ENABLE <on_off>
 | BUCKETS <unsigned_integer>
 | {MEMORY <memory_bytes> | | MEMORY PERCENT <memory_percentage> }
 | CONSTRAINT <constraint_param>
```

Restrictions to which properties apply to which statistic types are noted in the property descriptions.

##### REFRESH TYPE refresh_type

Specifies the strategy for the data statistics object.

```sql
<refresh_type> ::= { AUTO | MANUAL | DEFAULT }
```

AUTO specifies that the data statistics object is refreshed automatically when underlying data changes. AUTO is only supported on column store, extended store, and multistore tables.

MANUAL specifies that the database statistics object is not refreshed until a rebuild is explicitly requested by a REFRESH STATISTICS statement.

DEFAULT specifies that the database server decides the best refresh strategy based on the data source. For example, for data statistics objects on column store data sources, the database server applies AUTO for the default.

REFRESH TYPE only affects data statistics objects that are enabled.

##### ENABLE on_off

Controls whether the optimizer uses the data statistics object.

```sql
<on_off> ::= { ON | OFF }
```

ENABLE ON enables the optimizer to see the data statistics object. The data statistics object must be populated with data for the optimizer to use it. ENABLE ON specified with NO INITIAL REFRESH returns an error.

ENABLE ON is the default behavior.

ENABLE OFF disables the use of the data statistics object by the optimizer and prevents the ability to refresh the data statistics object. Data statistics objects that are not enabled can still be dropped. To make a data statistics object with ENABLE OFF accessible to the optimizer, execute an ALTER STATISTICS...ENABLE ON statement.

##### BUCKETS unsigned_integer

The BUCKETS property is only for use with TYPE HISTOGRAM or TOPK. For HISTOGRAM, BUCKETS specifies the maximum number of data buckets in the HISTOGRAM. For TOPK, BUCKETS specifies the K value.

The default is automatically determined by the data statistics building algorithm in use.

If a very small number of buckets is specified for a QOPTIMAL HISTOGRAM, then the algorithm may fail to build a valid HISTOGRAM either during the first build or during a subsequent refresh executed for the HISTOGRAM.

For column store, extended store, and multistore tables only, if a very small number of buckets is specified for a QOPTIMAL HISTOGRAM, then the algorithm may fail to build a valid HISTOGRAM either during the first build or during a subsequent refresh executed for the HISTOGRAM.

##### MEMORY memory_bytes

Specifies the maximum amount of memory, in bytes, to use for QOPTIMAL HISTOGRAMS.

```sql
<memory_bytes> ::= <unsigned_integer>
```

The MEMORY parameter limits the memory for QOPTIMAL HISTOGRAMS. MEMORY applies only to the QOPTIMAL HISTOGRAM algorithm. Small values for MEMORY may cause the QOPTIMAL HISTOGRAM algorithm to pick a small number of buckets, which can lead to failures building or refreshing the HISTOGRAM.

##### MEMORY PERCENT memory_percentage

Specifies the maximum amount of memory to use for the data statistics object, expressed as a percentage of the space used by the data source.

```sql
<memory_percentage> ::= <unsigned_integer>
```

HISTOGRAMS can use a large amount of memory for some data sources. `<memory_percentage>` represents the maximum amount of memory that can be used for the data statistics object. For example, if a data source is a table column that uses 100 MB of memory, and `<memory_percentage>` is 5, then the data statistics object for this column can use, at most, 5 MB for its in-memory representation.

The default is automatically determined by the HISTOGRAM algorithm in use. Small values for MEMORY PERCENT may cause the QOPTIMAL HISTOGRAM algorithm to pick a small number of buckets, which can lead to failures building or refreshing the HISTOGRAM.

##### CONSTRAINT

Specifies constraints to use for the specified for type HISTOGRAM.

```sql
CONSTRAINT <constraint_param>
<constraint_param> ::= MAXDIFF
```

Histogram sizing restrictions (BUCKETS, MEMORY, and MEMORY PERCENT) are applied per HISTOGRAM.

A non-default CONSTRAINT for a HISTOGRAM returns an error.

#### initial_refresh

Specifies whether to populate the data statistics object with data after creation.

```sql
<initial_refresh> ::= [ NO ] INITIAL REFRESH
```

##### INITIAL REFRESH

Creates the definition of the data statistics object and populates it with data. The default behavior is INITIAL REFRESH.

##### NO INITIAL REFRESH

Creates the definition of the data statistics object, but does not populate it with data.

Use NO INITIAL REFRESH when you want to change the underlying data before refreshing the data statistics object.

You cannot specify NO INITIAL REFRESH if ENABLE OFF is not specified.

## Permissions

One of the following is true with regards to required permission:

- You own the table you are creating statistics on.
- You have the ALTER privilege on the object you are creating statistics on.

## Description

CREATE STATISTICS statement creates data statistics objects that approximate the specified `<data_sources>`. Data statistics objects are used to estimate the properties of the data without directly accessing the data itself. This can be useful during query optimization, query execution, and so on.

## Examples

You create a MAXDIFF HISTOGRAM with a maximum of 1000 buckets on the column T(X), where T is an extended storage table:

```sql
CREATE STATISTICS ON MYSYSTEM.T(X) TYPE HISTOGRAM BUCKETS 1000
```

You create a MAXDIFF HISTOGRAM on the column T(X), where T is an extended store table. The BUCKETS value that is not specified is determined by the HISTOGRAM build algorithm. You specify the name of this data as "HISTOGRAM_T_X":

```sql
CREATE STATISTICS "HISTOGRAM_T_X" ON MYSYSTEM.T(X) TYPE HISTOGRAM
```

Create a SKETCH on T(A, B):

```sql
CREATE STATISTICS ON MYSYSTEM.T(A,B) TYPE SKETCH;
```

## Related Information

ALTER STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](ALTER-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) DROP STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](DROP-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) REFRESH STATISTICS Statement (Extended Store Table) [Dynamic Tiering] [→](REFRESH-STATISTICS-Statement-Extended-Store-Table-Dynamic.md) M_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md) M_SYSTEM_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md)
