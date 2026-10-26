# 4.9.1.95 INDEXING_ERROR_MESSAGE Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 205–206

Returns the indexing error messages for values in a column that has a fulltext index on it.

## Syntax

```sql
INDEXING_ERROR_MESSAGE(<column_name>)
```

## Syntax Elements

#### column_name

Specifies the column to return indexing error messages from.

```sql
<column_name> ::= <identifier>
```

## Description

The INDEXING_ERROR_MESSAGE function returns the indexing error message for entries in `<column_name>`. You must have a fulltext index on `<column_name>`.

## Examples

The following statements create a table, create a fulltext index on the table, insert data into the table, and then return the indexing errors for the entries:

```sql
CREATE COLUMN TABLE T (CONTENT VARCHAR(50));
 CREATE FULLTEXT INDEX I ON T(CONTENT) ASYNC MIME TYPE 'text/xml' FAST
PREPROCESS OFF;
 INSERT INTO T VALUES ('This is an example');
 INSERT INTO T VALUES ('<xml>This is an example</xml>');
SELECT INDEXING_ERROR_MESSAGE(CONTENT) "error messsge", CONTENT FROM T;
```

| **error message** | **CONTENT** |
| --- | --- |
| Xerces parser error | This is an example. |
| No error | \<xml>This is an example.\</xml> |
