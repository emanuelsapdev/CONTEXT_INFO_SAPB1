# 4.9.1.116 LOCATE_REGEXPR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 241–243

Searches a string for a regular expression pattern and returns an integer indicating the beginning position, or the ending position plus 1, of one occurrence of the matched substring.

## Syntax

```sql
LOCATE_REGEXPR( [ <regex_position_start_or_after> ] <pattern>
   [  FLAG <flag> ]
   IN <regex_subject_string>
   [ FROM <start_position> ]
   [ OCCURRENCE <regex_occurrence> ]
   [ GROUP <regex_capture_group> ]
)
```

## Syntax Elements

#### regex_position_start_or_after

Searches a string for a regular expression pattern and returns an integer indicating the beginning position, or the ending position plus 1, of one occurrence of the matched substring.

```sql
<regex_position_start_or_after> ::= START | AFTER
```

If `<regex_position_start_or_after>` is not specified, then START is implicit.

#### pattern

A search pattern based on Perl Compatible Regular Expression (PCRE).

#### flag

The matching behavior of the function can be defined by the `<flag>` literal. The following options are available:

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

```sql
<regex_subject_string> ::= <string>
```

Specifies a string in which to search for the regular expression pattern.

#### start_position

The `<start_position>` parameter is a positive integer and indicates the character of `<regex_subject_string>` where the search is started. If `<start_position>` is not a positive integer, then 0 is returned.

```sql
<start_position> ::= <positive_integer>
```

**regex_occurrence** Specifies a positive integer to the occurrence of the `<pattern>` in `<regex_subject_string>`. The default is 1.

```sql
<regex_occurrence> ::= <integer>
```

If `<regex_occurrence>` is not a positive integer, then 0 is returned.

#### regex_capture_group

The `<regex_capture_group>` parameter is a non-negative integer and indicates the number of the captured substring's group by the regular expression. The default is 0.

```sql
<regex_capture_group> ::= <integer>
```

If `<regex_capture_group>` is a negative integer, then 0 is returned.

## Description

Searches a string for a regular expression pattern and returns an integer indicating the beginning position, or the ending position plus 1, of one occurrence of the matched substring.

If any of the following parameters is `NULL`: `<pattern>`, `<flag>`, `<regex_subject_string>`, , `<start_position>`, `<regex_occurrence>` or `<regex_capture_group>`, then the function returns NULL.

## Example

This example returns the start position of the day part from the date value 20140401; it returns 7:

```sql
SELECT LOCATE_REGEXPR(START '([[:digit:]]{4})([[:digit:]]{2})([[:digit:]]{2})'
IN '20140401' GROUP 3) "locate_regexpr" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
