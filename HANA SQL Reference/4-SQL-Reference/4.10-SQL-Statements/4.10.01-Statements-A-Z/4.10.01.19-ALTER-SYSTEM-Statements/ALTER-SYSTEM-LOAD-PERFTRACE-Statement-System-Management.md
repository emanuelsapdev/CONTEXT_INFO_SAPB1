# 4.10.1.19.32 ALTER SYSTEM LOAD PERFTRACE Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 518–519

Converts a `.tpt` file into tables.

## Syntax

```sql
ALTER SYSTEM LOAD PERFTRACE [FILE <file_name>]
   INTO TABLES <table_prefix> [WITH REPLACE]
```

## Syntax Elements

#### FILE file_name

Specifies the file that raw performance data is loaded from.

```sql
<file_name> ::= <string_literal>
```

#### INTO TABLES table_prefix

Specifies the table prefix to be used with optional schema name.

> **Note**
>
> The created tables are only to used in conjunction with SAP tools or support personnel; the format of the tables is intentionally not documented for end users.

```sql
<table_prefix> ::= [ <schema_name>. ]<identifier>

<schema_name> ::= <unicode_name>
```

#### WITH REPLACE

Specifies that previously existing tables are removed. If the REPLACE option is not specified, then an error is thrown if tables with the specified prefix already exist.

## Description

Tables beginning with `<table_prefix>`_PERFTRACE_... are created and filled with the content from the `.tpt` file. The `.tpt` file is loaded from the trace directory of your SAP HANA database instance. If you do not specify a file name, then `perftrace.tpt` is used.

## Example

Load performance trace data from the `mytrace.tpt` file into tables. The created tables include MYTRACE_PERFTRACE_INFO MYTRACE_PERFTRACE_SERVICES, and MYTRACE_PERFTRACE_CALLS.

```sql
ALTER SYSTEM LOAD PERFTRACE FILE 'mytrace.tpt' INTO TABLES mytrace WITH REPLACE;
```
