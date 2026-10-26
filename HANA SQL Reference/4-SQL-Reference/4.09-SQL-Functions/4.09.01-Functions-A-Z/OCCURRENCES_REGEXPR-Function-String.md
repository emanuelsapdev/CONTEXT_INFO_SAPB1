# 4.9.1.143 OCCURRENCES_REGEXPR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 273–274

Returns the number of matches of a regular expression search within a string.

## Syntax

```sql
OCCURRENCES_REGEXPR( <pattern> [ FLAG <flag> ] IN <regex_subject_string> [ FROM
<start_position> ] )
```

## Syntax Elements

#### pattern

Specifies a search pattern based on Perl Compatible Regular Expression (PCRE).

```sql
<pattern> ::= !!Perl Compatible Regular Expression
```

#### flag

Specifies the matching behavior of the function and can be defined by the flag literal.

```sql
<flag> ::= { 'i' | 'm' | 's' | 'x' }
```

| Flag options **Flag option** | **Description** |
| --- | --- |
| i | Enables case-insensitive matching |
| m | Enables multiline mode, where the `<subject_string>` will be treated as multiple lines and the expression ^ and $ match just after or just before, respectively, a line terminator or the end of the input sequence |
| s | Enables the expression `<.>` as a wildcard to match any character, including a line terminator |
| x | Permits whitespace and comments in the pattern |
| U | SAP HANA uses the Perl-compatible Regular Expressions (PCRE) library to process regular expressions. Specifying 'U' (short for "ungreedy") inverts the "greediness" of quantifiers so that they are not greedy by default but become greedy only when followed by "?". Ungreedy matching can often perform faster because it finds the shorter match at times when it is only interesting to know whether there is any match.<br>For a full understanding of the "greedy" versus "ungreedy" matching behavior of the Perl-compatible Regular Expressions (PCRE) library, visit:https://www.pcre.org/original/doc/html/pcre matching.html . |

#### regex_subject_string

Specifies the string to search within. If `<regex_subject_string>` is empty, then the result is empty.

```sql
<regex_subject_string> ::= <string>
```

#### start_position

Specifies a positive integer that indicates the character of `<regex_subject_string>` where the search is started. If `<start_position>` is not a positive integer, then -1 is returned.

```sql
<start_position> ::= <positive_integer>
```

## Description

Returns the number of matches of a regular expression search within a string.

## Example

The following example returns the number of occurrences of digits in the specified string, `'a1b2'`, and returns the value `2`:

```sql
SELECT OCCURRENCES_REGEXPR('([[:digit:]])' IN 'a1b2') "occurrences_regexpr" FROM
DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
