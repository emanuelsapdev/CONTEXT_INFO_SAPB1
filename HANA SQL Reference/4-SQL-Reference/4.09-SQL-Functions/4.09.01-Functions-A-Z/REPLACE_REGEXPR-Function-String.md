# 4.9.1.157 REPLACE_REGEXPR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 292–294

Searches a string for a regular expression pattern and returns the string with either one or every occurrence of the regular expression pattern that is replaced using a replacement string.

## Syntax

```sql
REPLACE_REGEXPR(<pattern> [ FLAG <flag> ]
 IN <regex_subject_string>
 [ WITH <replacement_string> ]
 [ FROM <start_position> ]
 [ OCCURRENCE <regex_replace_occurrence> ])
```

## Syntax Elements

#### pattern

Specifies a search pattern based on Perl Compatible Regular Expression (PCRE).

```sql
<pattern> ::= !!Perl Compatible Regular Expression
```

#### flag

Specifies the matching behavior to use.

```sql
<flag> ::= 'i' | 'm' | 's' | 'x'
```

| Flag options **Flag option** | **Description** |
| --- | --- |
| i | Enables case-insensitive matching |
| m | Enables multiline mode, where the `<subject_string>` will be treated as multiple lines and the expression ^ and $ match just after or just before, respectively, a line terminator or the end of the input sequence |
| s | Enables the expression `<.>` as a wildcard to match any character, including a line terminator |
| x | Permits whitespace and comments in the pattern |
| U | SAP HANA uses the Perl-compatible Regular Expressions (PCRE) library to process regular expressions. Specifying 'U' (short for "ungreedy") inverts the "greediness" of quantifiers so that they are not greedy by default but become greedy only when followed by "?". Ungreedy matching can often perform faster because it finds the shorter match at times when it is only interesting to know whether there is any match.<br>For a full understanding of the "greedy" versus "ungreedy" matching behavior of the Perl-compatible Regular Expressions (PCRE) library, visit:https://www.pcre.org/original/doc/html/pcre matching.html . |

#### regex_subject_string

Specifies the string that the search pattern should be applied to. If `<regex_subject_string>` is empty, the result is empty.

```sql
<regex_subject_string> ::= <string_literal>
```

#### replacement_string

Specifies the string that replaces all occurrences found by the function. The default is an empty string.

```sql
<replacement_string> ::= <string_literal>
```

#### start_position

Specifies the character of `<regex_subject_string>` where the search is started, if the value is a positive integer. Otherwise, NULL is returned.

```sql
<start_position> ::= <numeric_literal>
```

#### regex_replace_occurrence

Specifies a non-negative integer or ALL, and indicates the occurrence of the replace operation. If `<regex_replace_occurrence>` is a negative integer, then the `<regex_subject_string>` is returned without any change. The default value is ALL.

```sql
<regex_replace_occurrence> ::= <numeric_literal> | ALL
```

## Description

Searches a string for a regular expression pattern and returns the string with either one or every occurrence of the regular expression pattern that is replaced using a replacement string.

If any of the following parameters is NULL, then the function returns NULL: `<pattern>`, `<flag>`, `<regex subject_string>`, `<replacement_string>`, `<start_position>` or `<regex_replace_occurrence>`.

## Example

The following example uses a regular expression to replace date format `2014-04-01` with the value `01/04/2014`:

```sql
SELECT REPLACE_REGEXPR('([[:digit:]]{4})-([[:digit:]]{2})-([[:digit:]]{2})' IN
'2014-04-01'
WITH '\3/\2/\1' OCCURRENCE ALL) "replace_regexpr" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
