# 4.9.1.188 SUBSTR_BEFORE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 342–343

Returns a substring from a specified string before the first occurrence of the specified pattern.

## Syntax

```sql
SUBSTR_BEFORE(<string>, <pattern>)
```

## Syntax Elements

**string** Specifies the string containing the substring. **pattern** Specifies the occurrence within the string that marks the place immediately after the returned substring.

## Description

Returns a substring from the specified string before the first occurrence of the specified pattern.

- If `<string>` does not contain the `<pattern>` substring, then an empty string is returned.
- If `<pattern>` is an empty string, then `<string>` is returned.
- If `<string>` or `<pattern>` is NULL, then NULL is returned.

## Example

The following example returns `Hello`, the part of the given string that is to the left of the first occurrence of `My`:

```sql
SELECT SUBSTR_BEFORE ('Hello My Friend','My') "substr before" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
