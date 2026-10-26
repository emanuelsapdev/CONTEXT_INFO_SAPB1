# 4.9.1.147 PLAINTEXT Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 280–281

Returns the plain text representation of a value in a column that has a full text index.

## Syntax

```sql
PLAINTEXT(<column_name>)
```

## Syntax Elements

#### column_name

Specifies the identifier for a column that has a full text index on it.

## Description

The PLAINTEXT function returns the plain text representation of a value in a column that has a full text index. Use this function when you have binary data, such as a PDF, as a column value.

If the specified column does not have a full text index on it, then an error is returned.

## Example

The following example runs the PLAINTEXT function on a fictitious column value `<somePDF>` (a PDF) and returns the plain text representation of the value, `This is an example;<somePDF>`:

```sql
CREATE COLUMN TABLE T (CONTENT BLOB);
CREATE FULLTEXT INDEX I ON T(CONTENT);
INSERT INTO T VALUES (<somePDF>);
SELECT PLAINTEXT(CONTENT),CONTENT FROM T;
```
