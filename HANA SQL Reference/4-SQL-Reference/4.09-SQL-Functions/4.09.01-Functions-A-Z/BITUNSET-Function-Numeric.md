# 4.9.1.30 BITUNSET Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 118–119

Sets a specified number of bits to 0 in a target number from a specified 1-based index position.

## Syntax

```sql
BITUNSET(<target_num>, <start_bit>, <num_to_unset>)
```

## Syntax Elements

#### target_num

The VARBINARY number where the bits are to be unset.

```sql
<target_num> ::= <string_literal>
```

#### start_bit

A 1-based index position where the first bit is to be unset.

```sql
<start_bit> ::= <unsigned_integer>
```

#### num_to_set

The number of bits to be unset in the target number.

```sql
<num_to_set> ::= <unsigned_integer>
```

## Description

Sets `<num_to_unset>` bits to 0 in `<target_num>` from the `<start_bit>` position.

## Example

The following example returns the value `1FFF` for `"bitunset"`:

```sql
SELECT BITUNSET ('ffff', 1, 3) "bitunset" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
