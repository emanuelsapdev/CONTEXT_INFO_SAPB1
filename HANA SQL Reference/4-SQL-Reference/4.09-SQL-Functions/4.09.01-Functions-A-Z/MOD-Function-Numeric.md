# 4.9.1.128 MOD Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 258–259

Returns the remainder of a specified number divided by a specified divisor.

## Syntax

```sql
MOD(<number>, <divisor>)
```

## Description

Returns the remainder of a number `<number>` divided by a divisor `<divisor>`.

When `<number>` is negative, this function acts differently to the standard computational modulo operation. The following list shows examples of what the MOD function returns as the result:

- If `<divisor>` is zero, then `<number>` is returned.
- If `<number>` is greater than 0 and `<number>` is less than `<divisor>`, then `<number>` is returned.
- If `<number>` is less than 0 and `<number>` is greater than `<divisor>`, then `<number>` is returned.
- In cases other than those mentioned above, the remainder of the absolute value of `<number>` divided by the absolute value of `<divisor>` is used to calculate the remainder. If `<number>` is less than 0, then the returned remainder from MOD is a negative number, and if `<number>` is greater than 0, then the returned remainder from MOD is a positive number.

## Example

The following example returns the value `3`:

```sql
SELECT MOD (15, 4) "modulus" FROM DUMMY;
```

The following example returns the value `-3`:

```sql
SELECT MOD (-15, 4) "modulus" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
