# 4.9.1.24 BINTOSTR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 112–113

Converts a VARBINARY string to a character string.

## Syntax

```sql
BINTOSTR(<varbinary_string>)
```

## Syntax Elements

**varbinary_string** The VARBINARY string to be converted to a character string.

## Description

Converts a VARBINARY string `<varbinary_string>` to a character string with CESU-8 encoding.

## Example

This example converts the VARBINARY string `416E74` to a CESU-8 encoded character string, and returns the value `Ant`:

```sql
SELECT BINTOSTR ('416E74') "bintostr" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
