# 4.9.1.94 INDEXING_ERROR_CODE Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 204–205

Returns the indexing error codes for values in a column that has a fulltext index on it.

## Syntax

```sql
INDEXING_ERROR_CODE(<column_name>)
```

## Syntax Elements

#### column_name

Specifies the column to return the indexing error codes for.

```sql
<column_name> ::= <identifier>
```

## Description

You must have a fulltext index on `<column_name>`.

## Examples

The following statements create a table, build a fulltext index on it, insert some data, and then return the indexing error codes for the entries in the table.

```sql
DROP TABLE T;
CREATE COLUMN TABLE T (CONTENT varchar(50));
CREATE FULLTEXT INDEX I ON T(CONTENT) ASYNC MIME TYPE 'text/xml' FAST PREPROCESS
OFF;
INSERT INTO T VALUES ('This is an example');
INSERT INTO T VALUES ('<xml>This is an example</xml>');
–- Wait a few seconds
SELECT INDEXING_ERROR_CODE(CONTENT),CONTENT FROM T;
```

| **INDEXING_ERROR_CODE(CONTENT)** | **CONTENT** |
| --- | --- |
| 5122 | This is an example. |
| 0 | \<xml>This is an example.\</xml> |
