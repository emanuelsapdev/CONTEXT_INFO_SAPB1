# 4.9.1.208 TO_JSON_BOOLEAN (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 360–361

Converts a given `<value>` to a boolean value in JSON format.

## Syntax

```sql
TO_JSON_BOOLEAN(<value>)
```

## Description

If the `<value>` cannot be converted to a JSON boolean value, then an error is returned.

## Example

Create and populate the collection myCollection1:

```sql
CREATE COLLECTION myCollection1;
INSERT INTO myCollection1 VALUES ('{"k1" : true}');
```

Running the following statement returns an error:

```sql
SELECT * FROM myCollection1 WHERE "k1" = TRUE;
```

Running the following statement returns the record:

```sql
SELECT * FROM myCollection1 WHERE "k1" = TO_JSON_BOOLEAN(TRUE);
```
