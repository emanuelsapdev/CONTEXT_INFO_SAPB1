# 4.9.1.97 INITCAP Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 207–208

Converts the first character of each word in a specified string to uppercase and converts remaining characters to lowercase.

## Syntax

```sql
INITCAP(<inputString>)
```

## Syntax Elements

#### inputString

Specifies the string to be converted. `<inputString>` can be either a VARCHAR or NVARCHAR value.

```sql
<inputString> ::= <string>
```

## Description

A word is delimited by any of the following characters:

- Blank space
- New line
- Form feed
- Carriage return
- Line feed
- Any of the following: `` ! " # $ % & ' ( ) * + , − . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~ ``

## Example

The following query returns `The Example One`:

```sql
SELECT INITCAP('the EXAMPLE one') FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
