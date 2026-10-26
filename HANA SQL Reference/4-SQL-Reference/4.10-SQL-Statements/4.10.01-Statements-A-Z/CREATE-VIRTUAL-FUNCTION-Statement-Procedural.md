# 4.10.1.74 CREATE VIRTUAL FUNCTION Statement (Procedural)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 867–872

Creates a virtual function that allows you to employ smart data access on service interfaces exposed by remote systems (both ODBC/non-ODBC).

## Syntax

```sql
CREATE VIRTUAL FUNCTION <func_name> [(<parameter_clause>)]
   RETURNS <return_table_type> [SQL SECURITY <mode>] [<package_clause>]
   CONFIGURATION <remote_proc_properties> AT <source_name>
```

## Syntax Elements

#### func_name

Specifies the function name with optional schema name.

```sql
<func_name> ::= [<schema_name>.]<identifier>
<schema_name> ::= <identifier>
```

#### parameter_clause

Specifies input parameters for the virtual function.

```sql
<parameter_clause> ::= <parameter> [{,<parameter>}...]
```

These input parameters are only supported when creating a virtual function that is used with the syntax element PACKAGE. The syntax element PACKAGE allows the function to pass information to the custom MR.

##### parameter

Defines a function parameter with associated data type, consisting of a name and the data type definition.

```sql
<parameter> ::= [IN] <param_name> <datatype>
<param_name> ::= <identifier>
<datatype> ::= <sql_type>
```

##### sql_type

Specifies the data type.

```sql
<sql_type> ::=
 BIGINT
 | INTEGER
 | SMALLINT
 | TINYINT
 | DATE
 | TIME
 | TIMESTAMP
| SMALLDECIMAL
| DECIMAL
| REAL
| DOUBLE
```

Virtual functions support scalar functions types and primitive SQL types as input.

#### return_type

```sql
<return_type> ::= <return_table_type> | <table_type>
```

Table functions must return a table whose type is defined by `<return_type>`. Non-scalar functions are supported.

##### return_table_type

Defines the structure of the returned table data.

```sql
<return_table_type> ::= TABLE ( <ret_column_list> )
```

##### ret_column_list

Defines the list of columns returned from the function.

```sql
<ret_column_list> ::= <ret_column_elem>[{, <ret_column_elem>}...]
```

##### ret_column_elem

Defines the name of column element with associated data type.

```sql
<ret_column_elem> ::= <column_name> <sql_type>
<column_name> ::= <identifier>
```

##### table_type

Defines the output parameters and you can utilize a table type previously defined with the CREATE TYPE command. See CREATE TYPE for details.

```sql
<table_type> ::= <identifier>
```

#### SQL SECURITY mode

Specifies the security mode of the table function.

```sql
<mode> ::= DEFINER | INVOKER
```

The default value is DEFINER.

#### package_clause

Defines the identifier of the map reduce program that was developed or imported into SAP HANA repository via the SAP HANA Studio plugin.

```sql
<package_clause> ::= PACKAGE <schema>.<jobPackage>
<schema> ::= <identifier>
<jobPackage> ::= <identifier>
```

The map reduce program is a collection of artifacts that can be executed on a Hadoop system. The schema name is optional.

#### CONFIGURATION remote_proc_properties

Defines required and optional properties for executing remote procedures.

```sql
<remote_proc_properties> ::= <string_literal>
```

The properties have the format of key-value pairs. The target map reduce program can read these key-value pairs. Additional custom properties can also be passed to the remote procedure. The following table lists the userdefined key properties to define a virtual UDF function

| UserDefined Key Properties **Property** | **Optional** | **Default** | **Definition** |
| --- | --- | --- | --- |
| enable_remote_cache | optional | false | Instructs SAP HANA to store results of the initial remote query fragment in HDFS and subsequent queries are read directly from the result set. |
| remote_cache_validity | optional | 3600 | Defines the duration of time (in seconds) after which the cache is stale. |

The following table lists the required user defined key properties, to define a virtual UDF function that reads HDFS files:

| UserDefined Key Properties **Property** | **Optional** | **Default** | **Definition** |
| --- | --- | --- | --- |
| hdfs_location |   |   | Defines the directory from where the query would read the HDFS file(s). For example, /user/hive/warehouse/ test. |
| hdfs_input_format | optional | csv | Defines the type of the data source file for the query. |
| hdfs_field_delimiter | optional | , | Defines the character that delimits columns in a file. The default value is a comma. |
| date_format |   | yyyy-MM-dd | Defines the ISO date format of a date typed column in the format. |
| time_format |   | HH:mm:ss.S | Defines the ISO time format of a time typed column. |
| datetime_format |   |   | Defines the ISO date_time format for the date_time typed column. |

The following table lists the required user defined key properties to define a virtual UDF function calling a custom map reduce program:

| UserDefined Key Properties **Property** | **Optional** | **Default** | **Definition** |
| --- | --- | --- | --- |
| mapred_jobchain |   |   | Provides a sequence of all `<mapred>` properties listed below |
| mapred_mapper |   |   | Specifies the function that responsible for transforming each element in an input list into a new output list. One or more functions can be listed. |
| mapred_reducer |   |   | Defines the aggregation function of the output list from a mapper. There could be zero or many reducers. |
| mapred_combiner |   |   | Defines the aggregation of input from a mapper, normally used to help limit the amount of data passed to a `<mapred_reducer>`. |
| mapred_input |   |   | Defines the data source. Values can be an input file input or the result of a map per function. There can be one or many `<mapred_input>`. |
| mapred_input_format |   |   | Defines the data input format. |
| mapred_output_format | optional | text | Defines the data output format for writing the results to HDFS. |
| mapred_field_delimiter | optional | , | Defines the delimiter between columns when generating output files. The default value is a comma. |

#### AT source_name

Defines the name of the remote source.

```sql
<source_name> ::= <identifier>
```

## Description

A virtual function allows you to use smart data access on service interfaces exposed by remote systems (both ODBC/non-ODBC). These service interfaces could be a SQLScript Procedure on remote SAP HANA system (ODBC Compliant) or a custom map reduce job executed on a Hadoop system. This feature complements the Virtual Table feature of SDA.

Remote procedure properties are specific to a given service interface on a remote system. It is a delimited list of name value pairs enclosed in quotes. The source name is the name of the remote source created using the CREATE REMOTE SOURCE statement. There is no language type specified and the function body is empty. The execution is delegated to the remote side through respective adapter for the given source name. This function is strictly a table UDF and can be invoked part of regular SQL fragment.

From SP08, HANA supports custom map reduce invocation on a Hadoop system. For this reason, a new adapter called hadoop is included along with a remote source that contains all the necessary connectivity information.

## Permissions

This statement requires the CREATE VIRTUAL FUNCTION object privilege.

## Example

The following example shows how to create a remote destination with the adapter type hadoop.

```sql
CREATE REMOTE SOURCE HOSTA1 ADAPTER
   "hadoop" CONFIGURATION 'webhdfs.url=http://hostA:50070/;webhcat.url=http://
hostA:50111'  WITH CREDENTIAL
   TYPE 'PASSWORD' USING 'user=dbuser;password=dbtest';
```

The following example explains how to create a virtual function with the remote source created in the above example.

```sql
CREATE VIRTUAL FUNCTION word_count() RETURNS TABLE ( word
   NVARCHAR(60),  count INT) PACKAGE "SYSTEM"."WORD_COUNT" CONFIGURATION
   'sap.hana.hadoop.mapper=com.sap.hadoop.examples.WordCountMapper;

sap.hana.hadoop.reducer=com.sap.hadoop.examples.WordCountReducer;sap.hana.hadoop.
input'/path/to/input'
   AT HOSTA1;
```

The following example explains how to create a virtual function with the remote source created above,

```sql
CREATE VIRTUAL FUNCTION  v_tpch10() RETURNS TABLE
   ("c_custkey" integer , "c_name"  varchar (255), "revenue"  double ,
   "c_acctbal" double , "n_name"  varchar (255), "c_address" varchar (255),
   "c_phone"  varchar (255), "c_comment"  varchar (255))
   PACKAGESYSTEM ."tpch10" CONFIGURATION'mapred_jobchain=[{"mapred_input":"/user/
hive/warehouse/tpch.db/orders,/user/hive/warehouse/tpch.db/customer",
     "mapred_mapper":"com.sap.hana.hadoop.samples.TestQuery5$Map",
     "mapred_reducer":"com.sap.hana.hadoop.samples.TestQuery5$Reduce"},
     {"mapred_input":"result{0},/user/hive/warehouse/tpch.db/lineitem",
     "mapred_mapper":"com.sap.hana.hadoop.samples.TestQuery4$Map",
     "mapred_reducer":"com.sap.hana.hadoop.samples.TestQuery4$Reduce"},
     {"mapred_input":"result{1},/user/hive/warehouse/tpch.db/nation",
     "mapred_mapper":"com.sap.hana.hadoop.samples.TestQuery3$Map",
     "mapred_reducer":"com.sap.hana.hadoop.samples.TestQuery3$Reduce"},
{"mapred_input":"result{2}","mapred_mapper":"com.sap.hana.hadoop.samples.TestQuer
y2$Map",
     "mapred_reducer":"com.sap.hana.hadoop.samples.TestQuery2$Reduce"},

{"mapred_input":"result{3}","mapred_mapper":"com.sap.hana.hadoop.samples.TestQuer
y1$Map",
     "mapred_reducer":"com.sap.hana.hadoop.samples.TestQuery1$Reduce",

"mapreduce.partitioner.class":"org.apache.hadoop.mapred.lib.KeyFieldBasedPartitio
ner",

"mapred.output.key.comparator.class":"org.apache.hadoop.mapred.lib.KeyFieldBasedC
omparator",
     "mapreduce.partition.keycomparator.options":"-k1,1nr",
     "mapreduce.map.output.key.field.separator":"|"}]'
   AT HOSTA1;
```

## Related Information

[CREATE TYPE Statement (Procedural)](CREATE-TYPE-Statement-Procedural.md)
