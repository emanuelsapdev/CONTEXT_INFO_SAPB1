# 4.10.1.97 DROP PSE Statement (System Management)

> [↑ 4.10.1 Alphabetical List of Statements](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 911–912

Drops a PSE store.

## Syntax

```sql
DROP PSE <pse_name>
```

## Syntax Elements

#### pse_name

Specifies the name of the PSE store to drop.

```sql
<pse_name> ::= <identifier>
```

## Description

Dropping of a PSE store fails if the PSE store is assigned to a purpose. Existing certificates remain in the Certificate Store.

When the owner of a PSE Store is dropped, their PSE Stores are dropped as well, even if they are assigned to a purpose. So for example, with SSL enforced, dropping a certain user may render the whole HDB unusable.

## Permissions

To use this statement, you must have the DROP privilege on the PSE Store object.

## Examples

Drop the PSE store `examplepse`.

```sql
DROP PSE examplepse;
```
