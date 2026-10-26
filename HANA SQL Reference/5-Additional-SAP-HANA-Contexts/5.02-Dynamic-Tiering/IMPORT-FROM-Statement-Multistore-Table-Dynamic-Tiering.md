# 5.2.32 IMPORT FROM Statement (Multistore Table) [Dynamic Tiering]

> [↑ 5.2 Dynamic Tiering](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1348–1354

Imports external data from a file into existing extended storage partitions in a multistore table.

## Syntax

```sql
IMPORT FROM CSV [ <file_type> ] <file_path>
  [ INTO <table_name> ]
  [ WITH <import_from_option_list> ]
```

## Syntax Elements

#### file_type

Specifies the type of the file to be imported (comma-separated values or control file format).

```sql
<file_type> ::= CSV FILE | CONTROL FILE
```

When importing data statistics objects, only import from a control file is supported.

#### file_path

Specifies the complete path and file name of the file to import.

```sql
<file_path> ::= <string_literal>
```

When `<file_type>` is CSV, a GZIP (.gz) file is supported in`<file_path>` to indicate a GZIP file containing the CSV data.

#### table_name

Specifies the target table name or data statistics object name into which the imported data will be imported.

```sql
<database_object_name> ::=
 [<schema_name>.]<table_name>
 | STATISTICS [<schema_name>.]<data_statistics_object_name>
<schema_name> ::= <unicode_name>
<table_name> ::= <identifier>
<data_statistics_object_name> ::= <identifier>
```

Specify STATISTICS when importing data into an existing database statistics object. If the data statistics objects already has data, then the data is overwritten by the data being imported. INTO STATISTICS can only be specified in a control file. When importing data to a data statistics object, the only supported `<import_from_option>` option is ERROR LOG.

#### import_from_option_list

Specifies a list of options that control import behavior.

```sql
WITH <import_from_option_list>
<import_from_option_list> ::= <import_from_option>[{,
<import_from_option>}...]
```

```sql
<import_from_option> ::=
   NO TYPE CHECK
   | SKIP FIRST <number_of_rows_to_skip> ROW
   | COLUMN LIST IN FIRST ROW
   | COLUMN LIST ( <column_name_list> ) [WITH SCHEMA FLEXIBILITY]
   | RECORD DELIMITED BY <string_for_record_delimiter>
   | FIELD DELIMITED BY <string_for_field_delimiter>
   | OPTIONALLY ENCLOSED BY <character_for_optional_enclosure>
   | ESCAPE <escape_character>
   | DATE FORMAT <string_for_date_format>
   | TIME FORMAT <string_for_time_format>
   | TIMESTAMP FORMAT <string_for_timestamp_format>
   | ERROR LOG <file_path_of_error_log>
   | THREADS <number_of_threads>
   | FAIL ON INVALID DATA
```

##### NO TYPE CHECK

Specifies that the record is inserted without checking the type of each field.

##### SKIP FIRST number_of_rows_to_skip ROW

Skips the specified number of rows in the import file.

```sql
SKIP FIRST <number_of_rows_to_skip> ROW
<number_of_rows_to_skip> ::= <unsigned_integer>
```

##### COLUMN LIST IN FIRST ROW

Indicates that the column list is stored in the first row of the CSV import file.

WITH SCHEMA FLEXIBILITY clause is not supported. If specified, an error is returned.

##### COLUMN LIST ( column_name_list )

The column list for the data being imported. The name list has one or more column names. The ordering of the column names has to match the order of the column data in the CSV file and the columns in the target table.

```sql
COLUMN LIST ( <column_name_list> )
```

```sql
<column_name_list> ::= <column_name> [{, <column_name>}...]
```

```sql
<column_name> ::= <identifier>
```

##### RECORD DELIMITED BY string_for_record_delimiter

Specifies the record delimiter used in the CSV file being imported.

```sql
RECORD DELIMITED BY <string_for_record_delimiter>
<string_for_record_delimiter> ::= <string_literal>
```

##### FIELD DELIMITED BY string_for_field_delimiter

Specifies the field delimiter of the CSV file.

```sql
FIELD DELIMITED BY <string_for_field_delimiter>
<string_for_field_delimiter> ::= <string_literal>
```

##### OPTIONALLY ENCLOSED BY character_for_optional_enclosure

Specifies the optional enclosure character that delimits field data.

```sql
OPTIONALLY ENCLOSED BY <character_for_optional_enclosure>
<character_for_optional_enclosure> ::= <character_literal>
```

##### ESCAPE escape_character

Specifies the escape character used in the import data.

```sql
<escape_character> ::= <character_literal>
```

##### DATE FORMAT string_for_date_format

Specifies the format that date strings are encoded with in the import data.

```sql
DATE FORMAT <string_for_date_format>
<string_for_date_format> ::= <string_literal>
```

Values can include:

- Y: year
- MM: month
- MON: name of month
- DD: day

For example:

- 'YYYYMMDD' = 20120520
- 'YYYY-MM-DD' = 2012-05-20
- 'YYYY-MON-DD' : 2012-MAY-20

##### TIME FORMAT string_for_time_format

Specifies the format that time strings are encoded with in the import data.

```sql
TIME FORMAT <string_for_time_format>
<string_for_time_format> ::= <string_literal>
```

Values can include:

- HH24: hour
- MI: minute
- SS: second

For example:

- 'HH24MISS': 143025
- 'HH24:MI:SS': 14:30:25

##### TIMESTAMP FORMAT string_for_timestamp_format

Specifies the format that timestamp strings are encoded with in the import data.

```sql
TIMESTAMP FORMAT <string_for_timestamp_format>
<string_for_timestamp_format> ::= <string_literal>
```

For example:

- 'YYYY-MM-DD HH24:MI:SS': 2012-05-20 14:30:25

##### ERROR LOG file_path_of_error_log

Creates a HANA error log, DT message log, and DT row log at the specified file path.

```sql
ERROR LOG <file_path_of_error_log>
```

```sql
<file_path_of_error_log> ::= <string_literal>
```

**THREADS number_of_threads** Specifies the number of threads that can be used for concurrent import. The default value is 1 and maximum allowed is 256.

##### FAIL ON INVALID DATA

Specifies that the IMPORT FROM command fails unless all the entries import successfully.

## Permissions

You must have the IMPORT privilege.

## Description

The IMPORT FROM statement imports external data from a file into an existing table or data statistics object. To import catalog objects (tables, views, etc.) that have been exported with the EXPORT Statement (Extended Store Table) [Dynamic Tiering] [→](EXPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md) statement, use the IMPORT Statement (Extended Store Table) [Dynamic Tiering] [→](IMPORT-Statement-Extended-Store-Table-Dynamic-Tiering.md) statement.

> **Restriction**
>
> Do not use IMPORT FROM CSV for a multistore table if the table has generated columns, and the CSV file also has data for generated columns.

Optional enclosure, if used, must be a single character.

When importing from data statistics objects, the schema of a data statistics object is the same as that of the schema of the data source on which the data statistics object was created.

File locations for extended storage must be on a shared file system accessible to both SAP HANA and the extended storage system.

> **Note**
>
> All `<string_literal>`s in the `<import_from_option>` support UTF-8 except surrogate-pair encoding.

For security reasons, only CSV files located at paths defined in the `csv_import_path_filter` configuration parameter can be loaded by using the IMPORT FROM SQL statement. This feature can be disabled by using the `enable_csv_import_path_filter` configuration parameter. Two related configuration parameters are specified in the `import_export` section of the indexserver (nameserver in the case of multi-DB) configuration, so you can turn off this feature or update path filter as follows:

```sql
ALTER SYSTEM ALTER CONFIGURATION ('indexserver.ini', 'system') set
('import_export', 'enable_csv_import_path_filter') = 'false' with reconfigure
ALTER SYSTEM ALTER CONFIGURATION ('indexserver.ini', 'system') set
('import_export', 'csv_import_path_filter') = '/A;/B' with reconfigure
```

Once you add a path '/A' to the path filter, every sub-path of '/A' is automatically added as well.

If you are importing data into a multistore table that already has data, take a binary export of the table before you import data from new files. If the import fails, you can import the table using the export, and then retry `IMPORT FROM CSV` after you fix the issue that caused the failure.

When you perform `IMPORT FROM CSV` with entries that contain TIME or SECONDDATE values that have fractional second values, dynamic tiering retains the fractions, while SAP HANA does not. This can lead to unexpected failures while selecting data from the tables containing those values. For example, dynamic tiering stores "2017-06-08 21:35:00.109" exactly, where SAP HANA stores "2017-06-08 21:35:00". The two are not equal (the HANA column store value is less than the dynamic tiering extended store value), so that any time a query tries to join those two values — one from a column store partition (or table) and second from an extended store partition (or table), such as in a multistore table — the result may seem unexpected. See Values and Behaviors of Numeric and Temporal Data Types in the Dynamic Tiering Administration Guide for details.

## Examples

Example 1 – Importing data from a single CSV file.

Create a table mytable1 to store the imported data:

```sql
CREATE COLUMN TABLE mytable1 (A INT, B VARCHAR(10), C DATE, D TIME)
    PARTITION BY RANGE (A) (USING DEFAULT STORAGE (PARTITION 1 <= VALUES < 1000,
PARTITION OTHERS)
    USING EXTENDED STORAGE (PARTITION 1000 <= VALUES < 10000));
```

Create a CSV text file `/data/data1.csv` and add the following contents:

```sql
1,"DATA1","2016-05-20","14:30:25"
2,"DATA2","2016-05-21","15:30:25"
3,"DATA3","2016-05-22","16:30:25"
4,"DATA4","2016-05-23","17:30:25"
```

Execute the following to import the data:

```sql
IMPORT FROM CSV FILE '/data/data1.csv' INTO mytable1
   WITH RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ',';
```

Example 2 – Import using date formats

In the example below, the date format is of the CSV import data is different to the default date format 'YYYY-MM-DD'. In this import data the date format used is 'MM-DD-YYYY'. You create a CSV text file `/data/ data_different_date.csv` and add the following contents:

```sql
1,"DATA1","05-20-2012","14:30:25",123456
2,"DATA2","05-21-2012","15:30:25",234567
3,"DATA3","05-22-2012","16:30:25",345678
4,"DATA4","05-23-2012","17:30:25",456789
```

You execute the following command to import the data:

```sql
IMPORT FROM CSV FILE '/data/data_different_date.csv' INTO mytable1
   WITH RECORD
   DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   DATE FORMAT 'MM-DD-YYYY';
```

Example 3 – Import using COLUMN LIST

You create a CSV text file `/data/data_col_list.csv` and add the following contents:

```sql
1,"DATA1","2012-05-20",123456
2,"DATA2","2012-05-21",234567
3,"DATA3","2012-05-22",345678
4,"DATA4","2012-05-23",456789
```

You execute the following commands to import the data using a column list:

```sql
IMPORT FROM CSV FILE '/data/data_col_list.csv' INTO mytable1
   WITH RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   COLUMN LIST ("A", "B", "C", "D");
```

Example 4 – Importing using timestamp format

```sql
IMPORT FROM CSV FILE '/data/data1.csv' INTO mytable1
    WITH RECORD DELIMITED BY '\n'
    FIELD DELIMITED BY ','
    TIMESTAMP FORMAT 'HH:MI:SS';
```

Example 5 – Importing using a control file

You import the data from Example 1 using a control file you create (`/data/data.ctl`) that points to the CSV file. The control file contains the following commands:

```sql
IMPORT DATA INTO TABLE mytable1 FROM '/data/data.csv'
   RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   OPTIONALLY ENCLOSED BY '"'
   ERROR LOG '/data/data.err'
```

You execute the following command to import the data using the control file:

```sql
IMPORT FROM CONTROL FILE '/data/data.ctl';
```
