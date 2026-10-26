# 4.9.1.38 CONCAT_NAZ Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 126–127

Returns a combined, non-null value string consisting of two specified strings.

## Syntax

```sql
CONCAT_NAZ(<string1>, <string2>)
```

## Syntax Elements

**string1** Specifies the first string to combine. **string2** Specifies the second string to combine.

## Description

Returns a combined value string consisting of `<string1>` followed by `<string2>`. If one value is NULL, the other value is returned. If both values are NULL, NULL is returned.

The maximum length of the concatenated string is 8,388,607. If the string length is longer than the maximum length, then an exception is thrown. Exceptionally, an implicit truncation is performed when converting an (N)CLOB typed value with a size greater than the maximum length of an (N)VARCHAR typed value.

## Example

The following example returns the AB:

```sql
SELECT CONCAT_NAZ ('A', 'B') "concat" FROM DUMMY;
```

| **concat** |
| --- |
| AB |

The following example returns C:

```sql
SELECT CONCAT_NAZ ('C', null) "concat" FROM DUMMY;
```

| **concat** |
| --- |
| C |

The following example returns the NULL value:

```sql
SELECT CONCAT_NAZ (null, null) "concat" FROM DUMMY;
```

| **concat** |
| --- |
| NULL |

## Related Information

Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md) Character String Data Types [→](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
