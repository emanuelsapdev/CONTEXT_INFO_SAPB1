# 4.10.1.17 ALTER STATISTICS Statement (Data Definition)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 459–466

Alters the properties of a data statistics object.

## Syntax

```sql
ALTER STATISTICS { <data_statistics_name> [,...] | ON <data_sources>
[ [ HAVING ] <match_properties> ] }
 [ SET <set_data_statistics_properties> ]
 [ <add_drop_data_statistics_properties> ]
 [ <initial_refresh> ]
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

For RECORD COUNT data statistics objects, you cannot specify columns as part of `<data_sources>`.

##### table_name

Specifies the table on which the data statistics are defined.

```sql
<table_name> ::= [ [ <database_name>.]<schema_name>.]<identifier>
```

For linked database, `<database_name>` is the name of the remote source. For all other cases, `<database_name>` is the name of the database where the table is located.

##### column_name

Specifies the column for which the data statistics are defined.

```sql
<column_name> ::= <identifier>
```

If no `<column_name>` is specified, then all statistics for the table that match the specified properties are altered, including table-wide statistics (RECORD COUNT).

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

T(A,X)

T(B,C)

T(A)

| **Match type** | **Example matches** | **Example non-matches** |
| --- | --- | --- |
|   | T(C,B,A,X) |   |

#### match_properties

Specifies properties to use for matching when selecting data statistics.

```sql
<match_properties> ::= <match_property>[...]
<match_property> ::=
 TYPE <data_statistics_type>  | REFRESH TYPE <refresh_type_filter>
```

If TYPE is not specified, then all data statistics objects of any type on the specified data sources are refreshed (ALL). For descriptions of the supported data statistics types see the CREATE STATISTICS Statement topic.

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

Specifies the refresh strategy to match in the data statistics objects when selecting the data statistics to refresh. ALL is the default.

```sql
<refresh_type_filter> ::= AUTO | MANUAL | ALL
```

#### set_data_statistics_properties

Specifies the properties of the data statistics objects to modify.

```sql
<data_statistics_properties> ::=
 <data_statistics_property>[, <data_statistics_property>[,...] ]

<data_statistics_property> ::=
 REFRESH TYPE <refresh_type>
 | ENABLE <on_off>
 | BUCKETS <unsigned_integer>
 | QERROR <numeric_literal>
 | QTHETA <unsigned_integer>
 | { MEMORY <memory_bytes> | MEMORY PERCENT <memory_percentage> }
 | ACCURACY <numeric_literal>
 | PREFIXBITS <unsigned_integer>
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

##### ACCURACY numeric_literal

Controls the time and space requirements to use for the SKETCH algorithms. This parameter can only be specified when TYPE is SKETCH and must be a number between 0 and 1, with larger values causing decreased time and space requirements but poorer SKETCH resolution. The default is 0.1.

##### PREFIX BITS unsigned_integer

Controls the number of bits the SKETCH algorithms use when constructing the SKETCH statistics. Specify this parameter when TYPE is SKETCH. Its value is an integer between 0 and 63. The default is 8.

##### CONSTRAINT constraint_param

Specifies constraints to use for the specified `<data_statistics_type>`. For SKETCH, `<constraint_param>` specifies the algorithm to use to build the SKETCH. The default is LOGLOGCOUNTING; the remaining algorithms are for internal use.

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
- You have the ALTER privilege on the object you are altering statistics on.
- For linked database, you have the LINKED DATABASE object level privilege on the remote source, regardless of who owns the remote source.

## Description

The ALTER STATISTICS statement alters the properties of a data statistics object. A typical change to a data statistics object might be to enable or disable it, or to change settings for properties such as BUCKETS or ENABLE ON/OFF.

ADD, DROP and SET clauses can be specified in any order in the ALTER STATISTICS statement, but not more than once each.

You cannot alter the type for the data statistics object. For example, you cannot change a data statistics object from a HISTOGRAM to a SKETCH, you must create the SKETCH data statistics object separately.

## Example

The following example sets the refresh type of a HISTOGRAM on data source T(X) to AUTO and rebuilds the data statistics object:

```sql
ALTER STATISTICS on MYSYSTEM.T(X) TYPE HISTOGRAM SET REFRESH TYPE AUTO;
```

The following example alters the MYSIMPLESTAT data statistics object to enable it for use with dynamic partition pruning and rebuilds the data statistics object:

```sql
ALTER STATISTICS MYSIMPLESTA ADD VALID FOR DATA DEPENDENCY;
```

The following example sets the number of buckets to 10 on the remote source REMOTE2 using linked database. The NO INITIAL REFRESH clause means the new setting will not take effect until the next time the object is rebuilt using the REFRESH STATISTICS statement.

```sql
ALTER STATISTICS on "REMOTE2"."SYSTEM"."A1" TYPE TOPK SET BUCKETS 10 NO INITIAL
REFRESH;
```

The following example sets the number of buckets to 150 for the TOPK data statistics object on the virtual table REMOTE2_A1.

```sql
ALTER STATISTICS on MYSYSTEM.REMOTE2_A1 TYPE TOPK SET BUCKETS 10;
```

## Related Information

CREATE STATISTICS Statement (Data Definition) [→](CREATE-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](REFRESH-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](DROP-STATISTICS-Statement-Data-Definition.md) M_DATA_STATISTICS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md)

M_SYSTEM_DATA_STATISTICS System View [→](../../../6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md) DATA_STATISTICS System View [→](../../../6-System-Views-Reference/6.01-System-Views/DATA_STATISTICS-System-View.md)
