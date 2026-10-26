# 4.9.1.190 SUBSTRING Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 345–346

Returns a substring from an input value, starting from a specified position within the input value.

## Syntax

```sql
SUBSTRING(<string>, <start_position> [, <string_length>])
```

## Syntax Elements

**string** Specifies the string containing the substring. `<string>` can also be a binary type BLOB or VARBINARY. **start_position** Specifies where the substring starts within the string. **string_length** Specifies the substring length.

## Description

Returns a substring from the specified string starting from `<start_position>` within the string. SUBSTRING can return the remaining part of a string from the `<start_position>`, or optionally, a number of characters set by the `<string_length>` parameter.

- If `<start_position>` is less than 1, then it is considered to be 1.
- If `<string_length>` is less than 1, then an empty string is returned.
- If `<string_length>` is greater than the length of remaining part of `<str>`, then the remaining part is returned without blank padding.

When used on binary types, SUBSTRING factors in byte length and interprets the offsets, `<start_position>` and `<string_length>`, as byte positions.

## Example

The following example selects two characters from the string `1234567890` starting at position `4`, and returns the value `45`:

```sql
SELECT SUBSTRING ('1234567890',4,2) "substring" FROM DUMMY;
```

The following example returns `'ABCD'` from the binary value `x'ABCDEF'`:

```sql
SELECT SUBSTRING(x'ABCDEF',1,2) "substring" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
