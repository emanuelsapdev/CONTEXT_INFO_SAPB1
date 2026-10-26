# 4.9.1.98 IS_SQL_INJECTION_SAFE Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 208–209

Checks a specified SQL identifier for possible SQL injection risks.

## Syntax

```sql
IS_SQL_INJECTION_SAFE(<value>[, <max_tokens>])
```

## Syntax Elements

#### value

Specifies the string to be checked.

```sql
<value> ::= <string>
```

#### max_tokens

Specifies the maximum number of tokens expected in `<value>`. The default value is 1.

```sql
<max_tokens> ::= <integer>
```

## Description

Use this function to ensure a string contains the specified number of tokens and SQL comments before using it in an SQL statement. A 1 (safe) is returned when the actual number of tokens found does not exceed `<max_tokens>` and no comments were found; otherwise, a 0 is returned (not safe).

For the purposes of counting, SAP HANA interprets whitespaces and the following characters as separators between tokens:

```sql
, ( ) [ ] . ; : + - * / % ^ < >  =
```

## Example

The following query returns 0 (not safe) because two tokens were found and the default to check for was 1.

```sql
SELECT IS_SQL_INJECTION_SAFE('tab,le') "safe" FROM DUMMY;
```

The following query returns 1 (safe) because the number of tokens found did not exceed `<max_tokens>`:

```sql
SELECT IS_SQL_INJECTION_SAFE('CREATE STRUCTURED PRIVILEGE', 3) "safe" FROM DUMMY;
```

The following query returns 0 (not safe) because comments are not allowed.

```sql
SELECT IS_SQL_INJECTION_SAFE('mytab /*', 4) "safe" FROM DUMMY;
```
