# 4.10.1.118 EXPORT INTO Statement (Data Import Export)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 950–952

Exports a table or view into a single CSV file.

## Syntax

```sql
EXPORT INTO <file_path> FROM <table_or_view_name>
 [ WITH <export_into_option_list> ]
```

## Syntax Elements

#### file_path

Specifies the complete path to the CSV file.

```sql
<file_path> ::= <string_literal>
```

#### table_or_view_name

Specifies the name of the table or view to be exported.

```sql
<table_or_view_object_name> ::= [ <schema_name>.]<identifier>
```

#### export_into_option_list

Specifies a list of options that control export behavior.

```sql
<export_into_option_list> ::= <export_into_option> [ <export_into_option>
[…] ]
<export_into_option> ::=
 THREADS <number_of_threads>
  | COLUMN LIST IN FIRST ROW
  | RECORD DELIMITED BY <string_for_record_delimiter>
  | FIELD DELIMITED BY <string_for_field_delimiter>
  | OPTIONALLY ENCLOSED BY <character_for_optional_enclosure>
  | ESCAPE <escape_character>
```

##### THREADS number_of_threads

Specifies the number of threads that can be used the export. The default value is the smaller of: 10 or the number of CPU cores.

```sql
THREADS <number_of_threads>
<number_of_threads> ::= <unsigned_integer>
```

##### COLUMN LIST IN FIRST ROW

Indicates that the column list is stored in the first row of the CSV import file.

##### RECORD DELIMITED BY string_for_record_delimiter

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

##### escape_character

Specifies the escape character used in the import data.

```sql
<escape_character> ::= <character_literal>
```

## Description

Use the EXPORT INTO statement to export the data from a table or view into a single CSV file.

The EXPORT INTO command does not support parameterized views.

## Examples

The following example creates a table and view, populates them, and exports each of them to a separate CSV file.

```sql
CREATE TABLE t (a INT, b NVARCHAR(50));
INSERT INTO t VALUES (0, 'test!@#$%');
CREATE VIEW v AS SELECT * FROM t;
EXPORT INTO '/tmp/view_content.csv' FROM v;
EXPORT INTO '/tmp/table_with_header.csv' FROM t WITH COLUMN LIST IN FIRST ROW
FIELD DELIMITED BY '!' ESCAPE '@';
```
