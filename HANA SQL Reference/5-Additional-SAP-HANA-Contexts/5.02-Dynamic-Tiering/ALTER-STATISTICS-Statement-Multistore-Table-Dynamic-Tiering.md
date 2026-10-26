# 5.2.6 ALTER STATISTICS Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1229–1236

Alters the properties of a data statistics object.

## Syntax

```sql
ALTER STATISTICS { <data_statistics_name>[,...] | ON <data_sources> [ [ HAVING ]
<match_properties> ] }
 [ SET <set_data_statistics_properties> ]
 [ <add_drop_data_statistics_properties> ]
 [ <initial_refresh> ];
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

For RECORD COUNT data statistics objects, you cannot specify columns as part of data_sources.

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
| EXACT | T(A,B,C) | T(B,A,C) - because the column order is different than the column order of `<data_sources>`.<br>T(A)- because it does not contain the exact same columns and column order of `<data_sources>`.<br>T(X,A,B,C) - because T.(X) is not a column in `<data_sources>`. |

CASCADE T(A,C) T(X) - because it does not contain

any columns that match the

T(C)

columns in `<data_sources>`.

T(B,A)

T(A,B,C)

| **Match type** | **Example matches** | **Example non-matches** |
| --- | --- | --- |
|   | T(A,X)<br>T(B,C)<br>T(A)<br>T(C,B,A,X) |   |

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

#### set_data_statistics_properties

Specifies the properties of the data statistics objects to modify.

```sql
<set_data_statistics_properties> :=
 <data_statistics_property>[, <data_statistics_property>[,...] ]
<data_statistics_property> ::=
 | REFRESH TYPE <refresh_type>
 | ENABLE <on_off>
 | BUCKETS <unsigned_integer>
 | QERROR <numeric_literal>
 | QTHETA <unsigned_integer>
 | { MEMORY <memory_bytes> | MEMORY PERCENT <memory_percentage> }
 | PERSISTENT <on_off>
 | CONSTRAINT <constraint_param>
```

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

ENABLE ON enables the optimizer to see the data statistics object. The data statistics object must be populated with data for the optimizer to use it.

ENABLE OFF disables the use of the data statistics object by the optimizer and prevents the ability to refresh the data statistics object. Data statistics objects that are not enabled can still be dropped. To make a data statistics object with ENABLE OFF accessible to the optimizer, execute an ALTER STATISTICS...ENABLE ON statement.

##### BUCKETS unsigned_integer

The BUCKETS property is only for use with TYPE HISTOGRAM or TOPK. For HISTOGRAM, BUCKETS specifies the maximum number of data buckets in the HISTOGRAM. For TOPK, BUCKETS specifies the K value.

The default is automatically determined by the data statistics building algorithm in use.

If a very small number of buckets is specified for a QOPTIMAL HISTOGRAM, then the algorithm may fail to build a valid HISTOGRAM either during the first build or during a subsequent refresh executed for the HISTOGRAM.

For column store, extended store, and multistore tables only, if a very small number of buckets is specified for a QOPTIMAL HISTOGRAM, then the algorithm may fail to build a valid HISTOGRAM either during the first build or during a subsequent refresh executed for the HISTOGRAM.

##### QERROR numeric_literal

Specifies the Q error to use for the q-optimal HISTOGRAM. You can specify this parameter when TYPE is HISTOGRAM and CONSTRAINT is QOPTIMAL. The default is automatically determined by the HISTOGRAM algorithm in use.

##### QTHETA unsigned_integer

Specifies a lower bound on the frequencies for which a q error constraint is applied for a q-optimal HISTOGRAM. You can specify this parameter when TYPE is HISTOGRAM and CONSTRAINT is QOPTIMAL. The default is automatically determined by the HISTOGRAM algorithm in use.

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

##### PERSISTENT on_off

Specifies whether data statistics object data persists in the storage of the table, and only applies to QOPTIMAL HISTOGRAMS on column store tables. The default is PERSISTENT ON.

```sql
<on_off> ::= { ON | OFF }
```

Other statistics types are always persistent.

##### CONSTRAINT constraint_param

Specifies the mathematical constraint used to build HISTOGRAM or SKETCH.

```sql
CONSTRAINT <constraint_param>
```

- HISTOGRAM `<constraint_param>` specifies the mathematical constraint for the HISTOGRAM:

```sql
<constraint_param> ::= QOPTIMAL | MAXDIFF
```

- QOPTIMAL – For column store tables, the default value of `<constraint_param>` for the column storage part of the table is QOPTIMAL.
- MAXDIFF – Dor extended tables, and extended partitions of multistore tables, the default value of `<constraint_param>` for the extended storage part of the table is MAXDIFF.

> **Note**
>
> HISTOGRAM sizing restrictions (BUCKETS, MEMORY, and MEMORY PERCENT) are applied per HISTOGRAM. A non-default CONSTRAINT for a HISTOGRAM returns an error.

- SKETCH constraints apply only to the column store data statistics, not to the extended storage part of the table. `<constraint_param>` specifies the algorithm to use to build the SKETCH. The default is LOGLOGCOUNTING; the remaining algorithms are for internal use.

```sql
<constraint_param> ::=
KMINVAL
| PCSA
| LINEARCOUNTING
| LOGCOUNTING
| LOGLOGCOUNTING
| SUPERLOGLOGCOUNTING
```

#### add_drop_data_statistics_properties

Specifies the properties of the data statistics objects you set using the ADD and DROP keywords.

```sql
<add_drop_data_statistics_properties> ::= <add_drop_property>
[ <add_drop_property> […]]
<add_drop_property> ::=
{ ADD | DROP } VALID FOR <valid_for_list>
```

This property is supported for column store, extended store, and multistore tables, but not virtual tables or linked database.

##### VALID FOR valid_for_list

Defines how the data statistics object may be used. The VALID FOR clause is only permitted with statistics type SIMPLE.

```sql
<valid_for_list> ::= <usage>[, <usage>[,...] ]
<usage> ::= { ESTIMATION | DATA DEPENDENCY }
```

ESTIMATION initializes the data statistics object for use by the optimizer to improve selectivity estimation. SIMPLE data statistics objects are initialized for estimation use by default.

DATA DEPENDENCY applies to partitioned column store and multistore tables only. It initializes the data statistics object to be used by features that require higher (or more) data consistency (including automatically refreshing and rebuilding when needed), such as the dynamic partition pruning feature. For more information about the dynamic partition pruning feature, including the types of columns that can have data statistics defined for dynamic partition pruning, see the SAP HANA Administration Guide.

#### initial_refresh

Specifies whether to repopulate the data statistics object with data after altering it.

```sql
<initial_refresh> ::= [ NO ] INITIAL REFRESH
```

If the object was built, then disabled, and is now being re-enabled, then initial refresh is not required.

##### INITIAL REFRESH

Alters the definition of the data statistics object and repopulates it with data. The default behavior is INITIAL REFRESH.

##### NO INITIAL REFRESH

Alters the definition of the data statistics object, but does not repopulate it with data.

Use NO INITIAL REFRESH when you want to change the underlying data before refreshing the data statistics object.

You cannot specify NO INITIAL REFRESH if ENABLE OFF is not specified.

## Permissions

One of the following is true:

- You own the object you are altering statistics on.
- You have the ALTER privilege on the object, which was created by another user and you are altering statistics on.

## Description

The ALTER STATISTICS statement alters the properties of a data statistics object. A typical change to a data statistics object might be to enable or disable it, or to change settings for constraints such as BUCKETS or ENABLE ON/OFF.

Refer to the CREATE STATISTICS statement for complete descriptions of the data statistic types (`<data_statistics_type>`).

You cannot alter the type for the data statistics object. For example, you cannot change a data statistics object from a HISTOGRAM to a SIMPLE, you must create the SIMPLE data statistics object separately.

## Example

Set the refresh type of HISTOGRAMS on data source T(X) to AUTO and rebuilds the data statistics object:

```sql
ALTER STATISTICS on MYSYSTEM.T(X) TYPE HISTOGRAM SET REFRESH TYPE AUTO;
```

Set the refresh type and number of buckets for two HISTOGRAMS on table T, specifying histograms by name and rebuilds the data statistics object:

```sql
ALTER STATISTICS HIST1_T, HIST2_T SET BUCKETS 100 REFRESH TYPE AUTO;
```

## Related Information

REFRESH STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](REFRESH-STATISTICS-Statement-Multistore-Table-Dynamic.md) CREATE STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](CREATE-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md) DROP STATISTICS Statement (Multistore Table) [Dynamic Tiering] [→](DROP-STATISTICS-Statement-Multistore-Table-Dynamic-Tiering.md) M_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md) M_SYSTEM_DATA_STATISTICS System View [→](../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md)
