# 4.10.1.121 IMPORT FROM Statement (Data Import Export)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 978–985

Imports external data from a file into an existing table or an existing data statistics object.

## Syntax

```sql
IMPORT FROM [ <file_type> ] <file_path>
 [ INTO <database_object_name> ]
 [ WITH <import_from_option_list> ]
```

## Syntax Elements

#### file_type

Specifies the type of file being imported from.

```sql
<file_type> ::= CSV FILE | CONTROL FILE
```

When importing data statistics objects, you can only import from a control file.

#### file_path

Specifies the complete path and file name of the file to import.

```sql
<file_path> ::= <string_literal>
```

Named pipes (FIFO) are supported for `<file_path>`.

When `<file_type>` is CSV, a GZIP (.gz) file is supported in `<file_path>` to indicate a GZIP file containing the CSV data.

In distributed systems, `<file_path>` must be a shared disk; otherwise, the operation may fail or have unexpected results.

#### database_object_name

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
<import_from_option_list> ::= <import_from_option>[, <import_from_option> [,
…] ]
<import_from_option> ::=
 THREADS <number_of_threads>
 | BATCH <number_of_records_of_each_commit>
 | TABLE LOCK
 | NO TYPE CHECK
 | SKIP FIRST <number_of_rows_to_skip> ROW
 | COLUMN LIST IN FIRST ROW [<with_schema_flexibility>]
 | COLUMN LIST (<column_name_list>) [<with_schema_flexibility>]
 | RECORD DELIMITED BY <string_for_record_delimiter>
 | FIELD DELIMITED BY <string_for_field_delimiter>
 | OPTIONALLY ENCLOSED BY <character_for_optional_enclosure>
 | ESCAPE <escape_character>
 | DATE FORMAT <string_for_date_format>
 | TIME FORMAT <string_for_time_format>
 | TIMESTAMP FORMAT <string_for_timestamp_format>
 | ERROR LOG <file_path_of_error_log>
 | FAIL ON INVALID DATA
```

##### THREADS number_of_threads

Specifies the number of threads that can be used for concurrent import. The default value is 1 and the maximum allowed value is 256.

```sql
THREADS <number_of_threads>
<number_of_threads> ::= <unsigned_integer>
```

##### BATCH number_of_records_of_each_commit

Specifies the number of records to be inserted in each commit.

```sql
BATCH <number_of_records_of_each_commit>
<number_of_records_of_each_commit> ::= <unsigned_integer>
```

THREADS and BATCH provide high loading performance by enabling parallel loading and also by committing many records at once. In general, for column tables, a good setting to use is 10 parallel loading threads, with a commit frequency of 10,000 records or greater.

##### TABLE LOCK

Provides faster data loading for column store tables.

Use this option carefully as it incurs table locks in exclusive mode, as well as explicit hard merges and save points after data loading is finished. The performance gain from this option can vary according to the table constraints (like primary key) and optimization of other layers (like persistence or a DML command).

##### NO TYPE CHECK

Specifies that the record is inserted without checking the type of each field.

##### SKIP FIRST number_of_rows_to_skip ROW

Skips the specified number of rows in the import file.

```sql
SKIP FIRST <number_of_rows_to_skip> ROW
<number_of_rows_to_skip> ::= <unsigned_integer>
```

##### COLUMN LIST IN FIRST ROW [with_schema_flexibility]

Indicates that the column list is stored in the first row of the CSV import file.

```sql
COLUMN LIST IN FIRST ROW [<with_schema_flexibility>]
<with_schema_flexibility> ::= WITH SCHEMA FLEXIBILITY
```

WITH SCHEMA FLEXIBILITY creates missing columns in flexible tables during CSV imports, as specified in the header (first row) of the CSV file or column list. By default, missing columns in flexible tables are not created automatically during data imports.

##### COLUMN LIST ( column_name_list ) [with_schema_flexibility]

Specifies the list of table columns for the data being imported.

```sql
COLUMN LIST (<column_name_list>)
<column_name_list> ::= <column_name> [, <column_name>...]
<column_name> ::= <identifier>
<with_schema_flexibility> ::= WITH SCHEMA FLEXIBILITY
```

The name list has one or more column names. The ordering of the column names has to match the order of the column data in the CSV file from the leftmost column. The column names must exist in the target table, and the data types must match those in the CSV file. Unmatched columns in the target table have NULL values. If the number of column names is larger than the number of columns in the CSV file, unmatched columns have NULL values. WITH SCHEMA FLEXIBILITY creates missing columns in flexible tables during CSV imports, as specified in the header (first row) of the CSV file or column list. By default, missing columns in flexible tables are not created automatically during data imports.

##### RECORD DELIMITED BY string_for_record_delimiter and FIELD DELIMITED BY string_for_field_delimiter

Specifies the record and field delimiters used in the CSV file, respectively. Supported delimiters are as follows:

- Any string of ASCII characters
- \Uhhhhhhhh: 8 hexadecimal digits
- \uhhhh: 4 hexadecimal digits
- \xhh…: 1 or more hexadecimal digits
- \nnn: one, two, or three octal numbers

Special characters such as '\036' or '\u0007' are useful when importing datafiles that have special characters like '\u0001' or chr(1). These values are then converted to non-escaped values and used as the delimiter.

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

Specifies that a log file of errors is generated and stored in this file. Ensure that the database can write to this file.

```sql
ERROR LOG <file_path_of_error_log>
<file_path_of_error_log> ::= <string_literal>
```

For security reasons, the path for ERROR LOG must not contain symbolic links and must not point to the same drive location (folder) as the database. It can, however, point to the location of the backup or work subfolders

##### FAIL ON INVALID DATA

Specifies that the IMPORT FROM command fails unless all the entries import successfully.

## Description

Use the IMPORT FROM statement to import data into database objects, such as tables and data statistics objects from files such as CSV files.

To import catalog objects (tables, views, and so on) that have been exported with the EXPORT statement, use the IMPORT statement instead.

When importing from data statistics objects, the schema of a data statistics object is the same as that of the schema of the data source on which the data statistics object was created.

All `<string_literals>` in the `<import_from_option>` support UTF-8 except surrogate-pair encoding.

For security reasons, only CSV files located at paths defined in the `csv_import_path_filter` configuration parameter can be loaded by using the IMPORT FROM SQL statement. This feature can be disabled by using the `enable_csv_import_path_filter` configuration parameter. Two related configuration parameters are specified in the `import_export` section of the indexserver (nameserver in the case of multi-DB) configuration, so you can turn off this feature or update path filter as follows:

```sql
ALTER SYSTEM ALTER CONFIGURATION ('indexserver.ini', 'system') set
('import_export', 'enable_csv_import_path_filter') = 'false' with reconfigure
ALTER SYSTEM ALTER CONFIGURATION ('indexserver.ini', 'system') set
('import_export', 'csv_import_path_filter') = '/A;/B' with reconfigure
```

Once you add a path '/A' to the path filter, every sub-path of '/A' is automatically added as well.

When using CSV format to export/import tables that have columns of type GENERATED ALWAYS AS `<expression>`, verify that the imported records match what was exported. If there are anomalies:

- For column tables, switch to exporting/importing as BINARY.
- For row tables, change the table to be a column table and export/import as BINARY.

## Permissions

You must have the IMPORT system privilege, and the CREATE ANY privilege on the schema that is being imported into.

## Examples

**Example** - Auto data type promotion during importing from flexible tables

Suppose you have a CSV file, `data.csv`, similar to the following:

```sql
ORG_ID,INT_COL,DEC_COL,DATE_COL,STR_COL,LOB_COL
1,12,12.34,"2017-01-03","my text","my text is longer than 5000 chars"
```

And that you have a table defined as follows:

```sql
CREATE COLUMN TABLE TEST.IMPORT_TABLE (
    "_ID" BIGINT GENERATED ALWAYS AS IDENTITY
) WITH SCHEMA FLEXIBILITY (DEFAULT DATA TYPE * AUTO DATA TYPE PROMOTION);
```

Your import statement would look as follows:

```sql
IMPORT FROM CSV FILE 'data.csv'
    INTO TEST.IMPORT_TABLE
    WITH THREADS 20
    BATCH 50000
    COLUMN LIST IN FIRST ROW WITH SCHEMA FLEXIBILITY
    RECORD DELIMITED BY '\n'
    FIELD DELIMITED BY ','
    OPTIONALLY ENCLOSED BY '"'
    DATE FORMAT 'YYYY-MM-DD'
    ERROR LOG 'error_log.txt'
;
```

Your resulting table columns and data types would be as follows:

```sql
_ID BIGINT
ORG_ID INTEGER
INT_COL INTEGER
DOC_COL DECIMAL
DATE_COL DATE
STR_COL NVARCHAR(5000)
LOB_COL NCLOB
```

**Example** - Importing CSV Data

Create a table, `mytable`, to store the imported data.

```sql
CREATE ROW TABLE mytable ( A INT, B VARCHAR(10), C DATE, D TIME, E DECIMAL );
```

Create a CSV text file, `/data/data.csv`, and add the following contents.

```sql
1,"DATA1","2012-05-20","14:30:25",123456
2,"DATA2","2012-05-21","15:30:25",234567
3,"DATA3","2012-05-22","16:30:25",345678
4,"DATA4","2012-05-23","17:30:25",456789
```

Execute the following command to import the data.

```sql
IMPORT FROM CSV FILE '/data/data.csv' INTO "MYTABLE"
   WITH RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ',';
```

**Example** - Importing by using a control file

Import the data from Example 1 using a control file you create (`/data/data.ctl`) that points to the CSV file. The control file contains the following commands:

```sql
IMPORT DATA INTO TABLE "MYTABLE" FROM '/data/data.csv'
   RECORD DELIMITED BY '\n'
FIELD DELIMITED BY ','
OPTIONALLY ENCLOSED BY '"'
ERROR LOG '/data/data.err';
```

Execute the following command to import the data using the control file: `IMPORT FROM CONTROL FILE '/ data/data.ctl';`

The fictitious example below imports data into the data statistics object `My_Schema.SKETCH5` using a control file (`/data/data.ctl`). The control file contains the following commands:

```sql
IMPORT DATA INTO STATISTICS "My_Schema"."SKETCH5" FROM '/data/data'
 ERROR LOG '/data/data.err';
```

Execute the following command to import the data using the control file: `IMPORT FROM CONTROL FILE '/ data/data.ctl';`.

**Example** - Importing by using date formats

In the example below, the date format is of the CSV import data is different from the default date format 'YYYY-MM-DD'. In this import data, the date format used is 'MM-DD-YYYY'. You create a CSV text file, `/data/ data_different_date.csv`, and add the following contents.

```sql
1,"DATA1","05-20-2012","14:30:25",123456
2,"DATA2","05-21-2012","15:30:25",234567
3,"DATA3","05-22-2012","16:30:25",345678
4,"DATA4","05-23-2012","17:30:25",456789
```

Execute the following command to import the data.

```sql
IMPORT FROM CSV FILE '/data/data_different_date.csv' INTO "MYTABLE" WITH RECORD
   DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   DATE FORMAT 'MM-DD-YYYY';
```

**Example** - Importing by using COLUMN LIST

Create a table called COLLIST to store the imported data.

```sql
CREATE ROW TABLE COLLIST ( A INT, B VARCHAR(10), C DATE, D DECIMAL );
```

Create a CSV text file `/data/data_col_list.csv` and add the following contents.

```sql
1,"DATA1","2012-05-20",123456
2,"DATA2","2012-05-21",234567
3,"DATA3","2012-05-22",345678
4,"DATA4","2012-05-23",456789
```

Execute the following commands to import the data using a column list.

```sql
IMPORT FROM CSV FILE '/data/data_col_list.csv' INTO "COLLIST"
   WITH RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   COLUMN LIST ("A", "B", "C", "D");
```

To import data without dealing with the proper table layout, it is possible to use WITH SCHEMA FLEXIBILITY as extended option of COLUMN LIST to import into a flexible table.

Create a flexible table to store the imported data as follows:

```sql
CREATE ROW TABLE FLEX ( X INT ) WITH SCHEMA FLEXIBILITY;
```

Execute the following commands to import previously created CSV file `data_col_list.csv` without explicitly adding columns.

```sql
IMPORT FROM CSV FILE '/data/data_col_list.csv' INTO "FLEX"
   WITH RECORD DELIMITED BY '\n'
   FIELD DELIMITED BY ','
   COLUMN LIST ("A", "B", "C", "D")
   WITH SCHEMA FLEXIBILITY;
```

## Related Information

EXPORT Statement (Data Import Export) [→](EXPORT-Statement-Data-Import-Export.md) IMPORT Statement (Data Import Export) [→](IMPORT-Statement-Data-Import-Export.md)
