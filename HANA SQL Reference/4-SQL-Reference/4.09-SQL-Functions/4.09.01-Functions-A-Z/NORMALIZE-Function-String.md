# 4.9.1.137 NORMALIZE Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 265–267

Applies a normalizing format to a character value expression and returns a normalized string.

## Syntax

```sql
NORMALIZE( <character_value_expression> [ , <normalized_format> ] )
```

## Syntax Elements

#### character_value_expression

Specifies the VARCHAR or NVARCHAR string to normalize.

#### normalized_format

Specifies the encoding format to use for the result. The default format is NFC.

```sql
<normalized_format> ::=
 NFC
 | NFD
 | NFKC
 | NFKD
```

The four Unicode normalization forms are as follows:

| **Form** | **Description** |
| --- | --- |
| Normalization Form D (NFD) | Specifies canonical decomposition. |
| Normalization Form C (NFC) | Specifies canonical decomposition followed by canonical composition. |
| Normalization Form KD (NFKD) | Specifies compatibility decomposition. |
| Normalization Form KC (NFKC) | Specifies compatibility decomposition followed by canonical composition. |

## Description

The Unicode standard defines two formal types, which are canonically and compatibility equivalent to the same characters by four normalization forms. The Unicode normalization algorithm puts all combined marks in a specified order. Decomposition only or decomposition followed by the composition rule is applied to transform each string. The details can be found from the following Unicode Standard Annex #15: http:// www.unicode.org/reports/tr15/

## Example

The examples in this section use the NORMALIZE function to return the normalized equivalent of `<character_value_expression>` based on the `<normalized_format>` form.

The following is an example of canonical equivalence:

| **Statement** | **Result** |
| --- | --- |
| `SELECT NORMALIZE('Å') FROM DUMMY;` | Å (0x00C5) |
| `SELECT NORMALIZE('A °') FROM DUMMY;` | Å |
| `SELECT NORMALIZE('Å', 'NFC') FROM DUMMY;` | Å (0x00C5) |
| `SELECT NORMALIZE('Å', 'NFD') FROM DUMMY;` | A °(0x0041 0x030A) |
| `SELECT NORMALIZE('A °', 'NFC') FROM DUMMY;` | Å (0x00C5) |
| `SELECT NORMALIZE('A °', 'NFD') FROM DUMMY;` | A °(0x0041 0x030A) |

> **Note**
>
> The example is illustrative and does not work as shown with copy and paste.

The following is an example of compatibility equivalence:

| **Statement** | **Result** |
| --- | --- |
| `SELECT NORMALIZE('ﻉ', 'NFKC') FROM DUMMY;` | ﻉ (positional variants) |
| `SELECT NORMALIZE ('ﻊ', 'NFKC') FROM DUMMY;` | ﻉ (positional variants) |
| `SELECT NORMALIZE('`①`', 'NFKC') FROM` `DUMMY;` | 1 (circled variants) |
| `SELECT NORMALIZE('`ｶ`', 'NFKC') FROM` `DUMMY;` | カ (width variants) |
| `SELECT NORMALIZE('¼', 'NFKC') FROM DUMMY;` | 1/4 (fractions) |
| `SELECT NORMALIZE('i`⁹`', 'NFD') FROM` `DUMMY;` | i9 (superscripts/subscripts) |

## Related Information

[Expressions](../../4.06-Expressions.md)
