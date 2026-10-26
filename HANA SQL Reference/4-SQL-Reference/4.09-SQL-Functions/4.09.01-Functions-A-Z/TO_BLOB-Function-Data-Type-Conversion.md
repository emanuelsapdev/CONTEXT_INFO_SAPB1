# 4.9.1.198 TO_BLOB Function (Data Type Conversion)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 352–353

Converts a binary string or (N)CLOB data type to a BLOB data type.

## Syntax

```sql
TO_BLOB(<value>)
<value> ::= <binary string> | <nclob_value> | <clob_value>
```

## Description

Converts a BINARY, CLOB, or NCLOB `<value>` to a BLOB data type.

## Example

The following example converts the BINARY value `abcde` to the BLOB value `abcde`:

```sql
SELECT TO_BLOB (TO_BINARY('abcde')) "to blob" FROM DUMMY;
```

The following example converts the CLOB value `abc` to the BLOB value `abc`:

```sql
SELECT TO_BLOB (TO_CLOB('abc')) "to blob" FROM DUMMY;
```

## Related Information

[Data Type Conversion](../../4.03-Data-Types/4.03.04-Data-Type-Conversion.md)
