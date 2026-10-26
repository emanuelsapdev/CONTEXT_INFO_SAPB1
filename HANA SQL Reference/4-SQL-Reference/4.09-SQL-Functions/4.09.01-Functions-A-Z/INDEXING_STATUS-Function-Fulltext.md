# 4.9.1.96 INDEXING_STATUS Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 206–207

Returns the indexing status of values in a column that has a fulltext index.

## Syntax

```sql
INDEXING_STATUS(<column_name>)
```

## Description

This function returns the indexing status of values in a column that has a fulltext index. Possible return values are:

- ERROR - the value could not be indexed due to a mismatch in the data type
- INDEXED - the value is been indexed
- QUEUED - the value is queued for indexing

You must have a fulltext index on `<column_name>` to use this function.

## Examples

```sql
DROP TABLE T;
CREATE COLUMN TABLE T (CONTENT VARCHAR(500));
CREATE FULLTEXT INDEX I on T(CONTENT) ASYNC MIME TYPE 'text/xml' FAST PREPROCESS
OFF;
INSERT INTO T VALUES ('This string cannot be indexed due to its formatting, so
its INDEXING_STATUS is ERROR');
INSERT INTO T VALUES ('<xml>This string was indexed, so its INDEXING_STATUS is
INDEXED</xml>');
-- Wait a couple of seconds
ALTER FULLTEXT INDEX I SUSPEND QUEUE;
INSERT INTO T VALUES ('<xml>This string is queued for indexing, so its
INDEXING_STATUS is QUEUED</xm>');
SELECT INDEXING_STATUS(CONTENT), CONTENT FROM T;The following statements create
a table, create a fulltext index on the table, and then
                suspend the index before inserting data into the table:
```

| **INDEXING_STATUS(CONTENT)** | **CONTENT** |
| --- | --- |
| ERROR | This string cannot not be indexed due to its formatting, so its INDEXING_STATUS is ERROR |
| INDEXED | \<xml>This string was indexed, so its INDEXING_STATUS is INDEXED\</xml> |
| QUEUED | \<xml>This string is queued for indexing, so its INDEXING_STATUS is QUEUED\</xml> |
