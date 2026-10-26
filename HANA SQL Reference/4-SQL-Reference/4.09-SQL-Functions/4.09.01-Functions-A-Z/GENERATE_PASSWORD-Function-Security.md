# 4.9.1.83 GENERATE_PASSWORD Function (Security)

> [↑ 4.9.1 Alphabetical List Of Functions](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 191–192

Generates a password.

## Syntax

```sql
GENERATE_PASSWORD( <password_length> [, <usergroup_name>] )
```

## Syntax Elements

#### password_length

Specifies the length of the password to generate as an integer.

#### usergroup_name

Specifies a usergroup name. If there are password policy parameters defined for the usergroup, they are applied during password generation.

## Description

Generates and returns a password of type VARCHAR(128).

## Example

The following example returns a generated password of 16 characters::

```sql
SELECT GENERATE_PASSWORD(16) FROM Dummy;
```
