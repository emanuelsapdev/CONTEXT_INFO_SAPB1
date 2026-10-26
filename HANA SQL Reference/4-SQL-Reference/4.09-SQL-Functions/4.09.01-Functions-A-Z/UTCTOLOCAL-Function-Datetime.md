# 4.9.1.225 UTCTOLOCAL Function (Datetime)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 375–377

Converts the specified timestamp between UTC and local time.

## Syntax

```sql
UTCTOLOCAL (<time> [, <timezone> [, <timezone_dataset>]])
```

## Syntax Elements

#### time

Specifies a timestamp in UTC to be converted to local time.

```sql
<time> ::= <timestamp>
```

#### timezone

Specifies a string parameter holding the timezone defining the local time. If the local timezone is not explicitly specified, then the local timezone of the SAP HANA system is used.

```sql
<timezone> ::= <string_literal>
```

#### timezone_dataset

Specifies the dataset in which to search for the given timezone.

```sql
<timezone_dataset> ::= <string_literal>
```

Possible values of this string parameter are:

- `sap` searches in the dataset in the timezone definition tables. This is the default value. To use this value, import a timezone dataset (see SAP Note 1791342). If you use this value without importing a dataset, the function uses hardcoded fallback values. These fallback values are deprecated and will be removed in a future support package stack.
- `platform` searches in the dataset provided by the operating system.

## Description

Converts the UTC(GMT) time `<t>` to the local time in a timezone.

Use UTC times instead of local timestamps. The use of local times or conversion between local time zones might require additional handling in the application code.

## Examples

The following example returns the value `Dec 31, 2011 8:00:00.0 PM` as the local time equivalent (in EST) of the specified UTC time:

```sql
SELECT UTCTOLOCAL (TO_TIMESTAMP('2012-01-01 01:00:00', 'YYYY-MM-DD HH24:MI:SS'),
'EST') "utctolocal" FROM DUMMY;
```

The following example returns the value `Dec 31, 2011 8:00:00.0 PM` as the local time equivalent (in EST) of the specified UTC time:

```sql
 SELECT UTCTOLOCAL (TO_TIMESTAMP('2012-01-01 01:00:00', 'YYYY-MM-DD
HH24:MI:SS'), 'EST', 'sap') "utctolocal" FROM DUMMY;
```

## Related Information

Datetime Data Types [→](../../4.03-Data-Types/4.03.05-Datetime-Data-Types.md) SAP Note 1791342
