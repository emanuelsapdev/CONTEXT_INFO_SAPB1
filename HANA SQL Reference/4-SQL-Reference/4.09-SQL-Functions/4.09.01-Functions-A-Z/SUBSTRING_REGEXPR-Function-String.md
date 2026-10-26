# 4.9.1.189 SUBSTRING_REGEXPR Function (String)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 343–345

Searches a string for a regular expression pattern and returns one occurrence of the matching substring.

## Syntax

```sql
SUBSTR[ING]_REGEXPR( <pattern> [ FLAG <flag> ] IN <regex_subject_string>
 [ FROM <start_position> ]
 [ OCCURRENCE <regex_occurrence> ]
 [ GROUP <regex_capture_group> ] )
```

## Syntax Elements

**pattern** Specifies a search pattern based on Perl Compatible Regular Expression (PCRE).

```sql
<pattern> ::= !!Perl Compatible Regular Expression
```

**flag** Specifies that the matching behavior of the function can be defined by the flag literal. The following options are available:

| Flag options **Flag option** | **Description** |
| --- | --- |
| i | Enables case-insensitive matching |
| m | Enables multiline mode, where the `<subject_string>` will be treated as multiple lines and the expression ^ and $ match just after or just before, respectively, a line terminator or the end of the input sequence |
| s | Enables the expression `<.>` as a wildcard to match any character, including a line terminator |

| **Flag option** | **Description** |
| --- | --- |
| x | Permits whitespace and comments in the pattern |
| U | SAP HANA uses the Perl-compatible Regular Expressions (PCRE) library to process regular expressions. Specifying 'U' (short for "ungreedy") inverts the "greediness" of quantifiers so that they are not greedy by default but become greedy only when followed by "?". Ungreedy matching can often perform faster because it finds the shorter match at times when it is only interesting to know whether there is any match.<br>For a full understanding of the "greedy" versus "ungreedy" matching behavior of the Perl-compatible Regular Expressions (PCRE) library, visit:https://www.pcre.org/original/doc/html/pcre matching.html . |

```sql
<flag> ::= 'i' | 'm' | 's' | 'x'
```

**regex_subject_string** Defines the string that the search pattern should be applied to. If `<regex_subject_string>` is empty, then the result is empty.

```sql
<regex_subject_string> ::= <string>
```

**start_position** Setting this parameter to a positive integer indicates which character of `<regex_subject_string>` the search begins at. If `<start_position>` is not a positive integer, then NULL is returned.

```sql
<start_position> ::= <numeric_literal>
```

**regex_occurrence** Setting this parameter to a positive integer indicates the occurrence of the `<pattern>` in `<regex_subject_string>`. The default is 1 and returns the first occurrence. If `<regex_occurrence>` is not a positive integer, then NULL is returned.

```sql
<regex_occurrence> ::= <numeric_literal >
```

**regex_capture_group** Indicates the number of the captured substring's group by the regular expression. The default is 0. If `<regex_capture_group>` is a negative integer, then 0 is returned.

```sql
<regex_capture_group> ::= <integer>
```

## Description

Searches a string for a regular expression pattern and returns one occurrence of the matching substring.

If any of the following parameters is NULL, then the function returns NULL: `<pattern>`, `<flag>`, `<regex_subject_string>`, `<start_position>`, `<regex_occurrence>`, or `<regex_capture_group>`.

## Example

The following example returns the day `01` from the date value `20140401`:

```sql
SELECT SUBSTR_REGEXPR('([[:digit:]]{4})([[:digit:]]{2})([[:digit:]]{2})' IN
'20140401' GROUP 3) "substring_regexpr" FROM DUMMY;
```

## Related Information

[Character String Data Types](../../4.03-Data-Types/4.03.03-Character-String-Data-Types.md)
