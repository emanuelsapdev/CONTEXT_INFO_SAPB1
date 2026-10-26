# 4.9.1.29 BITSET Function (Numeric)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 117–118

Sets a specific number of bits to 1 in a target number from a specified 1-based index position.

## Syntax

```sql
BITSET(<target_num>, <start_bit>, <num_to_set>)
```

## Syntax Elements

#### target_num

The VARBINARY number where the bits are to be set.

```sql
<target_num> ::= <string_literal>
```

#### start_bit

A 1-based index position where the first bit is to be set.

```sql
<start_bit> ::= <unsigned_integer>
```

#### num_to_set

The number of bits to be set in the target number.

```sql
<num_to_set> ::= <unsigned_integer>
```

## Description

Sets `<num_to_set>` bits to 1 in `<target_num>` from the `<start_bit>` position.

## Example

The following example returns the value `E000` for `"bitset"`:

```sql
SELECT BITSET ('0000', 1, 3) "bitset" FROM DUMMY;
```

## Related Information

[Numeric Data Types](../../4.03-Data-Types/4.03.08-Numeric-Data-Types.md)
