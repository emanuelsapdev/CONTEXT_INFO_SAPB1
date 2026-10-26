# 4.9.1.156 REPLACE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 291–292

Searches within a string for all occurrences of a specified string and replaces them with another specified string.

## Syntax

```sql
REPLACE(<original_string>, <search_string>, <replace_string>)
```

## Syntax Elements

#### original_string

Specifies the string to perform the search and replace within. If `<original_string>` is empty, then the result is an empty string.

#### search_string

Specifies the pattern to search for in `<original_string>`.

#### replace_string

Specifies the string to replace `<search_string>` with.

## Description

Searches in `<original_string>` for all occurrences of `<search_string>` and replaces them with `<replace_string>`.

- If two overlapping substrings match the `<search_string>` in the `<original_string>`, then only the first occurrence is replaced.
- If `<original_string>` does not contain an occurrence of `<search_string>`, then `<original_string>` is returned unchanged.
- If `<original_string>`, `<search_string>`, or `<replace_string>` are NULL, then NULL is returned.

## Example

The following example changes all occurrences of `DOWN` in the original string to `UP`, and returns the value `UPGRADE UPWARD`:

```sql
SELECT REPLACE ('DOWNGRADE DOWNWARD','DOWN', 'UP') "replace" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
