# 4.9.1.115 LOCATE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 240–241

Returns the position of a substring within a string.

## Syntax

```sql
LOCATE( <haystack>, <needle>, [<start_position>] , [ <occurrences> ] )
```

## Description

The LOCATE function returns the position of a substring `<needle>` within a string `<haystack>`.

- If `<needle>` is not found within `<haystack>`, or if `<occurrences>` is set to less than 1, then 0 is returned.
- If `<haystack>`, `<needle>`, or `<occurences>` is (explicitly) NULL, then NULL is returned.
- If `<occurrences>` is not specified, then the first matched position is returned. A setting of 1 for `<occurrences>` is the same as not specifying it, while a setting of n returns the nth match (or 0 if there are no more matches found).
- If `<start_position>` is a positive integer, or 0, or not specified, then the matching direction proceeds from left to right.
- If `<start_position>` is negative, then matching starts at the end of `<haystack>` and proceeds in the reverse direction (right to left). For example:

| **Statement** | **Returns** |
| --- | --- |
| `SELECT LOCATE('AAA', 'A', -1) FROM "DUMMY";` | 3 - the position of the last A |
| `SELECT LOCATE('AAA', 'A', -2) FROM "DUMMY";` | 2 - the position of the second to last A |
| `SELECT LOCATE('AAA', 'A', -3) FROM "DUMMY";` | 1 - the position of the third to last A |
| `SELECT LOCATE('AAA', 'A', -4) FROM "DUMMY";` | 0 - not found |

- If a match is found, then the match position returned is always a positive number, even when `<start_position>` is a negative number.

## Examples

The following example returns `1` because `<needle>` is an empty string.

```sql
SELECT LOCATE ('length in char', '') "locate" FROM DUMMY;
```

The following example returns the starting position (`1`) of `length` in the string `length in char`:

```sql
SELECT LOCATE ('length in char', 'length') "locate" FROM DUMMY;
```

The following example returns `0` because the search pattern `zchar` cannot be found in the given string:

```sql
SELECT LOCATE ('length in char', 'zchar') "locate" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
