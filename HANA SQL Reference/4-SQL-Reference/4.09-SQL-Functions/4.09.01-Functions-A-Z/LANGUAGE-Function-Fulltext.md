# 4.9.1.104 LANGUAGE Function (Fulltext)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 226–227

Returns the language of the specified column entries.

## Syntax

```sql
LANGUAGE(<column_name>)
```

## Description

`<column_name>` is the column where the language detection occurs.

You must have an existing fulltext index for the specified column.

## Example

Create a table with two detectable languages, English and German, and populate it with some entries.

```sql
CREATE COLUMN TABLE T (CONTENT TEXT FAST PREPROCESS OFF LANGUAGE
DETECTION('EN','DE'));
 INSERT INTO T VALUES('This is a very short example.');
 INSERT INTO T VALUES('Dies ist ein ganz kurzes Beispiel.');
```

Execute the following query to select the content and detect the language of the entries.

```sql
SELECT LANGUAGE(CONTENT),CONTENT FROM T;
```

The query returns the language of each column:

| **LANGUAGE(CONTENT)** | **CONTENT** |
| --- | --- |
| en | `This is a very short example.` |
| de | `Dies ist ein ganz kurzes Beispiel.` |
