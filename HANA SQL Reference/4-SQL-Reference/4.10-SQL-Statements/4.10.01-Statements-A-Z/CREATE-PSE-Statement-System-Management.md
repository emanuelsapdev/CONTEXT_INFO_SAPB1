# 4.10.1.58 CREATE PSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 754–755

Creates a personal security environment (PSE) store.

## Syntax

```sql
CREATE PSE <pse_name>
```

## Syntax Elements

#### pse_name

Specifies a unique name for the PSE store to be created.

```sql
<pse_name> ::= <identifier>
```

## Description

Creates a personal security environment (PSE) store.

## Permissions

You must have the TRUST ADMIN privilege to execute this statement.

## Examples

Create a PSE store with the name `example_pse`.

```sql
CREATE PSE example_pse;
```

## Related Information

ALTER PSE Statement (System Management) [→](ALTER-PSE-Statement-System-Management.md) SET PSE Statement (System Management) [→](SET-PSE-Statement-System-Management.md)

[UNSET PSE Statement (System Management)](UNSET-PSE-Statement-System-Management.md)
