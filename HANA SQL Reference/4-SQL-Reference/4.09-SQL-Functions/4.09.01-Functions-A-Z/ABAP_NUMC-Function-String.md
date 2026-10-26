# 4.9.1.2 ABAP_NUMC Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 84–85

Converts an input string to a string of a specified length, that contains only digits.

## Syntax

```sql
ABAP_NUMC( <string>, <length> )
```

## Syntax Elements

**string** Specifies the input string to convert. **length** Specifies the length that the returned string should be.

## Description

String and numeric values are left-padded with 0s if `<string>` is shorter than `<length>`. If `<string>` is longer than `<length>`, then characters are truncated from the left.

Numeric values are rounded to their integer part and the sign is discarded.

TIMESTAMP, SECONDDATE, DATE, and TIME values are padded and truncated from the right side, as necessary.

DECIMAL and SMALLDECIMAL inputs are never truncated but create an overflow error if they are found to be too long.

## Example

The following example returns `012`.

```sql
SELECT ABAP_NUMC(12, 3) FROM DUMMY;
```

The following example returns `234`.

```sql
SELECT ABAP_NUMC(1234, 3) FROM DUMMY;
```

The following example returns `01230000000000000000`.

```sql
SELECT ABAP_NUMC(1.23e18, 20) FROM DUMMY;
```

The following example returns `001235`.

```sql
SELECT ABAP_NUMC(-1234.5, 6) FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
