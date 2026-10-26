# 4.9.1.77 ESCAPE_SINGLE_QUOTES Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 185–186

Escapes single quotes in the specified string.

## Syntax

```sql
ESCAPE_SINGLE_QUOTES(<value>)
```

## Description

Escapes single quotes (apostrophes) in the given string `<value>`, ensuring a valid SQL string literal is used in dynamic SQL statements to prevent SQL injections. Returns the input string with escaped single quotes.

## Examples

The following query escapes the parameter content `Str'ing` to `Str''ing`.

```sql
SELECT ESCAPE_SINGLE_QUOTES('Str''ing') "string_literal" FROM DUMMY;
```

The following query example shows the strings retrieved from a table `t`, both without and with ESCAPE_SINGLE_QUOTES applied. The column `col_txt` contains the two entries `Adam's` and `Eve`.

```sql
CREATE COLUMN TABLE txt(
col_txt NVARCHAR(5000) NOT NULL);
INSERT INTO txt VALUES ('Adam''s');
INSERT INTO txt VALUES ('Eve');
SELECT col_txt, escape_single_quotes(col_txt) FROM txt;
```

The results are as follows:

| **COL_TXT** | **ESCAPE_SINGLE_QUOTES(COL_TXT)** |
| --- | --- |
| Adam's | Adam''s |
| Eve | Eve |
