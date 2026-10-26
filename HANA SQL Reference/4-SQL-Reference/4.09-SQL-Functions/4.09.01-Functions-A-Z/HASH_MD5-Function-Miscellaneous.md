# 4.9.1.88 HASH_MD5 Function (Miscellaneous)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 198–199

Returns a 32 byte hash value of the concatenated arguments.

## Syntax

```sql
HASH_MD5(<argument> [,...])
```

## Syntax Elements

#### argument

Specifies a VARBINARY value.

```sql
<argument> ::= <string_literal>
```

## Description

Returns a 32 byte VARBINARY hash value of the concatenated arguments. The hash is calculated using a MD5 algorithm.

To ensure unique results from concatenated arguments, delimit the arguments with another string as shown in following the examples.

## Example

In the example below, the query generates a hash value based on the provided input:

```sql
SELECT HASH_MD5 (TO_BINARY('database')) "hash" FROM DUMMY;
```

The following examples, which both return `7AC66C0F148DE9519B8BD264312C4D64`, show how the function concatenates its arguments:

```sql
SELECT HASH_MD5(to_binary('abcd'), TO_BINARY('efg')) "test1" FROM DUMMY;
```

```sql
SELECT HASH_MD5(TO_BINARY('abc'), TO_BINARY('defg')) "test2" FROM DUMMY;
```

The following examples show how you can delimit the arguments with another string (in this case with 00) to ensure unique results from the concatenation. The first statement returns `6BB6BD45C57D57ECC69A9EB81F7409BE`, whereas the second statement returns `1CEDEB6EB7ED12D948F66593589FBD23`. Without the delimiter, both statements return the same value: `7AC66C0F148DE9519B8BD264312C4D64`.

```sql
SELECT HASH_MD5(TO_BINARY('abcd'), '00', TO_BINARY('efg')) "test1" FROM DUMMY;
```

```sql
SELECT HASH_MD5(TO_BINARY('abc'), '00', TO_BINARY('defg')) "test2" FROM DUMMY;
```
