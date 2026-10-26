# 4.9.1.179 SOUNDEX Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 331–332

Converts alphabet characters into a sound code that represents their sound.

## Syntax

```sql
SOUNDEX(<string>)
```

## Syntax Elements

**string** Specifies the string to be converted into sound code.

## Description

Use the SOUNDEX function to find names that sound the same but are spelled differently.

SOUNDEX returns a code consisting of one letter and three numbers. The letter is the first letter of the word, and the numbers represent the next three consonants of the word, other than H, W, and Y, which are ignored. Vowels are also ignored, unless they are the first letter of the string. Double letters are counted as one letter. If necessary, zeroes are added at the end to ensure a four-character code.

The following characters are ignored:

- Blank spaces
- New lines
- Form feeds
- Carriage returns
- Line feeds
- Any of the following: ! " # $ % & ' ( ) \* + , - . / : ; < = > ? @ [ ] ^ _ ` { | } ~

## Example

The following fictitious example returns two identical codes, `S530`, which represent the sound of each name:

```sql
SELECT SOUNDEX ('Smith'), SOUNDEX ('Smythe') FROM DUMMY;
```

This fictitious example searches MyTable.MyColumn for values that sound like Smith:

```sql
SELECT * FROM MyTable WHERE SOUNDEX(MyColumn) = SOUNDEX('SMITH');
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
