# 4.9.1.125 MIMETYPE Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 254–255

Returns the MIME type of a value in a column that has a fulltext index.

## Syntax

```sql
MIMETYPE(<column_name>)
```

## Syntax Elements

**column_name** Specifies the column values to test for the MIME type.

```sql
<column_name> ::= <identifier>
```

## Description

Returns the MIME type of the corresponding column value. This function requires a fulltext index on the input column.

## Example

The following example creates a table with two differing types of text content, plain text and HTML:

```sql
CREATE COLUMN TABLE T (CONTENT TEXT FAST PREPROCESS OFF);
 INSERT INTO T VALUES('This is an example');
 INSERT INTO T VALUES('<html>This is an example</html>');
```

Select the content and detect the MIME type of the entries:

```sql
SELECT MIMETYPE(CONTENT),CONTENT FROM T;
```

| **MIMETYPE(CONTENT)** | **CONTENT** |
| --- | --- |
| text/plain | This is an example |
| text/html | \<html>This is an example\</html> |
