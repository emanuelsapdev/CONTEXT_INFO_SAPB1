# 4.10.1.19.28 ALTER SYSTEM CREATE RUNTIMEDUMP Statement (System Management)

> [↑ 4.10.1.19 ALTER SYSTEM ... (All ALTER SYSTEM Statements)](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 513–515

Creates a runtimedump (RTE) dump file containing information about specific sections and profiles.

## Syntax

```sql
ALTER SYSTEM CREATE RUNTIMEDUMP [ AT [ LOCATION ] <location_ref> ]
    [ { SECTION <section_ref> | PROFILE <profile_name> } ] [ INTO FILE
'<file_name>' ]
<profile_name> ::= <string_literal>
<file_name> ::= <string_literal>
```

## Syntax Elements

#### location_ref

Specifies the location of the service.

```sql
<location_ref> ::= '<host>:<port>'
```

If no location is specified, then the trace folder of the specified service is used.

#### SECTION

Specifies one of the section names defined in the runtimedump section in the `global.ini` file.

```sql
<section_ref> ::= ( '<section_name>' [, '<section_name>' , ... ]
<section_name> ::= <string_literal>
```

If no section is specified, then all sections are written.

#### PROFILE

Specifies the named subset of sections defined in the runtimedump section in the `global.ini` file.

#### INTO FILE

Specifies the name for the dump file. If a file name is not specified, then the default file name `<servicename>_<hostname>.<port>.rtedump.<YYYYMMDD-HHMMSS>.<pid>.trc` is used.

## Permissions

You need the RESOURCE_ADMIN system privilege.

## Description

This syntax lets you create an RTE dump file containing information about specific sections and profiles.

## Examples

Writes information relating to the STACK_SHORT section only to a file named `my_rte_dump.trc` on myhost, port 30003.

```sql
ALTER SYSTEM CREATE RUNTIMEDUMP AT LOCATION 'myhost:30003' SECTIONS
('STACK_SHORT') INTO FILE 'my_rte_dump.trc';
```

Writes information relating to all sections defined by the profile named myRTEProfile on the connected service to the file named `my_rte_dump.trc`.

```sql
ALTER SYSTEM CREATE RUNTIMEDUMP PROFILE 'myRTEProfile' INTO FILE
'my_rte_dump.trc';
```
